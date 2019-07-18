---
ms.openlocfilehash: f357a17f698d68c1a29dcb78f83671973fd6ecad
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863740"
---
## <a name="240---july-2019"></a><span data-ttu-id="2db92-101">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-102">Az.Accounts</span></span>
* <span data-ttu-id="2db92-103">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="2db92-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2db92-104">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="2db92-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2db92-105">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2db92-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2db92-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2db92-106">Az.Advisor</span></span>
* <span data-ttu-id="2db92-107">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2db92-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2db92-108">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="2db92-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2db92-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2db92-109">Az.ApiManagement</span></span>
* <span data-ttu-id="2db92-110">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2db92-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2db92-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2db92-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2db92-112">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="2db92-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2db92-113">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="2db92-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2db92-114">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2db92-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2db92-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2db92-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2db92-116">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="2db92-116">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-117">Az.Automation</span></span>
* <span data-ttu-id="2db92-118">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="2db92-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-119">Az.Compute</span></span>
* <span data-ttu-id="2db92-120">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2db92-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2db92-121">Az.DataFactory</span></span>
* <span data-ttu-id="2db92-122">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="2db92-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2db92-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2db92-123">Az.EventGrid</span></span>
* <span data-ttu-id="2db92-124">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="2db92-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2db92-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2db92-125">Az.IotHub</span></span>
* <span data-ttu-id="2db92-126">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="2db92-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-127">Az.Network</span></span>
* <span data-ttu-id="2db92-128">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="2db92-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2db92-129">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="2db92-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2db92-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="2db92-131">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2db92-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2db92-132">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2db92-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2db92-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="2db92-134">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2db92-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-136">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="2db92-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-137">Az.Resources</span></span>
    - <span data-ttu-id="2db92-138">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2db92-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2db92-139">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="2db92-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2db92-140">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="2db92-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2db92-141">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="2db92-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2db92-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2db92-142">Az.ServiceBus</span></span>
* <span data-ttu-id="2db92-143">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2db92-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-144">Az.Sql</span></span>
* <span data-ttu-id="2db92-145">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="2db92-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2db92-146">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="2db92-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2db92-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2db92-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2db92-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2db92-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2db92-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2db92-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2db92-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2db92-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2db92-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2db92-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2db92-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2db92-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2db92-153">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="2db92-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-154">Az.Storage</span></span>
* <span data-ttu-id="2db92-155">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="2db92-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2db92-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2db92-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2db92-157">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="2db92-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2db92-158">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="2db92-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2db92-159">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="2db92-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2db92-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2db92-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2db92-162">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="2db92-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2db92-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2db92-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2db92-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2db92-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2db92-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2db92-165">Az.StorageSync</span></span>
* <span data-ttu-id="2db92-166">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="2db92-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2db92-167">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-168">Az.Accounts</span></span>
* <span data-ttu-id="2db92-169">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="2db92-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2db92-170">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2db92-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2db92-171">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="2db92-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2db92-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2db92-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2db92-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2db92-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-174">Az.Compute</span></span>
* <span data-ttu-id="2db92-175">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="2db92-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2db92-176">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="2db92-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2db92-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2db92-177">Az.Dns</span></span>
* <span data-ttu-id="2db92-178">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="2db92-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2db92-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2db92-179">Az.EventGrid</span></span>
* <span data-ttu-id="2db92-180">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2db92-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2db92-181">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="2db92-181">New cmdlets:</span></span>
    - <span data-ttu-id="2db92-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2db92-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2db92-183">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="2db92-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2db92-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2db92-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2db92-185">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="2db92-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2db92-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2db92-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2db92-187">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="2db92-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2db92-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2db92-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2db92-189">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="2db92-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2db92-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2db92-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2db92-191">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="2db92-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2db92-192">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2db92-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2db92-193">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="2db92-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2db92-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2db92-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2db92-195">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="2db92-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="2db92-196">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2db92-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2db92-197">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="2db92-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2db92-198">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="2db92-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="2db92-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2db92-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2db92-200">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="2db92-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2db92-201">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="2db92-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2db92-202">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="2db92-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2db92-203">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="2db92-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2db92-204">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="2db92-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2db92-205">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="2db92-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2db92-206">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="2db92-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2db92-207">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="2db92-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="2db92-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="2db92-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2db92-209">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="2db92-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2db92-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2db92-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2db92-211">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="2db92-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2db92-212">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="2db92-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2db92-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2db92-213">Az.FrontDoor</span></span>
