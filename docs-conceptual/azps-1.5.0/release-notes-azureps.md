---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882298"
---
## <a name="150---march-2019"></a><span data-ttu-id="a540b-101">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="a540b-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a540b-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-102">Az.Accounts</span></span>
* <span data-ttu-id="a540b-103">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="a540b-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a540b-104">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a540b-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a540b-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a540b-105">Az.Automation</span></span>
* <span data-ttu-id="a540b-106">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="a540b-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a540b-107">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="a540b-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a540b-108">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="a540b-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a540b-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a540b-109">Az.Cdn</span></span>
* <span data-ttu-id="a540b-110">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="a540b-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-111">Az.Compute</span></span>
* <span data-ttu-id="a540b-112">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="a540b-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a540b-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a540b-113">Az.DataFactory</span></span>
* <span data-ttu-id="a540b-114">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a540b-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a540b-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a540b-115">Az.LogicApp</span></span>
* <span data-ttu-id="a540b-116">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="a540b-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a540b-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-117">Az.Network</span></span>
* <span data-ttu-id="a540b-118">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="a540b-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a540b-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a540b-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="a540b-120">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="a540b-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a540b-121">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="a540b-121">SDK Update</span></span>
* <span data-ttu-id="a540b-122">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a540b-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a540b-123">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a540b-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-124">Az.Resources</span></span>
* <span data-ttu-id="a540b-125">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="a540b-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a540b-126">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a540b-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a540b-127">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a540b-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a540b-128">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a540b-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a540b-129">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a540b-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a540b-130">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a540b-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a540b-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-131">Az.Sql</span></span>
* <span data-ttu-id="a540b-132">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="a540b-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a540b-133">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="a540b-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a540b-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a540b-134">Az.Storage</span></span>
* <span data-ttu-id="a540b-135">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a540b-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a540b-136">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="a540b-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a540b-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a540b-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="a540b-138">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="a540b-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a540b-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a540b-139">Az.Automation</span></span>
* <span data-ttu-id="a540b-140">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a540b-141">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a540b-142">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a540b-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a540b-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="a540b-144">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a540b-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-145">Az.Compute</span></span>
* <span data-ttu-id="a540b-146">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="a540b-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a540b-147">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="a540b-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a540b-148">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a540b-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a540b-149">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="a540b-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a540b-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="a540b-151">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="a540b-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a540b-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a540b-152">Az.EventHub</span></span>
* <span data-ttu-id="a540b-153">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="a540b-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a540b-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a540b-154">Az.KeyVault</span></span>
* <span data-ttu-id="a540b-155">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a540b-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a540b-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a540b-156">Az.LogicApp</span></span>
* <span data-ttu-id="a540b-157">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="a540b-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a540b-158">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="a540b-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a540b-159">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="a540b-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a540b-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a540b-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a540b-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a540b-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a540b-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a540b-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a540b-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a540b-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a540b-164">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="a540b-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a540b-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a540b-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a540b-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a540b-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a540b-169">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a540b-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a540b-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a540b-170">Az.Monitor</span></span>
* <span data-ttu-id="a540b-171">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="a540b-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a540b-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-172">Az.Network</span></span>
* <span data-ttu-id="a540b-173">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a540b-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a540b-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a540b-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="a540b-175">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a540b-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a540b-176">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="a540b-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a540b-177">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="a540b-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a540b-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-178">Az.Resources</span></span>
* <span data-ttu-id="a540b-179">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a540b-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a540b-180">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a540b-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a540b-181">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a540b-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a540b-182">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a540b-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a540b-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-183">Az.Sql</span></span>
* <span data-ttu-id="a540b-184">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="a540b-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a540b-185">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="a540b-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a540b-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a540b-186">Az.Websites</span></span>
* <span data-ttu-id="a540b-187">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a540b-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a540b-188">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="a540b-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a540b-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-189">Az.Accounts</span></span>
* <span data-ttu-id="a540b-190">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a540b-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a540b-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a540b-191">Az.AnalysisServices</span></span>
<span data-ttu-id="a540b-192">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a540b-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-193">Az.Compute</span></span>
* <span data-ttu-id="a540b-194">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="a540b-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a540b-195">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a540b-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a540b-196">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a540b-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a540b-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a540b-197">Az.RecoveryServices</span></span>
<span data-ttu-id="a540b-198">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a540b-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-199">Az.Resources</span></span>
* <span data-ttu-id="a540b-200">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="a540b-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a540b-201">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a540b-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a540b-202">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a540b-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a540b-203">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a540b-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a540b-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-204">Az.Sql</span></span>
* <span data-ttu-id="a540b-205">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a540b-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a540b-206">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="a540b-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a540b-207">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a540b-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a540b-208">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="a540b-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a540b-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-209">Az.Accounts</span></span>
* <span data-ttu-id="a540b-210">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="a540b-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a540b-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a540b-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="a540b-212">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="a540b-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a540b-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a540b-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="a540b-214">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="a540b-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a540b-215">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="a540b-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a540b-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-216">Az.Accounts</span></span>
* <span data-ttu-id="a540b-217">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="a540b-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a540b-218">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a540b-219">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a540b-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a540b-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a540b-220">Az.Aks</span></span>
* <span data-ttu-id="a540b-221">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a540b-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a540b-222">Az.Automation</span></span>
* <span data-ttu-id="a540b-223">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="a540b-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a540b-224">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a540b-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a540b-225">Az.Cdn</span></span>
* <span data-ttu-id="a540b-226">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-227">Az.Compute</span></span>
* <span data-ttu-id="a540b-228">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a540b-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a540b-229">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a540b-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a540b-230">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a540b-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a540b-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a540b-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a540b-232">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a540b-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a540b-233">Az.DataFactory</span></span>
* <span data-ttu-id="a540b-234">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a540b-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a540b-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="a540b-236">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="a540b-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a540b-237">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a540b-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a540b-238">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a540b-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a540b-239">Az.IotHub</span></span>
* <span data-ttu-id="a540b-240">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a540b-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a540b-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a540b-241">Az.KeyVault</span></span>
* <span data-ttu-id="a540b-242">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a540b-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-243">Az.Network</span></span>
* <span data-ttu-id="a540b-244">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-245">Az.Resources</span></span>
* <span data-ttu-id="a540b-246">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="a540b-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a540b-247">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="a540b-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a540b-248">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a540b-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a540b-249">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a540b-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a540b-250">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a540b-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a540b-251">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="a540b-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a540b-252">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a540b-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a540b-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a540b-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="a540b-254">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a540b-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a540b-255">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a540b-255">Fix some error messages.</span></span>
* <span data-ttu-id="a540b-256">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="a540b-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a540b-257">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="a540b-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a540b-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a540b-258">Az.SignalR</span></span>
* <span data-ttu-id="a540b-259">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a540b-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-260">Az.Sql</span></span>
* <span data-ttu-id="a540b-261">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a540b-262">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a540b-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a540b-263">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="a540b-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a540b-264">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="a540b-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a540b-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a540b-265">Az.Storage</span></span>
* <span data-ttu-id="a540b-266">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a540b-267">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="a540b-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a540b-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a540b-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a540b-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a540b-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a540b-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a540b-270">Az.TrafficManager</span></span>
* <span data-ttu-id="a540b-271">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a540b-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a540b-272">Az.Websites</span></span>
* <span data-ttu-id="a540b-273">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="a540b-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a540b-274">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="a540b-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a540b-275">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="a540b-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a540b-276">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="a540b-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a540b-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-277">Az.Accounts</span></span>
* <span data-ttu-id="a540b-278">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a540b-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-279">Az.Compute</span></span>
* <span data-ttu-id="a540b-280">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a540b-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a540b-281">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="a540b-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a540b-282">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a540b-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="a540b-284">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="a540b-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a540b-285">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="a540b-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a540b-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a540b-286">Az.EventGrid</span></span>
* <span data-ttu-id="a540b-287">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a540b-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a540b-288">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a540b-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a540b-289">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="a540b-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a540b-290">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="a540b-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a540b-291">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="a540b-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a540b-292">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="a540b-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a540b-293">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="a540b-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a540b-294">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="a540b-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a540b-295">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="a540b-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a540b-296">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="a540b-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="a540b-297">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a540b-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a540b-298">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a540b-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a540b-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a540b-299">Az.IotHub</span></span>
* <span data-ttu-id="a540b-300">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="a540b-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a540b-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a540b-301">Az.LogicApp</span></span>
* <span data-ttu-id="a540b-302">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="a540b-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-303">Az.Resources</span></span>
* <span data-ttu-id="a540b-304">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="a540b-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a540b-305">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a540b-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a540b-306">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a540b-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a540b-307">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a540b-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a540b-308">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="a540b-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a540b-309">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a540b-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a540b-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a540b-310">Az.SignalR</span></span>
* <span data-ttu-id="a540b-311">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a540b-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-312">Az.Sql</span></span>
* <span data-ttu-id="a540b-313">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="a540b-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a540b-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a540b-314">Az.Storage</span></span>
* <span data-ttu-id="a540b-315">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="a540b-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a540b-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a540b-316">New-AzStorageContext</span></span>
* <span data-ttu-id="a540b-317">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="a540b-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a540b-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a540b-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a540b-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a540b-319">Az.Websites</span></span>
* <span data-ttu-id="a540b-320">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="a540b-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a540b-321">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a540b-322">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a540b-323">Généralités</span><span class="sxs-lookup"><span data-stu-id="a540b-323">General</span></span>

