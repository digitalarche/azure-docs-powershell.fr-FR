---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048629"
---
## <a name="200---may-2019"></a><span data-ttu-id="cabe4-101">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cabe4-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-102">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-103">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="cabe4-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cabe4-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="cabe4-105">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="cabe4-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cabe4-106">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="cabe4-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-107">Az.Compute</span></span>
* <span data-ttu-id="cabe4-108">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="cabe4-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cabe4-109">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cabe4-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cabe4-110">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cabe4-111">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cabe4-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cabe4-112">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cabe4-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cabe4-113">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cabe4-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="cabe4-114">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="cabe4-114">Breaking changes</span></span>
    - <span data-ttu-id="cabe4-115">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cabe4-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cabe4-116">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="cabe4-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cabe4-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cabe4-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="cabe4-118">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="cabe4-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cabe4-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cabe4-119">Az.Dns</span></span>
* <span data-ttu-id="cabe4-120">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="cabe4-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cabe4-121">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="cabe4-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cabe4-122">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="cabe4-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cabe4-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cabe4-123">Az.FrontDoor</span></span>
* <span data-ttu-id="cabe4-124">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cabe4-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cabe4-125">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="cabe4-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cabe4-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cabe4-126">Az.HDInsight</span></span>
* <span data-ttu-id="cabe4-127">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="cabe4-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cabe4-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cabe4-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cabe4-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cabe4-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cabe4-130">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cabe4-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cabe4-131">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="cabe4-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cabe4-132">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="cabe4-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cabe4-133">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="cabe4-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cabe4-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cabe4-134">Az.Monitor</span></span>
* <span data-ttu-id="cabe4-135">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="cabe4-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="cabe4-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cabe4-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cabe4-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cabe4-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cabe4-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cabe4-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cabe4-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cabe4-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cabe4-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cabe4-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cabe4-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cabe4-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cabe4-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cabe4-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cabe4-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cabe4-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cabe4-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cabe4-147">[Plus d’informations](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="cabe4-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cabe4-148">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="cabe4-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-149">Az.Network</span></span>
* <span data-ttu-id="cabe4-150">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cabe4-151">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="cabe4-151">New cmdlets</span></span>
        - <span data-ttu-id="cabe4-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="cabe4-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cabe4-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cabe4-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cabe4-156">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="cabe4-156">Updated cmdlets</span></span>
        - <span data-ttu-id="cabe4-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cabe4-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cabe4-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cabe4-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cabe4-159">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="cabe4-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cabe4-160">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="cabe4-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cabe4-161">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="cabe4-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cabe4-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cabe4-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="cabe4-163">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="cabe4-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cabe4-164">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cabe4-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cabe4-165">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="cabe4-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="cabe4-167">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="cabe4-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cabe4-168">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cabe4-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cabe4-169">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cabe4-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cabe4-170">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cabe4-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cabe4-171">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="cabe4-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cabe4-172">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="cabe4-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cabe4-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cabe4-173">Az.Relay</span></span>
