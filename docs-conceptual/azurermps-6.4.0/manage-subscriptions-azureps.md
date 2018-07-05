---
title: Gérer les abonnements Azure avec Azure PowerShell
description: Gérer les abonnements Azure avec Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: fbd2fe315efbdfb2147218229d51e983e2b61361
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406284"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="da506-103">Gérer plusieurs abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="da506-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="da506-104">Si vous débutez avec Azure, vous avez probablement un seul abonnement.</span><span class="sxs-lookup"><span data-stu-id="da506-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="da506-105">Si vous utilisez Azure depuis un moment déjà, vous avez peut-être créé plusieurs abonnements Azure.</span><span class="sxs-lookup"><span data-stu-id="da506-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="da506-106">Vous pouvez configurer Azure PowerShell pour exécuter les commandes sur un abonnement spécifique.</span><span class="sxs-lookup"><span data-stu-id="da506-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="da506-107">Obtenez la liste de tous les abonnements créés dans votre compte.</span><span class="sxs-lookup"><span data-stu-id="da506-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="da506-108">Définissez l’abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="da506-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="da506-109">Vérifiez que cette modification a été prise en compte en exécutant l’applet de commande `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="da506-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="da506-110">Une fois que vous avez défini votre abonnement par défaut, toutes les commandes Azure PowerShell suivantes s’exécuteront sur cet abonnement.</span><span class="sxs-lookup"><span data-stu-id="da506-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
