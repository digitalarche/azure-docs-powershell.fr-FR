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
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Dernières modifications de Microsoft Azure PowerShell 4.0.0

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell. Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance. Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.

## <a name="table-of-contents"></a>Sommaire

- [Dernières modifications des applets de commande Compute](#breaking-changes-to-compute-cmdlets)
- [Dernières modifications des applets de commande EventHub](#breaking-changes-to-eventhub-cmdlets)
- [Dernières modifications des applets de commande Insights](#breaking-changes-to-insights-cmdlets)
- [Dernières modifications des applets de commande Network](#breaking-changes-to-network-cmdlets)
- [Dernières modifications des applets de commande ServiceBus](#breaking-changes-to-servicebus-cmdlets)
- [Dernières modifications des applets de commande Sql](#breaking-changes-to-sql-cmdlets)
- [Dernières modifications des applets de commande Storage](#breaking-changes-to-storage-cmdlets)
- [Dernières modifications des applets de commande Profile](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>Dernières modifications des applets de commande Compute

Les types de sortie suivants affectaient cette version :

### <a name="psvirtualmachine"></a>PSVirtualMachine
- Les propriétés de niveau supérieur `DataDiskNames` et `NetworkInterfaceIDs` de l’objet `PSVirtualMachine` ont été supprimées du type de sortie. Ces propriétés ont toujours été disponibles dans les propriétés `StorageProfile` et `NetworkProfile` de l’objet `PSVirtualMachine` ; il s’agit ici de la méthode d’accès à suivre à l’avenir.
- Cette modification affecte les applets de commande suivantes :
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

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Dernières modifications des applets de commande EventHub

Les applets de commande suivantes affectaient cette version :

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.

## <a name="breaking-changes-to-insights-cmdlets"></a>Dernières modifications des applets de commande Insights

Les applets de commande suivantes affectaient cette version :
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- Cette applet de commande a été dépréciée.

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- La sortie de cette applet de commande a été modifiée d’une liste comportant un seul objet en un objet unique ; cette objet inclut l’ID de requête et le code de statut.
    
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
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- Cette applet de commande a été dépréciée.
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- Chaque élément de la sortie (une liste d’objets) de cette applet de commande est déprécié, autrement dit au lieu de renvoyer des objets avec la structure `{ Id, Location, Name, Tags, Properties }`, ils renverront des objets présentant la structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, ce qui correspond à l’ensemble des attributs d’une ressource Azure, auxquels s’ajoutent les attributs d’une instance AlertRuleResource au niveau supérieur.
    
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
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- Le champ `AutoscaleSettingResourceName` est déprécié, car il comporte toujours la même valeur dans le champ `Name`.

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
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- La sortie de cette applet de commande sera modifiée de `Boolean` en un objet comportant `RequestId` et `StatusCode`.

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
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- La sortie de cette applet de commande sera modifiée d’un objet comportant l’ID de requête, le code de statut et la ressource mise à jour ou nouvellement créée.
    
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
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- La commande sera renommée en `Update-AzureRmDiagnsoticSettings`.

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Dernières modifications des applets de commande Network

Les applets de commande suivantes affectaient cette version :

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- Le paramètre `EnableBgp` a été modifiée pour prendre une valeur `boolean` en lieu et place d’une valeur `string`.

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Dernières modifications des applets de commande ServiceBus

Les applets de commande suivantes affectaient cette version :

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- La propriété `ResourceGroupName` a été supprimée du type de sortie `NamespaceAttributes`.

## <a name="breaking-changes-to-sql-cmdlets"></a>Dernières modifications des applets de commande Sql

Les applets de commande suivantes affectaient cette version :

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- Le paramètre `Tag` a été renommé.
- Le paramètre `GracePeriodWithDataLossHour` a été renommé en `GracePeriodWithDataLossHours`.

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- Le paramètre `Tag` a été renommé.
- Le paramètre `GracePeriodWithDataLossHour` a été renommé en `GracePeriodWithDataLossHours`.

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- Le paramètre `Tag` a été renommé.

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- Le paramètre `Tag` a été renommé.

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- Le paramètre `PartnerResourceGroupName` a été renommé.
- Le paramètre `PartnerServerName` a été renommé.

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- La valeur `Usage_Anomaly` n’est plus valide pour le paramètre `ExcludedDetectionType`.

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- La valeur `Usage_Anomaly` n’est plus valide pour le paramètre `ExcludedDetectionType`.

## <a name="breaking-changes-to-storage-cmdlets"></a>Dernières modifications des applets de commande Storage

Les propriétés de type de sortie suivantes affectaient cette version :

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Cette modification affecte les applets de commande suivantes :
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- Cette modification affecte les applets de commande suivantes :
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- Cette modification affecte les applets de commande suivantes :
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- Les propriétés suivantes ont été supprimées de ce type (_remarque_ : elles sont toujours identifiées dans la propriété `DefaultRequestOptions`) :
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- Cette modification affecte les applets de commande suivantes :
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

## <a name="breaking-changes-to-profile-cmdlets"></a>Dernières modifications des applets de commande Profile

Les applets de commande suivantes et les types de sorties d’applet de commande ont été modifiés dans cette version.

### <a name="add-azurermaccount-breaking-changes"></a>Dernières modifications de Add-AzureRmAccount

- Le paramètre de ```EnvironmentName``` a été supprimé et remplacé par ```Environment``` ; l’instance ```Environment``` comporte désormais une chaîne, pas d’objet ```AzureEnvironment```.

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Select-AzureRmProfile a été renommée Import-AzureRmContext

```Select-AzureRmProfile``` a été renommée ```Import-AzureRmContext```.

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Save-AzureRmProfile a été renommée Save-AzureRmContext.

```Save-AzureRmProfile``` a été renommée ```Save-AzureRmContext```

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>Dernières modifications du type de sortie PSAzureContext

- La propriété ```TokenCache``` a été modifiée d’un type implémentant ```IAzureTokenCache``` en lieu et place d’une instance ```byte[]```.

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

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>Dernières modifications du type de sortie PSAzureAccount

- La propriété ```AccountType``` a été modifiée en ```Type```.

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

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>Dernières modifications du type de sortie PSAzureSubscription
- La propriété ```SubscriptionId``` a été modifiée en ```Id```.

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

- La propriété ```SubscriptionName``` a été modifiée en ```Name```.

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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>Dernières modifications du type de sortie PSAzureTenant

- La propriété ```TenantId``` a été modifiée en ```Id```.

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

- La propriété ```Domain``` a été modifiée en ```Directory```.

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