* <span data-ttu-id="cabe4-174">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="cabe4-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cabe4-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cabe4-175">Az.ServiceBus</span></span>
* <span data-ttu-id="cabe4-176">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="cabe4-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cabe4-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-177">Az.Storage</span></span>
* <span data-ttu-id="cabe4-178">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="cabe4-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cabe4-179">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="cabe4-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cabe4-180">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="cabe4-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cabe4-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="cabe4-182">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="cabe4-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cabe4-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cabe4-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cabe4-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-186">Az.Websites</span></span>
* <span data-ttu-id="cabe4-187">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cabe4-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cabe4-188">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="cabe4-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cabe4-189">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cabe4-190">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="cabe4-190">Highlights since the last major release</span></span>
* <span data-ttu-id="cabe4-191">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="cabe4-191">General availability of `Az` module</span></span>
* <span data-ttu-id="cabe4-192">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cabe4-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cabe4-193">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cabe4-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cabe4-194">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cabe4-195">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="cabe4-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cabe4-196">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cabe4-197">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="cabe4-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cabe4-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-198">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-199">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="cabe4-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cabe4-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cabe4-200">Az.Batch</span></span>
* <span data-ttu-id="cabe4-201">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cabe4-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cabe4-202">Az.Cdn</span></span>
* <span data-ttu-id="cabe4-203">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cabe4-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="cabe4-205">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-206">Az.Compute</span></span>
* <span data-ttu-id="cabe4-207">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="cabe4-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cabe4-208">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cabe4-209">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="cabe4-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cabe4-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cabe4-210">Az.DataFactory</span></span>
* <span data-ttu-id="cabe4-211">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="cabe4-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="cabe4-213">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cabe4-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cabe4-214">Az.EventGrid</span></span>
* <span data-ttu-id="cabe4-215">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="cabe4-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cabe4-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cabe4-216">Az.EventHub</span></span>
* <span data-ttu-id="cabe4-217">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="cabe4-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cabe4-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cabe4-218">Az.HDInsight</span></span>
* <span data-ttu-id="cabe4-219">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cabe4-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cabe4-220">Az.IotHub</span></span>
* <span data-ttu-id="cabe4-221">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cabe4-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cabe4-222">Az.KeyVault</span></span>
* <span data-ttu-id="cabe4-223">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cabe4-224">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="cabe4-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cabe4-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cabe4-225">Az.MachineLearning</span></span>
* <span data-ttu-id="cabe4-226">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cabe4-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cabe4-227">Az.Media</span></span>
* <span data-ttu-id="cabe4-228">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cabe4-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cabe4-229">Az.Monitor</span></span>
  * <span data-ttu-id="cabe4-230">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="cabe4-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cabe4-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cabe4-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cabe4-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cabe4-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cabe4-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cabe4-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cabe4-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cabe4-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cabe4-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cabe4-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cabe4-236">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="cabe4-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-237">Az.Network</span></span>
* <span data-ttu-id="cabe4-238">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cabe4-239">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="cabe4-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cabe4-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cabe4-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="cabe4-241">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cabe4-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cabe4-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="cabe4-243">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cabe4-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cabe4-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cabe4-245">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="cabe4-247">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cabe4-248">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="cabe4-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cabe4-249">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="cabe4-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cabe4-250">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="cabe4-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cabe4-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cabe4-251">Az.RedisCache</span></span>
* <span data-ttu-id="cabe4-252">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-253">Az.Resources</span></span>
* <span data-ttu-id="cabe4-254">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="cabe4-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-255">Az.Sql</span></span>
* <span data-ttu-id="cabe4-256">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="cabe4-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cabe4-257">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cabe4-258">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="cabe4-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cabe4-259">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="cabe4-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cabe4-260">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="cabe4-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cabe4-261">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="cabe4-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cabe4-262">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="cabe4-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-263">Az.Websites</span></span>
* <span data-ttu-id="cabe4-264">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="cabe4-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cabe4-265">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="cabe4-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cabe4-266">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="cabe4-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cabe4-267">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cabe4-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cabe4-268">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cabe4-269">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="cabe4-269">Highlights since the last major release</span></span>
* <span data-ttu-id="cabe4-270">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="cabe4-270">General availability of `Az` module</span></span>
* <span data-ttu-id="cabe4-271">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cabe4-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cabe4-272">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cabe4-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cabe4-273">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cabe4-274">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="cabe4-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cabe4-275">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cabe4-276">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="cabe4-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cabe4-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-277">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-278">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="cabe4-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cabe4-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="cabe4-280">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="cabe4-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cabe4-281">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="cabe4-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cabe4-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-282">Az.Automation</span></span>
* <span data-ttu-id="cabe4-283">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="cabe4-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cabe4-284">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="cabe4-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cabe4-285">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="cabe4-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-286">Az.Compute</span></span>
* <span data-ttu-id="cabe4-287">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cabe4-288">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="cabe4-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="cabe4-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="cabe4-290">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="cabe4-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cabe4-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cabe4-291">Az.DataFactory</span></span>
* <span data-ttu-id="cabe4-292">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="cabe4-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cabe4-293">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cabe4-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-294">Az.Resources</span></span>
* <span data-ttu-id="cabe4-295">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="cabe4-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cabe4-296">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="cabe4-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cabe4-297">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="cabe4-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cabe4-298">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cabe4-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cabe4-299">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="cabe4-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cabe4-300">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cabe4-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-301">Az.Sql</span></span>
* <span data-ttu-id="cabe4-302">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="cabe4-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cabe4-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-303">Az.Storage</span></span>
* <span data-ttu-id="cabe4-304">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="cabe4-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cabe4-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cabe4-305">New-AzStorageContext</span></span>
* <span data-ttu-id="cabe4-306">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="cabe4-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cabe4-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cabe4-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cabe4-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cabe4-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cabe4-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cabe4-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cabe4-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cabe4-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cabe4-311">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="cabe4-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cabe4-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cabe4-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cabe4-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cabe4-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cabe4-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cabe4-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cabe4-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cabe4-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cabe4-316">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cabe4-317">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="cabe4-317">Highlights since the last major release</span></span>
* <span data-ttu-id="cabe4-318">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="cabe4-318">General availability of `Az` module</span></span>
* <span data-ttu-id="cabe4-319">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cabe4-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cabe4-320">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cabe4-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cabe4-321">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cabe4-322">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="cabe4-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cabe4-323">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cabe4-324">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="cabe4-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cabe4-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-325">Az.Automation</span></span>
* <span data-ttu-id="cabe4-326">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="cabe4-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cabe4-327">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="cabe4-327">Dynamic grouping</span></span>
    * <span data-ttu-id="cabe4-328">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="cabe4-328">Pre-Post script</span></span>
    * <span data-ttu-id="cabe4-329">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="cabe4-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-330">Az.Compute</span></span>
