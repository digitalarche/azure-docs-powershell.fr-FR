---
title: Utiliser des principaux de service avec Azure PowerShell
description: Découvrez comment créer et utiliser des principaux de service avec Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: abb85d3d3f6a20697510447cda2c02b2703ef921
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2019
ms.locfileid: "67192799"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Créer un principal du service Azure avec Azure PowerShell

Les outils automatisés qui utilisent les services Azure doivent toujours avoir des autorisations restreintes. Plutôt que de faire se connecter des applications en tant qu’utilisateur entièrement privilégié, Azure offre des principaux du service.

Un principal de service Azure est une identité créée pour une utilisation avec les applications, des services hébergés et des outils automatisés permettant d’accéder aux ressources Azure. Cet accès est limité par les rôles assignés au principal du service, ce qui vous permet de contrôler quelles ressources sont accessibles et à quel niveau. Pour des raisons de sécurité, il est toujours recommandé d’utiliser les principaux du service avec des outils automatisés, plutôt que de leur permettre de se connecter avec une identité d’utilisateur.

Cet article vous explique les étapes à suivre pour créer un principal du service, obtenir des informations à son sujet et le réinitialiser avec Azure PowerShell.

## <a name="create-a-service-principal"></a>Créer un principal du service

Créez un principal de service avec l’applet de commande [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). Lorsque vous créez un principal de service, vous choisissez le type d’authentification de connexion qu’il utilise.

> [!NOTE]
>
> Si votre compte ne dispose pas d’autorisations pour créer un principal de service, `New-AzADServicePrincipal` vous retournera un message d’erreur contenant « Privilèges insuffisants pour effectuer l’opération ». Contactez votre administrateur Azure Active Directory pour créer un principal de service.

Il existe deux types d’authentification disponibles pour les principaux de service : L’authentification basée sur un mot de passe et l’authentification basée sur un certificat.

### <a name="password-based-authentication"></a>L’authentification basée sur un mot de passe

Sans autres paramètres d’authentification, l’authentification par mot de passe est utilisée et un mot de passe aléatoire est créé. Si vous souhaitez une authentification basée sur un mot de passe, cette méthode est recommandée.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

