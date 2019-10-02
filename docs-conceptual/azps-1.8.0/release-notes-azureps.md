---
title: Notes de publication Azure PowerShell
description: Découvrez toutes les dernières mises à jour des modules Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319305"
---
## <a name="180---april-2019"></a><span data-ttu-id="abfe4-103">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abfe4-104">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="abfe4-104">Highlights since the last major release</span></span>
* <span data-ttu-id="abfe4-105">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="abfe4-105">General availability of `Az` module</span></span>
* <span data-ttu-id="abfe4-106">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="abfe4-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="abfe4-107">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="abfe4-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="abfe4-108">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="abfe4-109">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="abfe4-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abfe4-110">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="abfe4-111">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="abfe4-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abfe4-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-112">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-113">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="abfe4-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="abfe4-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abfe4-114">Az.Batch</span></span>
* <span data-ttu-id="abfe4-115">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abfe4-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abfe4-116">Az.Cdn</span></span>
* <span data-ttu-id="abfe4-117">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="abfe4-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="abfe4-119">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-120">Az.Compute</span></span>
* <span data-ttu-id="abfe4-121">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="abfe4-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="abfe4-122">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abfe4-123">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="abfe4-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abfe4-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abfe4-124">Az.DataFactory</span></span>
* <span data-ttu-id="abfe4-125">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="abfe4-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="abfe4-127">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="abfe4-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="abfe4-128">Az.EventGrid</span></span>
* <span data-ttu-id="abfe4-129">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="abfe4-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abfe4-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abfe4-130">Az.EventHub</span></span>
* <span data-ttu-id="abfe4-131">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="abfe4-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="abfe4-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="abfe4-132">Az.HDInsight</span></span>
* <span data-ttu-id="abfe4-133">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abfe4-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abfe4-134">Az.IotHub</span></span>
* <span data-ttu-id="abfe4-135">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abfe4-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abfe4-136">Az.KeyVault</span></span>
* <span data-ttu-id="abfe4-137">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abfe4-138">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="abfe4-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="abfe4-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="abfe4-139">Az.MachineLearning</span></span>
* <span data-ttu-id="abfe4-140">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="abfe4-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="abfe4-141">Az.Media</span></span>
* <span data-ttu-id="abfe4-142">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abfe4-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abfe4-143">Az.Monitor</span></span>
  * <span data-ttu-id="abfe4-144">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="abfe4-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="abfe4-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="abfe4-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="abfe4-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="abfe4-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="abfe4-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="abfe4-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="abfe4-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="abfe4-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="abfe4-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="abfe4-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="abfe4-150">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="abfe4-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-151">Az.Network</span></span>