* <span data-ttu-id="cabe4-331">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cabe4-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cabe4-332">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="cabe4-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cabe4-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cabe4-333">Az.KeyVault</span></span>
* <span data-ttu-id="cabe4-334">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="cabe4-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-335">Az.Network</span></span>
* <span data-ttu-id="cabe4-336">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="cabe4-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cabe4-337">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="cabe4-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="cabe4-339">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="cabe4-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cabe4-340">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="cabe4-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-341">Az.Resources</span></span>
* <span data-ttu-id="cabe4-342">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cabe4-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cabe4-343">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="cabe4-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-344">Az.Sql</span></span>
* <span data-ttu-id="cabe4-345">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="cabe4-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cabe4-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-346">Az.Storage</span></span>
* <span data-ttu-id="cabe4-347">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="cabe4-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cabe4-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cabe4-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cabe4-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cabe4-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cabe4-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cabe4-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cabe4-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cabe4-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cabe4-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cabe4-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cabe4-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-354">Az.Websites</span></span>
* <span data-ttu-id="cabe4-355">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="cabe4-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="cabe4-356">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cabe4-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-357">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-358">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="cabe4-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cabe4-359">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cabe4-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-360">Az.Automation</span></span>
* <span data-ttu-id="cabe4-361">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cabe4-362">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="cabe4-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cabe4-363">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="cabe4-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cabe4-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cabe4-364">Az.Cdn</span></span>
* <span data-ttu-id="cabe4-365">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="cabe4-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-366">Az.Compute</span></span>
* <span data-ttu-id="cabe4-367">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="cabe4-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cabe4-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cabe4-368">Az.DataFactory</span></span>
* <span data-ttu-id="cabe4-369">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="cabe4-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cabe4-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cabe4-370">Az.LogicApp</span></span>
* <span data-ttu-id="cabe4-371">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="cabe4-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-372">Az.Network</span></span>
* <span data-ttu-id="cabe4-373">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="cabe4-375">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="cabe4-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cabe4-376">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="cabe4-376">SDK Update</span></span>
* <span data-ttu-id="cabe4-377">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cabe4-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cabe4-378">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cabe4-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-379">Az.Resources</span></span>
* <span data-ttu-id="cabe4-380">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="cabe4-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cabe4-381">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cabe4-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cabe4-382">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="cabe4-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cabe4-383">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cabe4-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cabe4-384">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="cabe4-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cabe4-385">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cabe4-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-386">Az.Sql</span></span>
* <span data-ttu-id="cabe4-387">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="cabe4-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cabe4-388">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="cabe4-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cabe4-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-389">Az.Storage</span></span>
* <span data-ttu-id="cabe4-390">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cabe4-391">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cabe4-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="cabe4-393">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="cabe4-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cabe4-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-394">Az.Automation</span></span>
* <span data-ttu-id="cabe4-395">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cabe4-396">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cabe4-397">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cabe4-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="cabe4-399">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="cabe4-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-400">Az.Compute</span></span>
* <span data-ttu-id="cabe4-401">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="cabe4-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cabe4-402">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="cabe4-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cabe4-403">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="cabe4-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cabe4-404">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="cabe4-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="cabe4-406">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="cabe4-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cabe4-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cabe4-407">Az.EventHub</span></span>
* <span data-ttu-id="cabe4-408">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="cabe4-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="cabe4-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cabe4-409">Az.KeyVault</span></span>
* <span data-ttu-id="cabe4-410">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cabe4-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cabe4-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cabe4-411">Az.LogicApp</span></span>
* <span data-ttu-id="cabe4-412">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="cabe4-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cabe4-413">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="cabe4-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cabe4-414">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="cabe4-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cabe4-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cabe4-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cabe4-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cabe4-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cabe4-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cabe4-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cabe4-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cabe4-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cabe4-419">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="cabe4-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cabe4-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cabe4-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cabe4-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cabe4-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cabe4-424">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="cabe4-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cabe4-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cabe4-425">Az.Monitor</span></span>
* <span data-ttu-id="cabe4-426">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="cabe4-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-427">Az.Network</span></span>
* <span data-ttu-id="cabe4-428">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="cabe4-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cabe4-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cabe4-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="cabe4-430">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cabe4-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cabe4-431">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="cabe4-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="cabe4-432">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="cabe4-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="cabe4-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-433">Az.Resources</span></span>
* <span data-ttu-id="cabe4-434">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cabe4-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cabe4-435">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cabe4-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cabe4-436">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="cabe4-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cabe4-437">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="cabe4-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-438">Az.Sql</span></span>
* <span data-ttu-id="cabe4-439">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="cabe4-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cabe4-440">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="cabe4-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-441">Az.Websites</span></span>
* <span data-ttu-id="cabe4-442">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="cabe4-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cabe4-443">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cabe4-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-444">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-445">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cabe4-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cabe4-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-446">Az.AnalysisServices</span></span>
<span data-ttu-id="cabe4-447">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="cabe4-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-448">Az.Compute</span></span>
* <span data-ttu-id="cabe4-449">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="cabe4-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cabe4-450">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cabe4-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cabe4-451">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="cabe4-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-452">Az.RecoveryServices</span></span>
<span data-ttu-id="cabe4-453">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="cabe4-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-454">Az.Resources</span></span>
* <span data-ttu-id="cabe4-455">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="cabe4-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="cabe4-456">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cabe4-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cabe4-457">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="cabe4-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="cabe4-458">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cabe4-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-459">Az.Sql</span></span>
* <span data-ttu-id="cabe4-460">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cabe4-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cabe4-461">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="cabe4-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cabe4-462">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="cabe4-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cabe4-463">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cabe4-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-464">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-465">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="cabe4-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cabe4-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="cabe4-467">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="cabe4-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="cabe4-469">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="cabe4-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cabe4-470">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cabe4-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-471">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-472">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="cabe4-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cabe4-473">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cabe4-474">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="cabe4-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cabe4-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cabe4-475">Az.Aks</span></span>
* <span data-ttu-id="cabe4-476">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cabe4-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-477">Az.Automation</span></span>
* <span data-ttu-id="cabe4-478">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="cabe4-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cabe4-479">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cabe4-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cabe4-480">Az.Cdn</span></span>
* <span data-ttu-id="cabe4-481">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-482">Az.Compute</span></span>
* <span data-ttu-id="cabe4-483">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="cabe4-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cabe4-484">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cabe4-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cabe4-485">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="cabe4-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cabe4-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cabe4-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cabe4-487">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cabe4-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cabe4-488">Az.DataFactory</span></span>
* <span data-ttu-id="cabe4-489">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="cabe4-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="cabe4-491">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="cabe4-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cabe4-492">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cabe4-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cabe4-493">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cabe4-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cabe4-494">Az.IotHub</span></span>
* <span data-ttu-id="cabe4-495">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cabe4-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cabe4-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cabe4-496">Az.KeyVault</span></span>
* <span data-ttu-id="cabe4-497">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-498">Az.Network</span></span>
* <span data-ttu-id="cabe4-499">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-500">Az.Resources</span></span>
* <span data-ttu-id="cabe4-501">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="cabe4-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cabe4-502">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="cabe4-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cabe4-503">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cabe4-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cabe4-504">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="cabe4-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cabe4-505">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="cabe4-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cabe4-506">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="cabe4-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cabe4-507">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cabe4-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cabe4-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cabe4-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="cabe4-509">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cabe4-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cabe4-510">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="cabe4-510">Fix some error messages.</span></span>
* <span data-ttu-id="cabe4-511">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="cabe4-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cabe4-512">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="cabe4-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cabe4-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cabe4-513">Az.SignalR</span></span>
* <span data-ttu-id="cabe4-514">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-515">Az.Sql</span></span>
* <span data-ttu-id="cabe4-516">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cabe4-517">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="cabe4-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cabe4-518">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="cabe4-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cabe4-519">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="cabe4-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cabe4-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-520">Az.Storage</span></span>
* <span data-ttu-id="cabe4-521">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cabe4-522">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="cabe4-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cabe4-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cabe4-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cabe4-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cabe4-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cabe4-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cabe4-525">Az.TrafficManager</span></span>
* <span data-ttu-id="cabe4-526">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-527">Az.Websites</span></span>
* <span data-ttu-id="cabe4-528">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="cabe4-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cabe4-529">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="cabe4-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cabe4-530">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="cabe4-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cabe4-531">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="cabe4-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cabe4-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-532">Az.Accounts</span></span>
* <span data-ttu-id="cabe4-533">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="cabe4-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-534">Az.Compute</span></span>
* <span data-ttu-id="cabe4-535">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="cabe4-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cabe4-536">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="cabe4-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cabe4-537">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="cabe4-539">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="cabe4-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cabe4-540">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="cabe4-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cabe4-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cabe4-541">Az.EventGrid</span></span>
* <span data-ttu-id="cabe4-542">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cabe4-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cabe4-543">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="cabe4-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cabe4-544">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="cabe4-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cabe4-545">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="cabe4-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cabe4-546">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="cabe4-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cabe4-547">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="cabe4-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cabe4-548">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="cabe4-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cabe4-549">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="cabe4-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cabe4-550">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="cabe4-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cabe4-551">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="cabe4-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="cabe4-552">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cabe4-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cabe4-553">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cabe4-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cabe4-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cabe4-554">Az.IotHub</span></span>
* <span data-ttu-id="cabe4-555">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="cabe4-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cabe4-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cabe4-556">Az.LogicApp</span></span>
* <span data-ttu-id="cabe4-557">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="cabe4-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-558">Az.Resources</span></span>
* <span data-ttu-id="cabe4-559">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="cabe4-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cabe4-560">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cabe4-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cabe4-561">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cabe4-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cabe4-562">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="cabe4-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cabe4-563">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="cabe4-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cabe4-564">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cabe4-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cabe4-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cabe4-565">Az.SignalR</span></span>
* <span data-ttu-id="cabe4-566">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-567">Az.Sql</span></span>
* <span data-ttu-id="cabe4-568">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="cabe4-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cabe4-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-569">Az.Storage</span></span>
* <span data-ttu-id="cabe4-570">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="cabe4-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cabe4-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cabe4-571">New-AzStorageContext</span></span>
* <span data-ttu-id="cabe4-572">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="cabe4-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cabe4-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cabe4-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-574">Az.Websites</span></span>
* <span data-ttu-id="cabe4-575">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cabe4-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cabe4-576">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cabe4-577">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cabe4-578">Généralités</span><span class="sxs-lookup"><span data-stu-id="cabe4-578">General</span></span>

