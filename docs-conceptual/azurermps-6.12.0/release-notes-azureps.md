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
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574530"
---
# <a name="release-notes"></a><span data-ttu-id="31fbd-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="31fbd-103">Release notes</span></span>

<span data-ttu-id="31fbd-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="31fbd-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="31fbd-105">6.12.0 - novembre 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-106">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-107">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="31fbd-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="31fbd-108">Changement de nom du param TenantId dans la cmdlet Connect-AzureRmAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="31fbd-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="31fbd-109">Mise à jour de la description TenantId pour Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="31fbd-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="31fbd-110">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="31fbd-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="31fbd-111">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="31fbd-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="31fbd-112">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="31fbd-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="31fbd-113">Correction du problème de levée de « Disconnect-AzureRmAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="31fbd-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="31fbd-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="31fbd-114">AzureRM.Automation</span></span>
* <span data-ttu-id="31fbd-115">Changement du nom du fichier DLL de la cmdlet en Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="31fbd-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="31fbd-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="31fbd-117">Ajout de l’opération Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="31fbd-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-118">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-119">Ajout des cmdlets Add-AzureRmVmssVMDataDisk et Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="31fbd-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="31fbd-120">Get-AzureRmVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="31fbd-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="31fbd-121">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzureRmVMChefExtension qui ne sont pas définies au format json.</span><span class="sxs-lookup"><span data-stu-id="31fbd-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="31fbd-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31fbd-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="31fbd-123">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="31fbd-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="31fbd-124">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="31fbd-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="31fbd-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="31fbd-125">AzureRM.Insights</span></span>
* <span data-ttu-id="31fbd-126">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="31fbd-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="31fbd-127">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="31fbd-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="31fbd-128">Correction du problème #7513 [Insights], les catégories de Set-AzureRMDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="31fbd-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="31fbd-129">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="31fbd-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-130">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-131">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="31fbd-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="31fbd-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="31fbd-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="31fbd-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="31fbd-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="31fbd-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31fbd-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="31fbd-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="31fbd-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="31fbd-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="31fbd-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="31fbd-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31fbd-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="31fbd-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31fbd-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="31fbd-139">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="31fbd-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="31fbd-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31fbd-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31fbd-141">Ajout de la prise en charge des partages de fichiers Azure partages dans Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="31fbd-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-142">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-143">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="31fbd-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="31fbd-144">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="31fbd-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-146">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="31fbd-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="31fbd-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31fbd-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="31fbd-148">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="31fbd-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="31fbd-149">Correction de « Add-AzureRmServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="31fbd-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="31fbd-150">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="31fbd-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="31fbd-151">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="31fbd-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="31fbd-152">Correction de « Update-AzureRmServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="31fbd-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="31fbd-153">6.11.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-154">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-155">Problème résolu avec Get-AzureRmSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="31fbd-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="31fbd-156">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="31fbd-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="31fbd-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="31fbd-157">AzureRM.Backup</span></span>
* <span data-ttu-id="31fbd-158">Applets de commande Sauvegarde Azure déconseillés.</span><span class="sxs-lookup"><span data-stu-id="31fbd-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-159">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-160">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation de l’ensemble de paramètres simple pour « New-AzureRmVm »</span><span class="sxs-lookup"><span data-stu-id="31fbd-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="31fbd-161">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="31fbd-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="31fbd-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31fbd-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="31fbd-163">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="31fbd-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="31fbd-164">Get-AzureRmDataLakeStoreVirtualNetworkRule : obtient ou liste la règle de réseau virtuel d’Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31fbd-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="31fbd-165">Add-AzureRmDataLakeStoreVirtualNetworkRule : ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="31fbd-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31fbd-166">Set-AzureRmDataLakeStoreVirtualNetworkRule : modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="31fbd-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="31fbd-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule : supprime une règle de réseau virtuel d’Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31fbd-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-168">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-169">Mise à jour de l’applet de commande Test-AzureRmNetworkWatcherConnectivity, passage de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="31fbd-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="31fbd-170">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="31fbd-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-171">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-172">Résout les problèmes où Get-AzureRMRoleDefinition lève une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="31fbd-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="31fbd-173">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="31fbd-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="31fbd-174">6.10.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="31fbd-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-175">Azure.Storage</span></span>
* <span data-ttu-id="31fbd-176">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="31fbd-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="31fbd-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="31fbd-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="31fbd-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="31fbd-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="31fbd-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="31fbd-180">Prise en charge de Get-AzureRmCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="31fbd-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-181">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-182">Correction de Get-AzureRmVM -ResourceGroupName <rg> pour retourner plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="31fbd-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="31fbd-183">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="31fbd-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="31fbd-184">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="31fbd-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="31fbd-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31fbd-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="31fbd-186">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="31fbd-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-187">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-188">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="31fbd-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="31fbd-189">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="31fbd-189">new cmdlets added</span></span>
    - <span data-ttu-id="31fbd-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31fbd-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="31fbd-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31fbd-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="31fbd-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31fbd-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="31fbd-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="31fbd-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="31fbd-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="31fbd-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="31fbd-196">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="31fbd-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="31fbd-197">Ajout des cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="31fbd-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="31fbd-198">Ajout des cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="31fbd-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31fbd-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="31fbd-200">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="31fbd-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="31fbd-201">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="31fbd-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-202">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-203">Ajout du paramètre manquant -Mode à Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31fbd-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="31fbd-204">Correction d’un bug de la cmdlet Get-AzureRmProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="31fbd-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-205">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-206">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="31fbd-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="31fbd-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-207">AzureRM.Storage</span></span>
