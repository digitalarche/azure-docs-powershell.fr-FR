---
title: Se connecter avec Azure PowerShell
description: Se connecter avec Azure PowerShell
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f07dee0eed106e39879d58ae06ff08b787faa531
ms.sourcegitcommit: 5f0013981fcea1d689649b9a2b2ffe84ae842e56
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="log-in-with-azure-powershell"></a>Se connecter avec Azure PowerShell

Azure PowerShell prend en charge plusieurs méthodes de connexion. La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.

## <a name="interactive-log-in"></a>Connexion interactive

1. Saisissez `Connect-AzureRmAccount`. Une boîte de dialogue s’affiche pour vous demander vos informations d’identification Azure.

2. Entrez l’adresse de messagerie et le mot de passe associés à votre compte. Azure authentifie et enregistre les informations d’identification, puis ferme la fenêtre.

## <a name="log-in-with-a-service-principal"></a>Connexion avec un principal du service

Les principaux du service offrent un moyen de créer des comptes non interactifs que vous pouvez ensuite utiliser pour manipuler les ressources. Les principaux du service sont comme des comptes d’utilisateur auxquels vous pouvez appliquer des règles à l’aide d’Azure Active Directory. En accordant les autorisations minimales nécessaires à un principal du service, vous sécurisez encore davantage vos scripts d’automatisation.

1. Si vous n’avez pas encore de principal du service, [créez-en un](create-azure-service-principal-azureps.md).

2. Connectez-vous avec le principal du service.

    ```powershell
    Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    Pour obtenir votre ID de locataire (TenantId), connectez-vous de manière interactive, puis recherchez la valeur TenantId dans votre abonnement.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Connectez-vous à l’aide d’une identité de service administrée de machine virtuelle Azure

L’identité du service administré (MSI) est une fonctionnalité en version préliminaire d’Azure Active Directory. Vous pouvez utiliser un principal du service MSI pour vous connecter et obtenir un jeton d’accès d’application uniquement pour accéder aux autres ressources.

Pour en savoir plus sur MSI, consultez [Utilisation d’une identité de service administré (MSI) de machine virtuelle Azure pour se connecter et obtenir des jetons](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="log-in-to-another-cloud"></a>Connexion à un autre cloud

Les services de cloud computing d’Azure offrent différents environnements conformes aux règles de traitement des données de nombreux gouvernements. Si votre compte Azure se trouve dans un des clouds gouvernementaux, vous devez spécifier cet environnement lors de la connexion. Par exemple, si votre compte se trouve dans le cloud de la Chine, connectez-vous à l’aide la commande suivante :

```powershell
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Pour obtenir la liste d’environnements disponibles, utilisez la commande suivante :

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure

Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).

Applets de commande Azure PowerShell pour la gestion des rôles

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