* <span data-ttu-id="2db92-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2db92-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2db92-215">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="2db92-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2db92-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2db92-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2db92-217">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="2db92-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-218">Az.Network</span></span>
* <span data-ttu-id="2db92-219">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2db92-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2db92-220">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-220">New cmdlets</span></span>
        - <span data-ttu-id="2db92-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2db92-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2db92-222">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2db92-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2db92-223">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-223">New cmdlets</span></span> 
        - <span data-ttu-id="2db92-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2db92-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2db92-225">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2db92-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2db92-226">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-226">New cmdlets</span></span> 
        - <span data-ttu-id="2db92-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2db92-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="2db92-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2db92-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2db92-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2db92-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2db92-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2db92-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2db92-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2db92-232">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2db92-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2db92-233">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-233">New cmdlets</span></span>
        - <span data-ttu-id="2db92-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2db92-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2db92-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2db92-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2db92-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2db92-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2db92-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2db92-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2db92-238">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2db92-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2db92-239">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="2db92-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2db92-240">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="2db92-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2db92-241">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2db92-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2db92-242">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2db92-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2db92-243">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2db92-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2db92-244">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2db92-245">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="2db92-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2db92-246">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2db92-247">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="2db92-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2db92-248">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2db92-249">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2db92-250">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2db92-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2db92-251">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="2db92-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2db92-252">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="2db92-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2db92-253">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="2db92-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2db92-254">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2db92-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2db92-255">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="2db92-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2db92-256">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2db92-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="2db92-257">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2db92-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="2db92-258">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="2db92-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2db92-259">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="2db92-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2db92-260">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="2db92-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2db92-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="2db92-262">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="2db92-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-263">Az.Resources</span></span>
* <span data-ttu-id="2db92-264">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="2db92-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2db92-265">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2db92-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2db92-266">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2db92-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2db92-267">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="2db92-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2db92-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2db92-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="2db92-269">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-270">Az.Sql</span></span>
* <span data-ttu-id="2db92-271">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2db92-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2db92-272">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="2db92-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2db92-273">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="2db92-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2db92-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2db92-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2db92-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2db92-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2db92-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2db92-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2db92-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2db92-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2db92-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2db92-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-279">Az.Storage</span></span>
* <span data-ttu-id="2db92-280">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="2db92-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2db92-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="2db92-282">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="2db92-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2db92-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-284">Az.Websites</span></span>
* <span data-ttu-id="2db92-285">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="2db92-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2db92-286">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2db92-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2db92-287">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2db92-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2db92-288">Az.Cdn</span></span>
* <span data-ttu-id="2db92-289">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="2db92-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-290">Az.Compute</span></span>
* <span data-ttu-id="2db92-291">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2db92-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2db92-292">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2db92-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2db92-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2db92-293">Az.EventHub</span></span>
* <span data-ttu-id="2db92-294">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="2db92-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2db92-295">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db92-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-296">Az.Network</span></span>
* <span data-ttu-id="2db92-297">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="2db92-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2db92-298">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="2db92-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2db92-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="2db92-300">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2db92-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-302">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="2db92-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2db92-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2db92-303">Az.ServiceBus</span></span>
* <span data-ttu-id="2db92-304">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2db92-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2db92-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2db92-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="2db92-306">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="2db92-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2db92-307">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2db92-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-308">Az.Sql</span></span>
* <span data-ttu-id="2db92-309">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="2db92-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2db92-310">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2db92-311">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="2db92-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2db92-312">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="2db92-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-313">Az.Websites</span></span>
* <span data-ttu-id="2db92-314">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="2db92-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2db92-315">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2db92-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2db92-316">Az.ApiManagement</span></span>
* <span data-ttu-id="2db92-317">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2db92-318">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2db92-319">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2db92-320">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="2db92-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2db92-321">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="2db92-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2db92-322">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="2db92-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2db92-323">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2db92-324">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2db92-325">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="2db92-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2db92-326">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="2db92-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2db92-327">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="2db92-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2db92-328">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="2db92-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2db92-329">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="2db92-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2db92-330">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="2db92-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2db92-331">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="2db92-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2db92-332">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2db92-333">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2db92-334">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="2db92-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2db92-335">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2db92-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="2db92-336">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="2db92-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2db92-337">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="2db92-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2db92-338">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="2db92-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2db92-339">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="2db92-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2db92-340">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="2db92-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="2db92-341">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="2db92-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2db92-342">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="2db92-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2db92-343">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="2db92-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2db92-344">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="2db92-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2db92-345">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="2db92-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2db92-346">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="2db92-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2db92-347">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="2db92-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="2db92-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2db92-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2db92-349">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="2db92-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2db92-350">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2db92-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2db92-351">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="2db92-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2db92-352">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="2db92-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2db92-353">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="2db92-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2db92-354">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="2db92-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2db92-355">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="2db92-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2db92-356">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2db92-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="2db92-357">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="2db92-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2db92-358">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="2db92-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2db92-359">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="2db92-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2db92-360">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="2db92-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2db92-361">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2db92-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2db92-362">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="2db92-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2db92-363">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="2db92-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="2db92-364">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="2db92-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="2db92-365">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="2db92-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2db92-366">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="2db92-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2db92-367">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="2db92-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2db92-368">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="2db92-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2db92-369">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="2db92-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2db92-370">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="2db92-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2db92-371">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="2db92-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2db92-372">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="2db92-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2db92-373">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2db92-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2db92-374">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="2db92-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2db92-375">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="2db92-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2db92-376">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="2db92-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2db92-377">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2db92-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2db92-378">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="2db92-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2db92-379">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="2db92-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2db92-380">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="2db92-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2db92-381">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="2db92-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2db92-382">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="2db92-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2db92-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2db92-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2db92-384">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="2db92-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2db92-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2db92-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2db92-386">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="2db92-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2db92-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2db92-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2db92-388">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="2db92-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2db92-389">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="2db92-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2db92-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2db92-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2db92-391">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="2db92-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="2db92-392">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="2db92-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2db92-393">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="2db92-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-394">Az.Automation</span></span>
* <span data-ttu-id="2db92-395">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="2db92-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2db92-396">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2db92-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2db92-397">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2db92-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2db92-398">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="2db92-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2db92-399">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2db92-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2db92-400">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="2db92-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2db92-401">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="2db92-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-402">Az.Compute</span></span>
* <span data-ttu-id="2db92-403">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2db92-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2db92-404">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2db92-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-406">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="2db92-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2db92-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2db92-407">Az.Monitor</span></span>
* <span data-ttu-id="2db92-408">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="2db92-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-409">Az.Network</span></span>
* <span data-ttu-id="2db92-410">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="2db92-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2db92-411">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="2db92-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="2db92-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db92-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2db92-413">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2db92-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-414">Az.Resources</span></span>
* <span data-ttu-id="2db92-415">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="2db92-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-416">Az.Sql</span></span>
* <span data-ttu-id="2db92-417">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="2db92-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2db92-418">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-419">Az.Accounts</span></span>
* <span data-ttu-id="2db92-420">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="2db92-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2db92-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2db92-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="2db92-422">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="2db92-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2db92-423">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="2db92-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-424">Az.Compute</span></span>
* <span data-ttu-id="2db92-425">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="2db92-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2db92-426">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2db92-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2db92-427">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2db92-428">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2db92-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2db92-429">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2db92-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2db92-430">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2db92-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="2db92-431">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="2db92-431">Breaking changes</span></span>
    - <span data-ttu-id="2db92-432">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2db92-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2db92-433">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2db92-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2db92-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2db92-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="2db92-435">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="2db92-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2db92-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2db92-436">Az.Dns</span></span>
