---
ms.openlocfilehash: 96e6d7bc0cc29adc1c0e49ba344d27349454c214
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226437"
---
## <a name="270---september-2019"></a><span data-ttu-id="5a6a9-101">2.7.0 - septembre 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-101">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5a6a9-102">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-102">Az.ApiManagement</span></span>
* <span data-ttu-id="5a6a9-103">Mise à jour de la description du paramètre « -Format » dans la documentation de référence de « Set-AzApiManagementPolicy »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-103">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="5a6a9-104">Suppression des références de la cmdlet dépréciée « Update-AzApiManagementDeployment » dans la documentation de référence.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-104">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="5a6a9-105">Utilisation de « Set-AzApiManagement » à la place.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-105">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-106">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-107">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Register-AzAutomationDscNode »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-107">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="5a6a9-108">Ajout d’une précision sur la restriction de système d’exploitation à Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="5a6a9-108">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="5a6a9-109">Correction de l’exception de référence Null de la comdlet Start-AzAutomationRunbook pour l’option -Wait.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-109">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-110">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-111">Ajout du paramètre UploadSizeInBytes à New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-111">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="5a6a9-112">Ajout du paramètre Incremental à New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-112">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5a6a9-113">Ajouter d’une fonctionnalité de machine virtuelle basse priorité :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-113">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="5a6a9-114">Les paramètres MaxPrice, EvictionPolicy et Priority sont ajoutés à New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-114">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="5a6a9-115">Le paramètre MaxPrice est ajouté aux cmdlets New-AzVmssConfig, Update-AzVM et Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-115">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="5a6a9-116">Correction du problème de référence de machine virtuelle pour la cmdlet AzAvailabilitySet quand elle liste tous les groupes à haute disponibilité inclus dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-116">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="5a6a9-117">Correction de l’exception Null pour Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-117">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="5a6a9-118">Correction de la méthode de recherche de disque dur virtuel pour la position relative de fin.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-118">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="5a6a9-119">Correction du problème UltraSSD pour New-AzVM et Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-119">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-120">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-121">Ajout de 3 nouvelles commandes pour ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription et Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-121">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="5a6a9-122">Mise à jour de la version du SDK .NET ADF vers la version 4.1.3</span><span class="sxs-lookup"><span data-stu-id="5a6a9-122">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5a6a9-123">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5a6a9-123">Az.HDInsight</span></span>
* <span data-ttu-id="5a6a9-124">Explication des changements cassants</span><span class="sxs-lookup"><span data-stu-id="5a6a9-124">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5a6a9-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-125">Az.IotHub</span></span>
* <span data-ttu-id="5a6a9-126">Ajout de la prise en charge pour appeler le basculement d’un IotHub vers la région de reprise d’activité géocouplée.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-126">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="5a6a9-127">Ajout de la prise en charge pour gérer l’enrichissement de message pour un IotHub.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-127">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="5a6a9-128">Les nouvelles cmdlets sont :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-128">New cmdlets are:</span></span>
    - <span data-ttu-id="5a6a9-129">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5a6a9-129">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5a6a9-130">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5a6a9-130">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5a6a9-131">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5a6a9-131">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5a6a9-132">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5a6a9-132">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5a6a9-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-133">Az.Monitor</span></span>
* <span data-ttu-id="5a6a9-134">Pointage vers le dernier SDK Monitor, par exemple, 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="5a6a9-134">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="5a6a9-135">Ajout de changements non cassants aux cmdlets Metrics, c.-à-d. que l’énumération Unit prend en charge plusieurs nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-135">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="5a6a9-136">Il s’agit de cmdlets en lecture seule, donc aucune modification n’est apportée à leur entrée.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-136">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="5a6a9-137">La version d’API des demandes **ActionGroups** est désormais **2019-06-01**, auparavant il s’agissait de la version **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-137">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="5a6a9-138">Les tests de scénario ont été mis à jour pour tenir compte de cette modification.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-138">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="5a6a9-139">Les constructeurs des classes **EmailReceiver** et **WebhookReceiver** ont un nouvel argument obligatoire, à savoir une valeur booléenne appelée **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-139">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="5a6a9-140">Actuellement, la valeur est définie sur **false** pour masquer ce changement cassant par rapport aux cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-140">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="5a6a9-141">**REMARQUE** : Il s’agit d’une modification temporaire qui doit être validée par l’équipe des alertes.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-141">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="5a6a9-142">L’ordre des arguments pour le constructeur de la classe **Source** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-142">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5a6a9-143">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-143">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="5a6a9-144">L’ordre des arguments pour le constructeur de la classe **AlertingAction** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-144">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5a6a9-145">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="5a6a9-146">Prise en charge des critères de seuil dynamique pour l’alerte de métrique V2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-146">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="5a6a9-147">New-AzMetricAlertRuleV2Criteria : création de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="5a6a9-147">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="5a6a9-148">Add-AzMetricAlertRuleV2 : acceptation de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="5a6a9-148">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="5a6a9-149">Améliorations apportées aux cmdlets de règle de requête planifiée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-149">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="5a6a9-150">Les cmdlets acceptent le paramètre « location » dans les deux formats, à savoir l’emplacement (par exemple, usa-est) ou le nom d’affichage de l’emplacement (par exemple, USA Est)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-150">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="5a6a9-151">Illustration correcte du paramètre « Enabled » dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="5a6a9-151">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="5a6a9-152">Ajout d’exemples pour le paramètre facultatif « ActionGroup »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-152">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="5a6a9-153">Amélioration globale des fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="5a6a9-153">Overall improved help files</span></span>
* <span data-ttu-id="5a6a9-154">Correction du bogue lié à la détermination du type d’étendue pour « Set-AzActionRule »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-154">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-155">Az.Network</span></span>
* <span data-ttu-id="5a6a9-156">Correction de l’exemple incorrect dans la documentation de référence de « New-AzApplicationGateway »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-156">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="5a6a9-157">Ajout d’une remarque à la documentation de référence de « Get-AzNetworkWatcherPacketCapturee » à propos de la récupération de toutes les propriétés d’une capture de paquets</span><span class="sxs-lookup"><span data-stu-id="5a6a9-157">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="5a6a9-158">Correction de l’exemple dans la documentation de référence de « Test-AzNetworkWatcherIPFlow » pour énumérer correctement les cartes réseau</span><span class="sxs-lookup"><span data-stu-id="5a6a9-158">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="5a6a9-159">Amélioration de l’analyse des exceptions cloud pour afficher des détails supplémentaires s’ils existent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-159">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="5a6a9-160">Amélioration de l’analyse des exceptions cloud pour gérer un type supplémentaire d’exception de SDK</span><span class="sxs-lookup"><span data-stu-id="5a6a9-160">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="5a6a9-161">Correction du mappage incorrect des modèles de règle de sécurité</span><span class="sxs-lookup"><span data-stu-id="5a6a9-161">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="5a6a9-162">Ajout de propriétés à une interface réseau pour la fonctionnalité d’adresse IP privée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-162">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="5a6a9-163">Ajout de la propriété « PrivateEndpoint » comme type de PSResourceId à PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5a6a9-163">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="5a6a9-164">Ajout de la propriété « PrivateLinkConnectionProperties » comme type de PSIpConfigurationConnectivityInformation à PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-164">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="5a6a9-165">Ajout d’une nouvelle classe de modèle PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-165">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="5a6a9-166">Ajout de « MSSQL » ApplicationRuleProtocolType pour la ressource du Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-166">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="5a6a9-167">Prise en charge de liaisons multiples dans Azure Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="5a6a9-167">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="5a6a9-168">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-168">New cmdlets</span></span>
        - <span data-ttu-id="5a6a9-169">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5a6a9-169">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="5a6a9-170">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-170">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="5a6a9-171">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-171">Updated cmdlet:</span></span>
        - <span data-ttu-id="5a6a9-172">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5a6a9-172">New-VpnSite</span></span>
        - <span data-ttu-id="5a6a9-173">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5a6a9-173">Update-VpnSite</span></span>
        - <span data-ttu-id="5a6a9-174">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-174">New-VpnConnection</span></span>
        - <span data-ttu-id="5a6a9-175">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-175">Update-VpnConnection</span></span>
