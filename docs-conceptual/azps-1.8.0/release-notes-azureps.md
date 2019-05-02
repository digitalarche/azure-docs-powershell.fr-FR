---
ms.openlocfilehash: 10d8d50131b3c55ae19c5142c42cb47f37c68c92
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068912"
---
## <a name="180---april-2019"></a><span data-ttu-id="187f5-101">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="187f5-102">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="187f5-102">Highlights since the last major release</span></span>
* <span data-ttu-id="187f5-103">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="187f5-103">General availability of `Az` module</span></span>
* <span data-ttu-id="187f5-104">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="187f5-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="187f5-105">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="187f5-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="187f5-106">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="187f5-107">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="187f5-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="187f5-108">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="187f5-109">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="187f5-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="187f5-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-110">Az.Accounts</span></span>
* <span data-ttu-id="187f5-111">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="187f5-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="187f5-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="187f5-112">Az.Batch</span></span>
* <span data-ttu-id="187f5-113">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="187f5-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="187f5-114">Az.Cdn</span></span>
* <span data-ttu-id="187f5-115">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="187f5-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="187f5-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="187f5-117">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-118">Az.Compute</span></span>
* <span data-ttu-id="187f5-119">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="187f5-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="187f5-120">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="187f5-121">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="187f5-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="187f5-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="187f5-122">Az.DataFactory</span></span>
* <span data-ttu-id="187f5-123">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="187f5-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="187f5-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="187f5-125">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="187f5-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="187f5-126">Az.EventGrid</span></span>
* <span data-ttu-id="187f5-127">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="187f5-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="187f5-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="187f5-128">Az.EventHub</span></span>
* <span data-ttu-id="187f5-129">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="187f5-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="187f5-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="187f5-130">Az.HDInsight</span></span>
* <span data-ttu-id="187f5-131">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="187f5-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="187f5-132">Az.IotHub</span></span>
* <span data-ttu-id="187f5-133">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="187f5-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="187f5-134">Az.KeyVault</span></span>
* <span data-ttu-id="187f5-135">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="187f5-136">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="187f5-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="187f5-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="187f5-137">Az.MachineLearning</span></span>
* <span data-ttu-id="187f5-138">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="187f5-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="187f5-139">Az.Media</span></span>
* <span data-ttu-id="187f5-140">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="187f5-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="187f5-141">Az.Monitor</span></span>
  * <span data-ttu-id="187f5-142">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="187f5-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="187f5-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="187f5-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="187f5-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="187f5-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="187f5-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="187f5-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="187f5-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="187f5-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="187f5-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="187f5-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="187f5-148">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="187f5-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-149">Az.Network</span></span>