* <span data-ttu-id="2db92-437">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="2db92-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2db92-438">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="2db92-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2db92-439">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="2db92-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2db92-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2db92-440">Az.FrontDoor</span></span>
* <span data-ttu-id="2db92-441">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2db92-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2db92-442">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="2db92-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2db92-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2db92-443">Az.HDInsight</span></span>
* <span data-ttu-id="2db92-444">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="2db92-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2db92-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2db92-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2db92-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2db92-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2db92-447">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2db92-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2db92-448">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="2db92-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2db92-449">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="2db92-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2db92-450">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="2db92-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2db92-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2db92-451">Az.Monitor</span></span>
* <span data-ttu-id="2db92-452">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="2db92-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="2db92-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2db92-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2db92-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2db92-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2db92-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2db92-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2db92-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2db92-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2db92-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2db92-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2db92-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2db92-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2db92-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2db92-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2db92-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2db92-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2db92-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2db92-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2db92-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2db92-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2db92-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2db92-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2db92-464">[Plus d’informations](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="2db92-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2db92-465">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="2db92-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-466">Az.Network</span></span>
* <span data-ttu-id="2db92-467">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="2db92-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2db92-468">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-468">New cmdlets</span></span>
        - <span data-ttu-id="2db92-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="2db92-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2db92-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2db92-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2db92-473">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="2db92-473">Updated cmdlets</span></span>
        - <span data-ttu-id="2db92-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2db92-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2db92-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2db92-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2db92-476">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="2db92-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2db92-477">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="2db92-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2db92-478">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="2db92-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2db92-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="2db92-480">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2db92-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2db92-481">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2db92-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2db92-482">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="2db92-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-484">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="2db92-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2db92-485">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2db92-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2db92-486">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2db92-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2db92-487">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2db92-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2db92-488">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="2db92-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2db92-489">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="2db92-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2db92-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2db92-490">Az.Relay</span></span>