L’objet retourné contient le membre `Secret`, qui est un `SecureString` contenant le mot de passe généré. Veillez à stocker cette valeur dans un endroit sécurisé pour vous authentifier auprès du principal de service. Sa valeur __ne s’affichera pas__ dans la console. Si vous perdez le mot de passe, effectuez une [réinitialisation des informations d’identification du principal de service](#reset-credentials). 

Pour les mots de passe fournis par l’utilisateur, l’argument `-PasswordCredential` accepte les objets `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Ces objets doivent avoir un `StartDate` et un `EndDate` valides, et accepter un `Password` en texte en clair. Lorsque vous créez un mot de passe, assurez-vous de suivre les [règles et restrictions relatives aux mots de passe Azure Active Directory](/azure/active-directory/active-directory-passwords-policy). N’utilisez pas de mot de passe faible. Ne réutilisez pas de mot de passe.

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

L’objet retourné par `New-AzADServicePrincipal` contient les membres `Id` et `DisplayName`, qui peuvent être utilisés pour se connecter au principal de service.

> [!IMPORTANT]
>
> La connexion au principal de service nécessite l’ID du locataire dans lequel le principal de service a été créé. Pour obtenir le locataire qui était actif au moment de la création du principal de service, exécutez la commande suivante __immédiatement après__ avoir créé le principal de service :
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>Authentification par certificat

Les principaux de service qui utilisent l’authentification par certificat sont créés avec le paramètre `-CertValue`. Ce paramètre accepte la chaîne ASCII codée en base64 du certificat public. Celui-ci est représenté par un fichier PEM, ou par un fichier CRT ou CER avec texte encodé. Les encodages binaires du certificat public ne sont pas pris en charge. Ces instructions supposent que vous disposez déjà d’un certificat.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Vous pouvez également utiliser le paramètre `-KeyCredential`, qui accepte les objets `PSADKeyCredential`. Ces objets doivent avoir un `StartDate` et un `EndDate` valides. De plus, leur membre `CertValue` doit être défini sur la chaîne ASCII codée en base64 du certificat public.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

L’objet retourné par `New-AzADServicePrincipal` contient les membres `Id` et `DisplayName`, qui peuvent être utilisés pour se connecter au principal de service. Les clients qui se connectent au principal de service ont également besoin d’accéder à la clé privée du certificat.

> [!IMPORTANT]
>
> La connexion au principal de service nécessite l’ID du locataire dans lequel le principal de service a été créé. Pour obtenir le locataire qui était actif au moment de la création du principal de service, exécutez la commande suivante __immédiatement après__ avoir créé le principal de service :
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>Obtenir un principal de service existant

Vous pouvez récupérer la liste des principaux de service du locataire actif à l’aide de [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). Par défaut, cette commande retourne __tous__ les principaux de service d’un locataire. Pour les grandes organisations, les résultats peuvent donc mettre du temps à s’afficher. Pour cette raison, il est recommandé d’utiliser l’un des arguments de filtrage côté serveur facultatifs :

* `-DisplayNameBeginsWith` demande les principaux de service ayant un _préfixe_ qui correspond à la valeur fournie. Le nom d’affichage d’un principal de service correspond à la valeur définie avec `-DisplayName` lors de la création.
* `-DisplayName` demande une _correspondance exacte_ du nom du principal de service.

## <a name="manage-service-principal-roles"></a>Gérer les rôles du principal du service

Azure PowerShell fournit les applets de commande suivantes pour gérer les attributions de rôles :

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Un principal du service a le rôle **Contributor** (Collaborateur) par défaut. Ce rôle dispose des autorisations complètes de lecture et d’écriture dans un compte Azure. Le rôle de **Lecteur** est plus restrictif avec un accès en lecture seule.  Pour plus d’informations sur les rôles et le contrôle d’accès en fonction du rôle, consultez [RBAC : rôles intégrés pour les ressources Azure](/azure/active-directory/role-based-access-built-in-roles).

Cet exemple ajoute le rôle de **Lecteur** et supprime le rôle de **Contributeur** :

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> Les applets de commande d’attribution de rôle n’acceptent pas l’ID d’objet du principal de service. Elles acceptent l’ID d’application associé, qui est généré au moment de la création. Pour obtenir l’ID d’application d’un principal de service, utilisez `Get-AzADServicePrincipal`.

> [!NOTE]
> Si votre compte ne dispose pas d’autorisations pour assigner un rôle, un message d’erreur vous indiquera que votre compte « n’est pas autorisé à effectuer l’action ’Microsoft.Authorization/roleAssignments/write’ ». Contactez votre administrateur Azure Active Directory pour gérer les rôles.

L’ajout d’un rôle ne restreint _pas_ les autorisations précédemment assignées. Lors de la restriction des autorisations du principal du service, le rôle de __Contributeur__ dot être supprimé.

Les modifications peuvent être vérifiées en répertoriant les rôles attribués :

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Se connecter en tant que principal du service

Testez les informations d’identification et les autorisations du nouveau principal du service en vous connectant. Pour vous connecter à un principal de service, vous avez besoin de la valeur `applicationId` qui lui est associée, ainsi que du locataire dans lequel il a été créé.

Pour vous connecter avec un principal du service utilisant un mot de passe :

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

L’authentification par certificat nécessite qu’Azure PowerShell puisse récupérer des informations à partir d’un magasin de certificats local en se basant sur l’empreinte numérique du certificat.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

Pour obtenir des instructions sur l’importation d’un certificat dans un magasin d’informations d’identification accessible par PowerShell, consultez [Se connecter avec Azure PowerShell](authenticate-azureps.md#sp-signin).

## <a name="reset-credentials"></a>Réinitialiser les informations d’identification

Si vous avez oublié les informations d’identification d’un principal de service, utilisez [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) pour ajouter de nouvelles informations d’identification. Cette applet de commande accepte les mêmes arguments d’informations d’identification et les mêmes types que `New-AzADServicePrincipal`. En l’absence d’arguments d’informations d’identification, un nouveau `PasswordCredential` et un mot de passe aléatoire sont créés.

> [!IMPORTANT]
> Avant d’attribuer de nouvelles informations d’identification, vous pouvez supprimer les informations d’identification existantes afin d’empêcher qu’elles soient utilisées pour la connexion. Pour ce faire, utilisez l’applet de commande [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) :
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