- <span data-ttu-id="cabe4-579">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="cabe4-579">General Availability of Az Module</span></span>
- <span data-ttu-id="cabe4-580">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="cabe4-580">Online help for each module</span></span>
- <span data-ttu-id="cabe4-581">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="cabe4-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cabe4-582">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="cabe4-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cabe4-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-583">Az.Accounts</span></span>
- <span data-ttu-id="cabe4-584">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cabe4-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="cabe4-585">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="cabe4-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cabe4-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cabe4-586">Az.ApiManagement</span></span>
- <span data-ttu-id="cabe4-587">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="cabe4-587">Fixes for #7002</span></span>
- <span data-ttu-id="cabe4-588">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cabe4-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cabe4-589">Az.Batch</span></span>
- <span data-ttu-id="cabe4-590">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="cabe4-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cabe4-591">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="cabe4-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cabe4-592">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cabe4-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cabe4-593">Az.Billing</span></span>
- <span data-ttu-id="cabe4-594">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cabe4-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-595">Az.CognitivServices</span></span>
- <span data-ttu-id="cabe4-596">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cabe4-597">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="cabe4-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cabe4-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="cabe4-599">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cabe4-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cabe4-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cabe4-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cabe4-601">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="cabe4-603">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cabe4-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cabe4-604">Az.Monitor</span></span>
- <span data-ttu-id="cabe4-605">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cabe4-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cabe4-606">Az.KeyVault</span></span>
- <span data-ttu-id="cabe4-607">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="cabe4-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cabe4-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cabe4-608">Az.MachineLearning</span></span>
- <span data-ttu-id="cabe4-609">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cabe4-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cabe4-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cabe4-610">Az.Media</span></span>
- <span data-ttu-id="cabe4-611">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cabe4-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cabe4-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-612">Az.Network</span></span>
<span data-ttu-id="cabe4-613">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cabe4-614">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="cabe4-614">New cmdlets added:</span></span>
        - <span data-ttu-id="cabe4-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cabe4-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cabe4-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cabe4-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cabe4-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cabe4-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cabe4-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cabe4-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cabe4-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cabe4-623">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cabe4-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cabe4-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cabe4-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cabe4-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cabe4-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cabe4-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cabe4-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cabe4-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cabe4-629">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="cabe4-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cabe4-630">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cabe4-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cabe4-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cabe4-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cabe4-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cabe4-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cabe4-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cabe4-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cabe4-634">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cabe4-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cabe4-635">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cabe4-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cabe4-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="cabe4-637">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cabe4-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cabe4-638">Az.Profile</span></span>
