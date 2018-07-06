---
title: Interroger la sortie d’applets de commande Azure PowerShell
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/08/2018
ms.openlocfilehash: daa39ada5b4e969264b6e8596dc7b090bb196fd5
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406250"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="ba8ce-103">Interroger la sortie d’applets de commande Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ba8ce-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="ba8ce-104">Vous pouvez effectuer des requêtes dans PowerShell en utilisant les applets de commande intégrées.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="ba8ce-105">Dans PowerShell, les noms des applets de commande ont le format suivant : **_Verbe-Substantif_**.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="ba8ce-106">Les applets de commande contenant le verbe **_Get_** sont les applets de commande de requête.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="ba8ce-107">Les substantifs des applets de commande correspondent aux types des ressources Azure sur lesquelles sont exécutés les verbes des applets de commande.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="ba8ce-108">Sélectionner des propriétés simples</span><span class="sxs-lookup"><span data-stu-id="ba8ce-108">Select simple properties</span></span>

<span data-ttu-id="ba8ce-109">Azure PowerShell a une mise en forme par défaut prédéfinie pour chaque applet de commande.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="ba8ce-110">Pour chaque type de ressources, les propriétés les plus courantes sont automatiquement affichées sous forme de tableau ou de liste.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="ba8ce-111">Pour plus d’informations sur la mise en forme de la sortie, consultez [Mise en forme des résultats de requête](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="ba8ce-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="ba8ce-112">Utilisez l’applet de commande `Get-AzureRmVM` pour obtenir la liste des machines virtuelles dans votre compte.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="ba8ce-113">La sortie par défaut est automatiquement présentée sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="ba8ce-114">Vous pouvez utiliser l’applet de commande `Select-Object` pour sélectionner uniquement les propriétés qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="ba8ce-115">Sélectionner des propriétés imbriquées complexes</span><span class="sxs-lookup"><span data-stu-id="ba8ce-115">Select complex nested properties</span></span>

<span data-ttu-id="ba8ce-116">Si la propriété que vous souhaitez sélectionner est imbriquée en profondeur dans la sortie JSON, vous devez fournir le chemin complet à cette propriété imbriquée.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="ba8ce-117">L’exemple suivant montre comment sélectionner le nom de la machine virtuelle et le type de système d’exploitation à partir de l’applet de commande `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="ba8ce-118">Filtrer les résultats à l’aide de l’applet de commande Where-Object</span><span class="sxs-lookup"><span data-stu-id="ba8ce-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="ba8ce-119">L’applet de commande `Where-Object` vous permet de filtrer les résultats selon la valeur de propriété de votre choix.</span><span class="sxs-lookup"><span data-stu-id="ba8ce-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="ba8ce-120">Dans l’exemple suivant, le filtre sélectionne uniquement les machines virtuelles dont le nom contient le texte « RGD ».</span><span class="sxs-lookup"><span data-stu-id="ba8ce-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="ba8ce-121">Dans l’exemple suivant, les résultats retournent les machines virtuelles dont la taille vmSize est « Standard_DS1_V2 ».</span><span class="sxs-lookup"><span data-stu-id="ba8ce-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```