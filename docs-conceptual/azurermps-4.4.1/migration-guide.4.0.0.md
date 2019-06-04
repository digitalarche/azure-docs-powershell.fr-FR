---
title: Dernières modifications de Microsoft Azure PowerShell 4.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version 4.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: b966025532a3bb4d4423ac1a7a6d398988758043
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534602"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="248ca-103">Dernières modifications de Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="248ca-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="248ca-104">Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="248ca-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="248ca-105">Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance.</span><span class="sxs-lookup"><span data-stu-id="248ca-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="248ca-106">Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.</span><span class="sxs-lookup"><span data-stu-id="248ca-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="248ca-107">Sommaire</span><span class="sxs-lookup"><span data-stu-id="248ca-107">Table of Contents</span></span>

- [<span data-ttu-id="248ca-108">Dernières modifications des applets de commande Compute</span><span class="sxs-lookup"><span data-stu-id="248ca-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="248ca-109">Dernières modifications des applets de commande EventHub</span><span class="sxs-lookup"><span data-stu-id="248ca-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="248ca-110">Dernières modifications des applets de commande Insights</span><span class="sxs-lookup"><span data-stu-id="248ca-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="248ca-111">Dernières modifications des applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="248ca-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="248ca-112">Dernières modifications des applets de commande ServiceBus</span><span class="sxs-lookup"><span data-stu-id="248ca-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="248ca-113">Dernières modifications des applets de commande Sql</span><span class="sxs-lookup"><span data-stu-id="248ca-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="248ca-114">Dernières modifications des applets de commande Storage</span><span class="sxs-lookup"><span data-stu-id="248ca-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="248ca-115">Dernières modifications des applets de commande Profile</span><span class="sxs-lookup"><span data-stu-id="248ca-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="248ca-116">Dernières modifications des applets de commande Compute</span><span class="sxs-lookup"><span data-stu-id="248ca-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="248ca-117">Les types de sortie suivants affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="248ca-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="248ca-118">PSVirtualMachine</span></span>
- <span data-ttu-id="248ca-119">Les propriétés de niveau supérieur `DataDiskNames` et `NetworkInterfaceIDs` de l’objet `PSVirtualMachine` ont été supprimées du type de sortie.</span><span class="sxs-lookup"><span data-stu-id="248ca-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="248ca-120">Ces propriétés ont toujours été disponibles dans les propriétés `StorageProfile` et `NetworkProfile` de l’objet `PSVirtualMachine` ; il s’agit ici de la méthode d’accès à suivre à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="248ca-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="248ca-121">Cette modification affecte les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="248ca-121">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="248ca-122">Dernières modifications des applets de commande EventHub</span><span class="sxs-lookup"><span data-stu-id="248ca-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="248ca-123">Les applets de commande suivantes affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="248ca-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="248ca-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="248ca-125">La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="248ca-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="248ca-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="248ca-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="248ca-127">La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="248ca-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="248ca-128">Dernières modifications des applets de commande Insights</span><span class="sxs-lookup"><span data-stu-id="248ca-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="248ca-129">Les applets de commande suivantes affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-129">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="248ca-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="248ca-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="248ca-131">Cette applet de commande a été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="248ca-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="248ca-132">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="248ca-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="248ca-133">La sortie de cette applet de commande a été modifiée d’une liste comportant un seul objet en un objet unique ; cette objet inclut l’ID de requête et le code de statut.</span><span class="sxs-lookup"><span data-stu-id="248ca-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="248ca-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="248ca-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="248ca-135">Cette applet de commande a été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="248ca-135">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="248ca-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="248ca-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="248ca-137">Chaque élément de la sortie (une liste d’objets) de cette applet de commande est déprécié, autrement dit au lieu de renvoyer des objets avec la structure `{ Id, Location, Name, Tags, Properties }`, ils renverront des objets présentant la structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, ce qui correspond à l’ensemble des attributs d’une ressource Azure, auxquels s’ajoutent les attributs d’une instance AlertRuleResource au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="248ca-137">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="248ca-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="248ca-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="248ca-139">Le champ `AutoscaleSettingResourceName` est déprécié, car il comporte toujours la même valeur dans le champ `Name`.</span><span class="sxs-lookup"><span data-stu-id="248ca-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="248ca-140">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="248ca-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="248ca-141">La sortie de cette applet de commande sera modifiée de `Boolean` en un objet comportant `RequestId` et `StatusCode`.</span><span class="sxs-lookup"><span data-stu-id="248ca-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="248ca-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="248ca-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="248ca-143">La sortie de cette applet de commande sera modifiée d’un objet comportant l’ID de requête, le code de statut et la ressource mise à jour ou nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="248ca-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="248ca-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="248ca-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="248ca-145">La commande sera renommée en `Update-AzureRmDiagnsoticSettings`.</span><span class="sxs-lookup"><span data-stu-id="248ca-145">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="248ca-146">Dernières modifications des applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="248ca-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="248ca-147">Les applets de commande suivantes affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="248ca-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="248ca-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="248ca-149">Le paramètre `EnableBgp` a été modifiée pour prendre une valeur `boolean` en lieu et place d’une valeur `string`.</span><span class="sxs-lookup"><span data-stu-id="248ca-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="248ca-150">Dernières modifications des applets de commande ServiceBus</span><span class="sxs-lookup"><span data-stu-id="248ca-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="248ca-151">Les applets de commande suivantes affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="248ca-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="248ca-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="248ca-153">La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="248ca-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="248ca-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="248ca-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="248ca-155">La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="248ca-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="248ca-156">Dernières modifications des applets de commande Sql</span><span class="sxs-lookup"><span data-stu-id="248ca-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="248ca-157">Les applets de commande suivantes affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="248ca-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="248ca-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="248ca-159">Le paramètre `Tag` a été renommé.</span><span class="sxs-lookup"><span data-stu-id="248ca-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="248ca-160">Le paramètre `GracePeriodWithDataLossHour` a été renommé en `GracePeriodWithDataLossHours`.</span><span class="sxs-lookup"><span data-stu-id="248ca-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="248ca-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="248ca-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="248ca-162">Le paramètre `Tag` a été renommé.</span><span class="sxs-lookup"><span data-stu-id="248ca-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="248ca-163">Le paramètre `GracePeriodWithDataLossHour` a été renommé en `GracePeriodWithDataLossHours`.</span><span class="sxs-lookup"><span data-stu-id="248ca-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="248ca-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="248ca-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="248ca-165">Le paramètre `Tag` a été renommé.</span><span class="sxs-lookup"><span data-stu-id="248ca-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="248ca-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="248ca-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="248ca-167">Le paramètre `Tag` a été renommé.</span><span class="sxs-lookup"><span data-stu-id="248ca-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="248ca-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="248ca-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="248ca-169">Le paramètre `PartnerResourceGroupName` a été renommé.</span><span class="sxs-lookup"><span data-stu-id="248ca-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="248ca-170">Le paramètre `PartnerServerName` a été renommé.</span><span class="sxs-lookup"><span data-stu-id="248ca-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="248ca-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="248ca-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="248ca-172">La valeur `Usage_Anomaly` n’est plus valide pour le paramètre `ExcludedDetectionType`.</span><span class="sxs-lookup"><span data-stu-id="248ca-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="248ca-173">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="248ca-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="248ca-174">La valeur `Usage_Anomaly` n’est plus valide pour le paramètre `ExcludedDetectionType`.</span><span class="sxs-lookup"><span data-stu-id="248ca-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="248ca-175">Dernières modifications des applets de commande Storage</span><span class="sxs-lookup"><span data-stu-id="248ca-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="248ca-176">Les propriétés de type de sortie suivantes affectaient cette version :</span><span class="sxs-lookup"><span data-stu-id="248ca-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="248ca-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="248ca-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="248ca-178">Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :</span><span class="sxs-lookup"><span data-stu-id="248ca-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="248ca-179">Cette modification affecte les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="248ca-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="248ca-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="248ca-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="248ca-181">Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :</span><span class="sxs-lookup"><span data-stu-id="248ca-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="248ca-182">Cette modification affecte les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="248ca-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="248ca-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="248ca-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="248ca-184">Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :</span><span class="sxs-lookup"><span data-stu-id="248ca-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="248ca-185">Cette modification affecte les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="248ca-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="248ca-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="248ca-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="248ca-187">Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :</span><span class="sxs-lookup"><span data-stu-id="248ca-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="248ca-188">Cette modification affecte les applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="248ca-188">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="248ca-189">Dernières modifications des applets de commande Profile</span><span class="sxs-lookup"><span data-stu-id="248ca-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="248ca-190">Les applets de commande suivantes et les types de sorties d’applet de commande ont été modifiés dans cette version.</span><span class="sxs-lookup"><span data-stu-id="248ca-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="248ca-191">Dernières modifications de Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="248ca-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="248ca-192">Le paramètre de ```EnvironmentName``` a été supprimé et remplacé par ```Environment``` ; l’instance ```Environment``` comporte désormais une chaîne, pas d’objet ```AzureEnvironment```.</span><span class="sxs-lookup"><span data-stu-id="248ca-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="248ca-193">Select-AzureRmProfile a été renommée Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="248ca-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="248ca-194">```Select-AzureRmProfile``` a été renommée ```Import-AzureRmContext```.</span><span class="sxs-lookup"><span data-stu-id="248ca-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="248ca-195">Save-AzureRmProfile a été renommée Save-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="248ca-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="248ca-196">```Save-AzureRmProfile``` a été renommée ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="248ca-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="248ca-197">Dernières modifications du type de sortie PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="248ca-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="248ca-198">La propriété ```TokenCache``` a été modifiée d’un type implémentant ```IAzureTokenCache``` en lieu et place d’une instance ```byte[]```.</span><span class="sxs-lookup"><span data-stu-id="248ca-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="248ca-199">Dernières modifications du type de sortie PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="248ca-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="248ca-200">La propriété ```AccountType``` a été modifiée en ```Type```.</span><span class="sxs-lookup"><span data-stu-id="248ca-200">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="248ca-201">Dernières modifications du type de sortie PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="248ca-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="248ca-202">La propriété ```SubscriptionId``` a été modifiée en ```Id```.</span><span class="sxs-lookup"><span data-stu-id="248ca-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="248ca-203">La propriété ```SubscriptionName``` a été modifiée en ```Name```.</span><span class="sxs-lookup"><span data-stu-id="248ca-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="248ca-204">Dernières modifications du type de sortie PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="248ca-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="248ca-205">La propriété ```TenantId``` a été modifiée en ```Id```.</span><span class="sxs-lookup"><span data-stu-id="248ca-205">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="248ca-206">La propriété ```Domain``` a été modifiée en ```Directory```.</span><span class="sxs-lookup"><span data-stu-id="248ca-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
