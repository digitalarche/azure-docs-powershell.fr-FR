---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461751"
---
# <a name="release-notes"></a><span data-ttu-id="ed5c4-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="ed5c4-103">Release notes</span></span>

<span data-ttu-id="ed5c4-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="ed5c4-105">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="ed5c4-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ed5c4-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ed5c4-106">AzureRM.Profile</span></span>
* <span data-ttu-id="ed5c4-107">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="ed5c4-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ed5c4-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ed5c4-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ed5c4-109">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="ed5c4-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ed5c4-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ed5c4-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ed5c4-111">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="ed5c4-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ed5c4-112">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed5c4-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ed5c4-113">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="ed5c4-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ed5c4-114">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="ed5c4-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ed5c4-115">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="ed5c4-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ed5c4-116">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="ed5c4-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ed5c4-117">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="ed5c4-117">Added support for MSI identity</span></span>
* <span data-ttu-id="ed5c4-118">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="ed5c4-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ed5c4-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ed5c4-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ed5c4-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed5c4-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ed5c4-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ed5c4-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ed5c4-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ed5c4-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ed5c4-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ed5c4-123">AzureRM.Batch</span></span>
* <span data-ttu-id="ed5c4-124">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ed5c4-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ed5c4-125">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ed5c4-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ed5c4-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ed5c4-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="ed5c4-127">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="ed5c4-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ed5c4-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ed5c4-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ed5c4-129">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ed5c4-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ed5c4-130">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ed5c4-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ed5c4-131">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ed5c4-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ed5c4-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ed5c4-132">AzureRM.Network</span></span>
* <span data-ttu-id="ed5c4-133">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="ed5c4-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ed5c4-134">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="ed5c4-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ed5c4-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed5c4-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ed5c4-136">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="ed5c4-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ed5c4-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed5c4-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ed5c4-138">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="ed5c4-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ed5c4-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed5c4-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ed5c4-140">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="ed5c4-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ed5c4-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ed5c4-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ed5c4-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ed5c4-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ed5c4-143">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="ed5c4-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ed5c4-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ed5c4-144">AzureRM.Sql</span></span>
* <span data-ttu-id="ed5c4-145">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ed5c4-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ed5c4-146">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ed5c4-147">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="ed5c4-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ed5c4-148">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="ed5c4-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ed5c4-149">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="ed5c4-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ed5c4-150">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed5c4-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ed5c4-151">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ed5c4-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ed5c4-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ed5c4-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ed5c4-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ed5c4-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ed5c4-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ed5c4-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ed5c4-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ed5c4-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ed5c4-156">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="ed5c4-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>