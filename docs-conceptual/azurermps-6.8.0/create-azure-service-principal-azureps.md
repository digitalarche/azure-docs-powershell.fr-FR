---
title: Créer un principal du service Azure avec Azure PowerShell
description: Découvrez comment créer un principal du service pour votre application ou service avec Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 76d690f3a7206857861e1ee26d8284de419dc70a
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117574"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Créer un principal du service Azure avec Azure PowerShell

Si vous prévoyez de gérer votre application ou service avec Azure PowerShell, vous devez l’exécuter avec un principal du service Azure Active Directory (AAD) plutôt qu’avec vos informations d’identification personnelles. Cette rubrique vous explique pas à pas comment créer un principal de sécurité avec Azure PowerShell.

> [!NOTE]
> Vous pouvez également créer un principal du service par l’intermédiaire du portail Azure. Pour plus d’informations, consultez [Utiliser le portail pour créer une application et un principal du service Active Directory pouvant accéder aux ressources](/azure/azure-resource-manager/resource-group-create-service-principal-portal).

## <a name="what-is-a-service-principal"></a>Qu’est-ce qu’un « principal du service » ?

Un principal du service Azure est une identité de sécurité utilisée par les applications, les services et les outils d’automatisation créés par l’utilisateur pour accéder à des ressources Azure spécifiques. Il équivaut un peu à une identité d’utilisateur (nom d’utilisateur et mot de passe ou certificat) avec un rôle spécifique et des autorisations étroitement contrôlées. Il doit pouvoir effectuer uniquement des opérations spécifiques, contrairement à une identité d’utilisateur. Il améliore la sécurité si vous lui octroyez seulement le niveau d’autorisation minimal nécessaire pour effectuer ses tâches de gestion.

## <a name="verify-your-own-permission-level"></a>Vérifier votre propre niveau d’autorisation

Tout d’abord, vous devez avoir les autorisations suffisantes dans votre annuaire Azure Active Directory et votre abonnement Azure. Plus précisément, vous devez pouvoir créer une application dans l’annuaire Active Directory et affecter un rôle au principal du service.

Le moyen le plus simple pour vérifier que votre compte dispose des autorisations adéquates est d’utiliser le portail. Consultez [Vérifier l’autorisation requise dans le portail](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Créer un principal du service pour votre application

Une fois que vous êtes connecté à votre compte Azure, vous pouvez créer le principal du service. Vous devez identifier votre application déployée par l’une des informations suivantes :

* Le nom unique de votre application déployée (par exemple, « MyDemoWebApp » dans les exemples suivants)
* L’ID de l’application, le GUID unique associé à votre application, service ou objet déployé

### <a name="get-information-about-your-application"></a>Obtenir des informations sur votre application

Vous pouvez utiliser l’applet de commande `Get-AzureRmADApplication` pour obtenir des informations sur votre application.

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Créer un principal du service pour votre application

Utilisez l’applet de commande `New-AzureRmADServicePrincipal` pour créer le principal du service.

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Obtenir des informations sur le principal du service

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Se connecter en tant que principal du service

Vous pouvez maintenant vous connecter en tant que nouveau principal du service pour votre application en utilisant les valeurs *appId* et *password* que vous avez fournies. Vous devez fournir l’ID de locataire (TenantId) pour votre compte. Cet ID s’affiche quand vous vous connectez à Azure avec vos informations d’identification personnelles.

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Exécutez cette commande à partir d’une nouvelle session PowerShell. Une fois que vous êtes connecté, vous voyez un message similaire à celui-ci :

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Félicitations ! Vous pouvez utiliser ces informations d’identification pour exécuter votre application. Ensuite, modifiez les autorisations du principal du service.

## <a name="managing-roles"></a>Gestion des rôles

> [!NOTE]
> Le contrôle d’accès en fonction du rôle (RBAC) dans Azure est un modèle utilisé pour définir et gérer les rôles des principaux de l’utilisateur et du service. Les rôles sont associés à des ensembles d’autorisations, qui déterminent les ressources qu’un principal peut lire, écrire ou gérer, ou auxquelles il peut accéder. Pour plus d’informations sur le contrôle d’accès en fonction du rôle et sur les différents rôles, consultez [Rôles intégrés pour le contrôle d’accès en fonction du rôle Azure](/azure/active-directory/role-based-access-built-in-roles).

Azure PowerShell fournit les applets de commande suivantes pour gérer les attributions de rôle :

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

Un principal du service a le rôle **Contributor** (Collaborateur) par défaut. En raison des autorisations générales qu’il inclut, ce rôle n’est pas forcément le meilleur choix en fonction de l’étendue des interactions de votre application avec les services Azure.
Le rôle **Reader** (Lecteur) étant plus restrictif, il peut être un bon choix pour les applications en lecture seule. Vous pouvez afficher les détails des autorisations propres à chaque rôle ou créer des autorisations personnalisées par le biais du portail Azure.

Dans cet exemple, nous ajoutons le rôle **Reader** à notre exemple précédent, et nous supprimons le rôle **Contributor** :

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Pour afficher les rôles actuellement attribués :

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Autres applets de commande Azure PowerShell pour la gestion des rôles :

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Changer les informations d’identification du principal de sécurité

Nous vous recommandons de vérifier les autorisations et de mettre à jour le mot de passe régulièrement. Vous pouvez également gérer et modifier les informations d’identification de sécurité à mesure que votre application évolue. Par exemple, changez le mot de passe du principal du service en remplaçant le mot de passe existant par un nouveau mot de passe de votre choix.

### <a name="add-a-new-password-for-the-service-principal"></a>Ajouter un nouveau mot de passe pour le principal du service

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Obtenir la liste des informations d’identification pour le principal du service

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Supprimer l’ancien mot de passe du principal du service

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Vérifier la liste des informations d’identification pour le principal du service

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
