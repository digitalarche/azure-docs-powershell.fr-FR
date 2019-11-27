---
title: Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell
description: Découvrez comment exécuter des applets de commande Azure PowerShell en parallèle ou en tant que tâches en arrière-plan, en utilisant -AsJob et Start-Job.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537068"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="89dbb-103">Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell</span><span class="sxs-lookup"><span data-stu-id="89dbb-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="89dbb-104">Azure PowerShell dépend de la connexion à un cloud Azure et de l’attente des réponses : la plupart de ces applets de commande bloquent donc votre session PowerShell jusqu’à ce qu’elles reçoivent une réponse du cloud.</span><span class="sxs-lookup"><span data-stu-id="89dbb-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="89dbb-105">Les travaux PowerShell vous permettent d’exécuter des applets de commande en arrière-plan ou d’effectuer plusieurs tâches en même temps sur Azure, à partir d’une seule session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="89dbb-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="89dbb-106">Cet article est une brève vue d’ensemble de la façon d’exécuter des applets de commande Azure PowerShell en tant que travaux PowerShell et de vérifier leur achèvement.</span><span class="sxs-lookup"><span data-stu-id="89dbb-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="89dbb-107">L’exécution de commandes dans Azure PowerShell nécessite l’utilisation de contextes Azure PowerShell, qui sont abordés en détail dans [Contextes et informations d’identification de connexion Azure](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="89dbb-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="89dbb-108">Pour plus d’informations sur les travaux PowerShell, consultez [À propos des travaux PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="89dbb-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="89dbb-109">Contextes Azure avec des travaux PowerShell</span><span class="sxs-lookup"><span data-stu-id="89dbb-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="89dbb-110">Les travaux PowerShell sont exécutés en tant que processus distincts sans session PowerShell attachée : vos informations d’identification Azure doivent donc être partagées avec ces travaux.</span><span class="sxs-lookup"><span data-stu-id="89dbb-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="89dbb-111">Les informations d’identification sont passées en tant qu’objets de contexte Azure, selon une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="89dbb-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="89dbb-112">Persistance de contexte automatique</span><span class="sxs-lookup"><span data-stu-id="89dbb-112">Automatic context persistence.</span></span> <span data-ttu-id="89dbb-113">La persistance de contexte est activée par défaut et elle conserve vos informations de connexion entre plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="89dbb-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="89dbb-114">Si la persistance du contexte est activée, le contexte Azure actuel est passé au nouveau processus :</span><span class="sxs-lookup"><span data-stu-id="89dbb-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="89dbb-115">Utilisez le paramètre `-AzContext` avec les applets de commande Azure PowerShell pour fournir un objet de contexte Azure :</span><span class="sxs-lookup"><span data-stu-id="89dbb-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="89dbb-116">Si la persistance de contexte est désactivée, l’argument `-AzContext` est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="89dbb-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="89dbb-117">Utilisez le commutateur `-AsJob` fourni par certaines applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="89dbb-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="89dbb-118">Ce commutateur démarre automatiquement l’applet de commande en tant que travail PowerShell, en utilisant le contexte Azure actuellement actif :</span><span class="sxs-lookup"><span data-stu-id="89dbb-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="89dbb-119">Pour voir si une applet de commande prend en charge `-AsJob`, consultez sa documentation de référence.</span><span class="sxs-lookup"><span data-stu-id="89dbb-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="89dbb-120">Le commutateur `-AsJob` ne nécessite pas que l’enregistrement automatique du contexte soit activé.</span><span class="sxs-lookup"><span data-stu-id="89dbb-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="89dbb-121">Vous pouvez vérifier l’état d’un travail en cours d’exécution avec l’applet de commande [Get-Job](/powershell/module/microsoft.powershell.core/get-job).</span><span class="sxs-lookup"><span data-stu-id="89dbb-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="89dbb-122">Pour obtenir le résultat d’un travail à un moment donné, utilisez l’applet de commande [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="89dbb-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="89dbb-123">Pour vérifier la progression d’une opération à distance sur Azure, utilisez les applets de commande `Get-` associées au type de ressource modifié par le travail :</span><span class="sxs-lookup"><span data-stu-id="89dbb-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="89dbb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89dbb-124">See Also</span></span>

* [<span data-ttu-id="89dbb-125">Contextes Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="89dbb-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="89dbb-126">À propos des travaux PowerShell</span><span class="sxs-lookup"><span data-stu-id="89dbb-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="89dbb-127">Informations de référence sur Get-Job</span><span class="sxs-lookup"><span data-stu-id="89dbb-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="89dbb-128">Informations de référence sur Receive-Job</span><span class="sxs-lookup"><span data-stu-id="89dbb-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