* <span data-ttu-id="31fbd-208">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="31fbd-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="31fbd-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="31fbd-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-210">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-211">Nouvelle cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="31fbd-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="31fbd-212">Nouvelles cmdlets New-AzureRMWebAppContainerPSSession et Enter-WebAppContainerPSSession - démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="31fbd-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="31fbd-213">6.9.0 - septembre 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31fbd-214">Généralités</span><span class="sxs-lookup"><span data-stu-id="31fbd-214">General</span></span>
* <span data-ttu-id="31fbd-215">AzureRM.SignalR a été ajouté au module Rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="31fbd-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-216">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-217">Modifications mineures du code commun de stockage</span><span class="sxs-lookup"><span data-stu-id="31fbd-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="31fbd-218">Mise à jour des fichiers d’aide pour inclure des types de paramètre complet.</span><span class="sxs-lookup"><span data-stu-id="31fbd-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="31fbd-219">Modification de -ServicePrincipal en non obligatoire dans l’ensemble de paramètres ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31fbd-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="31fbd-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-220">Azure.Storage</span></span>
* <span data-ttu-id="31fbd-221">Prise en charge du contexte de stockage avec OAuth.</span><span class="sxs-lookup"><span data-stu-id="31fbd-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="31fbd-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="31fbd-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="31fbd-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="31fbd-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="31fbd-224">Ajout de Standard_Microsoft dans la référence SKU de tarification d’un CDN.</span><span class="sxs-lookup"><span data-stu-id="31fbd-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-225">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-226">Déplacement des dépendances du coffre de clés et du stockage vers les dépendances communes</span><span class="sxs-lookup"><span data-stu-id="31fbd-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="31fbd-227">Ajout de la prise en charge de plus de tailles de machine virtuelle aux cmdlets AEM</span><span class="sxs-lookup"><span data-stu-id="31fbd-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="31fbd-228">Ajout du paramètre PublicIPPrefix à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="31fbd-229">Ajout du paramètre ResourceId à la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="31fbd-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="31fbd-230">Ajout de la cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="31fbd-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="31fbd-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="31fbd-231">AzureRM.Dns</span></span>
* <span data-ttu-id="31fbd-232">Prise en charge de l’enregistrement d’alias pendant la création d’enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="31fbd-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="31fbd-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="31fbd-233">AzureRM.Insights</span></span>
* <span data-ttu-id="31fbd-234">Résolution des problèmes #6833 et #7102 (zone Paramètres de diagnostic)</span><span class="sxs-lookup"><span data-stu-id="31fbd-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="31fbd-235">Problèmes avec un nom par défaut, par exemple « service », lors de la création et l’obtention/le référencement des paramètres de diagnostic</span><span class="sxs-lookup"><span data-stu-id="31fbd-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="31fbd-236">Problèmes créant des paramètres de diagnostic avec des catégories</span><span class="sxs-lookup"><span data-stu-id="31fbd-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="31fbd-237">Ajout de message de désapprobation pour les paramètres de fragments de temps de métriques</span><span class="sxs-lookup"><span data-stu-id="31fbd-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="31fbd-238">Les paramètres Timegrains sont toujours acceptés (il s’agit d’une modification sans rupture,), mais ils sont ignorés dans le serveur principal dans la mesure où seul PT1M est valide</span><span class="sxs-lookup"><span data-stu-id="31fbd-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-239">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-240">Modifications apportées aux cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31fbd-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="31fbd-241">LoadBalancerInboundNatPoolConfig : ajout des paramètres IdleTimeoutInMinutes, EnableFloatingIp et EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="31fbd-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="31fbd-242">LoadBalancerInboundNatRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="31fbd-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="31fbd-243">LoadBalancerRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="31fbd-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="31fbd-244">LoadBalancerProbeConfig : ajout d’une prise en charge de la valeur « Https » pour le paramètre Protocole</span><span class="sxs-lookup"><span data-stu-id="31fbd-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="31fbd-245">Ajout de nouvelles commandes pour la sous-ressource OutboundRule du nouveau LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="31fbd-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="31fbd-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="31fbd-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="31fbd-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="31fbd-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="31fbd-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="31fbd-251">Ajout d’une nouvelle propriété HostedWorkloads pour PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="31fbd-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="31fbd-252">Ajouté de nouvelles cmdlets pour la fonctionnalité : Pare-feu Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="31fbd-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="31fbd-253">Ajout de Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="31fbd-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="31fbd-254">Ajout de Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="31fbd-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="31fbd-255">Ajout de New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="31fbd-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="31fbd-256">Ajout de Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="31fbd-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="31fbd-257">Ajout de New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="31fbd-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="31fbd-258">Ajout de New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="31fbd-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="31fbd-259">Ajout de New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="31fbd-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="31fbd-260">Ajout de New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="31fbd-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="31fbd-261">Ajout de New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="31fbd-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="31fbd-262">Ajout de New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="31fbd-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="31fbd-263">Ajout de la prise en charge du certificat racine approuvé et de la configuration de mise à l’échelle automatique dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="31fbd-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="31fbd-264">Nouvelles cmdlets ajoutées :</span><span class="sxs-lookup"><span data-stu-id="31fbd-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="31fbd-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="31fbd-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="31fbd-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="31fbd-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="31fbd-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="31fbd-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="31fbd-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="31fbd-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="31fbd-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="31fbd-274">Cmdlets mises à jour avec le paramètre facultatif -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="31fbd-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31fbd-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="31fbd-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31fbd-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="31fbd-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="31fbd-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="31fbd-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="31fbd-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="31fbd-279">Cmdlets mises à jour avec le paramètre facultatif -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="31fbd-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31fbd-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="31fbd-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31fbd-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="31fbd-282">Ajout d’une cmdlet pour le point de terminaison d’interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="31fbd-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="31fbd-283">Ajout de la prise en charge de plusieurs préfixes d’adresse dans un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="31fbd-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="31fbd-284">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="31fbd-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="31fbd-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="31fbd-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="31fbd-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="31fbd-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="31fbd-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="31fbd-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="31fbd-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="31fbd-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="31fbd-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="31fbd-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="31fbd-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="31fbd-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="31fbd-297">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="31fbd-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="31fbd-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="31fbd-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="31fbd-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="31fbd-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="31fbd-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="31fbd-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="31fbd-304">Ajout de cmdlets pour la délégation de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="31fbd-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="31fbd-305">New-AzureRmDelegation : crée une nouvelle délégation, celle-ci peut être ajoutée à un sous-réseau</span><span class="sxs-lookup"><span data-stu-id="31fbd-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="31fbd-306">Remove-AzureRmDelegation : accepte un sous-réseau et supprime le nom de délégation fourni de ce sous-réseau</span><span class="sxs-lookup"><span data-stu-id="31fbd-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="31fbd-307">Add-AzureRmDelegation : accepte un sous-réseau et ajoute le nom de service fourni en tant que délégation à ce sous-réseau</span><span class="sxs-lookup"><span data-stu-id="31fbd-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="31fbd-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="31fbd-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="31fbd-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="31fbd-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="31fbd-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="31fbd-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="31fbd-311">Prise en charge de la gestion de disque managé</span><span class="sxs-lookup"><span data-stu-id="31fbd-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="31fbd-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31fbd-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="31fbd-313">Mise à jour de la dépendance Insights.</span><span class="sxs-lookup"><span data-stu-id="31fbd-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-314">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-315">Mise à jour de New-AzureRmResourceGroupDeployment avec le nouveau paramètre RollbackAction</span><span class="sxs-lookup"><span data-stu-id="31fbd-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="31fbd-316">Ajout de la prise en charge d’OnErrorDeployment avec le nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="31fbd-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="31fbd-317">Prise en charge des identités managées sur les affectations de stratégies.</span><span class="sxs-lookup"><span data-stu-id="31fbd-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="31fbd-318">Des paramètres avec des valeurs par défaut ne sont plus requis lors de l’affectation d’une stratégie avec « New-AzureRmPolicyAssignment »</span><span class="sxs-lookup"><span data-stu-id="31fbd-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="31fbd-319">Ajout de la nouvelle cmdlet Get-AzureRmPolicyAlias pour récupérer les alias de stratégie</span><span class="sxs-lookup"><span data-stu-id="31fbd-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-321">Résolution du problème #7161</span><span class="sxs-lookup"><span data-stu-id="31fbd-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="31fbd-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="31fbd-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="31fbd-323">Mise à jour des noms de référence SKU en Free_F1 et Standard_S1</span><span class="sxs-lookup"><span data-stu-id="31fbd-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="31fbd-324">Ajout d’un champ de version à l’objet PSSignalRResource et d’une chaîne de connexion à l’objet PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="31fbd-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="31fbd-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-325">AzureRM.Storage</span></span>
* <span data-ttu-id="31fbd-326">Prise en charge de la stratégie d’immuabilité dans AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="31fbd-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="31fbd-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="31fbd-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31fbd-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="31fbd-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31fbd-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="31fbd-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31fbd-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="31fbd-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="31fbd-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="31fbd-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="31fbd-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="31fbd-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="31fbd-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="31fbd-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="31fbd-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="31fbd-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="31fbd-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-338">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-339">Ajout de deux nouvelles cmdlets : Get-AzureRmDeletedWebApp et Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="31fbd-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="31fbd-340">New-AzureRmAppServicePlan : le commutateur HyperV est ajouté pour créer un plan App Service avec conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="31fbd-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="31fbd-341">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot : les nouveaux paramètres (la chaîne -ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) ajoutés pour créer et gérer l’application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="31fbd-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="31fbd-342">6.8.1 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31fbd-343">Généralités</span><span class="sxs-lookup"><span data-stu-id="31fbd-343">General</span></span>
* <span data-ttu-id="31fbd-344">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="31fbd-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="31fbd-345">Mise à jour des assemblys de runtime courants</span><span class="sxs-lookup"><span data-stu-id="31fbd-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="31fbd-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31fbd-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="31fbd-347">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="31fbd-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="31fbd-348">Problème résolu https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="31fbd-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="31fbd-349">Les cmdlets Import-AzureRmApiManagementApi et \*-AzureRmApiManagementCertificate peuvent maintenant gérer les chemins d’accès relatifs</span><span class="sxs-lookup"><span data-stu-id="31fbd-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="31fbd-350">Problème résolu https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="31fbd-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="31fbd-351">CertificateInformation est une propriété définissable permettant à la cmdlet Set-AzureRmApiManagement de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="31fbd-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="31fbd-352">Résolu en passant au nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="31fbd-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="31fbd-353">Problème résolu https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="31fbd-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="31fbd-354">Recherche par nom sur produit du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="31fbd-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="31fbd-355">Problème résolu https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="31fbd-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="31fbd-356">Recherche par nom sur Api du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="31fbd-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="31fbd-357">Ajout de la prise en charge de l’enregistreur d'événements AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="31fbd-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-358">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-359">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="31fbd-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="31fbd-360">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="31fbd-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="31fbd-361">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="31fbd-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="31fbd-362">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="31fbd-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-363">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-364">Modification de la présentation d’une sortie de cmdlet par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="31fbd-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="31fbd-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="31fbd-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="31fbd-366">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="31fbd-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="31fbd-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-367">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-368">Résolution du problème de création d’applications managées depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="31fbd-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-370">Problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="31fbd-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="31fbd-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31fbd-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="31fbd-372">Ajout de la prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="31fbd-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="31fbd-373">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="31fbd-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="31fbd-374">Ajout de la prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="31fbd-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="31fbd-375">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="31fbd-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="31fbd-376">Ajout de la prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="31fbd-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="31fbd-377">Ajout de la prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="31fbd-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="31fbd-378">Ajout de la prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="31fbd-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="31fbd-379">6.8.0 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31fbd-380">Généralités</span><span class="sxs-lookup"><span data-stu-id="31fbd-380">General</span></span>
* <span data-ttu-id="31fbd-381">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="31fbd-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-382">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-383">Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="31fbd-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-384">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-385">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="31fbd-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="31fbd-386">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="31fbd-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="31fbd-387">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="31fbd-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="31fbd-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="31fbd-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="31fbd-389">Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="31fbd-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-390">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-391">Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="31fbd-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="31fbd-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="31fbd-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="31fbd-393">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="31fbd-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-394">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-395">Résolution du problème de création d’application managée depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="31fbd-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-397">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="31fbd-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="31fbd-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31fbd-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="31fbd-399">Prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="31fbd-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="31fbd-400">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="31fbd-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="31fbd-401">Prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="31fbd-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="31fbd-402">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="31fbd-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="31fbd-403">Prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="31fbd-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="31fbd-404">Prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="31fbd-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="31fbd-405">Prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="31fbd-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-406">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-407">Résolution du problème relatif aux groupes de ressources par défaut mal définis.</span><span class="sxs-lookup"><span data-stu-id="31fbd-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="31fbd-408">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-409">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-410">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="31fbd-411">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="31fbd-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="31fbd-412">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="31fbd-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="31fbd-413">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="31fbd-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="31fbd-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-414">Azure.Storage</span></span>
* <span data-ttu-id="31fbd-415">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="31fbd-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="31fbd-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="31fbd-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="31fbd-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="31fbd-418">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="31fbd-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="31fbd-420">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="31fbd-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31fbd-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="31fbd-422">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="31fbd-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="31fbd-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="31fbd-424">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="31fbd-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="31fbd-425">AzureRM.Automation</span></span>
* <span data-ttu-id="31fbd-426">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="31fbd-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="31fbd-427">AzureRM.Backup</span></span>
* <span data-ttu-id="31fbd-428">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="31fbd-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="31fbd-429">AzureRM.Batch</span></span>
* <span data-ttu-id="31fbd-430">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="31fbd-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="31fbd-431">AzureRM.Billing</span></span>
* <span data-ttu-id="31fbd-432">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="31fbd-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="31fbd-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="31fbd-434">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="31fbd-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="31fbd-436">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-437">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-438">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="31fbd-439">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="31fbd-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="31fbd-440">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="31fbd-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="31fbd-441">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="31fbd-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="31fbd-442">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="31fbd-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="31fbd-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="31fbd-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="31fbd-444">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="31fbd-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="31fbd-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="31fbd-446">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="31fbd-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="31fbd-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="31fbd-448">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="31fbd-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="31fbd-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="31fbd-450">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="31fbd-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31fbd-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="31fbd-452">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="31fbd-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="31fbd-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="31fbd-454">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="31fbd-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31fbd-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="31fbd-456">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31fbd-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="31fbd-457">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="31fbd-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="31fbd-458">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="31fbd-459">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="31fbd-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="31fbd-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="31fbd-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="31fbd-461">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="31fbd-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="31fbd-462">AzureRM.Dns</span></span>
* <span data-ttu-id="31fbd-463">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="31fbd-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31fbd-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="31fbd-465">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="31fbd-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="31fbd-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="31fbd-467">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="31fbd-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31fbd-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="31fbd-469">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="31fbd-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="31fbd-470">AzureRM.Insights</span></span>
* <span data-ttu-id="31fbd-471">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="31fbd-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="31fbd-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="31fbd-473">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="31fbd-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31fbd-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="31fbd-475">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="31fbd-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31fbd-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="31fbd-477">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="31fbd-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="31fbd-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="31fbd-479">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="31fbd-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="31fbd-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="31fbd-481">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="31fbd-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="31fbd-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="31fbd-483">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="31fbd-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="31fbd-484">AzureRM.Media</span></span>
* <span data-ttu-id="31fbd-485">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-486">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-487">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="31fbd-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="31fbd-488">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="31fbd-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="31fbd-489">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="31fbd-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="31fbd-490">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="31fbd-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="31fbd-491">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="31fbd-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="31fbd-492">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="31fbd-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="31fbd-493">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="31fbd-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="31fbd-494">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="31fbd-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="31fbd-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="31fbd-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="31fbd-496">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="31fbd-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31fbd-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="31fbd-498">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="31fbd-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31fbd-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="31fbd-500">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="31fbd-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="31fbd-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="31fbd-502">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="31fbd-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="31fbd-504">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="31fbd-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31fbd-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31fbd-506">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="31fbd-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="31fbd-507">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="31fbd-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="31fbd-508">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="31fbd-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="31fbd-509">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="31fbd-510">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="31fbd-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="31fbd-511">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="31fbd-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="31fbd-512">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="31fbd-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="31fbd-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="31fbd-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="31fbd-514">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="31fbd-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="31fbd-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="31fbd-516">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="31fbd-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="31fbd-517">AzureRM.Relay</span></span>
* <span data-ttu-id="31fbd-518">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-519">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-520">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="31fbd-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="31fbd-521">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="31fbd-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="31fbd-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="31fbd-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="31fbd-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="31fbd-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="31fbd-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="31fbd-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="31fbd-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="31fbd-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="31fbd-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="31fbd-529">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="31fbd-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="31fbd-530">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="31fbd-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="31fbd-531">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="31fbd-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="31fbd-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="31fbd-533">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-535">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="31fbd-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31fbd-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="31fbd-537">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-538">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-539">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="31fbd-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-540">AzureRM.Storage</span></span>
* <span data-ttu-id="31fbd-541">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="31fbd-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="31fbd-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="31fbd-543">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="31fbd-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="31fbd-544">AzureRM.Tags</span></span>
* <span data-ttu-id="31fbd-545">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="31fbd-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31fbd-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="31fbd-547">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="31fbd-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="31fbd-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="31fbd-549">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-550">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-551">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="31fbd-552">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31fbd-553">Généralités</span><span class="sxs-lookup"><span data-stu-id="31fbd-553">General</span></span>
* <span data-ttu-id="31fbd-554">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="31fbd-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-555">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-556">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="31fbd-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="31fbd-557">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="31fbd-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-558">Azure.Storage</span></span>
* <span data-ttu-id="31fbd-559">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="31fbd-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="31fbd-560">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="31fbd-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="31fbd-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31fbd-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="31fbd-562">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="31fbd-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="31fbd-563">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="31fbd-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="31fbd-564">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="31fbd-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="31fbd-565">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="31fbd-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="31fbd-566">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="31fbd-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="31fbd-567">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="31fbd-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-568">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-569">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="31fbd-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="31fbd-570">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="31fbd-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="31fbd-571">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="31fbd-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="31fbd-572">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="31fbd-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="31fbd-573">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="31fbd-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="31fbd-574">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="31fbd-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="31fbd-575">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="31fbd-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="31fbd-576">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="31fbd-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="31fbd-577">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="31fbd-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="31fbd-578">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="31fbd-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="31fbd-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31fbd-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="31fbd-580">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="31fbd-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="31fbd-581">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="31fbd-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="31fbd-582">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="31fbd-583">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="31fbd-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="31fbd-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31fbd-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="31fbd-585">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="31fbd-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="31fbd-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="31fbd-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="31fbd-587">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="31fbd-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="31fbd-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="31fbd-588">AzureRM.Insights</span></span>
* <span data-ttu-id="31fbd-589">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="31fbd-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="31fbd-590">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="31fbd-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="31fbd-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31fbd-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="31fbd-592">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-593">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-594">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="31fbd-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-595">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-596">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="31fbd-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="31fbd-597">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="31fbd-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-599">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="31fbd-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="31fbd-600">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="31fbd-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-601">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-602">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="31fbd-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="31fbd-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="31fbd-604">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="31fbd-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="31fbd-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="31fbd-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="31fbd-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="31fbd-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="31fbd-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="31fbd-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="31fbd-608">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="31fbd-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="31fbd-609">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="31fbd-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="31fbd-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-610">AzureRM.Storage</span></span>
* <span data-ttu-id="31fbd-611">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="31fbd-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="31fbd-612">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="31fbd-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="31fbd-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31fbd-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="31fbd-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31fbd-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="31fbd-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="31fbd-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="31fbd-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="31fbd-616">AzureRM.Tags</span></span>
* <span data-ttu-id="31fbd-617">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="31fbd-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="31fbd-618">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-619">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-620">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="31fbd-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="31fbd-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-621">Azure.Storage</span></span>
* <span data-ttu-id="31fbd-622">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="31fbd-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="31fbd-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="31fbd-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="31fbd-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="31fbd-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="31fbd-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="31fbd-626">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="31fbd-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="31fbd-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="31fbd-627">AzureRM.Automation</span></span>
* <span data-ttu-id="31fbd-628">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="31fbd-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-629">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-630">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="31fbd-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="31fbd-631">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="31fbd-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="31fbd-632">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="31fbd-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="31fbd-633">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="31fbd-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="31fbd-634">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="31fbd-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="31fbd-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="31fbd-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="31fbd-636">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="31fbd-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="31fbd-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31fbd-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="31fbd-638">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="31fbd-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="31fbd-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="31fbd-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="31fbd-640">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="31fbd-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-641">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-642">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="31fbd-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="31fbd-643">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="31fbd-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="31fbd-644">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="31fbd-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="31fbd-645">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="31fbd-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="31fbd-646">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="31fbd-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="31fbd-647">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="31fbd-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="31fbd-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="31fbd-648">AzureRM.Relay</span></span>
* <span data-ttu-id="31fbd-649">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="31fbd-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-650">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-651">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="31fbd-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="31fbd-652">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="31fbd-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="31fbd-653">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="31fbd-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="31fbd-654">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="31fbd-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="31fbd-655">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="31fbd-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-657">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="31fbd-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="31fbd-658">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="31fbd-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="31fbd-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31fbd-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="31fbd-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31fbd-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="31fbd-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31fbd-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="31fbd-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31fbd-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="31fbd-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="31fbd-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="31fbd-664">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="31fbd-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="31fbd-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31fbd-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="31fbd-666">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="31fbd-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-667">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-668">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="31fbd-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="31fbd-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="31fbd-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-671">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-672">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="31fbd-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="31fbd-673">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="31fbd-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="31fbd-674">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="31fbd-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="31fbd-675">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="31fbd-676">Généralités</span><span class="sxs-lookup"><span data-stu-id="31fbd-676">General</span></span>
* <span data-ttu-id="31fbd-677">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="31fbd-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-678">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-679">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="31fbd-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-680">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-681">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="31fbd-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="31fbd-682">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="31fbd-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="31fbd-683">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="31fbd-684">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="31fbd-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="31fbd-685">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="31fbd-686">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="31fbd-687">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="31fbd-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="31fbd-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="31fbd-689">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="31fbd-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="31fbd-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31fbd-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="31fbd-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31fbd-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="31fbd-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31fbd-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="31fbd-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31fbd-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="31fbd-694">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="31fbd-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="31fbd-695">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="31fbd-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="31fbd-696">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="31fbd-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="31fbd-697">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="31fbd-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="31fbd-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="31fbd-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="31fbd-699">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="31fbd-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="31fbd-700">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="31fbd-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="31fbd-701">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="31fbd-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="31fbd-702">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="31fbd-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="31fbd-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31fbd-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="31fbd-704">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="31fbd-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-705">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-706">Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone</span><span class="sxs-lookup"><span data-stu-id="31fbd-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="31fbd-707">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="31fbd-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="31fbd-708">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="31fbd-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="31fbd-709">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="31fbd-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="31fbd-710">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="31fbd-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="31fbd-711">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="31fbd-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="31fbd-712">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="31fbd-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="31fbd-713">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="31fbd-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="31fbd-714">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="31fbd-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="31fbd-715">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31fbd-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="31fbd-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31fbd-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31fbd-717">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="31fbd-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="31fbd-718">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="31fbd-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="31fbd-719">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="31fbd-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-720">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-721">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="31fbd-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="31fbd-722">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="31fbd-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="31fbd-723">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="31fbd-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="31fbd-724">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="31fbd-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="31fbd-725">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="31fbd-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="31fbd-726">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="31fbd-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="31fbd-727">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="31fbd-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="31fbd-728">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="31fbd-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="31fbd-729">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="31fbd-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="31fbd-730">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="31fbd-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="31fbd-731">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="31fbd-732">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="31fbd-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="31fbd-733">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="31fbd-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="31fbd-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="31fbd-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="31fbd-735">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="31fbd-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-736">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-737">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="31fbd-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="31fbd-738">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="31fbd-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="31fbd-739">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-740">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-741">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="31fbd-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="31fbd-742">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="31fbd-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="31fbd-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="31fbd-743">Azure.Storage</span></span>
* <span data-ttu-id="31fbd-744">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="31fbd-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-745">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-746">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="31fbd-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="31fbd-747">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="31fbd-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="31fbd-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="31fbd-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="31fbd-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="31fbd-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="31fbd-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="31fbd-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="31fbd-751">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="31fbd-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="31fbd-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="31fbd-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="31fbd-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="31fbd-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="31fbd-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="31fbd-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="31fbd-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="31fbd-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="31fbd-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="31fbd-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="31fbd-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="31fbd-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="31fbd-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="31fbd-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="31fbd-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="31fbd-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="31fbd-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="31fbd-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="31fbd-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="31fbd-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="31fbd-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="31fbd-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="31fbd-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="31fbd-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="31fbd-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="31fbd-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="31fbd-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="31fbd-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="31fbd-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="31fbd-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="31fbd-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="31fbd-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="31fbd-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="31fbd-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="31fbd-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="31fbd-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="31fbd-772">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="31fbd-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="31fbd-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31fbd-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="31fbd-774">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="31fbd-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="31fbd-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="31fbd-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="31fbd-776">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="31fbd-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="31fbd-777">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="31fbd-778">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="31fbd-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="31fbd-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="31fbd-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="31fbd-780">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="31fbd-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="31fbd-781">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="31fbd-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-782">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-783">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="31fbd-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="31fbd-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31fbd-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="31fbd-785">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-786">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-787">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="31fbd-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="31fbd-788">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="31fbd-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="31fbd-789">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="31fbd-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="31fbd-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="31fbd-791">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="31fbd-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="31fbd-792">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-793">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-794">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="31fbd-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="31fbd-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="31fbd-795">AzureRM.Compute</span></span>
* <span data-ttu-id="31fbd-796">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="31fbd-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="31fbd-797">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="31fbd-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="31fbd-798">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="31fbd-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="31fbd-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="31fbd-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="31fbd-800">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="31fbd-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="31fbd-801">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="31fbd-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="31fbd-802">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="31fbd-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="31fbd-803">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="31fbd-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="31fbd-804">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="31fbd-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="31fbd-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="31fbd-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="31fbd-806">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="31fbd-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-807">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-808">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="31fbd-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="31fbd-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="31fbd-809">AzureRM.Resources</span></span>
* <span data-ttu-id="31fbd-810">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="31fbd-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="31fbd-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="31fbd-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="31fbd-812">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="31fbd-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="31fbd-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-813">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-814">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="31fbd-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="31fbd-815">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31fbd-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="31fbd-816">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="31fbd-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="31fbd-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="31fbd-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="31fbd-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="31fbd-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="31fbd-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31fbd-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="31fbd-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="31fbd-820">AzureRM.Websites</span></span>
* <span data-ttu-id="31fbd-821">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="31fbd-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="31fbd-822">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="31fbd-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="31fbd-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="31fbd-823">AzureRM.Profile</span></span>
* <span data-ttu-id="31fbd-824">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="31fbd-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="31fbd-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="31fbd-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="31fbd-826">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="31fbd-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="31fbd-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="31fbd-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="31fbd-828">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="31fbd-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="31fbd-829">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31fbd-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="31fbd-830">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="31fbd-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="31fbd-831">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="31fbd-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="31fbd-832">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="31fbd-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="31fbd-833">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="31fbd-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="31fbd-834">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="31fbd-834">Added support for MSI identity</span></span>
* <span data-ttu-id="31fbd-835">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="31fbd-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="31fbd-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="31fbd-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="31fbd-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="31fbd-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="31fbd-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="31fbd-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="31fbd-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="31fbd-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="31fbd-840">AzureRM.Batch</span></span>
* <span data-ttu-id="31fbd-841">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="31fbd-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="31fbd-842">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="31fbd-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="31fbd-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="31fbd-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="31fbd-844">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="31fbd-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="31fbd-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="31fbd-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="31fbd-846">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="31fbd-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="31fbd-847">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31fbd-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="31fbd-848">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31fbd-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="31fbd-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="31fbd-849">AzureRM.Network</span></span>
* <span data-ttu-id="31fbd-850">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="31fbd-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="31fbd-851">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="31fbd-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="31fbd-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="31fbd-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="31fbd-853">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="31fbd-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="31fbd-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="31fbd-855">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="31fbd-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="31fbd-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="31fbd-857">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="31fbd-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="31fbd-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="31fbd-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="31fbd-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="31fbd-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="31fbd-860">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="31fbd-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="31fbd-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="31fbd-861">AzureRM.Sql</span></span>
* <span data-ttu-id="31fbd-862">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="31fbd-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="31fbd-863">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="31fbd-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="31fbd-864">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="31fbd-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="31fbd-865">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="31fbd-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="31fbd-866">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="31fbd-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="31fbd-867">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31fbd-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="31fbd-868">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="31fbd-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="31fbd-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="31fbd-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="31fbd-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="31fbd-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="31fbd-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="31fbd-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="31fbd-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="31fbd-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="31fbd-873">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="31fbd-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
