---
title: Mettre en forme la sortie de l’applet de commande Azure PowerShell
description: Mise en forme la sortie de l’applet de commande pour Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/07/2018
ms.openlocfilehash: 833c82903305f99be5ad43f707e22644bb568abe
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383904"
---
# <a name="format-azurepowershell-cmdlet-output"></a>Mettre en forme la sortie de l’applet de commande Azure PowerShell

Par défaut, chaque applet de commande Azure PowerShell met en forme la sortie selon des paramètres prédéfinis pour faciliter la lecture.  PowerShell offre également une grande flexibilité pour adapter la sortie ou convertir la sortie de l’applet de commande dans un format différent. Pour cela, vous pouvez utiliser les applets de commande suivantes :

| Mise en forme      | Conversion       |
|-----------------|------------------|
| [Format-Custom](/powershell/module/microsoft.powershell.utility/format-custom) | [ConvertTo-Csv](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [Format-List](/powershell/module/microsoft.powershell.utility/format-list)   | [ConvertTo-Html](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [Format-Table](/powershell/module/microsoft.powershell.utility/format-table)  | [ConvertTo-Json](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [Format-Wide](/powershell/module/microsoft.powershell.utility/format-wide)   | [ConvertTo-Xml](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a>Exemples de mise en forme

Dans cet exemple, nous obtenons une liste des machines virtuelles Azure créées dans notre abonnement par défaut.  Par défaut, la commande `Get-AzureRmVM` présente la sortie sous forme de tableau.

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Si vous souhaitez limiter les colonnes retournées, utilisez l’applet de commande `Format-Table`. Dans l’exemple suivant, nous obtenons la même liste de machines virtuelles, mais nous limitons la sortie pour afficher uniquement le nom de la machine virtuelle, le groupe de ressources et l’emplacement de la machine virtuelle.  Le paramètre `-Autosize` redimensionne les colonnes en fonction de la taille des données.

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

La sortie peut également être mise en forme dans une liste. L’exemple suivant définit ce format à l’aide de l’applet de commande `Format-List`.

```azurepowershell-interactive
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a>Conversion en d’autres types de données

PowerShell permet également de prendre la sortie de la commande et de la convertir en plusieurs formats de données. Dans l’exemple suivant, nous utilisons l’applet de commande `Select-Object` pour obtenir les attributs des machines virtuelles créées dans notre abonnement, et nous convertissons la sortie au format CSV pour pouvoir ensuite l’importer facilement dans une base de données ou une feuille de calcul.

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

La sortie peut également être convertie au format JSON.  L’exemple suivant crée la même liste de machines virtuelles, mais utilise le format de sortie JSON à la place.

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