* <span data-ttu-id="abfe4-152">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abfe4-153">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="abfe4-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="abfe4-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="abfe4-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="abfe4-155">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abfe4-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abfe4-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="abfe4-157">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="abfe4-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="abfe4-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="abfe4-159">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="abfe4-161">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abfe4-162">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="abfe4-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="abfe4-163">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="abfe4-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="abfe4-164">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="abfe4-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abfe4-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abfe4-165">Az.RedisCache</span></span>
* <span data-ttu-id="abfe4-166">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-167">Az.Resources</span></span>
* <span data-ttu-id="abfe4-168">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="abfe4-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-169">Az.Sql</span></span>
* <span data-ttu-id="abfe4-170">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="abfe4-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="abfe4-171">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abfe4-172">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="abfe4-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="abfe4-173">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="abfe4-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="abfe4-174">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="abfe4-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="abfe4-175">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="abfe4-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="abfe4-176">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="abfe4-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abfe4-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-177">Az.Websites</span></span>
* <span data-ttu-id="abfe4-178">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="abfe4-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="abfe4-179">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="abfe4-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abfe4-180">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="abfe4-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="abfe4-181">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="abfe4-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="abfe4-182">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abfe4-183">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="abfe4-183">Highlights since the last major release</span></span>
* <span data-ttu-id="abfe4-184">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="abfe4-184">General availability of `Az` module</span></span>
* <span data-ttu-id="abfe4-185">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="abfe4-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="abfe4-186">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="abfe4-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="abfe4-187">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="abfe4-188">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="abfe4-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abfe4-189">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="abfe4-190">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="abfe4-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abfe4-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-191">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-192">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="abfe4-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="abfe4-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="abfe4-194">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="abfe4-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="abfe4-195">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="abfe4-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abfe4-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-196">Az.Automation</span></span>
* <span data-ttu-id="abfe4-197">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="abfe4-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="abfe4-198">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="abfe4-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="abfe4-199">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="abfe4-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-200">Az.Compute</span></span>
* <span data-ttu-id="abfe4-201">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="abfe4-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="abfe4-202">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="abfe4-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="abfe4-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="abfe4-204">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="abfe4-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abfe4-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abfe4-205">Az.DataFactory</span></span>
* <span data-ttu-id="abfe4-206">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="abfe4-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="abfe4-207">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="abfe4-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-208">Az.Resources</span></span>
* <span data-ttu-id="abfe4-209">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="abfe4-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="abfe4-210">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="abfe4-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="abfe4-211">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="abfe4-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="abfe4-212">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="abfe4-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="abfe4-213">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="abfe4-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="abfe4-214">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="abfe4-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-215">Az.Sql</span></span>
* <span data-ttu-id="abfe4-216">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="abfe4-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abfe4-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-217">Az.Storage</span></span>
* <span data-ttu-id="abfe4-218">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="abfe4-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="abfe4-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="abfe4-219">New-AzStorageContext</span></span>
* <span data-ttu-id="abfe4-220">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="abfe4-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="abfe4-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="abfe4-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="abfe4-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="abfe4-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="abfe4-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="abfe4-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="abfe4-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="abfe4-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="abfe4-225">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="abfe4-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="abfe4-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abfe4-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="abfe4-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abfe4-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="abfe4-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="abfe4-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="abfe4-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="abfe4-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="abfe4-230">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abfe4-231">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="abfe4-231">Highlights since the last major release</span></span>
* <span data-ttu-id="abfe4-232">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="abfe4-232">General availability of `Az` module</span></span>
* <span data-ttu-id="abfe4-233">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="abfe4-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="abfe4-234">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="abfe4-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="abfe4-235">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="abfe4-236">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="abfe4-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abfe4-237">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="abfe4-238">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="abfe4-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abfe4-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-239">Az.Automation</span></span>
* <span data-ttu-id="abfe4-240">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="abfe4-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="abfe4-241">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="abfe4-241">Dynamic grouping</span></span>
    * <span data-ttu-id="abfe4-242">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="abfe4-242">Pre-Post script</span></span>
    * <span data-ttu-id="abfe4-243">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="abfe4-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-244">Az.Compute</span></span>
