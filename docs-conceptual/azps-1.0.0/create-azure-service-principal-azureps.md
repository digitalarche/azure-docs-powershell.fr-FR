---
title: Créer un principal du service Azure avec Azure PowerShell
description: Découvrez comment créer un principal du service pour votre application ou service avec Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594780"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Créer un principal du service Azure avec Azure PowerShell

Si vous prévoyez de gérer votre application ou service avec Azure PowerShell, vous devez l’exécuter avec un principal du service Azure Active Directory (AAD) plutôt qu’avec vos informations d’identification personnelles. Cet article vous explique pas à pas comment créer un principal de sécurité avec Azure PowerShell.

## <a name="what-is-a-service-principal"></a>Qu’est-ce qu’un principal de service ?

Un principal du service Azure est une identité de sécurité utilisée par les applications, les services et les outils d’automatisation créés par l’utilisateur pour accéder à des ressources Azure spécifiques. Les principaux de service reçoivent des autorisations spécifiques liées à leurs tâches, ce qui vous donne un meilleur contrôle sur la sécurité. Contrairement à une identité d’utilisateur, qui est généralement autorisée à apporter des modifications.

## <a name="verify-your-own-permission-level"></a>Vérifier votre propre niveau d’autorisation

Tout d’abord, vous devez avoir les autorisations suffisantes dans votre annuaire Azure Active Directory et votre abonnement Azure. Vous devez être en mesure de créer une application dans Active Directory et d’affecter un rôle au principal du service.

Le moyen le plus simple de vous assurer que votre compte dispose des autorisations appropriées est d’utiliser le portail. Consultez [Vérifier l’autorisation requise dans le portail](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Créer un principal du service pour votre application

Une fois que vous êtes connecté à votre compte Azure, vous pouvez créer le principal de service. Vous devez identifier votre application déployée par l’une des informations suivantes :

* Le nom unique de votre application déployée (par exemple, « MyDemoWebApp » dans les exemples suivants)
* L’ID de l’application, le GUID unique associé à votre application, service ou objet déployé

### <a name="get-information-about-your-application"></a>Obtenir des informations sur votre application

Vous pouvez utiliser la cmdlet `Get-AzADApplication` pour obtenir des informations à propos de votre application.

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
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

Utilisez l’applet de commande `New-AzADServicePrincipal` pour créer le principal du service.

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

À ce stade, vous pouvez directement utiliser la propriété `$servicePrincipal.Secret` en tant qu’argument pour `Connect-AzAccount` (voir « Connexion à l’aide du principal de service »), ou vous pouvez convertir `SecureString` en une chaîne de texte brut :

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a>Se connecter en tant que principal du service

Vous pouvez maintenant vous connecter en tant que nouveau principal du service pour votre application en utilisant la valeur `appId` que vous avez fournie et `password` qui a été  
généré. Vous allez également avoir besoin de l’ID de locataire pour le principal de service. Votre ID de locataire s’affiche lorsque vous vous connectez à Azure avec vos informations d’identification personnelles. Pour vous connecter avec un principal de service, utilisez les commandes :

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Lorsque la connexion aboutit, la sortie est semblable à ce qui suit :

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
> Le contrôle d’accès en fonction du rôle (RBAC) dans Azure est un modèle utilisé pour définir et gérer les rôles des principaux de l’utilisateur et du service. Les rôles sont associés à des ensembles d’autorisations, qui déterminent les ressources qu’un principal peut lire, écrire ou gérer, ou auxquelles il peut accéder. Pour plus d’informations sur le contrôle d’accès en fonction du rôle (RBAC) et sur les différents rôles, consultez [Rôles intégrés pour le contrôle d’accès en fonction du rôle Azure](/azure/active-directory/role-based-access-built-in-roles).

Azure PowerShell fournit les applets de commande suivantes pour gérer les attributions de rôle :

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Un principal du service a le rôle **Contributor** (Collaborateur) par défaut. En raison des autorisations générales qu’il inclut, ce rôle n’est pas forcément le meilleur choix en fonction de l’étendue des interactions de votre application avec les services Azure.
Le rôle **Reader** (Lecteur) étant plus restrictif, il peut être un bon choix pour les applications en lecture seule. Vous pouvez afficher les détails des autorisations propres à chaque rôle ou créer des autorisations personnalisées par le biais du portail Azure.

Dans cet exemple, nous ajoutons le rôle **Reader** à notre exemple précédent, et nous supprimons le rôle **Contributor** :

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Pour afficher les rôles actuellement attribués :

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

* [Get-AzRoleDefinition](/powershell/module/az.resources/Get-azRoleDefinition)
* [New-AzRoleDefinition](/powershell/module/az.resources/New-azRoleDefinition)
* [Remove-AzRoleDefinition](/powershell/module/az.resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Changer les informations d’identification du principal de sécurité

Nous vous recommandons de vérifier les autorisations et de mettre à jour le mot de passe régulièrement. Vous pouvez également gérer et modifier les informations d’identification de sécurité à mesure que votre application évolue. Par exemple, changez le mot de passe du principal du service en remplaçant le mot de passe existant par un nouveau mot de passe de votre choix.

### <a name="add-a-new-password-for-the-service-principal"></a>Ajouter un nouveau mot de passe pour le principal du service

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Obtenir la liste des informations d’identification pour le principal du service

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Supprimer l’ancien mot de passe du principal du service

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Vérifier la liste des informations d’identification pour le principal du service

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a>Obtenir des informations sur le principal du service

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