* <span data-ttu-id="2db92-491">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="2db92-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2db92-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2db92-492">Az.ServiceBus</span></span>
* <span data-ttu-id="2db92-493">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="2db92-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-494">Az.Storage</span></span>
* <span data-ttu-id="2db92-495">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="2db92-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2db92-496">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="2db92-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2db92-497">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="2db92-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2db92-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="2db92-499">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="2db92-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2db92-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2db92-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2db92-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-503">Az.Websites</span></span>
* <span data-ttu-id="2db92-504">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2db92-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2db92-505">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="2db92-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2db92-506">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2db92-507">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="2db92-507">Highlights since the last major release</span></span>
* <span data-ttu-id="2db92-508">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="2db92-508">General availability of `Az` module</span></span>
* <span data-ttu-id="2db92-509">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2db92-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2db92-510">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2db92-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2db92-511">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2db92-512">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="2db92-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2db92-513">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2db92-514">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="2db92-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2db92-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-515">Az.Accounts</span></span>
* <span data-ttu-id="2db92-516">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="2db92-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2db92-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2db92-517">Az.Batch</span></span>
* <span data-ttu-id="2db92-518">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2db92-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2db92-519">Az.Cdn</span></span>
* <span data-ttu-id="2db92-520">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2db92-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2db92-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="2db92-522">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-523">Az.Compute</span></span>
* <span data-ttu-id="2db92-524">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="2db92-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2db92-525">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2db92-526">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="2db92-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2db92-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2db92-527">Az.DataFactory</span></span>
* <span data-ttu-id="2db92-528">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="2db92-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-530">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2db92-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2db92-531">Az.EventGrid</span></span>
* <span data-ttu-id="2db92-532">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="2db92-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2db92-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2db92-533">Az.EventHub</span></span>
* <span data-ttu-id="2db92-534">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="2db92-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="2db92-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2db92-535">Az.HDInsight</span></span>
* <span data-ttu-id="2db92-536">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2db92-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2db92-537">Az.IotHub</span></span>
* <span data-ttu-id="2db92-538">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2db92-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-539">Az.KeyVault</span></span>
* <span data-ttu-id="2db92-540">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2db92-541">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="2db92-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2db92-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2db92-542">Az.MachineLearning</span></span>
* <span data-ttu-id="2db92-543">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2db92-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2db92-544">Az.Media</span></span>
* <span data-ttu-id="2db92-545">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2db92-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2db92-546">Az.Monitor</span></span>
  * <span data-ttu-id="2db92-547">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="2db92-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2db92-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2db92-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2db92-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2db92-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2db92-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2db92-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2db92-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2db92-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2db92-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2db92-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2db92-553">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="2db92-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-554">Az.Network</span></span>
* <span data-ttu-id="2db92-555">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2db92-556">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="2db92-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2db92-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2db92-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="2db92-558">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2db92-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="2db92-560">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2db92-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2db92-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2db92-562">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-564">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2db92-565">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="2db92-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2db92-566">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="2db92-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2db92-567">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="2db92-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2db92-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2db92-568">Az.RedisCache</span></span>
* <span data-ttu-id="2db92-569">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-570">Az.Resources</span></span>
* <span data-ttu-id="2db92-571">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="2db92-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-572">Az.Sql</span></span>
* <span data-ttu-id="2db92-573">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="2db92-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2db92-574">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2db92-575">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="2db92-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2db92-576">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="2db92-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2db92-577">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="2db92-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2db92-578">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="2db92-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2db92-579">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="2db92-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-580">Az.Websites</span></span>
* <span data-ttu-id="2db92-581">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="2db92-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2db92-582">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="2db92-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2db92-583">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="2db92-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2db92-584">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2db92-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2db92-585">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2db92-586">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="2db92-586">Highlights since the last major release</span></span>
* <span data-ttu-id="2db92-587">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="2db92-587">General availability of `Az` module</span></span>
* <span data-ttu-id="2db92-588">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2db92-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2db92-589">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2db92-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2db92-590">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2db92-591">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="2db92-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2db92-592">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2db92-593">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="2db92-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2db92-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-594">Az.Accounts</span></span>
* <span data-ttu-id="2db92-595">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2db92-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2db92-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2db92-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="2db92-597">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="2db92-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2db92-598">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="2db92-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-599">Az.Automation</span></span>
* <span data-ttu-id="2db92-600">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="2db92-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2db92-601">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="2db92-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2db92-602">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="2db92-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-603">Az.Compute</span></span>
* <span data-ttu-id="2db92-604">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2db92-605">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="2db92-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="2db92-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="2db92-607">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="2db92-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2db92-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2db92-608">Az.DataFactory</span></span>
* <span data-ttu-id="2db92-609">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="2db92-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2db92-610">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2db92-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-611">Az.Resources</span></span>
* <span data-ttu-id="2db92-612">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="2db92-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2db92-613">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2db92-613">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2db92-614">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2db92-615">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2db92-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2db92-616">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="2db92-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2db92-617">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2db92-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-618">Az.Sql</span></span>
* <span data-ttu-id="2db92-619">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="2db92-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-620">Az.Storage</span></span>
* <span data-ttu-id="2db92-621">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="2db92-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2db92-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2db92-622">New-AzStorageContext</span></span>
* <span data-ttu-id="2db92-623">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="2db92-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2db92-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2db92-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2db92-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2db92-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2db92-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2db92-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2db92-628">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="2db92-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2db92-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2db92-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2db92-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2db92-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2db92-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2db92-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2db92-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2db92-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2db92-633">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2db92-634">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="2db92-634">Highlights since the last major release</span></span>
* <span data-ttu-id="2db92-635">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="2db92-635">General availability of `Az` module</span></span>
* <span data-ttu-id="2db92-636">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2db92-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2db92-637">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2db92-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2db92-638">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2db92-639">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="2db92-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2db92-640">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2db92-641">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="2db92-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-642">Az.Automation</span></span>
* <span data-ttu-id="2db92-643">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="2db92-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2db92-644">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="2db92-644">Dynamic grouping</span></span>
    * <span data-ttu-id="2db92-645">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="2db92-645">Pre-Post script</span></span>
    * <span data-ttu-id="2db92-646">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="2db92-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-647">Az.Compute</span></span>