* <span data-ttu-id="abfe4-245">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="abfe4-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="abfe4-246">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="abfe4-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abfe4-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abfe4-247">Az.KeyVault</span></span>
* <span data-ttu-id="abfe4-248">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="abfe4-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-249">Az.Network</span></span>
* <span data-ttu-id="abfe4-250">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="abfe4-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="abfe4-251">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="abfe4-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="abfe4-253">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="abfe4-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="abfe4-254">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="abfe4-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-255">Az.Resources</span></span>
* <span data-ttu-id="abfe4-256">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="abfe4-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="abfe4-257">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="abfe4-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-258">Az.Sql</span></span>
* <span data-ttu-id="abfe4-259">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="abfe4-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abfe4-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-260">Az.Storage</span></span>
* <span data-ttu-id="abfe4-261">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="abfe4-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="abfe4-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="abfe4-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="abfe4-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="abfe4-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="abfe4-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="abfe4-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="abfe4-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="abfe4-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="abfe4-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="abfe4-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="abfe4-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="abfe4-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abfe4-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-268">Az.Websites</span></span>
* <span data-ttu-id="abfe4-269">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="abfe4-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="abfe4-270">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abfe4-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-271">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-272">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="abfe4-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="abfe4-273">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="abfe4-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abfe4-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-274">Az.Automation</span></span>
* <span data-ttu-id="abfe4-275">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="abfe4-276">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="abfe4-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="abfe4-277">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="abfe4-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abfe4-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abfe4-278">Az.Cdn</span></span>
* <span data-ttu-id="abfe4-279">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="abfe4-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-280">Az.Compute</span></span>
* <span data-ttu-id="abfe4-281">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="abfe4-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abfe4-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abfe4-282">Az.DataFactory</span></span>
* <span data-ttu-id="abfe4-283">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="abfe4-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abfe4-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abfe4-284">Az.LogicApp</span></span>
* <span data-ttu-id="abfe4-285">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="abfe4-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-286">Az.Network</span></span>
* <span data-ttu-id="abfe4-287">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="abfe4-289">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="abfe4-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="abfe4-290">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="abfe4-290">SDK Update</span></span>
* <span data-ttu-id="abfe4-291">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="abfe4-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="abfe4-292">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="abfe4-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-293">Az.Resources</span></span>
* <span data-ttu-id="abfe4-294">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="abfe4-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="abfe4-295">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="abfe4-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="abfe4-296">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="abfe4-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="abfe4-297">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="abfe4-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="abfe4-298">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="abfe4-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="abfe4-299">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="abfe4-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-300">Az.Sql</span></span>
* <span data-ttu-id="abfe4-301">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="abfe4-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="abfe4-302">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="abfe4-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abfe4-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-303">Az.Storage</span></span>
* <span data-ttu-id="abfe4-304">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abfe4-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="abfe4-305">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="abfe4-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="abfe4-307">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="abfe4-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abfe4-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-308">Az.Automation</span></span>
* <span data-ttu-id="abfe4-309">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="abfe4-310">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="abfe4-311">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="abfe4-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="abfe4-313">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="abfe4-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-314">Az.Compute</span></span>
* <span data-ttu-id="abfe4-315">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="abfe4-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="abfe4-316">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="abfe4-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="abfe4-317">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="abfe4-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="abfe4-318">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="abfe4-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="abfe4-320">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="abfe4-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abfe4-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abfe4-321">Az.EventHub</span></span>
* <span data-ttu-id="abfe4-322">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="abfe4-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="abfe4-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abfe4-323">Az.KeyVault</span></span>
* <span data-ttu-id="abfe4-324">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="abfe4-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abfe4-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abfe4-325">Az.LogicApp</span></span>
* <span data-ttu-id="abfe4-326">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="abfe4-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="abfe4-327">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="abfe4-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="abfe4-328">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="abfe4-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="abfe4-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abfe4-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="abfe4-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abfe4-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="abfe4-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abfe4-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="abfe4-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abfe4-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="abfe4-333">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="abfe4-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="abfe4-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="abfe4-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="abfe4-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="abfe4-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="abfe4-338">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="abfe4-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abfe4-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abfe4-339">Az.Monitor</span></span>
* <span data-ttu-id="abfe4-340">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="abfe4-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-341">Az.Network</span></span>
* <span data-ttu-id="abfe4-342">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="abfe4-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abfe4-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abfe4-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="abfe4-344">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="abfe4-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="abfe4-345">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="abfe4-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="abfe4-346">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="abfe4-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="abfe4-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-347">Az.Resources</span></span>
* <span data-ttu-id="abfe4-348">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="abfe4-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="abfe4-349">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="abfe4-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="abfe4-350">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="abfe4-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="abfe4-351">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="abfe4-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-352">Az.Sql</span></span>
* <span data-ttu-id="abfe4-353">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="abfe4-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="abfe4-354">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="abfe4-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abfe4-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-355">Az.Websites</span></span>
* <span data-ttu-id="abfe4-356">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="abfe4-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="abfe4-357">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abfe4-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-358">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-359">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="abfe4-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="abfe4-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-360">Az.AnalysisServices</span></span>
<span data-ttu-id="abfe4-361">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="abfe4-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-362">Az.Compute</span></span>
* <span data-ttu-id="abfe4-363">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="abfe4-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="abfe4-364">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="abfe4-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="abfe4-365">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="abfe4-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-366">Az.RecoveryServices</span></span>
<span data-ttu-id="abfe4-367">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="abfe4-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-368">Az.Resources</span></span>
* <span data-ttu-id="abfe4-369">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="abfe4-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="abfe4-370">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="abfe4-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="abfe4-371">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="abfe4-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="abfe4-372">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="abfe4-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-373">Az.Sql</span></span>
* <span data-ttu-id="abfe4-374">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="abfe4-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="abfe4-375">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="abfe4-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="abfe4-376">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="abfe4-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="abfe4-377">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abfe4-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-378">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-379">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="abfe4-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="abfe4-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="abfe4-381">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="abfe4-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="abfe4-383">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="abfe4-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="abfe4-384">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abfe4-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-385">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-386">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="abfe4-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abfe4-387">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abfe4-388">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="abfe4-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="abfe4-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="abfe4-389">Az.Aks</span></span>
* <span data-ttu-id="abfe4-390">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abfe4-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-391">Az.Automation</span></span>
* <span data-ttu-id="abfe4-392">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="abfe4-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="abfe4-393">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abfe4-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abfe4-394">Az.Cdn</span></span>
* <span data-ttu-id="abfe4-395">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-396">Az.Compute</span></span>
* <span data-ttu-id="abfe4-397">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="abfe4-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="abfe4-398">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="abfe4-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="abfe4-399">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="abfe4-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="abfe4-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="abfe4-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="abfe4-401">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abfe4-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abfe4-402">Az.DataFactory</span></span>
* <span data-ttu-id="abfe4-403">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="abfe4-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="abfe4-405">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="abfe4-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="abfe4-406">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="abfe4-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="abfe4-407">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abfe4-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abfe4-408">Az.IotHub</span></span>
* <span data-ttu-id="abfe4-409">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="abfe4-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abfe4-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abfe4-410">Az.KeyVault</span></span>
* <span data-ttu-id="abfe4-411">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-412">Az.Network</span></span>
* <span data-ttu-id="abfe4-413">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-414">Az.Resources</span></span>
* <span data-ttu-id="abfe4-415">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="abfe4-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="abfe4-416">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="abfe4-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="abfe4-417">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="abfe4-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="abfe4-418">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="abfe4-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="abfe4-419">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="abfe4-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="abfe4-420">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="abfe4-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="abfe4-421">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="abfe4-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abfe4-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abfe4-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="abfe4-423">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="abfe4-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="abfe4-424">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="abfe4-424">Fix some error messages.</span></span>
* <span data-ttu-id="abfe4-425">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="abfe4-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="abfe4-426">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="abfe4-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="abfe4-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="abfe4-427">Az.SignalR</span></span>
* <span data-ttu-id="abfe4-428">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-429">Az.Sql</span></span>
* <span data-ttu-id="abfe4-430">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abfe4-431">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="abfe4-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="abfe4-432">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="abfe4-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="abfe4-433">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="abfe4-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abfe4-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-434">Az.Storage</span></span>
* <span data-ttu-id="abfe4-435">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abfe4-436">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="abfe4-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="abfe4-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="abfe4-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="abfe4-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="abfe4-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="abfe4-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="abfe4-439">Az.TrafficManager</span></span>
* <span data-ttu-id="abfe4-440">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abfe4-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-441">Az.Websites</span></span>
* <span data-ttu-id="abfe4-442">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="abfe4-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abfe4-443">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="abfe4-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="abfe4-444">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="abfe4-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="abfe4-445">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="abfe4-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abfe4-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-446">Az.Accounts</span></span>
* <span data-ttu-id="abfe4-447">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="abfe4-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-448">Az.Compute</span></span>
* <span data-ttu-id="abfe4-449">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="abfe4-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="abfe4-450">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="abfe4-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="abfe4-451">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="abfe4-453">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="abfe4-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="abfe4-454">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="abfe4-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="abfe4-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="abfe4-455">Az.EventGrid</span></span>
* <span data-ttu-id="abfe4-456">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="abfe4-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="abfe4-457">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="abfe4-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="abfe4-458">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="abfe4-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="abfe4-459">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="abfe4-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="abfe4-460">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="abfe4-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="abfe4-461">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="abfe4-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="abfe4-462">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="abfe4-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="abfe4-463">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="abfe4-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="abfe4-464">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="abfe4-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="abfe4-465">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="abfe4-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="abfe4-466">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="abfe4-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="abfe4-467">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="abfe4-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abfe4-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abfe4-468">Az.IotHub</span></span>
* <span data-ttu-id="abfe4-469">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="abfe4-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abfe4-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abfe4-470">Az.LogicApp</span></span>
* <span data-ttu-id="abfe4-471">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="abfe4-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-472">Az.Resources</span></span>
* <span data-ttu-id="abfe4-473">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="abfe4-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="abfe4-474">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="abfe4-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="abfe4-475">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="abfe4-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="abfe4-476">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="abfe4-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="abfe4-477">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="abfe4-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="abfe4-478">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="abfe4-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="abfe4-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="abfe4-479">Az.SignalR</span></span>
* <span data-ttu-id="abfe4-480">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-481">Az.Sql</span></span>
* <span data-ttu-id="abfe4-482">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="abfe4-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abfe4-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-483">Az.Storage</span></span>
* <span data-ttu-id="abfe4-484">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="abfe4-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="abfe4-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="abfe4-485">New-AzStorageContext</span></span>
* <span data-ttu-id="abfe4-486">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="abfe4-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="abfe4-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="abfe4-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abfe4-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-488">Az.Websites</span></span>
* <span data-ttu-id="abfe4-489">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="abfe4-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="abfe4-490">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="abfe4-491">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="abfe4-492">Généralités</span><span class="sxs-lookup"><span data-stu-id="abfe4-492">General</span></span>