- <span data-ttu-id="a540b-324">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="a540b-324">General Availability of Az Module</span></span>
- <span data-ttu-id="a540b-325">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="a540b-325">Online help for each module</span></span>
- <span data-ttu-id="a540b-326">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a540b-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a540b-327">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="a540b-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a540b-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-328">Az.Accounts</span></span>
- <span data-ttu-id="a540b-329">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a540b-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="a540b-330">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="a540b-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a540b-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a540b-331">Az.ApiManagement</span></span>
- <span data-ttu-id="a540b-332">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="a540b-332">Fixes for #7002</span></span>
- <span data-ttu-id="a540b-333">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a540b-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a540b-334">Az.Batch</span></span>
- <span data-ttu-id="a540b-335">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a540b-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a540b-336">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="a540b-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a540b-337">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a540b-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a540b-338">Az.Billing</span></span>
- <span data-ttu-id="a540b-339">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a540b-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a540b-340">Az.CognitivServices</span></span>
- <span data-ttu-id="a540b-341">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a540b-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a540b-342">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a540b-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a540b-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a540b-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="a540b-344">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a540b-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a540b-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a540b-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a540b-346">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a540b-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="a540b-348">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a540b-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a540b-349">Az.Monitor</span></span>
- <span data-ttu-id="a540b-350">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a540b-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a540b-351">Az.KeyVault</span></span>
- <span data-ttu-id="a540b-352">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="a540b-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a540b-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a540b-353">Az.MachineLearning</span></span>
- <span data-ttu-id="a540b-354">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a540b-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a540b-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a540b-355">Az.Media</span></span>
- <span data-ttu-id="a540b-356">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a540b-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a540b-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-357">Az.Network</span></span>
<span data-ttu-id="a540b-358">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a540b-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a540b-359">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="a540b-359">New cmdlets added:</span></span>
        - <span data-ttu-id="a540b-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a540b-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a540b-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a540b-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a540b-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a540b-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a540b-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a540b-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a540b-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a540b-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a540b-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a540b-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a540b-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a540b-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a540b-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a540b-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a540b-368">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a540b-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a540b-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a540b-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a540b-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a540b-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a540b-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a540b-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a540b-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a540b-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a540b-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a540b-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a540b-374">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="a540b-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a540b-375">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a540b-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a540b-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a540b-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a540b-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a540b-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a540b-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a540b-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a540b-379">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a540b-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a540b-380">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a540b-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a540b-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="a540b-382">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a540b-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a540b-383">Az.Profile</span></span>
