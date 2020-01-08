---
title: Tous les changements d’AzureRM à Azure PowerShell Az 1.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: e5121d61b0f5f68ff3e1f33d774e3533adfeb64f
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75721953"
---
# <a name="breaking-changes-for-az-100"></a>Changements cassants pour Az 1.0.0

Ce document fournit des informations détaillées sur les changements intervenus entre AzureRM 6.x et le nouveau module Az version 1.x et ultérieure. La table des matières constitue un guide du parcours de migration complet, notamment en ce qui concerne les modifications spécifiques aux modules susceptibles d’affecter vos scripts.

Pour obtenir des conseils généraux sur la préparation d’une migration d’AzureRM vers Az, consultez [Démarrer la migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).

> [!IMPORTANT]
> Des changements cassants ont également été introduits entre Az 1.0.0 et Az 2.0.0. Après avoir suivi ce guide pour la mise à jour d’AzureRM vers Az, consultez les [Changements cassants d’Az 2.0.0](migrate-az-2.0.0.md) pour savoir si vous devez apporter des modifications supplémentaires.

## <a name="table-of-contents"></a>Sommaire

- [Dernières modifications générales](#general-breaking-changes)
  - [Modifications des préfixes des noms des applets de commande](#cmdlet-noun-prefix-changes)
  - [Modifications de nom de module](#module-name-changes)
  - [Modules supprimés](#removed-modules)
  - [Windows PowerShell 5.1 et .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Suppression temporaire de la connexion de l’utilisateur avec PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web](#default-device-code-login-instead-of-web-browser-prompt)
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

Cette section détaille les changements cassants généraux qui font partie de cette reconception du module Az.

### <a name="cmdlet-noun-prefix-changes"></a>Modifications de préfixe de nom de cmdlet

Dans le module AzureRM, les applets de commande utilisaient `AzureRM` ou `Azure` comme préfixes pour les noms.  Az simplifie et normalise les noms des applets de commande : elles utilisent dorénavant toutes « Az » comme préfixe pour leurs noms. Par exemple :

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

A été remplacé par :

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

Pour simplifier la transition vers ces nouveaux noms des applets de commande, Az introduit deux nouvelles applets de commande : [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) et [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).  `Enable-AzureRmAlias` crée des alias pour les anciens noms des applets de commande dans AzureRM qui établissent la correspondance avec leurs nouveaux noms dans Az. L’utilisation de l’argument `-Scope` avec `Enable-AzureRmAlias` vous permet de choisir où les alias sont activés.

Par exemple, le script suivant dans AzureRM :

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Peut être exécuté avec des modifications minimes à l’aide de `Enable-AzureRmAlias` :

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

L’exécution de `Enable-AzureRmAlias -Scope CurrentUser` active les alias pour toutes les sessions PowerShell que vous ouvrez. Ainsi, après l’exécution de cette applet de commande, un script comme celui-ci ne nécessite aucune modification :

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Pour plus d’informations sur l’utilisation des alias des applets de commande, consultez les [Informations de référence sur Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

Quand vous êtes prêt à désactiver les alias, `Disable-AzureRmAlias` supprime les alias créés. Pour plus d’informations, consultez les [Informations de référence sur Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Quand vous désactivez les alias, vérifiez qu’ils sont désactivés pour _toutes_ les étendues où les alias étaient activés.

### <a name="module-name-changes"></a>Modifications de nom de module

Les noms de module ont été modifiés de `AzureRM.*` vers `Az.*`, sauf pour les modules suivants :

| Module AzureRM | Module Az |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.Profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

Les modifications dans les noms de module signifient que n’importe quel script qui utilise `#Requires` ou `Import-Module` pour charger des modules spécifiques devra être modifié pour utiliser le nouveau module à la place. Pour les modules où le suffixe des applets de commande n’a pas changé, cela signifie que, bien que le nom du module ait changé, le suffixe indiquant l’espace des opérations n’a _pas_ changé.

#### <a name="migrating-requires-and-import-module-statements"></a>Migration des instructions #Requires et Import-Module

Les scripts qui utilisent `#Requires`ou `Import-Module` pour déclarer une dépendance vis-à-vis de modules AzureRM doivent être mis à jour de façon à utiliser les nouveaux noms des modules. Par exemple :

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

Doit être remplacé par :

```azurepowershell-interactive
#Requires -Module Az.Compute
```

Pour `Import-Module` :

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

Doit être remplacé par :

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migration des appels de cmdlet complets

Les scripts qui utilisent des appels d’applets de commande qualifiés par module, comme :

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

doivent être modifiés de façon à utiliser les nouveaux noms des modules et des applets de commande :

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migration des dépendances de manifeste de module

Pour les modules qui expriment des dépendances vis-à-vis de modules AzureRM via un fichier manifeste de module (.psd1), vous devez mettre à jour les noms des modules dans leur section `RequiredModules` :

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Doit être remplacé par :

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Modules supprimés

Les modules suivants ont été supprimés :

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Les outils pour ces services ne sont plus activement pris en charge.  Les clients sont encouragés à choisir d’autres services dès que possible.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 et .NET 4.7.2

L’utilisation d’Az avec PowerShell 5.1 pour Windows nécessite l’installation de .NET Framework 4.7.2. L’utilisation de PowerShell Core 6.x ou ultérieur ne nécessite pas le .NET Framework.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential

En raison de modifications dans le flux d’authentification pour .NET Standard, nous supprimons temporairement la connexion utilisateur via PSCredential. Cette fonctionnalité sera réintroduite dans la version du 15/01/2019 pour PowerShell 5.1 pour Windows. Les détails sont abordés dans [ce problème GitHub.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web

En raison de modifications dans le flux d’authentification pour .NET Standard, nous utilisons la connexion à l’appareil en tant que flux de connexion par défaut lors de la connexion interactive. La connexion basée sur un navigateur web sera réintroduite pour PowerShell 5.1 pour Windows comme option par défaut dans la version du 15/01/2019. À ce moment, les utilisateurs seront en mesure de se connecter à l’appareil à l’aide d’un paramètre de commutateur.

## <a name="module-breaking-changes"></a>Changements cassants de module

Cette section détaille les changements cassants spécifiques à des applets de commande et des modules individuels.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (précédemment AzureRM.ApiManagement)

- Les applets de commande suivantes ont été supprimées :
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Utilisez à la place l’applet de commande **Set-AzApiManagement** pour définir ces propriétés.
- Les propriétés suivantes ont été supprimées :
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
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Doit être remplacé par
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Suppression des propriétés déconseillées `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` et `FirewallAllowAzureIps` de l’objet `PSDataLakeStoreAccountBasic`.  Aucun script utilisant l’élément `PSDatalakeStoreAccount` renvoyé par `Get-AzDataLakeStoreAccount` ne doit référencer ces propriétés.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (précédemment AzureRM.KeyVault)

- La propriété `PurgeDisabled` a été supprimée des objets `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` et `PSKeyVaultSecretAttributes`. Les scripts ne doivent plus faire référence à la propriété ```PurgeDisabled``` pour prendre des décisions de traitement.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (précédemment AzureRM.Media)

- Suppression de l’alias de propriété `Tags` déconseillé de la cmdlet `New-AzMediaService`. Tout script utilisant
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Doit être remplacé par
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (précédemment AzureRM.Insights)

- Suppression des paramètres `Categories` et `Timegrains` avec des noms pluriels en faveur des noms de paramètre au singulier dans la cmdlet `Set-AzDiagnosticSetting`. Tout script utilisant
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Doit être remplacé par
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (précédemment AzureRM.Network)

- Suppression du paramètre déconseillé `ResourceId` de la cmdlet `Get-AzServiceEndpointPolicyDefinition`
- Suppression de la propriété déconseillée `EnableVmProtection` de l’objet `PSVirtualNetwork`
- Suppression de la cmdlet déconseillée `Set-AzVirtualNetworkGatewayVpnClientConfig`

Les scripts ne doivent plus décider des traitements sur la base des valeurs de ces champs.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (précédemment AzureRM.OperationalInsights)

- Le jeu de paramètres par défaut pour `Get-AzOperationalInsightsDataSource` est supprimé, et `ByWorkspaceNameByKind` est devenu le jeu de paramètres par défaut

  Tout script qui répertorie des sources de données utilisant
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  Doit être modifié selon un type spécifique
  ```azurepowershell-interactive
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

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Doit être changé de façon à récupérer le mot de passe à partir de la sortie :

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (précédemment AzureRM.ServiceFabric)

- Les types de retour de cmdlet suivants ont été modifiés :
  - La propriété `ServiceTypeHealthPolicies` de type `ApplicationHealthPolicy` a été supprimée.
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
- Les méthodes d’API de stockage utilisent maintenant le modèle asynchrone basé sur des tâches (TAP), au lieu d’appels d’API synchrones. Les exemples suivants montrent les nouvelles commandes asynchrones :

#### <a name="blob-snapshot"></a>Instantané d’objet blob

AzureRM :

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az :

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Partager l’instantané

AzureRM :

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az :

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Annuler la suppression d’un objet blob supprimé de manière réversible

AzureRM :

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az :

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Définir un niveau d’objet blob

AzureRM :

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az :

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (précédemment AzureRM.Websites)

- Suppression des propriétés déconseillées des objets `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` et `PSSite`.
