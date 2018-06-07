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
ms.openlocfilehash: d28da700efbc2927cb3f73ae696759fb1e0c0cd6
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821953"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="99da5-104">Gérer plusieurs abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="99da5-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="99da5-105">Si vous débutez avec Azure, vous avez probablement un seul abonnement.</span><span class="sxs-lookup"><span data-stu-id="99da5-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="99da5-106">Si vous utilisez Azure depuis un moment déjà, vous avez peut-être créé plusieurs abonnements Azure.</span><span class="sxs-lookup"><span data-stu-id="99da5-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="99da5-107">Vous pouvez configurer Azure PowerShell pour exécuter les commandes sur un abonnement spécifique.</span><span class="sxs-lookup"><span data-stu-id="99da5-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="99da5-108">Obtenez la liste de tous les abonnements créés dans votre compte.</span><span class="sxs-lookup"><span data-stu-id="99da5-108">Get a list of all subscriptions in your account.</span></span>

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

2. <span data-ttu-id="99da5-109">Définissez l’abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="99da5-109">Set the default.</span></span>

    ```powershell
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="99da5-110">Vérifiez que cette modification a été prise en compte en exécutant l’applet de commande `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="99da5-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell
    Get-AzureRmContext
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="99da5-111">Une fois que vous avez défini votre abonnement par défaut, toutes les commandes Azure PowerShell suivantes s’exécuteront sur cet abonnement.</span><span class="sxs-lookup"><span data-stu-id="99da5-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
