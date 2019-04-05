---
title: Exécuter des cmdlets en parallèle à l’aide de travaux PowerShell
description: Comment exécuter des applets de commande en parallèle à l’aide du paramètre -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 825a07e01194a07b747712a62384c7f162e63d7d
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808034"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="94469-103">Applets de commande en cours d’exécution en parallèle à l’aide de travaux PowerShell</span><span class="sxs-lookup"><span data-stu-id="94469-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="94469-104">PowerShell prend en charge les actions asynchrones avec les [travaux PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="94469-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="94469-105">Azure PowerShell dépend fortement du passage et de l’attente d’appels réseau vers Azure.</span><span class="sxs-lookup"><span data-stu-id="94469-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="94469-106">Il se peut que vous deviez souvent effectuer des appels non bloquants.</span><span class="sxs-lookup"><span data-stu-id="94469-106">You may often find yourself needing to make non-blocking calls.</span></span> <span data-ttu-id="94469-107">Pour répondre à ce besoin, Azure PowerShell assure une prise en charge haut de gamme de [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="94469-107">To address this need, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="94469-108">Persistance de contexte et PSJobs</span><span class="sxs-lookup"><span data-stu-id="94469-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="94469-109">Dans la mesure où les PSJobs sont exécutés en tant que processus distincts, vous devez partager votre connexion Azure avec eux.</span><span class="sxs-lookup"><span data-stu-id="94469-109">Since PSJobs are run as separate processes, your Azure connection must be shared with them.</span></span> <span data-ttu-id="94469-110">Après vous être connecté à votre compte Azure avec `Connect-AzAccount`, transmettez le contexte à une tâche.</span><span class="sxs-lookup"><span data-stu-id="94469-110">After signing in to your Azure account with `Connect-AzAccount`, pass the context to a job.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList (Get-AzContext),$creds
```

<span data-ttu-id="94469-111">Toutefois, si vous avez choisi l’enregistrement automatique de votre contexte avec `Enable-AzContextAutosave`, le contexte est automatiquement partagé avec tous les travaux créés.</span><span class="sxs-lookup"><span data-stu-id="94469-111">However, if you have chosen to have your context automatically saved with `Enable-AzContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -ArgumentList $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="94469-112">Travaux automatiques avec `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="94469-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="94469-113">Pour des raisons pratiques, Azure PowerShell fournit également un commutateur `-AsJob` sur certains applets de commande de longue durée.</span><span class="sxs-lookup"><span data-stu-id="94469-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="94469-114">Le commutateur `-AsJob` rend encore plus facile la création de PSJobs.</span><span class="sxs-lookup"><span data-stu-id="94469-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="94469-115">Vous pouvez examiner le travail et la progression à tout moment avec `Get-Job` et `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="94469-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzVM`.</span></span>

```azurepowershell-interactive
Get-Job $job
Get-AzVM MyVm
```

```output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzVM' AzureLongRunningJob`1 Running True        localhost New-AzVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="94469-116">Lorsque la tâche est terminée, consultez le résultat avec `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="94469-116">When the job completes, get the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="94469-117">`Receive-Job` renvoie le résultat à partir de l’applet de commande comme si l’indicateur `-AsJob` n’était pas présent.</span><span class="sxs-lookup"><span data-stu-id="94469-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="94469-118">Par exemple, le résultat `Receive-Job` de `Do-Action -AsJob` est du même type que le résultat de `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="94469-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```azurepowershell-interactive
$vm = Receive-Job $job
$vm
```

```output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="94469-119">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="94469-119">Example Scenarios</span></span>

<span data-ttu-id="94469-120">Créez plusieurs machines virtuelles simultanément :</span><span class="sxs-lookup"><span data-stu-id="94469-120">Create several VMs at once:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzVM
```

<span data-ttu-id="94469-121">Dans cet exemple, l’applet de commande `Wait-Job` génère la mise en pause du script pendant l’exécution des travaux.</span><span class="sxs-lookup"><span data-stu-id="94469-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="94469-122">Le script continue de s’exécuter une fois tous les travaux terminés.</span><span class="sxs-lookup"><span data-stu-id="94469-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="94469-123">Plusieurs tâches s’exécutent en parallèle. Le script attend leur conclusion avant de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="94469-123">Several jobs run in parallel then the script waits for completion before continuing.</span></span>

```output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```