- <span data-ttu-id="abfe4-493">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="abfe4-493">General Availability of Az Module</span></span>
- <span data-ttu-id="abfe4-494">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="abfe4-494">Online help for each module</span></span>
- <span data-ttu-id="abfe4-495">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="abfe4-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="abfe4-496">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="abfe4-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="abfe4-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-497">Az.Accounts</span></span>
- <span data-ttu-id="abfe4-498">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abfe4-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="abfe4-499">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="abfe4-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="abfe4-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abfe4-500">Az.ApiManagement</span></span>
- <span data-ttu-id="abfe4-501">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="abfe4-501">Fixes for #7002</span></span>
- <span data-ttu-id="abfe4-502">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="abfe4-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abfe4-503">Az.Batch</span></span>
- <span data-ttu-id="abfe4-504">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="abfe4-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="abfe4-505">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="abfe4-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="abfe4-506">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="abfe4-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="abfe4-507">Az.Billing</span></span>
- <span data-ttu-id="abfe4-508">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="abfe4-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-509">Az.CognitivServices</span></span>
- <span data-ttu-id="abfe4-510">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="abfe4-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="abfe4-511">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="abfe4-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="abfe4-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="abfe4-513">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="abfe4-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="abfe4-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="abfe4-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="abfe4-515">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="abfe4-517">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="abfe4-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abfe4-518">Az.Monitor</span></span>
- <span data-ttu-id="abfe4-519">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="abfe4-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abfe4-520">Az.KeyVault</span></span>
- <span data-ttu-id="abfe4-521">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="abfe4-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="abfe4-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="abfe4-522">Az.MachineLearning</span></span>
- <span data-ttu-id="abfe4-523">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="abfe4-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="abfe4-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="abfe4-524">Az.Media</span></span>
- <span data-ttu-id="abfe4-525">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="abfe4-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="abfe4-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-526">Az.Network</span></span>
<span data-ttu-id="abfe4-527">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="abfe4-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="abfe4-528">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="abfe4-528">New cmdlets added:</span></span>
        - <span data-ttu-id="abfe4-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abfe4-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abfe4-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abfe4-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abfe4-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abfe4-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="abfe4-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="abfe4-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="abfe4-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="abfe4-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="abfe4-537">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abfe4-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="abfe4-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abfe4-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="abfe4-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="abfe4-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="abfe4-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="abfe4-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="abfe4-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abfe4-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="abfe4-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="abfe4-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="abfe4-543">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="abfe4-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="abfe4-544">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="abfe4-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="abfe4-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abfe4-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="abfe4-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abfe4-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="abfe4-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abfe4-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="abfe4-548">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="abfe4-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="abfe4-549">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="abfe4-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abfe4-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="abfe4-551">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="abfe4-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abfe4-552">Az.Profile</span></span>