- <span data-ttu-id="a540b-384">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a540b-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a540b-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a540b-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="a540b-386">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a540b-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-387">Az.Resources</span></span>
- <span data-ttu-id="a540b-388">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a540b-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a540b-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="a540b-390">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="a540b-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a540b-391">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a540b-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a540b-392">Az.SIgnalR</span></span>
- <span data-ttu-id="a540b-393">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a540b-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a540b-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-394">Az.Sql</span></span>
- <span data-ttu-id="a540b-395">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="a540b-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a540b-396">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="a540b-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a540b-397">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a540b-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a540b-398">Az.Storage</span></span>
- <span data-ttu-id="a540b-399">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a540b-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a540b-400">Az.Websites</span></span>
- <span data-ttu-id="a540b-401">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="a540b-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a540b-402">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a540b-403">Généralités</span><span class="sxs-lookup"><span data-stu-id="a540b-403">General</span></span>

* <span data-ttu-id="a540b-404">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="a540b-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a540b-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-405">Az.Compute</span></span>

* <span data-ttu-id="a540b-406">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a540b-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a540b-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="a540b-408">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="a540b-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a540b-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a540b-409">Az.FrontDoor</span></span>

* <span data-ttu-id="a540b-410">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="a540b-410">Fixed some broken links</span></span>
    - <span data-ttu-id="a540b-411">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a540b-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a540b-412">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a540b-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a540b-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a540b-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="a540b-414">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="a540b-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a540b-415">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="a540b-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a540b-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-416">Az.Resources</span></span>