* <span data-ttu-id="187f5-150">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="187f5-151">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="187f5-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="187f5-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="187f5-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="187f5-153">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="187f5-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="187f5-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="187f5-155">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="187f5-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="187f5-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="187f5-157">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="187f5-159">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="187f5-160">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="187f5-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="187f5-161">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="187f5-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="187f5-162">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="187f5-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="187f5-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="187f5-163">Az.RedisCache</span></span>
* <span data-ttu-id="187f5-164">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-165">Az.Resources</span></span>
* <span data-ttu-id="187f5-166">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="187f5-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-167">Az.Sql</span></span>
* <span data-ttu-id="187f5-168">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="187f5-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="187f5-169">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="187f5-170">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="187f5-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="187f5-171">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="187f5-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="187f5-172">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="187f5-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="187f5-173">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="187f5-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="187f5-174">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="187f5-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="187f5-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-175">Az.Websites</span></span>
* <span data-ttu-id="187f5-176">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="187f5-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="187f5-177">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="187f5-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="187f5-178">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="187f5-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="187f5-179">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="187f5-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="187f5-180">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="187f5-181">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="187f5-181">Highlights since the last major release</span></span>
* <span data-ttu-id="187f5-182">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="187f5-182">General availability of `Az` module</span></span>
* <span data-ttu-id="187f5-183">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="187f5-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="187f5-184">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="187f5-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="187f5-185">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="187f5-186">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="187f5-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="187f5-187">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="187f5-188">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="187f5-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="187f5-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-189">Az.Accounts</span></span>
* <span data-ttu-id="187f5-190">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="187f5-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="187f5-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="187f5-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="187f5-192">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="187f5-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="187f5-193">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="187f5-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="187f5-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-194">Az.Automation</span></span>
* <span data-ttu-id="187f5-195">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="187f5-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="187f5-196">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="187f5-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="187f5-197">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="187f5-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-198">Az.Compute</span></span>
* <span data-ttu-id="187f5-199">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="187f5-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="187f5-200">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="187f5-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="187f5-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="187f5-202">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="187f5-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="187f5-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="187f5-203">Az.DataFactory</span></span>
* <span data-ttu-id="187f5-204">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="187f5-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="187f5-205">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="187f5-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-206">Az.Resources</span></span>
* <span data-ttu-id="187f5-207">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="187f5-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="187f5-208">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="187f5-208">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="187f5-209">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="187f5-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="187f5-210">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="187f5-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="187f5-211">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="187f5-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="187f5-212">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="187f5-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-213">Az.Sql</span></span>
* <span data-ttu-id="187f5-214">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="187f5-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="187f5-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-215">Az.Storage</span></span>
* <span data-ttu-id="187f5-216">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="187f5-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="187f5-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="187f5-217">New-AzStorageContext</span></span>
* <span data-ttu-id="187f5-218">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="187f5-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="187f5-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="187f5-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="187f5-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="187f5-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="187f5-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="187f5-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="187f5-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="187f5-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="187f5-223">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="187f5-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="187f5-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="187f5-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="187f5-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="187f5-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="187f5-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="187f5-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="187f5-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="187f5-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="187f5-228">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="187f5-229">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="187f5-229">Highlights since the last major release</span></span>
* <span data-ttu-id="187f5-230">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="187f5-230">General availability of `Az` module</span></span>
* <span data-ttu-id="187f5-231">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="187f5-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="187f5-232">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="187f5-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="187f5-233">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="187f5-234">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="187f5-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="187f5-235">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="187f5-236">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="187f5-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="187f5-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-237">Az.Automation</span></span>
* <span data-ttu-id="187f5-238">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="187f5-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="187f5-239">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="187f5-239">Dynamic grouping</span></span>
    * <span data-ttu-id="187f5-240">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="187f5-240">Pre-Post script</span></span>
    * <span data-ttu-id="187f5-241">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="187f5-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-242">Az.Compute</span></span>
