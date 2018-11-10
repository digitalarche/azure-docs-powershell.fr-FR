---
title: Interroger la sortie d’applets de commande Azure PowerShell
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bd1bea43303e9f5a2b46d63a3ac51b4c4031b9f
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275025"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a>Interroger la sortie d’applets de commande Azure PowerShell

Vous pouvez effectuer des requêtes dans PowerShell en utilisant les applets de commande intégrées. Dans PowerShell, les noms des applets de commande ont le format suivant : **_Verbe-Substantif_**. Les applets de commande contenant le verbe **_Get_** sont les applets de commande de requête. Les substantifs des applets de commande correspondent aux types des ressources Azure sur lesquelles sont exécutés les verbes des applets de commande.

## <a name="select-simple-properties"></a>Sélectionner des propriétés simples

Azure PowerShell a une mise en forme par défaut prédéfinie pour chaque applet de commande. Pour chaque type de ressources, les propriétés les plus courantes sont automatiquement affichées sous forme de tableau ou de liste. Pour plus d’informations sur la mise en forme de la sortie, consultez [Mise en forme des résultats de requête](formatting-output.md).

Utilisez l’applet de commande `Get-AzureRmVM` pour obtenir la liste des machines virtuelles dans votre compte.

```azurepowershell-interactive
Get-AzureRmVM
```

La sortie par défaut est automatiquement présentée sous forme de tableau.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

Vous pouvez utiliser l’applet de commande `Select-Object` pour sélectionner uniquement les propriétés qui vous intéressent.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a>Sélectionner des propriétés imbriquées complexes

Si la propriété dont vous avez besoin est imbriquée dans la sortie JSON, vous devez fournir le chemin complet vers cette propriété. L’exemple suivant montre comment sélectionner le nom de la machine virtuelle et le type de système d’exploitation à partir de l’applet de commande `Get-AzureRmVM`.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a>Filtrer les résultats à l’aide de l’applet de commande Where-Object

L’applet de commande `Where-Object` vous permet de filtrer les résultats selon la valeur de propriété de votre choix. Dans l’exemple suivant, le filtre sélectionne uniquement les machines virtuelles dont le nom contient le texte « RGD ».

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Dans l’exemple suivant, les résultats retournent les machines virtuelles dont la taille vmSize est « Standard_DS1_V2 ».

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```