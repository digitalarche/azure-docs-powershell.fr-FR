---
title: Exécuter des cmdlets en parallèle à l’aide de travaux PowerShell
description: Comment exécuter des applets de commande en parallèle à l’aide du paramètre -AsJob.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 58aa777ca599c2a6181f0ecc5c20f6db7a89b75f
ms.sourcegitcommit: 32dad89878c7e728f740936f5f338b8ae878a6a1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2019
ms.locfileid: "58192903"
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a>Applets de commande en cours d’exécution en parallèle à l’aide de travaux PowerShell

PowerShell prend en charge les actions asynchrones avec les [travaux PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).
Azure PowerShell dépend fortement du passage et de l’attente d’appels réseau vers Azure. Il se peut que vous deviez souvent effectuer des appels non bloquants. Pour répondre à ce besoin, Azure PowerShell assure une prise en charge haut de gamme de [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="context-persistence-and-psjobs"></a>Persistance de contexte et PSJobs

Dans la mesure où les PSJobs sont exécutés en tant que processus distincts, vous devez partager votre connexion Azure avec eux. Après vous être connecté à votre compte Azure avec `Connect-AzAccount`, transmettez le contexte à une tâche.

```azurepowershell-interactive
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -Arguments (Get-AzContext),$creds
```

Toutefois, si vous avez choisi l’enregistrement automatique de votre contexte avec `Enable-AzContextAutosave`, le contexte est automatiquement partagé avec tous les travaux créés.

```azurepowershell-interactive
Enable-AzContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a>Travaux automatiques avec `-AsJob`

Pour des raisons pratiques, Azure PowerShell fournit également un commutateur `-AsJob` sur certains applets de commande de longue durée.
Le commutateur `-AsJob` rend encore plus facile la création de PSJobs.

```azurepowershell-interactive
$creds = Get-Credential
$job = New-AzVM -Name MyVm -Credential $creds -AsJob
```

Vous pouvez examiner le travail et la progression à tout moment avec `Get-Job` et `Get-AzVM`.

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

Lorsque la tâche est terminée, consultez le résultat avec `Receive-Job`.

> [!NOTE]
> `Receive-Job` renvoie le résultat à partir de l’applet de commande comme si l’indicateur `-AsJob` n’était pas présent.
> Par exemple, le résultat `Receive-Job` de `Do-Action -AsJob` est du même type que le résultat de `Do-Action`.

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

## <a name="example-scenarios"></a>Exemples de scénarios

Créez plusieurs machines virtuelles simultanément :

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

Dans cet exemple, l’applet de commande `Wait-Job` génère la mise en pause du script pendant l’exécution des travaux. Le script continue de s’exécuter une fois tous les travaux terminés. Plusieurs tâches s’exécutent en parallèle. Le script attend leur conclusion avant de poursuivre.

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
