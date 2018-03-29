---
title: Applets de commande en cours d’exécution en parallèle à l’aide de travaux PowerShell
description: Comment exécuter des applets de commande en parallèle à l’aide du paramètre -AsJob.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: 0a445a7db84c8deb6518b826b4096983669c5961
ms.sourcegitcommit: 15bf69bf95eceb936b3a429e741add95c308826a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2018
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="0c4d7-103">Applets de commande en cours d’exécution en parallèle à l’aide de travaux PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c4d7-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="0c4d7-104">PowerShell prend en charge les actions asynchrones avec les [travaux PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="0c4d7-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="0c4d7-105">Azure PowerShell dépend fortement du passage et de l’attente d’appels réseau vers Azure.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="0c4d7-106">En tant que développeur, il se peut que vous cherchiez souvent à passer plusieurs appels non bloquants vers Azure dans un script, ou que vous vouliez créer des ressources Azure dans la boucle REPL sans bloquer la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="0c4d7-107">Pour répondre à ces besoins, Azure PowerShell assure la prise en charge haut de gamme de [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="0c4d7-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="0c4d7-108">Persistance de contexte et PSJobs</span><span class="sxs-lookup"><span data-stu-id="0c4d7-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="0c4d7-109">Les PSJobs sont exécutés dans des processus distincts, ce qui signifie que les informations de connexion Azure doivent être partagées correctement avec les travaux créés.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="0c4d7-110">Lors de la connexion de votre Azure compte à votre session PowerShell avec `Login-AzureRmAccount`, vous pouvez transmettre le contexte à un travail.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-110">Upon connecting your Azure account to your PowerShell session with `Login-AzureRmAccount`, you can pass the context to a job.</span></span>

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="0c4d7-111">Toutefois, si vous avez choisi l’enregistrement automatique de votre contexte avec `Enable-AzureRmContextAutosave`, le contexte est automatiquement partagé avec tous les travaux créés.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="0c4d7-112">Travaux automatiques avec `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="0c4d7-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="0c4d7-113">Pour des raisons pratiques, Azure PowerShell fournit également un commutateur `-AsJob` sur certains applets de commande de longue durée.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="0c4d7-114">Le commutateur `-AsJob` rend encore plus facile la création de PSJobs.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="0c4d7-115">Vous pouvez examiner le travail et la progression à tout moment avec `Get-Job` et `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```powershell
Get-Job $job
Get-AzureRmVM MyVm
```

```Output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="0c4d7-116">Par la suite, à la fin, vous pouvez obtenir le résultat du travail avec `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="0c4d7-117">`Receive-Job` renvoie le résultat à partir de l’applet de commande comme si l’indicateur `-AsJob` n’était pas présent.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="0c4d7-118">Par exemple, le résultat `Receive-Job` de `Do-Action -AsJob` est du même type que le résultat de `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```powershell
$vm = Receive-Job $job
$vm
```

```Output
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

## <a name="example-scenarios"></a><span data-ttu-id="0c4d7-119">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="0c4d7-119">Example Scenarios</span></span>

<span data-ttu-id="0c4d7-120">Créez plusieurs machines virtuelles à la fois.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-120">Create multiple VMs at once.</span></span>

```powershell
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="0c4d7-121">Dans cet exemple, l’applet de commande `Wait-Job` génère la mise en pause du script pendant l’exécution des travaux.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="0c4d7-122">Le script continue de s’exécuter une fois tous les travaux terminés.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="0c4d7-123">Cela vous permet de créer plusieurs travaux s’exécutant en parallèle, puis d’attendre la fin avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0c4d7-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```Output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
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
