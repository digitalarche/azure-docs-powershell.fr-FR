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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018697"
---
# <a name="release-notes"></a><span data-ttu-id="0b9d1-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="0b9d1-103">Release notes</span></span>

<span data-ttu-id="0b9d1-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="0b9d1-105">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-106">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-107">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0b9d1-108">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="0b9d1-109">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="0b9d1-110">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="0b9d1-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-111">Azure.Storage</span></span>
* <span data-ttu-id="0b9d1-112">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="0b9d1-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0b9d1-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0b9d1-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b9d1-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0b9d1-115">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="0b9d1-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b9d1-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="0b9d1-117">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0b9d1-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b9d1-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0b9d1-119">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="0b9d1-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="0b9d1-121">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="0b9d1-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="0b9d1-122">AzureRM.Automation</span></span>
* <span data-ttu-id="0b9d1-123">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="0b9d1-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="0b9d1-124">AzureRM.Backup</span></span>
* <span data-ttu-id="0b9d1-125">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="0b9d1-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0b9d1-126">AzureRM.Batch</span></span>
* <span data-ttu-id="0b9d1-127">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="0b9d1-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="0b9d1-128">AzureRM.Billing</span></span>
* <span data-ttu-id="0b9d1-129">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="0b9d1-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="0b9d1-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="0b9d1-131">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="0b9d1-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0b9d1-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="0b9d1-133">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0b9d1-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-134">AzureRM.Compute</span></span>
* <span data-ttu-id="0b9d1-135">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0b9d1-136">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="0b9d1-137">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="0b9d1-138">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="0b9d1-139">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="0b9d1-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0b9d1-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="0b9d1-141">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="0b9d1-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0b9d1-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="0b9d1-143">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="0b9d1-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0b9d1-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="0b9d1-145">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="0b9d1-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="0b9d1-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="0b9d1-147">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0b9d1-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b9d1-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0b9d1-149">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="0b9d1-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0b9d1-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="0b9d1-151">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0b9d1-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b9d1-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0b9d1-153">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="0b9d1-154">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="0b9d1-155">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0b9d1-156">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="0b9d1-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0b9d1-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="0b9d1-158">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="0b9d1-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="0b9d1-159">AzureRM.Dns</span></span>
* <span data-ttu-id="0b9d1-160">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="0b9d1-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0b9d1-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="0b9d1-162">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0b9d1-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b9d1-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="0b9d1-164">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="0b9d1-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0b9d1-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="0b9d1-166">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="0b9d1-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-167">AzureRM.Insights</span></span>
* <span data-ttu-id="0b9d1-168">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="0b9d1-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="0b9d1-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="0b9d1-170">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0b9d1-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b9d1-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0b9d1-172">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="0b9d1-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b9d1-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="0b9d1-174">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="0b9d1-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0b9d1-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="0b9d1-176">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="0b9d1-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="0b9d1-178">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="0b9d1-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0b9d1-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="0b9d1-180">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="0b9d1-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="0b9d1-181">AzureRM.Media</span></span>
* <span data-ttu-id="0b9d1-182">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0b9d1-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0b9d1-183">AzureRM.Network</span></span>
* <span data-ttu-id="0b9d1-184">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="0b9d1-185">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0b9d1-186">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="0b9d1-187">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="0b9d1-188">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="0b9d1-189">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0b9d1-190">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="0b9d1-191">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="0b9d1-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0b9d1-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="0b9d1-193">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="0b9d1-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="0b9d1-195">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="0b9d1-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="0b9d1-197">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="0b9d1-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0b9d1-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="0b9d1-199">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="0b9d1-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0b9d1-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="0b9d1-201">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0b9d1-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0b9d1-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0b9d1-203">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="0b9d1-204">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="0b9d1-205">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="0b9d1-206">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="0b9d1-207">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="0b9d1-208">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="0b9d1-209">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="0b9d1-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0b9d1-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0b9d1-211">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="0b9d1-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0b9d1-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="0b9d1-213">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="0b9d1-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="0b9d1-214">AzureRM.Relay</span></span>
* <span data-ttu-id="0b9d1-215">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0b9d1-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0b9d1-216">AzureRM.Resources</span></span>
* <span data-ttu-id="0b9d1-217">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="0b9d1-218">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="0b9d1-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="0b9d1-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="0b9d1-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="0b9d1-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="0b9d1-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="0b9d1-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0b9d1-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="0b9d1-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0b9d1-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="0b9d1-226">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="0b9d1-227">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="0b9d1-228">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="0b9d1-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="0b9d1-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="0b9d1-230">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0b9d1-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b9d1-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0b9d1-232">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0b9d1-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b9d1-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0b9d1-234">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0b9d1-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-235">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-236">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="0b9d1-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-237">AzureRM.Storage</span></span>
* <span data-ttu-id="0b9d1-238">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="0b9d1-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="0b9d1-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="0b9d1-240">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="0b9d1-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="0b9d1-241">AzureRM.Tags</span></span>
* <span data-ttu-id="0b9d1-242">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0b9d1-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0b9d1-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0b9d1-244">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="0b9d1-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="0b9d1-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="0b9d1-246">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0b9d1-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0b9d1-247">AzureRM.Websites</span></span>
* <span data-ttu-id="0b9d1-248">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="0b9d1-249">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0b9d1-250">Généralités</span><span class="sxs-lookup"><span data-stu-id="0b9d1-250">General</span></span>
* <span data-ttu-id="0b9d1-251">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-252">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-253">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="0b9d1-254">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0b9d1-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-255">Azure.Storage</span></span>
* <span data-ttu-id="0b9d1-256">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="0b9d1-257">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0b9d1-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b9d1-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0b9d1-259">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="0b9d1-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="0b9d1-260">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="0b9d1-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="0b9d1-261">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="0b9d1-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="0b9d1-262">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="0b9d1-263">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="0b9d1-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="0b9d1-264">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="0b9d1-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0b9d1-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-265">AzureRM.Compute</span></span>
* <span data-ttu-id="0b9d1-266">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="0b9d1-267">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="0b9d1-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="0b9d1-268">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="0b9d1-269">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="0b9d1-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="0b9d1-270">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="0b9d1-271">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="0b9d1-272">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0b9d1-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="0b9d1-273">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="0b9d1-274">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="0b9d1-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="0b9d1-275">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0b9d1-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b9d1-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0b9d1-277">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="0b9d1-278">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="0b9d1-279">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="0b9d1-280">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0b9d1-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b9d1-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0b9d1-282">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="0b9d1-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0b9d1-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b9d1-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="0b9d1-284">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="0b9d1-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="0b9d1-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-285">AzureRM.Insights</span></span>
* <span data-ttu-id="0b9d1-286">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="0b9d1-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="0b9d1-287">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="0b9d1-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0b9d1-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b9d1-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0b9d1-289">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b9d1-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0b9d1-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0b9d1-290">AzureRM.Network</span></span>
* <span data-ttu-id="0b9d1-291">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0b9d1-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0b9d1-292">AzureRM.Resources</span></span>
* <span data-ttu-id="0b9d1-293">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="0b9d1-294">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0b9d1-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b9d1-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0b9d1-296">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="0b9d1-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="0b9d1-297">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="0b9d1-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="0b9d1-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-298">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-299">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="0b9d1-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0b9d1-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0b9d1-301">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="0b9d1-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="0b9d1-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="0b9d1-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="0b9d1-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="0b9d1-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="0b9d1-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="0b9d1-305">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0b9d1-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="0b9d1-306">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="0b9d1-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="0b9d1-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-307">AzureRM.Storage</span></span>
* <span data-ttu-id="0b9d1-308">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b9d1-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="0b9d1-309">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="0b9d1-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="0b9d1-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b9d1-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="0b9d1-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b9d1-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="0b9d1-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b9d1-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="0b9d1-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="0b9d1-313">AzureRM.Tags</span></span>
* <span data-ttu-id="0b9d1-314">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="0b9d1-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="0b9d1-315">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-316">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-317">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0b9d1-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-318">Azure.Storage</span></span>
* <span data-ttu-id="0b9d1-319">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="0b9d1-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="0b9d1-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0b9d1-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="0b9d1-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0b9d1-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0b9d1-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b9d1-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0b9d1-323">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="0b9d1-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="0b9d1-324">AzureRM.Automation</span></span>
* <span data-ttu-id="0b9d1-325">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0b9d1-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-326">AzureRM.Compute</span></span>
* <span data-ttu-id="0b9d1-327">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b9d1-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="0b9d1-328">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="0b9d1-329">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="0b9d1-330">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="0b9d1-331">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0b9d1-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b9d1-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="0b9d1-333">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="0b9d1-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0b9d1-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b9d1-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0b9d1-335">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b9d1-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="0b9d1-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0b9d1-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="0b9d1-337">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0b9d1-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0b9d1-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0b9d1-338">AzureRM.Network</span></span>
* <span data-ttu-id="0b9d1-339">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0b9d1-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="0b9d1-340">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0b9d1-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="0b9d1-341">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="0b9d1-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="0b9d1-342">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="0b9d1-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="0b9d1-343">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="0b9d1-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="0b9d1-344">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="0b9d1-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="0b9d1-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="0b9d1-345">AzureRM.Relay</span></span>
* <span data-ttu-id="0b9d1-346">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="0b9d1-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0b9d1-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0b9d1-347">AzureRM.Resources</span></span>
* <span data-ttu-id="0b9d1-348">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="0b9d1-349">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="0b9d1-350">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="0b9d1-351">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="0b9d1-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="0b9d1-352">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="0b9d1-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="0b9d1-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b9d1-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0b9d1-354">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="0b9d1-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="0b9d1-355">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="0b9d1-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0b9d1-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0b9d1-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0b9d1-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="0b9d1-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="0b9d1-361">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="0b9d1-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0b9d1-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b9d1-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0b9d1-363">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0b9d1-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-364">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-365">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="0b9d1-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="0b9d1-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0b9d1-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="0b9d1-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="0b9d1-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0b9d1-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0b9d1-368">AzureRM.Websites</span></span>
* <span data-ttu-id="0b9d1-369">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="0b9d1-370">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="0b9d1-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="0b9d1-371">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="0b9d1-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="0b9d1-372">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0b9d1-373">Généralités</span><span class="sxs-lookup"><span data-stu-id="0b9d1-373">General</span></span>
* <span data-ttu-id="0b9d1-374">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="0b9d1-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-375">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-376">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="0b9d1-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0b9d1-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-377">AzureRM.Compute</span></span>
* <span data-ttu-id="0b9d1-378">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="0b9d1-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="0b9d1-379">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="0b9d1-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="0b9d1-380">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="0b9d1-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="0b9d1-381">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="0b9d1-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="0b9d1-382">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="0b9d1-383">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="0b9d1-384">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="0b9d1-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0b9d1-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="0b9d1-386">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="0b9d1-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b9d1-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="0b9d1-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b9d1-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="0b9d1-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b9d1-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0b9d1-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b9d1-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0b9d1-391">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="0b9d1-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="0b9d1-392">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0b9d1-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0b9d1-393">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="0b9d1-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="0b9d1-394">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="0b9d1-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="0b9d1-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="0b9d1-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="0b9d1-396">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="0b9d1-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="0b9d1-397">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="0b9d1-398">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="0b9d1-399">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0b9d1-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b9d1-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0b9d1-401">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="0b9d1-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="0b9d1-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0b9d1-402">AzureRM.Network</span></span>
* <span data-ttu-id="0b9d1-403">Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone</span><span class="sxs-lookup"><span data-stu-id="0b9d1-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="0b9d1-404">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="0b9d1-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="0b9d1-405">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0b9d1-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="0b9d1-406">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0b9d1-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="0b9d1-407">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0b9d1-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0b9d1-408">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0b9d1-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0b9d1-409">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0b9d1-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="0b9d1-410">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0b9d1-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0b9d1-411">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b9d1-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0b9d1-412">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0b9d1-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0b9d1-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0b9d1-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0b9d1-414">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="0b9d1-415">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="0b9d1-416">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0b9d1-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0b9d1-417">AzureRM.Resources</span></span>
* <span data-ttu-id="0b9d1-418">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="0b9d1-419">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="0b9d1-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="0b9d1-420">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="0b9d1-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="0b9d1-421">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="0b9d1-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="0b9d1-422">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0b9d1-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="0b9d1-423">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="0b9d1-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="0b9d1-424">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="0b9d1-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="0b9d1-425">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="0b9d1-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="0b9d1-426">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="0b9d1-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="0b9d1-427">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="0b9d1-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="0b9d1-428">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="0b9d1-429">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0b9d1-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="0b9d1-430">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="0b9d1-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="0b9d1-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0b9d1-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="0b9d1-432">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0b9d1-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-433">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-434">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="0b9d1-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="0b9d1-435">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="0b9d1-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="0b9d1-436">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-437">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-438">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="0b9d1-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="0b9d1-439">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="0b9d1-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="0b9d1-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-440">Azure.Storage</span></span>
* <span data-ttu-id="0b9d1-441">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0b9d1-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-442">AzureRM.Compute</span></span>
* <span data-ttu-id="0b9d1-443">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="0b9d1-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="0b9d1-444">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="0b9d1-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="0b9d1-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0b9d1-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="0b9d1-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0b9d1-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="0b9d1-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="0b9d1-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="0b9d1-448">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="0b9d1-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0b9d1-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="0b9d1-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0b9d1-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="0b9d1-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0b9d1-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="0b9d1-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0b9d1-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="0b9d1-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="0b9d1-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="0b9d1-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="0b9d1-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="0b9d1-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="0b9d1-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="0b9d1-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="0b9d1-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="0b9d1-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="0b9d1-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="0b9d1-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0b9d1-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="0b9d1-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="0b9d1-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="0b9d1-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="0b9d1-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="0b9d1-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="0b9d1-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="0b9d1-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0b9d1-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="0b9d1-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0b9d1-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="0b9d1-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="0b9d1-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="0b9d1-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0b9d1-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="0b9d1-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0b9d1-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="0b9d1-469">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="0b9d1-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b9d1-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0b9d1-471">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="0b9d1-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="0b9d1-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="0b9d1-473">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="0b9d1-474">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="0b9d1-475">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="0b9d1-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="0b9d1-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0b9d1-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0b9d1-477">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="0b9d1-478">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0b9d1-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-479">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-480">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="0b9d1-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0b9d1-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0b9d1-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0b9d1-482">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0b9d1-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0b9d1-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0b9d1-483">AzureRM.Websites</span></span>
* <span data-ttu-id="0b9d1-484">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0b9d1-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="0b9d1-485">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0b9d1-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="0b9d1-486">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="0b9d1-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="0b9d1-488">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="0b9d1-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="0b9d1-489">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-490">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-491">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="0b9d1-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="0b9d1-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="0b9d1-492">AzureRM.Compute</span></span>
* <span data-ttu-id="0b9d1-493">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="0b9d1-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="0b9d1-494">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="0b9d1-495">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0b9d1-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="0b9d1-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b9d1-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="0b9d1-497">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="0b9d1-498">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="0b9d1-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="0b9d1-499">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="0b9d1-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="0b9d1-500">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="0b9d1-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="0b9d1-501">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="0b9d1-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="0b9d1-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0b9d1-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="0b9d1-503">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="0b9d1-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="0b9d1-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0b9d1-504">AzureRM.Network</span></span>
* <span data-ttu-id="0b9d1-505">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="0b9d1-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="0b9d1-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="0b9d1-506">AzureRM.Resources</span></span>
* <span data-ttu-id="0b9d1-507">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="0b9d1-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="0b9d1-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="0b9d1-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="0b9d1-509">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="0b9d1-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="0b9d1-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-510">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-511">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="0b9d1-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="0b9d1-512">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b9d1-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0b9d1-513">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b9d1-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0b9d1-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0b9d1-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0b9d1-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0b9d1-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0b9d1-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b9d1-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="0b9d1-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="0b9d1-517">AzureRM.Websites</span></span>
* <span data-ttu-id="0b9d1-518">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="0b9d1-519">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="0b9d1-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0b9d1-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0b9d1-520">AzureRM.Profile</span></span>
* <span data-ttu-id="0b9d1-521">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="0b9d1-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0b9d1-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0b9d1-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0b9d1-523">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="0b9d1-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0b9d1-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0b9d1-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0b9d1-525">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="0b9d1-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="0b9d1-526">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b9d1-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="0b9d1-527">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="0b9d1-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="0b9d1-528">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="0b9d1-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="0b9d1-529">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="0b9d1-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="0b9d1-530">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="0b9d1-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="0b9d1-531">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="0b9d1-531">Added support for MSI identity</span></span>
* <span data-ttu-id="0b9d1-532">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="0b9d1-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0b9d1-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="0b9d1-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="0b9d1-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0b9d1-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="0b9d1-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0b9d1-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="0b9d1-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0b9d1-537">AzureRM.Batch</span></span>
* <span data-ttu-id="0b9d1-538">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="0b9d1-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="0b9d1-539">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="0b9d1-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="0b9d1-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0b9d1-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="0b9d1-541">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="0b9d1-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0b9d1-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0b9d1-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0b9d1-543">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0b9d1-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0b9d1-544">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b9d1-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="0b9d1-545">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0b9d1-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="0b9d1-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0b9d1-546">AzureRM.Network</span></span>
* <span data-ttu-id="0b9d1-547">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="0b9d1-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="0b9d1-548">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="0b9d1-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b9d1-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="0b9d1-550">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="0b9d1-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b9d1-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0b9d1-552">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="0b9d1-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b9d1-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0b9d1-554">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="0b9d1-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0b9d1-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0b9d1-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0b9d1-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0b9d1-557">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="0b9d1-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0b9d1-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0b9d1-558">AzureRM.Sql</span></span>
* <span data-ttu-id="0b9d1-559">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="0b9d1-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="0b9d1-560">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="0b9d1-561">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="0b9d1-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="0b9d1-562">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="0b9d1-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="0b9d1-563">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="0b9d1-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="0b9d1-564">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b9d1-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0b9d1-565">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b9d1-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0b9d1-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0b9d1-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0b9d1-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0b9d1-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0b9d1-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0b9d1-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0b9d1-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0b9d1-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0b9d1-570">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="0b9d1-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