* <span data-ttu-id="187f5-243">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="187f5-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="187f5-244">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="187f5-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="187f5-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="187f5-245">Az.KeyVault</span></span>
* <span data-ttu-id="187f5-246">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="187f5-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-247">Az.Network</span></span>
* <span data-ttu-id="187f5-248">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="187f5-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="187f5-249">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="187f5-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="187f5-251">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="187f5-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="187f5-252">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="187f5-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-253">Az.Resources</span></span>
* <span data-ttu-id="187f5-254">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="187f5-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="187f5-255">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="187f5-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-256">Az.Sql</span></span>
* <span data-ttu-id="187f5-257">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="187f5-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="187f5-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-258">Az.Storage</span></span>
* <span data-ttu-id="187f5-259">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="187f5-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="187f5-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="187f5-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="187f5-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="187f5-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="187f5-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="187f5-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="187f5-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="187f5-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="187f5-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="187f5-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="187f5-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="187f5-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="187f5-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-266">Az.Websites</span></span>
* <span data-ttu-id="187f5-267">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="187f5-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="187f5-268">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="187f5-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-269">Az.Accounts</span></span>
* <span data-ttu-id="187f5-270">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="187f5-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="187f5-271">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="187f5-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="187f5-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-272">Az.Automation</span></span>
* <span data-ttu-id="187f5-273">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="187f5-274">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="187f5-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="187f5-275">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="187f5-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="187f5-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="187f5-276">Az.Cdn</span></span>
* <span data-ttu-id="187f5-277">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="187f5-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-278">Az.Compute</span></span>
* <span data-ttu-id="187f5-279">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="187f5-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="187f5-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="187f5-280">Az.DataFactory</span></span>
* <span data-ttu-id="187f5-281">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="187f5-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="187f5-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="187f5-282">Az.LogicApp</span></span>
* <span data-ttu-id="187f5-283">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="187f5-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-284">Az.Network</span></span>
* <span data-ttu-id="187f5-285">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="187f5-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="187f5-287">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="187f5-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="187f5-288">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="187f5-288">SDK Update</span></span>
* <span data-ttu-id="187f5-289">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="187f5-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="187f5-290">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="187f5-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-291">Az.Resources</span></span>
* <span data-ttu-id="187f5-292">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="187f5-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="187f5-293">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="187f5-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="187f5-294">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="187f5-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="187f5-295">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="187f5-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="187f5-296">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="187f5-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="187f5-297">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="187f5-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-298">Az.Sql</span></span>
* <span data-ttu-id="187f5-299">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="187f5-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="187f5-300">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="187f5-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="187f5-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-301">Az.Storage</span></span>
* <span data-ttu-id="187f5-302">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="187f5-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="187f5-303">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="187f5-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="187f5-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="187f5-305">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="187f5-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="187f5-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-306">Az.Automation</span></span>
* <span data-ttu-id="187f5-307">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="187f5-308">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="187f5-309">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="187f5-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="187f5-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="187f5-311">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="187f5-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-312">Az.Compute</span></span>
* <span data-ttu-id="187f5-313">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="187f5-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="187f5-314">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="187f5-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="187f5-315">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="187f5-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="187f5-316">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="187f5-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="187f5-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="187f5-318">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="187f5-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="187f5-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="187f5-319">Az.EventHub</span></span>
* <span data-ttu-id="187f5-320">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="187f5-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="187f5-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="187f5-321">Az.KeyVault</span></span>
* <span data-ttu-id="187f5-322">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="187f5-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="187f5-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="187f5-323">Az.LogicApp</span></span>
* <span data-ttu-id="187f5-324">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="187f5-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="187f5-325">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="187f5-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="187f5-326">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="187f5-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="187f5-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="187f5-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="187f5-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="187f5-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="187f5-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="187f5-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="187f5-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="187f5-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="187f5-331">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="187f5-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="187f5-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="187f5-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="187f5-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="187f5-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="187f5-336">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="187f5-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="187f5-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="187f5-337">Az.Monitor</span></span>
* <span data-ttu-id="187f5-338">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="187f5-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-339">Az.Network</span></span>
* <span data-ttu-id="187f5-340">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="187f5-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="187f5-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="187f5-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="187f5-342">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="187f5-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="187f5-343">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="187f5-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="187f5-344">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="187f5-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="187f5-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-345">Az.Resources</span></span>
* <span data-ttu-id="187f5-346">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="187f5-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="187f5-347">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="187f5-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="187f5-348">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="187f5-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="187f5-349">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="187f5-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-350">Az.Sql</span></span>
* <span data-ttu-id="187f5-351">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="187f5-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="187f5-352">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="187f5-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="187f5-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-353">Az.Websites</span></span>
* <span data-ttu-id="187f5-354">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="187f5-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="187f5-355">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="187f5-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-356">Az.Accounts</span></span>
* <span data-ttu-id="187f5-357">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="187f5-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="187f5-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="187f5-358">Az.AnalysisServices</span></span>
<span data-ttu-id="187f5-359">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="187f5-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-360">Az.Compute</span></span>
* <span data-ttu-id="187f5-361">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="187f5-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="187f5-362">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="187f5-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="187f5-363">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="187f5-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-364">Az.RecoveryServices</span></span>
<span data-ttu-id="187f5-365">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="187f5-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-366">Az.Resources</span></span>
* <span data-ttu-id="187f5-367">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="187f5-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="187f5-368">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="187f5-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="187f5-369">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="187f5-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="187f5-370">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="187f5-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-371">Az.Sql</span></span>
* <span data-ttu-id="187f5-372">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="187f5-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="187f5-373">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="187f5-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="187f5-374">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="187f5-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="187f5-375">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="187f5-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-376">Az.Accounts</span></span>
* <span data-ttu-id="187f5-377">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="187f5-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="187f5-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="187f5-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="187f5-379">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="187f5-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="187f5-381">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="187f5-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="187f5-382">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="187f5-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-383">Az.Accounts</span></span>
* <span data-ttu-id="187f5-384">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="187f5-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="187f5-385">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="187f5-386">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="187f5-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="187f5-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="187f5-387">Az.Aks</span></span>
* <span data-ttu-id="187f5-388">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="187f5-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-389">Az.Automation</span></span>
* <span data-ttu-id="187f5-390">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="187f5-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="187f5-391">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="187f5-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="187f5-392">Az.Cdn</span></span>
* <span data-ttu-id="187f5-393">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-394">Az.Compute</span></span>
* <span data-ttu-id="187f5-395">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="187f5-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="187f5-396">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="187f5-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="187f5-397">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="187f5-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="187f5-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="187f5-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="187f5-399">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="187f5-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="187f5-400">Az.DataFactory</span></span>
* <span data-ttu-id="187f5-401">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="187f5-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="187f5-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="187f5-403">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="187f5-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="187f5-404">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="187f5-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="187f5-405">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="187f5-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="187f5-406">Az.IotHub</span></span>
* <span data-ttu-id="187f5-407">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="187f5-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="187f5-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="187f5-408">Az.KeyVault</span></span>
* <span data-ttu-id="187f5-409">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-410">Az.Network</span></span>
* <span data-ttu-id="187f5-411">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-412">Az.Resources</span></span>
* <span data-ttu-id="187f5-413">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="187f5-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="187f5-414">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="187f5-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="187f5-415">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="187f5-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="187f5-416">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="187f5-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="187f5-417">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="187f5-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="187f5-418">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="187f5-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="187f5-419">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="187f5-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="187f5-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="187f5-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="187f5-421">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="187f5-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="187f5-422">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="187f5-422">Fix some error messages.</span></span>
* <span data-ttu-id="187f5-423">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="187f5-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="187f5-424">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="187f5-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="187f5-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="187f5-425">Az.SignalR</span></span>
* <span data-ttu-id="187f5-426">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-427">Az.Sql</span></span>
* <span data-ttu-id="187f5-428">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="187f5-429">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="187f5-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="187f5-430">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="187f5-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="187f5-431">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="187f5-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="187f5-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-432">Az.Storage</span></span>
* <span data-ttu-id="187f5-433">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="187f5-434">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="187f5-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="187f5-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="187f5-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="187f5-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="187f5-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="187f5-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="187f5-437">Az.TrafficManager</span></span>
* <span data-ttu-id="187f5-438">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="187f5-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-439">Az.Websites</span></span>
* <span data-ttu-id="187f5-440">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="187f5-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="187f5-441">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="187f5-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="187f5-442">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="187f5-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="187f5-443">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="187f5-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="187f5-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-444">Az.Accounts</span></span>
* <span data-ttu-id="187f5-445">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="187f5-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-446">Az.Compute</span></span>
* <span data-ttu-id="187f5-447">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="187f5-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="187f5-448">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="187f5-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="187f5-449">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="187f5-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="187f5-451">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="187f5-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="187f5-452">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="187f5-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="187f5-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="187f5-453">Az.EventGrid</span></span>
* <span data-ttu-id="187f5-454">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="187f5-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="187f5-455">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="187f5-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="187f5-456">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="187f5-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="187f5-457">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="187f5-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="187f5-458">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="187f5-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="187f5-459">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="187f5-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="187f5-460">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="187f5-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="187f5-461">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="187f5-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="187f5-462">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="187f5-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="187f5-463">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="187f5-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="187f5-464">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="187f5-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="187f5-465">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="187f5-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="187f5-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="187f5-466">Az.IotHub</span></span>
* <span data-ttu-id="187f5-467">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="187f5-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="187f5-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="187f5-468">Az.LogicApp</span></span>
* <span data-ttu-id="187f5-469">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="187f5-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-470">Az.Resources</span></span>
* <span data-ttu-id="187f5-471">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="187f5-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="187f5-472">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="187f5-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="187f5-473">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="187f5-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="187f5-474">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="187f5-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="187f5-475">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="187f5-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="187f5-476">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="187f5-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="187f5-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="187f5-477">Az.SignalR</span></span>
* <span data-ttu-id="187f5-478">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-479">Az.Sql</span></span>
* <span data-ttu-id="187f5-480">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="187f5-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="187f5-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-481">Az.Storage</span></span>
* <span data-ttu-id="187f5-482">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="187f5-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="187f5-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="187f5-483">New-AzStorageContext</span></span>
* <span data-ttu-id="187f5-484">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="187f5-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="187f5-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="187f5-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="187f5-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-486">Az.Websites</span></span>
* <span data-ttu-id="187f5-487">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="187f5-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="187f5-488">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="187f5-489">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="187f5-490">Généralités</span><span class="sxs-lookup"><span data-stu-id="187f5-490">General</span></span>