* <span data-ttu-id="5a6a9-176">Correction des documents de certains exemples PowerShell pour utiliser des cmdlets Az à la place de cmdlets AzureRM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-176">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-177">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-177">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-178">Mise à jour de l’objet AzureVMpolicy avec l’attribut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-178">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="5a6a9-179">Ajout de tests pour la stratégie de machine virtuelle et la restauration du compte de stockage d’origine</span><span class="sxs-lookup"><span data-stu-id="5a6a9-179">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-180">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-180">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-181">Correction du bogue qui empêchait l’appel de New-AzRoleAssignment sans paramètre d’étendue.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-181">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-182">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-182">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-183">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-183">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="5a6a9-184">Ajout de nouvelles cmdlets pour gérer les applications et les services :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-184">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="5a6a9-185">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5a6a9-185">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5a6a9-186">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5a6a9-186">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5a6a9-187">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-187">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5a6a9-188">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-188">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="5a6a9-189">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5a6a9-189">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5a6a9-190">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5a6a9-190">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5a6a9-191">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5a6a9-191">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5a6a9-192">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-192">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5a6a9-193">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-193">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="5a6a9-194">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5a6a9-194">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5a6a9-195">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5a6a9-195">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5a6a9-196">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-196">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5a6a9-197">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="5a6a9-197">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="5a6a9-198">Mise à niveau du SDK Service Fabric vers la version 1.2.0 qui utilise la version d’API du fournisseur de ressources Service Fabric 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-198">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5a6a9-199">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5a6a9-199">Az.SignalR</span></span>
* <span data-ttu-id="5a6a9-200">Ajout de cmdlets Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-200">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-201">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-202">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzSqlElasticPool »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-202">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="5a6a9-203">Ajout d’un exemple vCore à la création d’un pool élastique (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-203">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="5a6a9-204">Suppression de la validation de EmailAddresses et de la vérification que EmailAdmins n’a pas la valeur false quand EmailAddresses est vide dans Set-AzSqlServerAdvancedThreatProtectionPolicy et Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-204">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="5a6a9-205">Activation de la suppression des paramètres d’audit du serveur/de la base de données quand il existe plusieurs paramètres de diagnostic qui activent la catégorie d’audit.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-205">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="5a6a9-206">Correction de la validation des adresses e-mail dans plusieurs cmdlets d’évaluation des vulnérabilités SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting et Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-206">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-207">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-207">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-208">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzStorageAccountKey »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-208">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5a6a9-209">Lors d’un chargement/téléchargement de fichier Azure, prise en charge de la conservation des propriétés SMB des fichiers sources (attributs du fichier, heure de création du fichier, heure de la dernière écriture du fichier) dans le fichier de destination</span><span class="sxs-lookup"><span data-stu-id="5a6a9-209">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="5a6a9-210">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-210">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="5a6a9-211">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-211">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="5a6a9-212">Correction de l’échec de chargement de l’objet blob de blocs avec des propriétés/métadonnées sur ImmutabilityPolicy avec conteneur activé.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-212">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="5a6a9-213">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-213">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="5a6a9-214">Prise en charge de la gestion des partages de fichiers Azure avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-214">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="5a6a9-215">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5a6a9-215">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5a6a9-216">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5a6a9-216">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5a6a9-217">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5a6a9-217">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5a6a9-218">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5a6a9-218">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-219">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-220">Résolution du problème de suppression des balises d’application web lors de la migration de l’application vers un nouvel ASP</span><span class="sxs-lookup"><span data-stu-id="5a6a9-220">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="5a6a9-221">Correction de Publish-AzureWebapp pour un fonctionnement sur Linux et Windows</span><span class="sxs-lookup"><span data-stu-id="5a6a9-221">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="5a6a9-222">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzWebAppPublishingProfile »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-222">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="5a6a9-223">2.6.0 - Août 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-223">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="5a6a9-224">Généralités</span><span class="sxs-lookup"><span data-stu-id="5a6a9-224">General</span></span>
* <span data-ttu-id="5a6a9-225">Correction des fautes de frappe diverses dans de nombreux modules</span><span class="sxs-lookup"><span data-stu-id="5a6a9-225">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-226">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-227">Prise en charge de l’identité MSI affectée à l’utilisateur dans l’authentification Azure Functions (n° 9479)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-227">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5a6a9-228">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5a6a9-228">Az.Aks</span></span>
* <span data-ttu-id="5a6a9-229">Résolution du problème relatif à la sortie de « Get-AzAks »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-229">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="5a6a9-230">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="5a6a9-230">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5a6a9-231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-231">Az.ApiManagement</span></span>
* <span data-ttu-id="5a6a9-232">Corriger le problème https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="5a6a9-232">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="5a6a9-233">Mise à jour de la version de .Net NuGet, qui n’applique pas de restrictions sur productId, apiId, groupId et userId</span><span class="sxs-lookup"><span data-stu-id="5a6a9-233">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="5a6a9-234">**Get-AzApiManagementProduct** : ajout de la prise en charge de l’interrogation de produits à l’aide d’une API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-234">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="5a6a9-235">**New-AzApiManagementApiRevision** : résolution du problème où ApiRevisionDescription n’était pas défini lors de la création d’une révision d’API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="5a6a9-235">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="5a6a9-236">Correction d’une faute de frappe dans le modèle « PsApiManagementOAuth2AuthrozationServer » remplacé par « PsApiManagementOAuth2AuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-236">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5a6a9-237">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5a6a9-237">Az.Batch</span></span>
* <span data-ttu-id="5a6a9-238">Correction d’une faute de frappe dans un message d’aide et la documentation pour mettre Windows en majuscules</span><span class="sxs-lookup"><span data-stu-id="5a6a9-238">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5a6a9-239">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5a6a9-239">Az.Cdn</span></span>
* <span data-ttu-id="5a6a9-240">Correction d’une faute de frappe dans l’application d’assistance du module CDN</span><span class="sxs-lookup"><span data-stu-id="5a6a9-240">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-241">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-242">Ajout de VmssId à l’applet de commande New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-242">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="5a6a9-243">Ajout des paramètres TerminateScheduledEvents et TerminateScheduledEventNotBeforeTimeoutInMinutes à New-AzVmssConfig et Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5a6a9-243">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="5a6a9-244">Ajout de la propriété HyperVGeneration à l’objet image de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="5a6a9-244">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="5a6a9-245">Ajout des fonctionnalités Host et HostGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-245">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="5a6a9-246">Nouvelles applets de commande :   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5a6a9-246">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="5a6a9-247">Le paramètre HostId est ajouté à New-AzVMConfig et New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-247">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="5a6a9-248">Mise à jour de l’exemple dans la documentation « Invoke-AzVMRunCommand » de manière utiliser le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="5a6a9-248">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="5a6a9-249">Mise à jour de la description « -VolumeType » dans la documentation de référence de « Set-AzVMDiskEncryptionExtension » et de « Set-AzVmssDiskEncryptionExtension »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-249">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-250">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-250">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-251">Correction de la faute de frappe pour mettre « Windows » en majuscules dans la documentation de « New-AzDataFactoryEncryptValue »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-251">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="5a6a9-252">Mise à jour de la version du SDK .NET ADF vers la version 4.1.2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-252">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="5a6a9-253">Ajout des paramètres « DataProxyIntegrationRuntimeName », « DataProxyStagingLinkedServiceName » et « DataProxyStagingPath » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin de permettre la configuration du runtime d’intégration auto-hébergé comme proxy pour SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="5a6a9-253">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="5a6a9-254">Mise à jour de PSTriggerRun pour afficher les pipelines déclenchés, le message et les propriétés, et de PSActivityRun pour afficher le type d’activité</span><span class="sxs-lookup"><span data-stu-id="5a6a9-254">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-255">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-255">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-256">Correction de la suspension de Get-DataLakeStoreDeletedItem pour toutes les erreurs ou exceptions à distance.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-256">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5a6a9-257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-257">Az.EventHub</span></span>
* <span data-ttu-id="5a6a9-258">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNteworkRule dans Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-258">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="5a6a9-259">Résolution du problème n° 9558 : Set-AzEventHubNamespace utilise PATCH au lieu de PUT</span><span class="sxs-lookup"><span data-stu-id="5a6a9-259">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="5a6a9-260">Ajout du paramètre EnableKafka à l’applet de commande Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5a6a9-260">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="5a6a9-261">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-261">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="5a6a9-262">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5a6a9-262">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5a6a9-263">Résolution de la faute de frappe où « Azure » était tout en minuscules dans la documentation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-263">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5a6a9-264">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-264">Az.Monitor</span></span>
* <span data-ttu-id="5a6a9-265">Correction du nom de paramètre incorrect dans la documentation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-265">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-266">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-266">Az.Network</span></span>
* <span data-ttu-id="5a6a9-267">Mise à jour dans New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-267">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="5a6a9-268">Dépréciation du paramètre « PublicIpAddress », car il n’est jamais utilisé côté serveur.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-268">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="5a6a9-269">Ajout d’un paramètre facultatif « Primary » qui indique si la configuration IP actuelle est primaire ou non.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-269">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="5a6a9-270">Amélioration de la gestion de l’exception d’erreur de demande à partir du SDK : résolution du problème où les exceptions du SDK n’étaient précédemment pas gérées correctement, ce qui empêchait l’affichage des détails des erreurs de clé</span><span class="sxs-lookup"><span data-stu-id="5a6a9-270">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="5a6a9-271">Ajustement de la logique de validation pour le préfixe IP IPv6 afin de rechercher la longueur de préfixe IPv6 appropriée.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-271">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="5a6a9-272">Mise à jour de Get-AzVirtualNetworkSubnetConfig : Ajout d’un paramètre défini pour obtenir l’ID de ressource de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-272">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="5a6a9-273">Mise à jour de la description du paramètre Location pour AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5a6a9-273">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-274">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-274">Az.OperationalInsights</span></span>
* <span data-ttu-id="5a6a9-275">Mise à jour de la documentation pour « New-AzOperationalInsightsLinuxSyslogDataSource »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-275">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="5a6a9-276">Ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="5a6a9-276">Added example</span></span>
    - <span data-ttu-id="5a6a9-277">Mise à jour de la description du paramètre « -Name »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-277">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="5a6a9-278">Ajout d’un exemple pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-278">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="5a6a9-279">Changement de la description du paramètre -Name pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-279">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-280">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-280">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-281">Mise à jour de « Get-AzRecoveryServicesBackupJobDetail.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-281">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-282">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-282">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-283">Ajout de la prise en charge de la nouvelle API version 2019-05-10 pour Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-283">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="5a6a9-284">Ajout de la prise en charge de « copy.count = 0 » pour les variables, les ressources et les propriétés</span><span class="sxs-lookup"><span data-stu-id="5a6a9-284">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="5a6a9-285">Les ressources avec « condition = false » ou « copy.count = 0 » seront supprimées en mode Complet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-285">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="5a6a9-286">Ajout d’un exemple d’affectation de stratégie au niveau de l’abonnement à la documentation d’aide</span><span class="sxs-lookup"><span data-stu-id="5a6a9-286">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5a6a9-287">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-287">Az.ServiceBus</span></span>
* <span data-ttu-id="5a6a9-288">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNetworkRule dans Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-288">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="5a6a9-289">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-289">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="5a6a9-290">Ajout de la nouvelle commande « Test-AzServiceBusNameAvailability » afin de vérifier la disponibilité du nom pour la file d’attente et la rubrique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-290">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-292">Correction des bogues relatifs à l’applet de commande add node type :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-292">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="5a6a9-293">bogue NullReferenceException quand un groupe de ressources avait d’autres groupes de machines virtuelles identiques non liés au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-293">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="5a6a9-294">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="5a6a9-294">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="5a6a9-295">Correction du bogue où l’applet de commande échouait si virtualNetwork se trouvait dans un groupe de ressources différent de celui du cluster.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-295">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="5a6a9-296">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="5a6a9-296">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="5a6a9-297">Dépréciation de l’applet de commande Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="5a6a9-297">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-298">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-299">Mise à jour de la documentation des anciennes applets de commande d’audit.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-299">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-300">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-300">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-301">Mise à jour de l’aide pour Get/Close-AzStorageFileHandle, en ajoutant d’autres scénarios aux exemples d’applets de commande et mise à jour des descriptions des paramètres</span><span class="sxs-lookup"><span data-stu-id="5a6a9-301">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="5a6a9-302">Prise en charge de StandardBlobTier dans le chargement d’objet blob et la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="5a6a9-302">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="5a6a9-303">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-303">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="5a6a9-304">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-304">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="5a6a9-305">Prise en charge de la priorité de réalimentation dans la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="5a6a9-305">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="5a6a9-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-306">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-307">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-307">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-308">Ajout d’une clarification concernant le paramètre -AppSettings dans Set-AzWebApp et Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a6a9-308">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="5a6a9-309">2.5.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-309">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-310">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-310">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-311">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5a6a9-311">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5a6a9-312">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-312">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5a6a9-313">Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-313">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-314">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-314">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-315">Correction d’une faute de frappe dans la chaîne de ressource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-315">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="5a6a9-316">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-316">Az.CognitiveServices</span></span>
* <span data-ttu-id="5a6a9-317">Prise en charge de NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-317">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-318">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-318">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-319">Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-319">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5a6a9-320">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5a6a9-320">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5a6a9-321">Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication</span><span class="sxs-lookup"><span data-stu-id="5a6a9-321">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="5a6a9-322">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="5a6a9-322">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-323">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-324">Mise à jour du SDK .NET ADF avec la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5a6a9-324">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="5a6a9-325">Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-325">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5a6a9-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-326">Az.EventHub</span></span>
* <span data-ttu-id="5a6a9-327">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5a6a9-327">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5a6a9-328">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="5a6a9-328">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5a6a9-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-329">Az.KeyVault</span></span>
* <span data-ttu-id="5a6a9-330">Possibilité de spécifier KeySize pour les stratégies de certificat</span><span class="sxs-lookup"><span data-stu-id="5a6a9-330">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5a6a9-331">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-331">Az.LogicApp</span></span>
* <span data-ttu-id="5a6a9-332">Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-332">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="5a6a9-333">Ajout d’un nouveau paramètre MapType pour le filtrage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-333">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5a6a9-334">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-334">Az.ManagedServices</span></span>
* <span data-ttu-id="5a6a9-335">Ajout de la prise en charge de l’API version 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-335">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-336">Az.Network</span></span>
* <span data-ttu-id="5a6a9-337">Prise en charge d’un point de terminaison privé et du service de liaison privée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-337">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="5a6a9-338">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-338">New cmdlets</span></span>
        - <span data-ttu-id="5a6a9-339">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a6a9-339">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5a6a9-340">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-340">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5a6a9-341">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-341">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5a6a9-342">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-342">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5a6a9-343">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-343">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5a6a9-344">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-344">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5a6a9-345">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5a6a9-345">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="5a6a9-346">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-346">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="5a6a9-347">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a6a9-347">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="5a6a9-348">Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-348">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="5a6a9-349">Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-349">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="5a6a9-350">Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-350">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="5a6a9-351">Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="5a6a9-351">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="5a6a9-352">Activation du protocole ICMP pour les configurations des règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="5a6a9-352">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="5a6a9-353">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="5a6a9-353">Updated cmdlets</span></span>
        - <span data-ttu-id="5a6a9-354">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-354">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5a6a9-355">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-355">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5a6a9-356">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-356">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5a6a9-357">Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-357">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5a6a9-358">Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-358">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="5a6a9-359">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-359">Updated cmdlet:</span></span>
        - <span data-ttu-id="5a6a9-360">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-360">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5a6a9-361">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-361">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5a6a9-362">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-362">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="5a6a9-363">Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde</span><span class="sxs-lookup"><span data-stu-id="5a6a9-363">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="5a6a9-364">Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-364">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="5a6a9-365">Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-365">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-366">Az.OperationalInsights</span></span>
* <span data-ttu-id="5a6a9-367">Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-367">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="5a6a9-368">Correction de la gestion des expressions régulières null des journaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="5a6a9-368">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-370">Mise à jour de « Get-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-370">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5a6a9-371">Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-371">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="5a6a9-372">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-372">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="5a6a9-373">Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-373">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5a6a9-374">Mise à jour de « Set-AzRecoveryServicesVaultContext.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-374">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="5a6a9-375">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-375">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5a6a9-376">Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-376">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="5a6a9-377">Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-377">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5a6a9-378">Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-378">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="5a6a9-379">Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-379">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-380">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-380">Az.Resources</span></span>
- <span data-ttu-id="5a6a9-381">Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-381">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="5a6a9-382">Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5a6a9-382">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5a6a9-383">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-383">Az.ServiceBus</span></span>
* <span data-ttu-id="5a6a9-384">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5a6a9-384">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5a6a9-385">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="5a6a9-385">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-386">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-387">Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5a6a9-387">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="5a6a9-388">Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="5a6a9-388">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="5a6a9-389">Correction d’une faute de frappe dans un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-389">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-390">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-390">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-391">Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="5a6a9-391">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5a6a9-392">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5a6a9-392">Az.StorageSync</span></span>
* <span data-ttu-id="5a6a9-393">Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-393">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="5a6a9-394">Résolution du problème 9551 pour honorer TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="5a6a9-394">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-395">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-396">Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-396">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="5a6a9-397">Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-397">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="5a6a9-398">Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="5a6a9-398">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="5a6a9-399">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-399">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-400">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-400">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-401">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="5a6a9-401">Add support for profile cmdlets</span></span>
* <span data-ttu-id="5a6a9-402">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-402">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="5a6a9-403">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5a6a9-403">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5a6a9-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-404">Az.Advisor</span></span>
* <span data-ttu-id="5a6a9-405">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-405">GA release of Az.Advisor</span></span>
* <span data-ttu-id="5a6a9-406">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="5a6a9-406">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5a6a9-407">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-407">Az.ApiManagement</span></span>
* <span data-ttu-id="5a6a9-408">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="5a6a9-408">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="5a6a9-409">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-409">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="5a6a9-410">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-410">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="5a6a9-411">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-411">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="5a6a9-412">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="5a6a9-412">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="5a6a9-413">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-413">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="5a6a9-414">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-414">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-415">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-415">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-416">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-416">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-417">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-418">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-418">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-419">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-419">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-420">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-420">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5a6a9-421">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5a6a9-421">Az.EventGrid</span></span>
* <span data-ttu-id="5a6a9-422">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-422">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5a6a9-423">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-423">Az.IotHub</span></span>
* <span data-ttu-id="5a6a9-424">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-424">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-425">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-425">Az.Network</span></span>
* <span data-ttu-id="5a6a9-426">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="5a6a9-426">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="5a6a9-427">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-427">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5a6a9-428">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-428">Az.PolicyInsights</span></span>
* <span data-ttu-id="5a6a9-429">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-429">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="5a6a9-430">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="5a6a9-430">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-431">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-431">Az.OperationalInsights</span></span>
* <span data-ttu-id="5a6a9-432">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-432">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-433">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-433">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-434">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="5a6a9-434">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-435">Az.Resources</span></span>
    - <span data-ttu-id="5a6a9-436">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="5a6a9-436">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="5a6a9-437">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="5a6a9-437">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="5a6a9-438">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="5a6a9-438">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="5a6a9-439">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="5a6a9-439">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5a6a9-440">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-440">Az.ServiceBus</span></span>
* <span data-ttu-id="5a6a9-441">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-441">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-442">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-442">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-443">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-443">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="5a6a9-444">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-444">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="5a6a9-445">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-445">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5a6a9-446">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-446">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5a6a9-447">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-447">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5a6a9-448">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-448">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5a6a9-449">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-449">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5a6a9-450">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-450">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="5a6a9-451">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="5a6a9-451">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-452">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-453">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-453">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="5a6a9-454">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5a6a9-454">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="5a6a9-455">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="5a6a9-455">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="5a6a9-456">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="5a6a9-456">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="5a6a9-457">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="5a6a9-457">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="5a6a9-458">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-458">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5a6a9-459">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-459">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5a6a9-460">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="5a6a9-460">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="5a6a9-461">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5a6a9-461">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="5a6a9-462">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5a6a9-462">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5a6a9-463">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5a6a9-463">Az.StorageSync</span></span>
* <span data-ttu-id="5a6a9-464">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="5a6a9-464">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="5a6a9-465">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-465">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-466">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-467">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="5a6a9-467">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="5a6a9-468">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="5a6a9-468">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="5a6a9-469">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="5a6a9-469">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="5a6a9-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5a6a9-470">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="5a6a9-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5a6a9-471">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-472">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-473">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-473">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="5a6a9-474">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-474">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="5a6a9-475">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5a6a9-475">Az.Dns</span></span>
* <span data-ttu-id="5a6a9-476">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-476">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5a6a9-477">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5a6a9-477">Az.EventGrid</span></span>
* <span data-ttu-id="5a6a9-478">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-478">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="5a6a9-479">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-479">New cmdlets:</span></span>
    - <span data-ttu-id="5a6a9-480">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5a6a9-480">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5a6a9-481">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-481">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5a6a9-482">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5a6a9-482">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5a6a9-483">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-483">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="5a6a9-484">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5a6a9-484">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5a6a9-485">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-485">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5a6a9-486">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5a6a9-486">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5a6a9-487">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-487">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5a6a9-488">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5a6a9-488">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5a6a9-489">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-489">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="5a6a9-490">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5a6a9-490">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5a6a9-491">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-491">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="5a6a9-492">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5a6a9-492">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="5a6a9-493">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-493">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="5a6a9-494">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5a6a9-494">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5a6a9-495">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-495">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="5a6a9-496">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-496">Updated cmdlets:</span></span>
    - <span data-ttu-id="5a6a9-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5a6a9-497">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="5a6a9-498">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-498">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5a6a9-499">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-499">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5a6a9-500">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-500">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="5a6a9-501">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-501">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="5a6a9-502">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="5a6a9-502">Event subscription expiration date,</span></span>
            - <span data-ttu-id="5a6a9-503">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="5a6a9-503">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="5a6a9-504">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-504">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="5a6a9-505">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="5a6a9-505">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="5a6a9-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-506">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="5a6a9-507">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-507">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="5a6a9-508">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5a6a9-508">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="5a6a9-509">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-509">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="5a6a9-510">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-510">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5a6a9-511">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-511">Az.FrontDoor</span></span>
* <span data-ttu-id="5a6a9-512">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5a6a9-512">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="5a6a9-513">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-513">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="5a6a9-514">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="5a6a9-514">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="5a6a9-515">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-515">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-516">Az.Network</span></span>
* <span data-ttu-id="5a6a9-517">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="5a6a9-517">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="5a6a9-518">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-518">New cmdlets</span></span>
        - <span data-ttu-id="5a6a9-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5a6a9-519">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="5a6a9-520">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5a6a9-520">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="5a6a9-521">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-521">New cmdlets</span></span> 
        - <span data-ttu-id="5a6a9-522">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5a6a9-522">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="5a6a9-523">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-523">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="5a6a9-524">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-524">New cmdlets</span></span> 
        - <span data-ttu-id="5a6a9-525">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-525">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="5a6a9-526">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-526">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5a6a9-527">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-527">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5a6a9-528">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-528">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="5a6a9-529">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-529">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5a6a9-530">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a6a9-530">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="5a6a9-531">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-531">New cmdlets</span></span>
        - <span data-ttu-id="5a6a9-532">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a6a9-532">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5a6a9-533">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a6a9-533">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5a6a9-534">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a6a9-534">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5a6a9-535">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-535">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="5a6a9-536">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-536">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="5a6a9-537">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-537">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="5a6a9-538">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-538">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="5a6a9-539">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-539">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="5a6a9-540">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-540">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="5a6a9-541">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5a6a9-541">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="5a6a9-542">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-542">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="5a6a9-543">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-543">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="5a6a9-544">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-544">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="5a6a9-545">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="5a6a9-545">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="5a6a9-546">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-546">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="5a6a9-547">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-547">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="5a6a9-548">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5a6a9-548">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="5a6a9-549">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-549">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="5a6a9-550">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-550">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5a6a9-551">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-551">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="5a6a9-552">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="5a6a9-552">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="5a6a9-553">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-553">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="5a6a9-554">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5a6a9-554">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="5a6a9-555">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-555">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="5a6a9-556">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-556">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5a6a9-557">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-557">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5a6a9-558">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-558">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="5a6a9-560">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-560">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-561">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-561">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-562">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="5a6a9-562">Support for additional Template Export options</span></span>
    - <span data-ttu-id="5a6a9-563">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-563">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5a6a9-564">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-564">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5a6a9-565">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-565">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-566">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-567">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-567">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-568">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-569">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-569">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="5a6a9-570">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="5a6a9-570">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="5a6a9-571">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-571">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="5a6a9-572">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a6a9-572">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5a6a9-573">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a6a9-573">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5a6a9-574">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5a6a9-574">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5a6a9-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5a6a9-575">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="5a6a9-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5a6a9-576">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-577">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-577">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-578">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-578">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="5a6a9-579">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-579">New-AzStorageAccount</span></span>
* <span data-ttu-id="5a6a9-580">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="5a6a9-580">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="5a6a9-581">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-581">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-582">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-583">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="5a6a9-583">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="5a6a9-584">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5a6a9-584">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="5a6a9-585">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-585">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="5a6a9-586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5a6a9-586">Az.Cdn</span></span>
* <span data-ttu-id="5a6a9-587">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-587">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-588">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-589">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-589">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="5a6a9-590">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-590">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5a6a9-591">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-591">Az.EventHub</span></span>
* <span data-ttu-id="5a6a9-592">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-592">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="5a6a9-593">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6a9-593">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-594">Az.Network</span></span>
* <span data-ttu-id="5a6a9-595">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-595">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="5a6a9-596">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="5a6a9-596">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5a6a9-597">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-597">Az.PolicyInsights</span></span>
* <span data-ttu-id="5a6a9-598">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-598">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-600">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="5a6a9-600">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5a6a9-601">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-601">Az.ServiceBus</span></span>
* <span data-ttu-id="5a6a9-602">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6a9-602">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-603">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-603">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-604">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-604">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="5a6a9-605">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-605">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-606">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-606">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-607">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-607">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="5a6a9-608">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-608">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5a6a9-609">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-609">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="5a6a9-610">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-610">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-611">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-611">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-612">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-612">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="5a6a9-613">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-613">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5a6a9-614">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-614">Az.ApiManagement</span></span>
* <span data-ttu-id="5a6a9-615">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-615">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="5a6a9-616">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-616">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="5a6a9-617">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-617">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="5a6a9-618">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="5a6a9-618">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="5a6a9-619">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-619">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="5a6a9-620">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="5a6a9-620">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="5a6a9-621">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-621">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="5a6a9-622">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-622">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="5a6a9-623">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-623">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="5a6a9-624">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="5a6a9-624">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="5a6a9-625">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="5a6a9-625">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="5a6a9-626">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="5a6a9-626">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="5a6a9-627">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="5a6a9-627">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="5a6a9-628">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-628">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="5a6a9-629">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-629">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="5a6a9-630">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-630">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="5a6a9-631">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-631">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="5a6a9-632">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-632">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="5a6a9-633">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-633">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="5a6a9-634">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="5a6a9-634">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="5a6a9-635">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="5a6a9-635">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="5a6a9-636">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-636">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="5a6a9-637">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-637">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="5a6a9-638">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="5a6a9-638">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="5a6a9-639">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-639">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="5a6a9-640">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-640">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="5a6a9-641">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-641">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="5a6a9-642">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-642">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="5a6a9-643">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-643">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="5a6a9-644">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-644">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="5a6a9-645">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="5a6a9-645">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="5a6a9-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="5a6a9-646">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="5a6a9-647">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-647">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="5a6a9-648">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-648">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5a6a9-649">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-649">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="5a6a9-650">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-650">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="5a6a9-651">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-651">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="5a6a9-652">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-652">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="5a6a9-653">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-653">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="5a6a9-654">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-654">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="5a6a9-655">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-655">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5a6a9-656">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-656">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5a6a9-657">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-657">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="5a6a9-658">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-658">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5a6a9-659">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-659">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5a6a9-660">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-660">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5a6a9-661">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-661">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="5a6a9-662">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-662">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="5a6a9-663">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-663">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="5a6a9-664">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-664">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="5a6a9-665">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-665">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="5a6a9-666">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-666">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="5a6a9-667">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-667">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="5a6a9-668">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-668">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="5a6a9-669">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-669">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="5a6a9-670">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-670">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="5a6a9-671">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-671">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5a6a9-672">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-672">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5a6a9-673">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-673">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5a6a9-674">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-674">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5a6a9-675">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5a6a9-675">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5a6a9-676">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-676">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5a6a9-677">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-677">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5a6a9-678">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-678">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5a6a9-679">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-679">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="5a6a9-680">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-680">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="5a6a9-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="5a6a9-681">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="5a6a9-682">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-682">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="5a6a9-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="5a6a9-683">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="5a6a9-684">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-684">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="5a6a9-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="5a6a9-685">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="5a6a9-686">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-686">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="5a6a9-687">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-687">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="5a6a9-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-688">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="5a6a9-689">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-689">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="5a6a9-690">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-690">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="5a6a9-691">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-691">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-692">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-693">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-693">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="5a6a9-694">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="5a6a9-694">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="5a6a9-695">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="5a6a9-695">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="5a6a9-696">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-696">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="5a6a9-697">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="5a6a9-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="5a6a9-698">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-698">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="5a6a9-699">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-699">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-700">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-701">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-701">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="5a6a9-702">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-702">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-703">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-703">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-704">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-704">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5a6a9-705">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-705">Az.Monitor</span></span>
* <span data-ttu-id="5a6a9-706">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="5a6a9-706">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-707">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-707">Az.Network</span></span>
* <span data-ttu-id="5a6a9-708">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="5a6a9-708">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="5a6a9-709">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-709">Updated cmdlet:</span></span>
        - <span data-ttu-id="5a6a9-710">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a6a9-710">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="5a6a9-711">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5a6a9-711">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-712">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-712">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-713">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-713">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-714">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-715">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="5a6a9-715">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="5a6a9-716">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-716">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-717">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-717">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-718">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="5a6a9-718">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5a6a9-719">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-719">Az.CognitiveServices</span></span>
* <span data-ttu-id="5a6a9-720">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-720">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="5a6a9-721">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-721">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-722">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-723">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-723">Proximity placement group feature.</span></span>
    - <span data-ttu-id="5a6a9-724">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-724">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="5a6a9-725">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-725">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="5a6a9-726">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-726">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="5a6a9-727">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-727">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="5a6a9-728">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5a6a9-728">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="5a6a9-729">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="5a6a9-729">Breaking changes</span></span>
    - <span data-ttu-id="5a6a9-730">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-730">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="5a6a9-731">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-731">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5a6a9-732">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5a6a9-732">Az.DeploymentManager</span></span>
* <span data-ttu-id="5a6a9-733">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="5a6a9-733">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="5a6a9-734">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5a6a9-734">Az.Dns</span></span>
* <span data-ttu-id="5a6a9-735">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-735">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="5a6a9-736">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-736">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="5a6a9-737">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-737">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5a6a9-738">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-738">Az.FrontDoor</span></span>
* <span data-ttu-id="5a6a9-739">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-739">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="5a6a9-740">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-740">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="5a6a9-741">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5a6a9-741">Az.HDInsight</span></span>
* <span data-ttu-id="5a6a9-742">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-742">Removed two cmdlets:</span></span>
    - <span data-ttu-id="5a6a9-743">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5a6a9-743">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="5a6a9-744">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5a6a9-744">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5a6a9-745">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5a6a9-745">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5a6a9-746">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-746">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="5a6a9-747">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-747">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="5a6a9-748">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-748">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5a6a9-749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-749">Az.Monitor</span></span>
* <span data-ttu-id="5a6a9-750">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-750">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="5a6a9-751">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5a6a9-751">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="5a6a9-752">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-752">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="5a6a9-753">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5a6a9-753">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="5a6a9-754">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-754">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="5a6a9-755">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-755">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="5a6a9-756">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5a6a9-756">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="5a6a9-757">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-757">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5a6a9-758">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-758">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5a6a9-759">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-759">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5a6a9-760">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-760">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5a6a9-761">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-761">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5a6a9-762">[Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="5a6a9-762">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="5a6a9-763">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-763">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-764">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-764">Az.Network</span></span>
* <span data-ttu-id="5a6a9-765">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-765">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="5a6a9-766">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-766">New cmdlets</span></span>
        - <span data-ttu-id="5a6a9-767">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-767">New-AzNatGateway</span></span>
        - <span data-ttu-id="5a6a9-768">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-768">Get-AzNatGateway</span></span>
        - <span data-ttu-id="5a6a9-769">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-769">Set-AzNatGateway</span></span>
        - <span data-ttu-id="5a6a9-770">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-770">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="5a6a9-771">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="5a6a9-771">Updated cmdlets</span></span>
        - <span data-ttu-id="5a6a9-772">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5a6a9-772">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="5a6a9-773">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5a6a9-773">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="5a6a9-774">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-774">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="5a6a9-775">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-775">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="5a6a9-776">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-776">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5a6a9-777">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-777">Az.PolicyInsights</span></span>
* <span data-ttu-id="5a6a9-778">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-778">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="5a6a9-779">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-779">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="5a6a9-780">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-780">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-782">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-782">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="5a6a9-783">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-783">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="5a6a9-784">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-784">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="5a6a9-785">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-785">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="5a6a9-786">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-786">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="5a6a9-787">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-787">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="5a6a9-788">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5a6a9-788">Az.Relay</span></span>
* <span data-ttu-id="5a6a9-789">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="5a6a9-789">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5a6a9-790">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-790">Az.ServiceBus</span></span>
* <span data-ttu-id="5a6a9-791">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="5a6a9-791">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-792">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-793">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-793">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="5a6a9-794">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-794">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="5a6a9-795">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-795">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="5a6a9-796">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-796">New-AzStorageAccount</span></span>
* <span data-ttu-id="5a6a9-797">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-797">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="5a6a9-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-798">New-AzStorageAccount</span></span>
    - <span data-ttu-id="5a6a9-799">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-799">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="5a6a9-800">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-800">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-801">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-801">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-802">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-802">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="5a6a9-803">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="5a6a9-803">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="5a6a9-804">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-804">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5a6a9-805">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-805">Highlights since the last major release</span></span>
* <span data-ttu-id="5a6a9-806">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="5a6a9-806">General availability of `Az` module</span></span>
* <span data-ttu-id="5a6a9-807">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5a6a9-807">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5a6a9-808">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5a6a9-808">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5a6a9-809">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-809">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5a6a9-810">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-810">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5a6a9-811">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-811">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5a6a9-812">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-812">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-813">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-813">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-814">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="5a6a9-814">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5a6a9-815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5a6a9-815">Az.Batch</span></span>
* <span data-ttu-id="5a6a9-816">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-816">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5a6a9-817">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5a6a9-817">Az.Cdn</span></span>
* <span data-ttu-id="5a6a9-818">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5a6a9-819">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-819">Az.CognitiveServices</span></span>
* <span data-ttu-id="5a6a9-820">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-821">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-821">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-822">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="5a6a9-822">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5a6a9-823">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-823">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5a6a9-824">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="5a6a9-824">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-825">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-826">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-826">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-827">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-828">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-828">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5a6a9-829">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5a6a9-829">Az.EventGrid</span></span>
* <span data-ttu-id="5a6a9-830">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-830">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5a6a9-831">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-831">Az.EventHub</span></span>
* <span data-ttu-id="5a6a9-832">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="5a6a9-832">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="5a6a9-833">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5a6a9-833">Az.HDInsight</span></span>
* <span data-ttu-id="5a6a9-834">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-834">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5a6a9-835">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-835">Az.IotHub</span></span>
* <span data-ttu-id="5a6a9-836">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5a6a9-837">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-837">Az.KeyVault</span></span>
* <span data-ttu-id="5a6a9-838">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5a6a9-839">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="5a6a9-839">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5a6a9-840">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5a6a9-840">Az.MachineLearning</span></span>
* <span data-ttu-id="5a6a9-841">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-841">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5a6a9-842">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5a6a9-842">Az.Media</span></span>
* <span data-ttu-id="5a6a9-843">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5a6a9-844">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-844">Az.Monitor</span></span>
  * <span data-ttu-id="5a6a9-845">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-845">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5a6a9-846">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5a6a9-846">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5a6a9-847">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5a6a9-847">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5a6a9-848">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-848">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5a6a9-849">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-849">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5a6a9-850">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-850">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5a6a9-851">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="5a6a9-851">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-852">Az.Network</span></span>
* <span data-ttu-id="5a6a9-853">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5a6a9-854">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="5a6a9-854">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5a6a9-855">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5a6a9-855">Az.NotificationHubs</span></span>
* <span data-ttu-id="5a6a9-856">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-856">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-857">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-857">Az.OperationalInsights</span></span>
* <span data-ttu-id="5a6a9-858">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5a6a9-859">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5a6a9-859">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5a6a9-860">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-861">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-861">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-862">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5a6a9-863">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-863">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5a6a9-864">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="5a6a9-864">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5a6a9-865">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="5a6a9-865">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5a6a9-866">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5a6a9-866">Az.RedisCache</span></span>
* <span data-ttu-id="5a6a9-867">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-867">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-868">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-868">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-869">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="5a6a9-869">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-870">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-870">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-871">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="5a6a9-871">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5a6a9-872">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-872">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5a6a9-873">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-873">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5a6a9-874">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-874">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5a6a9-875">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-875">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5a6a9-876">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-876">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5a6a9-877">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="5a6a9-877">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-878">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-878">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-879">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="5a6a9-879">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5a6a9-880">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-880">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5a6a9-881">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-881">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5a6a9-882">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-882">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5a6a9-883">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-883">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5a6a9-884">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-884">Highlights since the last major release</span></span>
* <span data-ttu-id="5a6a9-885">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="5a6a9-885">General availability of `Az` module</span></span>
* <span data-ttu-id="5a6a9-886">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5a6a9-886">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5a6a9-887">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5a6a9-887">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5a6a9-888">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-888">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5a6a9-889">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-889">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5a6a9-890">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-890">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5a6a9-891">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-891">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-892">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-892">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-893">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="5a6a9-893">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5a6a9-894">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-894">Az.AnalysisServices</span></span>
* <span data-ttu-id="5a6a9-895">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="5a6a9-895">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5a6a9-896">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="5a6a9-896">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-897">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-897">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-898">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-898">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5a6a9-899">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-899">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5a6a9-900">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-900">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-901">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-901">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-902">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-902">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5a6a9-903">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-903">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="5a6a9-904">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-904">Az.ContainerInstance</span></span>
* <span data-ttu-id="5a6a9-905">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="5a6a9-905">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-906">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-906">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-907">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-907">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5a6a9-908">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-908">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-909">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-909">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-910">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="5a6a9-910">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5a6a9-911">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5a6a9-911">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5a6a9-912">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-912">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5a6a9-913">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5a6a9-913">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5a6a9-914">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="5a6a9-914">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5a6a9-915">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5a6a9-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-916">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-917">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-917">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-918">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-918">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-919">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-919">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5a6a9-920">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a6a9-920">New-AzStorageContext</span></span>
* <span data-ttu-id="5a6a9-921">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-921">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5a6a9-922">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5a6a9-922">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5a6a9-923">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5a6a9-923">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5a6a9-924">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-924">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5a6a9-925">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-925">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5a6a9-926">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="5a6a9-926">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5a6a9-927">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-927">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5a6a9-928">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-928">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5a6a9-929">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-929">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5a6a9-930">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5a6a9-930">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5a6a9-931">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-931">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5a6a9-932">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-932">Highlights since the last major release</span></span>
* <span data-ttu-id="5a6a9-933">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="5a6a9-933">General availability of `Az` module</span></span>
* <span data-ttu-id="5a6a9-934">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5a6a9-934">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5a6a9-935">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5a6a9-935">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5a6a9-936">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-936">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5a6a9-937">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-937">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5a6a9-938">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-938">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5a6a9-939">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-939">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-940">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-941">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-941">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5a6a9-942">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-942">Dynamic grouping</span></span>
    * <span data-ttu-id="5a6a9-943">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="5a6a9-943">Pre-Post script</span></span>
    * <span data-ttu-id="5a6a9-944">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-944">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-945">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-945">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-946">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="5a6a9-946">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5a6a9-947">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-947">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5a6a9-948">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-948">Az.KeyVault</span></span>
* <span data-ttu-id="5a6a9-949">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-949">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-950">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-950">Az.Network</span></span>
* <span data-ttu-id="5a6a9-951">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-951">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5a6a9-952">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-952">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-953">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-953">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-954">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="5a6a9-954">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5a6a9-955">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="5a6a9-955">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-956">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-957">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-957">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5a6a9-958">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-958">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-959">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-959">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-960">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-960">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-961">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-962">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-962">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5a6a9-963">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-963">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5a6a9-964">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-964">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5a6a9-965">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-965">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5a6a9-966">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5a6a9-966">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5a6a9-967">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5a6a9-967">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5a6a9-968">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-968">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-969">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-969">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-970">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="5a6a9-970">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="5a6a9-971">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-971">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-972">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-972">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-973">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-973">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5a6a9-974">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-974">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-975">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-976">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-976">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5a6a9-977">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-977">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5a6a9-978">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="5a6a9-978">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5a6a9-979">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5a6a9-979">Az.Cdn</span></span>
* <span data-ttu-id="5a6a9-980">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-980">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-981">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-982">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="5a6a9-982">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-983">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-984">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="5a6a9-984">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5a6a9-985">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-985">Az.LogicApp</span></span>
* <span data-ttu-id="5a6a9-986">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="5a6a9-986">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-987">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-987">Az.Network</span></span>
* <span data-ttu-id="5a6a9-988">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-988">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-990">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="5a6a9-990">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5a6a9-991">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="5a6a9-991">SDK Update</span></span>
* <span data-ttu-id="5a6a9-992">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5a6a9-992">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5a6a9-993">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5a6a9-993">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-994">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-994">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-995">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-995">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5a6a9-996">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="5a6a9-996">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5a6a9-997">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5a6a9-997">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5a6a9-998">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="5a6a9-998">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5a6a9-999">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5a6a9-999">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5a6a9-1000">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1000">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-1001">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1001">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1002">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1002">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5a6a9-1003">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1003">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-1004">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1004">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-1005">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1005">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5a6a9-1006">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1006">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5a6a9-1007">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1007">Az.AnalysisServices</span></span>
* <span data-ttu-id="5a6a9-1008">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1008">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1009">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-1010">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1010">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5a6a9-1011">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1011">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5a6a9-1012">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1012">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5a6a9-1013">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1013">Az.CognitiveServices</span></span>
* <span data-ttu-id="5a6a9-1014">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1014">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1015">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1016">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1016">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5a6a9-1017">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1017">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5a6a9-1018">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1018">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5a6a9-1019">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1019">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1020">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1020">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-1021">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1021">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5a6a9-1022">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1022">Az.EventHub</span></span>
* <span data-ttu-id="5a6a9-1023">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1023">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="5a6a9-1024">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1024">Az.KeyVault</span></span>
* <span data-ttu-id="5a6a9-1025">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1025">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5a6a9-1026">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1026">Az.LogicApp</span></span>
* <span data-ttu-id="5a6a9-1027">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1027">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5a6a9-1028">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1028">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5a6a9-1029">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1029">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5a6a9-1030">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1030">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5a6a9-1031">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1031">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5a6a9-1032">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1032">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5a6a9-1033">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1033">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5a6a9-1034">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1034">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5a6a9-1035">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1035">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5a6a9-1036">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1036">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5a6a9-1037">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1037">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5a6a9-1038">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1038">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5a6a9-1039">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1039">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5a6a9-1040">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1040">Az.Monitor</span></span>
* <span data-ttu-id="5a6a9-1041">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1041">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1042">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1042">Az.Network</span></span>
* <span data-ttu-id="5a6a9-1043">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1043">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-1044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1044">Az.OperationalInsights</span></span>
* <span data-ttu-id="5a6a9-1045">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1045">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5a6a9-1046">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1046">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="5a6a9-1047">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1047">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1048">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1049">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1049">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5a6a9-1050">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1050">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5a6a9-1051">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5a6a9-1052">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1052">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1053">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1054">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1054">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5a6a9-1055">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1055">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-1056">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1056">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-1057">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1057">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5a6a9-1058">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1058">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-1059">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1059">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-1060">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1060">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5a6a9-1061">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1061">Az.AnalysisServices</span></span>
<span data-ttu-id="5a6a9-1062">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1062">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1063">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1063">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1064">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1064">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5a6a9-1065">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1065">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5a6a9-1066">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1066">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-1067">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1067">Az.RecoveryServices</span></span>
<span data-ttu-id="5a6a9-1068">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1068">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1069">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1069">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1070">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1070">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="5a6a9-1071">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1071">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5a6a9-1072">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1072">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="5a6a9-1073">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1073">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-1074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1074">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1075">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1075">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5a6a9-1076">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1076">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5a6a9-1077">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1077">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5a6a9-1078">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1078">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1079">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-1080">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1080">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5a6a9-1081">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1081">Az.AnalysisServices</span></span>
* <span data-ttu-id="5a6a9-1082">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1082">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-1083">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1083">Az.RecoveryServices</span></span>
* <span data-ttu-id="5a6a9-1084">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1084">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5a6a9-1085">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1085">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-1086">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1086">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-1087">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1087">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5a6a9-1088">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1088">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5a6a9-1089">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1089">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5a6a9-1090">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1090">Az.Aks</span></span>
* <span data-ttu-id="5a6a9-1091">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1091">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5a6a9-1092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1092">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-1093">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1093">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5a6a9-1094">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1094">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5a6a9-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1095">Az.Cdn</span></span>
* <span data-ttu-id="5a6a9-1096">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1096">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1097">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1098">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1098">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5a6a9-1099">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1099">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5a6a9-1100">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1100">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5a6a9-1101">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1101">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5a6a9-1102">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1102">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5a6a9-1103">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1103">Az.DataFactory</span></span>
* <span data-ttu-id="5a6a9-1104">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1104">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1105">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-1106">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1106">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5a6a9-1107">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1107">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5a6a9-1108">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1108">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5a6a9-1109">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1109">Az.IotHub</span></span>
* <span data-ttu-id="5a6a9-1110">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1110">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5a6a9-1111">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1111">Az.KeyVault</span></span>
* <span data-ttu-id="5a6a9-1112">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1112">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1113">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1113">Az.Network</span></span>
* <span data-ttu-id="5a6a9-1114">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1114">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1115">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1116">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1116">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5a6a9-1117">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1117">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5a6a9-1118">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1118">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5a6a9-1119">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1119">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5a6a9-1120">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1120">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5a6a9-1121">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1121">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5a6a9-1122">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1122">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-1123">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1123">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-1124">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1124">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5a6a9-1125">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1125">Fix some error messages.</span></span>
* <span data-ttu-id="5a6a9-1126">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1126">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5a6a9-1127">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1127">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5a6a9-1128">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1128">Az.SignalR</span></span>
* <span data-ttu-id="5a6a9-1129">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1129">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-1130">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1130">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1131">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1131">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5a6a9-1132">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1132">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5a6a9-1133">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1133">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5a6a9-1134">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1134">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-1135">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1135">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-1136">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1136">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5a6a9-1137">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1137">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5a6a9-1138">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1138">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5a6a9-1139">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1139">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5a6a9-1140">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1140">Az.TrafficManager</span></span>
* <span data-ttu-id="5a6a9-1141">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1141">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-1142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1142">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-1143">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1143">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5a6a9-1144">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1144">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5a6a9-1145">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1145">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5a6a9-1146">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1146">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5a6a9-1147">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1147">Az.Accounts</span></span>
* <span data-ttu-id="5a6a9-1148">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1148">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1149">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1149">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1150">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1150">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5a6a9-1151">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1151">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5a6a9-1152">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1152">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1153">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1153">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-1154">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1154">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5a6a9-1155">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1155">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5a6a9-1156">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1156">Az.EventGrid</span></span>
* <span data-ttu-id="5a6a9-1157">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1157">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5a6a9-1158">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1158">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5a6a9-1159">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1159">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5a6a9-1160">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1160">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5a6a9-1161">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1161">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5a6a9-1162">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1162">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5a6a9-1163">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1163">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5a6a9-1164">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1164">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5a6a9-1165">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1165">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5a6a9-1166">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1166">Dead letter endpoint.</span></span>
* <span data-ttu-id="5a6a9-1167">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1167">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5a6a9-1168">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1168">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5a6a9-1169">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1169">Az.IotHub</span></span>
* <span data-ttu-id="5a6a9-1170">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1170">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5a6a9-1171">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1171">Az.LogicApp</span></span>
* <span data-ttu-id="5a6a9-1172">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1172">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1173">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1173">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1174">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1174">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5a6a9-1175">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1175">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5a6a9-1176">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1176">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5a6a9-1177">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1177">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5a6a9-1178">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1178">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5a6a9-1179">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1179">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5a6a9-1180">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1180">Az.SignalR</span></span>
* <span data-ttu-id="5a6a9-1181">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1181">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-1182">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1182">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1183">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1183">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5a6a9-1184">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1184">Az.Storage</span></span>
* <span data-ttu-id="5a6a9-1185">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1185">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5a6a9-1186">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1186">New-AzStorageContext</span></span>
* <span data-ttu-id="5a6a9-1187">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1187">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5a6a9-1188">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1188">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-1189">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1189">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-1190">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1190">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5a6a9-1191">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1191">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5a6a9-1192">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1192">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5a6a9-1193">Généralités</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1193">General</span></span>

- <span data-ttu-id="5a6a9-1194">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1194">General Availability of Az Module</span></span>
- <span data-ttu-id="5a6a9-1195">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1195">Online help for each module</span></span>
- <span data-ttu-id="5a6a9-1196">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1196">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5a6a9-1197">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1197">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5a6a9-1198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1198">Az.Accounts</span></span>
- <span data-ttu-id="5a6a9-1199">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1199">Changed from Az.Profile</span></span>
- <span data-ttu-id="5a6a9-1200">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1200">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5a6a9-1201">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1201">Az.ApiManagement</span></span>
- <span data-ttu-id="5a6a9-1202">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1202">Fixes for #7002</span></span>
- <span data-ttu-id="5a6a9-1203">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1203">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5a6a9-1204">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1204">Az.Batch</span></span>
- <span data-ttu-id="5a6a9-1205">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1205">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5a6a9-1206">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1206">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5a6a9-1207">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5a6a9-1208">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1208">Az.Billing</span></span>
- <span data-ttu-id="5a6a9-1209">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1209">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5a6a9-1210">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1210">Az.CognitivServices</span></span>
- <span data-ttu-id="5a6a9-1211">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1211">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5a6a9-1212">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1212">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5a6a9-1213">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1213">Az.ContainerInstance</span></span>
- <span data-ttu-id="5a6a9-1214">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1214">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5a6a9-1215">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1215">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5a6a9-1216">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1216">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1217">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1217">Az.DataLakeStore</span></span>
- <span data-ttu-id="5a6a9-1218">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5a6a9-1219">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1219">Az.Monitor</span></span>
- <span data-ttu-id="5a6a9-1220">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1220">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5a6a9-1221">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1221">Az.KeyVault</span></span>
- <span data-ttu-id="5a6a9-1222">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1222">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5a6a9-1223">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1223">Az.MachineLearning</span></span>
- <span data-ttu-id="5a6a9-1224">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1224">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5a6a9-1225">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1225">Az.Media</span></span>
- <span data-ttu-id="5a6a9-1226">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1226">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1227">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1227">Az.Network</span></span>
<span data-ttu-id="5a6a9-1228">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1228">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5a6a9-1229">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1229">New cmdlets added:</span></span>
        - <span data-ttu-id="5a6a9-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1230">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5a6a9-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1231">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5a6a9-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1232">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5a6a9-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1233">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5a6a9-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1234">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5a6a9-1235">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1235">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5a6a9-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1236">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5a6a9-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1237">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5a6a9-1238">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1238">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5a6a9-1239">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1239">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5a6a9-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1240">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5a6a9-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1241">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5a6a9-1242">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1242">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5a6a9-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1243">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5a6a9-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1244">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5a6a9-1245">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1245">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5a6a9-1246">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1246">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5a6a9-1247">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1247">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5a6a9-1248">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1248">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5a6a9-1249">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1249">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5a6a9-1250">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1250">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5a6a9-1251">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1251">Az.OperationalInsights</span></span>
- <span data-ttu-id="5a6a9-1252">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5a6a9-1253">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1253">Az.Profile</span></span>
- <span data-ttu-id="5a6a9-1254">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1254">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1255">Az.RecoveryServices</span></span>
- <span data-ttu-id="5a6a9-1256">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1256">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5a6a9-1257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1257">Az.Resources</span></span>
- <span data-ttu-id="5a6a9-1258">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-1259">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1259">Az.ServiceFabric</span></span>
- <span data-ttu-id="5a6a9-1260">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1260">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5a6a9-1261">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1261">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5a6a9-1262">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1262">Az.SIgnalR</span></span>
- <span data-ttu-id="5a6a9-1263">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1263">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5a6a9-1264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1264">Az.Sql</span></span>
- <span data-ttu-id="5a6a9-1265">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1265">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5a6a9-1266">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1266">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5a6a9-1267">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1267">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5a6a9-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1268">Az.Storage</span></span>
- <span data-ttu-id="5a6a9-1269">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5a6a9-1270">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1270">Az.Websites</span></span>
- <span data-ttu-id="5a6a9-1271">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5a6a9-1272">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1272">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5a6a9-1273">Généralités</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1273">General</span></span>

* <span data-ttu-id="5a6a9-1274">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1274">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5a6a9-1275">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1275">Az.Compute</span></span>

* <span data-ttu-id="5a6a9-1276">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1276">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1277">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1277">Az.DataLakeStore</span></span>

* <span data-ttu-id="5a6a9-1278">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1278">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5a6a9-1279">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1279">Az.FrontDoor</span></span>

* <span data-ttu-id="5a6a9-1280">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1280">Fixed some broken links</span></span>
    - <span data-ttu-id="5a6a9-1281">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1281">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5a6a9-1282">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1282">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5a6a9-1283">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1283">Az.RecoveryServices</span></span>

* <span data-ttu-id="5a6a9-1284">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1284">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5a6a9-1285">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1285">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5a6a9-1286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1286">Az.Resources</span></span>

* <span data-ttu-id="5a6a9-1287">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1287">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5a6a9-1288">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1288">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5a6a9-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1289">Az.Sql</span></span>

* <span data-ttu-id="5a6a9-1290">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1290">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5a6a9-1291">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1291">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5a6a9-1292">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1292">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5a6a9-1293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1293">Az.Storage</span></span>

* <span data-ttu-id="5a6a9-1294">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1294">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5a6a9-1295">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1295">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5a6a9-1296">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1296">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5a6a9-1297">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1297">Support Static Website configuration</span></span>
    - <span data-ttu-id="5a6a9-1298">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1298">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5a6a9-1299">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1299">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5a6a9-1300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1300">Az.Websites</span></span>

* <span data-ttu-id="5a6a9-1301">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1301">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="5a6a9-1302">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1302">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5a6a9-1303">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1303">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5a6a9-1304">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1304">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5a6a9-1305">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1305">Az.ApiManagement</span></span>
* <span data-ttu-id="5a6a9-1306">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1306">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5a6a9-1307">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1307">Az.Automation</span></span>
* <span data-ttu-id="5a6a9-1308">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1308">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5a6a9-1309">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1309">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5a6a9-1310">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1310">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5a6a9-1311">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1311">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5a6a9-1312">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1312">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5a6a9-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1313">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1314">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1314">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5a6a9-1315">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1315">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5a6a9-1316">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1316">Az.ContainerInstance</span></span>
* <span data-ttu-id="5a6a9-1317">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1317">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5a6a9-1318">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1318">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5a6a9-1319">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1319">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1320">Az.Network</span></span>
* <span data-ttu-id="5a6a9-1321">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1321">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5a6a9-1322">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1322">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5a6a9-1323">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1323">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="5a6a9-1324">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1324">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5a6a9-1325">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1325">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5a6a9-1326">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1326">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5a6a9-1327">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1327">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5a6a9-1328">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1328">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5a6a9-1329">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1329">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5a6a9-1330">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1330">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5a6a9-1331">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1331">Az.Relay</span></span>
* <span data-ttu-id="5a6a9-1332">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1332">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5a6a9-1333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1333">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1334">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1334">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5a6a9-1335">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1335">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5a6a9-1336">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1336">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-1337">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1337">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-1338">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1338">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5a6a9-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1339">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1340">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1340">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5a6a9-1341">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1341">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5a6a9-1342">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1342">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5a6a9-1343">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1343">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5a6a9-1344">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1344">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5a6a9-1345">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1345">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5a6a9-1346">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1346">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5a6a9-1347">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1347">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5a6a9-1348">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1348">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5a6a9-1349">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1349">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5a6a9-1350">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1350">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5a6a9-1351">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1351">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5a6a9-1352">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1352">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5a6a9-1353">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1353">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5a6a9-1354">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1354">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5a6a9-1355">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1355">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5a6a9-1356">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1356">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5a6a9-1357">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1357">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5a6a9-1358">Généralités</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1358">General</span></span>
* <span data-ttu-id="5a6a9-1359">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1359">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5a6a9-1360">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1360">Az.Profile</span></span>
* <span data-ttu-id="5a6a9-1361">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1361">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5a6a9-1362">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1362">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5a6a9-1363">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1363">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5a6a9-1364">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1364">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5a6a9-1365">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1365">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5a6a9-1366">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1366">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5a6a9-1367">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1367">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5a6a9-1368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1368">Az.CognitiveServices</span></span>
* <span data-ttu-id="5a6a9-1369">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1369">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1370">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1371">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1371">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5a6a9-1372">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1372">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5a6a9-1373">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1373">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1374">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1374">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-1375">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1375">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5a6a9-1376">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1376">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5a6a9-1377">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1377">Az.Insights</span></span>
* <span data-ttu-id="5a6a9-1378">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1378">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5a6a9-1379">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1379">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5a6a9-1380">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1380">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5a6a9-1381">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1381">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1382">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1382">Az.Network</span></span>
* <span data-ttu-id="5a6a9-1383">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1383">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5a6a9-1384">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1384">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5a6a9-1385">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1385">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5a6a9-1386">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1386">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5a6a9-1387">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1387">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5a6a9-1388">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1388">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5a6a9-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1389">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5a6a9-1390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1390">Az.PolicyInsights</span></span>
* <span data-ttu-id="5a6a9-1391">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1391">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1392">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1392">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1393">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1393">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5a6a9-1394">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1394">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5a6a9-1395">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1395">Az.ServiceBus</span></span>
* <span data-ttu-id="5a6a9-1396">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1396">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5a6a9-1397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1397">Az.ServiceFabric</span></span>
* <span data-ttu-id="5a6a9-1398">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1398">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5a6a9-1399">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1399">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5a6a9-1400">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1400">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5a6a9-1401">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1401">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5a6a9-1402">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1402">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5a6a9-1403">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1403">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5a6a9-1404">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1404">Az.Profile</span></span>
* <span data-ttu-id="5a6a9-1405">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1405">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5a6a9-1406">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1406">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1407">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1407">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1408">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1408">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5a6a9-1409">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1409">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5a6a9-1410">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1410">Az.DataLakeStore</span></span>
* <span data-ttu-id="5a6a9-1411">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1411">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5a6a9-1412">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1412">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5a6a9-1413">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1413">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5a6a9-1414">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1414">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5a6a9-1415">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1415">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1416">Az.Network</span></span>
* <span data-ttu-id="5a6a9-1417">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1417">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5a6a9-1418">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1418">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1419">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1420">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1420">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5a6a9-1421">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1421">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5a6a9-1422">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1422">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5a6a9-1423">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1423">Azure.Storage</span></span>
* <span data-ttu-id="5a6a9-1424">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1424">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5a6a9-1425">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1425">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5a6a9-1426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5a6a9-1427">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1427">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5a6a9-1428">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1428">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="5a6a9-1429">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1429">Az.CognitiveServices</span></span>
* <span data-ttu-id="5a6a9-1430">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1430">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5a6a9-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1431">Az.Compute</span></span>
* <span data-ttu-id="5a6a9-1432">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1432">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5a6a9-1433">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1433">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5a6a9-1434">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1434">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5a6a9-1435">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1435">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5a6a9-1436">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1436">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5a6a9-1437">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1437">Az.Network</span></span>
* <span data-ttu-id="5a6a9-1438">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1438">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5a6a9-1439">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1439">new cmdlets added</span></span>
    - <span data-ttu-id="5a6a9-1440">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1440">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5a6a9-1441">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1441">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5a6a9-1442">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1442">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5a6a9-1443">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1443">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5a6a9-1444">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1444">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5a6a9-1445">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1445">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5a6a9-1446">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1446">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5a6a9-1447">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1447">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5a6a9-1448">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1448">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5a6a9-1449">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1449">Az.RedisCache</span></span>
* <span data-ttu-id="5a6a9-1450">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1450">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5a6a9-1451">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1451">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5a6a9-1452">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1452">Az.Resources</span></span>
* <span data-ttu-id="5a6a9-1453">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1453">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5a6a9-1454">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1454">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5a6a9-1455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1455">Az.Sql</span></span>
* <span data-ttu-id="5a6a9-1456">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1456">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5a6a9-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1457">Az.Websites</span></span>
* <span data-ttu-id="5a6a9-1458">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1458">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5a6a9-1459">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1459">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5a6a9-1460">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1460">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5a6a9-1461">Version initiale</span><span class="sxs-lookup"><span data-stu-id="5a6a9-1461">Initial Release</span></span>