---
title: Gérer les abonnements Azure avec Azure PowerShell
description: Gérer les abonnements Azure avec Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 5edfe15a1ed4e321d28422e9e6c32a14b717b93c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56144303"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="20cc0-103">Gérer plusieurs abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="20cc0-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="20cc0-104">Si vous débutez avec Azure, vous avez probablement un seul abonnement.</span><span class="sxs-lookup"><span data-stu-id="20cc0-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="20cc0-105">Si vous utilisez Azure depuis un moment déjà, vous avez peut-être créé plusieurs abonnements Azure.</span><span class="sxs-lookup"><span data-stu-id="20cc0-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="20cc0-106">Vous pouvez configurer Azure PowerShell pour exécuter les commandes sur un abonnement spécifique.</span><span class="sxs-lookup"><span data-stu-id="20cc0-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="20cc0-107">Obtenez la liste de tous les abonnements créés dans votre compte.</span><span class="sxs-lookup"><span data-stu-id="20cc0-107">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="20cc0-108">Définissez l’abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="20cc0-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="20cc0-109">Vérifiez que cette modification a été prise en compte en exécutant l’applet de commande `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="20cc0-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

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

<span data-ttu-id="20cc0-110">Une fois que vous avez défini votre abonnement par défaut, toutes les commandes Azure PowerShell suivantes s’exécuteront sur cet abonnement.</span><span class="sxs-lookup"><span data-stu-id="20cc0-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
