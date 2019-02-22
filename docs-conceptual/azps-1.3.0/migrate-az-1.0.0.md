---
title: Dernières modifications de Microsoft Azure PowerShell Az 1.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153183"
---
# <a name="migration-guide-for-az-100"></a>Guide de migration pour Az 1.0.0

Ce document décrit les modifications apportées entre les versions 6.x d’AzureRM et la version Az 1.0.0.

## <a name="table-of-contents"></a>Sommaire
- [Dernières modifications générales](#general-breaking-changes)
  - [Modifications de préfixe de nom de cmdlet](#cmdlet-noun-prefix-changes)
  - [Modifications de nom de module](#module-name-changes)
  - [Modules supprimés](#removed-modules)
  - [Windows PowerShell 5.1 et .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [Changements cassants de module](#module-breaking-changes)
  - [Az.ApiManagement (précédemment AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (précédemment AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (précédemment AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (précédemment AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (précédemment AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (précédemment AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (précédemment AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (précédemment AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (précédemment AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (précédemment AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (précédemment AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (précédemment AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (précédemment Azure.Storage et AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (précédemment AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Dernières modifications générales
### <a name="cmdlet-noun-prefix-changes"></a>Modifications de préfixe de nom de cmdlet
Dans AzureRM, les cmdlets utilisaient « AzureRM » ou « Azure » comme préfixe de nom.  Az simplifie et normalise les noms de cmdlet, afin qu’elles utilisent toutes « Az » comme nom de préfixe de cmdlet. Par exemple : 
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

est devenu
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

Pour simplifier la transition vers ces nouveaux noms de cmdlet, Az introduit deux nouvelles cmdlets : ```Enable-AzureRmAlias``` et ```Disable-AzureRmAlias```.  ```Enable-AzureRmAlias``` crée des alias pour les noms de cmdlet Az récents à partir des anciens noms de cmdlet dans AzureRM.  La cmdlet permet de créer des alias dans la session active, ou dans toutes les sessions en modifiant le profil de l’ordinateur ou de l’utilisateur. 

Par exemple, le script suivant dans AzureRM :
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Peut être exécuté avec des modifications minimes à l’aide de ```Enable-AzureRmAlias``` :
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

L’exécution de ```Enable-AzureRmAlias -Scope CurrentUser``` activera les alias pour toutes les sessions PowerShell que vous ouvrez. Ainsi, après l’exécution de cette cmdlet, il serait inutile de modifier un tel script :
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Pour plus d’informations sur l’utilisation des cmdlets d’alias, exécutez ```Get-Help -Online Enable-AzureRmAlias``` à partir de l’invite PowerShell.

```Disable-AzureRmAlias``` supprime les alias de cmdlet AzureRM créés par ```Enable-AzureRmAlias```.  Pour plus d’informations, exécutez ```Get-Help -Online Disable-AzureRmAlias``` à partir de l’invite PowerShell.

### <a name="module-name-changes"></a>Modifications de nom de module
- Les noms de module ont été modifiés de `AzureRM.*` vers `Az.*`, sauf pour les modules suivants :
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

Les modifications dans les noms de module signifient que n’importe quel script qui utilise ```#Requires``` ou ```Import-Module``` pour charger des modules spécifiques devra être modifié pour utiliser le nouveau module à la place.

#### <a name="migrating-requires-statements"></a>Migration des instructions #Requires
Les scripts qui utilisent #Requires pour déclarer une dépendance sur les modules AzureRM doiventt être mis à jour pour utiliser les nouveaux noms de module.
```powershell
#Requires -Module AzureRM.Compute
```

Doit être remplacé par
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>Migration des instructions Import-Module
Les scripts qui utilisent ```Import-Module``` pour charger les modules AzureRM devront être mis à jour pour refléter les nouveaux noms de module.
```powershell
Import-Module -Name AzureRM.Compute
```

Doit être remplacé par
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migration des appels de cmdlet complets
Les scripts qui utilisent des appels de cmdlet complets par un module, comme
```powershell
AzureRM.Compute\Get-AzureRmVM
```

doivent être modifiés pour utiliser les nouveaux noms de module et de cmdlet
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migration des dépendances de manifeste de module
Les modules qui expriment les dépendances sur les modules AzureRM via un manifeste de module (.psd1) doivent mettre à jour les noms de module dans la section « RequiredModules ».

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Doit être remplacé par

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Modules supprimés
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Les outils destinés à ces services ne sont plus activement pris en charge.  Les clients sont encouragés à choisir d’autres services dès que possible.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 et .NET 4.7.2
- L’utilisation d’Az avec Windows PowerShell 5.1 nécessite l’installation de .NET 4.7.2. Toutefois, l’utilisation d’Az avec PowerShell Core ne nécessite pas .NET 4.7.2. 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential
- En raison de modifications dans le flux d’authentification pour .NET Standard, nous supprimons temporairement la connexion utilisateur via PSCredential. Cette fonctionnalité sera réintroduite dans la version du 15/1/2019 pour Windows PowerShell 5.1. Les détails sont abordés dans [ce problème.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web
- En raison de modifications dans le flux d’authentification pour .NET Standard, nous utilisons la connexion à l’appareil en tant que flux de connexion par défaut lors de la connexion interactive. La connexion basée sur un navigateur Web sera réintroduite pour Windows PowerShell 5.1 en tant que mode par défaut dans la version 15/1/2019. À ce moment, les utilisateurs seront en mesure de se connecter à l’appareil à l’aide d’un paramètre de commutateur.

## <a name="module-breaking-changes"></a>Changements cassants de module

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (précédemment AzureRM.ApiManagement)
- Suppression des cmdlets suivantes :
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Utilisez la cmdlet **Set-AzApiManagement** pour définir ces propriétés à la place.
- Les propriétés suivantes ont été supprimées.
  - Suppression des propriétés `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` et `ScmHostnameConfiguration` de type `PsApiManagementHostnameConfiguration` dans `PsApiManagementContext`. À la place, utilisez `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` et `ScmCustomHostnameConfiguration` de type `PsApiManagementCustomHostNameConfiguration`.
  - Suppression de la propriété `StaticIPs` dans PsApiManagementContext. La propriété a été divisée en `PublicIPAddresses` et `PrivateIPAddresses`.
  - Suppression de la propriété obligatoire `Location` dans la cmdlet New-AzureApiManagementVirtualNetwork.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)
- Le paramètre `InvoiceName` a été supprimé de la cmdlet `Get-AzConsumptionUsageDetail`.  Les scripts doivent utiliser d’autres paramètres d’identité pour la facture.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (précédemment AzureRM.CognitiveServices)
- Suppression du jeu de paramètres `GetSkusWithAccountParamSetName` dans la cmdlet `Get-AzCognitiveServicesAccountSkus`.  Vous devez obtenir des références (SKU) par type de compte et emplacement, au lieu d’utiliser ResourceGroupName et le nom du compte.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (précédemment AzureRM.Compute)
- `IdentityIds` sont supprimés de la propriété `Identity` dans les objets `PSVirtualMachine` et `PSVirtualMachineScaleSet`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.
- Le type de la propriété `InstanceView` de l’objet `PSVirtualMachineScaleSetVM` passe de `VirtualMachineInstanceView` à `VirtualMachineScaleSetVMInstanceView`.
- Les propriétés `AutoOSUpgradePolicy` et `AutomaticOSUpgrade` sont supprimées de la propriété `UpgradePolicy`.
- Le type de la propriété `Sku` de l’objet `PSSnapshotUpdate` passe de `DiskSku` à `SnapshotSku`.
- `VmScaleSetVMParameterSet` est supprimé de la cmdlet `Add-AzVMDataDisk`. Vous ne pouvez plus ajouter un disque de données individuellement à une machine virtuelle ScaleSet.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)
- Le paramètre `GatewayName` est devenu obligatoire dans la cmdlet `New-AzDataFactoryEncryptValue`.
- Suppression de la cmdlet `New-AzDataFactoryGatewayKey`
- Paramètre `LinkedServiceName` supprimé de la cmdlet `Get-AzDataFactoryV2ActivityRun`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)
- Suppression des cmdlets déconseillées : `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, et `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (précédemment AzureRM.DataLakeStore)
- Dans les cmdlets suivantes, le paramètre `Encoding` est passé du type `FileSystemCmdletProviderEncoding` à `System.Text.Encoding`. Cette modification supprime les valeurs de codage `String` et `Oem`. Toutes les autres valeurs de codage préalables demeurent identiques.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- Suppression de l’alias de propriété `Tags` déconseillé dans les cmdlets `New-AzDataLakeStoreAccount` et `Set-AzDataLakeStoreAccount`.

  Tout script utilisant
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Doit être remplacé par
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Suppression des propriétés déconseillées ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` et ```FirewallAllowAzureIps``` de l’objet ```PSDataLakeStoreAccountBasic```.  Aucun script utilisant l’élément ```PSDatalakeStoreAccount``` renvoyé par ```Get-AzDataLakeStoreAccount``` ne doit référencer ces propriétés.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (précédemment AzureRM.KeyVault)
- La propriété `PurgeDisabled` a été supprimée des objets `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` et `PSKeyVaultSecretAttributes`. Les scripts ne doivent plus faire référence à la propriété ```PurgeDisabled``` pour prendre des décisions de traitement.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (précédemment AzureRM.Media)
- Suppression de l’alias de propriété `Tags` déconseillé de la cmdlet `New-AzMediaService`. Tout script utilisant
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Doit être remplacé par
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (précédemment AzureRM.Insights)
- Suppression des paramètres `Categories` et `Timegrains` avec des noms pluriels en faveur des noms de paramètre au singulier dans la cmdlet `Set-AzDiagnosticSetting`. Tout script utilisant
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Doit être remplacé par
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (précédemment AzureRM.Network)
- Suppression du paramètre déconseillé `ResourceId` de la cmdlet `Get-AzServiceEndpointPolicyDefinition`
- Suppression de la propriété déconseillée `EnableVmProtection` de l’objet `PSVirtualNetwork`
- Suppression de la cmdlet déconseillée `Set-AzVirtualNetworkGatewayVpnClientConfig`
  
Les scripts ne doivent plus prendre de décisions de traitement reposant sur les valeurs de ces champs.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (précédemment AzureRM.OperationalInsights)
- Le jeu de paramètres par défaut pour `Get-AzOperationalInsightsDataSource` est supprimé, et `ByWorkspaceNameByKind` est devenu le jeu de paramètres par défaut

  Tout script qui répertorie des sources de données utilisant
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  Doit être modifié selon un type spécifique
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)
- Suppression du paramètre `Encryption` dans la cmdlet `New/Set-AzRecoveryServicesAsrPolicy`
- Le paramètre `TargetStorageAccountName` est maintenant obligatoire pour les restaurations de disque managé dans la cmdlet `Restore-AzRecoveryServicesBackupItem`.
- Suppression des paramètres `StorageAccountName` et `StorageAccountResourceGroupName` dans la cmdlet `Restore-AzRecoveryServicesBackupItem`
- Suppression du paramètre `Name` dans la cmdlet `Get-AzRecoveryServicesBackupContainer`

### <a name="azresources-previously-azurermresources"></a>Az.Resources (précédemment AzureRM.Resources)
- Suppression du paramètre `Sku` dans la cmdlet `New/Set-AzPolicyAssignment`
- Suppression du paramètre `Password` dans les cmdlets `New-AzADServicePrincipal` et `New-AzADSpCredential`. Les mots de passe sont automatiquement générés. Tout script qui a fourni le mot de passe :
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Doit être modifié par récupérer le mot de passe à partir de la sortie :
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (précédemment AzureRM.ServiceFabric)
- Les types de retour de cmdlet suivants ont été modifiés :
  - La propriété `SerivceTypeHealthPolicies` de type `ApplicationHealthPolicy` a été supprimée.
  - La propriété `ApplicationHealthPolicies` de type `ClusterUpgradeDeltaHealthPolicy` a été supprimée.
  - La propriété `OverrideUserUpgradePolicy` de type `ClusterUpgradePolicy` a été supprimée.
  - Ces modifications influent sur les cmdlets suivantes :
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (précédemment AzureRM.Sql)
- Suppression des paramètres `State` et `ResourceId` dans la cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Suppression des cmdlets déconseillées : `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`
- Suppression du paramètre déconseillé `Current` de la cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Suppression du paramètre déconseillé `DatabaseName` de la cmdlet `Get-AzSqlServerServiceObjective`
- Suppression du paramètre déconseillé `PrivilegedLogin` de la cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (précédemment Azure.Storage et AzureRM.Storage)
- Pour prendre en charge la création d’un contexte de stockage Oauth avec uniquement le nom du compte de stockage, le jeu de paramètres par défaut a été remplacé par `OAuthParameterSet`.
  - Exemple : `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- Le paramètre `Location` est devenu obligatoire dans la cmdlet `Get-AzStorageUsage`.
- Les méthodes d’API de stockage utilisent maintenant le modèle asynchrone basé sur des tâches (TAP), au lieu d’appels d’API synchrones.
#### <a name="1-blob-snapshot"></a>1. Instantané d’objet blob
##### <a name="before"></a>Avant :
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>Après :
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2. Partager l’instantané
##### <a name="before"></a>Avant :
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>Après :
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3. Restaurer un objet blob après une suppression réversible
##### <a name="before"></a>Avant :
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>Après :
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4. Définir un niveau d’objet blob
##### <a name="before"></a>Avant :
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>Après :
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (précédemment AzureRM.Websites)
- Suppression des propriétés déconseillées des objets `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` et `PSSite`.