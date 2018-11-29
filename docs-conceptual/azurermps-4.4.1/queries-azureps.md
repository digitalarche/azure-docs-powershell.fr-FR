---
title: Exécution de requêtes de ressources Azure et mise en forme des résultats | Microsoft Docs
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9a7627a25f9bbd196b1d615229e45a6e1ce7a7d9
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586443"
---
# <a name="querying-for-azure-resources"></a>Exécution de requêtes de ressources Azure

Vous pouvez effectuer des requêtes dans PowerShell en utilisant les applets de commande intégrées. Dans PowerShell, les noms des applets de commande ont le format suivant : **_Verbe-Substantif_**. Les applets de commande contenant le verbe **_Get_** sont les applets de commande de requête. Les substantifs des applets de commande correspondent aux types des ressources Azure sur lesquelles sont exécutés les verbes des applets de commande.

## <a name="selecting-simple-properties"></a>Sélectionner des propriétés simples

Azure PowerShell a une mise en forme par défaut prédéfinie pour chaque applet de commande. Pour chaque type de ressources, les propriétés les plus courantes sont automatiquement affichées sous forme de tableau ou de liste. Pour plus d’informations sur la mise en forme de la sortie, consultez [Mise en forme des résultats de requête](formatting-output.md).

Utilisez l’applet de commande `Get-AzureRmVM` pour obtenir la liste des machines virtuelles dans votre compte.

```powershell-interactive
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

```powershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Sélectionner des propriétés imbriquées complexes

Si la propriété que vous souhaitez sélectionner est imbriquée en profondeur dans la sortie JSON, vous devez fournir le chemin complet à cette propriété imbriquée. L’exemple suivant montre comment sélectionner le nom de la machine virtuelle et le type de système d’exploitation à partir de l’applet de commande `Get-AzureRmVM`.

```powershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Filtrer les résultats à l’aide de l’applet de commande Where-Object

L’applet de commande `Where-Object` vous permet de filtrer les résultats selon la valeur de propriété de votre choix. Dans l’exemple suivant, le filtre sélectionne uniquement les machines virtuelles dont le nom contient le texte « RGD ».

```powershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Dans l’exemple suivant, les résultats retournent les machines virtuelles dont la taille vmSize est « Standard_DS1_V2 ».

```powershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