* <span data-ttu-id="2db92-648">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="2db92-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2db92-649">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2db92-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2db92-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-650">Az.KeyVault</span></span>
* <span data-ttu-id="2db92-651">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-652">Az.Network</span></span>
* <span data-ttu-id="2db92-653">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="2db92-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2db92-654">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="2db92-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-656">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="2db92-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2db92-657">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="2db92-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-658">Az.Resources</span></span>
* <span data-ttu-id="2db92-659">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2db92-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2db92-660">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="2db92-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-661">Az.Sql</span></span>
* <span data-ttu-id="2db92-662">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="2db92-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-663">Az.Storage</span></span>
* <span data-ttu-id="2db92-664">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="2db92-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2db92-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2db92-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2db92-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2db92-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2db92-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2db92-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2db92-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2db92-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2db92-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-671">Az.Websites</span></span>
* <span data-ttu-id="2db92-672">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="2db92-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="2db92-673">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-674">Az.Accounts</span></span>
* <span data-ttu-id="2db92-675">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="2db92-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2db92-676">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-677">Az.Automation</span></span>
* <span data-ttu-id="2db92-678">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2db92-679">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="2db92-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2db92-680">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="2db92-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2db92-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2db92-681">Az.Cdn</span></span>
* <span data-ttu-id="2db92-682">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="2db92-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-683">Az.Compute</span></span>
* <span data-ttu-id="2db92-684">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="2db92-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2db92-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2db92-685">Az.DataFactory</span></span>
* <span data-ttu-id="2db92-686">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="2db92-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2db92-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2db92-687">Az.LogicApp</span></span>
* <span data-ttu-id="2db92-688">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="2db92-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-689">Az.Network</span></span>
* <span data-ttu-id="2db92-690">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="2db92-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-692">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="2db92-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2db92-693">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="2db92-693">SDK Update</span></span>
* <span data-ttu-id="2db92-694">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2db92-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2db92-695">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2db92-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-696">Az.Resources</span></span>
* <span data-ttu-id="2db92-697">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="2db92-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2db92-698">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2db92-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2db92-699">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2db92-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2db92-700">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2db92-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2db92-701">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2db92-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2db92-702">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2db92-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-703">Az.Sql</span></span>
* <span data-ttu-id="2db92-704">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2db92-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2db92-705">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="2db92-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-706">Az.Storage</span></span>
* <span data-ttu-id="2db92-707">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2db92-708">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2db92-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2db92-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="2db92-710">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="2db92-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-711">Az.Automation</span></span>
* <span data-ttu-id="2db92-712">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2db92-713">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2db92-714">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2db92-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2db92-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="2db92-716">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="2db92-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-717">Az.Compute</span></span>
* <span data-ttu-id="2db92-718">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="2db92-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2db92-719">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="2db92-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2db92-720">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2db92-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2db92-721">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="2db92-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-723">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="2db92-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2db92-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2db92-724">Az.EventHub</span></span>
* <span data-ttu-id="2db92-725">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="2db92-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="2db92-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-726">Az.KeyVault</span></span>
* <span data-ttu-id="2db92-727">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2db92-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2db92-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2db92-728">Az.LogicApp</span></span>
* <span data-ttu-id="2db92-729">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="2db92-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2db92-730">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="2db92-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2db92-731">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="2db92-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2db92-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2db92-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2db92-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2db92-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2db92-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2db92-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2db92-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2db92-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2db92-736">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="2db92-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2db92-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2db92-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2db92-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2db92-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2db92-741">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2db92-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2db92-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2db92-742">Az.Monitor</span></span>
* <span data-ttu-id="2db92-743">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="2db92-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-744">Az.Network</span></span>
* <span data-ttu-id="2db92-745">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2db92-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2db92-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="2db92-747">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2db92-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2db92-748">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="2db92-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="2db92-749">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="2db92-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="2db92-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-750">Az.Resources</span></span>
* <span data-ttu-id="2db92-751">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2db92-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2db92-752">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2db92-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2db92-753">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2db92-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2db92-754">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="2db92-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-755">Az.Sql</span></span>
* <span data-ttu-id="2db92-756">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="2db92-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2db92-757">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="2db92-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-758">Az.Websites</span></span>
* <span data-ttu-id="2db92-759">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="2db92-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2db92-760">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-761">Az.Accounts</span></span>
* <span data-ttu-id="2db92-762">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2db92-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2db92-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2db92-763">Az.AnalysisServices</span></span>
<span data-ttu-id="2db92-764">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2db92-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-765">Az.Compute</span></span>
* <span data-ttu-id="2db92-766">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="2db92-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2db92-767">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2db92-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2db92-768">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2db92-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-769">Az.RecoveryServices</span></span>
<span data-ttu-id="2db92-770">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2db92-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-771">Az.Resources</span></span>
* <span data-ttu-id="2db92-772">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="2db92-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="2db92-773">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2db92-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2db92-774">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="2db92-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="2db92-775">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2db92-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-776">Az.Sql</span></span>
* <span data-ttu-id="2db92-777">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2db92-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2db92-778">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="2db92-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2db92-779">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="2db92-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2db92-780">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-781">Az.Accounts</span></span>
* <span data-ttu-id="2db92-782">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="2db92-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2db92-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2db92-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="2db92-784">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="2db92-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="2db92-786">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="2db92-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2db92-787">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-788">Az.Accounts</span></span>
* <span data-ttu-id="2db92-789">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="2db92-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2db92-790">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2db92-791">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2db92-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2db92-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2db92-792">Az.Aks</span></span>
* <span data-ttu-id="2db92-793">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2db92-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-794">Az.Automation</span></span>
* <span data-ttu-id="2db92-795">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="2db92-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2db92-796">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2db92-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2db92-797">Az.Cdn</span></span>
* <span data-ttu-id="2db92-798">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-799">Az.Compute</span></span>
* <span data-ttu-id="2db92-800">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2db92-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2db92-801">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2db92-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2db92-802">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2db92-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2db92-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2db92-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2db92-804">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2db92-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2db92-805">Az.DataFactory</span></span>
* <span data-ttu-id="2db92-806">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="2db92-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-808">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="2db92-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2db92-809">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2db92-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2db92-810">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2db92-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2db92-811">Az.IotHub</span></span>
* <span data-ttu-id="2db92-812">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2db92-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2db92-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-813">Az.KeyVault</span></span>
* <span data-ttu-id="2db92-814">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-815">Az.Network</span></span>
* <span data-ttu-id="2db92-816">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-817">Az.Resources</span></span>
* <span data-ttu-id="2db92-818">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="2db92-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2db92-819">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="2db92-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2db92-820">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2db92-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2db92-821">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2db92-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2db92-822">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2db92-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2db92-823">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="2db92-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2db92-824">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2db92-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2db92-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2db92-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="2db92-826">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2db92-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2db92-827">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2db92-827">Fix some error messages.</span></span>
* <span data-ttu-id="2db92-828">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="2db92-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2db92-829">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="2db92-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2db92-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2db92-830">Az.SignalR</span></span>
* <span data-ttu-id="2db92-831">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-832">Az.Sql</span></span>
* <span data-ttu-id="2db92-833">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2db92-834">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2db92-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2db92-835">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="2db92-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2db92-836">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="2db92-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-837">Az.Storage</span></span>
* <span data-ttu-id="2db92-838">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2db92-839">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="2db92-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2db92-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2db92-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2db92-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2db92-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2db92-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2db92-842">Az.TrafficManager</span></span>
* <span data-ttu-id="2db92-843">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-844">Az.Websites</span></span>
* <span data-ttu-id="2db92-845">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="2db92-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2db92-846">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="2db92-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2db92-847">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="2db92-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2db92-848">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="2db92-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2db92-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-849">Az.Accounts</span></span>
* <span data-ttu-id="2db92-850">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2db92-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-851">Az.Compute</span></span>
* <span data-ttu-id="2db92-852">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2db92-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2db92-853">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="2db92-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2db92-854">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-856">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="2db92-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2db92-857">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="2db92-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2db92-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2db92-858">Az.EventGrid</span></span>
* <span data-ttu-id="2db92-859">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2db92-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2db92-860">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2db92-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2db92-861">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="2db92-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2db92-862">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="2db92-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2db92-863">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="2db92-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2db92-864">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="2db92-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2db92-865">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="2db92-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2db92-866">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="2db92-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2db92-867">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="2db92-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2db92-868">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="2db92-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="2db92-869">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2db92-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2db92-870">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2db92-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2db92-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2db92-871">Az.IotHub</span></span>
* <span data-ttu-id="2db92-872">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="2db92-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2db92-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2db92-873">Az.LogicApp</span></span>
* <span data-ttu-id="2db92-874">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="2db92-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-875">Az.Resources</span></span>
* <span data-ttu-id="2db92-876">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="2db92-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2db92-877">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2db92-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2db92-878">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2db92-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2db92-879">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2db92-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2db92-880">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="2db92-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2db92-881">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2db92-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2db92-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2db92-882">Az.SignalR</span></span>
* <span data-ttu-id="2db92-883">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-884">Az.Sql</span></span>
* <span data-ttu-id="2db92-885">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="2db92-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2db92-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-886">Az.Storage</span></span>
* <span data-ttu-id="2db92-887">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="2db92-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2db92-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2db92-888">New-AzStorageContext</span></span>
* <span data-ttu-id="2db92-889">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="2db92-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2db92-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2db92-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-891">Az.Websites</span></span>
* <span data-ttu-id="2db92-892">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="2db92-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2db92-893">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2db92-894">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2db92-895">Généralités</span><span class="sxs-lookup"><span data-stu-id="2db92-895">General</span></span>

