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
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153171"
---
# <a name="release-notes"></a><span data-ttu-id="fe586-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="fe586-103">Release notes</span></span>

<span data-ttu-id="fe586-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="fe586-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="fe586-105">6.13.0 - novembre 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-106">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-107">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fe586-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fe586-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe586-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fe586-109">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="fe586-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fe586-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fe586-110">AzureRM.Automation</span></span>
* <span data-ttu-id="fe586-111">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="fe586-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="fe586-112">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="fe586-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="fe586-113">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="fe586-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="fe586-114">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="fe586-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="fe586-115">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="fe586-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-116">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-117">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="fe586-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="fe586-118">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="fe586-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fe586-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe586-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fe586-120">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="fe586-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="fe586-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fe586-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="fe586-122">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="fe586-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-123">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-124">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="fe586-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="fe586-125">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe586-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="fe586-126">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="fe586-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="fe586-127">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe586-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fe586-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fe586-129">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="fe586-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="fe586-130">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="fe586-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fe586-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fe586-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fe586-132">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fe586-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="fe586-133">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="fe586-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fe586-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fe586-134">AzureRM.Relay</span></span>
* <span data-ttu-id="fe586-135">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="fe586-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-136">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-137">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="fe586-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="fe586-138">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="fe586-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="fe586-139">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="fe586-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fe586-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe586-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fe586-141">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="fe586-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-142">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-143">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="fe586-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="fe586-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe586-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe586-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe586-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe586-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe586-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe586-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fe586-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="fe586-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fe586-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fe586-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="fe586-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="fe586-152">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="fe586-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="fe586-153">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="fe586-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="fe586-154">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="fe586-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="fe586-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe586-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fe586-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe586-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="fe586-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe586-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="fe586-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="fe586-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="fe586-159">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="fe586-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="fe586-160">6.12.0 - novembre 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-161">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-162">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fe586-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="fe586-163">Changement de nom du param TenantId dans la cmdlet Connect-AzureRmAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="fe586-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="fe586-164">Mise à jour de la description TenantId pour Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fe586-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="fe586-165">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="fe586-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="fe586-166">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="fe586-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="fe586-167">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="fe586-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="fe586-168">Correction du problème de levée de « Disconnect-AzureRmAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="fe586-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="fe586-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fe586-169">AzureRM.Automation</span></span>
* <span data-ttu-id="fe586-170">Changement du nom du fichier DLL de la cmdlet en Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="fe586-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fe586-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe586-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fe586-172">Ajout de l’opération Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="fe586-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-173">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-174">Ajout des cmdlets Add-AzureRmVmssVMDataDisk et Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fe586-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="fe586-175">Get-AzureRmVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="fe586-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="fe586-176">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzureRmVMChefExtension qui ne sont pas définies au format json.</span><span class="sxs-lookup"><span data-stu-id="fe586-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fe586-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe586-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fe586-178">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="fe586-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="fe586-179">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="fe586-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fe586-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fe586-180">AzureRM.Insights</span></span>
* <span data-ttu-id="fe586-181">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="fe586-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="fe586-182">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="fe586-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="fe586-183">Correction du problème #7513 [Insights], les catégories de Set-AzureRMDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="fe586-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="fe586-184">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="fe586-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-185">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-186">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="fe586-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="fe586-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe586-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="fe586-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="fe586-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="fe586-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fe586-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="fe586-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fe586-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fe586-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe586-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fe586-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fe586-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fe586-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe586-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fe586-194">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="fe586-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fe586-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fe586-196">Ajout de la prise en charge des partages de fichiers Azure partages dans Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="fe586-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-197">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-198">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="fe586-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="fe586-199">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="fe586-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-201">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="fe586-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fe586-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe586-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fe586-203">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="fe586-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="fe586-204">Correction de « Add-AzureRmServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="fe586-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="fe586-205">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="fe586-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="fe586-206">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="fe586-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="fe586-207">Correction de « Update-AzureRmServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="fe586-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="fe586-208">6.11.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-209">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-210">Problème résolu avec Get-AzureRmSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="fe586-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="fe586-211">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="fe586-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="fe586-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-212">AzureRM.Backup</span></span>
* <span data-ttu-id="fe586-213">Applets de commande Sauvegarde Azure déconseillés.</span><span class="sxs-lookup"><span data-stu-id="fe586-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-214">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-215">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation de l’ensemble de paramètres simple pour « New-AzureRmVm »</span><span class="sxs-lookup"><span data-stu-id="fe586-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="fe586-216">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="fe586-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fe586-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe586-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fe586-218">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="fe586-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="fe586-219">Get-AzureRmDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe586-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="fe586-220">Add-AzureRmDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="fe586-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fe586-221">Set-AzureRmDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="fe586-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="fe586-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fe586-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-223">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-224">Mise à jour de l’applet de commande Test-AzureRmNetworkWatcherConnectivity, passage de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="fe586-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="fe586-225">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="fe586-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-226">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-227">Résout les problèmes où Get-AzureRMRoleDefinition lève une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="fe586-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="fe586-228">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="fe586-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="fe586-229">6.10.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="fe586-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-230">Azure.Storage</span></span>
* <span data-ttu-id="fe586-231">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="fe586-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="fe586-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fe586-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="fe586-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="fe586-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fe586-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe586-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fe586-235">Prise en charge de Get-AzureRmCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="fe586-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-236">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-237">Correction de Get-AzureRmVM -ResourceGroupName <rg> pour retourner plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="fe586-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="fe586-238">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="fe586-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="fe586-239">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="fe586-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fe586-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fe586-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fe586-241">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="fe586-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-242">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-243">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="fe586-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="fe586-244">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="fe586-244">new cmdlets added</span></span>
    - <span data-ttu-id="fe586-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe586-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fe586-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe586-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fe586-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe586-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fe586-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="fe586-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="fe586-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="fe586-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="fe586-251">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="fe586-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="fe586-252">Ajout des cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fe586-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="fe586-253">Ajout des cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fe586-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe586-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fe586-255">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="fe586-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="fe586-256">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="fe586-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-257">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-258">Ajout du paramètre manquant -Mode à Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe586-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="fe586-259">Correction d’un bug de la cmdlet Get-AzureRmProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="fe586-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-260">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-261">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="fe586-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fe586-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-262">AzureRM.Storage</span></span>