- <span data-ttu-id="cabe4-639">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cabe4-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="cabe4-641">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cabe4-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-642">Az.Resources</span></span>
- <span data-ttu-id="cabe4-643">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cabe4-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cabe4-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="cabe4-645">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="cabe4-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cabe4-646">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cabe4-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cabe4-647">Az.SIgnalR</span></span>
- <span data-ttu-id="cabe4-648">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cabe4-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cabe4-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-649">Az.Sql</span></span>
- <span data-ttu-id="cabe4-650">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="cabe4-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cabe4-651">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="cabe4-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cabe4-652">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cabe4-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-653">Az.Storage</span></span>
- <span data-ttu-id="cabe4-654">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cabe4-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-655">Az.Websites</span></span>
- <span data-ttu-id="cabe4-656">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="cabe4-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cabe4-657">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cabe4-658">Généralités</span><span class="sxs-lookup"><span data-stu-id="cabe4-658">General</span></span>

* <span data-ttu-id="cabe4-659">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="cabe4-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cabe4-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-660">Az.Compute</span></span>

* <span data-ttu-id="cabe4-661">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="cabe4-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="cabe4-663">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="cabe4-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cabe4-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cabe4-664">Az.FrontDoor</span></span>

* <span data-ttu-id="cabe4-665">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="cabe4-665">Fixed some broken links</span></span>
    - <span data-ttu-id="cabe4-666">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cabe4-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cabe4-667">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="cabe4-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cabe4-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="cabe4-669">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="cabe4-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cabe4-670">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="cabe4-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cabe4-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-671">Az.Resources</span></span>

