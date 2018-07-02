---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, principal de service ou avec MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: e2eb6767d16dd15529b35b7a4134f4dcdd257d60
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237727"
---
# <a name="sign-in-with-azure-powershell"></a>Se connecter avec Azure PowerShell

Azure PowerShell prend en charge plusieurs méthodes de connexion. La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.

## <a name="sign-in-interactively"></a>Connexion interactive

Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell
Connect-AzureRmAccount
```

L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure. Lorsque vous vous authentifiez, ces informations sont enregistrées pour la session PowerShell actuelle, la boîte de dialogue est fermée, et vous avez accès à toutes les applets de commande Azure PowerShell.

> [!IMPORTANT]
> Cette procédure de connexion est valable pour la session PowerShell _uniquement_. Pour conserver la connexion sur plusieurs sessions, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Connexion avec un principal de service

Les principaux du service offrent un moyen de créer des comptes non interactifs que vous pouvez ensuite utiliser pour manipuler les ressources. Les principaux du service sont comme des comptes d’utilisateur auxquels vous pouvez appliquer des règles à l’aide d’Azure Active Directory. En accordant les autorisations minimales nécessaires à un principal du service, vous sécurisez encore davantage vos scripts d’automatisation.

Si vous avez besoin de créer un principal de service à utiliser avec Azure PowerShell, consultez [Créer un principal de service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).

Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`. Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion et de l’ID du locataire associé au principal du service. Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez l’applet de commande [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Connexion à l’aide d’une identité de service administrée de machine virtuelle Azure

L’identité du service administré (MSI) est une fonctionnalité en version préliminaire d’Azure Active Directory. Vous pouvez utiliser un principal du service MSI pour vous connecter et obtenir un jeton d’accès d’application uniquement pour accéder aux autres ressources. MSI est disponible uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.

Pour en savoir plus sur MSI, consultez [Utilisation d’une identité de service administré (MSI) de machine virtuelle Azure pour se connecter et obtenir des jetons](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="sign-in-to-another-cloud"></a>Connexion à un autre cloud

Les services de cloud Azure offrent différents environnements conformes aux règles de traitement des données de nombreuses régions. Si votre compte Azure se trouve dans un cloud associé à une de ces régions, vous devez spécifier cet environnement lors de la connexion. Par exemple, si votre compte se trouve dans le cloud de la Chine, connectez-vous à l’aide la commande suivante :

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Pour obtenir la liste d’environnements disponibles, utilisez la commande suivante :

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure

Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).

Applets de commande Azure PowerShell pour la gestion des rôles :

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
