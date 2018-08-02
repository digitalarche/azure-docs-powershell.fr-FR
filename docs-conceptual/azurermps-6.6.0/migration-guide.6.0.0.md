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
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368005"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="a78d8-103">Dernières modifications de Microsoft Azure PowerShell 6.0.0</span><span class="sxs-lookup"><span data-stu-id="a78d8-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="a78d8-104">Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a78d8-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a78d8-105">Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance.</span><span class="sxs-lookup"><span data-stu-id="a78d8-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="a78d8-106">Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.</span><span class="sxs-lookup"><span data-stu-id="a78d8-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="a78d8-107">Sommaire</span><span class="sxs-lookup"><span data-stu-id="a78d8-107">Table of Contents</span></span>

- [<span data-ttu-id="a78d8-108">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="a78d8-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="a78d8-109">Version PowerShell minimale requise passée à la version 5.0</span><span class="sxs-lookup"><span data-stu-id="a78d8-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="a78d8-110">Enregistrement automatique du contexte activé par défaut</span><span class="sxs-lookup"><span data-stu-id="a78d8-110">Context autosaved enabled by default</span></span>](#context-autosaved-enabled-by-default)
    - [<span data-ttu-id="a78d8-111">Suppression de l’alias des balises</span><span class="sxs-lookup"><span data-stu-id="a78d8-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="a78d8-112">Dernières modifications des applets de commande AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a78d8-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="a78d8-113">Dernières modifications des applets de commande AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a78d8-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="a78d8-114">Dernières modifications des applets de commande AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a78d8-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="a78d8-115">Dernières modifications des applets de commande AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a78d8-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="a78d8-116">Dernières modifications des applets de commande AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a78d8-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="a78d8-117">Dernières modifications des applets de commande AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a78d8-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="a78d8-118">Dernières modifications des applets de commande AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a78d8-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="a78d8-119">Dernières modifications des applets de commande AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a78d8-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="a78d8-120">Dernières modifications des applets de commande AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a78d8-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="a78d8-121">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="a78d8-122">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="a78d8-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="a78d8-123">Version PowerShell minimale requise passée à la version 5.0</span><span class="sxs-lookup"><span data-stu-id="a78d8-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="a78d8-124">Auparavant, Azure PowerShell nécessitait _au moins_ la version 3.0 de PowerShell pour exécuter un applet de commande.</span><span class="sxs-lookup"><span data-stu-id="a78d8-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="a78d8-125">La version 5.0 de PowerShell est maintenant exigée.</span><span class="sxs-lookup"><span data-stu-id="a78d8-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="a78d8-126">Pour plus d’informations sur la mise à niveau vers PowerShell 5.0, consultez [ce tableau](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="a78d8-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="a78d8-127">Enregistrement automatique du contexte activé par défaut</span><span class="sxs-lookup"><span data-stu-id="a78d8-127">Context autosave enabled by default</span></span>

<span data-ttu-id="a78d8-128">L’enregistrement automatique du contexte correspond au stockage des informations de connexion Azure pouvant être utilisées entre des sessions nouvelles et différentes de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a78d8-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="a78d8-129">Pour plus d’informations sur cet enregistrement automatique du contexte, consultez [ce document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="a78d8-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/en-us/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="a78d8-130">Précédemment, cette fonctionnalité d’enregistrement automatique du contexte était désactivée par défaut, ce qui signifie que les informations d’authentification Azure de l’utilisateur n’étaient pas stockées entre les sessions jusqu’à l’exécution de l’applet de commande `Enable-AzureRmContextAutosave` visant à activer la persistance du contexte.</span><span class="sxs-lookup"><span data-stu-id="a78d8-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="a78d8-131">En progressant, l’enregistrement automatique du contexte sera activé par défaut, ce qui signifie que les utilisateurs _sans aucun paramètre d’enregistrement automatique du contexte_ verront leur contexte stocké lors de leur prochaine connexion.</span><span class="sxs-lookup"><span data-stu-id="a78d8-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="a78d8-132">Les utilisateurs peuvent désactiver cette fonctionnalité à l’aide de l’applet de commande `Disable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="a78d8-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="a78d8-133">_Remarque_ : les utilisateurs ayant précédemment désactivé cet enregistrement automatique du contexte ou bien les utilisateurs dont l’enregistrement automatique du contexte est activé et des contextes existants ne seront pas affectés par cette modification</span><span class="sxs-lookup"><span data-stu-id="a78d8-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="a78d8-134">Suppression de l’alias des balises</span><span class="sxs-lookup"><span data-stu-id="a78d8-134">Removal of Tags alias</span></span>

<span data-ttu-id="a78d8-135">L’alias `Tags` pour le paramètre `Tag` a été supprimé sur nombreux applets de commande.</span><span class="sxs-lookup"><span data-stu-id="a78d8-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="a78d8-136">Voici une liste des modules affectés (et les applets de commande correspondants) :</span><span class="sxs-lookup"><span data-stu-id="a78d8-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

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

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="a78d8-137">Dernières modifications des applets de commande AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a78d8-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="a78d8-138">**Divers**</span><span class="sxs-lookup"><span data-stu-id="a78d8-138">**Miscellaneous**</span></span>
- <span data-ttu-id="a78d8-139">La propriété de nom de référence (SKU) imbriquée dans les types `PSDisk` et `PSSnapshot` a été remplacée, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="a78d8-140">La propriété de type de compte de stockage imbriquée dans les types `PSVirtualMachine`, `PSVirtualMachineScaleSet` et `PSImage` a été remplacée, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="a78d8-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="a78d8-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="a78d8-142">Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="a78d8-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="a78d8-144">Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de `StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="a78d8-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="a78d8-146">Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="a78d8-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="a78d8-148">Le paramètre `Managed` a été supprimé en faveur de `Sku`</span><span class="sxs-lookup"><span data-stu-id="a78d8-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="a78d8-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="a78d8-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="a78d8-150">Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="a78d8-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="a78d8-152">Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="a78d8-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="a78d8-154">Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="a78d8-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="a78d8-156">Les valeurs acceptées pour le paramètre `SkuName` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="a78d8-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="a78d8-158">Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="a78d8-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="a78d8-160">Le paramètre `DisableWAD` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="a78d8-161">Les diagnostics Microsoft Azure ont été désactivés par défaut</span><span class="sxs-lookup"><span data-stu-id="a78d8-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="a78d8-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="a78d8-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="a78d8-163">Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="a78d8-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="a78d8-165">Les valeurs acceptées pour le paramètre `StorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="a78d8-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="a78d8-167">Les valeurs acceptées pour le paramètre `ManagedDisk` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="a78d8-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="a78d8-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="a78d8-169">Les valeurs acceptées pour le paramètre `ManagedDiskStorageAccountType` ont été remplacées, respectivement de`StandardLRS` et `PremiumLRS` vers `Standard_LRS` et `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="a78d8-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="a78d8-170">Dernières modifications des applets de commande AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a78d8-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="a78d8-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="a78d8-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="a78d8-172">Les paramètres `PerFileThreadCount` et `ConcurrentFileCount` ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="a78d8-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="a78d8-173">Utilisez dorénavant le paramètre `Concurrency`</span><span class="sxs-lookup"><span data-stu-id="a78d8-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="a78d8-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="a78d8-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="a78d8-175">Les paramètres `PerFileThreadCount` et `ConcurrentFileCount` ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="a78d8-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="a78d8-176">Utilisez dorénavant le paramètre `Concurrency`</span><span class="sxs-lookup"><span data-stu-id="a78d8-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="a78d8-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="a78d8-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="a78d8-178">Le paramètre `Clean` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="a78d8-179">Dernières modifications des applets de commande AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="a78d8-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="a78d8-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="a78d8-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="a78d8-181">Le paramètre `Force` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="a78d8-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="a78d8-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="a78d8-183">Le paramètre `Force` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="a78d8-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="a78d8-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="a78d8-185">Le paramètre `Force` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="a78d8-186">Dernières modifications des applets de commande AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a78d8-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="a78d8-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="a78d8-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="a78d8-188">Les alias des paramètres `AutoscaleProfiles` et `Notifications` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="a78d8-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="a78d8-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="a78d8-190">Les alias des paramètres `Categories` et `Locations` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="a78d8-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="a78d8-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="a78d8-192">L’alias des paramètres `Actions` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="a78d8-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="a78d8-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="a78d8-194">L’alias des paramètres `Actions` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="a78d8-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="a78d8-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="a78d8-196">Les alias des paramètres `MaxRecords` et `MaxEvents` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="a78d8-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="a78d8-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="a78d8-198">L’alias des paramètres `MetricNames` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="a78d8-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="a78d8-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="a78d8-200">Les alias des paramètres `CustomEmails` et `SendToServiceOwners` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="a78d8-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="a78d8-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="a78d8-202">L’alias des paramètres `Properties` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="a78d8-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="a78d8-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="a78d8-204">Les alias des paramètres `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` et `Webhooks` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="a78d8-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="a78d8-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="a78d8-206">Les alias des paramètres `Rules`, `ScheduleDays`, `ScheduleHours` et `ScheduleMinutes` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="a78d8-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="a78d8-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="a78d8-208">L’alias des paramètres `Properties` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="a78d8-209">Dernières modifications des applets de commande AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a78d8-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="a78d8-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="a78d8-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="a78d8-211">Le paramètre `CertificatePolicy` est devenu obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a78d8-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="a78d8-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="a78d8-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="a78d8-213">L’applet de commande n’accepte plus de paramètres individuels qui composent le jeton d’accès ; au lieu de cela, l’applet de commande remplace les paramètres de jeton explicites, comme `Service` ou `Permissions`, par un paramètre générique `TemplateUri`, correspondant à un exemple de jeton d’accès défini ailleurs (vraisemblablement à l’aide des applets de commande de stockage PowerShell, ou composé manuellement en fonction de la documentation du stockage.) L’applet de commande conserve le paramètre `ValidityPeriod`.</span><span class="sxs-lookup"><span data-stu-id="a78d8-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="a78d8-214">Pour plus d’informations sur la composition de jetons d’accès partagés pour le stockage Azure, reportez-vous aux pages de documentation, respectivement :</span><span class="sxs-lookup"><span data-stu-id="a78d8-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="a78d8-215">[Construction d’un service SAP] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="a78d8-215">[Constructing a Service SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="a78d8-216">[Construction d’un compte SAP] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="a78d8-216">[Constructing an Account SAS] (https://docs.microsoft.com/en-us/rest/api/storageservices/constructing-an-account-sas)</span></span>

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

<span data-ttu-id="a78d8-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="a78d8-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="a78d8-218">Le paramètre `IssuerProvider` est devenu obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a78d8-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="a78d8-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="a78d8-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="a78d8-220">La sortie de cet applet de commande est passée de `CertificateBundle` à `PSKeyVaultCertificate`.</span><span class="sxs-lookup"><span data-stu-id="a78d8-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="a78d8-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="a78d8-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="a78d8-222">`ResourceGroupName` a été supprimé de l’ensemble de paramètres `InputObject`, et il est maintenant obtenu à partir de la propriété `ResourceId` du paramètre `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="a78d8-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="a78d8-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="a78d8-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="a78d8-224">L’autorisation `all` a été supprimée de `PermissionsToKeys`, `PermissionsToSecrets`, et `PermissionsToCertificates`.</span><span class="sxs-lookup"><span data-stu-id="a78d8-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="a78d8-225">**Généralités**</span><span class="sxs-lookup"><span data-stu-id="a78d8-225">**General**</span></span>
- <span data-ttu-id="a78d8-226">La propriété `ValueFromPipelineByPropertyName` a été supprimée de tous les applets de commande où la redirection par `InputObject` était activée.</span><span class="sxs-lookup"><span data-stu-id="a78d8-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="a78d8-227">Les applets de commande affectés sont :</span><span class="sxs-lookup"><span data-stu-id="a78d8-227">The cmdlets affected are:</span></span>
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

- <span data-ttu-id="a78d8-228">Les niveaux `ConfirmImpact` ont été supprimés de tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="a78d8-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="a78d8-229">Les applets de commande affectés sont :</span><span class="sxs-lookup"><span data-stu-id="a78d8-229">The cmdlets affected are:</span></span>
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

- <span data-ttu-id="a78d8-230">`IKeyVaultDataServiceClient` a été mis à jour afin que toutes les opérations de certificat retournent PSTypes plutôt que des types de kits de développement logiciel.</span><span class="sxs-lookup"><span data-stu-id="a78d8-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="a78d8-231">notamment :</span><span class="sxs-lookup"><span data-stu-id="a78d8-231">This includes:</span></span>
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

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="a78d8-232">Dernières modifications des applets de commande AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a78d8-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="a78d8-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d8-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="a78d8-234">Le paramètre `ProbeEnabled` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="a78d8-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="a78d8-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="a78d8-236">L’alias des paramètres `AlloowGatewayTransit` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="a78d8-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d8-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="a78d8-238">Le paramètre `ProbeEnabled` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="a78d8-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d8-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="a78d8-240">Le paramètre `ProbeEnabled` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="a78d8-241">Dernières modifications des applets de commande AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a78d8-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="a78d8-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="a78d8-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="a78d8-243">Les paramètres `Subnet` et `VirtualNetwork` ont été supprimés en faveur de `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="a78d8-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="a78d8-244">Le paramètre `RedisVersion` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="a78d8-245">Le paramètre `MaxMemoryPolicy` a été supprimé en faveur de `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="a78d8-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="a78d8-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="a78d8-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="a78d8-247">Le paramètre `MaxMemoryPolicy` a été supprimé en faveur de `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="a78d8-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="a78d8-248">Dernières modifications des applets de commande AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a78d8-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="a78d8-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="a78d8-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="a78d8-250">Cet applet de commande a été supprimé et la fonctionnalité a été déplacée vers `Get-AzureRmResource`</span><span class="sxs-lookup"><span data-stu-id="a78d8-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="a78d8-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="a78d8-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="a78d8-252">Cet applet de commande a été supprimé et la fonctionnalité a été déplacée vers `Get-AzureRmResourceGroup`</span><span class="sxs-lookup"><span data-stu-id="a78d8-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

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

<span data-ttu-id="a78d8-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="a78d8-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="a78d8-254">Le paramètre `AtScopeAndBelow` a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="a78d8-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="a78d8-255">Dernières modifications des applets de commande AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a78d8-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="a78d8-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="a78d8-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="a78d8-257">Le paramètre `EnableEncryptionService` a été supprimé</span><span class="sxs-lookup"><span data-stu-id="a78d8-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="a78d8-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="a78d8-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="a78d8-259">Les paramètres `EnableEncryptionService` et `DisableEncryptionService` ont été supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="a78d8-260">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="a78d8-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="a78d8-261">Le service Outils de gestion de serveur a été [retirée l’an dernier](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/) et par conséquent, le module correspondant pour SMT, `AzureRM.ServerManagement`, a été supprimé de `AzureRM` et s’arrête de faire progresser la livraison.</span><span class="sxs-lookup"><span data-stu-id="a78d8-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="a78d8-262">Le module `AzureRM.SiteRecovery` est remplacé par `AzureRM.RecoveryServices.SiteRecovery`, qui est un sur-ensemble fonctionnel du module `AzureRM.SiteRecovery` et inclut un nouvel ensemble d’applets de commande équivalents.</span><span class="sxs-lookup"><span data-stu-id="a78d8-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="a78d8-263">Vous trouverez ci-dessous la liste complète des mappages entre les anciens applets de commande et les nouveaux :</span><span class="sxs-lookup"><span data-stu-id="a78d8-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="a78d8-264">Applets de commande déconseillés</span><span class="sxs-lookup"><span data-stu-id="a78d8-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="a78d8-265">Applets de commande équivalents</span><span class="sxs-lookup"><span data-stu-id="a78d8-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="a78d8-266">Alias</span><span class="sxs-lookup"><span data-stu-id="a78d8-266">Aliases</span></span>                                  |
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
