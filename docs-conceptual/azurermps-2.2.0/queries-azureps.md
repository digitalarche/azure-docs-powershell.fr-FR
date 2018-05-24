---
title: Exécution de requêtes de ressources Azure et mise en forme des résultats | Microsoft Docs
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: d8c8720cbbc4d584225d765d862c912bd9aee8cb
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="querying-for-azure-resources"></a><span data-ttu-id="465be-103">Exécution de requêtes de ressources Azure</span><span class="sxs-lookup"><span data-stu-id="465be-103">Querying for Azure resources</span></span>

<span data-ttu-id="465be-104">Vous pouvez effectuer des requêtes dans PowerShell en utilisant les applets de commande intégrées.</span><span class="sxs-lookup"><span data-stu-id="465be-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="465be-105">Dans PowerShell, les noms des applets de commande ont le format suivant : **_Verbe-Substantif_**.</span><span class="sxs-lookup"><span data-stu-id="465be-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="465be-106">Les applets de commande contenant le verbe **_Get_** sont les applets de commande de requête.</span><span class="sxs-lookup"><span data-stu-id="465be-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="465be-107">Les substantifs des applets de commande correspondent aux types des ressources Azure sur lesquelles sont exécutés les verbes des applets de commande.</span><span class="sxs-lookup"><span data-stu-id="465be-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>


## <a name="selecting-simple-properties"></a><span data-ttu-id="465be-108">Sélectionner des propriétés simples</span><span class="sxs-lookup"><span data-stu-id="465be-108">Selecting simple properties</span></span>

<span data-ttu-id="465be-109">Azure PowerShell a une mise en forme par défaut prédéfinie pour chaque applet de commande.</span><span class="sxs-lookup"><span data-stu-id="465be-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="465be-110">Pour chaque type de ressources, les propriétés les plus courantes sont automatiquement affichées sous forme de tableau ou de liste.</span><span class="sxs-lookup"><span data-stu-id="465be-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="465be-111">Pour plus d’informations sur la mise en forme de la sortie, consultez [Mise en forme des résultats de requête](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="465be-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="465be-112">Utilisez l’applet de commande `Get-AzureRmVM` pour obtenir la liste des machines virtuelles dans votre compte.</span><span class="sxs-lookup"><span data-stu-id="465be-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```powershell
Get-AzureRmVM
```

<span data-ttu-id="465be-113">La sortie par défaut est automatiquement présentée sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="465be-113">The default output is automatically formatted as a table.</span></span>

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="465be-114">Vous pouvez utiliser l’applet de commande `Select-Object` pour sélectionner uniquement les propriétés qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="465be-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```powershell
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="465be-115">Sélectionner des propriétés imbriquées complexes</span><span class="sxs-lookup"><span data-stu-id="465be-115">Selecting complex nested properties</span></span>

<span data-ttu-id="465be-116">Si la propriété que vous souhaitez sélectionner est imbriquée en profondeur dans la sortie JSON, vous devez fournir le chemin complet à cette propriété imbriquée.</span><span class="sxs-lookup"><span data-stu-id="465be-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="465be-117">L’exemple suivant montre comment sélectionner le nom de la machine virtuelle et le type de système d’exploitation à partir de l’applet de commande `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="465be-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a><span data-ttu-id="465be-118">Filtrer les résultats à l’aide de l’applet de commande Where-Object</span><span class="sxs-lookup"><span data-stu-id="465be-118">Filter result using the Where-Object cmdlet</span></span>

<span data-ttu-id="465be-119">L’applet de commande `Where-Object` vous permet de filtrer les résultats selon la valeur de propriété de votre choix.</span><span class="sxs-lookup"><span data-stu-id="465be-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="465be-120">Dans l’exemple suivant, le filtre sélectionne uniquement les machines virtuelles dont le nom contient le texte « RGD ».</span><span class="sxs-lookup"><span data-stu-id="465be-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```powershell
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="465be-121">Dans l’exemple suivant, les résultats retournent les machines virtuelles dont la taille vmSize est « Standard_DS1_V2 ».</span><span class="sxs-lookup"><span data-stu-id="465be-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```powershell
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```
