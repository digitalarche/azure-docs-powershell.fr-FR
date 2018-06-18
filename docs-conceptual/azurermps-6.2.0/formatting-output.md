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
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323048"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="b2f13-103">Mettre en forme la sortie de l’applet de commande Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2f13-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="b2f13-104">Par défaut, chaque applet de commande Azure PowerShell met en forme la sortie selon des paramètres prédéfinis pour faciliter la lecture.</span><span class="sxs-lookup"><span data-stu-id="b2f13-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="b2f13-105">PowerShell offre également une grande flexibilité pour adapter la sortie ou convertir la sortie de l’applet de commande dans un format différent. Pour cela, vous pouvez utiliser les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2f13-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="b2f13-106">Mise en forme</span><span class="sxs-lookup"><span data-stu-id="b2f13-106">Formatting</span></span>      | <span data-ttu-id="b2f13-107">Conversion</span><span class="sxs-lookup"><span data-stu-id="b2f13-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="b2f13-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="b2f13-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="b2f13-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="b2f13-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="b2f13-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="b2f13-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="b2f13-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="b2f13-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="b2f13-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="b2f13-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="b2f13-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="b2f13-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="b2f13-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="b2f13-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="b2f13-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="b2f13-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="b2f13-116">Exemples de mise en forme</span><span class="sxs-lookup"><span data-stu-id="b2f13-116">Format examples</span></span>

<span data-ttu-id="b2f13-117">Dans cet exemple, nous obtenons une liste des machines virtuelles Azure créées dans notre abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="b2f13-117">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="b2f13-118">Par défaut, la commande `Get-AzureRmVM` présente la sortie sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="b2f13-118">The `Get-AzureRmVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="b2f13-119">Si vous souhaitez limiter les colonnes retournées, utilisez l’applet de commande `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="b2f13-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="b2f13-120">Dans l’exemple suivant, nous obtenons la même liste de machines virtuelles, mais nous limitons la sortie pour afficher uniquement le nom de la machine virtuelle, le groupe de ressources et l’emplacement de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b2f13-120">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="b2f13-121">Le paramètre `-Autosize` redimensionne les colonnes en fonction de la taille des données.</span><span class="sxs-lookup"><span data-stu-id="b2f13-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="b2f13-122">La sortie peut également être mise en forme dans une liste.</span><span class="sxs-lookup"><span data-stu-id="b2f13-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="b2f13-123">L’exemple suivant définit ce format à l’aide de l’applet de commande `Format-List`.</span><span class="sxs-lookup"><span data-stu-id="b2f13-123">The following example shows this using the`Format-List` cmdlet.</span></span>

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

## <a name="convert-to-other-data-types"></a><span data-ttu-id="b2f13-124">Conversion en d’autres types de données</span><span class="sxs-lookup"><span data-stu-id="b2f13-124">Convert to other data types</span></span>

<span data-ttu-id="b2f13-125">PowerShell permet également de prendre la sortie de la commande et de la convertir en plusieurs formats de données.</span><span class="sxs-lookup"><span data-stu-id="b2f13-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="b2f13-126">Dans l’exemple suivant, nous utilisons l’applet de commande `Select-Object` pour obtenir les attributs des machines virtuelles créées dans notre abonnement, et nous convertissons la sortie au format CSV pour pouvoir ensuite l’importer facilement dans une base de données ou une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="b2f13-126">In the following example the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="b2f13-127">La sortie peut également être convertie au format JSON.</span><span class="sxs-lookup"><span data-stu-id="b2f13-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="b2f13-128">L’exemple suivant crée la même liste de machines virtuelles, mais utilise le format de sortie JSON à la place.</span><span class="sxs-lookup"><span data-stu-id="b2f13-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

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
