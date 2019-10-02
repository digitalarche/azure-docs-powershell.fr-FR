---
title: Notes de publication Azure PowerShell
description: Découvrez toutes les dernières mises à jour des modules Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/25/2019
ms.openlocfilehash: b879d970d3237098e481dba0419ee65efa8d51cd
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319311"
---
## <a name="270---september-2019"></a><span data-ttu-id="9446c-103">2.7.0 - septembre 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-103">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="9446c-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9446c-104">Az.ApiManagement</span></span>
* <span data-ttu-id="9446c-105">Mise à jour de la description du paramètre « -Format » dans la documentation de référence de « Set-AzApiManagementPolicy »</span><span class="sxs-lookup"><span data-stu-id="9446c-105">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="9446c-106">Suppression des références de la cmdlet dépréciée « Update-AzApiManagementDeployment » dans la documentation de référence.</span><span class="sxs-lookup"><span data-stu-id="9446c-106">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="9446c-107">Utilisation de « Set-AzApiManagement » à la place.</span><span class="sxs-lookup"><span data-stu-id="9446c-107">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-108">Az.Automation</span></span>
* <span data-ttu-id="9446c-109">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Register-AzAutomationDscNode »</span><span class="sxs-lookup"><span data-stu-id="9446c-109">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="9446c-110">Ajout d’une précision sur la restriction de système d’exploitation à Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="9446c-110">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="9446c-111">Correction de l’exception de référence Null de la comdlet Start-AzAutomationRunbook pour l’option -Wait.</span><span class="sxs-lookup"><span data-stu-id="9446c-111">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-112">Az.Compute</span></span>
* <span data-ttu-id="9446c-113">Ajout du paramètre UploadSizeInBytes à New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-113">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="9446c-114">Ajout du paramètre Incremental à New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-114">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="9446c-115">Ajouter d’une fonctionnalité de machine virtuelle basse priorité :</span><span class="sxs-lookup"><span data-stu-id="9446c-115">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="9446c-116">Les paramètres MaxPrice, EvictionPolicy et Priority sont ajoutés à New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="9446c-116">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="9446c-117">Le paramètre MaxPrice est ajouté aux cmdlets New-AzVmssConfig, Update-AzVM et Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="9446c-117">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="9446c-118">Correction du problème de référence de machine virtuelle pour la cmdlet AzAvailabilitySet quand elle liste tous les groupes à haute disponibilité inclus dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="9446c-118">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="9446c-119">Correction de l’exception Null pour Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="9446c-119">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="9446c-120">Correction de la méthode de recherche de disque dur virtuel pour la position relative de fin.</span><span class="sxs-lookup"><span data-stu-id="9446c-120">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="9446c-121">Correction du problème UltraSSD pour New-AzVM et Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="9446c-121">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-122">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-123">Ajout de 3 nouvelles commandes pour ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription et Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="9446c-123">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="9446c-124">Mise à jour de la version du SDK .NET ADF vers la version 4.1.3</span><span class="sxs-lookup"><span data-stu-id="9446c-124">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="9446c-125">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9446c-125">Az.HDInsight</span></span>
* <span data-ttu-id="9446c-126">Explication des changements cassants</span><span class="sxs-lookup"><span data-stu-id="9446c-126">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9446c-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9446c-127">Az.IotHub</span></span>
* <span data-ttu-id="9446c-128">Ajout de la prise en charge pour appeler le basculement d’un IotHub vers la région de reprise d’activité géocouplée.</span><span class="sxs-lookup"><span data-stu-id="9446c-128">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="9446c-129">Ajout de la prise en charge pour gérer l’enrichissement de message pour un IotHub.</span><span class="sxs-lookup"><span data-stu-id="9446c-129">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="9446c-130">Les nouvelles cmdlets sont :</span><span class="sxs-lookup"><span data-stu-id="9446c-130">New cmdlets are:</span></span>
    - <span data-ttu-id="9446c-131">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9446c-131">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="9446c-132">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9446c-132">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="9446c-133">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9446c-133">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="9446c-134">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="9446c-134">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9446c-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-135">Az.Monitor</span></span>
* <span data-ttu-id="9446c-136">Pointage vers le dernier SDK Monitor, par exemple, 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="9446c-136">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="9446c-137">Ajout de changements non cassants aux cmdlets Metrics, c.-à-d. que l’énumération Unit prend en charge plusieurs nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="9446c-137">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="9446c-138">Il s’agit de cmdlets en lecture seule, donc aucune modification n’est apportée à leur entrée.</span><span class="sxs-lookup"><span data-stu-id="9446c-138">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="9446c-139">La version d’API des demandes **ActionGroups** est désormais **2019-06-01**, auparavant il s’agissait de la version **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="9446c-139">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="9446c-140">Les tests de scénario ont été mis à jour pour tenir compte de cette modification.</span><span class="sxs-lookup"><span data-stu-id="9446c-140">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="9446c-141">Les constructeurs des classes **EmailReceiver** et **WebhookReceiver** ont un nouvel argument obligatoire, à savoir une valeur booléenne appelée **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="9446c-141">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="9446c-142">Actuellement, la valeur est définie sur **false** pour masquer ce changement cassant par rapport aux cmdlets.</span><span class="sxs-lookup"><span data-stu-id="9446c-142">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="9446c-143">**REMARQUE** : Il s’agit d’une modification temporaire qui doit être validée par l’équipe des alertes.</span><span class="sxs-lookup"><span data-stu-id="9446c-143">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="9446c-144">L’ordre des arguments pour le constructeur de la classe **Source** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="9446c-144">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="9446c-145">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="9446c-145">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="9446c-146">L’ordre des arguments pour le constructeur de la classe **AlertingAction** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="9446c-146">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="9446c-147">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="9446c-147">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="9446c-148">Prise en charge des critères de seuil dynamique pour l’alerte de métrique V2</span><span class="sxs-lookup"><span data-stu-id="9446c-148">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="9446c-149">New-AzMetricAlertRuleV2Criteria : création de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="9446c-149">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="9446c-150">Add-AzMetricAlertRuleV2 : acceptation de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="9446c-150">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="9446c-151">Améliorations apportées aux cmdlets de règle de requête planifiée</span><span class="sxs-lookup"><span data-stu-id="9446c-151">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="9446c-152">Les cmdlets acceptent le paramètre « location » dans les deux formats, à savoir l’emplacement (par exemple, usa-est) ou le nom d’affichage de l’emplacement (par exemple, USA Est)</span><span class="sxs-lookup"><span data-stu-id="9446c-152">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="9446c-153">Illustration correcte du paramètre « Enabled » dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="9446c-153">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="9446c-154">Ajout d’exemples pour le paramètre facultatif « ActionGroup »</span><span class="sxs-lookup"><span data-stu-id="9446c-154">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="9446c-155">Amélioration globale des fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="9446c-155">Overall improved help files</span></span>
* <span data-ttu-id="9446c-156">Correction du bogue lié à la détermination du type d’étendue pour « Set-AzActionRule »</span><span class="sxs-lookup"><span data-stu-id="9446c-156">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-157">Az.Network</span></span>
* <span data-ttu-id="9446c-158">Correction de l’exemple incorrect dans la documentation de référence de « New-AzApplicationGateway »</span><span class="sxs-lookup"><span data-stu-id="9446c-158">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="9446c-159">Ajout d’une remarque à la documentation de référence de « Get-AzNetworkWatcherPacketCapturee » à propos de la récupération de toutes les propriétés d’une capture de paquets</span><span class="sxs-lookup"><span data-stu-id="9446c-159">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="9446c-160">Correction de l’exemple dans la documentation de référence de « Test-AzNetworkWatcherIPFlow » pour énumérer correctement les cartes réseau</span><span class="sxs-lookup"><span data-stu-id="9446c-160">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="9446c-161">Amélioration de l’analyse des exceptions cloud pour afficher des détails supplémentaires s’ils existent</span><span class="sxs-lookup"><span data-stu-id="9446c-161">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="9446c-162">Amélioration de l’analyse des exceptions cloud pour gérer un type supplémentaire d’exception de SDK</span><span class="sxs-lookup"><span data-stu-id="9446c-162">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="9446c-163">Correction du mappage incorrect des modèles de règle de sécurité</span><span class="sxs-lookup"><span data-stu-id="9446c-163">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="9446c-164">Ajout de propriétés à une interface réseau pour la fonctionnalité d’adresse IP privée</span><span class="sxs-lookup"><span data-stu-id="9446c-164">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="9446c-165">Ajout de la propriété « PrivateEndpoint » comme type de PSResourceId à PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9446c-165">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="9446c-166">Ajout de la propriété « PrivateLinkConnectionProperties » comme type de PSIpConfigurationConnectivityInformation à PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-166">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="9446c-167">Ajout d’une nouvelle classe de modèle PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="9446c-167">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="9446c-168">Ajout de « MSSQL » ApplicationRuleProtocolType pour la ressource du Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-168">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="9446c-169">Prise en charge de liaisons multiples dans Azure Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="9446c-169">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="9446c-170">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-170">New cmdlets</span></span>
        - <span data-ttu-id="9446c-171">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="9446c-171">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="9446c-172">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-172">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="9446c-173">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="9446c-173">Updated cmdlet:</span></span>
        - <span data-ttu-id="9446c-174">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="9446c-174">New-VpnSite</span></span>
        - <span data-ttu-id="9446c-175">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="9446c-175">Update-VpnSite</span></span>
        - <span data-ttu-id="9446c-176">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-176">New-VpnConnection</span></span>
        - <span data-ttu-id="9446c-177">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-177">Update-VpnConnection</span></span>