- <span data-ttu-id="2db92-896">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="2db92-896">General Availability of Az Module</span></span>
- <span data-ttu-id="2db92-897">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="2db92-897">Online help for each module</span></span>
- <span data-ttu-id="2db92-898">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="2db92-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2db92-899">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="2db92-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2db92-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-900">Az.Accounts</span></span>
- <span data-ttu-id="2db92-901">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2db92-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="2db92-902">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="2db92-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2db92-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2db92-903">Az.ApiManagement</span></span>
- <span data-ttu-id="2db92-904">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="2db92-904">Fixes for #7002</span></span>
- <span data-ttu-id="2db92-905">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2db92-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2db92-906">Az.Batch</span></span>
- <span data-ttu-id="2db92-907">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2db92-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2db92-908">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="2db92-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2db92-909">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2db92-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2db92-910">Az.Billing</span></span>
- <span data-ttu-id="2db92-911">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2db92-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2db92-912">Az.CognitivServices</span></span>
- <span data-ttu-id="2db92-913">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2db92-914">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2db92-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2db92-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="2db92-916">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2db92-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2db92-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2db92-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2db92-918">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2db92-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="2db92-920">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2db92-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2db92-921">Az.Monitor</span></span>
- <span data-ttu-id="2db92-922">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2db92-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2db92-923">Az.KeyVault</span></span>
- <span data-ttu-id="2db92-924">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="2db92-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2db92-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2db92-925">Az.MachineLearning</span></span>
- <span data-ttu-id="2db92-926">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2db92-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2db92-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2db92-927">Az.Media</span></span>
- <span data-ttu-id="2db92-928">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2db92-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2db92-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-929">Az.Network</span></span>
<span data-ttu-id="2db92-930">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2db92-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2db92-931">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="2db92-931">New cmdlets added:</span></span>
        - <span data-ttu-id="2db92-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2db92-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2db92-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2db92-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2db92-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2db92-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2db92-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2db92-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2db92-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2db92-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2db92-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2db92-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2db92-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2db92-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2db92-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2db92-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2db92-940">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2db92-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2db92-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2db92-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2db92-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2db92-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2db92-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2db92-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2db92-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2db92-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2db92-946">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="2db92-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2db92-947">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2db92-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2db92-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2db92-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2db92-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2db92-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2db92-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2db92-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2db92-951">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2db92-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2db92-952">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2db92-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="2db92-954">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2db92-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2db92-955">Az.Profile</span></span>
