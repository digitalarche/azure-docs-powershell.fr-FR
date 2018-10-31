---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117256"
---
# <a name="release-notes"></a><span data-ttu-id="8cc1d-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="8cc1d-103">Release notes</span></span>

<span data-ttu-id="8cc1d-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="8cc1d-105">6.8.0 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc1d-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="8cc1d-106">General</span></span>
* <span data-ttu-id="8cc1d-107">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-108">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-109">Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-110">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-111">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="8cc1d-112">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="8cc1d-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="8cc1d-113">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="8cc1d-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8cc1d-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc1d-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="8cc1d-115">Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-116">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-117">Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="8cc1d-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8cc1d-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8cc1d-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8cc1d-119">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="8cc1d-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc1d-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc1d-120">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc1d-121">Résolution du problème de création d’application managée depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc1d-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc1d-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc1d-123">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="8cc1d-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc1d-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc1d-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc1d-125">Prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="8cc1d-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="8cc1d-126">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="8cc1d-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="8cc1d-127">Prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="8cc1d-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="8cc1d-128">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8cc1d-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="8cc1d-129">Prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="8cc1d-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="8cc1d-130">Prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="8cc1d-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="8cc1d-131">Prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8cc1d-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc1d-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc1d-132">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc1d-133">Résolution du problème relatif aux groupes de ressources par défaut mal définis.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="8cc1d-134">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-135">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-136">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc1d-137">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="8cc1d-138">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="8cc1d-139">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="8cc1d-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-140">Azure.Storage</span></span>
* <span data-ttu-id="8cc1d-141">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="8cc1d-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8cc1d-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8cc1d-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8cc1d-144">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="8cc1d-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="8cc1d-146">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc1d-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc1d-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc1d-148">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="8cc1d-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="8cc1d-150">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8cc1d-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8cc1d-151">AzureRM.Automation</span></span>
* <span data-ttu-id="8cc1d-152">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="8cc1d-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc1d-153">AzureRM.Backup</span></span>
* <span data-ttu-id="8cc1d-154">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8cc1d-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8cc1d-155">AzureRM.Batch</span></span>
* <span data-ttu-id="8cc1d-156">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="8cc1d-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="8cc1d-157">AzureRM.Billing</span></span>
* <span data-ttu-id="8cc1d-158">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="8cc1d-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="8cc1d-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="8cc1d-160">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="8cc1d-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="8cc1d-162">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-163">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-164">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc1d-165">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="8cc1d-166">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="8cc1d-167">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8cc1d-168">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8cc1d-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8cc1d-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="8cc1d-170">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="8cc1d-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8cc1d-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="8cc1d-172">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="8cc1d-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8cc1d-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="8cc1d-174">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="8cc1d-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="8cc1d-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="8cc1d-176">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc1d-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc1d-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc1d-178">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8cc1d-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cc1d-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8cc1d-180">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc1d-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc1d-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc1d-182">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="8cc1d-183">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8cc1d-184">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc1d-185">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="8cc1d-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8cc1d-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="8cc1d-187">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="8cc1d-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="8cc1d-188">AzureRM.Dns</span></span>
* <span data-ttu-id="8cc1d-189">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8cc1d-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc1d-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8cc1d-191">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc1d-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc1d-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc1d-193">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="8cc1d-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc1d-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="8cc1d-195">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8cc1d-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-196">AzureRM.Insights</span></span>
* <span data-ttu-id="8cc1d-197">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8cc1d-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc1d-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="8cc1d-199">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc1d-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc1d-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc1d-201">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8cc1d-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8cc1d-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8cc1d-203">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="8cc1d-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8cc1d-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="8cc1d-205">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="8cc1d-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="8cc1d-207">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="8cc1d-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8cc1d-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="8cc1d-209">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="8cc1d-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="8cc1d-210">AzureRM.Media</span></span>
* <span data-ttu-id="8cc1d-211">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-212">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-213">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="8cc1d-214">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8cc1d-215">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="8cc1d-216">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8cc1d-217">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8cc1d-218">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8cc1d-219">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="8cc1d-220">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="8cc1d-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8cc1d-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="8cc1d-222">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="8cc1d-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8cc1d-224">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8cc1d-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8cc1d-226">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8cc1d-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8cc1d-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8cc1d-228">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="8cc1d-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="8cc1d-230">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8cc1d-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc1d-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8cc1d-232">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="8cc1d-233">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="8cc1d-234">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="8cc1d-235">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc1d-236">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="8cc1d-237">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8cc1d-238">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="8cc1d-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8cc1d-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8cc1d-240">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="8cc1d-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8cc1d-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="8cc1d-242">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8cc1d-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8cc1d-243">AzureRM.Relay</span></span>
* <span data-ttu-id="8cc1d-244">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc1d-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc1d-245">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc1d-246">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="8cc1d-247">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="8cc1d-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc1d-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc1d-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc1d-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc1d-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc1d-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8cc1d-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="8cc1d-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8cc1d-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="8cc1d-255">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="8cc1d-256">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="8cc1d-257">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8cc1d-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8cc1d-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8cc1d-259">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc1d-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc1d-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc1d-261">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8cc1d-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc1d-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8cc1d-263">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc1d-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-264">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-265">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8cc1d-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-266">AzureRM.Storage</span></span>
* <span data-ttu-id="8cc1d-267">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="8cc1d-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cc1d-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="8cc1d-269">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8cc1d-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8cc1d-270">AzureRM.Tags</span></span>
* <span data-ttu-id="8cc1d-271">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc1d-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc1d-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc1d-273">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="8cc1d-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="8cc1d-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="8cc1d-275">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc1d-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc1d-276">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc1d-277">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="8cc1d-278">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc1d-279">Généralités</span><span class="sxs-lookup"><span data-stu-id="8cc1d-279">General</span></span>
* <span data-ttu-id="8cc1d-280">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-281">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-282">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="8cc1d-283">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8cc1d-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-284">Azure.Storage</span></span>
* <span data-ttu-id="8cc1d-285">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="8cc1d-286">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc1d-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc1d-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc1d-288">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="8cc1d-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="8cc1d-289">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="8cc1d-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="8cc1d-290">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="8cc1d-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="8cc1d-291">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="8cc1d-292">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="8cc1d-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="8cc1d-293">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="8cc1d-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-294">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-295">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="8cc1d-296">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="8cc1d-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="8cc1d-297">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="8cc1d-298">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="8cc1d-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="8cc1d-299">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="8cc1d-300">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="8cc1d-301">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8cc1d-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="8cc1d-302">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="8cc1d-303">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="8cc1d-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="8cc1d-304">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc1d-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc1d-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc1d-306">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="8cc1d-307">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="8cc1d-308">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="8cc1d-309">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc1d-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc1d-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc1d-311">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="8cc1d-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc1d-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc1d-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc1d-313">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="8cc1d-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8cc1d-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-314">AzureRM.Insights</span></span>
* <span data-ttu-id="8cc1d-315">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="8cc1d-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="8cc1d-316">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="8cc1d-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc1d-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc1d-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc1d-318">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc1d-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-319">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-320">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc1d-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc1d-321">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc1d-322">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="8cc1d-323">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc1d-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc1d-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc1d-325">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="8cc1d-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="8cc1d-326">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="8cc1d-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="8cc1d-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-327">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-328">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="8cc1d-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc1d-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8cc1d-330">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="8cc1d-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="8cc1d-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="8cc1d-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="8cc1d-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="8cc1d-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="8cc1d-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="8cc1d-334">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8cc1d-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="8cc1d-335">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="8cc1d-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8cc1d-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-336">AzureRM.Storage</span></span>
* <span data-ttu-id="8cc1d-337">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cc1d-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="8cc1d-338">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="8cc1d-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="8cc1d-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cc1d-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8cc1d-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cc1d-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8cc1d-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cc1d-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8cc1d-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8cc1d-342">AzureRM.Tags</span></span>
* <span data-ttu-id="8cc1d-343">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="8cc1d-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="8cc1d-344">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-345">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-346">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8cc1d-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-347">Azure.Storage</span></span>
* <span data-ttu-id="8cc1d-348">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="8cc1d-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="8cc1d-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8cc1d-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="8cc1d-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8cc1d-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8cc1d-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8cc1d-352">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8cc1d-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8cc1d-353">AzureRM.Automation</span></span>
* <span data-ttu-id="8cc1d-354">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-355">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-356">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8cc1d-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="8cc1d-357">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8cc1d-358">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8cc1d-359">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="8cc1d-360">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc1d-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc1d-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc1d-362">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="8cc1d-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc1d-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc1d-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc1d-364">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc1d-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8cc1d-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8cc1d-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8cc1d-366">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8cc1d-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-367">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-368">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cc1d-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="8cc1d-369">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8cc1d-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="8cc1d-370">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="8cc1d-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="8cc1d-371">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="8cc1d-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="8cc1d-372">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="8cc1d-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="8cc1d-373">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="8cc1d-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8cc1d-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8cc1d-374">AzureRM.Relay</span></span>
* <span data-ttu-id="8cc1d-375">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="8cc1d-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc1d-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc1d-376">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc1d-377">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="8cc1d-378">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="8cc1d-379">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="8cc1d-380">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8cc1d-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="8cc1d-381">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="8cc1d-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc1d-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc1d-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc1d-383">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="8cc1d-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="8cc1d-384">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="8cc1d-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc1d-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc1d-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc1d-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc1d-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="8cc1d-390">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="8cc1d-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8cc1d-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc1d-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8cc1d-392">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc1d-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-393">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-394">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="8cc1d-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="8cc1d-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc1d-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="8cc1d-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc1d-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc1d-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc1d-397">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc1d-398">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="8cc1d-399">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="8cc1d-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="8cc1d-400">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="8cc1d-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="8cc1d-401">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc1d-402">Généralités</span><span class="sxs-lookup"><span data-stu-id="8cc1d-402">General</span></span>
* <span data-ttu-id="8cc1d-403">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="8cc1d-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-404">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-405">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="8cc1d-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-406">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-407">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="8cc1d-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="8cc1d-408">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="8cc1d-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="8cc1d-409">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc1d-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="8cc1d-410">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="8cc1d-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="8cc1d-411">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="8cc1d-412">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="8cc1d-413">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8cc1d-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cc1d-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8cc1d-415">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="8cc1d-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc1d-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8cc1d-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc1d-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8cc1d-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc1d-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc1d-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc1d-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc1d-420">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="8cc1d-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8cc1d-421">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="8cc1d-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8cc1d-422">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="8cc1d-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="8cc1d-423">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="8cc1d-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc1d-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc1d-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc1d-425">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8cc1d-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="8cc1d-426">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="8cc1d-427">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="8cc1d-428">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc1d-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc1d-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc1d-430">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="8cc1d-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-431">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-432">Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone</span><span class="sxs-lookup"><span data-stu-id="8cc1d-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="8cc1d-433">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="8cc1d-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="8cc1d-434">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8cc1d-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8cc1d-435">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8cc1d-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8cc1d-436">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8cc1d-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8cc1d-437">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8cc1d-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8cc1d-438">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8cc1d-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8cc1d-439">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8cc1d-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8cc1d-440">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8cc1d-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8cc1d-441">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8cc1d-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8cc1d-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc1d-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8cc1d-443">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="8cc1d-444">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="8cc1d-445">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc1d-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc1d-446">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc1d-447">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="8cc1d-448">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="8cc1d-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="8cc1d-449">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="8cc1d-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="8cc1d-450">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="8cc1d-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="8cc1d-451">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8cc1d-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="8cc1d-452">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="8cc1d-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8cc1d-453">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="8cc1d-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8cc1d-454">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8cc1d-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="8cc1d-455">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="8cc1d-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8cc1d-456">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="8cc1d-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8cc1d-457">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="8cc1d-458">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8cc1d-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="8cc1d-459">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="8cc1d-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc1d-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc1d-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc1d-461">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc1d-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-462">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-463">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8cc1d-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="8cc1d-464">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="8cc1d-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="8cc1d-465">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-466">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-467">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="8cc1d-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="8cc1d-468">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="8cc1d-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8cc1d-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-469">Azure.Storage</span></span>
* <span data-ttu-id="8cc1d-470">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-471">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-472">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="8cc1d-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="8cc1d-473">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="8cc1d-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="8cc1d-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8cc1d-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8cc1d-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8cc1d-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8cc1d-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8cc1d-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8cc1d-477">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="8cc1d-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc1d-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="8cc1d-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc1d-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="8cc1d-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc1d-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="8cc1d-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc1d-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="8cc1d-482">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc1d-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="8cc1d-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc1d-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="8cc1d-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="8cc1d-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8cc1d-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="8cc1d-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc1d-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc1d-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc1d-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc1d-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc1d-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8cc1d-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="8cc1d-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8cc1d-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8cc1d-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="8cc1d-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="8cc1d-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8cc1d-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8cc1d-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8cc1d-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="8cc1d-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8cc1d-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="8cc1d-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8cc1d-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8cc1d-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc1d-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8cc1d-498">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc1d-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc1d-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc1d-500">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="8cc1d-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8cc1d-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8cc1d-502">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="8cc1d-503">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="8cc1d-504">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8cc1d-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8cc1d-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc1d-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8cc1d-506">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="8cc1d-507">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc1d-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-508">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-509">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="8cc1d-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc1d-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc1d-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc1d-511">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8cc1d-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc1d-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc1d-512">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc1d-513">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8cc1d-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="8cc1d-514">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8cc1d-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="8cc1d-515">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="8cc1d-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8cc1d-517">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="8cc1d-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="8cc1d-518">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-519">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-520">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="8cc1d-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc1d-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc1d-521">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc1d-522">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="8cc1d-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="8cc1d-523">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="8cc1d-524">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8cc1d-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc1d-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc1d-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc1d-526">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="8cc1d-527">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="8cc1d-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="8cc1d-528">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="8cc1d-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="8cc1d-529">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="8cc1d-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="8cc1d-530">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="8cc1d-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="8cc1d-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc1d-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc1d-532">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="8cc1d-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-533">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-534">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="8cc1d-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc1d-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc1d-535">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc1d-536">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="8cc1d-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8cc1d-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8cc1d-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8cc1d-538">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="8cc1d-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="8cc1d-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-539">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-540">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="8cc1d-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="8cc1d-541">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc1d-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8cc1d-542">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cc1d-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8cc1d-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8cc1d-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8cc1d-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8cc1d-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8cc1d-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc1d-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc1d-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc1d-546">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc1d-547">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="8cc1d-548">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="8cc1d-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc1d-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc1d-549">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc1d-550">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="8cc1d-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8cc1d-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc1d-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8cc1d-552">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="8cc1d-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc1d-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc1d-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc1d-554">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="8cc1d-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="8cc1d-555">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc1d-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="8cc1d-556">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="8cc1d-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="8cc1d-557">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="8cc1d-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="8cc1d-558">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="8cc1d-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="8cc1d-559">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="8cc1d-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="8cc1d-560">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="8cc1d-560">Added support for MSI identity</span></span>
* <span data-ttu-id="8cc1d-561">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="8cc1d-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc1d-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="8cc1d-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="8cc1d-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="8cc1d-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="8cc1d-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc1d-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8cc1d-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8cc1d-566">AzureRM.Batch</span></span>
* <span data-ttu-id="8cc1d-567">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="8cc1d-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="8cc1d-568">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="8cc1d-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8cc1d-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8cc1d-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="8cc1d-570">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="8cc1d-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc1d-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc1d-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc1d-572">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="8cc1d-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8cc1d-573">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc1d-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="8cc1d-574">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc1d-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc1d-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc1d-575">AzureRM.Network</span></span>
* <span data-ttu-id="8cc1d-576">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="8cc1d-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="8cc1d-577">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="8cc1d-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc1d-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="8cc1d-579">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="8cc1d-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8cc1d-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8cc1d-581">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="8cc1d-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8cc1d-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8cc1d-583">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="8cc1d-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8cc1d-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8cc1d-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc1d-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8cc1d-586">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="8cc1d-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc1d-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc1d-587">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc1d-588">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8cc1d-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="8cc1d-589">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="8cc1d-590">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="8cc1d-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="8cc1d-591">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="8cc1d-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="8cc1d-592">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="8cc1d-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="8cc1d-593">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc1d-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8cc1d-594">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cc1d-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8cc1d-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8cc1d-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8cc1d-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8cc1d-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8cc1d-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc1d-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc1d-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc1d-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc1d-599">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="8cc1d-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