- <span data-ttu-id="187f5-491">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="187f5-491">General Availability of Az Module</span></span>
- <span data-ttu-id="187f5-492">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="187f5-492">Online help for each module</span></span>
- <span data-ttu-id="187f5-493">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="187f5-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="187f5-494">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="187f5-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="187f5-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-495">Az.Accounts</span></span>
- <span data-ttu-id="187f5-496">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="187f5-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="187f5-497">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="187f5-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="187f5-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="187f5-498">Az.ApiManagement</span></span>
- <span data-ttu-id="187f5-499">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="187f5-499">Fixes for #7002</span></span>
- <span data-ttu-id="187f5-500">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="187f5-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="187f5-501">Az.Batch</span></span>
- <span data-ttu-id="187f5-502">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="187f5-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="187f5-503">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="187f5-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="187f5-504">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="187f5-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="187f5-505">Az.Billing</span></span>
- <span data-ttu-id="187f5-506">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="187f5-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="187f5-507">Az.CognitivServices</span></span>
- <span data-ttu-id="187f5-508">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="187f5-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="187f5-509">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="187f5-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="187f5-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="187f5-511">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="187f5-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="187f5-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="187f5-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="187f5-513">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="187f5-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="187f5-515">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="187f5-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="187f5-516">Az.Monitor</span></span>
- <span data-ttu-id="187f5-517">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="187f5-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="187f5-518">Az.KeyVault</span></span>
- <span data-ttu-id="187f5-519">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="187f5-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="187f5-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="187f5-520">Az.MachineLearning</span></span>
- <span data-ttu-id="187f5-521">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="187f5-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="187f5-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="187f5-522">Az.Media</span></span>
- <span data-ttu-id="187f5-523">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="187f5-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="187f5-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-524">Az.Network</span></span>
<span data-ttu-id="187f5-525">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="187f5-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="187f5-526">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="187f5-526">New cmdlets added:</span></span>
        - <span data-ttu-id="187f5-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="187f5-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="187f5-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="187f5-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="187f5-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="187f5-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="187f5-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="187f5-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="187f5-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="187f5-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="187f5-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="187f5-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="187f5-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="187f5-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="187f5-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="187f5-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="187f5-535">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="187f5-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="187f5-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="187f5-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="187f5-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="187f5-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="187f5-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="187f5-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="187f5-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="187f5-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="187f5-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="187f5-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="187f5-541">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="187f5-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="187f5-542">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="187f5-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="187f5-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="187f5-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="187f5-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="187f5-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="187f5-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="187f5-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="187f5-546">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="187f5-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="187f5-547">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="187f5-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="187f5-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="187f5-549">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="187f5-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="187f5-550">Az.Profile</span></span>
