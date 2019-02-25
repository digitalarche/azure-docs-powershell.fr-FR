---
title: Dernières modifications de Microsoft Azure PowerShell 5.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version 5.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: b4cbeb1b523664fb49c4640eaafd56e3b843ebaa
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56144274"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Dernières modifications de Microsoft Azure PowerShell 5.0.0

Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell. Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance. Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.

## <a name="table-of-contents"></a>Sommaire

- [Dernières modifications des applets de commande ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
- [Dernières modifications des applets de commande Batch](#breaking-changes-to-batch-cmdlets)
- [Dernières modifications des applets de commande Compute](#breaking-changes-to-compute-cmdlets)
- [Dernières modifications des applets de commande EventHub](#breaking-changes-to-eventhub-cmdlets)
- [Dernières modifications des applets de commande Insights](#breaking-changes-to-insights-cmdlets)
- [Dernières modifications des applets de commande Network](#breaking-changes-to-network-cmdlets)
- [Dernières modifications des applets de commande Resources](#breaking-changes-to-resources-cmdlets)
- [Dernières modifications des applets de commande ServiceBus](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Dernières modifications des applets de commande ApiManagement

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- Les paramètres UserName et Password sont remplacés par une instance PSCredential.

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Dernières modifications des applets de commande Batch

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Le paramètre `Password` est remplacé par une chaîne sécurisée.

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Le paramètre `Password` est remplacé par une chaîne sécurisée.

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Le paramètre `Password` est remplacé par une chaîne sécurisée.

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - Le commutateur `RunElevated` a été remplacé par `UserIdentity`.

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Cela affecte par ailleurs la propriété `RunElevated` sur `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` et `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- Le constructeur `PSMultiInstanceSettings` ne prend plus de paramètre `numberOfInstances` requis, il prend plutôt un paramètre `coordinationCommandLine` requis.

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - La propriété `RunElevated` a été supprimée sur `PSCloudTask`. La propriété `UserIdentity` a été ajoutée pour remplacer `RunElevated`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Cela affecte par ailleurs la propriété `RunElevated` sur `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` et `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Plusieurs types**

- La propriété `SchedulingError` a été renommée sur `PSExitConditions`, en `PreProcessingError`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Plusieurs types**

- La propriété `SchedulingError` a été renommée sur `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` et `PSTaskExecutionInformation`, en `FailureInformation`.
  - `FailureInformation` est renvoyé lors de chaque défaillance de tâche. Sont concernés ici l’ensemble des erreurs de planification précédentes, les codes de sortie de tâche différents de 0 et les défaillances de chargement de fichiers de la nouvelle fonctionnalité de fichiers de sortie.
  - La structure restant identique, aucune modification de code n’est nécessaire lors de l’utilisation de ce type.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

Les instances suivantes sont également affectées : Get-AzureBatchPool, Get-AzureBatchSubtask et Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - L’instance `TargetDedicated` a été supprimée et remplacée par `TargetDedicatedComputeNodes` et `TargetLowPriorityComputeNodes`.
 - `TargetDedicatedComputeNodes` possède un alias `TargetDedicated`.

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Les instances suivantes sont également affectées : Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - Les propriétés `TargetDedicated` et `CurrentDedicated` sur `PSCloudPool` ont été renommées en `TargetDedicatedComputeNodes` et `CurrentDedicatedComputeNodes`.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**Type PSCloudPool**

- La propriété `ResizeError` a été renommée en `ResizeErrors` sur `PSCloudPool` ; il s’agit désormais d’une collection.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- La propriété `TargetDedicated` sur `PSPoolSpecification` a été renommée en `TargetDedicatedComputeNodes`.

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - La propriété `Name` a été supprimée et remplacée par `Path`.
 - `Path` possède un alias `Name`.

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Les instances suivantes sont également affectées : Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>Type **PSNodeFile**

 - La propriété `Name` sur `PSNodeFile` a été renommée en `Path`.

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- Les propriétés `PreviousState` et `State` de `PSSubtaskInformation` ne sont plus de type `TaskState`, mais de type `SubtaskState`.
  - Contrairement à `TaskState`, `SubtaskState` ne possède pas de valeur `Active`, dans la mesure où les sous-tâches ne peuvent pas présenter un état `Active`.

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Dernières modifications des applets de commande Compute

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- Les paramètres UserName et Password sont remplacés par une instance PSCredential.

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Dernières modifications des applets de commande EventHub

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- L’applet de commande New-AzureRmEventHubNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande New-AzureRmEventHubAuthorizationRule.
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- L’applet de commande Get-AzureRmEventHubNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande Get-AzureRmEventHubAuthorizationRule.
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- L’applet de commande Set-AzureRmEventHubNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande Set-AzureRmEventHubAuthorizationRule.
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- L’applet de commande Remove-AzureRmEventHubNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande Remove-AzureRmEventHubAuthorizationRule.
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- L’applet de commande New-AzureRmEventHubNamespaceKey a été supprimée. Utilisez l’applet de commande New-AzureRmEventHubKey.
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- L’applet de commande Get-AzureRmEventHubNamespaceKey a été supprimée. Utilisez l’applet de commande Get-AzureRmEventHubKey.
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- Les propriétés Status et Enabled de l’instance NamespceAttributes seront supprimées. 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- Les propriétés Status et Enabled de l’instance NamespceAttributes seront supprimées. 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- Les propriétés Status et Enabled de l’instance NamespceAttributes seront supprimées. 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- La propriété EventHubPath de l’instance ConsumerGroupAttributes sera supprimée.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- La propriété EventHubPath de l’instance ConsumerGroupAttributes sera supprimée.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- La propriété EventHubPath de l’instance ConsumerGroupAttributes sera supprimée.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Dernières modifications des applets de commande Insights

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- L’applet de commande **Add-AzureRMLogAlertRule** a été dépréciée.
- À compter du 1er octobre, cette applet de commande n’aura plus aucun effet, dans la mesure où cette fonctionnalité est en cours de transition vers les alertes de journal d’activité. Pour plus d’informations, consultez https://aka.ms/migratemealerts.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- L’applet de commande **Get-AzureRMUsage** a été dépréciée.

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Modification de sortie : le champ EventChannels de l’objet EventData (renvoyé par ces applets de commande) est déconseillé, car il renvoie désormais une valeur constante (Admin, Operation).

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Modification de sortie : la sortie de cette applet de commande sera tronquée, par l’élimination du champs des propriétés, ceci pour améliorer l’expérience utilisateur.

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Modification de sortie : le champ AutoscaleSettingResourceName sera déprécié, car il est toujours identique au champ Name.

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Modification de sortie : le type de sortie sera modifié pour renvoyer un seul objet contenant l’ID de requête et le code d’état.

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Dernières modifications des applets de commande Network

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Dernières modifications des applets de commande Resources

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- Le paramètre Password est remplacé par une instance SecureString.

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Dernières modifications des applets de commande ServiceBus

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- L’applet de commande Get-AzureRmServiceBusTopicAuthorizationRule a été supprimée. Utilisez l’applet de commande Get-AzureRmServiceBusAuthorizationRule.    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- L’applet de commande Get-AzureRmServiceBusTopicKey a été supprimée. Utilisez l’applet de commande Get-AzureRmServiceBusKey.

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- L’applet de commande New-AzureRmServiceBusTopicAuthorizationRule a été supprimée. Utilisez l’applet de commande New-AzureRmServiceBusAuthorizationRule.

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- L’applet de commande New-AzureRmServiceBusTopicKey a été supprimée. Utilisez l’applet de commande New-AzureRmServiceBusKey.

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- L’applet de commande Remove-AzureRmServiceBusTopicAuthorizationRule a été supprimée. Utilisez l’applet de commande Remove-AzureRmServiceBusAuthorizationRule.

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- L’applet de commande Set-AzureRmServiceBusTopicAuthorizationRule a été supprimée. Utilisez l’applet de commande Set-AzureRmServiceBusAuthorizationRule.

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- L’applet de commande New-AzureRmServiceBusNamespaceKey a été supprimée. Utilisez l’applet de commande New-AzureRmServiceBusKey.

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- L’applet de commande Get-AzureRmServiceBusQueueAuthorizationRule a été supprimée. Utilisez l’applet de commande Get-AzureRmServiceBusAuthorizationRule.

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- L’applet de commande Get-AzureRmServiceBusQueueKey a été supprimée. Utilisez l’applet de commande Get-AzureRmServiceBusKey.

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- L’applet de commande New-AzureRmServiceBusQueueAuthorizationRule a été supprimée. Utilisez l’applet de commande New-AzureRmServiceBusAuthorizationRule.

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- L’applet de commande New-AzureRmServiceBusQueueKey a été supprimée. Utilisez l’applet de commande New-AzureRmServiceBusKey.

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- L’applet de commande Remove-AzureRmServiceBusQueueAuthorizationRule a été supprimée. Utilisez l’applet de commande GRemove-AzureRmServiceBusAuthorizationRule.

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- L’applet de commande Set-AzureRmServiceBusQueueAuthorizationRule a été supprimée. Utilisez l’applet de commande Set-AzureRmServiceBusAuthorizationRule.

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- L’applet de commande Get-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande Get-AzureRmServiceBusAuthorizationRule.

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- L’applet de commande Get-AzureRmServiceBusNamespaceKey a été supprimée. Utilisez l’applet de commande Get-AzureRmServiceBusKey.

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- L’applet de commande New-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande New-AzureRmServiceBusAuthorizationRule.

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- L’applet de commande Remove-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande Remove-AzureRmServiceBusAuthorizationRule.

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- L’applet de commande Set-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée. Utilisez l’applet de commande Set-AzureRmServiceBusAuthorizationRule.

### <a name="type-namespaceattributes"></a>**Type NamespaceAttributes**
- Les propriétés suivantes ont été supprimées :
    - activé
    - Statut
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**Type QueueAttribute**
- Les propriétés suivantes sont marquées comme obsolètes :
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a>**Type TopicAttribute**
- Les propriétés suivantes sont marquées comme obsolètes :
    - Lieu
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a>**Type SubscriptionAttribute**
- Les propriétés suivantes sont marquées comme obsolètes :
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Lieu
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```