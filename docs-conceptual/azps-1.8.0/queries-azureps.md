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
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068793"
---
# <a name="query-output-of-azure-powershell"></a>Interroger la sortie d’Azure PowerShell 

Les résultats de chaque cmdlet d’Azure PowerShell constituent un objet Azure PowerShell. Même les cmdlets qui ne sont pas explicitement des opérations `Get-` pourraient retourner une valeur pouvant être inspectée, pour donner des informations au sujet d’une ressource qui a été créée ou modifiée. Certaines cmdlets retournent un groupe qui doit être itéré, tandis que la plupart retourne un objet unique.

Dans presque tous les cas, vous interrogez la sortie d’Azure PowerShell avec la cmdlet [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object), aussi abrégée `select`. Une sortie peut être filtrée avec [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), ou son alias `where`.

## <a name="select-simple-properties"></a>Sélectionner des propriétés simples

Dans le format de table par défaut, les cmdlets Azure PowerShell n’affichent pas toutes les propriétés disponibles. Vous pouvez obtenir toutes les propriétés à l’aide de la cmdlet [Format-List](/powershell/module/microsoft.powershell.utility/format-list), ou en dirigeant la sortie vers `Select-Object *` :

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

Une fois que vous connaissez les noms des propriétés qui vous intéressent, vous pouvez les utiliser avec `Select-Object` pour les obtenir directement :

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

La sortie obtenue avec `Select-Object` est toujours formatée pour afficher les informations demandées. Pour en savoir plus sur l’utilisation du formatage avec la requête de résultats de cmdlet, consultez [Formater une sortie de cmdlet Azure PowerShell](formatting-output.md).

## <a name="select-nested-properties"></a>Sélectionner des propriétés imbriquées

Certaines propriétés dans la sortie de cmdlet Azure PowerShell utilisent des objets imbriqués, comme la propriété `StorageProfile` de la sortie `Get-AzVM`. Pour obtenir une valeur d’une propriété imbriquée, renseignez un nom d’affichage et le chemin d’accès complet à la valeur que vous souhaitez inspecter dans un argument de dictionnaire dans `Select-Object` :

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

Chaque argument de dictionnaire sélectionne une propriété de l’objet. La propriété à extraire doit faire partie d’une expression.

## <a name="filter-results"></a>Filtrer les résultats 

La cmdlet `Where-Object` vous permet de filtrer les résultats selon la valeur de propriété de votre choix, y compris des propriétés imbriquées. L’exemple suivant montre comment utiliser `Where-Object` pour trouver les machines virtuelles dans un groupe de ressources.

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

Vous pouvez diriger les résultats de `Select-Object` et `Where-Object` l’un vers l’autre. À des fins de performances, nous vous recommandons de toujours placer l’opération `Where-Object` avant `Select-Object` :

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