- <span data-ttu-id="abfe4-553">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abfe4-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="abfe4-555">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="abfe4-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-556">Az.Resources</span></span>
- <span data-ttu-id="abfe4-557">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="abfe4-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abfe4-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="abfe4-559">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="abfe4-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="abfe4-560">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="abfe4-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="abfe4-561">Az.SIgnalR</span></span>
- <span data-ttu-id="abfe4-562">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="abfe4-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="abfe4-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-563">Az.Sql</span></span>
- <span data-ttu-id="abfe4-564">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="abfe4-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="abfe4-565">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="abfe4-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="abfe4-566">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="abfe4-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-567">Az.Storage</span></span>
- <span data-ttu-id="abfe4-568">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="abfe4-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-569">Az.Websites</span></span>
- <span data-ttu-id="abfe4-570">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="abfe4-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="abfe4-571">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="abfe4-572">Généralités</span><span class="sxs-lookup"><span data-stu-id="abfe4-572">General</span></span>

* <span data-ttu-id="abfe4-573">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="abfe4-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="abfe4-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-574">Az.Compute</span></span>

* <span data-ttu-id="abfe4-575">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="abfe4-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="abfe4-577">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="abfe4-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="abfe4-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abfe4-578">Az.FrontDoor</span></span>

* <span data-ttu-id="abfe4-579">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="abfe4-579">Fixed some broken links</span></span>
    - <span data-ttu-id="abfe4-580">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="abfe4-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="abfe4-581">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="abfe4-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="abfe4-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="abfe4-583">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="abfe4-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="abfe4-584">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="abfe4-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="abfe4-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-585">Az.Resources</span></span>

