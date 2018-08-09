---
title: Dernières modifications de Microsoft Azure PowerShell 6.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 5/1/2018
ms.openlocfilehash: 4f9c99152fd6ddc23aec005c8e8957e545e65246
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653319"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Dernières modifications de Microsoft Azure PowerShell 6.0.0

Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell. Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance. Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.

## <a name="table-of-contents"></a>Sommaire

- [Dernières modifications générales](#general-breaking-changes)
    - [Version PowerShell minimale requise passée à la version 5.0](#minimum-powershell-version-required-bumped-to-50)
    - [Enregistrement automatique du contexte activé par défaut](#context-autosaved-enabled-by-default)
    - [Suppression de l’alias des balises](#removal-of-tags-alias)
- [Dernières modifications des applets de commande AzureRM.Compute](#breaking-changes-to-azurermcompute-cmdlets)
- [Dernières modifications des applets de commande AzureRM.DataLakeStore](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Dernières modifications des applets de commande AzureRM.Dns](#breaking-changes-to-azurermdns-cmdlets)
- [Dernières modifications des applets de commande AzureRM.Insights](#breaking-changes-to-azurerminsights-cmdlets)
- [Dernières modifications des applets de commande AzureRM.KeyVault](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Dernières modifications des applets de commande AzureRM.Network](#breaking-changes-to-azurermnetwork-cmdlets)
- [Dernières modifications des applets de commande AzureRM.RedisCache](#breaking-changes-to-azurermrediscache-cmdlets)
- [Dernières modifications des applets de commande AzureRM.Resources](#breaking-changes-to-azurermresources-cmdlets)
- [Dernières modifications des applets de commande AzureRM.Storage](#breaking-changes-to-azurermstorage-cmdlets)
- [Modules supprimés](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Dernières modifications générales

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Version PowerShell minimale requise passée à la version 5.0

Auparavant, Azure PowerShell nécessitait _au moins_ la version 3.0 de PowerShell pour exécuter un applet de commande. La version 5.0 de PowerShell est maintenant exigée. Pour plus d’informations sur la mise à niveau vers PowerShell 5.0, consultez [ce tableau](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Enregistrement automatique du contexte activé par défaut

L’enregistrement automatique du contexte correspond au stockage des informations de connexion Azure pouvant être utilisées entre des sessions nouvelles et différentes de PowerShell. Pour plus d’informations sur cet enregistrement automatique du contexte, consultez [ce document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).

Précédemment, cette fonctionnalité d’enregistrement automatique du contexte était désactivée par défaut, ce qui signifie que les informations d’authentification Azure de l’utilisateur n’étaient pas stockées entre les sessions jusqu’à l’exécution de l’applet de commande `Enable-AzureRmContextAutosave` visant à activer la persistance du contexte. En progressant, l’enregistrement automatique du contexte sera activé par défaut, ce qui signifie que les utilisateurs _sans aucun paramètre d’enregistrement automatique du contexte_ verront leur contexte stocké lors de leur prochaine connexion. Les utilisateurs peuvent désactiver cette fonctionnalité à l’aide de l’applet de commande `Disable-AzureRmContextAutosave`.

_Remarque_ : les utilisateurs ayant précédemment désactivé cet enregistrement automatique du contexte ou bien les utilisateurs dont l’enregistrement automatique du contexte est activé et des contextes existants ne seront pas affectés par cette modification

### <a name="removal-of-tags-alias"></a>Suppression de l’alias des balises

L’alias `Tags` pour le paramètre `Tag` a été supprimé sur nombreux applets de commande. Voici une liste des modules affectés (et les applets de commande correspondants) :

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Dernières modifications des applets de commande AzureRM.Compute

**Divers**
- La propriété de nom de référence (SKU) imbriquée dans les types `PSDisk` et `PSSnapshot` a été remplacée, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- La propriété de type de compte de stockage imbriquée dans les types `PSVirtualMachine`, `PSVirtualMachineScaleSet` et `PSImage` a été remplacée, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Add-AzureRmVMDataDisk**
- Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Add-AzureRmVmssDataDisk**
- Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**New-AzureRmAvailabilitySet**
- Le paramètre `Managed` a été supprimé en faveur de `Sku`

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**New-AzureRmDiskUpdateConfig**
- Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**New-AzureRmSnapshotConfig**
- Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**New-AzureRmSnapshotUpdateConfig**
- Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Set-AzureRmImageOsDisk**
- Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Set-AzureRmVMAEMExtension**
- Le paramètre `DisableWAD` a été supprimé
    -  Les diagnostics Microsoft Azure ont été désactivés par défaut

**Set-AzureRmVMDataDisk**
- Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Set-AzureRmVMOSDisk**
- Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Set-AzureRmVmssStorageProfile**
- Les valeurs acceptées pour le paramètre `ManagedDisk` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

**Update-AzureRmVmss**
- Les valeurs acceptées pour le paramètre `ManagedDiskStorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Dernières modifications des applets de commande AzureRM.DataLakeStore

**Export-AzureRmDataLakeStoreItem**
- Les paramètres `PerFileThreadCount` et `ConcurrentFileCount` ont été supprimés. Utilisez dorénavant le paramètre `Concurrency`

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- Les paramètres `PerFileThreadCount` et `ConcurrentFileCount` ont été supprimés. Utilisez dorénavant le paramètre `Concurrency`

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- Le paramètre `Clean` a été supprimé

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Dernières modifications des applets de commande AzureRM.Dns

**New-AzureRmDnsRecordSet**
- Le paramètre `Force` a été supprimé

**Remove-AzureRmDnsRecordSet**
- Le paramètre `Force` a été supprimé

**Remove-AzureRmDnsZone**
- Le paramètre `Force` a été supprimé

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Dernières modifications des applets de commande AzureRM.Insights

**Add-AzureRmAutoscaleSetting**
- Les alias des paramètres `AutoscaleProfiles` et `Notifications` ont été supprimés

**Add-AzureRmLogProfile**
- Les alias des paramètres `Categories` et `Locations` ont été supprimés

**Add-AzureRmMetricAlertRule**
- L’alias des paramètres `Actions` a été supprimé

**Add-AzureRmWebtestAlertRule**
- L’alias des paramètres `Actions` a été supprimé

**Get-AzureRmLog**
- Les alias des paramètres `MaxRecords` et `MaxEvents` ont été supprimés

**Get-AzureRmMetricDefinition**
- L’alias des paramètres `MetricNames` a été supprimé

**New-AzureRmAlertRuleEmail**
- Les alias des paramètres `CustomEmails` et `SendToServiceOwners` ont été supprimés

**New-AzureRmAlertRuleWebhook**
- L’alias des paramètres `Properties` a été supprimé

**New-AzureRmAutoscaleNotification**
- Les alias des paramètres `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` et `Webhooks` ont été supprimés

**New-AzureRmAutoscaleProfile**
- Les alias des paramètres `Rules`, `ScheduleDays`, `ScheduleHours` et `ScheduleMinutes` ont été supprimés

**New-AzureRmAutoscaleWebhook**
- L’alias des paramètres `Properties` a été supprimé

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Dernières modifications des applets de commande AzureRM.KeyVault

**Add-AzureKeyVaultCertificate**
- Le paramètre `CertificatePolicy` est devenu obligatoire.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- L’applet de commande n’accepte plus de paramètres individuels qui composent le jeton d’accès ; au lieu de cela, l’applet de commande remplace les paramètres de jeton explicites, comme `Service` ou `Permissions`, par un paramètre générique `TemplateUri`, correspondant à un exemple de jeton d’accès défini ailleurs (vraisemblablement à l’aide des applets de commande de stockage PowerShell, ou composé manuellement en fonction de la documentation du stockage.) L’applet de commande conserve le paramètre `ValidityPeriod`.

Pour plus d’informations sur la composition de jetons d’accès partagés pour le stockage Azure, reportez-vous aux pages de documentation, respectivement :
- [Construction d’un service SAP] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)
- [Construction d’un compte SAP] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- Le paramètre `IssuerProvider` est devenu obligatoire.

**Undo-AzureKeyVaultCertificateRemoval**
- La sortie de cet applet de commande est passée de `CertificateBundle` à `PSKeyVaultCertificate`.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName` a été supprimé de l’ensemble de paramètres `InputObject`, et il est maintenant obtenu à partir de la propriété `ResourceId` du paramètre `InputObject`.

**Set-AzureRmKeyVaultAccessPolicy**
- L’autorisation `all` a été supprimée de `PermissionsToKeys`, `PermissionsToSecrets`, et `PermissionsToCertificates`.

**Généralités**
- La propriété `ValueFromPipelineByPropertyName` a été supprimée de tous les applets de commande où la redirection par `InputObject` était activée.  Les applets de commande affectés sont :
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- Les niveaux `ConfirmImpact` ont été supprimés de tous les applets de commande.  Les applets de commande affectés sont :
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `IKeyVaultDataServiceClient` a été mis à jour afin que toutes les opérations de certificat retournent PSTypes plutôt que des types de kits de développement logiciel. notamment :
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Dernières modifications des applets de commande AzureRM.Network


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- Le paramètre `ProbeEnabled` a été supprimé

**Add-AzureRmVirtualNetworkPeering**
- L’alias des paramètres `AlloowGatewayTransit` a été supprimé

**New-AzureRmApplicationGatewayBackendHttpSettings**
- Le paramètre `ProbeEnabled` a été supprimé

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- Le paramètre `ProbeEnabled` a été supprimé

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Dernières modifications des applets de commande AzureRM.RedisCache

**New-AzureRmRedisCache**
- Les paramètres `Subnet` et `VirtualNetwork` ont été supprimés en faveur de `SubnetId`
- Le paramètre `RedisVersion` a été supprimé
- Le paramètre `MaxMemoryPolicy` a été supprimé en faveur de `RedisConfiguration`

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- Le paramètre `MaxMemoryPolicy` a été supprimé en faveur de `RedisConfiguration`

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Dernières modifications des applets de commande AzureRM.Resources

**Find-AzureRmResource**
- Cet applet de commande a été supprimé et la fonctionnalité a été déplacée vers `Get-AzureRmResource`

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Cet applet de commande a été supprimé et la fonctionnalité a été déplacée vers `Get-AzureRmResourceGroup`

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- Le paramètre `AtScopeAndBelow` a été supprimé.

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Dernières modifications des applets de commande AzureRM.Storage

**New-AzureRmStorageAccount**
- Le paramètre `EnableEncryptionService` a été supprimé

**Set-AzureRmStorageAccount**
- Les paramètres `EnableEncryptionService` et `DisableEncryptionService` ont été supprimés

## <a name="removed-modules"></a>Modules supprimés

### `AzureRM.ServerManagement`

Le service Outils de gestion de serveur a été [retirée l’an dernier](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) et par conséquent, le module correspondant pour SMT, `AzureRM.ServerManagement`, a été supprimé de `AzureRM` et s’arrête de faire progresser la livraison.

### `AzureRM.SiteRecovery`

Le module `AzureRM.SiteRecovery` est remplacé par `AzureRM.RecoveryServices.SiteRecovery`, qui est un sur-ensemble fonctionnel du module `AzureRM.SiteRecovery` et inclut un nouvel ensemble d’applets de commande équivalents. Vous trouverez ci-dessous la liste complète des mappages entre les anciens applets de commande et les nouveaux :

| Applets de commande déconseillés                                        | Applets de commande équivalents                                                | Alias                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
