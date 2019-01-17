---
title: Mettre en forme la sortie de l’applet de commande Azure PowerShell
description: Mise en forme la sortie de l’applet de commande pour Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: d655be02df40049d82d686667684b7b26a2c19ea
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342414"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="c3f55-103">Mettre en forme la sortie de l’applet de commande Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c3f55-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="c3f55-104">Par défaut, chaque applet de commande Azure PowerShell applique une mise en forme à sa sortie pour la rendre lisible.</span><span class="sxs-lookup"><span data-stu-id="c3f55-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="c3f55-105">PowerShell vous permet de convertir ou de mettre en forme une sortie d’applet de commande en transmettant à une des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3f55-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="c3f55-106">Mise en forme</span><span class="sxs-lookup"><span data-stu-id="c3f55-106">Formatting</span></span>      | <span data-ttu-id="c3f55-107">Conversion</span><span class="sxs-lookup"><span data-stu-id="c3f55-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="c3f55-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="c3f55-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="c3f55-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="c3f55-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="c3f55-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="c3f55-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="c3f55-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="c3f55-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="c3f55-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="c3f55-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="c3f55-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="c3f55-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="c3f55-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="c3f55-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="c3f55-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="c3f55-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="c3f55-116">La mise en forme est utilisée pour l’affichage dans un terminal PowerShell, et la conversion pour la génération de données devant être consommées par d’autres scripts ou programmes.</span><span class="sxs-lookup"><span data-stu-id="c3f55-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="c3f55-117">Format de sortie de la table</span><span class="sxs-lookup"><span data-stu-id="c3f55-117">Table output format</span></span>

<span data-ttu-id="c3f55-118">Par défaut, les applets de commande Azure PowerShell sortent les données sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="c3f55-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="c3f55-119">Ce format n’affiche pas toutes les informations de la ressource demandée :</span><span class="sxs-lookup"><span data-stu-id="c3f55-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="c3f55-120">La largeur de la fenêtre de votre session PowerShell peut avoir une incidence sur la quantité de données affichées par `Format-Table`.</span><span class="sxs-lookup"><span data-stu-id="c3f55-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="c3f55-121">Pour limiter le résultat à des propriétés spécifiques et les trier, les noms de propriété peuvent être fournis en tant qu’arguments à `Format-Table` :</span><span class="sxs-lookup"><span data-stu-id="c3f55-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="c3f55-122">Format de sortie en liste</span><span class="sxs-lookup"><span data-stu-id="c3f55-122">List output format</span></span>

<span data-ttu-id="c3f55-123">Le format de sortie en liste génère deux colonnes, les noms de propriété suivis de la valeur.</span><span class="sxs-lookup"><span data-stu-id="c3f55-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="c3f55-124">Pour les objets complexes, le type de l’objet est affiché à la place.</span><span class="sxs-lookup"><span data-stu-id="c3f55-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="c3f55-125">Certains champs ont été supprimés dans la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="c3f55-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="c3f55-126">Comme `Format-Table`, les noms de propriété peuvent être fournis pour limiter et trier la sortie :</span><span class="sxs-lookup"><span data-stu-id="c3f55-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="c3f55-127">Format de sortie large</span><span class="sxs-lookup"><span data-stu-id="c3f55-127">Wide output format</span></span>

<span data-ttu-id="c3f55-128">Le format de sortie large ne produit qu’un seul nom de propriété par requête.</span><span class="sxs-lookup"><span data-stu-id="c3f55-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="c3f55-129">La propriété qui s’affiche peut être contrôlée en donnant une propriété en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="c3f55-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="c3f55-130">Format de sortie personnalisée</span><span class="sxs-lookup"><span data-stu-id="c3f55-130">Custom output format</span></span>

<span data-ttu-id="c3f55-131">Le type de sortie `Custom-Format` est destiné à la mise en forme des objets personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c3f55-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="c3f55-132">Sans aucun argument, il se comporte comme `Format-List`, mais affiche les noms de propriété des classes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c3f55-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="c3f55-133">Certains champs ont été supprimés dans la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="c3f55-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="c3f55-134">Le fait d’attribuer des noms de propriété en tant qu’arguments à `Custom-Format` affiche les paires propriété/valeur pour les objets personnalisés définis comme valeurs :</span><span class="sxs-lookup"><span data-stu-id="c3f55-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="c3f55-135">Certains champs ont été supprimés dans la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="c3f55-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="c3f55-136">Conversion en d’autres formats de données</span><span class="sxs-lookup"><span data-stu-id="c3f55-136">Conversion to other data formats</span></span>

<span data-ttu-id="c3f55-137">La famille `ConvertTo-*` d’applets de commande permet de convertir les résultats des applets de commande Azure PowerShell en formats lisible par une machine.</span><span class="sxs-lookup"><span data-stu-id="c3f55-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="c3f55-138">Pour obtenir uniquement certaines propriétés dans les résultats d’Azure PowerShell, utilisez la commande `Select-Object` dans un canal avant d’effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="c3f55-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="c3f55-139">Les exemples suivants montrent les différents types de sortie que chaque conversion génère.</span><span class="sxs-lookup"><span data-stu-id="c3f55-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="c3f55-140">Conversion au format CSV</span><span class="sxs-lookup"><span data-stu-id="c3f55-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="c3f55-141">Conversion au format JSON</span><span class="sxs-lookup"><span data-stu-id="c3f55-141">Conversion to JSON</span></span>

<span data-ttu-id="c3f55-142">La sortie JSON ne développe pas toutes les propriétés par défaut.</span><span class="sxs-lookup"><span data-stu-id="c3f55-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="c3f55-143">Pour changer la profondeur des propriétés développées, utilisez l’argument `-Depth`.</span><span class="sxs-lookup"><span data-stu-id="c3f55-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="c3f55-144">Par défaut, la profondeur de développement est `2`.</span><span class="sxs-lookup"><span data-stu-id="c3f55-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="c3f55-145">Certains champs ont été supprimés dans la sortie suivante.</span><span class="sxs-lookup"><span data-stu-id="c3f55-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="c3f55-146">Conversion au format XML</span><span class="sxs-lookup"><span data-stu-id="c3f55-146">Conversion to XML</span></span>

<span data-ttu-id="c3f55-147">L’applet de commande `ConvertTo-XML` convertit l’objet de réponse d’Azure PowerShell en objet XML pur, qui peut être traité comme tout autre objet XML dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c3f55-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="c3f55-148">Conversion au format HTML</span><span class="sxs-lookup"><span data-stu-id="c3f55-148">Conversion to HTML</span></span>

<span data-ttu-id="c3f55-149">La conversion d’un objet au format HTML génère une sortie qui est restituée sous la forme d’un tableau HTML.</span><span class="sxs-lookup"><span data-stu-id="c3f55-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="c3f55-150">Le rendu du contenu HTML varie selon le comportement de votre navigateur à restituer des tableaux qui ne contiennent aucune information de largeur.</span><span class="sxs-lookup"><span data-stu-id="c3f55-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="c3f55-151">Aucun objet de classe personnalisée n’est développé.</span><span class="sxs-lookup"><span data-stu-id="c3f55-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```