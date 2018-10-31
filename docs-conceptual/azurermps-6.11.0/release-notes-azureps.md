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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001505"
---
# <a name="release-notes"></a><span data-ttu-id="ce5a7-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="ce5a7-103">Release notes</span></span>

<span data-ttu-id="ce5a7-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="ce5a7-105">6.11.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-106">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-107">Problème résolu avec Get-AzureRmSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="ce5a7-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="ce5a7-108">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ce5a7-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ce5a7-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-109">AzureRM.Backup</span></span>
* <span data-ttu-id="ce5a7-110">Applets de commande Sauvegarde Azure déconseillés.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-111">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-112">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation de l’ensemble de paramètres simple pour « New-AzureRmVm »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="ce5a7-113">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce5a7-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce5a7-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce5a7-115">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="ce5a7-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ce5a7-116">Get-AzureRmDataLakeStoreVirtualNetworkRule : obtient ou liste la règle de réseau virtuel d’Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ce5a7-117">Add-AzureRmDataLakeStoreVirtualNetworkRule : ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ce5a7-118">Set-AzureRmDataLakeStoreVirtualNetworkRule : modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ce5a7-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule : supprime une règle de réseau virtuel d’Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-120">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-121">Mise à jour de l’applet de commande Test-AzureRmNetworkWatcherConnectivity, passage de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ce5a7-122">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-123">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-124">Résout les problèmes où Get-AzureRMRoleDefinition lève une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ce5a7-125">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="ce5a7-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="ce5a7-126">6.10.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ce5a7-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-127">Azure.Storage</span></span>
* <span data-ttu-id="ce5a7-128">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ce5a7-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ce5a7-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ce5a7-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ce5a7-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ce5a7-132">Prise en charge de Get-AzureRmCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-133">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-134">Correction de Get-AzureRmVM -ResourceGroupName <rg> pour retourner plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="ce5a7-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ce5a7-135">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="ce5a7-136">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="ce5a7-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce5a7-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce5a7-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce5a7-138">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-139">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-140">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ce5a7-141">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="ce5a7-141">new cmdlets added</span></span>
    - <span data-ttu-id="ce5a7-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce5a7-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce5a7-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce5a7-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="ce5a7-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="ce5a7-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ce5a7-148">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ce5a7-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ce5a7-149">Ajout des cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ce5a7-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="ce5a7-150">Ajout des cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ce5a7-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ce5a7-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ce5a7-152">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ce5a7-153">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ce5a7-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-154">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-155">Ajout du paramètre manquant -Mode à Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ce5a7-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="ce5a7-156">Correction d’un bug de la cmdlet Get-AzureRmProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="ce5a7-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-157">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-158">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="ce5a7-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce5a7-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-159">AzureRM.Storage</span></span>