- <span data-ttu-id="2db92-956">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2db92-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="2db92-958">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2db92-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-959">Az.Resources</span></span>
- <span data-ttu-id="2db92-960">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2db92-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2db92-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="2db92-962">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="2db92-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2db92-963">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2db92-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2db92-964">Az.SIgnalR</span></span>
- <span data-ttu-id="2db92-965">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2db92-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2db92-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-966">Az.Sql</span></span>
- <span data-ttu-id="2db92-967">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="2db92-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2db92-968">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="2db92-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2db92-969">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2db92-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-970">Az.Storage</span></span>
- <span data-ttu-id="2db92-971">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2db92-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-972">Az.Websites</span></span>
- <span data-ttu-id="2db92-973">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="2db92-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2db92-974">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2db92-975">Généralités</span><span class="sxs-lookup"><span data-stu-id="2db92-975">General</span></span>

* <span data-ttu-id="2db92-976">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="2db92-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2db92-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-977">Az.Compute</span></span>

* <span data-ttu-id="2db92-978">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2db92-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2db92-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="2db92-980">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="2db92-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2db92-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2db92-981">Az.FrontDoor</span></span>

* <span data-ttu-id="2db92-982">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="2db92-982">Fixed some broken links</span></span>
    - <span data-ttu-id="2db92-983">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2db92-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2db92-984">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2db92-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2db92-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2db92-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="2db92-986">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="2db92-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2db92-987">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="2db92-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2db92-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-988">Az.Resources</span></span>

* <span data-ttu-id="2db92-989">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2db92-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2db92-990">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="2db92-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2db92-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-991">Az.Sql</span></span>

* <span data-ttu-id="2db92-992">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="2db92-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2db92-993">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="2db92-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2db92-994">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="2db92-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2db92-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-995">Az.Storage</span></span>

* <span data-ttu-id="2db92-996">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2db92-997">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="2db92-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2db92-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2db92-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2db92-999">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="2db92-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="2db92-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2db92-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2db92-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2db92-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2db92-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-1002">Az.Websites</span></span>