* <span data-ttu-id="9446c-178">Correction des documents de certains exemples PowerShell pour utiliser des cmdlets Az à la place de cmdlets AzureRM</span><span class="sxs-lookup"><span data-stu-id="9446c-178">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-180">Mise à jour de l’objet AzureVMpolicy avec l’attribut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="9446c-180">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="9446c-181">Ajout de tests pour la stratégie de machine virtuelle et la restauration du compte de stockage d’origine</span><span class="sxs-lookup"><span data-stu-id="9446c-181">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-182">Az.Resources</span></span>
* <span data-ttu-id="9446c-183">Correction du bogue qui empêchait l’appel de New-AzRoleAssignment sans paramètre d’étendue.</span><span class="sxs-lookup"><span data-stu-id="9446c-183">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9446c-184">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-184">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-185">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="9446c-185">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="9446c-186">Ajout de nouvelles cmdlets pour gérer les applications et les services :</span><span class="sxs-lookup"><span data-stu-id="9446c-186">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="9446c-187">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9446c-187">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="9446c-188">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9446c-188">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="9446c-189">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9446c-189">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="9446c-190">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="9446c-190">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="9446c-191">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9446c-191">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="9446c-192">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9446c-192">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="9446c-193">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9446c-193">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="9446c-194">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9446c-194">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="9446c-195">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="9446c-195">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="9446c-196">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="9446c-196">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="9446c-197">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9446c-197">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="9446c-198">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="9446c-198">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="9446c-199">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="9446c-199">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="9446c-200">Mise à niveau du SDK Service Fabric vers la version 1.2.0 qui utilise la version d’API du fournisseur de ressources Service Fabric 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="9446c-200">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9446c-201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9446c-201">Az.SignalR</span></span>
* <span data-ttu-id="9446c-202">Ajout de cmdlets Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="9446c-202">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-203">Az.Sql</span></span>
* <span data-ttu-id="9446c-204">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzSqlElasticPool »</span><span class="sxs-lookup"><span data-stu-id="9446c-204">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="9446c-205">Ajout d’un exemple vCore à la création d’un pool élastique (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="9446c-205">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="9446c-206">Suppression de la validation de EmailAddresses et de la vérification que EmailAdmins n’a pas la valeur false quand EmailAddresses est vide dans Set-AzSqlServerAdvancedThreatProtectionPolicy et Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-206">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="9446c-207">Activation de la suppression des paramètres d’audit du serveur/de la base de données quand il existe plusieurs paramètres de diagnostic qui activent la catégorie d’audit.</span><span class="sxs-lookup"><span data-stu-id="9446c-207">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="9446c-208">Correction de la validation des adresses e-mail dans plusieurs cmdlets d’évaluation des vulnérabilités SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting et Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="9446c-208">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-209">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-209">Az.Storage</span></span>
* <span data-ttu-id="9446c-210">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzStorageAccountKey »</span><span class="sxs-lookup"><span data-stu-id="9446c-210">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="9446c-211">Lors d’un chargement/téléchargement de fichier Azure, prise en charge de la conservation des propriétés SMB des fichiers sources (attributs du fichier, heure de création du fichier, heure de la dernière écriture du fichier) dans le fichier de destination</span><span class="sxs-lookup"><span data-stu-id="9446c-211">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="9446c-212">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9446c-212">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="9446c-213">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9446c-213">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="9446c-214">Correction de l’échec de chargement de l’objet blob de blocs avec des propriétés/métadonnées sur ImmutabilityPolicy avec conteneur activé.</span><span class="sxs-lookup"><span data-stu-id="9446c-214">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="9446c-215">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9446c-215">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="9446c-216">Prise en charge de la gestion des partages de fichiers Azure avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="9446c-216">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="9446c-217">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9446c-217">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="9446c-218">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9446c-218">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="9446c-219">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9446c-219">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="9446c-220">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9446c-220">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-221">Az.Websites</span></span>
* <span data-ttu-id="9446c-222">Résolution du problème de suppression des balises d’application web lors de la migration de l’application vers un nouvel ASP</span><span class="sxs-lookup"><span data-stu-id="9446c-222">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="9446c-223">Correction de Publish-AzureWebapp pour un fonctionnement sur Linux et Windows</span><span class="sxs-lookup"><span data-stu-id="9446c-223">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="9446c-224">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzWebAppPublishingProfile »</span><span class="sxs-lookup"><span data-stu-id="9446c-224">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="9446c-225">2.6.0 - Août 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-225">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="9446c-226">Généralités</span><span class="sxs-lookup"><span data-stu-id="9446c-226">General</span></span>
* <span data-ttu-id="9446c-227">Correction des fautes de frappe diverses dans de nombreux modules</span><span class="sxs-lookup"><span data-stu-id="9446c-227">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="9446c-228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-228">Az.Accounts</span></span>
* <span data-ttu-id="9446c-229">Prise en charge de l’identité MSI affectée à l’utilisateur dans l’authentification Azure Functions (n° 9479)</span><span class="sxs-lookup"><span data-stu-id="9446c-229">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="9446c-230">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="9446c-230">Az.Aks</span></span>
* <span data-ttu-id="9446c-231">Résolution du problème relatif à la sortie de « Get-AzAks »</span><span class="sxs-lookup"><span data-stu-id="9446c-231">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="9446c-232">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="9446c-232">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="9446c-233">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9446c-233">Az.ApiManagement</span></span>
* <span data-ttu-id="9446c-234">Corriger le problème https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="9446c-234">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="9446c-235">Mise à jour de la version de .Net NuGet, qui n’applique pas de restrictions sur productId, apiId, groupId et userId</span><span class="sxs-lookup"><span data-stu-id="9446c-235">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="9446c-236">**Get-AzApiManagementProduct** : ajout de la prise en charge de l’interrogation de produits à l’aide d’une API.</span><span class="sxs-lookup"><span data-stu-id="9446c-236">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="9446c-237">**New-AzApiManagementApiRevision** : résolution du problème où ApiRevisionDescription n’était pas défini lors de la création d’une révision d’API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="9446c-237">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="9446c-238">Correction d’une faute de frappe dans le modèle « PsApiManagementOAuth2AuthrozationServer » remplacé par « PsApiManagementOAuth2AuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="9446c-238">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="9446c-239">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9446c-239">Az.Batch</span></span>
* <span data-ttu-id="9446c-240">Correction d’une faute de frappe dans un message d’aide et la documentation pour mettre Windows en majuscules</span><span class="sxs-lookup"><span data-stu-id="9446c-240">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9446c-241">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9446c-241">Az.Cdn</span></span>
* <span data-ttu-id="9446c-242">Correction d’une faute de frappe dans l’application d’assistance du module CDN</span><span class="sxs-lookup"><span data-stu-id="9446c-242">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-243">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-243">Az.Compute</span></span>
* <span data-ttu-id="9446c-244">Ajout de VmssId à l’applet de commande New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-244">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="9446c-245">Ajout des paramètres TerminateScheduledEvents et TerminateScheduledEventNotBeforeTimeoutInMinutes à New-AzVmssConfig et Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9446c-245">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="9446c-246">Ajout de la propriété HyperVGeneration à l’objet image de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="9446c-246">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="9446c-247">Ajout des fonctionnalités Host et HostGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-247">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="9446c-248">Nouvelles applets de commande :   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="9446c-248">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="9446c-249">Le paramètre HostId est ajouté à New-AzVMConfig et New-AzVM</span><span class="sxs-lookup"><span data-stu-id="9446c-249">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="9446c-250">Mise à jour de l’exemple dans la documentation « Invoke-AzVMRunCommand » de manière utiliser le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="9446c-250">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="9446c-251">Mise à jour de la description « -VolumeType » dans la documentation de référence de « Set-AzVMDiskEncryptionExtension » et de « Set-AzVmssDiskEncryptionExtension »</span><span class="sxs-lookup"><span data-stu-id="9446c-251">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-252">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-252">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-253">Correction de la faute de frappe pour mettre « Windows » en majuscules dans la documentation de « New-AzDataFactoryEncryptValue »</span><span class="sxs-lookup"><span data-stu-id="9446c-253">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="9446c-254">Mise à jour de la version du SDK .NET ADF vers la version 4.1.2</span><span class="sxs-lookup"><span data-stu-id="9446c-254">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="9446c-255">Ajout des paramètres « DataProxyIntegrationRuntimeName », « DataProxyStagingLinkedServiceName » et « DataProxyStagingPath » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin de permettre la configuration du runtime d’intégration auto-hébergé comme proxy pour SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="9446c-255">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="9446c-256">Mise à jour de PSTriggerRun pour afficher les pipelines déclenchés, le message et les propriétés, et de PSActivityRun pour afficher le type d’activité</span><span class="sxs-lookup"><span data-stu-id="9446c-256">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-257">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-257">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-258">Correction de la suspension de Get-DataLakeStoreDeletedItem pour toutes les erreurs ou exceptions à distance.</span><span class="sxs-lookup"><span data-stu-id="9446c-258">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9446c-259">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9446c-259">Az.EventHub</span></span>
* <span data-ttu-id="9446c-260">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNteworkRule dans Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-260">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="9446c-261">Résolution du problème n° 9558 : Set-AzEventHubNamespace utilise PATCH au lieu de PUT</span><span class="sxs-lookup"><span data-stu-id="9446c-261">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="9446c-262">Ajout du paramètre EnableKafka à l’applet de commande Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9446c-262">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="9446c-263">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="9446c-263">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="9446c-264">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9446c-264">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="9446c-265">Résolution de la faute de frappe où « Azure » était tout en minuscules dans la documentation</span><span class="sxs-lookup"><span data-stu-id="9446c-265">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9446c-266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-266">Az.Monitor</span></span>
* <span data-ttu-id="9446c-267">Correction du nom de paramètre incorrect dans la documentation</span><span class="sxs-lookup"><span data-stu-id="9446c-267">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-268">Az.Network</span></span>
* <span data-ttu-id="9446c-269">Mise à jour dans New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-269">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="9446c-270">Dépréciation du paramètre « PublicIpAddress », car il n’est jamais utilisé côté serveur.</span><span class="sxs-lookup"><span data-stu-id="9446c-270">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="9446c-271">Ajout d’un paramètre facultatif « Primary » qui indique si la configuration IP actuelle est primaire ou non.</span><span class="sxs-lookup"><span data-stu-id="9446c-271">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="9446c-272">Amélioration de la gestion de l’exception d’erreur de demande à partir du SDK : résolution du problème où les exceptions du SDK n’étaient précédemment pas gérées correctement, ce qui empêchait l’affichage des détails des erreurs de clé</span><span class="sxs-lookup"><span data-stu-id="9446c-272">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="9446c-273">Ajustement de la logique de validation pour le préfixe IP IPv6 afin de rechercher la longueur de préfixe IPv6 appropriée.</span><span class="sxs-lookup"><span data-stu-id="9446c-273">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="9446c-274">Mise à jour de Get-AzVirtualNetworkSubnetConfig : Ajout d’un paramètre défini pour obtenir l’ID de ressource de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="9446c-274">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="9446c-275">Mise à jour de la description du paramètre Location pour AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="9446c-275">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-276">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-276">Az.OperationalInsights</span></span>
* <span data-ttu-id="9446c-277">Mise à jour de la documentation pour « New-AzOperationalInsightsLinuxSyslogDataSource »</span><span class="sxs-lookup"><span data-stu-id="9446c-277">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="9446c-278">Ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="9446c-278">Added example</span></span>
    - <span data-ttu-id="9446c-279">Mise à jour de la description du paramètre « -Name »</span><span class="sxs-lookup"><span data-stu-id="9446c-279">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="9446c-280">Ajout d’un exemple pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="9446c-280">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="9446c-281">Changement de la description du paramètre -Name pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="9446c-281">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-283">Mise à jour de « Get-AzRecoveryServicesBackupJobDetail.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-283">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-284">Az.Resources</span></span>
* <span data-ttu-id="9446c-285">Ajout de la prise en charge de la nouvelle API version 2019-05-10 pour Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="9446c-285">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="9446c-286">Ajout de la prise en charge de « copy.count = 0 » pour les variables, les ressources et les propriétés</span><span class="sxs-lookup"><span data-stu-id="9446c-286">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="9446c-287">Les ressources avec « condition = false » ou « copy.count = 0 » seront supprimées en mode Complet</span><span class="sxs-lookup"><span data-stu-id="9446c-287">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="9446c-288">Ajout d’un exemple d’affectation de stratégie au niveau de l’abonnement à la documentation d’aide</span><span class="sxs-lookup"><span data-stu-id="9446c-288">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9446c-289">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9446c-289">Az.ServiceBus</span></span>
* <span data-ttu-id="9446c-290">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNetworkRule dans Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-290">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="9446c-291">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="9446c-291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="9446c-292">Ajout de la nouvelle commande « Test-AzServiceBusNameAvailability » afin de vérifier la disponibilité du nom pour la file d’attente et la rubrique</span><span class="sxs-lookup"><span data-stu-id="9446c-292">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="9446c-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-294">Correction des bogues relatifs à l’applet de commande add node type :</span><span class="sxs-lookup"><span data-stu-id="9446c-294">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="9446c-295">bogue NullReferenceException quand un groupe de ressources avait d’autres groupes de machines virtuelles identiques non liés au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="9446c-295">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="9446c-296">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="9446c-296">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="9446c-297">Correction du bogue où l’applet de commande échouait si virtualNetwork se trouvait dans un groupe de ressources différent de celui du cluster.</span><span class="sxs-lookup"><span data-stu-id="9446c-297">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="9446c-298">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="9446c-298">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="9446c-299">Dépréciation de l’applet de commande Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="9446c-299">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-300">Az.Sql</span></span>
* <span data-ttu-id="9446c-301">Mise à jour de la documentation des anciennes applets de commande d’audit.</span><span class="sxs-lookup"><span data-stu-id="9446c-301">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-302">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-302">Az.Storage</span></span>
* <span data-ttu-id="9446c-303">Mise à jour de l’aide pour Get/Close-AzStorageFileHandle, en ajoutant d’autres scénarios aux exemples d’applets de commande et mise à jour des descriptions des paramètres</span><span class="sxs-lookup"><span data-stu-id="9446c-303">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="9446c-304">Prise en charge de StandardBlobTier dans le chargement d’objet blob et la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="9446c-304">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="9446c-305">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9446c-305">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="9446c-306">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9446c-306">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="9446c-307">Prise en charge de la priorité de réalimentation dans la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="9446c-307">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="9446c-308">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9446c-308">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-309">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-309">Az.Websites</span></span>
* <span data-ttu-id="9446c-310">Ajout d’une clarification concernant le paramètre -AppSettings dans Set-AzWebApp et Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9446c-310">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="9446c-311">2.5.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-311">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-312">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-312">Az.Accounts</span></span>
* <span data-ttu-id="9446c-313">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9446c-313">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="9446c-314">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-314">Az.ApplicationInsights</span></span>
* <span data-ttu-id="9446c-315">Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey »</span><span class="sxs-lookup"><span data-stu-id="9446c-315">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="9446c-316">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-316">Az.Automation</span></span>
* <span data-ttu-id="9446c-317">Correction d’une faute de frappe dans la chaîne de ressource</span><span class="sxs-lookup"><span data-stu-id="9446c-317">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="9446c-318">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9446c-318">Az.CognitiveServices</span></span>
* <span data-ttu-id="9446c-319">Prise en charge de NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="9446c-319">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-320">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-320">Az.Compute</span></span>
* <span data-ttu-id="9446c-321">Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-321">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="9446c-322">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9446c-322">Az.ContainerRegistry</span></span>
* <span data-ttu-id="9446c-323">Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication</span><span class="sxs-lookup"><span data-stu-id="9446c-323">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="9446c-324">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="9446c-324">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-325">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-326">Mise à jour du SDK .NET ADF avec la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="9446c-326">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="9446c-327">Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »</span><span class="sxs-lookup"><span data-stu-id="9446c-327">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9446c-328">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9446c-328">Az.EventHub</span></span>
* <span data-ttu-id="9446c-329">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="9446c-329">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="9446c-330">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="9446c-330">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9446c-331">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-331">Az.KeyVault</span></span>
* <span data-ttu-id="9446c-332">Possibilité de spécifier KeySize pour les stratégies de certificat</span><span class="sxs-lookup"><span data-stu-id="9446c-332">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9446c-333">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9446c-333">Az.LogicApp</span></span>
* <span data-ttu-id="9446c-334">Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes</span><span class="sxs-lookup"><span data-stu-id="9446c-334">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="9446c-335">Ajout d’un nouveau paramètre MapType pour le filtrage</span><span class="sxs-lookup"><span data-stu-id="9446c-335">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="9446c-336">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="9446c-336">Az.ManagedServices</span></span>
* <span data-ttu-id="9446c-337">Ajout de la prise en charge de l’API version 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="9446c-337">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-338">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-338">Az.Network</span></span>
* <span data-ttu-id="9446c-339">Prise en charge d’un point de terminaison privé et du service de liaison privée</span><span class="sxs-lookup"><span data-stu-id="9446c-339">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="9446c-340">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-340">New cmdlets</span></span>
        - <span data-ttu-id="9446c-341">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9446c-341">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="9446c-342">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9446c-342">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="9446c-343">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-343">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="9446c-344">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-344">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="9446c-345">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-345">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="9446c-346">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-346">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="9446c-347">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="9446c-347">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="9446c-348">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9446c-348">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="9446c-349">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9446c-349">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="9446c-350">Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-350">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="9446c-351">Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="9446c-351">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="9446c-352">Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="9446c-352">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="9446c-353">Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="9446c-353">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="9446c-354">Activation du protocole ICMP pour les configurations des règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="9446c-354">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="9446c-355">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="9446c-355">Updated cmdlets</span></span>
        - <span data-ttu-id="9446c-356">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-356">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="9446c-357">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-357">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="9446c-358">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-358">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="9446c-359">Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-359">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="9446c-360">Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-360">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="9446c-361">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="9446c-361">Updated cmdlet:</span></span>
        - <span data-ttu-id="9446c-362">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-362">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="9446c-363">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-363">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="9446c-364">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-364">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="9446c-365">Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde</span><span class="sxs-lookup"><span data-stu-id="9446c-365">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="9446c-366">Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end.</span><span class="sxs-lookup"><span data-stu-id="9446c-366">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="9446c-367">Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="9446c-367">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-368">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-368">Az.OperationalInsights</span></span>
* <span data-ttu-id="9446c-369">Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="9446c-369">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="9446c-370">Correction de la gestion des expressions régulières null des journaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="9446c-370">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-371">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-371">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-372">Mise à jour de « Get-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-372">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="9446c-373">Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-373">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="9446c-374">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-374">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="9446c-375">Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-375">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="9446c-376">Mise à jour de « Set-AzRecoveryServicesVaultContext.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-376">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="9446c-377">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-377">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="9446c-378">Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-378">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="9446c-379">Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-379">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="9446c-380">Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-380">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="9446c-381">Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »</span><span class="sxs-lookup"><span data-stu-id="9446c-381">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-382">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-382">Az.Resources</span></span>
- <span data-ttu-id="9446c-383">Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="9446c-383">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="9446c-384">Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="9446c-384">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9446c-385">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9446c-385">Az.ServiceBus</span></span>
* <span data-ttu-id="9446c-386">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="9446c-386">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="9446c-387">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="9446c-387">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-388">Az.Sql</span></span>
* <span data-ttu-id="9446c-389">Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9446c-389">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="9446c-390">Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="9446c-390">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="9446c-391">Correction d’une faute de frappe dans un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="9446c-391">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-392">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-392">Az.Storage</span></span>
* <span data-ttu-id="9446c-393">Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="9446c-393">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="9446c-394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="9446c-394">Az.StorageSync</span></span>
* <span data-ttu-id="9446c-395">Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="9446c-395">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="9446c-396">Résolution du problème 9551 pour honorer TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="9446c-396">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-397">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-397">Az.Websites</span></span>
* <span data-ttu-id="9446c-398">Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-398">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="9446c-399">Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="9446c-399">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="9446c-400">Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="9446c-400">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="9446c-401">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-401">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-402">Az.Accounts</span></span>
* <span data-ttu-id="9446c-403">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="9446c-403">Add support for profile cmdlets</span></span>
* <span data-ttu-id="9446c-404">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="9446c-404">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="9446c-405">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9446c-405">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="9446c-406">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="9446c-406">Az.Advisor</span></span>
* <span data-ttu-id="9446c-407">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="9446c-407">GA release of Az.Advisor</span></span>
* <span data-ttu-id="9446c-408">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="9446c-408">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="9446c-409">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9446c-409">Az.ApiManagement</span></span>
* <span data-ttu-id="9446c-410">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="9446c-410">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="9446c-411">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="9446c-411">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="9446c-412">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="9446c-412">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="9446c-413">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="9446c-413">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="9446c-414">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="9446c-414">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="9446c-415">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="9446c-415">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="9446c-416">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="9446c-416">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-417">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-417">Az.Automation</span></span>
* <span data-ttu-id="9446c-418">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="9446c-418">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-419">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-419">Az.Compute</span></span>
* <span data-ttu-id="9446c-420">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-420">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-421">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-421">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-422">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="9446c-422">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9446c-423">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9446c-423">Az.EventGrid</span></span>
* <span data-ttu-id="9446c-424">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="9446c-424">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9446c-425">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9446c-425">Az.IotHub</span></span>
* <span data-ttu-id="9446c-426">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="9446c-426">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-427">Az.Network</span></span>
* <span data-ttu-id="9446c-428">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="9446c-428">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="9446c-429">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="9446c-429">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9446c-430">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-430">Az.PolicyInsights</span></span>
* <span data-ttu-id="9446c-431">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="9446c-431">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="9446c-432">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="9446c-432">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="9446c-434">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9446c-434">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-435">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-435">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-436">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="9446c-436">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-437">Az.Resources</span></span>
    - <span data-ttu-id="9446c-438">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="9446c-438">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="9446c-439">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="9446c-439">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="9446c-440">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="9446c-440">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="9446c-441">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="9446c-441">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9446c-442">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9446c-442">Az.ServiceBus</span></span>
* <span data-ttu-id="9446c-443">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="9446c-443">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-444">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-444">Az.Sql</span></span>
* <span data-ttu-id="9446c-445">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="9446c-445">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="9446c-446">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="9446c-446">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="9446c-447">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="9446c-447">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="9446c-448">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="9446c-448">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="9446c-449">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="9446c-449">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="9446c-450">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="9446c-450">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="9446c-451">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="9446c-451">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="9446c-452">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="9446c-452">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="9446c-453">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="9446c-453">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-454">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-454">Az.Storage</span></span>
* <span data-ttu-id="9446c-455">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="9446c-455">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="9446c-456">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9446c-456">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="9446c-457">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="9446c-457">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="9446c-458">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="9446c-458">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="9446c-459">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="9446c-459">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="9446c-460">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-460">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="9446c-461">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-461">Set-AzStorageAccount</span></span>
* <span data-ttu-id="9446c-462">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="9446c-462">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="9446c-463">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="9446c-463">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="9446c-464">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="9446c-464">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="9446c-465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="9446c-465">Az.StorageSync</span></span>
* <span data-ttu-id="9446c-466">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="9446c-466">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="9446c-467">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-467">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-468">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-468">Az.Accounts</span></span>
* <span data-ttu-id="9446c-469">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="9446c-469">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="9446c-470">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="9446c-470">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="9446c-471">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="9446c-471">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="9446c-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9446c-472">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="9446c-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="9446c-473">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-474">Az.Compute</span></span>
* <span data-ttu-id="9446c-475">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="9446c-475">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="9446c-476">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="9446c-476">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="9446c-477">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="9446c-477">Az.Dns</span></span>
* <span data-ttu-id="9446c-478">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="9446c-478">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9446c-479">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9446c-479">Az.EventGrid</span></span>
* <span data-ttu-id="9446c-480">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="9446c-480">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="9446c-481">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="9446c-481">New cmdlets:</span></span>
    - <span data-ttu-id="9446c-482">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9446c-482">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="9446c-483">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="9446c-483">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="9446c-484">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9446c-484">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="9446c-485">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="9446c-485">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="9446c-486">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="9446c-486">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="9446c-487">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="9446c-487">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="9446c-488">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="9446c-488">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="9446c-489">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="9446c-489">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="9446c-490">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="9446c-490">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="9446c-491">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="9446c-491">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="9446c-492">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9446c-492">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="9446c-493">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="9446c-493">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="9446c-494">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9446c-494">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="9446c-495">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="9446c-495">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="9446c-496">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="9446c-496">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="9446c-497">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="9446c-497">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="9446c-498">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="9446c-498">Updated cmdlets:</span></span>
    - <span data-ttu-id="9446c-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="9446c-499">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="9446c-500">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="9446c-500">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="9446c-501">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="9446c-501">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="9446c-502">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="9446c-502">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="9446c-503">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="9446c-503">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="9446c-504">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="9446c-504">Event subscription expiration date,</span></span>
            - <span data-ttu-id="9446c-505">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="9446c-505">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="9446c-506">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="9446c-506">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="9446c-507">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="9446c-507">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="9446c-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="9446c-508">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="9446c-509">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="9446c-509">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="9446c-510">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="9446c-510">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="9446c-511">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="9446c-511">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="9446c-512">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="9446c-512">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="9446c-513">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9446c-513">Az.FrontDoor</span></span>
* <span data-ttu-id="9446c-514">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="9446c-514">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="9446c-515">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="9446c-515">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="9446c-516">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="9446c-516">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="9446c-517">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="9446c-517">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-518">Az.Network</span></span>
* <span data-ttu-id="9446c-519">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="9446c-519">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="9446c-520">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-520">New cmdlets</span></span>
        - <span data-ttu-id="9446c-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="9446c-521">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="9446c-522">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="9446c-522">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="9446c-523">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-523">New cmdlets</span></span> 
        - <span data-ttu-id="9446c-524">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="9446c-524">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="9446c-525">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9446c-525">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="9446c-526">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-526">New cmdlets</span></span> 
        - <span data-ttu-id="9446c-527">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9446c-527">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="9446c-528">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9446c-528">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="9446c-529">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9446c-529">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="9446c-530">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-530">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="9446c-531">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-531">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="9446c-532">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9446c-532">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="9446c-533">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-533">New cmdlets</span></span>
        - <span data-ttu-id="9446c-534">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9446c-534">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="9446c-535">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9446c-535">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="9446c-536">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="9446c-536">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="9446c-537">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-537">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="9446c-538">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="9446c-538">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="9446c-539">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="9446c-539">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="9446c-540">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="9446c-540">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="9446c-541">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9446c-541">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="9446c-542">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9446c-542">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="9446c-543">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9446c-543">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="9446c-544">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-544">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="9446c-545">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="9446c-545">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="9446c-546">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-546">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="9446c-547">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="9446c-547">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="9446c-548">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-548">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="9446c-549">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-549">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="9446c-550">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="9446c-550">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="9446c-551">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-551">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="9446c-552">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="9446c-552">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="9446c-553">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="9446c-553">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="9446c-554">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="9446c-554">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="9446c-555">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="9446c-555">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="9446c-556">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9446c-556">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="9446c-557">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="9446c-557">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="9446c-558">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-558">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="9446c-559">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-559">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="9446c-560">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-560">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-561">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-561">Az.OperationalInsights</span></span>
* <span data-ttu-id="9446c-562">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="9446c-562">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-563">Az.Resources</span></span>
* <span data-ttu-id="9446c-564">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="9446c-564">Support for additional Template Export options</span></span>
    - <span data-ttu-id="9446c-565">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-565">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="9446c-566">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-566">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="9446c-567">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="9446c-567">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9446c-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-569">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-569">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-570">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-570">Az.Sql</span></span>
* <span data-ttu-id="9446c-571">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="9446c-571">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="9446c-572">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="9446c-572">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="9446c-573">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="9446c-573">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="9446c-574">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9446c-574">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="9446c-575">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9446c-575">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="9446c-576">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9446c-576">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="9446c-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="9446c-577">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="9446c-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="9446c-578">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-579">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-579">Az.Storage</span></span>
* <span data-ttu-id="9446c-580">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="9446c-580">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="9446c-581">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-581">New-AzStorageAccount</span></span>
* <span data-ttu-id="9446c-582">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="9446c-582">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="9446c-583">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-583">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-584">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-584">Az.Websites</span></span>
* <span data-ttu-id="9446c-585">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="9446c-585">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="9446c-586">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="9446c-586">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="9446c-587">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-587">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="9446c-588">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9446c-588">Az.Cdn</span></span>
* <span data-ttu-id="9446c-589">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="9446c-589">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-590">Az.Compute</span></span>
* <span data-ttu-id="9446c-591">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9446c-591">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="9446c-592">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9446c-592">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9446c-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9446c-593">Az.EventHub</span></span>
* <span data-ttu-id="9446c-594">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="9446c-594">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="9446c-595">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9446c-595">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-596">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-596">Az.Network</span></span>
* <span data-ttu-id="9446c-597">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="9446c-597">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="9446c-598">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="9446c-598">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9446c-599">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-599">Az.PolicyInsights</span></span>
* <span data-ttu-id="9446c-600">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="9446c-600">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-601">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-601">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-602">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="9446c-602">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9446c-603">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9446c-603">Az.ServiceBus</span></span>
* <span data-ttu-id="9446c-604">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9446c-604">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9446c-605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-605">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-606">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="9446c-606">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="9446c-607">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9446c-607">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-608">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-608">Az.Sql</span></span>
* <span data-ttu-id="9446c-609">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="9446c-609">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="9446c-610">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-610">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="9446c-611">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="9446c-611">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="9446c-612">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9446c-612">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-613">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-613">Az.Websites</span></span>
* <span data-ttu-id="9446c-614">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="9446c-614">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="9446c-615">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-615">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="9446c-616">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9446c-616">Az.ApiManagement</span></span>
* <span data-ttu-id="9446c-617">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-617">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="9446c-618">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-618">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="9446c-619">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-619">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="9446c-620">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="9446c-620">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="9446c-621">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-621">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="9446c-622">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="9446c-622">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="9446c-623">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-623">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="9446c-624">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-624">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="9446c-625">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="9446c-625">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="9446c-626">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="9446c-626">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="9446c-627">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="9446c-627">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="9446c-628">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="9446c-628">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="9446c-629">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="9446c-629">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="9446c-630">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="9446c-630">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="9446c-631">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="9446c-631">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="9446c-632">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-632">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="9446c-633">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-633">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="9446c-634">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="9446c-634">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="9446c-635">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9446c-635">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="9446c-636">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="9446c-636">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="9446c-637">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="9446c-637">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="9446c-638">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="9446c-638">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="9446c-639">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="9446c-639">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="9446c-640">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="9446c-640">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="9446c-641">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="9446c-641">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="9446c-642">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="9446c-642">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="9446c-643">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="9446c-643">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="9446c-644">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="9446c-644">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="9446c-645">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="9446c-645">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="9446c-646">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="9446c-646">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="9446c-647">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="9446c-647">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="9446c-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="9446c-648">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="9446c-649">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="9446c-649">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="9446c-650">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="9446c-650">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="9446c-651">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="9446c-651">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="9446c-652">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="9446c-652">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="9446c-653">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="9446c-653">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="9446c-654">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="9446c-654">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="9446c-655">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="9446c-655">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="9446c-656">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="9446c-656">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="9446c-657">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="9446c-657">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="9446c-658">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="9446c-658">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="9446c-659">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="9446c-659">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="9446c-660">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="9446c-660">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="9446c-661">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="9446c-661">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="9446c-662">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="9446c-662">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="9446c-663">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="9446c-663">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="9446c-664">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="9446c-664">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="9446c-665">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="9446c-665">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="9446c-666">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="9446c-666">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="9446c-667">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="9446c-667">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="9446c-668">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="9446c-668">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="9446c-669">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="9446c-669">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="9446c-670">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="9446c-670">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="9446c-671">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="9446c-671">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="9446c-672">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="9446c-672">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="9446c-673">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="9446c-673">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="9446c-674">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="9446c-674">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="9446c-675">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="9446c-675">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="9446c-676">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="9446c-676">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="9446c-677">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="9446c-677">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="9446c-678">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="9446c-678">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="9446c-679">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="9446c-679">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="9446c-680">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="9446c-680">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="9446c-681">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="9446c-681">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="9446c-682">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="9446c-682">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="9446c-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="9446c-683">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="9446c-684">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="9446c-684">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="9446c-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="9446c-685">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="9446c-686">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="9446c-686">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="9446c-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="9446c-687">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="9446c-688">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="9446c-688">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="9446c-689">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="9446c-689">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="9446c-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="9446c-690">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="9446c-691">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="9446c-691">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="9446c-692">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="9446c-692">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="9446c-693">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="9446c-693">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-694">Az.Automation</span></span>
* <span data-ttu-id="9446c-695">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="9446c-695">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="9446c-696">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="9446c-696">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="9446c-697">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="9446c-697">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="9446c-698">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="9446c-698">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="9446c-699">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="9446c-699">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="9446c-700">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="9446c-700">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="9446c-701">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="9446c-701">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-702">Az.Compute</span></span>
* <span data-ttu-id="9446c-703">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="9446c-703">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="9446c-704">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9446c-704">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-706">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-706">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9446c-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-707">Az.Monitor</span></span>
* <span data-ttu-id="9446c-708">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="9446c-708">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-709">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-709">Az.Network</span></span>
* <span data-ttu-id="9446c-710">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="9446c-710">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="9446c-711">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="9446c-711">Updated cmdlet:</span></span>
        - <span data-ttu-id="9446c-712">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="9446c-712">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="9446c-713">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9446c-713">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-714">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-714">Az.Resources</span></span>
* <span data-ttu-id="9446c-715">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="9446c-715">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-716">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-716">Az.Sql</span></span>
* <span data-ttu-id="9446c-717">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="9446c-717">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="9446c-718">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-718">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-719">Az.Accounts</span></span>
* <span data-ttu-id="9446c-720">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="9446c-720">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9446c-721">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9446c-721">Az.CognitiveServices</span></span>
* <span data-ttu-id="9446c-722">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="9446c-722">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="9446c-723">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="9446c-723">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-724">Az.Compute</span></span>
* <span data-ttu-id="9446c-725">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="9446c-725">Proximity placement group feature.</span></span>
    - <span data-ttu-id="9446c-726">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-726">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="9446c-727">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-727">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="9446c-728">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="9446c-728">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="9446c-729">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="9446c-729">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="9446c-730">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9446c-730">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="9446c-731">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="9446c-731">Breaking changes</span></span>
    - <span data-ttu-id="9446c-732">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="9446c-732">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="9446c-733">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="9446c-733">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="9446c-734">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="9446c-734">Az.DeploymentManager</span></span>
* <span data-ttu-id="9446c-735">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="9446c-735">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="9446c-736">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="9446c-736">Az.Dns</span></span>
* <span data-ttu-id="9446c-737">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="9446c-737">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="9446c-738">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9446c-738">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="9446c-739">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="9446c-739">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="9446c-740">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9446c-740">Az.FrontDoor</span></span>
* <span data-ttu-id="9446c-741">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9446c-741">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="9446c-742">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="9446c-742">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="9446c-743">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9446c-743">Az.HDInsight</span></span>
* <span data-ttu-id="9446c-744">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="9446c-744">Removed two cmdlets:</span></span>
    - <span data-ttu-id="9446c-745">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9446c-745">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="9446c-746">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9446c-746">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="9446c-747">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="9446c-747">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="9446c-748">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="9446c-748">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="9446c-749">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="9446c-749">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="9446c-750">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="9446c-750">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9446c-751">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-751">Az.Monitor</span></span>
* <span data-ttu-id="9446c-752">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="9446c-752">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="9446c-753">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9446c-753">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="9446c-754">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-754">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="9446c-755">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="9446c-755">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="9446c-756">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="9446c-756">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="9446c-757">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="9446c-757">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="9446c-758">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="9446c-758">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="9446c-759">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9446c-759">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9446c-760">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9446c-760">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9446c-761">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9446c-761">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9446c-762">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9446c-762">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9446c-763">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9446c-763">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="9446c-764">[Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="9446c-764">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="9446c-765">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="9446c-765">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-766">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-766">Az.Network</span></span>
* <span data-ttu-id="9446c-767">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="9446c-767">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="9446c-768">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-768">New cmdlets</span></span>
        - <span data-ttu-id="9446c-769">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-769">New-AzNatGateway</span></span>
        - <span data-ttu-id="9446c-770">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-770">Get-AzNatGateway</span></span>
        - <span data-ttu-id="9446c-771">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-771">Set-AzNatGateway</span></span>
        - <span data-ttu-id="9446c-772">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-772">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="9446c-773">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="9446c-773">Updated cmdlets</span></span>
        - <span data-ttu-id="9446c-774">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="9446c-774">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="9446c-775">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="9446c-775">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="9446c-776">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="9446c-776">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="9446c-777">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-777">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="9446c-778">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="9446c-778">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9446c-779">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-779">Az.PolicyInsights</span></span>
* <span data-ttu-id="9446c-780">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="9446c-780">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="9446c-781">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="9446c-781">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="9446c-782">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="9446c-782">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-783">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-783">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-784">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="9446c-784">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="9446c-785">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9446c-785">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="9446c-786">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9446c-786">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="9446c-787">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9446c-787">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="9446c-788">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="9446c-788">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="9446c-789">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="9446c-789">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="9446c-790">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9446c-790">Az.Relay</span></span>
* <span data-ttu-id="9446c-791">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="9446c-791">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9446c-792">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9446c-792">Az.ServiceBus</span></span>
* <span data-ttu-id="9446c-793">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="9446c-793">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-794">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-794">Az.Storage</span></span>
* <span data-ttu-id="9446c-795">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="9446c-795">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="9446c-796">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="9446c-796">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="9446c-797">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="9446c-797">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="9446c-798">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-798">New-AzStorageAccount</span></span>
* <span data-ttu-id="9446c-799">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="9446c-799">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="9446c-800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-800">New-AzStorageAccount</span></span>
    - <span data-ttu-id="9446c-801">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-801">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="9446c-802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-802">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-803">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-803">Az.Websites</span></span>
* <span data-ttu-id="9446c-804">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9446c-804">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="9446c-805">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="9446c-805">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="9446c-806">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-806">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9446c-807">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="9446c-807">Highlights since the last major release</span></span>
* <span data-ttu-id="9446c-808">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="9446c-808">General availability of `Az` module</span></span>
* <span data-ttu-id="9446c-809">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9446c-809">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9446c-810">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9446c-810">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9446c-811">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-811">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9446c-812">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="9446c-812">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9446c-813">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-813">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9446c-814">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="9446c-814">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="9446c-815">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-815">Az.Accounts</span></span>
* <span data-ttu-id="9446c-816">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="9446c-816">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="9446c-817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9446c-817">Az.Batch</span></span>
* <span data-ttu-id="9446c-818">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-818">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9446c-819">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9446c-819">Az.Cdn</span></span>
* <span data-ttu-id="9446c-820">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-820">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9446c-821">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9446c-821">Az.CognitiveServices</span></span>
* <span data-ttu-id="9446c-822">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-822">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-823">Az.Compute</span></span>
* <span data-ttu-id="9446c-824">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="9446c-824">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="9446c-825">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-825">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9446c-826">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="9446c-826">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-827">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-827">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-828">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="9446c-828">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-829">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-829">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-830">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-830">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9446c-831">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9446c-831">Az.EventGrid</span></span>
* <span data-ttu-id="9446c-832">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="9446c-832">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9446c-833">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9446c-833">Az.EventHub</span></span>
* <span data-ttu-id="9446c-834">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="9446c-834">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="9446c-835">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9446c-835">Az.HDInsight</span></span>
* <span data-ttu-id="9446c-836">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-836">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9446c-837">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9446c-837">Az.IotHub</span></span>
* <span data-ttu-id="9446c-838">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-838">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9446c-839">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-839">Az.KeyVault</span></span>
* <span data-ttu-id="9446c-840">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-840">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9446c-841">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="9446c-841">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="9446c-842">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9446c-842">Az.MachineLearning</span></span>
* <span data-ttu-id="9446c-843">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-843">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="9446c-844">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9446c-844">Az.Media</span></span>
* <span data-ttu-id="9446c-845">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-845">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9446c-846">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-846">Az.Monitor</span></span>
  * <span data-ttu-id="9446c-847">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="9446c-847">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="9446c-848">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="9446c-848">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="9446c-849">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="9446c-849">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="9446c-850">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="9446c-850">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="9446c-851">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="9446c-851">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="9446c-852">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="9446c-852">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="9446c-853">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="9446c-853">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-854">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-854">Az.Network</span></span>
* <span data-ttu-id="9446c-855">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-855">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9446c-856">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="9446c-856">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="9446c-857">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="9446c-857">Az.NotificationHubs</span></span>
* <span data-ttu-id="9446c-858">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-859">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-859">Az.OperationalInsights</span></span>
* <span data-ttu-id="9446c-860">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-860">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="9446c-861">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="9446c-861">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="9446c-862">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-862">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-863">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-863">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-864">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9446c-865">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="9446c-865">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="9446c-866">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="9446c-866">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="9446c-867">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="9446c-867">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9446c-868">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9446c-868">Az.RedisCache</span></span>
* <span data-ttu-id="9446c-869">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-869">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-870">Az.Resources</span></span>
* <span data-ttu-id="9446c-871">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="9446c-871">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-872">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-872">Az.Sql</span></span>
* <span data-ttu-id="9446c-873">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="9446c-873">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="9446c-874">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-874">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9446c-875">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="9446c-875">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="9446c-876">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="9446c-876">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="9446c-877">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="9446c-877">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="9446c-878">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="9446c-878">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="9446c-879">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="9446c-879">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-880">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-880">Az.Websites</span></span>
* <span data-ttu-id="9446c-881">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="9446c-881">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="9446c-882">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="9446c-882">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="9446c-883">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="9446c-883">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="9446c-884">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="9446c-884">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="9446c-885">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-885">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9446c-886">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="9446c-886">Highlights since the last major release</span></span>
* <span data-ttu-id="9446c-887">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="9446c-887">General availability of `Az` module</span></span>
* <span data-ttu-id="9446c-888">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9446c-888">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9446c-889">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9446c-889">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9446c-890">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-890">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9446c-891">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="9446c-891">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9446c-892">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-892">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9446c-893">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="9446c-893">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="9446c-894">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-894">Az.Accounts</span></span>
* <span data-ttu-id="9446c-895">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9446c-895">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9446c-896">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9446c-896">Az.AnalysisServices</span></span>
* <span data-ttu-id="9446c-897">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="9446c-897">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="9446c-898">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="9446c-898">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-899">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-899">Az.Automation</span></span>
* <span data-ttu-id="9446c-900">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="9446c-900">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="9446c-901">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="9446c-901">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="9446c-902">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-902">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-903">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-903">Az.Compute</span></span>
* <span data-ttu-id="9446c-904">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-904">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="9446c-905">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="9446c-905">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="9446c-906">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-906">Az.ContainerInstance</span></span>
* <span data-ttu-id="9446c-907">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="9446c-907">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-908">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-909">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="9446c-909">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="9446c-910">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9446c-910">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-911">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-911">Az.Resources</span></span>
* <span data-ttu-id="9446c-912">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="9446c-912">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="9446c-913">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="9446c-913">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="9446c-914">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-914">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="9446c-915">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="9446c-915">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="9446c-916">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="9446c-916">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="9446c-917">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="9446c-917">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-918">Az.Sql</span></span>
* <span data-ttu-id="9446c-919">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="9446c-919">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-920">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-920">Az.Storage</span></span>
* <span data-ttu-id="9446c-921">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="9446c-921">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="9446c-922">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9446c-922">New-AzStorageContext</span></span>
* <span data-ttu-id="9446c-923">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="9446c-923">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="9446c-924">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9446c-924">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="9446c-925">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9446c-925">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="9446c-926">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-926">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="9446c-927">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-927">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="9446c-928">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="9446c-928">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="9446c-929">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9446c-929">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="9446c-930">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9446c-930">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="9446c-931">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9446c-931">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="9446c-932">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9446c-932">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="9446c-933">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-933">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="9446c-934">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="9446c-934">Highlights since the last major release</span></span>
* <span data-ttu-id="9446c-935">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="9446c-935">General availability of `Az` module</span></span>
* <span data-ttu-id="9446c-936">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="9446c-936">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="9446c-937">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="9446c-937">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="9446c-938">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-938">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="9446c-939">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="9446c-939">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9446c-940">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-940">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="9446c-941">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="9446c-941">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-942">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-942">Az.Automation</span></span>
* <span data-ttu-id="9446c-943">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="9446c-943">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="9446c-944">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="9446c-944">Dynamic grouping</span></span>
    * <span data-ttu-id="9446c-945">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="9446c-945">Pre-Post script</span></span>
    * <span data-ttu-id="9446c-946">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="9446c-946">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-947">Az.Compute</span></span>
* <span data-ttu-id="9446c-948">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="9446c-948">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="9446c-949">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="9446c-949">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9446c-950">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-950">Az.KeyVault</span></span>
* <span data-ttu-id="9446c-951">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-951">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-952">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-952">Az.Network</span></span>
* <span data-ttu-id="9446c-953">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-953">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="9446c-954">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="9446c-954">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-955">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-955">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-956">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="9446c-956">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="9446c-957">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="9446c-957">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-958">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-958">Az.Resources</span></span>
* <span data-ttu-id="9446c-959">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-959">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="9446c-960">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="9446c-960">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-961">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-961">Az.Sql</span></span>
* <span data-ttu-id="9446c-962">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="9446c-962">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-963">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-963">Az.Storage</span></span>
* <span data-ttu-id="9446c-964">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="9446c-964">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="9446c-965">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-965">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9446c-966">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-966">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9446c-967">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-967">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="9446c-968">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="9446c-968">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="9446c-969">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="9446c-969">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="9446c-970">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="9446c-970">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-971">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-971">Az.Websites</span></span>
* <span data-ttu-id="9446c-972">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="9446c-972">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="9446c-973">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-973">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-974">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-974">Az.Accounts</span></span>
* <span data-ttu-id="9446c-975">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="9446c-975">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="9446c-976">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-976">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-977">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-977">Az.Automation</span></span>
* <span data-ttu-id="9446c-978">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-978">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="9446c-979">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="9446c-979">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="9446c-980">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="9446c-980">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9446c-981">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9446c-981">Az.Cdn</span></span>
* <span data-ttu-id="9446c-982">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="9446c-982">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-983">Az.Compute</span></span>
* <span data-ttu-id="9446c-984">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="9446c-984">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-985">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-985">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-986">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="9446c-986">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9446c-987">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9446c-987">Az.LogicApp</span></span>
* <span data-ttu-id="9446c-988">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="9446c-988">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-989">Az.Network</span></span>
* <span data-ttu-id="9446c-990">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="9446c-990">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-991">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-991">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-992">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="9446c-992">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="9446c-993">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="9446c-993">SDK Update</span></span>
* <span data-ttu-id="9446c-994">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9446c-994">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="9446c-995">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9446c-995">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-996">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-996">Az.Resources</span></span>
* <span data-ttu-id="9446c-997">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="9446c-997">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="9446c-998">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="9446c-998">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="9446c-999">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="9446c-999">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="9446c-1000">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="9446c-1000">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="9446c-1001">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="9446c-1001">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="9446c-1002">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="9446c-1002">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1003">Az.Sql</span></span>
* <span data-ttu-id="9446c-1004">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="9446c-1004">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="9446c-1005">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="9446c-1005">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-1006">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-1006">Az.Storage</span></span>
* <span data-ttu-id="9446c-1007">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-1007">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="9446c-1008">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-1008">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="9446c-1009">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1009">Az.AnalysisServices</span></span>
* <span data-ttu-id="9446c-1010">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="9446c-1010">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-1011">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-1011">Az.Automation</span></span>
* <span data-ttu-id="9446c-1012">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1012">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="9446c-1013">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1013">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="9446c-1014">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1014">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="9446c-1015">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1015">Az.CognitiveServices</span></span>
* <span data-ttu-id="9446c-1016">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9446c-1016">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1017">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1017">Az.Compute</span></span>
* <span data-ttu-id="9446c-1018">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="9446c-1018">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="9446c-1019">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="9446c-1019">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="9446c-1020">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="9446c-1020">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="9446c-1021">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="9446c-1021">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1022">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1022">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-1023">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="9446c-1023">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="9446c-1024">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="9446c-1024">Az.EventHub</span></span>
* <span data-ttu-id="9446c-1025">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="9446c-1025">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="9446c-1026">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-1026">Az.KeyVault</span></span>
* <span data-ttu-id="9446c-1027">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9446c-1027">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9446c-1028">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9446c-1028">Az.LogicApp</span></span>
* <span data-ttu-id="9446c-1029">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="9446c-1029">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="9446c-1030">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="9446c-1030">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="9446c-1031">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="9446c-1031">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="9446c-1032">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9446c-1032">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9446c-1033">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9446c-1033">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9446c-1034">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9446c-1034">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="9446c-1035">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="9446c-1035">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="9446c-1036">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="9446c-1036">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="9446c-1037">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1037">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9446c-1038">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1038">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9446c-1039">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1039">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="9446c-1040">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1040">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="9446c-1041">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="9446c-1041">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="9446c-1042">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-1042">Az.Monitor</span></span>
* <span data-ttu-id="9446c-1043">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="9446c-1043">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-1044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1044">Az.Network</span></span>
* <span data-ttu-id="9446c-1045">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9446c-1045">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-1046">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-1046">Az.OperationalInsights</span></span>
* <span data-ttu-id="9446c-1047">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="9446c-1047">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="9446c-1048">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="9446c-1048">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="9446c-1049">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="9446c-1049">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="9446c-1050">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1050">Az.Resources</span></span>
* <span data-ttu-id="9446c-1051">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="9446c-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9446c-1052">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="9446c-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="9446c-1053">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="9446c-1053">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="9446c-1054">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="9446c-1054">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-1055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1055">Az.Sql</span></span>
* <span data-ttu-id="9446c-1056">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="9446c-1056">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="9446c-1057">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="9446c-1057">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-1058">Az.Websites</span></span>
* <span data-ttu-id="9446c-1059">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="9446c-1059">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="9446c-1060">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-1060">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1061">Az.Accounts</span></span>
* <span data-ttu-id="9446c-1062">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9446c-1062">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9446c-1063">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1063">Az.AnalysisServices</span></span>
<span data-ttu-id="9446c-1064">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="9446c-1064">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1065">Az.Compute</span></span>
* <span data-ttu-id="9446c-1066">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="9446c-1066">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="9446c-1067">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9446c-1067">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="9446c-1068">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="9446c-1068">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-1069">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1069">Az.RecoveryServices</span></span>
<span data-ttu-id="9446c-1070">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="9446c-1070">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-1071">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1071">Az.Resources</span></span>
* <span data-ttu-id="9446c-1072">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="9446c-1072">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="9446c-1073">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="9446c-1073">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="9446c-1074">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="9446c-1074">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="9446c-1075">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="9446c-1075">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-1076">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1076">Az.Sql</span></span>
* <span data-ttu-id="9446c-1077">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9446c-1077">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="9446c-1078">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="9446c-1078">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="9446c-1079">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="9446c-1079">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="9446c-1080">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-1080">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1081">Az.Accounts</span></span>
* <span data-ttu-id="9446c-1082">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="9446c-1082">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="9446c-1083">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1083">Az.AnalysisServices</span></span>
* <span data-ttu-id="9446c-1084">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="9446c-1084">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-1085">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1085">Az.RecoveryServices</span></span>
* <span data-ttu-id="9446c-1086">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="9446c-1086">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="9446c-1087">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-1087">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-1088">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1088">Az.Accounts</span></span>
* <span data-ttu-id="9446c-1089">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="9446c-1089">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="9446c-1090">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1090">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9446c-1091">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="9446c-1091">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="9446c-1092">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="9446c-1092">Az.Aks</span></span>
* <span data-ttu-id="9446c-1093">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1093">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="9446c-1094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-1094">Az.Automation</span></span>
* <span data-ttu-id="9446c-1095">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="9446c-1095">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="9446c-1096">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1096">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="9446c-1097">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="9446c-1097">Az.Cdn</span></span>
* <span data-ttu-id="9446c-1098">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1098">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1099">Az.Compute</span></span>
* <span data-ttu-id="9446c-1100">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="9446c-1100">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="9446c-1101">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9446c-1101">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="9446c-1102">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="9446c-1102">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="9446c-1103">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9446c-1103">Az.ContainerRegistry</span></span>
* <span data-ttu-id="9446c-1104">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1104">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="9446c-1105">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9446c-1105">Az.DataFactory</span></span>
* <span data-ttu-id="9446c-1106">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="9446c-1106">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1107">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1107">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-1108">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="9446c-1108">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="9446c-1109">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="9446c-1109">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="9446c-1110">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1110">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9446c-1111">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9446c-1111">Az.IotHub</span></span>
* <span data-ttu-id="9446c-1112">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9446c-1112">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="9446c-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-1113">Az.KeyVault</span></span>
* <span data-ttu-id="9446c-1114">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1114">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-1115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1115">Az.Network</span></span>
* <span data-ttu-id="9446c-1116">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1116">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1117">Az.Resources</span></span>
* <span data-ttu-id="9446c-1118">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="9446c-1118">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="9446c-1119">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="9446c-1119">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="9446c-1120">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9446c-1120">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="9446c-1121">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="9446c-1121">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="9446c-1122">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="9446c-1122">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="9446c-1123">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="9446c-1123">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="9446c-1124">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="9446c-1124">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9446c-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-1126">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="9446c-1126">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="9446c-1127">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9446c-1127">Fix some error messages.</span></span>
* <span data-ttu-id="9446c-1128">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="9446c-1128">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="9446c-1129">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="9446c-1129">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9446c-1130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9446c-1130">Az.SignalR</span></span>
* <span data-ttu-id="9446c-1131">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1131">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1132">Az.Sql</span></span>
* <span data-ttu-id="9446c-1133">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1133">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9446c-1134">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9446c-1134">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="9446c-1135">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="9446c-1135">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="9446c-1136">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="9446c-1136">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-1137">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-1137">Az.Storage</span></span>
* <span data-ttu-id="9446c-1138">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1138">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9446c-1139">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="9446c-1139">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="9446c-1140">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9446c-1140">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="9446c-1141">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="9446c-1141">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="9446c-1142">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9446c-1142">Az.TrafficManager</span></span>
* <span data-ttu-id="9446c-1143">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1143">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-1144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-1144">Az.Websites</span></span>
* <span data-ttu-id="9446c-1145">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="9446c-1145">Update incorrect online help URLs</span></span>
* <span data-ttu-id="9446c-1146">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="9446c-1146">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="9446c-1147">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="9446c-1147">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="9446c-1148">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="9446c-1148">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9446c-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1149">Az.Accounts</span></span>
* <span data-ttu-id="9446c-1150">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9446c-1150">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1151">Az.Compute</span></span>
* <span data-ttu-id="9446c-1152">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9446c-1152">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="9446c-1153">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="9446c-1153">Updated the description of ID in help files</span></span>
* <span data-ttu-id="9446c-1154">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1154">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1155">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-1156">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="9446c-1156">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="9446c-1157">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="9446c-1157">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9446c-1158">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9446c-1158">Az.EventGrid</span></span>
* <span data-ttu-id="9446c-1159">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="9446c-1159">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="9446c-1160">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="9446c-1160">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="9446c-1161">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="9446c-1161">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9446c-1162">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="9446c-1162">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9446c-1163">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="9446c-1163">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9446c-1164">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="9446c-1164">Dead letter endpoint.</span></span>
    - <span data-ttu-id="9446c-1165">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="9446c-1165">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9446c-1166">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="9446c-1166">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9446c-1167">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="9446c-1167">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9446c-1168">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="9446c-1168">Dead letter endpoint.</span></span>
* <span data-ttu-id="9446c-1169">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="9446c-1169">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="9446c-1170">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9446c-1170">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9446c-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9446c-1171">Az.IotHub</span></span>
* <span data-ttu-id="9446c-1172">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="9446c-1172">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9446c-1173">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9446c-1173">Az.LogicApp</span></span>
* <span data-ttu-id="9446c-1174">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="9446c-1174">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-1175">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1175">Az.Resources</span></span>
* <span data-ttu-id="9446c-1176">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="9446c-1176">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="9446c-1177">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="9446c-1177">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="9446c-1178">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9446c-1178">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9446c-1179">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9446c-1179">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="9446c-1180">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="9446c-1180">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="9446c-1181">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="9446c-1181">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9446c-1182">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9446c-1182">Az.SignalR</span></span>
* <span data-ttu-id="9446c-1183">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1183">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1184">Az.Sql</span></span>
* <span data-ttu-id="9446c-1185">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="9446c-1185">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9446c-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-1186">Az.Storage</span></span>
* <span data-ttu-id="9446c-1187">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="9446c-1187">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="9446c-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9446c-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="9446c-1189">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="9446c-1189">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="9446c-1190">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9446c-1190">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-1191">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-1191">Az.Websites</span></span>
* <span data-ttu-id="9446c-1192">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="9446c-1192">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="9446c-1193">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1193">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="9446c-1194">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1194">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="9446c-1195">Généralités</span><span class="sxs-lookup"><span data-stu-id="9446c-1195">General</span></span>

- <span data-ttu-id="9446c-1196">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="9446c-1196">General Availability of Az Module</span></span>
- <span data-ttu-id="9446c-1197">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="9446c-1197">Online help for each module</span></span>
- <span data-ttu-id="9446c-1198">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="9446c-1198">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="9446c-1199">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="9446c-1199">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="9446c-1200">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1200">Az.Accounts</span></span>
- <span data-ttu-id="9446c-1201">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9446c-1201">Changed from Az.Profile</span></span>
- <span data-ttu-id="9446c-1202">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="9446c-1202">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9446c-1203">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9446c-1203">Az.ApiManagement</span></span>
- <span data-ttu-id="9446c-1204">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="9446c-1204">Fixes for #7002</span></span>
- <span data-ttu-id="9446c-1205">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="9446c-1206">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9446c-1206">Az.Batch</span></span>
- <span data-ttu-id="9446c-1207">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="9446c-1207">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="9446c-1208">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="9446c-1208">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="9446c-1209">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1209">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="9446c-1210">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9446c-1210">Az.Billing</span></span>
- <span data-ttu-id="9446c-1211">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1211">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="9446c-1212">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1212">Az.CognitivServices</span></span>
- <span data-ttu-id="9446c-1213">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-1213">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="9446c-1214">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="9446c-1214">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9446c-1215">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-1215">Az.ContainerInstance</span></span>
- <span data-ttu-id="9446c-1216">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="9446c-1216">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="9446c-1217">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9446c-1217">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="9446c-1218">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1218">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1219">Az.DataLakeStore</span></span>
- <span data-ttu-id="9446c-1220">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1220">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="9446c-1221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9446c-1221">Az.Monitor</span></span>
- <span data-ttu-id="9446c-1222">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1222">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="9446c-1223">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9446c-1223">Az.KeyVault</span></span>
- <span data-ttu-id="9446c-1224">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="9446c-1224">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="9446c-1225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9446c-1225">Az.MachineLearning</span></span>
- <span data-ttu-id="9446c-1226">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="9446c-1226">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="9446c-1227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9446c-1227">Az.Media</span></span>
- <span data-ttu-id="9446c-1228">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9446c-1228">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9446c-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1229">Az.Network</span></span>
<span data-ttu-id="9446c-1230">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9446c-1230">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="9446c-1231">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="9446c-1231">New cmdlets added:</span></span>
        - <span data-ttu-id="9446c-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1232">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9446c-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1233">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9446c-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1234">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9446c-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1235">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9446c-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1236">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9446c-1237">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9446c-1237">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="9446c-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1238">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="9446c-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9446c-1239">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="9446c-1240">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9446c-1240">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="9446c-1241">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9446c-1241">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="9446c-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9446c-1242">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9446c-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9446c-1243">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9446c-1244">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-1244">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="9446c-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-1245">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="9446c-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="9446c-1246">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="9446c-1247">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9446c-1247">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="9446c-1248">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9446c-1248">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9446c-1249">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9446c-1249">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9446c-1250">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9446c-1250">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="9446c-1251">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9446c-1251">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="9446c-1252">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1252">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="9446c-1253">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-1253">Az.OperationalInsights</span></span>
- <span data-ttu-id="9446c-1254">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1254">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="9446c-1255">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9446c-1255">Az.Profile</span></span>
- <span data-ttu-id="9446c-1256">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9446c-1256">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1257">Az.RecoveryServices</span></span>
- <span data-ttu-id="9446c-1258">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1258">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="9446c-1259">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1259">Az.Resources</span></span>
- <span data-ttu-id="9446c-1260">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1260">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9446c-1261">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-1261">Az.ServiceFabric</span></span>
- <span data-ttu-id="9446c-1262">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="9446c-1262">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="9446c-1263">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1263">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="9446c-1264">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9446c-1264">Az.SIgnalR</span></span>
- <span data-ttu-id="9446c-1265">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9446c-1265">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="9446c-1266">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1266">Az.Sql</span></span>
- <span data-ttu-id="9446c-1267">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="9446c-1267">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="9446c-1268">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="9446c-1268">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="9446c-1269">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1269">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="9446c-1270">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-1270">Az.Storage</span></span>
- <span data-ttu-id="9446c-1271">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1271">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9446c-1272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-1272">Az.Websites</span></span>
- <span data-ttu-id="9446c-1273">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="9446c-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="9446c-1274">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1274">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="9446c-1275">Généralités</span><span class="sxs-lookup"><span data-stu-id="9446c-1275">General</span></span>

* <span data-ttu-id="9446c-1276">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="9446c-1276">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="9446c-1277">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1277">Az.Compute</span></span>

* <span data-ttu-id="9446c-1278">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="9446c-1278">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1279">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1279">Az.DataLakeStore</span></span>

* <span data-ttu-id="9446c-1280">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="9446c-1280">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="9446c-1281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9446c-1281">Az.FrontDoor</span></span>

* <span data-ttu-id="9446c-1282">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="9446c-1282">Fixed some broken links</span></span>
    - <span data-ttu-id="9446c-1283">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="9446c-1283">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="9446c-1284">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="9446c-1284">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9446c-1285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1285">Az.RecoveryServices</span></span>

* <span data-ttu-id="9446c-1286">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="9446c-1286">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="9446c-1287">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="9446c-1287">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="9446c-1288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1288">Az.Resources</span></span>

* <span data-ttu-id="9446c-1289">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="9446c-1289">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="9446c-1290">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="9446c-1290">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="9446c-1291">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1291">Az.Sql</span></span>

* <span data-ttu-id="9446c-1292">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="9446c-1292">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="9446c-1293">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="9446c-1293">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="9446c-1294">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="9446c-1294">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="9446c-1295">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-1295">Az.Storage</span></span>

* <span data-ttu-id="9446c-1296">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-1296">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="9446c-1297">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="9446c-1297">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="9446c-1298">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9446c-1298">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9446c-1299">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="9446c-1299">Support Static Website configuration</span></span>
    - <span data-ttu-id="9446c-1300">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9446c-1300">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="9446c-1301">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9446c-1301">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9446c-1302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-1302">Az.Websites</span></span>

* <span data-ttu-id="9446c-1303">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9446c-1303">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="9446c-1304">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="9446c-1304">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="9446c-1305">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="9446c-1305">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="9446c-1306">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1306">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9446c-1307">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9446c-1307">Az.ApiManagement</span></span>
* <span data-ttu-id="9446c-1308">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="9446c-1308">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="9446c-1309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9446c-1309">Az.Automation</span></span>
* <span data-ttu-id="9446c-1310">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="9446c-1310">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="9446c-1311">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="9446c-1311">Added Update Management cmdlets</span></span>
* <span data-ttu-id="9446c-1312">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="9446c-1312">Added Source Control cmdlets</span></span>
* <span data-ttu-id="9446c-1313">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="9446c-1313">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="9446c-1314">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="9446c-1314">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="9446c-1315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1315">Az.Compute</span></span>
* <span data-ttu-id="9446c-1316">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="9446c-1316">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="9446c-1317">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="9446c-1317">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9446c-1318">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-1318">Az.ContainerInstance</span></span>
* <span data-ttu-id="9446c-1319">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="9446c-1319">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="9446c-1320">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9446c-1320">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="9446c-1321">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="9446c-1321">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9446c-1322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1322">Az.Network</span></span>
* <span data-ttu-id="9446c-1323">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9446c-1323">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="9446c-1324">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="9446c-1324">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="9446c-1325">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="9446c-1325">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="9446c-1326">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9446c-1326">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="9446c-1327">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9446c-1327">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9446c-1328">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="9446c-1328">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="9446c-1329">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="9446c-1329">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="9446c-1330">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9446c-1330">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9446c-1331">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9446c-1331">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="9446c-1332">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="9446c-1332">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="9446c-1333">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9446c-1333">Az.Relay</span></span>
* <span data-ttu-id="9446c-1334">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="9446c-1334">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="9446c-1335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1335">Az.Resources</span></span>
* <span data-ttu-id="9446c-1336">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="9446c-1336">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="9446c-1337">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="9446c-1337">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="9446c-1338">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="9446c-1338">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9446c-1339">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-1339">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-1340">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="9446c-1340">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="9446c-1341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1341">Az.Sql</span></span>
* <span data-ttu-id="9446c-1342">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="9446c-1342">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="9446c-1343">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-1343">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9446c-1344">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-1344">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9446c-1345">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-1345">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9446c-1346">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9446c-1346">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9446c-1347">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9446c-1347">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9446c-1348">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9446c-1348">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9446c-1349">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9446c-1349">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9446c-1350">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9446c-1350">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="9446c-1351">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="9446c-1351">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="9446c-1352">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="9446c-1352">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="9446c-1353">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="9446c-1353">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="9446c-1354">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9446c-1354">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9446c-1355">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="9446c-1355">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9446c-1356">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9446c-1356">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="9446c-1357">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="9446c-1357">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="9446c-1358">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="9446c-1358">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="9446c-1359">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1359">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9446c-1360">Généralités</span><span class="sxs-lookup"><span data-stu-id="9446c-1360">General</span></span>
* <span data-ttu-id="9446c-1361">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="9446c-1361">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="9446c-1362">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9446c-1362">Az.Profile</span></span>
* <span data-ttu-id="9446c-1363">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9446c-1363">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="9446c-1364">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="9446c-1364">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="9446c-1365">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="9446c-1365">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="9446c-1366">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="9446c-1366">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="9446c-1367">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="9446c-1367">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="9446c-1368">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="9446c-1368">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="9446c-1369">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="9446c-1369">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="9446c-1370">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1370">Az.CognitiveServices</span></span>
* <span data-ttu-id="9446c-1371">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="9446c-1371">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1372">Az.Compute</span></span>
* <span data-ttu-id="9446c-1373">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9446c-1373">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="9446c-1374">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="9446c-1374">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="9446c-1375">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="9446c-1375">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1376">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-1377">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="9446c-1377">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="9446c-1378">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="9446c-1378">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="9446c-1379">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="9446c-1379">Az.Insights</span></span>
* <span data-ttu-id="9446c-1380">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="9446c-1380">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="9446c-1381">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="9446c-1381">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="9446c-1382">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="9446c-1382">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="9446c-1383">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="9446c-1383">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-1384">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1384">Az.Network</span></span>
* <span data-ttu-id="9446c-1385">Modification du type de peering en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="9446c-1385">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="9446c-1386">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="9446c-1386">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="9446c-1387">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9446c-1387">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="9446c-1388">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9446c-1388">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="9446c-1389">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="9446c-1389">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9446c-1390">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9446c-1390">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9446c-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9446c-1391">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9446c-1392">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9446c-1392">Az.PolicyInsights</span></span>
* <span data-ttu-id="9446c-1393">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="9446c-1393">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-1394">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1394">Az.Resources</span></span>
* <span data-ttu-id="9446c-1395">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="9446c-1395">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="9446c-1396">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="9446c-1396">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9446c-1397">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9446c-1397">Az.ServiceBus</span></span>
* <span data-ttu-id="9446c-1398">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="9446c-1398">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9446c-1399">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9446c-1399">Az.ServiceFabric</span></span>
* <span data-ttu-id="9446c-1400">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="9446c-1400">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="9446c-1401">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="9446c-1401">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="9446c-1402">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="9446c-1402">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="9446c-1403">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="9446c-1403">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="9446c-1404">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="9446c-1404">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="9446c-1405">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1405">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="9446c-1406">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9446c-1406">Az.Profile</span></span>
* <span data-ttu-id="9446c-1407">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="9446c-1407">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="9446c-1408">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9446c-1408">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1409">Az.Compute</span></span>
* <span data-ttu-id="9446c-1410">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="9446c-1410">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="9446c-1411">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="9446c-1411">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9446c-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9446c-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="9446c-1413">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="9446c-1413">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="9446c-1414">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9446c-1414">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="9446c-1415">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="9446c-1415">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9446c-1416">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="9446c-1416">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9446c-1417">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9446c-1417">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-1418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1418">Az.Network</span></span>
* <span data-ttu-id="9446c-1419">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="9446c-1419">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="9446c-1420">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="9446c-1420">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1421">Az.Resources</span></span>
* <span data-ttu-id="9446c-1422">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="9446c-1422">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="9446c-1423">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="9446c-1423">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="9446c-1424">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1424">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="9446c-1425">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9446c-1425">Azure.Storage</span></span>
* <span data-ttu-id="9446c-1426">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9446c-1426">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="9446c-1427">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9446c-1427">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="9446c-1428">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9446c-1428">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9446c-1429">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="9446c-1429">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="9446c-1430">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="9446c-1430">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="9446c-1431">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9446c-1431">Az.CognitiveServices</span></span>
* <span data-ttu-id="9446c-1432">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="9446c-1432">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9446c-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9446c-1433">Az.Compute</span></span>
* <span data-ttu-id="9446c-1434">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="9446c-1434">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="9446c-1435">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="9446c-1435">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="9446c-1436">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="9446c-1436">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="9446c-1437">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9446c-1437">Az.DataFactoryV2</span></span>
* <span data-ttu-id="9446c-1438">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="9446c-1438">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9446c-1439">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9446c-1439">Az.Network</span></span>
* <span data-ttu-id="9446c-1440">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="9446c-1440">Added NetworkProfile functionality.</span></span> <span data-ttu-id="9446c-1441">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="9446c-1441">new cmdlets added</span></span>
    - <span data-ttu-id="9446c-1442">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9446c-1442">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="9446c-1443">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9446c-1443">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="9446c-1444">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9446c-1444">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="9446c-1445">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9446c-1445">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="9446c-1446">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-1446">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="9446c-1447">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-1447">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="9446c-1448">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="9446c-1448">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="9446c-1449">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9446c-1449">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="9446c-1450">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9446c-1450">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9446c-1451">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9446c-1451">Az.RedisCache</span></span>
* <span data-ttu-id="9446c-1452">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="9446c-1452">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="9446c-1453">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="9446c-1453">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="9446c-1454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9446c-1454">Az.Resources</span></span>
* <span data-ttu-id="9446c-1455">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9446c-1455">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9446c-1456">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="9446c-1456">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="9446c-1457">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9446c-1457">Az.Sql</span></span>
* <span data-ttu-id="9446c-1458">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="9446c-1458">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9446c-1459">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9446c-1459">Az.Websites</span></span>
* <span data-ttu-id="9446c-1460">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="9446c-1460">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="9446c-1461">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="9446c-1461">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="9446c-1462">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="9446c-1462">0.2.0 - September 2018</span></span>
 <span data-ttu-id="9446c-1463">Version initiale</span><span class="sxs-lookup"><span data-stu-id="9446c-1463">Initial Release</span></span>