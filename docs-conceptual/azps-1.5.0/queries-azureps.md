---
title: Interroger la sortie d’applets de commande Azure PowerShell
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882354"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="19c4a-103">Interroger la sortie d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="19c4a-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="19c4a-104">Les résultats de chaque cmdlet d’Azure PowerShell constituent un objet Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19c4a-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="19c4a-105">Même les cmdlets qui ne sont pas explicitement des opérations `Get-` pourraient retourner une valeur pouvant être inspectée, pour donner des informations au sujet d’une ressource qui a été créée ou modifiée.</span><span class="sxs-lookup"><span data-stu-id="19c4a-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="19c4a-106">Certaines cmdlets retournent un groupe qui doit être itéré, tandis que la plupart retourne un objet unique.</span><span class="sxs-lookup"><span data-stu-id="19c4a-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="19c4a-107">Dans presque tous les cas, vous interrogez la sortie d’Azure PowerShell avec la cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), aussi abrégée `select`.</span><span class="sxs-lookup"><span data-stu-id="19c4a-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="19c4a-108">Une sortie peut être filtrée avec [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), ou son alias `where`.</span><span class="sxs-lookup"><span data-stu-id="19c4a-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="19c4a-109">Sélectionner des propriétés simples</span><span class="sxs-lookup"><span data-stu-id="19c4a-109">Select simple properties</span></span>

<span data-ttu-id="19c4a-110">Dans le format de table par défaut, les cmdlets Azure PowerShell n’affichent pas toutes les propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="19c4a-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="19c4a-111">Vous pouvez obtenir toutes les propriétés à l’aide de la cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list), ou en dirigeant la sortie vers `Select-Object *` :</span><span class="sxs-lookup"><span data-stu-id="19c4a-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="19c4a-112">Une fois que vous connaissez les noms des propriétés qui vous intéressent, vous pouvez les utiliser avec `Select-Object` pour les obtenir directement :</span><span class="sxs-lookup"><span data-stu-id="19c4a-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="19c4a-113">La sortie obtenue avec `Select-Object` est toujours formatée pour afficher les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="19c4a-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="19c4a-114">Pour en savoir plus sur l’utilisation du formatage avec la requête de résultats de cmdlet, consultez [Formater une sortie de cmdlet Azure PowerShell](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="19c4a-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="19c4a-115">Sélectionner des propriétés imbriquées</span><span class="sxs-lookup"><span data-stu-id="19c4a-115">Select nested properties</span></span>

<span data-ttu-id="19c4a-116">Certaines propriétés dans la sortie de cmdlet Azure PowerShell utilisent des objets imbriqués, comme la propriété `StorageProfile` de la sortie `Get-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="19c4a-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="19c4a-117">Pour obtenir une valeur d’une propriété imbriquée, renseignez un nom d’affichage et le chemin d’accès complet à la valeur que vous souhaitez inspecter dans un argument de dictionnaire dans `Select-Object` :</span><span class="sxs-lookup"><span data-stu-id="19c4a-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="19c4a-118">Chaque argument de dictionnaire sélectionne une propriété de l’objet.</span><span class="sxs-lookup"><span data-stu-id="19c4a-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="19c4a-119">La propriété à extraire doit faire partie d’une expression.</span><span class="sxs-lookup"><span data-stu-id="19c4a-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="19c4a-120">Filtrer les résultats</span><span class="sxs-lookup"><span data-stu-id="19c4a-120">Filter results</span></span> 

<span data-ttu-id="19c4a-121">La cmdlet `Where-Object` vous permet de filtrer les résultats selon la valeur de propriété de votre choix, y compris des propriétés imbriquées.</span><span class="sxs-lookup"><span data-stu-id="19c4a-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="19c4a-122">L’exemple suivant montre comment utiliser `Where-Object` pour trouver les machines virtuelles dans un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="19c4a-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="19c4a-123">Vous pouvez diriger les résultats de `Select-Object` et `Where-Object` l’un vers l’autre.</span><span class="sxs-lookup"><span data-stu-id="19c4a-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="19c4a-124">À des fins de performances, nous vous recommandons de toujours placer l’opération `Where-Object` avant `Select-Object` :</span><span class="sxs-lookup"><span data-stu-id="19c4a-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```