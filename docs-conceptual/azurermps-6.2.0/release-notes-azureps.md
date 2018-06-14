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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853455"
---
# <a name="release-notes"></a><span data-ttu-id="17354-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="17354-103">Release notes</span></span>

<span data-ttu-id="17354-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="17354-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="17354-105">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="17354-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="17354-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="17354-106">AzureRM.Profile</span></span>
* <span data-ttu-id="17354-107">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="17354-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="17354-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="17354-108">AzureRM.Compute</span></span>
* <span data-ttu-id="17354-109">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="17354-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="17354-110">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="17354-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="17354-111">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="17354-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="17354-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="17354-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="17354-113">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="17354-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="17354-114">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="17354-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="17354-115">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="17354-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="17354-116">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="17354-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="17354-117">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="17354-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="17354-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="17354-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="17354-119">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="17354-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="17354-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="17354-120">AzureRM.Network</span></span>
* <span data-ttu-id="17354-121">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="17354-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="17354-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="17354-122">AzureRM.Resources</span></span>
* <span data-ttu-id="17354-123">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="17354-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="17354-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="17354-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="17354-125">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="17354-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="17354-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="17354-126">AzureRM.Sql</span></span>
* <span data-ttu-id="17354-127">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="17354-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="17354-128">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="17354-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="17354-129">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="17354-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="17354-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="17354-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="17354-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="17354-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="17354-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="17354-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="17354-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="17354-133">AzureRM.Websites</span></span>
* <span data-ttu-id="17354-134">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="17354-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="17354-135">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="17354-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="17354-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="17354-136">AzureRM.Profile</span></span>
* <span data-ttu-id="17354-137">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="17354-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="17354-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="17354-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="17354-139">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="17354-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="17354-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="17354-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="17354-141">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="17354-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="17354-142">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17354-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="17354-143">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="17354-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="17354-144">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="17354-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="17354-145">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="17354-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="17354-146">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="17354-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="17354-147">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="17354-147">Added support for MSI identity</span></span>
* <span data-ttu-id="17354-148">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="17354-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="17354-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="17354-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="17354-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="17354-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="17354-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="17354-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="17354-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="17354-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="17354-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="17354-153">AzureRM.Batch</span></span>
* <span data-ttu-id="17354-154">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="17354-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="17354-155">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="17354-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="17354-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="17354-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="17354-157">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="17354-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="17354-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="17354-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="17354-159">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="17354-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="17354-160">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="17354-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="17354-161">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="17354-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="17354-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="17354-162">AzureRM.Network</span></span>
* <span data-ttu-id="17354-163">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="17354-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="17354-164">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="17354-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="17354-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="17354-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="17354-166">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="17354-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="17354-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="17354-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="17354-168">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="17354-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="17354-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="17354-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="17354-170">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="17354-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="17354-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="17354-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="17354-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17354-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="17354-173">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="17354-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="17354-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="17354-174">AzureRM.Sql</span></span>
* <span data-ttu-id="17354-175">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="17354-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="17354-176">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="17354-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="17354-177">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="17354-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="17354-178">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="17354-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="17354-179">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="17354-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="17354-180">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="17354-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="17354-181">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="17354-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="17354-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="17354-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="17354-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="17354-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="17354-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="17354-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="17354-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="17354-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="17354-186">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="17354-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>