* <span data-ttu-id="ce5a7-160">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ce5a7-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-162">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-163">Nouvelle cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="ce5a7-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ce5a7-164">Nouvelles cmdlets New-AzureRMWebAppContainerPSSession et Enter-WebAppContainerPSSession - démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="ce5a7-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="ce5a7-165">6.9.0 - septembre 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce5a7-166">Généralités</span><span class="sxs-lookup"><span data-stu-id="ce5a7-166">General</span></span>
* <span data-ttu-id="ce5a7-167">AzureRM.SignalR a été ajouté au module Rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-168">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-169">Modifications mineures du code commun de stockage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ce5a7-170">Mise à jour des fichiers d’aide pour inclure des types de paramètre complet.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="ce5a7-171">Modification de -ServicePrincipal en non obligatoire dans l’ensemble de paramètres ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce5a7-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ce5a7-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-172">Azure.Storage</span></span>
* <span data-ttu-id="ce5a7-173">Prise en charge du contexte de stockage avec OAuth.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ce5a7-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce5a7-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ce5a7-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ce5a7-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="ce5a7-176">Ajout de Standard_Microsoft dans la référence SKU de tarification d’un CDN.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-177">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-178">Déplacement des dépendances du coffre de clés et du stockage vers les dépendances communes</span><span class="sxs-lookup"><span data-stu-id="ce5a7-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ce5a7-179">Ajout de la prise en charge de plus de tailles de machine virtuelle aux cmdlets AEM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ce5a7-180">Ajout du paramètre PublicIPPrefix à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ce5a7-181">Ajout du paramètre ResourceId à la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ce5a7-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ce5a7-182">Ajout de la cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ce5a7-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ce5a7-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ce5a7-183">AzureRM.Dns</span></span>
* <span data-ttu-id="ce5a7-184">Prise en charge de l’enregistrement d’alias pendant la création d’enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="ce5a7-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ce5a7-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-185">AzureRM.Insights</span></span>
* <span data-ttu-id="ce5a7-186">Résolution des problèmes #6833 et #7102 (zone Paramètres de diagnostic)</span><span class="sxs-lookup"><span data-stu-id="ce5a7-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ce5a7-187">Problèmes avec un nom par défaut, par exemple « service », lors de la création et l’obtention/le référencement des paramètres de diagnostic</span><span class="sxs-lookup"><span data-stu-id="ce5a7-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ce5a7-188">Problèmes créant des paramètres de diagnostic avec des catégories</span><span class="sxs-lookup"><span data-stu-id="ce5a7-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ce5a7-189">Ajout de message de désapprobation pour les paramètres de fragments de temps de métriques</span><span class="sxs-lookup"><span data-stu-id="ce5a7-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ce5a7-190">Les paramètres Timegrains sont toujours acceptés (il s’agit d’une modification sans rupture,), mais ils sont ignorés dans le serveur principal dans la mesure où seul PT1M est valide</span><span class="sxs-lookup"><span data-stu-id="ce5a7-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-191">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-192">Modifications apportées aux cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce5a7-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ce5a7-193">LoadBalancerInboundNatPoolConfig : ajout des paramètres IdleTimeoutInMinutes, EnableFloatingIp et EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ce5a7-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ce5a7-194">LoadBalancerInboundNatRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ce5a7-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ce5a7-195">LoadBalancerRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ce5a7-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ce5a7-196">LoadBalancerProbeConfig : ajout d’une prise en charge de la valeur « Https » pour le paramètre Protocole</span><span class="sxs-lookup"><span data-stu-id="ce5a7-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ce5a7-197">Ajout de nouvelles commandes pour la sous-ressource OutboundRule du nouveau LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce5a7-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ce5a7-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce5a7-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce5a7-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce5a7-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ce5a7-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ce5a7-203">Ajout d’une nouvelle propriété HostedWorkloads pour PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ce5a7-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ce5a7-204">Ajouté de nouvelles cmdlets pour la fonctionnalité : Pare-feu Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ce5a7-205">Ajout de Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce5a7-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce5a7-206">Ajout de Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce5a7-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce5a7-207">Ajout de New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce5a7-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce5a7-208">Ajout de Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce5a7-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ce5a7-209">Ajout de New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce5a7-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ce5a7-210">Ajout de New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ce5a7-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ce5a7-211">Ajout de New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce5a7-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ce5a7-212">Ajout de New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="ce5a7-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ce5a7-213">Ajout de New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce5a7-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ce5a7-214">Ajout de New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce5a7-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ce5a7-215">Ajout de la prise en charge du certificat racine approuvé et de la configuration de mise à l’échelle automatique dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ce5a7-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ce5a7-216">Nouvelles cmdlets ajoutées :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="ce5a7-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce5a7-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce5a7-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce5a7-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce5a7-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ce5a7-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce5a7-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce5a7-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce5a7-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ce5a7-226">Cmdlets mises à jour avec le paramètre facultatif -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ce5a7-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce5a7-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ce5a7-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce5a7-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ce5a7-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ce5a7-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ce5a7-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ce5a7-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ce5a7-231">Cmdlets mises à jour avec le paramètre facultatif -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ce5a7-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce5a7-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ce5a7-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce5a7-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ce5a7-234">Ajout d’une cmdlet pour le point de terminaison d’interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce5a7-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ce5a7-235">Ajout de la prise en charge de plusieurs préfixes d’adresse dans un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ce5a7-236">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="ce5a7-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce5a7-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce5a7-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce5a7-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ce5a7-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ce5a7-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ce5a7-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ce5a7-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ce5a7-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ce5a7-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ce5a7-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ce5a7-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ce5a7-249">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ce5a7-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ce5a7-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ce5a7-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ce5a7-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ce5a7-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ce5a7-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ce5a7-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ce5a7-256">Ajout de cmdlets pour la délégation de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ce5a7-257">New-AzureRmDelegation : crée une nouvelle délégation, celle-ci peut être ajoutée à un sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ce5a7-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ce5a7-258">Remove-AzureRmDelegation : accepte un sous-réseau et supprime le nom de délégation fourni de ce sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ce5a7-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ce5a7-259">Add-AzureRmDelegation : accepte un sous-réseau et ajoute le nom de service fourni en tant que délégation à ce sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ce5a7-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ce5a7-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ce5a7-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ce5a7-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ce5a7-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ce5a7-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ce5a7-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ce5a7-263">Prise en charge de la gestion de disque managé</span><span class="sxs-lookup"><span data-stu-id="ce5a7-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ce5a7-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ce5a7-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ce5a7-265">Mise à jour de la dépendance Insights.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-266">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-267">Mise à jour de New-AzureRmResourceGroupDeployment avec le nouveau paramètre RollbackAction</span><span class="sxs-lookup"><span data-stu-id="ce5a7-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ce5a7-268">Ajout de la prise en charge d’OnErrorDeployment avec le nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ce5a7-269">Prise en charge des identités managées sur les affectations de stratégies.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ce5a7-270">Des paramètres avec des valeurs par défaut ne sont plus requis lors de l’affectation d’une stratégie avec « New-AzureRmPolicyAssignment »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ce5a7-271">Ajout de la nouvelle cmdlet Get-AzureRmPolicyAlias pour récupérer les alias de stratégie</span><span class="sxs-lookup"><span data-stu-id="ce5a7-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-273">Résolution du problème #7161</span><span class="sxs-lookup"><span data-stu-id="ce5a7-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ce5a7-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ce5a7-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="ce5a7-275">Mise à jour des noms de référence SKU en Free_F1 et Standard_S1</span><span class="sxs-lookup"><span data-stu-id="ce5a7-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ce5a7-276">Ajout d’un champ de version à l’objet PSSignalRResource et d’une chaîne de connexion à l’objet PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce5a7-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-277">AzureRM.Storage</span></span>
* <span data-ttu-id="ce5a7-278">Prise en charge de la stratégie d’immuabilité dans AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ce5a7-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce5a7-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ce5a7-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce5a7-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce5a7-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce5a7-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce5a7-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce5a7-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce5a7-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ce5a7-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ce5a7-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ce5a7-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ce5a7-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ce5a7-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ce5a7-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ce5a7-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ce5a7-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ce5a7-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-290">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-291">Ajout de deux nouvelles cmdlets : Get-AzureRmDeletedWebApp et Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ce5a7-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ce5a7-292">New-AzureRmAppServicePlan : le commutateur HyperV est ajouté pour créer un plan App Service avec conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="ce5a7-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ce5a7-293">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot : les nouveaux paramètres (la chaîne -ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) ajoutés pour créer et gérer l’application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="ce5a7-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ce5a7-294">6.8.1 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce5a7-295">Généralités</span><span class="sxs-lookup"><span data-stu-id="ce5a7-295">General</span></span>
* <span data-ttu-id="ce5a7-296">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ce5a7-297">Mise à jour des assemblys de runtime courants</span><span class="sxs-lookup"><span data-stu-id="ce5a7-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce5a7-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce5a7-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce5a7-299">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ce5a7-300">Problème résolu https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="ce5a7-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ce5a7-301">Les cmdlets Import-AzureRmApiManagementApi et \*-AzureRmApiManagementCertificate peuvent maintenant gérer les chemins d’accès relatifs</span><span class="sxs-lookup"><span data-stu-id="ce5a7-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ce5a7-302">Problème résolu https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="ce5a7-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ce5a7-303">CertificateInformation est une propriété définissable permettant à la cmdlet Set-AzureRmApiManagement de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ce5a7-304">Résolu en passant au nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="ce5a7-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ce5a7-305">Problème résolu https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="ce5a7-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ce5a7-306">Recherche par nom sur produit du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="ce5a7-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ce5a7-307">Problème résolu https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="ce5a7-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ce5a7-308">Recherche par nom sur Api du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="ce5a7-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ce5a7-309">Ajout de la prise en charge de l’enregistreur d'événements AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="ce5a7-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-310">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-311">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ce5a7-312">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="ce5a7-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ce5a7-313">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ce5a7-314">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="ce5a7-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-315">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-316">Modification de la présentation d’une sortie de cmdlet par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="ce5a7-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ce5a7-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ce5a7-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ce5a7-318">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="ce5a7-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-319">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-320">Résolution du problème de création d’applications managées depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-322">Problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce5a7-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce5a7-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce5a7-324">Ajout de la prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ce5a7-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ce5a7-325">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ce5a7-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ce5a7-326">Ajout de la prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="ce5a7-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ce5a7-327">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce5a7-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ce5a7-328">Ajout de la prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="ce5a7-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ce5a7-329">Ajout de la prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="ce5a7-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ce5a7-330">Ajout de la prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce5a7-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ce5a7-331">6.8.0 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce5a7-332">Généralités</span><span class="sxs-lookup"><span data-stu-id="ce5a7-332">General</span></span>
* <span data-ttu-id="ce5a7-333">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-334">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-335">Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-336">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-337">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ce5a7-338">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="ce5a7-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ce5a7-339">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="ce5a7-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ce5a7-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ce5a7-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="ce5a7-341">Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-342">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-343">Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="ce5a7-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ce5a7-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ce5a7-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ce5a7-345">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="ce5a7-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-346">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-347">Résolution du problème de création d’application managée depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-349">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="ce5a7-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce5a7-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce5a7-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce5a7-351">Prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ce5a7-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ce5a7-352">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ce5a7-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ce5a7-353">Prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="ce5a7-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ce5a7-354">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce5a7-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ce5a7-355">Prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="ce5a7-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ce5a7-356">Prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="ce5a7-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ce5a7-357">Prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ce5a7-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-358">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-359">Résolution du problème relatif aux groupes de ressources par défaut mal définis.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ce5a7-360">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-361">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-362">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce5a7-363">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ce5a7-364">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ce5a7-365">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ce5a7-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-366">Azure.Storage</span></span>
* <span data-ttu-id="ce5a7-367">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ce5a7-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ce5a7-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ce5a7-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ce5a7-370">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ce5a7-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ce5a7-372">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce5a7-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce5a7-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce5a7-374">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ce5a7-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ce5a7-376">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ce5a7-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ce5a7-377">AzureRM.Automation</span></span>
* <span data-ttu-id="ce5a7-378">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ce5a7-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-379">AzureRM.Backup</span></span>
* <span data-ttu-id="ce5a7-380">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ce5a7-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ce5a7-381">AzureRM.Batch</span></span>
* <span data-ttu-id="ce5a7-382">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ce5a7-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ce5a7-383">AzureRM.Billing</span></span>
* <span data-ttu-id="ce5a7-384">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ce5a7-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ce5a7-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="ce5a7-386">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ce5a7-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ce5a7-388">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-389">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-390">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce5a7-391">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ce5a7-392">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ce5a7-393">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ce5a7-394">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ce5a7-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ce5a7-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="ce5a7-396">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ce5a7-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ce5a7-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ce5a7-398">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ce5a7-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce5a7-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ce5a7-400">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ce5a7-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ce5a7-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ce5a7-402">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce5a7-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce5a7-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce5a7-404">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ce5a7-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ce5a7-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ce5a7-406">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce5a7-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce5a7-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce5a7-408">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ce5a7-409">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ce5a7-410">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce5a7-411">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ce5a7-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ce5a7-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ce5a7-413">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ce5a7-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ce5a7-414">AzureRM.Dns</span></span>
* <span data-ttu-id="ce5a7-415">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ce5a7-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ce5a7-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ce5a7-417">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce5a7-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce5a7-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce5a7-419">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ce5a7-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ce5a7-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ce5a7-421">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ce5a7-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-422">AzureRM.Insights</span></span>
* <span data-ttu-id="ce5a7-423">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ce5a7-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ce5a7-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="ce5a7-425">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce5a7-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce5a7-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce5a7-427">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ce5a7-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ce5a7-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ce5a7-429">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ce5a7-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ce5a7-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ce5a7-431">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ce5a7-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ce5a7-433">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ce5a7-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ce5a7-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ce5a7-435">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ce5a7-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ce5a7-436">AzureRM.Media</span></span>
* <span data-ttu-id="ce5a7-437">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-438">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-439">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ce5a7-440">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ce5a7-441">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ce5a7-442">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ce5a7-443">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ce5a7-444">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ce5a7-445">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ce5a7-446">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ce5a7-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ce5a7-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ce5a7-448">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ce5a7-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ce5a7-450">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ce5a7-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ce5a7-452">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ce5a7-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ce5a7-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ce5a7-454">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ce5a7-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ce5a7-456">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ce5a7-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ce5a7-458">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ce5a7-459">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ce5a7-460">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ce5a7-461">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ce5a7-462">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ce5a7-463">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ce5a7-464">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ce5a7-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ce5a7-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ce5a7-466">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ce5a7-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ce5a7-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ce5a7-468">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ce5a7-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ce5a7-469">AzureRM.Relay</span></span>
* <span data-ttu-id="ce5a7-470">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-471">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-472">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ce5a7-473">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ce5a7-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce5a7-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce5a7-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce5a7-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce5a7-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ce5a7-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ce5a7-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ce5a7-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ce5a7-481">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ce5a7-482">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ce5a7-483">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ce5a7-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ce5a7-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ce5a7-485">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-487">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ce5a7-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce5a7-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ce5a7-489">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-490">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-491">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce5a7-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-492">AzureRM.Storage</span></span>
* <span data-ttu-id="ce5a7-493">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ce5a7-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ce5a7-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ce5a7-495">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ce5a7-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ce5a7-496">AzureRM.Tags</span></span>
* <span data-ttu-id="ce5a7-497">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce5a7-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce5a7-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce5a7-499">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ce5a7-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ce5a7-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ce5a7-501">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-502">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-503">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ce5a7-504">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce5a7-505">Généralités</span><span class="sxs-lookup"><span data-stu-id="ce5a7-505">General</span></span>
* <span data-ttu-id="ce5a7-506">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-507">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-508">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ce5a7-509">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ce5a7-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-510">Azure.Storage</span></span>
* <span data-ttu-id="ce5a7-511">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ce5a7-512">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce5a7-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce5a7-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce5a7-514">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="ce5a7-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ce5a7-515">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="ce5a7-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ce5a7-516">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="ce5a7-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ce5a7-517">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ce5a7-518">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="ce5a7-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ce5a7-519">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="ce5a7-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-520">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-521">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ce5a7-522">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ce5a7-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ce5a7-523">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ce5a7-524">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="ce5a7-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ce5a7-525">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ce5a7-526">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ce5a7-527">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ce5a7-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ce5a7-528">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ce5a7-529">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="ce5a7-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ce5a7-530">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce5a7-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce5a7-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce5a7-532">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ce5a7-533">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ce5a7-534">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ce5a7-535">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce5a7-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce5a7-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce5a7-537">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="ce5a7-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce5a7-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce5a7-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce5a7-539">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="ce5a7-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ce5a7-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-540">AzureRM.Insights</span></span>
* <span data-ttu-id="ce5a7-541">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="ce5a7-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ce5a7-542">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="ce5a7-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce5a7-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce5a7-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce5a7-544">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-545">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-546">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-547">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-548">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ce5a7-549">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-551">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="ce5a7-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ce5a7-552">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-553">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-554">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ce5a7-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ce5a7-556">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ce5a7-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="ce5a7-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ce5a7-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="ce5a7-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ce5a7-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="ce5a7-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ce5a7-560">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ce5a7-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ce5a7-561">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="ce5a7-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ce5a7-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-562">AzureRM.Storage</span></span>
* <span data-ttu-id="ce5a7-563">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="ce5a7-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ce5a7-564">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="ce5a7-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ce5a7-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce5a7-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ce5a7-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce5a7-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ce5a7-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce5a7-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ce5a7-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ce5a7-568">AzureRM.Tags</span></span>
* <span data-ttu-id="ce5a7-569">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="ce5a7-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ce5a7-570">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-571">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-572">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ce5a7-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-573">Azure.Storage</span></span>
* <span data-ttu-id="ce5a7-574">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="ce5a7-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ce5a7-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ce5a7-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ce5a7-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ce5a7-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ce5a7-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ce5a7-578">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ce5a7-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ce5a7-579">AzureRM.Automation</span></span>
* <span data-ttu-id="ce5a7-580">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-581">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-582">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce5a7-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ce5a7-583">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ce5a7-584">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ce5a7-585">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ce5a7-586">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce5a7-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce5a7-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce5a7-588">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="ce5a7-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce5a7-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce5a7-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce5a7-590">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ce5a7-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ce5a7-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ce5a7-592">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ce5a7-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-593">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-594">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ce5a7-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ce5a7-595">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ce5a7-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ce5a7-596">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="ce5a7-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ce5a7-597">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ce5a7-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ce5a7-598">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ce5a7-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ce5a7-599">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="ce5a7-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ce5a7-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ce5a7-600">AzureRM.Relay</span></span>
* <span data-ttu-id="ce5a7-601">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="ce5a7-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-602">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-603">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ce5a7-604">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ce5a7-605">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ce5a7-606">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="ce5a7-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ce5a7-607">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="ce5a7-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-609">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="ce5a7-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ce5a7-610">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ce5a7-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce5a7-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce5a7-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce5a7-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ce5a7-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ce5a7-616">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="ce5a7-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ce5a7-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce5a7-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ce5a7-618">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-619">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-620">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="ce5a7-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ce5a7-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ce5a7-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-623">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-624">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ce5a7-625">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="ce5a7-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ce5a7-626">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="ce5a7-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ce5a7-627">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ce5a7-628">Généralités</span><span class="sxs-lookup"><span data-stu-id="ce5a7-628">General</span></span>
* <span data-ttu-id="ce5a7-629">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="ce5a7-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-630">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-631">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="ce5a7-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-632">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-633">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="ce5a7-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ce5a7-634">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="ce5a7-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ce5a7-635">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ce5a7-636">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="ce5a7-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ce5a7-637">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ce5a7-638">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ce5a7-639">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ce5a7-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ce5a7-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ce5a7-641">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ce5a7-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce5a7-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ce5a7-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce5a7-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ce5a7-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce5a7-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce5a7-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce5a7-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce5a7-646">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ce5a7-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ce5a7-647">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ce5a7-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ce5a7-648">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="ce5a7-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ce5a7-649">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="ce5a7-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ce5a7-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ce5a7-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="ce5a7-651">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ce5a7-652">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ce5a7-653">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ce5a7-654">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce5a7-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce5a7-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce5a7-656">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="ce5a7-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-657">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-658">Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone</span><span class="sxs-lookup"><span data-stu-id="ce5a7-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ce5a7-659">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ce5a7-660">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ce5a7-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ce5a7-661">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ce5a7-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ce5a7-662">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ce5a7-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ce5a7-663">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ce5a7-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ce5a7-664">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ce5a7-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ce5a7-665">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ce5a7-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ce5a7-666">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ce5a7-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ce5a7-667">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ce5a7-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ce5a7-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ce5a7-669">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ce5a7-670">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ce5a7-671">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-672">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-673">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ce5a7-674">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="ce5a7-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ce5a7-675">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="ce5a7-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ce5a7-676">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="ce5a7-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ce5a7-677">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ce5a7-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ce5a7-678">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="ce5a7-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ce5a7-679">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="ce5a7-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ce5a7-680">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ce5a7-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ce5a7-681">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="ce5a7-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ce5a7-682">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="ce5a7-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ce5a7-683">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ce5a7-684">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ce5a7-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ce5a7-685">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="ce5a7-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ce5a7-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ce5a7-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ce5a7-687">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-688">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-689">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ce5a7-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ce5a7-690">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="ce5a7-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ce5a7-691">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-692">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-693">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="ce5a7-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ce5a7-694">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="ce5a7-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ce5a7-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-695">Azure.Storage</span></span>
* <span data-ttu-id="ce5a7-696">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-697">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-698">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="ce5a7-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ce5a7-699">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="ce5a7-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ce5a7-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ce5a7-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ce5a7-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ce5a7-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ce5a7-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ce5a7-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ce5a7-703">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ce5a7-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ce5a7-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ce5a7-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ce5a7-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ce5a7-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ce5a7-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ce5a7-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ce5a7-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ce5a7-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ce5a7-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ce5a7-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ce5a7-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ce5a7-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ce5a7-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ce5a7-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ce5a7-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ce5a7-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ce5a7-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ce5a7-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ce5a7-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ce5a7-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ce5a7-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ce5a7-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ce5a7-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ce5a7-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ce5a7-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ce5a7-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ce5a7-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ce5a7-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce5a7-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ce5a7-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ce5a7-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ce5a7-724">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ce5a7-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce5a7-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce5a7-726">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="ce5a7-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ce5a7-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ce5a7-728">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ce5a7-729">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ce5a7-730">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ce5a7-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ce5a7-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ce5a7-732">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ce5a7-733">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-734">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-735">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ce5a7-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce5a7-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce5a7-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce5a7-737">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-738">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-739">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ce5a7-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ce5a7-740">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ce5a7-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ce5a7-741">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ce5a7-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ce5a7-743">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="ce5a7-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ce5a7-744">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-745">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-746">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="ce5a7-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ce5a7-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ce5a7-747">AzureRM.Compute</span></span>
* <span data-ttu-id="ce5a7-748">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="ce5a7-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ce5a7-749">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ce5a7-750">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ce5a7-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ce5a7-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ce5a7-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ce5a7-752">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ce5a7-753">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="ce5a7-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ce5a7-754">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="ce5a7-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ce5a7-755">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="ce5a7-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ce5a7-756">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="ce5a7-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ce5a7-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce5a7-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ce5a7-758">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="ce5a7-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-759">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-760">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="ce5a7-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ce5a7-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ce5a7-761">AzureRM.Resources</span></span>
* <span data-ttu-id="ce5a7-762">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="ce5a7-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ce5a7-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ce5a7-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ce5a7-764">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="ce5a7-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ce5a7-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-765">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-766">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="ce5a7-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ce5a7-767">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce5a7-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ce5a7-768">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce5a7-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ce5a7-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ce5a7-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce5a7-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ce5a7-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce5a7-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ce5a7-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ce5a7-772">AzureRM.Websites</span></span>
* <span data-ttu-id="ce5a7-773">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ce5a7-774">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="ce5a7-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ce5a7-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ce5a7-775">AzureRM.Profile</span></span>
* <span data-ttu-id="ce5a7-776">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="ce5a7-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ce5a7-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ce5a7-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ce5a7-778">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="ce5a7-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ce5a7-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce5a7-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ce5a7-780">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="ce5a7-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ce5a7-781">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce5a7-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ce5a7-782">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="ce5a7-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ce5a7-783">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="ce5a7-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ce5a7-784">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="ce5a7-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ce5a7-785">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ce5a7-786">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="ce5a7-786">Added support for MSI identity</span></span>
* <span data-ttu-id="ce5a7-787">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ce5a7-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ce5a7-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ce5a7-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ce5a7-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ce5a7-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ce5a7-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ce5a7-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ce5a7-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ce5a7-792">AzureRM.Batch</span></span>
* <span data-ttu-id="ce5a7-793">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ce5a7-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ce5a7-794">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ce5a7-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ce5a7-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ce5a7-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="ce5a7-796">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="ce5a7-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ce5a7-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ce5a7-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ce5a7-798">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ce5a7-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ce5a7-799">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce5a7-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ce5a7-800">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ce5a7-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ce5a7-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ce5a7-801">AzureRM.Network</span></span>
* <span data-ttu-id="ce5a7-802">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="ce5a7-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ce5a7-803">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ce5a7-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce5a7-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ce5a7-805">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ce5a7-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ce5a7-807">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ce5a7-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ce5a7-809">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ce5a7-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ce5a7-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ce5a7-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ce5a7-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ce5a7-812">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="ce5a7-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ce5a7-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ce5a7-813">AzureRM.Sql</span></span>
* <span data-ttu-id="ce5a7-814">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ce5a7-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ce5a7-815">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ce5a7-816">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="ce5a7-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ce5a7-817">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="ce5a7-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ce5a7-818">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="ce5a7-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ce5a7-819">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce5a7-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ce5a7-820">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce5a7-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ce5a7-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ce5a7-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ce5a7-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce5a7-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ce5a7-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ce5a7-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ce5a7-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ce5a7-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ce5a7-825">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="ce5a7-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