- <span data-ttu-id="187f5-551">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="187f5-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="187f5-553">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="187f5-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-554">Az.Resources</span></span>
- <span data-ttu-id="187f5-555">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="187f5-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="187f5-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="187f5-557">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="187f5-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="187f5-558">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="187f5-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="187f5-559">Az.SIgnalR</span></span>
- <span data-ttu-id="187f5-560">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="187f5-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="187f5-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-561">Az.Sql</span></span>
- <span data-ttu-id="187f5-562">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="187f5-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="187f5-563">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="187f5-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="187f5-564">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="187f5-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-565">Az.Storage</span></span>
- <span data-ttu-id="187f5-566">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="187f5-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-567">Az.Websites</span></span>
- <span data-ttu-id="187f5-568">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="187f5-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="187f5-569">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="187f5-570">Généralités</span><span class="sxs-lookup"><span data-stu-id="187f5-570">General</span></span>

* <span data-ttu-id="187f5-571">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="187f5-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="187f5-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-572">Az.Compute</span></span>

* <span data-ttu-id="187f5-573">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="187f5-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="187f5-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="187f5-575">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="187f5-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="187f5-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="187f5-576">Az.FrontDoor</span></span>

* <span data-ttu-id="187f5-577">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="187f5-577">Fixed some broken links</span></span>
    - <span data-ttu-id="187f5-578">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="187f5-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="187f5-579">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="187f5-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="187f5-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="187f5-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="187f5-581">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="187f5-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="187f5-582">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="187f5-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="187f5-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-583">Az.Resources</span></span>

