---
title: Guide de migration pour Az 3.0.0
description: Ce guide de migration contient la liste des dernières modifications apportées à Azure PowerShell dans la publication d’Az version 3.0.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: e88752e0c997efc4f49161e358072803cb63450a
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75720504"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="48237-103">Guide de migration pour Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="48237-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="48237-104">Ce document décrit les modifications apportées entre les versions 2.0.0 et 3.0.0 d’Az.</span><span class="sxs-lookup"><span data-stu-id="48237-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="48237-105">Guide de migration pour Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="48237-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="48237-106">Batch</span><span class="sxs-lookup"><span data-stu-id="48237-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="48237-107">Incompatibilité avec les versions précédentes de `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="48237-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="48237-108">Calcul</span><span class="sxs-lookup"><span data-stu-id="48237-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="48237-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="48237-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="48237-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="48237-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="48237-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48237-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="48237-112">Ressources</span><span class="sxs-lookup"><span data-stu-id="48237-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="48237-113">Incompatibilité avec les versions précédentes de `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="48237-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="48237-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48237-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="48237-115">Sql</span><span class="sxs-lookup"><span data-stu-id="48237-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="48237-116">Batch</span><span class="sxs-lookup"><span data-stu-id="48237-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="48237-117">`Get-AzBatchNodeAgentSku` a été supprimé et remplacé par `Get-AzBatchSupportedImage`.</span><span class="sxs-lookup"><span data-stu-id="48237-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="48237-118">`Get-AzBatchSupportedImage` retourne les mêmes données que `Get-AzBatchNodeAgentSku` mais dans un format plus convivial.</span><span class="sxs-lookup"><span data-stu-id="48237-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="48237-119">Les nouvelles images non vérifiées sont désormais également retournées.</span><span class="sxs-lookup"><span data-stu-id="48237-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="48237-120">Vous trouverez également des informations supplémentaires sur `Capabilities` et `BatchSupportEndOfLife` pour chaque image.</span><span class="sxs-lookup"><span data-stu-id="48237-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-121">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="48237-122">After</span><span class="sxs-lookup"><span data-stu-id="48237-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="48237-123">Incompatibilité des versions précédentes avec le module Az.Resources</span><span class="sxs-lookup"><span data-stu-id="48237-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="48237-124">La version 2.0.1 du module « Az.Batch » est incompatible avec les versions antérieures (version 1.7.0 ou antérieure) du module « Az.Resources ».</span><span class="sxs-lookup"><span data-stu-id="48237-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="48237-125">Par conséquent, il est impossible d’importer la version 1.7.0 du module « Az.Resources » lors de l’importation de la version 2.0.1 du module « Az.Batch ».</span><span class="sxs-lookup"><span data-stu-id="48237-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="48237-126">Pour résoudre ce problème, mettez simplement à jour le module « Az.Resources » vers la version 1.7.1 ou ultérieure, ou installez simplement la dernière version du module « Az ».</span><span class="sxs-lookup"><span data-stu-id="48237-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="48237-127">Calcul</span><span class="sxs-lookup"><span data-stu-id="48237-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="48237-128">Le paramètre `UploadSizeInBytes` est utilisé à la place de `DiskSizeGB` pour `New-AzDiskConfig` lors du chargement de CreateOption.</span><span class="sxs-lookup"><span data-stu-id="48237-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="48237-129">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="48237-130">After</span><span class="sxs-lookup"><span data-stu-id="48237-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="48237-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="48237-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="48237-132">L’applet de commande `Get-AzHDInsightJobOutput` a été mise à jour de façon à prendre en charge la précision de l’accès en fonction du rôle à la clé de stockage.</span><span class="sxs-lookup"><span data-stu-id="48237-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="48237-133">Les utilisateurs avec les rôles Opérateur, Contributeur et Propriétaire de cluster HDInsight ne seront pas affectés.</span><span class="sxs-lookup"><span data-stu-id="48237-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="48237-134">Les utilisateurs qui ont seulement le rôle Lecteur doivent spécifier explicitement le paramètre `DefaultStorageAccountKey`.</span><span class="sxs-lookup"><span data-stu-id="48237-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-135">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="48237-136">After</span><span class="sxs-lookup"><span data-stu-id="48237-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="48237-137">L’applet de commande `Add-AzHDInsightConfigValue` a supprimé l’alias pour `Add-AzHDInsightConfigValues`.</span><span class="sxs-lookup"><span data-stu-id="48237-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-138">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-138">Before</span></span>
<span data-ttu-id="48237-139">Utilisation de l’alias déprécié</span><span class="sxs-lookup"><span data-stu-id="48237-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="48237-140">After</span><span class="sxs-lookup"><span data-stu-id="48237-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="48237-141">Une nouvelle applet de commande `Disable-AzHDInsightMonitoring` a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="48237-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="48237-142">Utilisez cette applet de commande pour désactiver l’analyse dans un cluster HDInsight (remplace `Disable-AzHDInsightOperationsManagementSuite` et `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="48237-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="48237-143">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="48237-144">After</span><span class="sxs-lookup"><span data-stu-id="48237-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="48237-145">Une nouvelle applet de commande `Enable-AzHDInsightMonitoring` a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="48237-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="48237-146">Utilisez cette applet de commande pour activer l’analyse dans un cluster HDInsight (remplace `Enable-AzHDInsightOperationsManagementSuite` et `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="48237-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="48237-147">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="48237-148">After</span><span class="sxs-lookup"><span data-stu-id="48237-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="48237-149">Une nouvelle applet de commande `Get-AzHDInsightMonitoring` a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="48237-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="48237-150">Utilisez cette applet de commande pour obtenir l’état de l’installation d’analyse dans un cluster Azure HDInsight (remplace `Get-AzHDInsightOperationsManagementSuite` et `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="48237-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="48237-151">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="48237-152">After</span><span class="sxs-lookup"><span data-stu-id="48237-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="48237-153">L’applet de commande `Get-HDInsightProperty` a supprimé l’alias pour `Get-AzHDInsightProperties`.</span><span class="sxs-lookup"><span data-stu-id="48237-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-154">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-154">Before</span></span>
<span data-ttu-id="48237-155">Utilisation de l’alias déprécié</span><span class="sxs-lookup"><span data-stu-id="48237-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="48237-156">After</span><span class="sxs-lookup"><span data-stu-id="48237-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="48237-157">Les applets de commande `Grant-AzHDInsightRdpServicesAccess` et `Revoke-AzHDInsightRdpServicesAccess` ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="48237-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="48237-158">Elles ne sont plus nécessaires, car les clusters utilisant le type de système d’exploitation Windows ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="48237-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="48237-159">Créez un cluster utilisant le type de système d’exploitation Linux à la place.</span><span class="sxs-lookup"><span data-stu-id="48237-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="48237-160">Le type de sortie de `Remove-AzHDInsightCluster` a été modifié de `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` à `bool`.</span><span class="sxs-lookup"><span data-stu-id="48237-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-161">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="48237-162">After</span><span class="sxs-lookup"><span data-stu-id="48237-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="48237-163">L’applet de commande est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="48237-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="48237-164">Aucun remplacement n’existe.</span><span class="sxs-lookup"><span data-stu-id="48237-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="48237-165">Le type de sortie de `Set-AzHDInsightGatewayCredential` a été modifié de `HttpConnectivitySettings` à `AzureHDInsightGatewaySettings`.</span><span class="sxs-lookup"><span data-stu-id="48237-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="48237-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="48237-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="48237-167">Cet alias a été supprimé. Utilisez `New-AzIotHubImportDevice` à la place.</span><span class="sxs-lookup"><span data-stu-id="48237-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-168">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="48237-169">After</span><span class="sxs-lookup"><span data-stu-id="48237-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="48237-170">Cet alias a été supprimé. Utilisez `New-AzIotHubExportDevice` à la place.</span><span class="sxs-lookup"><span data-stu-id="48237-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-171">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="48237-172">After</span><span class="sxs-lookup"><span data-stu-id="48237-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="48237-173">Le paramètre `EventHubEndPointName` est déconseillé sans être remplacé, car IotHub est fourni avec un seul point de terminaison intégré (« events ») capable de gérer les messages système et d’appareil.</span><span class="sxs-lookup"><span data-stu-id="48237-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-174">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="48237-175">After</span><span class="sxs-lookup"><span data-stu-id="48237-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="48237-176">Le paramètre `EventHubEndPointName` est déconseillé sans être remplacé, car IotHub est fourni avec un seul point de terminaison intégré (« events ») capable de gérer les messages système et d’appareil.</span><span class="sxs-lookup"><span data-stu-id="48237-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-177">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="48237-178">After</span><span class="sxs-lookup"><span data-stu-id="48237-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="48237-179">Le paramètre `EventHubEndPointName` est déconseillé sans être remplacé, car IotHub est fourni avec un seul point de terminaison intégré (« events ») capable de gérer les messages système et d’appareil.</span><span class="sxs-lookup"><span data-stu-id="48237-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-180">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="48237-181">After</span><span class="sxs-lookup"><span data-stu-id="48237-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="48237-182">Le paramètre `OperationsMonitoringProperties` est déconseillé sans être remplacé, car IotHub n’utilise plus le point de terminaison intégré (« operationsMonitoringEvents »).</span><span class="sxs-lookup"><span data-stu-id="48237-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="48237-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48237-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="48237-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` et `ASRRecoveryPlanGroup.EndGroupActions` sont supprimés de la sortie.</span><span class="sxs-lookup"><span data-stu-id="48237-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="48237-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` et `ASRRecoveryPlanGroup.EndGroupActions` sont supprimés de la sortie.</span><span class="sxs-lookup"><span data-stu-id="48237-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="48237-186">Le paramètre IncludeDiskId est modifié pour que l’écriture directe soit prise en charge sur un disque managé dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="48237-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-187">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="48237-188">After</span><span class="sxs-lookup"><span data-stu-id="48237-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="48237-189">Ressources</span><span class="sxs-lookup"><span data-stu-id="48237-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="48237-190">Incompatibilité des versions précédentes avec le module Az.Batch</span><span class="sxs-lookup"><span data-stu-id="48237-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="48237-191">La version 1.7.1 du module « Az.Resources » est incompatible avec les versions antérieures (version 1.1.2 ou antérieure) du module « Az.Batch ».</span><span class="sxs-lookup"><span data-stu-id="48237-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="48237-192">Par conséquent, il est impossible d’importer la version 1.1.2 du module « Az.Batch » lors de l’importation de la version 1.7.1 du module « Az.Resources ».</span><span class="sxs-lookup"><span data-stu-id="48237-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="48237-193">Pour résoudre ce problème, mettez à jour le module « Az.Batch » vers la version 2.0.1 ou ultérieure, ou installez simplement la dernière version du module « Az ».</span><span class="sxs-lookup"><span data-stu-id="48237-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="48237-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48237-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="48237-195">`Add-ServiceFabricApplicationCertificate` a été supprimé, car ce scénario est couvert par `Add-AzVmssSecret`.</span><span class="sxs-lookup"><span data-stu-id="48237-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-196">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="48237-197">After</span><span class="sxs-lookup"><span data-stu-id="48237-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="48237-198">SQL</span><span class="sxs-lookup"><span data-stu-id="48237-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="48237-199">Notez que la connexion sécurisée est déconseillée et que la commande a donc été supprimée.</span><span class="sxs-lookup"><span data-stu-id="48237-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="48237-200">Utilisez le panneau de la base de données SQL dans le Portail Azure pour afficher les chaînes de connexion.</span><span class="sxs-lookup"><span data-stu-id="48237-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="48237-201">L’alias `Get-AzSqlDatabaseIndexRecommendations` a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="48237-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="48237-202">Utilisez `Get-AzSqlDatabaseIndexRecommendation` à la place.</span><span class="sxs-lookup"><span data-stu-id="48237-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="48237-203">L’alias `Get-AzSqlDatabaseRestorePoints` a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="48237-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="48237-204">Utilisez `Get-AzSqlDatabaseRestorePoint` à la place.</span><span class="sxs-lookup"><span data-stu-id="48237-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="48237-205">L’applet de commande `Get-AzSqlDatabaseAudit` remplace cette applet de commande.</span><span class="sxs-lookup"><span data-stu-id="48237-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="48237-206">Le type de sortie existant « Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel » est remplacé par le nouveau type « Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel », avec la suppression des propriétés `AuditState`, `StorageAccountName`</span><span class="sxs-lookup"><span data-stu-id="48237-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="48237-207">et `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="48237-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="48237-208">Les scripts peuvent récupérer des informations de compte de stockage à partir de la nouvelle propriété `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="48237-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-209">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="48237-210">After</span><span class="sxs-lookup"><span data-stu-id="48237-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="48237-211">L’applet de commande `Set-AzSqlDatabaseAudit` remplace cette applet de commande.</span><span class="sxs-lookup"><span data-stu-id="48237-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="48237-212">Le type de sortie existant « Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel » est remplacé par le nouveau type « bool ».</span><span class="sxs-lookup"><span data-stu-id="48237-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="48237-213">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-214">After</span><span class="sxs-lookup"><span data-stu-id="48237-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="48237-215">L’applet de commande `Get-AzSqlServerAudit` remplace cette applet de commande.</span><span class="sxs-lookup"><span data-stu-id="48237-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="48237-216">Le type de sortie existant « Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel » est remplacé par le nouveau type « Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel ».</span><span class="sxs-lookup"><span data-stu-id="48237-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="48237-217">Les propriétés `AuditState`, `StorageAccountName` et `StorageAccountSubscriptionId` sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="48237-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="48237-218">Les scripts qui utilisent les propriétés `StorageAccountName` et `StorageAccountSubscriptionId` peuvent récupérer ces informations à partir de la nouvelle propriété `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="48237-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="48237-219">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="48237-220">After</span><span class="sxs-lookup"><span data-stu-id="48237-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="48237-221">L’applet de commande `Set-AzSqlServerAudit` remplace cette applet de commande.</span><span class="sxs-lookup"><span data-stu-id="48237-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="48237-222">Le type de sortie existant « Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel » est remplacé par le nouveau type « bool ».</span><span class="sxs-lookup"><span data-stu-id="48237-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="48237-223">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="48237-224">After</span><span class="sxs-lookup"><span data-stu-id="48237-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="48237-225">L’applet de commande `Get-AzSqlServerAdvancedThreatProtectionSettings` est remplacée par `Get-AzSqlServerAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-226">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="48237-227">After</span><span class="sxs-lookup"><span data-stu-id="48237-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="48237-228">L’applet de commande `Clear-AzSqlServerAdvancedThreatProtectionSettings` est remplacée par `Clear-AzSqlServerAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-229">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="48237-230">After</span><span class="sxs-lookup"><span data-stu-id="48237-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="48237-231">L’applet de commande `Update-AzSqlServerAdvancedThreatProtectionSettings` est remplacée par `Update-AzSqlServerAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-232">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="48237-233">After</span><span class="sxs-lookup"><span data-stu-id="48237-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="48237-234">L’applet de commande `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` est remplacée par `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-235">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-236">After</span><span class="sxs-lookup"><span data-stu-id="48237-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="48237-237">L’applet de commande `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` est remplacée par `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-238">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="48237-239">After</span><span class="sxs-lookup"><span data-stu-id="48237-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="48237-240">L’applet de commande `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` est remplacée par `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-241">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-242">After</span><span class="sxs-lookup"><span data-stu-id="48237-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-243">L’applet de commande `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` est remplacée par `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-244">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="48237-245">After</span><span class="sxs-lookup"><span data-stu-id="48237-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-246">L’applet de commande `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` est remplacée par `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-247">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-248">After</span><span class="sxs-lookup"><span data-stu-id="48237-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-249">L’applet de commande `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` est remplacée par `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-250">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-251">After</span><span class="sxs-lookup"><span data-stu-id="48237-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-252">L’applet de commande `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` est remplacée par `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-253">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="48237-254">After</span><span class="sxs-lookup"><span data-stu-id="48237-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-255">L’applet de commande `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` est remplacée par `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-256">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-257">After</span><span class="sxs-lookup"><span data-stu-id="48237-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-258">L’applet de commande `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` est remplacée par `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-259">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-260">After</span><span class="sxs-lookup"><span data-stu-id="48237-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-261">L’applet de commande `Update-AzSqlInstanceVulnerabilityAssessmentSettings` est remplacée par `Update-AzSqlInstanceVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-262">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="48237-263">After</span><span class="sxs-lookup"><span data-stu-id="48237-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-264">L’applet de commande `Get-AzSqlInstanceVulnerabilityAssessmentSettings` est remplacée par `Get-AzSqlInstanceVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-265">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-266">After</span><span class="sxs-lookup"><span data-stu-id="48237-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-267">L’applet de commande `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` est remplacée par `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-268">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-269">After</span><span class="sxs-lookup"><span data-stu-id="48237-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-270">L’applet de commande `Update-AzSqlServerVulnerabilityAssessmentSettings` est remplacée par `Update-AzSqlServerVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-271">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="48237-272">After</span><span class="sxs-lookup"><span data-stu-id="48237-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-273">L’applet de commande `Get-AzSqlServerVulnerabilityAssessmentSettings` est remplacée par `Get-AzSqlServerVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-274">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-275">After</span><span class="sxs-lookup"><span data-stu-id="48237-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="48237-276">L’applet de commande `Clear-AzSqlServerVulnerabilityAssessmentSettings` est remplacée par `Clear-AzSqlServerVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-277">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-278">After</span><span class="sxs-lookup"><span data-stu-id="48237-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="48237-279">L’applet de commande `Get-AzSqlServerAdvancedThreatProtectionPolicy` est supprimée et aucune applet de commande ne la remplace.</span><span class="sxs-lookup"><span data-stu-id="48237-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="48237-280">L’applet de commande `Get-AzSqlServerThreatDetectionPolicy` est remplacée par `Get-AzSqlServerThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-281">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="48237-282">After</span><span class="sxs-lookup"><span data-stu-id="48237-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="48237-283">L’applet de commande `Remove-AzSqlServerThreatDetectionPolicy` est remplacée par `Clear-AzSqlServerThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-284">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="48237-285">After</span><span class="sxs-lookup"><span data-stu-id="48237-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="48237-286">L’applet de commande `Set-AzSqlServerThreatDetectionPolicy` est remplacée par `Update-AzSqlServerThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-287">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="48237-288">After</span><span class="sxs-lookup"><span data-stu-id="48237-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="48237-289">L’applet de commande `Get-AzSqlDatabaseThreatDetectionPolicy` est remplacée par `Get-AzSqlDatabaseThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-290">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="48237-291">After</span><span class="sxs-lookup"><span data-stu-id="48237-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="48237-292">L’applet de commande `Set-AzSqlDatabaseThreatDetectionPolicy` est remplacée par `Update-AzSqlDatabaseThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-293">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="48237-294">After</span><span class="sxs-lookup"><span data-stu-id="48237-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="48237-295">L’applet de commande `Remove-AzSqlDatabaseThreatDetectionPolicy` est remplacée par `Clear-AzSqlDatabaseThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="48237-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="48237-296">Avant</span><span class="sxs-lookup"><span data-stu-id="48237-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="48237-297">After</span><span class="sxs-lookup"><span data-stu-id="48237-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
