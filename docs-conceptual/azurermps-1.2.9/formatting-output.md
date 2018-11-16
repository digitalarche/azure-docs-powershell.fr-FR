---
title: Mise en forme des résultats de requête | Microsoft Docs
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 37f240d371150928f10cb2811c4bb5f1b585c2f3
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51580576"
---
# <a name="formatting-query-results"></a>Mise en forme des résultats de requête

Par défaut, chaque applet de commande PowerShell met en forme la sortie selon des paramètres prédéfinis pour faciliter la lecture.  PowerShell offre également une grande flexibilité pour adapter la sortie ou convertir la sortie de l’applet de commande dans un format différent. Pour cela, vous pouvez utiliser les applets de commande suivantes :

| Mise en forme      | Conversion       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a>Exemples de mise en forme

Dans cet exemple, nous obtenons une liste des machines virtuelles Azure créées dans notre abonnement par défaut.  Par défaut, la commande Get-AzureRmVM présente la sortie sous forme de tableau.

```powershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Si vous souhaitez limiter les colonnes retournées, utilisez l’applet de commande `Format-Table`. Dans l’exemple suivant, nous obtenons la même liste de machines virtuelles, mais nous limitons la sortie pour afficher uniquement le nom de la machine virtuelle, le groupe de ressources et l’emplacement de la machine virtuelle.  Le paramètre `-Autosize` redimensionne les colonnes en fonction de la taille des données.

```powershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

Si vous préférez, vous pouvez afficher les informations sous forme de liste. L’exemple suivant définit ce format à l’aide de l’applet de commande `Format-List`.

```powershell-interactive
Get-AzureVM | Format-List Name,VmId,Location,ResourceGroupName
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

## <a name="converting-to-other-data-types"></a>Conversion en d’autres types de données

PowerShell propose également plusieurs formats de sortie à utiliser selon vos besoins.  Dans l’exemple suivant, nous utilisons l’applet de commande `Select-Object` pour obtenir les attributs des machines virtuelles créées dans notre abonnement, et nous convertissons la sortie au format CSV pour pouvoir ensuite l’importer facilement dans une base de données ou une feuille de calcul.

```powershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

Vous pouvez aussi convertir la sortie au format JSON.  L’exemple suivant crée la même liste de machines virtuelles, mais utilise le format de sortie JSON à la place.

```powershell-interactive
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