* <span data-ttu-id="187f5-584">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="187f5-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="187f5-585">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="187f5-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="187f5-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-586">Az.Sql</span></span>

* <span data-ttu-id="187f5-587">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="187f5-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="187f5-588">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="187f5-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="187f5-589">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="187f5-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="187f5-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-590">Az.Storage</span></span>

* <span data-ttu-id="187f5-591">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="187f5-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="187f5-592">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="187f5-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="187f5-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="187f5-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="187f5-594">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="187f5-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="187f5-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="187f5-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="187f5-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="187f5-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="187f5-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-597">Az.Websites</span></span>

* <span data-ttu-id="187f5-598">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="187f5-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="187f5-599">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="187f5-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="187f5-600">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="187f5-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="187f5-601">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="187f5-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="187f5-602">Az.ApiManagement</span></span>
* <span data-ttu-id="187f5-603">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="187f5-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="187f5-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="187f5-604">Az.Automation</span></span>
* <span data-ttu-id="187f5-605">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="187f5-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="187f5-606">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="187f5-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="187f5-607">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="187f5-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="187f5-608">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="187f5-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="187f5-609">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="187f5-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="187f5-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-610">Az.Compute</span></span>
* <span data-ttu-id="187f5-611">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="187f5-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="187f5-612">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="187f5-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="187f5-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="187f5-614">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="187f5-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="187f5-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="187f5-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="187f5-616">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="187f5-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="187f5-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-617">Az.Network</span></span>
* <span data-ttu-id="187f5-618">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="187f5-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="187f5-619">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="187f5-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="187f5-620">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="187f5-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="187f5-621">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="187f5-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="187f5-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="187f5-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="187f5-623">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="187f5-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="187f5-624">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="187f5-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="187f5-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="187f5-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="187f5-626">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="187f5-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="187f5-627">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="187f5-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="187f5-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="187f5-628">Az.Relay</span></span>
* <span data-ttu-id="187f5-629">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="187f5-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="187f5-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-630">Az.Resources</span></span>
* <span data-ttu-id="187f5-631">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="187f5-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="187f5-632">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="187f5-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="187f5-633">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="187f5-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="187f5-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="187f5-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="187f5-635">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="187f5-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="187f5-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-636">Az.Sql</span></span>
* <span data-ttu-id="187f5-637">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="187f5-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="187f5-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="187f5-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="187f5-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="187f5-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="187f5-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="187f5-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="187f5-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="187f5-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="187f5-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="187f5-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="187f5-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="187f5-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="187f5-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="187f5-646">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="187f5-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="187f5-647">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="187f5-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="187f5-648">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="187f5-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="187f5-649">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="187f5-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="187f5-650">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="187f5-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="187f5-651">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="187f5-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="187f5-652">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="187f5-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="187f5-653">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="187f5-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="187f5-654">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="187f5-655">Généralités</span><span class="sxs-lookup"><span data-stu-id="187f5-655">General</span></span>
* <span data-ttu-id="187f5-656">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="187f5-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="187f5-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="187f5-657">Az.Profile</span></span>
* <span data-ttu-id="187f5-658">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="187f5-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="187f5-659">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="187f5-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="187f5-660">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="187f5-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="187f5-661">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="187f5-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="187f5-662">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="187f5-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="187f5-663">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="187f5-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="187f5-664">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="187f5-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="187f5-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="187f5-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="187f5-666">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="187f5-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-667">Az.Compute</span></span>
* <span data-ttu-id="187f5-668">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="187f5-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="187f5-669">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="187f5-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="187f5-670">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="187f5-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="187f5-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="187f5-672">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="187f5-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="187f5-673">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="187f5-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="187f5-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="187f5-674">Az.Insights</span></span>
* <span data-ttu-id="187f5-675">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="187f5-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="187f5-676">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="187f5-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="187f5-677">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="187f5-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="187f5-678">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="187f5-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-679">Az.Network</span></span>
* <span data-ttu-id="187f5-680">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="187f5-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="187f5-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="187f5-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="187f5-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="187f5-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="187f5-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="187f5-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="187f5-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="187f5-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="187f5-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="187f5-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="187f5-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="187f5-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="187f5-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="187f5-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="187f5-688">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="187f5-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-689">Az.Resources</span></span>
* <span data-ttu-id="187f5-690">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="187f5-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="187f5-691">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="187f5-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="187f5-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="187f5-692">Az.ServiceBus</span></span>
* <span data-ttu-id="187f5-693">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="187f5-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="187f5-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="187f5-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="187f5-695">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="187f5-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="187f5-696">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="187f5-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="187f5-697">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="187f5-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="187f5-698">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="187f5-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="187f5-699">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="187f5-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="187f5-700">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="187f5-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="187f5-701">Az.Profile</span></span>
* <span data-ttu-id="187f5-702">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="187f5-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="187f5-703">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="187f5-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-704">Az.Compute</span></span>
* <span data-ttu-id="187f5-705">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="187f5-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="187f5-706">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="187f5-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="187f5-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="187f5-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="187f5-708">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="187f5-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="187f5-709">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="187f5-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="187f5-710">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="187f5-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="187f5-711">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="187f5-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="187f5-712">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="187f5-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-713">Az.Network</span></span>
* <span data-ttu-id="187f5-714">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="187f5-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="187f5-715">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="187f5-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-716">Az.Resources</span></span>
* <span data-ttu-id="187f5-717">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="187f5-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="187f5-718">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="187f5-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="187f5-719">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="187f5-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="187f5-720">Azure.Storage</span></span>
* <span data-ttu-id="187f5-721">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="187f5-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="187f5-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="187f5-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="187f5-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="187f5-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="187f5-724">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="187f5-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="187f5-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="187f5-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="187f5-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="187f5-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="187f5-727">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="187f5-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="187f5-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="187f5-728">Az.Compute</span></span>
* <span data-ttu-id="187f5-729">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="187f5-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="187f5-730">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="187f5-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="187f5-731">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="187f5-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="187f5-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="187f5-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="187f5-733">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="187f5-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="187f5-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="187f5-734">Az.Network</span></span>
* <span data-ttu-id="187f5-735">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="187f5-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="187f5-736">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="187f5-736">new cmdlets added</span></span>
    - <span data-ttu-id="187f5-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="187f5-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="187f5-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="187f5-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="187f5-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="187f5-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="187f5-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="187f5-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="187f5-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="187f5-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="187f5-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="187f5-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="187f5-743">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="187f5-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="187f5-744">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="187f5-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="187f5-745">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="187f5-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="187f5-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="187f5-746">Az.RedisCache</span></span>
* <span data-ttu-id="187f5-747">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="187f5-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="187f5-748">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="187f5-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="187f5-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="187f5-749">Az.Resources</span></span>
* <span data-ttu-id="187f5-750">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="187f5-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="187f5-751">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="187f5-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="187f5-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="187f5-752">Az.Sql</span></span>
* <span data-ttu-id="187f5-753">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="187f5-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="187f5-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="187f5-754">Az.Websites</span></span>
* <span data-ttu-id="187f5-755">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="187f5-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="187f5-756">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="187f5-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="187f5-757">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="187f5-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="187f5-758">Version initiale</span><span class="sxs-lookup"><span data-stu-id="187f5-758">Initial Release</span></span>