* <span data-ttu-id="cabe4-672">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cabe4-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cabe4-673">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="cabe4-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cabe4-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-674">Az.Sql</span></span>

* <span data-ttu-id="cabe4-675">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="cabe4-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cabe4-676">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="cabe4-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cabe4-677">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="cabe4-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cabe4-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-678">Az.Storage</span></span>

* <span data-ttu-id="cabe4-679">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cabe4-680">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="cabe4-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cabe4-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cabe4-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cabe4-682">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="cabe4-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="cabe4-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cabe4-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cabe4-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cabe4-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cabe4-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-685">Az.Websites</span></span>

* <span data-ttu-id="cabe4-686">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cabe4-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="cabe4-687">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="cabe4-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cabe4-688">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="cabe4-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cabe4-689">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cabe4-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cabe4-690">Az.ApiManagement</span></span>
* <span data-ttu-id="cabe4-691">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="cabe4-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cabe4-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cabe4-692">Az.Automation</span></span>
* <span data-ttu-id="cabe4-693">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="cabe4-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cabe4-694">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="cabe4-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cabe4-695">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="cabe4-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cabe4-696">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="cabe4-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cabe4-697">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="cabe4-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cabe4-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-698">Az.Compute</span></span>
* <span data-ttu-id="cabe4-699">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="cabe4-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cabe4-700">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="cabe4-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cabe4-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="cabe4-702">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="cabe4-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cabe4-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cabe4-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cabe4-704">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="cabe4-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cabe4-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-705">Az.Network</span></span>
* <span data-ttu-id="cabe4-706">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="cabe4-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cabe4-707">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="cabe4-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cabe4-708">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="cabe4-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="cabe4-709">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cabe4-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cabe4-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cabe4-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cabe4-711">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="cabe4-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cabe4-712">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="cabe4-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cabe4-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cabe4-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cabe4-714">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="cabe4-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cabe4-715">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="cabe4-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cabe4-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cabe4-716">Az.Relay</span></span>
* <span data-ttu-id="cabe4-717">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="cabe4-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cabe4-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-718">Az.Resources</span></span>
* <span data-ttu-id="cabe4-719">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="cabe4-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cabe4-720">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="cabe4-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cabe4-721">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="cabe4-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cabe4-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cabe4-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="cabe4-723">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="cabe4-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cabe4-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-724">Az.Sql</span></span>
* <span data-ttu-id="cabe4-725">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="cabe4-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cabe4-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cabe4-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cabe4-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cabe4-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cabe4-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cabe4-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cabe4-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cabe4-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cabe4-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cabe4-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cabe4-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cabe4-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cabe4-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cabe4-734">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="cabe4-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cabe4-735">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="cabe4-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cabe4-736">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="cabe4-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cabe4-737">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cabe4-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cabe4-738">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cabe4-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cabe4-739">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cabe4-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cabe4-740">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cabe4-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cabe4-741">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="cabe4-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cabe4-742">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cabe4-743">Généralités</span><span class="sxs-lookup"><span data-stu-id="cabe4-743">General</span></span>
* <span data-ttu-id="cabe4-744">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="cabe4-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cabe4-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cabe4-745">Az.Profile</span></span>
* <span data-ttu-id="cabe4-746">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cabe4-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cabe4-747">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="cabe4-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cabe4-748">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cabe4-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cabe4-749">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="cabe4-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cabe4-750">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="cabe4-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cabe4-751">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="cabe4-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cabe4-752">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="cabe4-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cabe4-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="cabe4-754">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cabe4-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-755">Az.Compute</span></span>
* <span data-ttu-id="cabe4-756">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cabe4-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cabe4-757">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cabe4-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cabe4-758">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="cabe4-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="cabe4-760">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="cabe4-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cabe4-761">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="cabe4-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cabe4-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cabe4-762">Az.Insights</span></span>
* <span data-ttu-id="cabe4-763">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="cabe4-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cabe4-764">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="cabe4-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cabe4-765">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="cabe4-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cabe4-766">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="cabe4-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-767">Az.Network</span></span>
* <span data-ttu-id="cabe4-768">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="cabe4-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cabe4-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cabe4-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cabe4-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cabe4-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cabe4-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cabe4-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cabe4-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cabe4-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cabe4-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cabe4-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cabe4-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cabe4-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cabe4-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cabe4-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="cabe4-776">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="cabe4-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-777">Az.Resources</span></span>
* <span data-ttu-id="cabe4-778">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cabe4-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cabe4-779">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="cabe4-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cabe4-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cabe4-780">Az.ServiceBus</span></span>
* <span data-ttu-id="cabe4-781">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="cabe4-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cabe4-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cabe4-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="cabe4-783">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="cabe4-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cabe4-784">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="cabe4-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cabe4-785">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="cabe4-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cabe4-786">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cabe4-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cabe4-787">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="cabe4-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cabe4-788">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cabe4-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cabe4-789">Az.Profile</span></span>
* <span data-ttu-id="cabe4-790">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="cabe4-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cabe4-791">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cabe4-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-792">Az.Compute</span></span>
* <span data-ttu-id="cabe4-793">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="cabe4-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cabe4-794">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="cabe4-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cabe4-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cabe4-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="cabe4-796">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="cabe4-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cabe4-797">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cabe4-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cabe4-798">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="cabe4-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cabe4-799">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="cabe4-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cabe4-800">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cabe4-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-801">Az.Network</span></span>
* <span data-ttu-id="cabe4-802">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="cabe4-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cabe4-803">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="cabe4-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-804">Az.Resources</span></span>
* <span data-ttu-id="cabe4-805">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="cabe4-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cabe4-806">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="cabe4-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cabe4-807">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cabe4-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cabe4-808">Azure.Storage</span></span>
* <span data-ttu-id="cabe4-809">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="cabe4-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cabe4-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cabe4-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cabe4-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cabe4-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cabe4-812">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="cabe4-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cabe4-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cabe4-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="cabe4-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cabe4-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="cabe4-815">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="cabe4-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cabe4-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cabe4-816">Az.Compute</span></span>
* <span data-ttu-id="cabe4-817">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="cabe4-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cabe4-818">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cabe4-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cabe4-819">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="cabe4-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cabe4-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cabe4-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cabe4-821">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="cabe4-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cabe4-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cabe4-822">Az.Network</span></span>
* <span data-ttu-id="cabe4-823">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="cabe4-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cabe4-824">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="cabe4-824">new cmdlets added</span></span>
    - <span data-ttu-id="cabe4-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cabe4-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cabe4-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cabe4-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cabe4-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cabe4-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cabe4-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cabe4-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cabe4-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cabe4-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cabe4-831">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="cabe4-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cabe4-832">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="cabe4-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cabe4-833">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="cabe4-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cabe4-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cabe4-834">Az.RedisCache</span></span>
* <span data-ttu-id="cabe4-835">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="cabe4-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cabe4-836">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="cabe4-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cabe4-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cabe4-837">Az.Resources</span></span>
* <span data-ttu-id="cabe4-838">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cabe4-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cabe4-839">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="cabe4-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cabe4-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cabe4-840">Az.Sql</span></span>
* <span data-ttu-id="cabe4-841">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="cabe4-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cabe4-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cabe4-842">Az.Websites</span></span>
* <span data-ttu-id="cabe4-843">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="cabe4-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cabe4-844">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="cabe4-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cabe4-845">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="cabe4-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cabe4-846">Version initiale</span><span class="sxs-lookup"><span data-stu-id="cabe4-846">Initial Release</span></span>