* <span data-ttu-id="a540b-417">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a540b-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a540b-418">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="a540b-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a540b-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-419">Az.Sql</span></span>

* <span data-ttu-id="a540b-420">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="a540b-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a540b-421">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="a540b-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a540b-422">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="a540b-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a540b-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a540b-423">Az.Storage</span></span>

* <span data-ttu-id="a540b-424">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a540b-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a540b-425">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="a540b-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a540b-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a540b-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a540b-427">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="a540b-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="a540b-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a540b-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a540b-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a540b-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a540b-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a540b-430">Az.Websites</span></span>

* <span data-ttu-id="a540b-431">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a540b-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a540b-432">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="a540b-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a540b-433">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="a540b-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a540b-434">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a540b-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a540b-435">Az.ApiManagement</span></span>
* <span data-ttu-id="a540b-436">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="a540b-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a540b-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a540b-437">Az.Automation</span></span>
* <span data-ttu-id="a540b-438">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="a540b-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a540b-439">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="a540b-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a540b-440">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="a540b-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a540b-441">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a540b-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a540b-442">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="a540b-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a540b-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-443">Az.Compute</span></span>
* <span data-ttu-id="a540b-444">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a540b-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a540b-445">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="a540b-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a540b-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a540b-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="a540b-447">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="a540b-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a540b-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a540b-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a540b-449">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="a540b-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a540b-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-450">Az.Network</span></span>
* <span data-ttu-id="a540b-451">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a540b-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a540b-452">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="a540b-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a540b-453">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="a540b-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a540b-454">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a540b-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a540b-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a540b-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a540b-456">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="a540b-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a540b-457">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="a540b-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a540b-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a540b-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a540b-459">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a540b-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a540b-460">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="a540b-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a540b-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a540b-461">Az.Relay</span></span>
* <span data-ttu-id="a540b-462">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a540b-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a540b-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-463">Az.Resources</span></span>
* <span data-ttu-id="a540b-464">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a540b-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a540b-465">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="a540b-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a540b-466">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a540b-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a540b-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a540b-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="a540b-468">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="a540b-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a540b-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-469">Az.Sql</span></span>
* <span data-ttu-id="a540b-470">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="a540b-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a540b-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a540b-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a540b-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a540b-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a540b-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a540b-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a540b-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a540b-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a540b-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a540b-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a540b-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a540b-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a540b-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a540b-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a540b-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a540b-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a540b-479">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="a540b-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a540b-480">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="a540b-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a540b-481">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="a540b-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a540b-482">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a540b-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a540b-483">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a540b-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a540b-484">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a540b-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a540b-485">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a540b-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a540b-486">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="a540b-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a540b-487">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a540b-488">Généralités</span><span class="sxs-lookup"><span data-stu-id="a540b-488">General</span></span>
* <span data-ttu-id="a540b-489">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="a540b-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a540b-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a540b-490">Az.Profile</span></span>
* <span data-ttu-id="a540b-491">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a540b-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a540b-492">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="a540b-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a540b-493">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a540b-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a540b-494">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="a540b-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a540b-495">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="a540b-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a540b-496">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="a540b-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a540b-497">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="a540b-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a540b-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a540b-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="a540b-499">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a540b-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-500">Az.Compute</span></span>
* <span data-ttu-id="a540b-501">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a540b-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a540b-502">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a540b-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a540b-503">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="a540b-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a540b-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="a540b-505">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a540b-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a540b-506">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="a540b-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a540b-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a540b-507">Az.Insights</span></span>
* <span data-ttu-id="a540b-508">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="a540b-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a540b-509">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="a540b-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a540b-510">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="a540b-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a540b-511">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="a540b-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a540b-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-512">Az.Network</span></span>
* <span data-ttu-id="a540b-513">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="a540b-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a540b-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a540b-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a540b-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a540b-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a540b-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a540b-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a540b-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a540b-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a540b-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a540b-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a540b-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a540b-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a540b-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a540b-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="a540b-521">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="a540b-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-522">Az.Resources</span></span>
* <span data-ttu-id="a540b-523">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a540b-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a540b-524">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="a540b-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a540b-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a540b-525">Az.ServiceBus</span></span>
* <span data-ttu-id="a540b-526">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="a540b-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a540b-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a540b-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="a540b-528">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="a540b-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a540b-529">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="a540b-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a540b-530">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a540b-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a540b-531">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a540b-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a540b-532">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="a540b-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a540b-533">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a540b-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a540b-534">Az.Profile</span></span>
* <span data-ttu-id="a540b-535">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="a540b-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a540b-536">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a540b-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-537">Az.Compute</span></span>
* <span data-ttu-id="a540b-538">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="a540b-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a540b-539">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="a540b-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a540b-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a540b-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="a540b-541">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="a540b-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a540b-542">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a540b-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a540b-543">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="a540b-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a540b-544">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="a540b-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a540b-545">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a540b-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a540b-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-546">Az.Network</span></span>
* <span data-ttu-id="a540b-547">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="a540b-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a540b-548">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="a540b-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-549">Az.Resources</span></span>
* <span data-ttu-id="a540b-550">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="a540b-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a540b-551">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="a540b-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a540b-552">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a540b-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a540b-553">Azure.Storage</span></span>
* <span data-ttu-id="a540b-554">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="a540b-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a540b-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a540b-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a540b-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a540b-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a540b-557">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="a540b-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a540b-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a540b-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a540b-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a540b-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="a540b-560">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="a540b-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a540b-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a540b-561">Az.Compute</span></span>
* <span data-ttu-id="a540b-562">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="a540b-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a540b-563">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a540b-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a540b-564">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="a540b-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a540b-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a540b-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a540b-566">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="a540b-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a540b-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a540b-567">Az.Network</span></span>
* <span data-ttu-id="a540b-568">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="a540b-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a540b-569">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="a540b-569">new cmdlets added</span></span>
    - <span data-ttu-id="a540b-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a540b-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a540b-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a540b-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a540b-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a540b-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a540b-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a540b-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a540b-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a540b-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a540b-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a540b-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a540b-576">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="a540b-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a540b-577">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a540b-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a540b-578">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a540b-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a540b-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a540b-579">Az.RedisCache</span></span>
* <span data-ttu-id="a540b-580">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="a540b-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a540b-581">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a540b-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a540b-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a540b-582">Az.Resources</span></span>
* <span data-ttu-id="a540b-583">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a540b-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a540b-584">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="a540b-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a540b-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a540b-585">Az.Sql</span></span>
* <span data-ttu-id="a540b-586">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="a540b-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a540b-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a540b-587">Az.Websites</span></span>
* <span data-ttu-id="a540b-588">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="a540b-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a540b-589">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="a540b-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a540b-590">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="a540b-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a540b-591">Version initiale</span><span class="sxs-lookup"><span data-stu-id="a540b-591">Initial Release</span></span>