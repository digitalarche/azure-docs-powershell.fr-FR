---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383836"
---
# <a name="release-notes"></a><span data-ttu-id="278b4-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="278b4-103">Release notes</span></span>

<span data-ttu-id="278b4-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="278b4-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="278b4-105">6.8.1 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="278b4-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="278b4-106">General</span></span>
* <span data-ttu-id="278b4-107">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="278b4-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="278b4-108">Mise à jour des assemblys de runtime courants</span><span class="sxs-lookup"><span data-stu-id="278b4-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="278b4-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="278b4-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="278b4-110">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="278b4-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="278b4-111">Problème résolu https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="278b4-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="278b4-112">Les cmdlets Import-AzureRmApiManagementApi et \*-AzureRmApiManagementCertificate peuvent maintenant gérer les chemins d’accès relatifs</span><span class="sxs-lookup"><span data-stu-id="278b4-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="278b4-113">Problème résolu https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="278b4-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="278b4-114">CertificateInformation est une propriété définissable permettant à la cmdlet Set-AzureRmApiManagement de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="278b4-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="278b4-115">Résolu en passant au nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="278b4-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="278b4-116">Problème résolu https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="278b4-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="278b4-117">Recherche par nom sur produit du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="278b4-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="278b4-118">Problème résolu https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="278b4-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="278b4-119">Recherche par nom sur Api du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="278b4-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="278b4-120">Ajout de la prise en charge de l’enregistreur d'événements AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="278b4-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="278b4-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-121">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-122">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="278b4-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="278b4-123">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="278b4-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="278b4-124">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="278b4-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="278b4-125">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="278b4-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-126">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-127">Modification de la présentation d’une sortie de cmdlet par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="278b4-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="278b4-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="278b4-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="278b4-129">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="278b4-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="278b4-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-130">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-131">Résolution du problème de création d’applications managées depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="278b4-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="278b4-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="278b4-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="278b4-133">Problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="278b4-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="278b4-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="278b4-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="278b4-135">Ajout de la prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="278b4-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="278b4-136">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="278b4-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="278b4-137">Ajout de la prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="278b4-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="278b4-138">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="278b4-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="278b4-139">Ajout de la prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="278b4-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="278b4-140">Ajout de la prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="278b4-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="278b4-141">Ajout de la prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="278b4-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="278b4-142">6.8.0 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="278b4-143">Généralités</span><span class="sxs-lookup"><span data-stu-id="278b4-143">General</span></span>
* <span data-ttu-id="278b4-144">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="278b4-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="278b4-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-145">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-146">Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="278b4-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-147">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-148">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="278b4-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="278b4-149">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="278b4-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="278b4-150">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="278b4-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="278b4-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="278b4-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="278b4-152">Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="278b4-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-153">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-154">Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="278b4-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="278b4-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="278b4-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="278b4-156">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="278b4-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="278b4-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-157">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-158">Résolution du problème de création d’application managée depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="278b4-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="278b4-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="278b4-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="278b4-160">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="278b4-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="278b4-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="278b4-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="278b4-162">Prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="278b4-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="278b4-163">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="278b4-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="278b4-164">Prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="278b4-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="278b4-165">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="278b4-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="278b4-166">Prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="278b4-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="278b4-167">Prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="278b4-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="278b4-168">Prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="278b4-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="278b4-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="278b4-169">AzureRM.Websites</span></span>
* <span data-ttu-id="278b4-170">Résolution du problème relatif aux groupes de ressources par défaut mal définis.</span><span class="sxs-lookup"><span data-stu-id="278b4-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="278b4-171">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="278b4-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-172">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-173">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="278b4-174">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="278b4-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="278b4-175">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="278b4-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="278b4-176">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="278b4-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="278b4-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-177">Azure.Storage</span></span>
* <span data-ttu-id="278b4-178">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="278b4-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="278b4-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="278b4-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="278b4-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="278b4-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="278b4-181">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="278b4-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="278b4-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="278b4-183">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="278b4-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="278b4-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="278b4-185">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="278b4-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="278b4-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="278b4-187">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="278b4-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="278b4-188">AzureRM.Automation</span></span>
* <span data-ttu-id="278b4-189">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="278b4-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="278b4-190">AzureRM.Backup</span></span>
* <span data-ttu-id="278b4-191">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="278b4-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="278b4-192">AzureRM.Batch</span></span>
* <span data-ttu-id="278b4-193">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="278b4-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="278b4-194">AzureRM.Billing</span></span>
* <span data-ttu-id="278b4-195">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="278b4-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="278b4-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="278b4-197">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="278b4-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="278b4-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="278b4-199">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-200">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-201">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="278b4-202">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="278b4-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="278b4-203">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="278b4-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="278b4-204">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="278b4-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="278b4-205">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="278b4-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="278b4-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="278b4-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="278b4-207">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="278b4-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="278b4-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="278b4-209">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="278b4-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="278b4-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="278b4-211">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="278b4-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="278b4-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="278b4-213">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="278b4-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="278b4-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="278b4-215">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="278b4-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="278b4-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="278b4-217">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="278b4-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="278b4-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="278b4-219">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="278b4-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="278b4-220">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="278b4-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="278b4-221">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="278b4-222">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="278b4-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="278b4-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="278b4-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="278b4-224">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="278b4-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="278b4-225">AzureRM.Dns</span></span>
* <span data-ttu-id="278b4-226">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="278b4-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="278b4-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="278b4-228">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="278b4-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="278b4-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="278b4-230">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="278b4-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="278b4-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="278b4-232">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="278b4-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="278b4-233">AzureRM.Insights</span></span>
* <span data-ttu-id="278b4-234">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="278b4-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="278b4-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="278b4-236">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="278b4-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="278b4-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="278b4-238">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="278b4-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="278b4-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="278b4-240">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="278b4-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="278b4-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="278b4-242">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="278b4-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="278b4-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="278b4-244">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="278b4-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="278b4-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="278b4-246">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="278b4-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="278b4-247">AzureRM.Media</span></span>
* <span data-ttu-id="278b4-248">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-249">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-250">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="278b4-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="278b4-251">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="278b4-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="278b4-252">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="278b4-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="278b4-253">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="278b4-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="278b4-254">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="278b4-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="278b4-255">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="278b4-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="278b4-256">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="278b4-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="278b4-257">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="278b4-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="278b4-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="278b4-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="278b4-259">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="278b4-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="278b4-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="278b4-261">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="278b4-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="278b4-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="278b4-263">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="278b4-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="278b4-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="278b4-265">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="278b4-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="278b4-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="278b4-267">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="278b4-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="278b4-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="278b4-269">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="278b4-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="278b4-270">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="278b4-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="278b4-271">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="278b4-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="278b4-272">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="278b4-273">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="278b4-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="278b4-274">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="278b4-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="278b4-275">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="278b4-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="278b4-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="278b4-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="278b4-277">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="278b4-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="278b4-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="278b4-279">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="278b4-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="278b4-280">AzureRM.Relay</span></span>
* <span data-ttu-id="278b4-281">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="278b4-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-282">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-283">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="278b4-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="278b4-284">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="278b4-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="278b4-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="278b4-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="278b4-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="278b4-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="278b4-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="278b4-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="278b4-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="278b4-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="278b4-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="278b4-292">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="278b4-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="278b4-293">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="278b4-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="278b4-294">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="278b4-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="278b4-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="278b4-296">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="278b4-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="278b4-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="278b4-298">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="278b4-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="278b4-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="278b4-300">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="278b4-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-301">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-302">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="278b4-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-303">AzureRM.Storage</span></span>
* <span data-ttu-id="278b4-304">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="278b4-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="278b4-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="278b4-306">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="278b4-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="278b4-307">AzureRM.Tags</span></span>
* <span data-ttu-id="278b4-308">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="278b4-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="278b4-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="278b4-310">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="278b4-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="278b4-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="278b4-312">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="278b4-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="278b4-313">AzureRM.Websites</span></span>
* <span data-ttu-id="278b4-314">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="278b4-315">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="278b4-316">Généralités</span><span class="sxs-lookup"><span data-stu-id="278b4-316">General</span></span>
* <span data-ttu-id="278b4-317">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="278b4-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="278b4-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-318">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-319">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="278b4-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="278b4-320">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="278b4-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-321">Azure.Storage</span></span>
* <span data-ttu-id="278b4-322">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="278b4-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="278b4-323">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="278b4-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="278b4-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="278b4-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="278b4-325">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="278b4-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="278b4-326">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="278b4-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="278b4-327">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="278b4-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="278b4-328">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="278b4-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="278b4-329">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="278b4-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="278b4-330">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="278b4-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-331">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-332">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="278b4-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="278b4-333">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="278b4-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="278b4-334">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="278b4-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="278b4-335">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="278b4-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="278b4-336">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="278b4-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="278b4-337">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="278b4-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="278b4-338">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="278b4-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="278b4-339">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="278b4-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="278b4-340">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="278b4-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="278b4-341">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="278b4-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="278b4-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="278b4-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="278b4-343">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="278b4-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="278b4-344">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="278b4-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="278b4-345">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="278b4-346">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="278b4-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="278b4-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="278b4-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="278b4-348">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="278b4-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="278b4-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="278b4-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="278b4-350">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="278b4-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="278b4-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="278b4-351">AzureRM.Insights</span></span>
* <span data-ttu-id="278b4-352">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="278b4-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="278b4-353">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="278b4-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="278b4-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="278b4-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="278b4-355">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="278b4-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-356">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-357">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="278b4-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="278b4-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-358">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-359">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="278b4-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="278b4-360">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="278b4-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="278b4-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="278b4-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="278b4-362">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="278b4-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="278b4-363">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="278b4-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="278b4-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-364">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-365">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="278b4-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="278b4-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="278b4-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="278b4-367">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="278b4-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="278b4-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="278b4-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="278b4-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="278b4-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="278b4-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="278b4-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="278b4-371">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="278b4-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="278b4-372">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="278b4-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="278b4-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-373">AzureRM.Storage</span></span>
* <span data-ttu-id="278b4-374">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="278b4-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="278b4-375">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="278b4-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="278b4-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="278b4-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="278b4-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="278b4-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="278b4-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="278b4-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="278b4-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="278b4-379">AzureRM.Tags</span></span>
* <span data-ttu-id="278b4-380">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="278b4-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="278b4-381">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="278b4-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-382">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-383">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="278b4-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="278b4-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-384">Azure.Storage</span></span>
* <span data-ttu-id="278b4-385">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="278b4-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="278b4-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="278b4-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="278b4-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="278b4-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="278b4-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="278b4-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="278b4-389">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="278b4-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="278b4-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="278b4-390">AzureRM.Automation</span></span>
* <span data-ttu-id="278b4-391">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="278b4-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-392">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-393">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="278b4-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="278b4-394">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="278b4-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="278b4-395">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="278b4-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="278b4-396">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="278b4-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="278b4-397">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="278b4-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="278b4-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="278b4-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="278b4-399">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="278b4-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="278b4-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="278b4-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="278b4-401">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="278b4-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="278b4-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="278b4-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="278b4-403">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="278b4-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-404">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-405">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="278b4-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="278b4-406">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="278b4-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="278b4-407">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="278b4-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="278b4-408">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="278b4-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="278b4-409">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="278b4-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="278b4-410">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="278b4-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="278b4-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="278b4-411">AzureRM.Relay</span></span>
* <span data-ttu-id="278b4-412">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="278b4-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="278b4-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-413">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-414">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="278b4-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="278b4-415">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="278b4-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="278b4-416">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="278b4-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="278b4-417">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="278b4-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="278b4-418">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="278b4-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="278b4-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="278b4-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="278b4-420">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="278b4-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="278b4-421">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="278b4-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="278b4-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="278b4-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="278b4-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="278b4-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="278b4-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="278b4-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="278b4-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="278b4-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="278b4-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="278b4-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="278b4-427">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="278b4-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="278b4-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="278b4-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="278b4-429">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="278b4-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="278b4-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-430">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-431">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="278b4-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="278b4-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="278b4-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="278b4-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="278b4-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="278b4-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="278b4-434">AzureRM.Websites</span></span>
* <span data-ttu-id="278b4-435">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="278b4-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="278b4-436">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="278b4-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="278b4-437">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="278b4-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="278b4-438">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="278b4-439">Généralités</span><span class="sxs-lookup"><span data-stu-id="278b4-439">General</span></span>
* <span data-ttu-id="278b4-440">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="278b4-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="278b4-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-441">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-442">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="278b4-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-443">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-444">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="278b4-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="278b4-445">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="278b4-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="278b4-446">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="278b4-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="278b4-447">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="278b4-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="278b4-448">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="278b4-449">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="278b4-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="278b4-450">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="278b4-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="278b4-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="278b4-452">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="278b4-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="278b4-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="278b4-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="278b4-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="278b4-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="278b4-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="278b4-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="278b4-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="278b4-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="278b4-457">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="278b4-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="278b4-458">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="278b4-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="278b4-459">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="278b4-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="278b4-460">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="278b4-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="278b4-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="278b4-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="278b4-462">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="278b4-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="278b4-463">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="278b4-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="278b4-464">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="278b4-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="278b4-465">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="278b4-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="278b4-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="278b4-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="278b4-467">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="278b4-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-468">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-469">Exposer les nouvelles références SKU pour Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="278b4-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="278b4-470">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="278b4-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="278b4-471">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="278b4-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="278b4-472">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="278b4-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="278b4-473">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="278b4-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="278b4-474">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="278b4-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="278b4-475">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="278b4-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="278b4-476">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="278b4-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="278b4-477">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="278b4-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="278b4-478">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="278b4-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="278b4-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="278b4-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="278b4-480">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="278b4-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="278b4-481">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="278b4-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="278b4-482">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="278b4-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="278b4-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-483">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-484">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="278b4-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="278b4-485">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="278b4-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="278b4-486">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="278b4-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="278b4-487">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="278b4-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="278b4-488">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="278b4-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="278b4-489">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="278b4-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="278b4-490">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="278b4-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="278b4-491">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="278b4-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="278b4-492">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="278b4-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="278b4-493">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="278b4-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="278b4-494">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="278b4-495">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="278b4-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="278b4-496">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="278b4-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="278b4-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="278b4-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="278b4-498">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="278b4-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="278b4-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-499">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-500">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="278b4-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="278b4-501">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="278b4-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="278b4-502">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="278b4-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-503">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-504">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="278b4-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="278b4-505">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="278b4-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="278b4-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="278b4-506">Azure.Storage</span></span>
* <span data-ttu-id="278b4-507">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="278b4-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-508">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-509">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="278b4-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="278b4-510">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="278b4-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="278b4-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="278b4-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="278b4-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="278b4-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="278b4-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="278b4-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="278b4-514">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="278b4-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="278b4-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="278b4-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="278b4-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="278b4-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="278b4-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="278b4-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="278b4-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="278b4-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="278b4-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="278b4-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="278b4-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="278b4-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="278b4-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="278b4-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="278b4-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="278b4-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="278b4-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="278b4-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="278b4-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="278b4-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="278b4-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="278b4-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="278b4-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="278b4-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="278b4-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="278b4-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="278b4-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="278b4-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="278b4-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="278b4-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="278b4-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="278b4-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="278b4-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="278b4-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="278b4-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="278b4-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="278b4-535">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="278b4-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="278b4-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="278b4-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="278b4-537">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="278b4-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="278b4-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="278b4-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="278b4-539">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="278b4-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="278b4-540">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="278b4-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="278b4-541">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="278b4-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="278b4-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="278b4-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="278b4-543">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="278b4-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="278b4-544">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="278b4-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="278b4-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-545">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-546">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="278b4-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="278b4-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="278b4-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="278b4-548">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="278b4-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="278b4-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="278b4-549">AzureRM.Websites</span></span>
* <span data-ttu-id="278b4-550">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="278b4-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="278b4-551">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="278b4-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="278b4-552">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="278b4-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="278b4-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="278b4-554">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="278b4-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="278b4-555">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="278b4-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-556">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-557">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="278b4-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="278b4-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="278b4-558">AzureRM.Compute</span></span>
* <span data-ttu-id="278b4-559">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="278b4-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="278b4-560">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="278b4-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="278b4-561">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="278b4-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="278b4-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="278b4-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="278b4-563">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="278b4-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="278b4-564">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="278b4-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="278b4-565">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="278b4-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="278b4-566">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="278b4-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="278b4-567">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="278b4-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="278b4-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="278b4-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="278b4-569">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="278b4-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="278b4-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-570">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-571">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="278b4-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="278b4-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="278b4-572">AzureRM.Resources</span></span>
* <span data-ttu-id="278b4-573">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="278b4-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="278b4-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="278b4-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="278b4-575">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="278b4-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="278b4-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-576">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-577">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="278b4-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="278b4-578">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="278b4-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="278b4-579">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="278b4-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="278b4-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="278b4-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="278b4-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="278b4-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="278b4-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="278b4-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="278b4-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="278b4-583">AzureRM.Websites</span></span>
* <span data-ttu-id="278b4-584">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="278b4-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="278b4-585">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="278b4-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="278b4-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="278b4-586">AzureRM.Profile</span></span>
* <span data-ttu-id="278b4-587">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="278b4-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="278b4-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="278b4-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="278b4-589">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="278b4-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="278b4-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="278b4-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="278b4-591">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="278b4-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="278b4-592">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="278b4-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="278b4-593">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="278b4-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="278b4-594">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="278b4-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="278b4-595">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="278b4-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="278b4-596">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="278b4-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="278b4-597">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="278b4-597">Added support for MSI identity</span></span>
* <span data-ttu-id="278b4-598">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="278b4-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="278b4-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="278b4-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="278b4-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="278b4-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="278b4-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="278b4-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="278b4-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="278b4-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="278b4-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="278b4-603">AzureRM.Batch</span></span>
* <span data-ttu-id="278b4-604">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="278b4-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="278b4-605">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="278b4-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="278b4-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="278b4-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="278b4-607">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="278b4-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="278b4-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="278b4-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="278b4-609">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="278b4-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="278b4-610">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="278b4-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="278b4-611">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="278b4-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="278b4-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="278b4-612">AzureRM.Network</span></span>
* <span data-ttu-id="278b4-613">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="278b4-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="278b4-614">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="278b4-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="278b4-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="278b4-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="278b4-616">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="278b4-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="278b4-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="278b4-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="278b4-618">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="278b4-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="278b4-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="278b4-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="278b4-620">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="278b4-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="278b4-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="278b4-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="278b4-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="278b4-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="278b4-623">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="278b4-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="278b4-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="278b4-624">AzureRM.Sql</span></span>
* <span data-ttu-id="278b4-625">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="278b4-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="278b4-626">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="278b4-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="278b4-627">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="278b4-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="278b4-628">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="278b4-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="278b4-629">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="278b4-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="278b4-630">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="278b4-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="278b4-631">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="278b4-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="278b4-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="278b4-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="278b4-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="278b4-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="278b4-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="278b4-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="278b4-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="278b4-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="278b4-636">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="278b4-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
