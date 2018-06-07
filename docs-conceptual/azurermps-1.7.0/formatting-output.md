---
title: Mise en forme des résultats de requête | Microsoft Docs
description: Comment effectuer une requête de ressources dans Azure et mettre en forme les résultats.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 9cef703f302651a48381dba70c0be23d4d24df0b
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821766"
---
# <a name="formatting-query-results"></a><span data-ttu-id="5a98d-103">Mise en forme des résultats de requête</span><span class="sxs-lookup"><span data-stu-id="5a98d-103">Formatting query results</span></span>

<span data-ttu-id="5a98d-104">Par défaut, chaque applet de commande PowerShell met en forme la sortie selon des paramètres prédéfinis pour faciliter la lecture.</span><span class="sxs-lookup"><span data-stu-id="5a98d-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="5a98d-105">PowerShell offre également une grande flexibilité pour adapter la sortie ou convertir la sortie de l’applet de commande dans un format différent. Pour cela, vous pouvez utiliser les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a98d-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="5a98d-106">Mise en forme</span><span class="sxs-lookup"><span data-stu-id="5a98d-106">Formatting</span></span>      | <span data-ttu-id="5a98d-107">Conversion</span><span class="sxs-lookup"><span data-stu-id="5a98d-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="5a98d-108">Exemples de mise en forme</span><span class="sxs-lookup"><span data-stu-id="5a98d-108">Formatting examples</span></span>

<span data-ttu-id="5a98d-109">Dans cet exemple, nous obtenons une liste des machines virtuelles Azure créées dans notre abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="5a98d-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="5a98d-110">Par défaut, la commande Get-AzureRmVM présente la sortie sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="5a98d-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="5a98d-111">Si vous souhaitez limiter les colonnes retournées, utilisez l’applet de commande `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="5a98d-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="5a98d-112">Dans l’exemple suivant, nous obtenons la même liste de machines virtuelles, mais nous limitons la sortie pour afficher uniquement le nom de la machine virtuelle, le groupe de ressources et l’emplacement de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5a98d-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="5a98d-113">Le paramètre `-Autosize` redimensionne les colonnes en fonction de la taille des données.</span><span class="sxs-lookup"><span data-stu-id="5a98d-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="5a98d-114">Si vous préférez, vous pouvez afficher les informations sous forme de liste.</span><span class="sxs-lookup"><span data-stu-id="5a98d-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="5a98d-115">L’exemple suivant définit ce format à l’aide de l’applet de commande `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="5a98d-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="5a98d-116">Conversion en d’autres types de données</span><span class="sxs-lookup"><span data-stu-id="5a98d-116">Converting to other data types</span></span>

<span data-ttu-id="5a98d-117">PowerShell propose également plusieurs formats de sortie à utiliser selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5a98d-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="5a98d-118">Dans l’exemple suivant, nous utilisons l’applet de commande `Select-Object` pour obtenir les attributs des machines virtuelles créées dans notre abonnement, et nous convertissons la sortie au format CSV pour pouvoir ensuite l’importer facilement dans une base de données ou une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="5a98d-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="5a98d-119">Vous pouvez aussi convertir la sortie au format JSON.</span><span class="sxs-lookup"><span data-stu-id="5a98d-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="5a98d-120">L’exemple suivant crée la même liste de machines virtuelles, mais utilise le format de sortie JSON à la place.</span><span class="sxs-lookup"><span data-stu-id="5a98d-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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