* <span data-ttu-id="fe586-263">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="fe586-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="fe586-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="fe586-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-265">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-266">Nouvelle cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="fe586-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="fe586-267">Nouvelles cmdlets New-AzureRMWebAppContainerPSSession et Enter-WebAppContainerPSSession - démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="fe586-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="fe586-268">6.9.0 - septembre 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fe586-269">Généralités</span><span class="sxs-lookup"><span data-stu-id="fe586-269">General</span></span>
* <span data-ttu-id="fe586-270">AzureRM.SignalR a été ajouté au module Rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="fe586-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fe586-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-271">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-272">Modifications mineures du code commun de stockage</span><span class="sxs-lookup"><span data-stu-id="fe586-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="fe586-273">Mise à jour des fichiers d’aide pour inclure des types de paramètre complet.</span><span class="sxs-lookup"><span data-stu-id="fe586-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="fe586-274">Modification de -ServicePrincipal en non obligatoire dans l’ensemble de paramètres ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe586-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="fe586-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-275">Azure.Storage</span></span>
* <span data-ttu-id="fe586-276">Prise en charge du contexte de stockage avec OAuth.</span><span class="sxs-lookup"><span data-stu-id="fe586-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="fe586-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe586-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fe586-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe586-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="fe586-279">Ajout de Standard_Microsoft dans la référence SKU de tarification d’un CDN.</span><span class="sxs-lookup"><span data-stu-id="fe586-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-280">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-281">Déplacement des dépendances du coffre de clés et du stockage vers les dépendances communes</span><span class="sxs-lookup"><span data-stu-id="fe586-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="fe586-282">Ajout de la prise en charge de plus de tailles de machine virtuelle aux cmdlets AEM</span><span class="sxs-lookup"><span data-stu-id="fe586-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="fe586-283">Ajout du paramètre PublicIPPrefix à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="fe586-284">Ajout du paramètre ResourceId à la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="fe586-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="fe586-285">Ajout de la cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="fe586-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fe586-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fe586-286">AzureRM.Dns</span></span>
* <span data-ttu-id="fe586-287">Prise en charge de l’enregistrement d’alias pendant la création d’enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="fe586-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fe586-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fe586-288">AzureRM.Insights</span></span>
* <span data-ttu-id="fe586-289">Résolution des problèmes #6833 et #7102 (zone Paramètres de diagnostic)</span><span class="sxs-lookup"><span data-stu-id="fe586-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="fe586-290">Problèmes avec un nom par défaut, par exemple « service », lors de la création et l’obtention/le référencement des paramètres de diagnostic</span><span class="sxs-lookup"><span data-stu-id="fe586-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="fe586-291">Problèmes créant des paramètres de diagnostic avec des catégories</span><span class="sxs-lookup"><span data-stu-id="fe586-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="fe586-292">Ajout de message de désapprobation pour les paramètres de fragments de temps de métriques</span><span class="sxs-lookup"><span data-stu-id="fe586-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="fe586-293">Les paramètres Timegrains sont toujours acceptés (il s’agit d’une modification sans rupture,), mais ils sont ignorés dans le serveur principal dans la mesure où seul PT1M est valide</span><span class="sxs-lookup"><span data-stu-id="fe586-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-294">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-295">Modifications apportées aux cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fe586-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="fe586-296">LoadBalancerInboundNatPoolConfig : ajout des paramètres IdleTimeoutInMinutes, EnableFloatingIp et EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="fe586-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="fe586-297">LoadBalancerInboundNatRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="fe586-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="fe586-298">LoadBalancerRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="fe586-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="fe586-299">LoadBalancerProbeConfig : ajout d’une prise en charge de la valeur « Https » pour le paramètre Protocole</span><span class="sxs-lookup"><span data-stu-id="fe586-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="fe586-300">Ajout de nouvelles commandes pour la sous-ressource OutboundRule du nouveau LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fe586-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="fe586-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fe586-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fe586-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fe586-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="fe586-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="fe586-306">Ajout d’une nouvelle propriété HostedWorkloads pour PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fe586-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="fe586-307">Ajout de nouvelles applets de commande pour la fonctionnalité : Pare-feu Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="fe586-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="fe586-308">Ajout de Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe586-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="fe586-309">Ajout de Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe586-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="fe586-310">Ajout de New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe586-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="fe586-311">Ajout de Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe586-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="fe586-312">Ajout de New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fe586-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="fe586-313">Ajout de New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="fe586-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="fe586-314">Ajout de New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fe586-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="fe586-315">Ajout de New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="fe586-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="fe586-316">Ajout de New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="fe586-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="fe586-317">Ajout de New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fe586-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="fe586-318">Ajout de la prise en charge du certificat racine approuvé et de la configuration de mise à l’échelle automatique dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fe586-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="fe586-319">Nouvelles cmdlets ajoutées :</span><span class="sxs-lookup"><span data-stu-id="fe586-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="fe586-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fe586-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fe586-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fe586-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fe586-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="fe586-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="fe586-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="fe586-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="fe586-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="fe586-329">Cmdlets mises à jour avec le paramètre facultatif -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="fe586-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe586-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="fe586-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe586-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="fe586-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fe586-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="fe586-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="fe586-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="fe586-334">Cmdlets mises à jour avec le paramètre facultatif -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="fe586-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe586-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="fe586-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe586-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="fe586-337">Ajout d’une cmdlet pour le point de terminaison d’interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe586-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="fe586-338">Ajout de la prise en charge de plusieurs préfixes d’adresse dans un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="fe586-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="fe586-339">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="fe586-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="fe586-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fe586-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fe586-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fe586-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="fe586-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="fe586-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="fe586-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="fe586-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="fe586-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="fe586-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="fe586-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="fe586-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="fe586-352">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="fe586-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="fe586-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="fe586-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="fe586-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="fe586-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="fe586-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fe586-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="fe586-359">Ajout de cmdlets pour la délégation de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="fe586-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="fe586-360">New-AzureRmDelegation : Crée une délégation, pouvant être ajoutée à un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="fe586-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="fe586-361">Remove-AzureRmDelegation : Accepte un sous-réseau et supprime le nom de délégation fourni de ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="fe586-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="fe586-362">Add-AzureRmDelegation : Accepte un sous-réseau et ajoute le nom de service fourni en tant que délégation à ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="fe586-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="fe586-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="fe586-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="fe586-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="fe586-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fe586-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fe586-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fe586-366">Prise en charge de la gestion de disque managé</span><span class="sxs-lookup"><span data-stu-id="fe586-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fe586-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe586-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fe586-368">Mise à jour de la dépendance Insights.</span><span class="sxs-lookup"><span data-stu-id="fe586-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-369">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-370">Mise à jour de New-AzureRmResourceGroupDeployment avec le nouveau paramètre RollbackAction</span><span class="sxs-lookup"><span data-stu-id="fe586-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="fe586-371">Ajout de la prise en charge d’OnErrorDeployment avec le nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="fe586-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="fe586-372">Prise en charge des identités managées sur les affectations de stratégies.</span><span class="sxs-lookup"><span data-stu-id="fe586-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="fe586-373">Des paramètres avec des valeurs par défaut ne sont plus requis lors de l’affectation d’une stratégie avec « New-AzureRmPolicyAssignment »</span><span class="sxs-lookup"><span data-stu-id="fe586-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="fe586-374">Ajout de la nouvelle cmdlet Get-AzureRmPolicyAlias pour récupérer les alias de stratégie</span><span class="sxs-lookup"><span data-stu-id="fe586-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-376">Résolution du problème #7161</span><span class="sxs-lookup"><span data-stu-id="fe586-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="fe586-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="fe586-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="fe586-378">Mise à jour des noms de référence SKU en Free_F1 et Standard_S1</span><span class="sxs-lookup"><span data-stu-id="fe586-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="fe586-379">Ajout d’un champ de version à l’objet PSSignalRResource et d’une chaîne de connexion à l’objet PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="fe586-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fe586-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-380">AzureRM.Storage</span></span>
* <span data-ttu-id="fe586-381">Prise en charge de la stratégie d’immuabilité dans AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="fe586-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fe586-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="fe586-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe586-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fe586-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe586-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fe586-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe586-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fe586-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fe586-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="fe586-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fe586-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="fe586-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fe586-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="fe586-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="fe586-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="fe586-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="fe586-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-393">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-394">Ajout de deux nouvelles applets de commande : Get-AzureRmDeletedWebApp et Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="fe586-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="fe586-395">New-AzureRmAppServicePlan : le commutateur HyperV est ajouté pour créer un plan App Service avec conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="fe586-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="fe586-396">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot : les nouveaux paramètres (la chaîne -ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) ajoutés pour créer et gérer l’application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="fe586-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="fe586-397">6.8.1 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fe586-398">Généralités</span><span class="sxs-lookup"><span data-stu-id="fe586-398">General</span></span>
* <span data-ttu-id="fe586-399">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="fe586-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="fe586-400">Mise à jour des assemblys de runtime courants</span><span class="sxs-lookup"><span data-stu-id="fe586-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fe586-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe586-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fe586-402">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="fe586-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="fe586-403">Problème résolu https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="fe586-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="fe586-404">Les cmdlets Import-AzureRmApiManagementApi et \*-AzureRmApiManagementCertificate peuvent maintenant gérer les chemins d’accès relatifs</span><span class="sxs-lookup"><span data-stu-id="fe586-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="fe586-405">Problème résolu https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="fe586-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="fe586-406">CertificateInformation est une propriété définissable permettant à la cmdlet Set-AzureRmApiManagement de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="fe586-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="fe586-407">Résolu en passant au nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="fe586-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="fe586-408">Problème résolu https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="fe586-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="fe586-409">Recherche par nom sur produit du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="fe586-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="fe586-410">Problème résolu https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="fe586-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="fe586-411">Recherche par nom sur Api du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="fe586-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="fe586-412">Ajout de la prise en charge de l’enregistreur d'événements AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="fe586-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="fe586-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-413">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-414">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fe586-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="fe586-415">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="fe586-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="fe586-416">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="fe586-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="fe586-417">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="fe586-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-418">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-419">Modification de la présentation d’une sortie de cmdlet par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="fe586-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fe586-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fe586-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fe586-421">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="fe586-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="fe586-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-422">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-423">Résolution du problème de création d’applications managées depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fe586-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-425">Problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="fe586-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fe586-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fe586-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fe586-427">Ajout de la prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="fe586-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="fe586-428">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="fe586-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="fe586-429">Ajout de la prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="fe586-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="fe586-430">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="fe586-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="fe586-431">Ajout de la prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="fe586-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="fe586-432">Ajout de la prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="fe586-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="fe586-433">Ajout de la prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="fe586-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="fe586-434">6.8.0 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fe586-435">Généralités</span><span class="sxs-lookup"><span data-stu-id="fe586-435">General</span></span>
* <span data-ttu-id="fe586-436">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="fe586-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fe586-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-437">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-438">Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="fe586-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-439">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-440">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fe586-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="fe586-441">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="fe586-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="fe586-442">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="fe586-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fe586-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe586-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="fe586-444">Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="fe586-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-445">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-446">Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="fe586-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fe586-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fe586-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fe586-448">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="fe586-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-449">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-450">Résolution du problème de création d’application managée depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fe586-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-452">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="fe586-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fe586-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fe586-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fe586-454">Prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="fe586-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="fe586-455">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="fe586-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="fe586-456">Prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="fe586-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="fe586-457">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="fe586-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="fe586-458">Prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="fe586-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="fe586-459">Prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="fe586-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="fe586-460">Prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="fe586-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-461">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-462">Résolution du problème relatif aux groupes de ressources par défaut mal définis.</span><span class="sxs-lookup"><span data-stu-id="fe586-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="fe586-463">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-464">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-465">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fe586-466">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="fe586-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="fe586-467">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="fe586-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="fe586-468">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="fe586-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="fe586-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-469">Azure.Storage</span></span>
* <span data-ttu-id="fe586-470">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="fe586-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="fe586-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="fe586-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fe586-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe586-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fe586-473">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="fe586-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe586-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="fe586-475">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fe586-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe586-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fe586-477">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="fe586-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fe586-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="fe586-479">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fe586-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fe586-480">AzureRM.Automation</span></span>
* <span data-ttu-id="fe586-481">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="fe586-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-482">AzureRM.Backup</span></span>
* <span data-ttu-id="fe586-483">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fe586-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fe586-484">AzureRM.Batch</span></span>
* <span data-ttu-id="fe586-485">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="fe586-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="fe586-486">AzureRM.Billing</span></span>
* <span data-ttu-id="fe586-487">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fe586-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fe586-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="fe586-489">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fe586-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fe586-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fe586-491">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-492">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-493">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fe586-494">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="fe586-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="fe586-495">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="fe586-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="fe586-496">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="fe586-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="fe586-497">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="fe586-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="fe586-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="fe586-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="fe586-499">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fe586-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fe586-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fe586-501">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="fe586-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe586-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="fe586-503">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="fe586-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="fe586-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="fe586-505">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fe586-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fe586-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fe586-507">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fe586-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fe586-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fe586-509">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fe586-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe586-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fe586-511">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe586-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="fe586-512">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="fe586-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="fe586-513">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fe586-514">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="fe586-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="fe586-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fe586-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="fe586-516">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fe586-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fe586-517">AzureRM.Dns</span></span>
* <span data-ttu-id="fe586-518">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fe586-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fe586-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fe586-520">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fe586-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe586-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="fe586-522">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="fe586-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fe586-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="fe586-524">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fe586-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fe586-525">AzureRM.Insights</span></span>
* <span data-ttu-id="fe586-526">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fe586-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fe586-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="fe586-528">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fe586-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe586-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fe586-530">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fe586-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fe586-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fe586-532">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="fe586-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fe586-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="fe586-534">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="fe586-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="fe586-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="fe586-536">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="fe586-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fe586-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="fe586-538">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="fe586-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="fe586-539">AzureRM.Media</span></span>
* <span data-ttu-id="fe586-540">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-541">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-542">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fe586-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="fe586-543">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="fe586-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fe586-544">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="fe586-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="fe586-545">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="fe586-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="fe586-546">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="fe586-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="fe586-547">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="fe586-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fe586-548">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="fe586-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="fe586-549">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="fe586-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="fe586-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fe586-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="fe586-551">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="fe586-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe586-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fe586-553">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fe586-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe586-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fe586-555">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fe586-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fe586-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fe586-557">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="fe586-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fe586-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="fe586-559">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fe586-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fe586-561">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="fe586-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="fe586-562">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="fe586-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="fe586-563">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="fe586-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="fe586-564">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fe586-565">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="fe586-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="fe586-566">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="fe586-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="fe586-567">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="fe586-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fe586-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fe586-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fe586-569">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fe586-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fe586-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fe586-571">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fe586-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fe586-572">AzureRM.Relay</span></span>
* <span data-ttu-id="fe586-573">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-574">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-575">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe586-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="fe586-576">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="fe586-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="fe586-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="fe586-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="fe586-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="fe586-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="fe586-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="fe586-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="fe586-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="fe586-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="fe586-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="fe586-584">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="fe586-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="fe586-585">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="fe586-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="fe586-586">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fe586-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fe586-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fe586-588">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-590">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fe586-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe586-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fe586-592">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-593">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-594">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fe586-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-595">AzureRM.Storage</span></span>
* <span data-ttu-id="fe586-596">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="fe586-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="fe586-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="fe586-598">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="fe586-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="fe586-599">AzureRM.Tags</span></span>
* <span data-ttu-id="fe586-600">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fe586-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fe586-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fe586-602">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="fe586-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="fe586-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="fe586-604">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-605">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-606">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="fe586-607">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fe586-608">Généralités</span><span class="sxs-lookup"><span data-stu-id="fe586-608">General</span></span>
* <span data-ttu-id="fe586-609">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="fe586-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fe586-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-610">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-611">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="fe586-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="fe586-612">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fe586-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-613">Azure.Storage</span></span>
* <span data-ttu-id="fe586-614">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="fe586-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="fe586-615">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fe586-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fe586-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe586-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fe586-617">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="fe586-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="fe586-618">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="fe586-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="fe586-619">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="fe586-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="fe586-620">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="fe586-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="fe586-621">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="fe586-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="fe586-622">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="fe586-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-623">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-624">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="fe586-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="fe586-625">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="fe586-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="fe586-626">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe586-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="fe586-627">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="fe586-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="fe586-628">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="fe586-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="fe586-629">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="fe586-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="fe586-630">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="fe586-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="fe586-631">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="fe586-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="fe586-632">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="fe586-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="fe586-633">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="fe586-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fe586-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fe586-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fe586-635">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="fe586-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="fe586-636">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="fe586-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="fe586-637">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="fe586-638">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="fe586-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fe586-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe586-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fe586-640">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="fe586-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fe586-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe586-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="fe586-642">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="fe586-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fe586-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fe586-643">AzureRM.Insights</span></span>
* <span data-ttu-id="fe586-644">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="fe586-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="fe586-645">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="fe586-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fe586-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe586-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fe586-647">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-648">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-649">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="fe586-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-650">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-651">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="fe586-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="fe586-652">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="fe586-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-654">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="fe586-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="fe586-655">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="fe586-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="fe586-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-656">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-657">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe586-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="fe586-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="fe586-659">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe586-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="fe586-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="fe586-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="fe586-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="fe586-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="fe586-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="fe586-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="fe586-663">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fe586-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="fe586-664">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="fe586-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fe586-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-665">AzureRM.Storage</span></span>
* <span data-ttu-id="fe586-666">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="fe586-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="fe586-667">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="fe586-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="fe586-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe586-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fe586-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe586-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fe586-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe586-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="fe586-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="fe586-671">AzureRM.Tags</span></span>
* <span data-ttu-id="fe586-672">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="fe586-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="fe586-673">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-674">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-675">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="fe586-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fe586-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-676">Azure.Storage</span></span>
* <span data-ttu-id="fe586-677">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="fe586-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="fe586-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fe586-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="fe586-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fe586-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fe586-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe586-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fe586-681">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="fe586-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fe586-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fe586-682">AzureRM.Automation</span></span>
* <span data-ttu-id="fe586-683">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="fe586-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-684">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-685">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe586-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="fe586-686">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="fe586-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="fe586-687">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="fe586-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="fe586-688">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="fe586-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="fe586-689">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="fe586-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fe586-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe586-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="fe586-691">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="fe586-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fe586-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe586-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fe586-693">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fe586-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fe586-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fe586-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fe586-695">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fe586-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-696">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-697">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fe586-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="fe586-698">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fe586-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="fe586-699">New-AzureRmApplicationGateway : Ajout d’un indicateur EnableFIPS et prise en charge de Zones</span><span class="sxs-lookup"><span data-stu-id="fe586-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="fe586-700">New-AzureRmApplicationGatewaySku : Ajout de nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="fe586-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="fe586-701">Set-AzureRmApplicationGatewaySku : Ajout de nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="fe586-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="fe586-702">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="fe586-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fe586-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fe586-703">AzureRM.Relay</span></span>
* <span data-ttu-id="fe586-704">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="fe586-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-705">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-706">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="fe586-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="fe586-707">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="fe586-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="fe586-708">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fe586-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="fe586-709">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="fe586-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="fe586-710">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="fe586-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-712">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="fe586-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="fe586-713">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="fe586-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="fe586-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fe586-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fe586-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fe586-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fe586-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fe586-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fe586-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fe586-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fe586-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fe586-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="fe586-719">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="fe586-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fe586-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe586-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fe586-721">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="fe586-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-722">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-723">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="fe586-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="fe586-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="fe586-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-726">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-727">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="fe586-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="fe586-728">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="fe586-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="fe586-729">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="fe586-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="fe586-730">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fe586-731">Généralités</span><span class="sxs-lookup"><span data-stu-id="fe586-731">General</span></span>
* <span data-ttu-id="fe586-732">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="fe586-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fe586-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-733">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-734">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="fe586-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-735">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-736">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="fe586-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="fe586-737">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="fe586-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="fe586-738">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="fe586-739">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="fe586-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="fe586-740">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="fe586-741">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="fe586-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="fe586-742">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fe586-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fe586-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fe586-744">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe586-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="fe586-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fe586-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="fe586-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fe586-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="fe586-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fe586-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fe586-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe586-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fe586-749">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fe586-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="fe586-750">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="fe586-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="fe586-751">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="fe586-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="fe586-752">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="fe586-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fe586-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fe586-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="fe586-754">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fe586-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="fe586-755">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="fe586-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="fe586-756">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="fe586-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="fe586-757">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="fe586-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fe586-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe586-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fe586-759">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="fe586-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-760">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-761">Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone</span><span class="sxs-lookup"><span data-stu-id="fe586-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="fe586-762">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="fe586-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="fe586-763">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fe586-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="fe586-764">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="fe586-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="fe586-765">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="fe586-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fe586-766">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="fe586-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fe586-767">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="fe586-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fe586-768">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="fe586-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fe586-769">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="fe586-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fe586-770">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="fe586-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fe586-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fe586-772">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="fe586-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="fe586-773">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="fe586-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="fe586-774">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="fe586-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-775">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-776">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="fe586-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="fe586-777">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="fe586-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="fe586-778">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="fe586-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="fe586-779">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="fe586-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="fe586-780">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe586-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="fe586-781">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="fe586-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="fe586-782">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="fe586-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="fe586-783">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="fe586-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="fe586-784">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="fe586-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="fe586-785">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="fe586-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="fe586-786">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="fe586-787">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fe586-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="fe586-788">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="fe586-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="fe586-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fe586-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fe586-790">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="fe586-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-791">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-792">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="fe586-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="fe586-793">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="fe586-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="fe586-794">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-795">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-796">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="fe586-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="fe586-797">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="fe586-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fe586-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fe586-798">Azure.Storage</span></span>
* <span data-ttu-id="fe586-799">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="fe586-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-800">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-801">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="fe586-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="fe586-802">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="fe586-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="fe586-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fe586-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="fe586-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fe586-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="fe586-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fe586-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="fe586-806">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="fe586-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="fe586-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fe586-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="fe586-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fe586-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="fe586-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fe586-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="fe586-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fe586-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="fe586-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="fe586-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="fe586-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="fe586-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fe586-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="fe586-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="fe586-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="fe586-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="fe586-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="fe586-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="fe586-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe586-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="fe586-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="fe586-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="fe586-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fe586-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="fe586-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="fe586-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="fe586-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fe586-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="fe586-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="fe586-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="fe586-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fe586-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="fe586-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe586-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fe586-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fe586-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fe586-827">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fe586-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fe586-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe586-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fe586-829">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="fe586-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fe586-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fe586-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fe586-831">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="fe586-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="fe586-832">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="fe586-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="fe586-833">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="fe586-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fe586-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fe586-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fe586-835">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="fe586-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="fe586-836">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="fe586-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-837">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-838">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="fe586-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fe586-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fe586-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fe586-840">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-841">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-842">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fe586-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="fe586-843">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fe586-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="fe586-844">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="fe586-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fe586-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fe586-846">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="fe586-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="fe586-847">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-848">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-849">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="fe586-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fe586-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fe586-850">AzureRM.Compute</span></span>
* <span data-ttu-id="fe586-851">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="fe586-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="fe586-852">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="fe586-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="fe586-853">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="fe586-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fe586-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fe586-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fe586-855">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe586-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="fe586-856">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="fe586-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="fe586-857">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="fe586-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="fe586-858">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="fe586-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="fe586-859">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="fe586-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="fe586-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fe586-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fe586-861">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="fe586-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="fe586-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-862">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-863">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="fe586-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fe586-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fe586-864">AzureRM.Resources</span></span>
* <span data-ttu-id="fe586-865">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="fe586-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fe586-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fe586-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fe586-867">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="fe586-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="fe586-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-868">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-869">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="fe586-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="fe586-870">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fe586-871">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fe586-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fe586-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fe586-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="fe586-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fe586-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="fe586-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fe586-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fe586-875">AzureRM.Websites</span></span>
* <span data-ttu-id="fe586-876">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="fe586-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="fe586-877">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="fe586-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fe586-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="fe586-878">AzureRM.Profile</span></span>
* <span data-ttu-id="fe586-879">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="fe586-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fe586-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fe586-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fe586-881">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="fe586-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fe586-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe586-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fe586-883">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="fe586-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="fe586-884">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe586-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="fe586-885">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="fe586-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="fe586-886">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="fe586-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="fe586-887">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="fe586-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="fe586-888">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="fe586-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="fe586-889">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="fe586-889">Added support for MSI identity</span></span>
* <span data-ttu-id="fe586-890">Ajout de la prise en charge des stratégies par le biais d’une URL REMARQUE : Les applets de commande suivantes seront dépréciées dans une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="fe586-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="fe586-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="fe586-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="fe586-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="fe586-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="fe586-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="fe586-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fe586-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fe586-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fe586-895">AzureRM.Batch</span></span>
* <span data-ttu-id="fe586-896">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="fe586-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="fe586-897">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="fe586-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="fe586-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="fe586-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="fe586-899">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="fe586-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fe586-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fe586-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fe586-901">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="fe586-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="fe586-902">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fe586-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="fe586-903">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fe586-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="fe586-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fe586-904">AzureRM.Network</span></span>
* <span data-ttu-id="fe586-905">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="fe586-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="fe586-906">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="fe586-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="fe586-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe586-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="fe586-908">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="fe586-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="fe586-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="fe586-910">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="fe586-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="fe586-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="fe586-912">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="fe586-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="fe586-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fe586-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fe586-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fe586-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fe586-915">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="fe586-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fe586-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fe586-916">AzureRM.Sql</span></span>
* <span data-ttu-id="fe586-917">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="fe586-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="fe586-918">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="fe586-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="fe586-919">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="fe586-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="fe586-920">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="fe586-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="fe586-921">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="fe586-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="fe586-922">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fe586-923">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fe586-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fe586-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fe586-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="fe586-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fe586-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="fe586-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fe586-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fe586-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fe586-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fe586-928">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="fe586-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