* <span data-ttu-id="abfe4-586">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="abfe4-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="abfe4-587">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="abfe4-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="abfe4-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-588">Az.Sql</span></span>

* <span data-ttu-id="abfe4-589">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="abfe4-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="abfe4-590">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="abfe4-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="abfe4-591">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="abfe4-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="abfe4-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-592">Az.Storage</span></span>

* <span data-ttu-id="abfe4-593">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abfe4-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="abfe4-594">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="abfe4-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="abfe4-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="abfe4-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="abfe4-596">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="abfe4-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="abfe4-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abfe4-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="abfe4-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abfe4-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="abfe4-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-599">Az.Websites</span></span>

* <span data-ttu-id="abfe4-600">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="abfe4-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="abfe4-601">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="abfe4-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="abfe4-602">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="abfe4-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="abfe4-603">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="abfe4-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abfe4-604">Az.ApiManagement</span></span>
* <span data-ttu-id="abfe4-605">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="abfe4-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="abfe4-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abfe4-606">Az.Automation</span></span>
* <span data-ttu-id="abfe4-607">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="abfe4-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="abfe4-608">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="abfe4-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="abfe4-609">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="abfe4-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="abfe4-610">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="abfe4-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="abfe4-611">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="abfe4-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="abfe4-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-612">Az.Compute</span></span>
* <span data-ttu-id="abfe4-613">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="abfe4-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="abfe4-614">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="abfe4-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="abfe4-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="abfe4-616">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="abfe4-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="abfe4-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="abfe4-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="abfe4-618">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="abfe4-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="abfe4-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-619">Az.Network</span></span>
* <span data-ttu-id="abfe4-620">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="abfe4-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="abfe4-621">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="abfe4-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="abfe4-622">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="abfe4-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="abfe4-623">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="abfe4-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="abfe4-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="abfe4-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="abfe4-625">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="abfe4-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="abfe4-626">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="abfe4-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="abfe4-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="abfe4-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="abfe4-628">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="abfe4-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="abfe4-629">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="abfe4-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="abfe4-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="abfe4-630">Az.Relay</span></span>
* <span data-ttu-id="abfe4-631">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="abfe4-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="abfe4-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-632">Az.Resources</span></span>
* <span data-ttu-id="abfe4-633">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="abfe4-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="abfe4-634">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="abfe4-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="abfe4-635">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="abfe4-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="abfe4-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abfe4-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="abfe4-637">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="abfe4-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="abfe4-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-638">Az.Sql</span></span>
* <span data-ttu-id="abfe4-639">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="abfe4-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="abfe4-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abfe4-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abfe4-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abfe4-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abfe4-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abfe4-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abfe4-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abfe4-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abfe4-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abfe4-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abfe4-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abfe4-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abfe4-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="abfe4-648">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="abfe4-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="abfe4-649">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="abfe4-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="abfe4-650">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="abfe4-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="abfe4-651">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="abfe4-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="abfe4-652">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="abfe4-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="abfe4-653">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="abfe4-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="abfe4-654">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="abfe4-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="abfe4-655">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="abfe4-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="abfe4-656">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="abfe4-657">Généralités</span><span class="sxs-lookup"><span data-stu-id="abfe4-657">General</span></span>
* <span data-ttu-id="abfe4-658">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="abfe4-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="abfe4-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abfe4-659">Az.Profile</span></span>
* <span data-ttu-id="abfe4-660">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="abfe4-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="abfe4-661">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="abfe4-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="abfe4-662">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="abfe4-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="abfe4-663">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="abfe4-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="abfe4-664">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="abfe4-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="abfe4-665">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="abfe4-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="abfe4-666">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="abfe4-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="abfe4-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="abfe4-668">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="abfe4-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-669">Az.Compute</span></span>
* <span data-ttu-id="abfe4-670">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="abfe4-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="abfe4-671">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="abfe4-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="abfe4-672">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="abfe4-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="abfe4-674">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="abfe4-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="abfe4-675">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="abfe4-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="abfe4-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="abfe4-676">Az.Insights</span></span>
* <span data-ttu-id="abfe4-677">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="abfe4-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="abfe4-678">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="abfe4-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="abfe4-679">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="abfe4-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="abfe4-680">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="abfe4-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-681">Az.Network</span></span>
* <span data-ttu-id="abfe4-682">Modification du type de peering en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="abfe4-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="abfe4-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="abfe4-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="abfe4-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="abfe4-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="abfe4-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abfe4-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="abfe4-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="abfe4-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="abfe4-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="abfe4-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="abfe4-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abfe4-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="abfe4-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="abfe4-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="abfe4-690">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="abfe4-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-691">Az.Resources</span></span>
* <span data-ttu-id="abfe4-692">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="abfe4-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="abfe4-693">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="abfe4-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abfe4-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abfe4-694">Az.ServiceBus</span></span>
* <span data-ttu-id="abfe4-695">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="abfe4-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abfe4-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abfe4-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="abfe4-697">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="abfe4-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="abfe4-698">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="abfe4-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="abfe4-699">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="abfe4-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="abfe4-700">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="abfe4-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="abfe4-701">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="abfe4-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="abfe4-702">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="abfe4-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abfe4-703">Az.Profile</span></span>
* <span data-ttu-id="abfe4-704">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="abfe4-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="abfe4-705">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="abfe4-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-706">Az.Compute</span></span>
* <span data-ttu-id="abfe4-707">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="abfe4-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="abfe4-708">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="abfe4-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abfe4-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abfe4-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="abfe4-710">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="abfe4-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="abfe4-711">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="abfe4-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="abfe4-712">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="abfe4-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="abfe4-713">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="abfe4-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="abfe4-714">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="abfe4-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-715">Az.Network</span></span>
* <span data-ttu-id="abfe4-716">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="abfe4-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="abfe4-717">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="abfe4-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-718">Az.Resources</span></span>
* <span data-ttu-id="abfe4-719">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="abfe4-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="abfe4-720">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="abfe4-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="abfe4-721">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="abfe4-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="abfe4-722">Azure.Storage</span></span>
* <span data-ttu-id="abfe4-723">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="abfe4-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="abfe4-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="abfe4-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="abfe4-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="abfe4-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="abfe4-726">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="abfe4-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="abfe4-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="abfe4-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="abfe4-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abfe4-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="abfe4-729">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="abfe4-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abfe4-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abfe4-730">Az.Compute</span></span>
* <span data-ttu-id="abfe4-731">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="abfe4-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="abfe4-732">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="abfe4-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="abfe4-733">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="abfe4-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="abfe4-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="abfe4-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="abfe4-735">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="abfe4-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abfe4-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abfe4-736">Az.Network</span></span>
* <span data-ttu-id="abfe4-737">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="abfe4-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="abfe4-738">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="abfe4-738">new cmdlets added</span></span>
    - <span data-ttu-id="abfe4-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abfe4-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="abfe4-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abfe4-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="abfe4-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abfe4-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="abfe4-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abfe4-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="abfe4-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="abfe4-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="abfe4-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="abfe4-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="abfe4-745">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="abfe4-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="abfe4-746">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="abfe4-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="abfe4-747">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="abfe4-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abfe4-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abfe4-748">Az.RedisCache</span></span>
* <span data-ttu-id="abfe4-749">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="abfe4-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="abfe4-750">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="abfe4-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="abfe4-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abfe4-751">Az.Resources</span></span>
* <span data-ttu-id="abfe4-752">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="abfe4-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="abfe4-753">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="abfe4-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="abfe4-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abfe4-754">Az.Sql</span></span>
* <span data-ttu-id="abfe4-755">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="abfe4-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abfe4-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abfe4-756">Az.Websites</span></span>
* <span data-ttu-id="abfe4-757">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="abfe4-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="abfe4-758">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="abfe4-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="abfe4-759">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="abfe4-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="abfe4-760">Version initiale</span><span class="sxs-lookup"><span data-stu-id="abfe4-760">Initial Release</span></span>