---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: c19d9ade0f69f4af9f14c68ad22b327c27c8ccfd
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001301"
---
# <a name="sign-in-with-azure-powershell"></a>Se connecter avec Azure PowerShell

Azure PowerShell prend en charge plusieurs méthodes d’authentification. La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.

## <a name="sign-in-interactively"></a>Connexion interactive

Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell
Connect-AzureRmAccount
```

L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure. Cette authentification est valable pour la session PowerShell en cours.

> [!IMPORTANT]
> À compter d’Azure PowerShell 6.3.0, vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté à Windows. Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Connexion avec un principal de service

Les principaux de service sont des comptes Azure non interactifs. À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory. En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.

Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).

Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`. Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service. Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Connexion à l’aide d’Azure Managed Service Identity

Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory. Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources. Les identités managées sont disponibles uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.

Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Se connecter en tant que fournisseur de solutions cloud (CSP)

Une connexion en tant que [fournisseur de solutions Cloud (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) nécessite l’utilisation de `-TenantId`. Normalement, ce paramètre peut être spécifié comme un ID de locataire ou un nom de domaine. Toutefois, pour les connexions en tant que CSP, un **ID de locataire** doit être fourni.

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Connexion à un autre cloud

Les services cloud Azure offrent des environnements conformes aux réglementations régionales en matière de gestion de données.
Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.
Par exemple, si votre compte se trouve dans le cloud situé en Chine :

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :

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
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