* <span data-ttu-id="2db92-1003">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2db92-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="2db92-1004">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="2db92-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2db92-1005">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="2db92-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2db92-1006">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2db92-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2db92-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="2db92-1008">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="2db92-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2db92-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2db92-1009">Az.Automation</span></span>
* <span data-ttu-id="2db92-1010">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="2db92-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2db92-1011">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="2db92-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2db92-1012">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="2db92-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2db92-1013">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="2db92-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2db92-1014">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="2db92-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2db92-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-1015">Az.Compute</span></span>
* <span data-ttu-id="2db92-1016">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2db92-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2db92-1017">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="2db92-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2db92-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="2db92-1019">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="2db92-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2db92-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2db92-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2db92-1021">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="2db92-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2db92-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-1022">Az.Network</span></span>
* <span data-ttu-id="2db92-1023">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2db92-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2db92-1024">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="2db92-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2db92-1025">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="2db92-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="2db92-1026">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2db92-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2db92-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2db92-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2db92-1028">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="2db92-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2db92-1029">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="2db92-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2db92-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2db92-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2db92-1031">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2db92-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2db92-1032">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="2db92-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2db92-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2db92-1033">Az.Relay</span></span>
* <span data-ttu-id="2db92-1034">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2db92-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2db92-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-1035">Az.Resources</span></span>
* <span data-ttu-id="2db92-1036">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="2db92-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2db92-1037">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="2db92-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2db92-1038">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2db92-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2db92-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2db92-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="2db92-1040">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="2db92-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2db92-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-1041">Az.Sql</span></span>
* <span data-ttu-id="2db92-1042">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="2db92-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2db92-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2db92-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2db92-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2db92-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2db92-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2db92-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2db92-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2db92-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2db92-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2db92-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2db92-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2db92-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2db92-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2db92-1051">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="2db92-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2db92-1052">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="2db92-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2db92-1053">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="2db92-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2db92-1054">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2db92-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2db92-1055">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2db92-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2db92-1056">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2db92-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2db92-1057">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2db92-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2db92-1058">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="2db92-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2db92-1059">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2db92-1060">Généralités</span><span class="sxs-lookup"><span data-stu-id="2db92-1060">General</span></span>
* <span data-ttu-id="2db92-1061">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="2db92-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2db92-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2db92-1062">Az.Profile</span></span>
* <span data-ttu-id="2db92-1063">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2db92-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2db92-1064">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="2db92-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2db92-1065">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2db92-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2db92-1066">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="2db92-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2db92-1067">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="2db92-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2db92-1068">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="2db92-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2db92-1069">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="2db92-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2db92-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2db92-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="2db92-1071">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2db92-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-1072">Az.Compute</span></span>
* <span data-ttu-id="2db92-1073">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2db92-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2db92-1074">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2db92-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2db92-1075">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="2db92-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-1077">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2db92-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2db92-1078">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="2db92-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2db92-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2db92-1079">Az.Insights</span></span>
* <span data-ttu-id="2db92-1080">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="2db92-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2db92-1081">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="2db92-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2db92-1082">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="2db92-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2db92-1083">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="2db92-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-1084">Az.Network</span></span>
* <span data-ttu-id="2db92-1085">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="2db92-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2db92-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db92-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2db92-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2db92-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2db92-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2db92-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2db92-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2db92-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2db92-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2db92-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2db92-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2db92-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2db92-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2db92-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="2db92-1093">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="2db92-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-1094">Az.Resources</span></span>
* <span data-ttu-id="2db92-1095">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2db92-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2db92-1096">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="2db92-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2db92-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2db92-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="2db92-1098">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="2db92-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2db92-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2db92-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="2db92-1100">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="2db92-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2db92-1101">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="2db92-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2db92-1102">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2db92-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2db92-1103">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2db92-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2db92-1104">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="2db92-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2db92-1105">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2db92-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2db92-1106">Az.Profile</span></span>
* <span data-ttu-id="2db92-1107">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="2db92-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2db92-1108">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2db92-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-1109">Az.Compute</span></span>
* <span data-ttu-id="2db92-1110">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="2db92-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2db92-1111">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="2db92-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2db92-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2db92-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="2db92-1113">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="2db92-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2db92-1114">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2db92-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2db92-1115">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="2db92-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2db92-1116">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="2db92-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2db92-1117">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2db92-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-1118">Az.Network</span></span>
* <span data-ttu-id="2db92-1119">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="2db92-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2db92-1120">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="2db92-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-1121">Az.Resources</span></span>
* <span data-ttu-id="2db92-1122">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="2db92-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2db92-1123">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="2db92-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2db92-1124">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2db92-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2db92-1125">Azure.Storage</span></span>
* <span data-ttu-id="2db92-1126">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="2db92-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2db92-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2db92-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2db92-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2db92-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2db92-1129">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="2db92-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2db92-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2db92-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="2db92-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2db92-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="2db92-1132">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="2db92-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2db92-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2db92-1133">Az.Compute</span></span>
* <span data-ttu-id="2db92-1134">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="2db92-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2db92-1135">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2db92-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2db92-1136">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="2db92-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2db92-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2db92-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2db92-1138">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="2db92-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2db92-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2db92-1139">Az.Network</span></span>
* <span data-ttu-id="2db92-1140">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="2db92-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2db92-1141">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="2db92-1141">new cmdlets added</span></span>
    - <span data-ttu-id="2db92-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2db92-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2db92-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2db92-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2db92-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2db92-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2db92-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2db92-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2db92-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2db92-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2db92-1148">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="2db92-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2db92-1149">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2db92-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2db92-1150">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2db92-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2db92-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2db92-1151">Az.RedisCache</span></span>
* <span data-ttu-id="2db92-1152">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="2db92-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2db92-1153">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2db92-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2db92-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2db92-1154">Az.Resources</span></span>
* <span data-ttu-id="2db92-1155">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2db92-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2db92-1156">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="2db92-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2db92-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2db92-1157">Az.Sql</span></span>
* <span data-ttu-id="2db92-1158">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="2db92-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2db92-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2db92-1159">Az.Websites</span></span>
* <span data-ttu-id="2db92-1160">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="2db92-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2db92-1161">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="2db92-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2db92-1162">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="2db92-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2db92-1163">Version initiale</span><span class="sxs-lookup"><span data-stu-id="2db92-1163">Initial Release</span></span>