---
title: Guide de migration pour Az 2.0.0
description: Ce guide de migration contient une liste des changements cassants apportés à Azure PowerShell dans la version Az 2.0.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 5f15d1a4f1e8416d7214aceb78494867fe4aad52
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537170"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="e12e9-103">Guide de migration pour Az 2.0.0</span><span class="sxs-lookup"><span data-stu-id="e12e9-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="e12e9-104">Ce document décrit les modifications apportées entre les versions 1.0.0 et 2.0.0 d’Az.</span><span class="sxs-lookup"><span data-stu-id="e12e9-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="e12e9-105">Sommaire</span><span class="sxs-lookup"><span data-stu-id="e12e9-105">Table of Contents</span></span>
- [<span data-ttu-id="e12e9-106">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="e12e9-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="e12e9-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e12e9-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="e12e9-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e12e9-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="e12e9-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e12e9-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="e12e9-110">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="e12e9-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="e12e9-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e12e9-111">Az.Compute</span></span>

- <span data-ttu-id="e12e9-112">Paramètre `Managed` supprimé des applets de commande `New-AzAvailabilitySet` et `Update-AzAvailabilitySet`, au profit de ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="e12e9-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-113">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-114">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="e12e9-115">Pour des raisons de cohérence, le paramètre `Image` a été supprimé des jeux de paramètres « ByName » et « ByResourceId » dans `Update-AzImage`</span><span class="sxs-lookup"><span data-stu-id="e12e9-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="e12e9-116">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-116">Before</span></span>

  <span data-ttu-id="e12e9-117">Notez que le code ci-dessous est fonctionnel, mais que le paramètre ImageName passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-118">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="e12e9-119">Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Restart-AzVM`</span><span class="sxs-lookup"><span data-stu-id="e12e9-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="e12e9-120">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-120">Before</span></span>

  <span data-ttu-id="e12e9-121">Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-122">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="e12e9-123">Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Start-AzVM`</span><span class="sxs-lookup"><span data-stu-id="e12e9-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="e12e9-124">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-124">Before</span></span>

  <span data-ttu-id="e12e9-125">Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-126">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="e12e9-127">Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Stop-AzVM`</span><span class="sxs-lookup"><span data-stu-id="e12e9-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="e12e9-128">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-128">Before</span></span>

  <span data-ttu-id="e12e9-129">Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-130">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="e12e9-131">Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Remove-AzVM`</span><span class="sxs-lookup"><span data-stu-id="e12e9-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="e12e9-132">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-132">Before</span></span>

  <span data-ttu-id="e12e9-133">Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-134">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="e12e9-135">Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Set-AzVM`</span><span class="sxs-lookup"><span data-stu-id="e12e9-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="e12e9-136">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-136">Before</span></span>

  <span data-ttu-id="e12e9-137">Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-138">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="e12e9-139">Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Save-AzVMImage`</span><span class="sxs-lookup"><span data-stu-id="e12e9-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="e12e9-140">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-140">Before</span></span>
  <span data-ttu-id="e12e9-141">Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="e12e9-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="e12e9-142">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="e12e9-143">La propriété ProtectionPolicy a été ajoutée pour encapsuler la propriété `ProtectFromScaleIn` dans `PSVirtualMachineScaleSetVM`</span><span class="sxs-lookup"><span data-stu-id="e12e9-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-144">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-145">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="e12e9-146">La propriété ```EncryptionSettingsCollection``` a été ajoutée pour inclure la propriété `EncryptionSettings` dans `PSDisk`</span><span class="sxs-lookup"><span data-stu-id="e12e9-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-147">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-148">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="e12e9-149">La propriété ```EncryptionSettingsCollection``` a été ajoutée pour inclure la propriété `EncryptionSettings` dans `PSSnapshot`</span><span class="sxs-lookup"><span data-stu-id="e12e9-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-150">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-151">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="e12e9-152">La propriété `VirtualMachineProfile` a été supprimée de `PSVirtualMachineScaleSet`</span><span class="sxs-lookup"><span data-stu-id="e12e9-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-153">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-154">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="e12e9-155">L’alias de l’applet de commande `Set-AzVMBootDiagnostic` vers `Set-AzVMBootDiagnostics` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="e12e9-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-156">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-156">Before</span></span>

  <span data-ttu-id="e12e9-157">Utilisation de l’alias déprécié</span><span class="sxs-lookup"><span data-stu-id="e12e9-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-158">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="e12e9-159">L’alias de l’applet de commande `Export-AzLogAnalyticThrottledRequest` vers `Export-AzLogAnalyticThrottledRequests` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="e12e9-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-160">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-160">Before</span></span>

  <span data-ttu-id="e12e9-161">Utilisation de l’alias déprécié</span><span class="sxs-lookup"><span data-stu-id="e12e9-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-162">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="e12e9-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e12e9-163">Az.HDInsight</span></span>

- <span data-ttu-id="e12e9-164">Les applets de commande `Grant-AzHDInsightHttpServicesAccess` et `Revoke-AzHDInsightHttpServicesAccess` ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="e12e9-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="e12e9-165">Elles ne sont plus nécessaires, car l’accès HTTP est toujours activé sur tous les clusters HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e12e9-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="e12e9-166">L’applet de commande `Set-AzHDInsightGatewayCredential` a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="e12e9-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="e12e9-167">Utilisez cette applet de commande pour changer le nom d’utilisateur et le mot de passe HTTP de la passerelle (elle remplace `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="e12e9-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="e12e9-168">L’applet de commande `Get-AzHDInsightJobOutput` a été mise à jour de façon à prendre en charge la précision de l’accès en fonction du rôle à la clé de stockage.</span><span class="sxs-lookup"><span data-stu-id="e12e9-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="e12e9-169">Les utilisateurs avec les rôles Opérateur, Contributeur et Propriétaire de cluster HDInsight ne seront pas affectés.</span><span class="sxs-lookup"><span data-stu-id="e12e9-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="e12e9-170">Les utilisateurs qui ont seulement le rôle Lecteur doivent spécifier explicitement le paramètre `DefaultStorageAccountKey`.</span><span class="sxs-lookup"><span data-stu-id="e12e9-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="e12e9-171">Pour plus d’informations sur ces modifications de l’accès en fonction du rôle, consultez [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="e12e9-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](http://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="e12e9-172">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-173">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="e12e9-174">Utilisateurs avec seulement le rôle Lecteur pour l’applet de commande Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="e12e9-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="e12e9-175">Avant</span><span class="sxs-lookup"><span data-stu-id="e12e9-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="e12e9-176">Après</span><span class="sxs-lookup"><span data-stu-id="e12e9-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="e12e9-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e12e9-177">Az.Storage</span></span>

- <span data-ttu-id="e12e9-178">Les espaces de noms pour les types retournés depuis les applets de commande pour les objets Blob, File d’attente et Fichier ont été changés de `Microsoft.WindowsAzure.Storage` en `Microsoft.Azure.Storage`.</span><span class="sxs-lookup"><span data-stu-id="e12e9-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="e12e9-179">Bien que ceci ne représente pas un changement cassant sur le plan technique du point de vue de la stratégie des changements cassants, il peut nécessiter certaines modifications dans le code qui utilise les méthodes du SDK Stockage .NET pour interagir avec les objets retournés par ces applets de commande.</span><span class="sxs-lookup"><span data-stu-id="e12e9-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="e12e9-180">Exemple 1 :  Ajouter un message à une file d’attente (changement de l’espace de noms de l’objet CloudQueueMessage)</span><span class="sxs-lookup"><span data-stu-id="e12e9-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="e12e9-181">Avant :</span><span class="sxs-lookup"><span data-stu-id="e12e9-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="e12e9-182">Après :</span><span class="sxs-lookup"><span data-stu-id="e12e9-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="e12e9-183">Exemple 2 :  Extraire les attributs d’un objet Blob/Fichier avec AccessCondition (changement de l’espace de noms de l’objet AccessCondition)</span><span class="sxs-lookup"><span data-stu-id="e12e9-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="e12e9-184">Avant :</span><span class="sxs-lookup"><span data-stu-id="e12e9-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="e12e9-185">Après :</span><span class="sxs-lookup"><span data-stu-id="e12e9-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="e12e9-186">Il ne s’agit pas techniquement d’un changement cassant, mais vous constaterez des différences de sortie dans la propriété Sku.Name des comptes de stockage retournés depuis `New/Get/Set-AzStorageAccount`. Les changements sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="e12e9-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="e12e9-187">(Après la modification, le SkuName en entrée et en sortie sont alignés.)</span><span class="sxs-lookup"><span data-stu-id="e12e9-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="e12e9-188">« StandardLRS » -> « Standard_LRS » ;</span><span class="sxs-lookup"><span data-stu-id="e12e9-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="e12e9-189">« StandardGRS » -> « Standard_GRS » ;</span><span class="sxs-lookup"><span data-stu-id="e12e9-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="e12e9-190">« StandardRAGRS » -> « Standard_RAGRS » ;</span><span class="sxs-lookup"><span data-stu-id="e12e9-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="e12e9-191">« StandardZRS » -> « Standard_ZRS » ;</span><span class="sxs-lookup"><span data-stu-id="e12e9-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="e12e9-192">« PremiumLRS » -> « Premium_LRS » ;</span><span class="sxs-lookup"><span data-stu-id="e12e9-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="e12e9-193">Le comportement par défaut du service quand vous créez un compte de stockage sans spécifier un type (Kind) a changé.</span><span class="sxs-lookup"><span data-stu-id="e12e9-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="e12e9-194">Dans les versions précédentes, quand un compte de stockage était créé sans spécification de `Kind`, le type de compte de stockage `Storage` était utilisé ; dans la nouvelle version, `StorageV2` est la valeur par défaut de `Kind`.</span><span class="sxs-lookup"><span data-stu-id="e12e9-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="e12e9-195">Si vous devez créer un compte de stockage V1 avec le type « Stockage », ajoutez le paramètre « -Kind Storage »</span><span class="sxs-lookup"><span data-stu-id="e12e9-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="e12e9-196">Exemple : Créer un stockage de compte (changement du type par défaut)</span><span class="sxs-lookup"><span data-stu-id="e12e9-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="e12e9-197">Avant :</span><span class="sxs-lookup"><span data-stu-id="e12e9-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="e12e9-198">Après :</span><span class="sxs-lookup"><span data-stu-id="e12e9-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
