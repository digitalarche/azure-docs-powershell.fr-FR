---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9a93145f2abeea466a739775ca8ae7e337e78166
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587616"
---
# <a name="sign-in-with-azure-powershell"></a>Se connecter avec Azure PowerShell

Azure PowerShell prend en charge plusieurs méthodes d’authentification. La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.

## <a name="sign-in-interactively"></a>Connexion interactive

Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell-interactive
Connect-AzureRmAccount
```

L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure. Lorsque vous vous authentifiez, ces informations sont enregistrées pour la session PowerShell actuelle, la boîte de dialogue est fermée, et vous avez accès à toutes les applets de commande Azure PowerShell.

> [!IMPORTANT]
> Cette procédure de connexion est valable pour la session PowerShell _uniquement_. Pour conserver l’authentification sur plusieurs sessions, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Connexion avec un principal de service

Les principaux du service offrent un moyen de créer des comptes non interactifs que vous pouvez ensuite utiliser pour manipuler les ressources. Les principaux du service sont comme des comptes d’utilisateur auxquels vous pouvez appliquer des règles à l’aide d’Azure Active Directory. En accordant les autorisations minimales nécessaires à un principal du service, vous sécurisez encore davantage vos scripts d’automatisation.

Si vous avez besoin de créer un principal de service à utiliser avec Azure PowerShell, consultez [Créer un principal de service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).

Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`. Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion et de l’ID du locataire associé au principal du service. Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez l’applet de commande [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>Se connecter en utilisant des identités managées pour les ressources Azure

Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory. Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources. Les identités managées sont disponibles uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.

Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

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
