---
title: Gérer les abonnements Azure avec Azure PowerShell | Microsoft Docs
description: Gérer les abonnements Azure avec Azure PowerShell
keywords: Azure PowerShell, abonnement
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 8869b700e513d6fc07e69de1dbfe852bd2a52df1
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576264"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="1d5c3-104">Gérer plusieurs abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="1d5c3-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="1d5c3-105">Si vous débutez avec Azure, vous avez probablement un seul abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="1d5c3-106">Si vous utilisez Azure depuis un moment déjà, vous avez peut-être créé plusieurs abonnements Azure.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="1d5c3-107">Vous pouvez configurer Azure PowerShell pour exécuter les commandes sur un abonnement spécifique.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="1d5c3-108">Obtenez la liste de tous les abonnements créés dans votre compte.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
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

2. <span data-ttu-id="1d5c3-109">Définissez l’abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="1d5c3-110">Vérifiez que cette modification a été prise en compte en exécutant l’applet de commande `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
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

<span data-ttu-id="1d5c3-111">Une fois que vous avez défini votre abonnement par défaut, toutes les commandes Azure PowerShell suivantes s’exécuteront sur cet abonnement.</span><span class="sxs-lookup"><span data-stu-id="1d5c3-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
