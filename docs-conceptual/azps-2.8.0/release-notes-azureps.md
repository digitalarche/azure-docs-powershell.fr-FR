---
title: Notes de publication Azure PowerShell
description: Découvrez toutes les dernières mises à jour des modules Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 8c1369cdedf8848f3c62ca6b6bc4eb3d2d78be95
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2019
ms.locfileid: "74656822"
---
## <a name="280---october-2019"></a><span data-ttu-id="e552e-103">2.8.0 - octobre 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e552e-104">Généralités</span><span class="sxs-lookup"><span data-stu-id="e552e-104">General</span></span>
* <span data-ttu-id="e552e-105">Az.HealthcareApis 1.0.0 release</span><span class="sxs-lookup"><span data-stu-id="e552e-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e552e-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-106">Az.Accounts</span></span>
* <span data-ttu-id="e552e-107">Mise à jour de la télémétrie et réécriture des URL pour les modules générés, correction des tests unitaires Windows.</span><span class="sxs-lookup"><span data-stu-id="e552e-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e552e-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-108">Az.ApiManagement</span></span>
* <span data-ttu-id="e552e-109">**Set-AzApiManagementApi** - Ajout de la prise en charge de la mise à jour d’Api dans ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e552e-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e552e-110">Corriger le problème https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="e552e-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-111">Az.Automation</span></span>
* <span data-ttu-id="e552e-112">Correction de l’applet de commande New-AzureAutomationSoftwareUpdateConfiguration pour le paramètre de définition de redémarrage Linux.</span><span class="sxs-lookup"><span data-stu-id="e552e-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="e552e-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e552e-113">Az.Batch</span></span>
* <span data-ttu-id="e552e-114">**Get-AzBatchNodeAgentSku** est déprécié et va être remplacé par **Get-AzBatchSupportImage** dans la version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="e552e-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-115">Az.Compute</span></span>
* <span data-ttu-id="e552e-116">Ajout des paramètres Priority, EvictionPolicy et MaxPrice aux applets de commande New-AzVM et New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e552e-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e552e-117">Correction du message d’avertissement et du document d’aide pour les applets de commande Add-AzVMAdditionalUnattendContent et Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e552e-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e552e-118">Correction de l’exception Fix-skipVmBackup pour les machines virtuelles Linux avec des disques managés pour Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="e552e-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="e552e-119">Correction du bogue dans les paramètres de chiffrement de mise à jour dans Set-AzVMDiskEncryptionExtension, deux scénarios de réussite.</span><span class="sxs-lookup"><span data-stu-id="e552e-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-120">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-121">Ajout des commandes CRUD pour le flux de données ADF V2 : Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow et Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="e552e-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e552e-122">Ajout de commandes d’action pour la session de débogage de flux de données ADF V2 : Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand et Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="e552e-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e552e-123">Mise à jour de la version du SDK .NET ADF vers la version 4.2.0</span><span class="sxs-lookup"><span data-stu-id="e552e-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-125">Correction de la validation de compte afin que les comptes avec '-' puissent être passés sans domaine</span><span class="sxs-lookup"><span data-stu-id="e552e-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e552e-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e552e-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="e552e-127">Mise à jour de la version PowerShell vers 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e552e-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e552e-128">Mise à jour de la version du SDK vers 1.0.2</span><span class="sxs-lookup"><span data-stu-id="e552e-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e552e-129">Mise à jour dans les tests pour faire référence à la nouvelle version du SDK</span><span class="sxs-lookup"><span data-stu-id="e552e-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e552e-130">Mise à jour de la structure de sortie qui passe d’un état imbriqué à un état aplati.</span><span class="sxs-lookup"><span data-stu-id="e552e-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e552e-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-131">Az.IotHub</span></span>
* <span data-ttu-id="e552e-132">Ajout d’une nouvelle source de routage : DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e552e-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e552e-133">Correctif de bogues mineurs : Get-AzIothub ne retourne pas subscriptionId</span><span class="sxs-lookup"><span data-stu-id="e552e-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="e552e-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-134">Az.Monitor</span></span>
* <span data-ttu-id="e552e-135">Nouveaux récepteurs de groupe d’actions ajoutés pour New-AzActionGroupReceiver :   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e552e-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e552e-136">Utiliser le schéma d’alerte commun activé pour les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="e552e-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e552e-137">Cela ne s’applique pas aux SMS, au push Azure App, à ITSM et aux systèmes vocaux</span><span class="sxs-lookup"><span data-stu-id="e552e-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e552e-138">Les webhooks prennent maintenant en charge l’authentification Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e552e-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-139">Az.Network</span></span>
* <span data-ttu-id="e552e-140">Ajout de la nouvelle applet de commande Get-AzAvailableServiceAlias qui peut être appelée pour obtenir des alias pouvant être utilisés pour les stratégies de point de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="e552e-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e552e-141">Ajout de la prise en charge des sélecteurs de trafic pour les connexions de passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="e552e-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e552e-142">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="e552e-142">New cmdlets added:</span></span>
        - <span data-ttu-id="e552e-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e552e-144">Applets de commande mises à jour avec un paramètre facultatif -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e552e-145">Ajout de la prise en charge des protocoles ESP et AH dans les configurations de règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="e552e-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e552e-146">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="e552e-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="e552e-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e552e-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e552e-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e552e-150">Amélioration de la gestion des exceptions dans les applets de commande cortex</span><span class="sxs-lookup"><span data-stu-id="e552e-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e552e-151">Nouvelles générations et références SKU pour VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e552e-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e552e-152">Introduction de nouvelles générations pour VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="e552e-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e552e-153">Introduction de nouvelles références SKU haut débit pour VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="e552e-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e552e-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e552e-154">Az.RedisCache</span></span>
* <span data-ttu-id="e552e-155">Mise à jour de la documentation de référence 'Set-AzRedisCache' afin d’inclure les valeurs manquantes pour le paramètre '-Size'</span><span class="sxs-lookup"><span data-stu-id="e552e-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-156">Az.Sql</span></span>
* <span data-ttu-id="e552e-157">Ajout de la prise en charge de la définition de l’administrateur Active Directory sur Managed Instance</span><span class="sxs-lookup"><span data-stu-id="e552e-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-158">Az.Storage</span></span>
* <span data-ttu-id="e552e-159">Mise à niveau de la bibliothèque de client de stockage vers la version 11.1.0</span><span class="sxs-lookup"><span data-stu-id="e552e-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e552e-160">Listing des conteneurs avec l’API de plan de gestion, sera listé avec NextPageLink</span><span class="sxs-lookup"><span data-stu-id="e552e-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e552e-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e552e-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e552e-162">Listing des comptes de stockage de l’abonnement, sera listé avec NextPageLink</span><span class="sxs-lookup"><span data-stu-id="e552e-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e552e-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e552e-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e552e-164">Az.StorageSync</span></span>
* <span data-ttu-id="e552e-165">Correction du problème 9810 dans Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="e552e-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-166">Az.Websites</span></span>
* <span data-ttu-id="e552e-167">Échec de la mise à jour Set-AzWebApp avec l’ASP d’une application</span><span class="sxs-lookup"><span data-stu-id="e552e-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e552e-168">2.7.0 - septembre 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e552e-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-169">Az.ApiManagement</span></span>
* <span data-ttu-id="e552e-170">Mise à jour de la description du paramètre « -Format » dans la documentation de référence de « Set-AzApiManagementPolicy »</span><span class="sxs-lookup"><span data-stu-id="e552e-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e552e-171">Suppression des références de la cmdlet dépréciée « Update-AzApiManagementDeployment » dans la documentation de référence.</span><span class="sxs-lookup"><span data-stu-id="e552e-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e552e-172">Utilisation de « Set-AzApiManagement » à la place.</span><span class="sxs-lookup"><span data-stu-id="e552e-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-173">Az.Automation</span></span>
* <span data-ttu-id="e552e-174">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Register-AzAutomationDscNode »</span><span class="sxs-lookup"><span data-stu-id="e552e-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e552e-175">Ajout d’une précision sur la restriction de système d’exploitation à Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="e552e-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e552e-176">Correction de l’exception de référence Null de la comdlet Start-AzAutomationRunbook pour l’option -Wait.</span><span class="sxs-lookup"><span data-stu-id="e552e-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-177">Az.Compute</span></span>
* <span data-ttu-id="e552e-178">Ajout du paramètre UploadSizeInBytes à New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e552e-179">Ajout du paramètre Incremental à New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e552e-180">Ajouter d’une fonctionnalité de machine virtuelle basse priorité :</span><span class="sxs-lookup"><span data-stu-id="e552e-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e552e-181">Les paramètres MaxPrice, EvictionPolicy et Priority sont ajoutés à New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="e552e-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e552e-182">Le paramètre MaxPrice est ajouté aux cmdlets New-AzVmssConfig, Update-AzVM et Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e552e-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e552e-183">Correction du problème de référence de machine virtuelle pour la cmdlet AzAvailabilitySet quand elle liste tous les groupes à haute disponibilité inclus dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="e552e-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e552e-184">Correction de l’exception Null pour Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="e552e-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e552e-185">Correction de la méthode de recherche de disque dur virtuel pour la position relative de fin.</span><span class="sxs-lookup"><span data-stu-id="e552e-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e552e-186">Correction du problème UltraSSD pour New-AzVM et Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e552e-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-187">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-188">Ajout de 3 nouvelles commandes pour ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription et Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e552e-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e552e-189">Mise à jour de la version du SDK .NET ADF vers la version 4.1.3</span><span class="sxs-lookup"><span data-stu-id="e552e-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e552e-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e552e-190">Az.HDInsight</span></span>
* <span data-ttu-id="e552e-191">Explication des changements cassants</span><span class="sxs-lookup"><span data-stu-id="e552e-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e552e-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-192">Az.IotHub</span></span>
* <span data-ttu-id="e552e-193">Ajout de la prise en charge pour appeler le basculement d’un IotHub vers la région de reprise d’activité géocouplée.</span><span class="sxs-lookup"><span data-stu-id="e552e-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e552e-194">Ajout de la prise en charge pour gérer l’enrichissement de message pour un IotHub.</span><span class="sxs-lookup"><span data-stu-id="e552e-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e552e-195">Les nouvelles cmdlets sont :</span><span class="sxs-lookup"><span data-stu-id="e552e-195">New cmdlets are:</span></span>
    - <span data-ttu-id="e552e-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e552e-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e552e-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e552e-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e552e-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e552e-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e552e-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e552e-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e552e-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-200">Az.Monitor</span></span>
* <span data-ttu-id="e552e-201">Pointage vers le dernier SDK Monitor, par exemple, 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="e552e-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e552e-202">Ajout de changements non cassants aux cmdlets Metrics, c.-à-d. que l’énumération Unit prend en charge plusieurs nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="e552e-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e552e-203">Il s’agit de cmdlets en lecture seule, donc aucune modification n’est apportée à leur entrée.</span><span class="sxs-lookup"><span data-stu-id="e552e-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e552e-204">La version d’API des demandes **ActionGroups** est désormais **2019-06-01**, auparavant il s’agissait de la version **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="e552e-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e552e-205">Les tests de scénario ont été mis à jour pour tenir compte de cette modification.</span><span class="sxs-lookup"><span data-stu-id="e552e-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e552e-206">Les constructeurs des classes **EmailReceiver** et **WebhookReceiver** ont un nouvel argument obligatoire, à savoir une valeur booléenne appelée **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="e552e-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e552e-207">Actuellement, la valeur est définie sur **false** pour masquer ce changement cassant par rapport aux cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e552e-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e552e-208">**REMARQUE** : Il s’agit d’une modification temporaire qui doit être validée par l’équipe des alertes.</span><span class="sxs-lookup"><span data-stu-id="e552e-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e552e-209">L’ordre des arguments pour le constructeur de la classe **Source** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="e552e-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e552e-210">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="e552e-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e552e-211">L’ordre des arguments pour le constructeur de la classe **AlertingAction** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="e552e-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e552e-212">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="e552e-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e552e-213">Prise en charge des critères de seuil dynamique pour l’alerte de métrique V2</span><span class="sxs-lookup"><span data-stu-id="e552e-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e552e-214">New-AzMetricAlertRuleV2Criteria : création de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="e552e-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e552e-215">Add-AzMetricAlertRuleV2 : acceptation de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="e552e-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e552e-216">Améliorations apportées aux cmdlets de règle de requête planifiée</span><span class="sxs-lookup"><span data-stu-id="e552e-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e552e-217">Les cmdlets acceptent le paramètre « location » dans les deux formats, à savoir l’emplacement (par exemple, usa-est) ou le nom d’affichage de l’emplacement (par exemple, USA Est)</span><span class="sxs-lookup"><span data-stu-id="e552e-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e552e-218">Illustration correcte du paramètre « Enabled » dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="e552e-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e552e-219">Ajout d’exemples pour le paramètre facultatif « ActionGroup »</span><span class="sxs-lookup"><span data-stu-id="e552e-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e552e-220">Amélioration globale des fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="e552e-220">Overall improved help files</span></span>
* <span data-ttu-id="e552e-221">Correction du bogue lié à la détermination du type d’étendue pour « Set-AzActionRule »</span><span class="sxs-lookup"><span data-stu-id="e552e-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-222">Az.Network</span></span>
* <span data-ttu-id="e552e-223">Correction de l’exemple incorrect dans la documentation de référence de « New-AzApplicationGateway »</span><span class="sxs-lookup"><span data-stu-id="e552e-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="e552e-224">Ajout d’une remarque à la documentation de référence de « Get-AzNetworkWatcherPacketCapturee » à propos de la récupération de toutes les propriétés d’une capture de paquets</span><span class="sxs-lookup"><span data-stu-id="e552e-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e552e-225">Correction de l’exemple dans la documentation de référence de « Test-AzNetworkWatcherIPFlow » pour énumérer correctement les cartes réseau</span><span class="sxs-lookup"><span data-stu-id="e552e-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e552e-226">Amélioration de l’analyse des exceptions cloud pour afficher des détails supplémentaires s’ils existent</span><span class="sxs-lookup"><span data-stu-id="e552e-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e552e-227">Amélioration de l’analyse des exceptions cloud pour gérer un type supplémentaire d’exception de SDK</span><span class="sxs-lookup"><span data-stu-id="e552e-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e552e-228">Correction du mappage incorrect des modèles de règle de sécurité</span><span class="sxs-lookup"><span data-stu-id="e552e-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e552e-229">Ajout de propriétés à une interface réseau pour la fonctionnalité d’adresse IP privée</span><span class="sxs-lookup"><span data-stu-id="e552e-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e552e-230">Ajout de la propriété « PrivateEndpoint » comme type de PSResourceId à PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e552e-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e552e-231">Ajout de la propriété « PrivateLinkConnectionProperties » comme type de PSIpConfigurationConnectivityInformation à PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e552e-232">Ajout d’une nouvelle classe de modèle PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="e552e-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e552e-233">Ajout de « MSSQL » ApplicationRuleProtocolType pour la ressource du Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e552e-234">Prise en charge de liaisons multiples dans Azure Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="e552e-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e552e-235">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-235">New cmdlets</span></span>
        - <span data-ttu-id="e552e-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e552e-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e552e-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e552e-238">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="e552e-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="e552e-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e552e-239">New-VpnSite</span></span>
        - <span data-ttu-id="e552e-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e552e-240">Update-VpnSite</span></span>
        - <span data-ttu-id="e552e-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-241">New-VpnConnection</span></span>
        - <span data-ttu-id="e552e-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-242">Update-VpnConnection</span></span>
* <span data-ttu-id="e552e-243">Correction des documents de certains exemples PowerShell pour utiliser des cmdlets Az à la place de cmdlets AzureRM</span><span class="sxs-lookup"><span data-stu-id="e552e-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-245">Mise à jour de l’objet AzureVMpolicy avec l’attribut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="e552e-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e552e-246">Ajout de tests pour la stratégie de machine virtuelle et la restauration du compte de stockage d’origine</span><span class="sxs-lookup"><span data-stu-id="e552e-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-247">Az.Resources</span></span>
* <span data-ttu-id="e552e-248">Correction du bogue qui empêchait l’appel de New-AzRoleAssignment sans paramètre d’étendue.</span><span class="sxs-lookup"><span data-stu-id="e552e-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e552e-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-250">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="e552e-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e552e-251">Ajout de nouvelles cmdlets pour gérer les applications et les services :</span><span class="sxs-lookup"><span data-stu-id="e552e-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e552e-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e552e-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e552e-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e552e-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e552e-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e552e-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e552e-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e552e-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e552e-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e552e-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e552e-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e552e-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e552e-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e552e-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e552e-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e552e-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e552e-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e552e-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e552e-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e552e-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e552e-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e552e-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e552e-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e552e-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e552e-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e552e-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e552e-265">Mise à niveau du SDK Service Fabric vers la version 1.2.0 qui utilise la version d’API du fournisseur de ressources Service Fabric 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="e552e-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e552e-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e552e-266">Az.SignalR</span></span>
* <span data-ttu-id="e552e-267">Ajout de cmdlets Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="e552e-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-268">Az.Sql</span></span>
* <span data-ttu-id="e552e-269">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzSqlElasticPool »</span><span class="sxs-lookup"><span data-stu-id="e552e-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e552e-270">Ajout d’un exemple vCore à la création d’un pool élastique (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="e552e-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e552e-271">Suppression de la validation de EmailAddresses et de la vérification que EmailAdmins n’a pas la valeur false quand EmailAddresses est vide dans Set-AzSqlServerAdvancedThreatProtectionPolicy et Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e552e-272">Activation de la suppression des paramètres d’audit du serveur/de la base de données quand il existe plusieurs paramètres de diagnostic qui activent la catégorie d’audit.</span><span class="sxs-lookup"><span data-stu-id="e552e-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e552e-273">Correction de la validation des adresses e-mail dans plusieurs cmdlets d’évaluation des vulnérabilités SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting et Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="e552e-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-274">Az.Storage</span></span>
* <span data-ttu-id="e552e-275">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzStorageAccountKey »</span><span class="sxs-lookup"><span data-stu-id="e552e-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e552e-276">Lors d’un chargement/téléchargement de fichier Azure, prise en charge de la conservation des propriétés SMB des fichiers sources (attributs du fichier, heure de création du fichier, heure de la dernière écriture du fichier) dans le fichier de destination</span><span class="sxs-lookup"><span data-stu-id="e552e-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e552e-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e552e-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e552e-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e552e-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e552e-279">Correction de l’échec de chargement de l’objet blob de blocs avec des propriétés/métadonnées sur ImmutabilityPolicy avec conteneur activé.</span><span class="sxs-lookup"><span data-stu-id="e552e-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e552e-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e552e-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e552e-281">Prise en charge de la gestion des partages de fichiers Azure avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="e552e-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e552e-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e552e-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e552e-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e552e-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e552e-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e552e-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e552e-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e552e-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-286">Az.Websites</span></span>
* <span data-ttu-id="e552e-287">Résolution du problème de suppression des balises webapp lors de la migration de l’application vers un nouvel ASP</span><span class="sxs-lookup"><span data-stu-id="e552e-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e552e-288">Correction de Publish-AzureWebapp pour un fonctionnement sur Linux et Windows</span><span class="sxs-lookup"><span data-stu-id="e552e-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e552e-289">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzWebAppPublishingProfile »</span><span class="sxs-lookup"><span data-stu-id="e552e-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e552e-290">2.6.0 - Août 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e552e-291">Généralités</span><span class="sxs-lookup"><span data-stu-id="e552e-291">General</span></span>
* <span data-ttu-id="e552e-292">Correction des fautes de frappe diverses dans de nombreux modules</span><span class="sxs-lookup"><span data-stu-id="e552e-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e552e-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-293">Az.Accounts</span></span>
* <span data-ttu-id="e552e-294">Prise en charge de l’identité MSI affectée à l’utilisateur dans l’authentification Azure Functions (n° 9479)</span><span class="sxs-lookup"><span data-stu-id="e552e-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e552e-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e552e-295">Az.Aks</span></span>
* <span data-ttu-id="e552e-296">Résolution du problème relatif à la sortie de « Get-AzAks »</span><span class="sxs-lookup"><span data-stu-id="e552e-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e552e-297">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e552e-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e552e-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-298">Az.ApiManagement</span></span>
* <span data-ttu-id="e552e-299">Corriger le problème https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="e552e-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e552e-300">Mise à jour de la version de .Net NuGet, qui n’applique pas de restrictions sur productId, apiId, groupId et userId</span><span class="sxs-lookup"><span data-stu-id="e552e-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e552e-301">**Get-AzApiManagementProduct** : ajout de la prise en charge de l’interrogation de produits à l’aide d’une API.</span><span class="sxs-lookup"><span data-stu-id="e552e-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e552e-302">**New-AzApiManagementApiRevision** : résolution du problème où ApiRevisionDescription n’était pas défini lors de la création d’une révision d’API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e552e-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e552e-303">Correction d’une faute de frappe dans le modèle « PsApiManagementOAuth2AuthrozationServer » remplacé par « PsApiManagementOAuth2AuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="e552e-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e552e-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e552e-304">Az.Batch</span></span>
* <span data-ttu-id="e552e-305">Correction d’une faute de frappe dans un message d’aide et la documentation pour mettre Windows en majuscules</span><span class="sxs-lookup"><span data-stu-id="e552e-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e552e-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e552e-306">Az.Cdn</span></span>
* <span data-ttu-id="e552e-307">Correction d’une faute de frappe dans l’application d’assistance du module CDN</span><span class="sxs-lookup"><span data-stu-id="e552e-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-308">Az.Compute</span></span>
* <span data-ttu-id="e552e-309">Ajout de VmssId à l’applet de commande New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e552e-310">Ajout des paramètres TerminateScheduledEvents et TerminateScheduledEventNotBeforeTimeoutInMinutes à New-AzVmssConfig et Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e552e-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e552e-311">Ajout de la propriété HyperVGeneration à l’objet image de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="e552e-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e552e-312">Ajout des fonctionnalités Host et HostGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e552e-313">Nouvelles applets de commande :   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e552e-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e552e-314">Le paramètre HostId est ajouté à New-AzVMConfig et New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e552e-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e552e-315">Mise à jour de l’exemple dans la documentation « Invoke-AzVMRunCommand » de manière utiliser le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="e552e-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e552e-316">Mise à jour de la description « -VolumeType » dans la documentation de référence de « Set-AzVMDiskEncryptionExtension » et de « Set-AzVmssDiskEncryptionExtension »</span><span class="sxs-lookup"><span data-stu-id="e552e-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-317">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-318">Correction de la faute de frappe pour mettre « Windows » en majuscules dans la documentation de « New-AzDataFactoryEncryptValue »</span><span class="sxs-lookup"><span data-stu-id="e552e-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e552e-319">Mise à jour de la version du SDK .NET ADF vers la version 4.1.2</span><span class="sxs-lookup"><span data-stu-id="e552e-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e552e-320">Ajout des paramètres « DataProxyIntegrationRuntimeName », « DataProxyStagingLinkedServiceName » et « DataProxyStagingPath » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin de permettre la configuration du runtime d’intégration auto-hébergé comme proxy pour SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="e552e-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e552e-321">Mise à jour de PSTriggerRun pour afficher les pipelines déclenchés, le message et les propriétés, et de PSActivityRun pour afficher le type d’activité</span><span class="sxs-lookup"><span data-stu-id="e552e-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-323">Correction de la suspension de Get-DataLakeStoreDeletedItem pour toutes les erreurs ou exceptions à distance.</span><span class="sxs-lookup"><span data-stu-id="e552e-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e552e-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e552e-324">Az.EventHub</span></span>
* <span data-ttu-id="e552e-325">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNteworkRule dans Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e552e-326">Résolution du problème n° 9558 : Set-AzEventHubNamespace utilise PATCH au lieu de PUT</span><span class="sxs-lookup"><span data-stu-id="e552e-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e552e-327">Ajout du paramètre EnableKafka à l’applet de commande Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e552e-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e552e-328">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="e552e-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e552e-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e552e-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e552e-330">Résolution de la faute de frappe où « Azure » était tout en minuscules dans la documentation</span><span class="sxs-lookup"><span data-stu-id="e552e-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e552e-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-331">Az.Monitor</span></span>
* <span data-ttu-id="e552e-332">Correction du nom de paramètre incorrect dans la documentation</span><span class="sxs-lookup"><span data-stu-id="e552e-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-333">Az.Network</span></span>
* <span data-ttu-id="e552e-334">Mise à jour dans New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e552e-335">Dépréciation du paramètre « PublicIpAddress », car il n’est jamais utilisé côté serveur.</span><span class="sxs-lookup"><span data-stu-id="e552e-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e552e-336">Ajout d’un paramètre facultatif « Primary » qui indique si la configuration IP actuelle est primaire ou non.</span><span class="sxs-lookup"><span data-stu-id="e552e-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e552e-337">Amélioration de la gestion de l’exception d’erreur de demande à partir du SDK : résolution du problème où les exceptions du SDK n’étaient précédemment pas gérées correctement, ce qui empêchait l’affichage des détails des erreurs de clé</span><span class="sxs-lookup"><span data-stu-id="e552e-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e552e-338">Ajustement de la logique de validation pour le préfixe IP IPv6 afin de rechercher la longueur de préfixe IPv6 appropriée.</span><span class="sxs-lookup"><span data-stu-id="e552e-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="e552e-339">Mise à jour de Get-AzVirtualNetworkSubnetConfig : Ajout d’un paramètre défini pour obtenir l’ID de ressource de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="e552e-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e552e-340">Mise à jour de la description du paramètre Location pour AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e552e-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="e552e-342">Mise à jour de la documentation pour « New-AzOperationalInsightsLinuxSyslogDataSource »</span><span class="sxs-lookup"><span data-stu-id="e552e-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e552e-343">Ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="e552e-343">Added example</span></span>
    - <span data-ttu-id="e552e-344">Mise à jour de la description du paramètre « -Name »</span><span class="sxs-lookup"><span data-stu-id="e552e-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e552e-345">Ajout d’un exemple pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e552e-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e552e-346">Changement de la description du paramètre -Name pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e552e-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-348">Mise à jour de « Get-AzRecoveryServicesBackupJobDetail.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-349">Az.Resources</span></span>
* <span data-ttu-id="e552e-350">Ajout de la prise en charge de la nouvelle API version 2019-05-10 pour Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="e552e-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e552e-351">Ajout de la prise en charge de « copy.count = 0 » pour les variables, les ressources et les propriétés</span><span class="sxs-lookup"><span data-stu-id="e552e-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e552e-352">Les ressources avec « condition = false » ou « copy.count = 0 » seront supprimées en mode Complet</span><span class="sxs-lookup"><span data-stu-id="e552e-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e552e-353">Ajout d’un exemple d’affectation de stratégie au niveau de l’abonnement à la documentation d’aide</span><span class="sxs-lookup"><span data-stu-id="e552e-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e552e-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e552e-354">Az.ServiceBus</span></span>
* <span data-ttu-id="e552e-355">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNetworkRule dans Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e552e-356">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="e552e-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e552e-357">Ajout de la nouvelle commande « Test-AzServiceBusNameAvailability » afin de vérifier la disponibilité du nom pour la file d’attente et la rubrique</span><span class="sxs-lookup"><span data-stu-id="e552e-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="e552e-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-359">Correction des bogues relatifs à l’applet de commande add node type :</span><span class="sxs-lookup"><span data-stu-id="e552e-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e552e-360">bogue NullReferenceException quand un groupe de ressources avait d’autres groupes de machines virtuelles identiques non liés au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e552e-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e552e-361">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e552e-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e552e-362">Correction du bogue où l’applet de commande échouait si virtualNetwork se trouvait dans un groupe de ressources différent de celui du cluster.</span><span class="sxs-lookup"><span data-stu-id="e552e-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e552e-363">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e552e-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e552e-364">Dépréciation de l’applet de commande Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e552e-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-365">Az.Sql</span></span>
* <span data-ttu-id="e552e-366">Mise à jour de la documentation des anciennes applets de commande d’audit.</span><span class="sxs-lookup"><span data-stu-id="e552e-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-367">Az.Storage</span></span>
* <span data-ttu-id="e552e-368">Mise à jour de l’aide pour Get/Close-AzStorageFileHandle, en ajoutant d’autres scénarios aux exemples d’applets de commande et mise à jour des descriptions des paramètres</span><span class="sxs-lookup"><span data-stu-id="e552e-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e552e-369">Prise en charge de StandardBlobTier dans le chargement d’objet blob et la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="e552e-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e552e-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e552e-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e552e-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e552e-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e552e-372">Prise en charge de la priorité de réalimentation dans la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="e552e-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e552e-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e552e-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-374">Az.Websites</span></span>
* <span data-ttu-id="e552e-375">Ajout d’une clarification concernant le paramètre -AppSettings dans Set-AzWebApp et Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e552e-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e552e-376">2.5.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-377">Az.Accounts</span></span>
* <span data-ttu-id="e552e-378">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e552e-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e552e-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e552e-380">Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey »</span><span class="sxs-lookup"><span data-stu-id="e552e-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="e552e-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-381">Az.Automation</span></span>
* <span data-ttu-id="e552e-382">Correction d’une faute de frappe dans la chaîne de ressource</span><span class="sxs-lookup"><span data-stu-id="e552e-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="e552e-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e552e-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="e552e-384">Prise en charge de NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="e552e-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-385">Az.Compute</span></span>
* <span data-ttu-id="e552e-386">Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e552e-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e552e-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e552e-388">Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication</span><span class="sxs-lookup"><span data-stu-id="e552e-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e552e-389">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e552e-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-390">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-391">Mise à jour du SDK .NET ADF avec la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e552e-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e552e-392">Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »</span><span class="sxs-lookup"><span data-stu-id="e552e-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e552e-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e552e-393">Az.EventHub</span></span>
* <span data-ttu-id="e552e-394">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e552e-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e552e-395">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="e552e-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e552e-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-396">Az.KeyVault</span></span>
* <span data-ttu-id="e552e-397">Possibilité de spécifier KeySize pour les stratégies de certificat</span><span class="sxs-lookup"><span data-stu-id="e552e-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e552e-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e552e-398">Az.LogicApp</span></span>
* <span data-ttu-id="e552e-399">Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes</span><span class="sxs-lookup"><span data-stu-id="e552e-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e552e-400">Ajout d’un nouveau paramètre MapType pour le filtrage</span><span class="sxs-lookup"><span data-stu-id="e552e-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e552e-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e552e-401">Az.ManagedServices</span></span>
* <span data-ttu-id="e552e-402">Ajout de la prise en charge de l’API version 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="e552e-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-403">Az.Network</span></span>
* <span data-ttu-id="e552e-404">Prise en charge d’un point de terminaison privé et du service de liaison privée</span><span class="sxs-lookup"><span data-stu-id="e552e-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e552e-405">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-405">New cmdlets</span></span>
        - <span data-ttu-id="e552e-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e552e-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e552e-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e552e-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e552e-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e552e-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e552e-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e552e-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e552e-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e552e-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e552e-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e552e-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e552e-414">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e552e-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e552e-415">Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e552e-416">Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="e552e-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e552e-417">Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="e552e-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e552e-418">Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="e552e-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e552e-419">Activation du protocole ICMP pour les configurations des règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="e552e-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e552e-420">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="e552e-420">Updated cmdlets</span></span>
        - <span data-ttu-id="e552e-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e552e-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e552e-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e552e-424">Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e552e-425">Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e552e-426">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="e552e-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="e552e-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e552e-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e552e-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e552e-430">Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde</span><span class="sxs-lookup"><span data-stu-id="e552e-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e552e-431">Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end.</span><span class="sxs-lookup"><span data-stu-id="e552e-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e552e-432">Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="e552e-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="e552e-434">Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="e552e-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="e552e-435">Correction de la gestion des expressions régulières null des journaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="e552e-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-437">Mise à jour de « Get-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e552e-438">Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e552e-439">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e552e-440">Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e552e-441">Mise à jour de « Set-AzRecoveryServicesVaultContext.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e552e-442">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e552e-443">Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e552e-444">Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e552e-445">Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e552e-446">Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »</span><span class="sxs-lookup"><span data-stu-id="e552e-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-447">Az.Resources</span></span>
- <span data-ttu-id="e552e-448">Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="e552e-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e552e-449">Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e552e-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e552e-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e552e-450">Az.ServiceBus</span></span>
* <span data-ttu-id="e552e-451">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e552e-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e552e-452">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="e552e-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-453">Az.Sql</span></span>
* <span data-ttu-id="e552e-454">Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e552e-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e552e-455">Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="e552e-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e552e-456">Correction d’une faute de frappe dans un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="e552e-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-457">Az.Storage</span></span>
* <span data-ttu-id="e552e-458">Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="e552e-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e552e-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e552e-459">Az.StorageSync</span></span>
* <span data-ttu-id="e552e-460">Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="e552e-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e552e-461">Résolution du problème 9551 pour honorer TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="e552e-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-462">Az.Websites</span></span>
* <span data-ttu-id="e552e-463">Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e552e-464">Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e552e-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e552e-465">Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e552e-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e552e-466">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-467">Az.Accounts</span></span>
* <span data-ttu-id="e552e-468">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="e552e-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e552e-469">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="e552e-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e552e-470">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e552e-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e552e-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e552e-471">Az.Advisor</span></span>
* <span data-ttu-id="e552e-472">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e552e-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e552e-473">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="e552e-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e552e-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-474">Az.ApiManagement</span></span>
* <span data-ttu-id="e552e-475">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="e552e-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e552e-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e552e-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e552e-477">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="e552e-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e552e-478">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="e552e-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e552e-479">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="e552e-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e552e-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e552e-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e552e-481">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="e552e-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-482">Az.Automation</span></span>
* <span data-ttu-id="e552e-483">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="e552e-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-484">Az.Compute</span></span>
* <span data-ttu-id="e552e-485">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-486">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-487">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="e552e-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e552e-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e552e-488">Az.EventGrid</span></span>
* <span data-ttu-id="e552e-489">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="e552e-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e552e-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-490">Az.IotHub</span></span>
* <span data-ttu-id="e552e-491">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="e552e-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-492">Az.Network</span></span>
* <span data-ttu-id="e552e-493">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="e552e-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e552e-494">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="e552e-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e552e-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="e552e-496">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e552e-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e552e-497">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e552e-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="e552e-499">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e552e-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-501">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="e552e-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-502">Az.Resources</span></span>
    - <span data-ttu-id="e552e-503">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e552e-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e552e-504">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="e552e-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e552e-505">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="e552e-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e552e-506">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="e552e-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e552e-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e552e-507">Az.ServiceBus</span></span>
* <span data-ttu-id="e552e-508">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e552e-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-509">Az.Sql</span></span>
* <span data-ttu-id="e552e-510">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="e552e-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e552e-511">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="e552e-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e552e-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e552e-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e552e-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e552e-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e552e-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e552e-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e552e-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e552e-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e552e-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e552e-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e552e-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e552e-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e552e-518">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e552e-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-519">Az.Storage</span></span>
* <span data-ttu-id="e552e-520">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="e552e-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e552e-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e552e-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e552e-522">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="e552e-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e552e-523">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="e552e-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e552e-524">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="e552e-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e552e-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e552e-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e552e-527">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="e552e-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e552e-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e552e-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e552e-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e552e-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e552e-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e552e-530">Az.StorageSync</span></span>
* <span data-ttu-id="e552e-531">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="e552e-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e552e-532">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-533">Az.Accounts</span></span>
* <span data-ttu-id="e552e-534">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="e552e-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e552e-535">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e552e-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e552e-536">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="e552e-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e552e-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e552e-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e552e-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e552e-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-539">Az.Compute</span></span>
* <span data-ttu-id="e552e-540">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="e552e-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e552e-541">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="e552e-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e552e-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e552e-542">Az.Dns</span></span>
* <span data-ttu-id="e552e-543">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="e552e-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e552e-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e552e-544">Az.EventGrid</span></span>
* <span data-ttu-id="e552e-545">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e552e-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e552e-546">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="e552e-546">New cmdlets:</span></span>
    - <span data-ttu-id="e552e-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e552e-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e552e-548">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="e552e-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e552e-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e552e-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e552e-550">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="e552e-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e552e-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e552e-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e552e-552">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="e552e-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e552e-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e552e-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e552e-554">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="e552e-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e552e-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e552e-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e552e-556">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="e552e-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e552e-557">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e552e-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e552e-558">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="e552e-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e552e-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e552e-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e552e-560">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="e552e-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="e552e-561">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e552e-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e552e-562">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="e552e-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e552e-563">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="e552e-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="e552e-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e552e-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e552e-565">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="e552e-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e552e-566">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="e552e-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e552e-567">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="e552e-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e552e-568">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="e552e-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e552e-569">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="e552e-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e552e-570">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="e552e-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e552e-571">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="e552e-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e552e-572">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="e552e-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="e552e-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="e552e-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e552e-574">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="e552e-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e552e-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e552e-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e552e-576">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="e552e-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e552e-577">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="e552e-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e552e-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e552e-578">Az.FrontDoor</span></span>
* <span data-ttu-id="e552e-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e552e-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e552e-580">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="e552e-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e552e-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e552e-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e552e-582">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="e552e-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-583">Az.Network</span></span>
* <span data-ttu-id="e552e-584">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="e552e-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e552e-585">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-585">New cmdlets</span></span>
        - <span data-ttu-id="e552e-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e552e-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e552e-587">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e552e-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e552e-588">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-588">New cmdlets</span></span> 
        - <span data-ttu-id="e552e-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e552e-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e552e-590">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e552e-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e552e-591">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-591">New cmdlets</span></span> 
        - <span data-ttu-id="e552e-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e552e-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="e552e-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e552e-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e552e-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e552e-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e552e-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e552e-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e552e-597">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e552e-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e552e-598">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-598">New cmdlets</span></span>
        - <span data-ttu-id="e552e-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e552e-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e552e-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e552e-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e552e-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e552e-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e552e-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e552e-603">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e552e-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e552e-604">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="e552e-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e552e-605">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="e552e-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e552e-606">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e552e-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e552e-607">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e552e-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e552e-608">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e552e-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e552e-609">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e552e-610">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="e552e-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e552e-611">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e552e-612">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="e552e-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e552e-613">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e552e-614">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e552e-615">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e552e-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e552e-616">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e552e-617">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="e552e-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e552e-618">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="e552e-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e552e-619">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="e552e-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e552e-620">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="e552e-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e552e-621">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e552e-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="e552e-622">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="e552e-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="e552e-623">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e552e-624">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e552e-625">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="e552e-627">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="e552e-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-628">Az.Resources</span></span>
* <span data-ttu-id="e552e-629">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="e552e-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e552e-630">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e552e-631">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e552e-632">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="e552e-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e552e-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-634">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-635">Az.Sql</span></span>
* <span data-ttu-id="e552e-636">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e552e-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e552e-637">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="e552e-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e552e-638">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="e552e-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e552e-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e552e-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e552e-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e552e-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e552e-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e552e-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e552e-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e552e-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e552e-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e552e-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-644">Az.Storage</span></span>
* <span data-ttu-id="e552e-645">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="e552e-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e552e-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="e552e-647">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="e552e-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e552e-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-649">Az.Websites</span></span>
* <span data-ttu-id="e552e-650">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="e552e-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e552e-651">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e552e-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e552e-652">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e552e-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e552e-653">Az.Cdn</span></span>
* <span data-ttu-id="e552e-654">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="e552e-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-655">Az.Compute</span></span>
* <span data-ttu-id="e552e-656">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e552e-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e552e-657">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e552e-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e552e-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e552e-658">Az.EventHub</span></span>
* <span data-ttu-id="e552e-659">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="e552e-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e552e-660">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e552e-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-661">Az.Network</span></span>
* <span data-ttu-id="e552e-662">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="e552e-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e552e-663">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="e552e-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e552e-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="e552e-665">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e552e-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-667">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="e552e-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e552e-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e552e-668">Az.ServiceBus</span></span>
* <span data-ttu-id="e552e-669">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e552e-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e552e-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-671">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="e552e-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e552e-672">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e552e-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-673">Az.Sql</span></span>
* <span data-ttu-id="e552e-674">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="e552e-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e552e-675">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e552e-676">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="e552e-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e552e-677">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="e552e-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-678">Az.Websites</span></span>
* <span data-ttu-id="e552e-679">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="e552e-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e552e-680">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e552e-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-681">Az.ApiManagement</span></span>
* <span data-ttu-id="e552e-682">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e552e-683">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e552e-684">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e552e-685">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="e552e-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e552e-686">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e552e-687">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="e552e-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e552e-688">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e552e-689">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e552e-690">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="e552e-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e552e-691">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="e552e-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e552e-692">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="e552e-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e552e-693">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="e552e-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e552e-694">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="e552e-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e552e-695">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="e552e-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e552e-696">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="e552e-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e552e-697">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e552e-698">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e552e-699">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="e552e-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e552e-700">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e552e-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e552e-701">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="e552e-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e552e-702">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="e552e-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e552e-703">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="e552e-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e552e-704">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="e552e-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e552e-705">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="e552e-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e552e-706">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="e552e-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e552e-707">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="e552e-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e552e-708">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="e552e-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e552e-709">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="e552e-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e552e-710">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="e552e-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e552e-711">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="e552e-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e552e-712">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="e552e-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e552e-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e552e-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e552e-714">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="e552e-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e552e-715">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e552e-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e552e-716">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="e552e-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e552e-717">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="e552e-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e552e-718">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="e552e-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e552e-719">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="e552e-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e552e-720">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="e552e-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e552e-721">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e552e-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e552e-722">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="e552e-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e552e-723">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="e552e-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e552e-724">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="e552e-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e552e-725">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="e552e-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e552e-726">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e552e-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e552e-727">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="e552e-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e552e-728">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="e552e-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e552e-729">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="e552e-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e552e-730">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="e552e-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e552e-731">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="e552e-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e552e-732">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="e552e-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e552e-733">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="e552e-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e552e-734">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="e552e-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e552e-735">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e552e-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e552e-736">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="e552e-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e552e-737">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="e552e-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e552e-738">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e552e-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e552e-739">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="e552e-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e552e-740">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="e552e-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e552e-741">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="e552e-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e552e-742">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e552e-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e552e-743">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="e552e-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e552e-744">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="e552e-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e552e-745">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="e552e-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e552e-746">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="e552e-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e552e-747">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="e552e-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e552e-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e552e-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e552e-749">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="e552e-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e552e-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e552e-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e552e-751">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="e552e-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e552e-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e552e-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e552e-753">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="e552e-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e552e-754">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="e552e-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e552e-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e552e-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e552e-756">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="e552e-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e552e-757">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="e552e-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e552e-758">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="e552e-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-759">Az.Automation</span></span>
* <span data-ttu-id="e552e-760">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="e552e-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e552e-761">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e552e-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e552e-762">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e552e-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e552e-763">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="e552e-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e552e-764">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e552e-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e552e-765">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="e552e-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e552e-766">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="e552e-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-767">Az.Compute</span></span>
* <span data-ttu-id="e552e-768">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="e552e-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e552e-769">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e552e-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-771">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e552e-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-772">Az.Monitor</span></span>
* <span data-ttu-id="e552e-773">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="e552e-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-774">Az.Network</span></span>
* <span data-ttu-id="e552e-775">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="e552e-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e552e-776">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="e552e-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="e552e-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e552e-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e552e-778">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e552e-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-779">Az.Resources</span></span>
* <span data-ttu-id="e552e-780">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="e552e-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-781">Az.Sql</span></span>
* <span data-ttu-id="e552e-782">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="e552e-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e552e-783">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-784">Az.Accounts</span></span>
* <span data-ttu-id="e552e-785">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="e552e-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e552e-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e552e-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="e552e-787">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="e552e-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e552e-788">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="e552e-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-789">Az.Compute</span></span>
* <span data-ttu-id="e552e-790">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="e552e-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e552e-791">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e552e-792">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e552e-793">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="e552e-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e552e-794">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="e552e-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e552e-795">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e552e-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e552e-796">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="e552e-796">Breaking changes</span></span>
    - <span data-ttu-id="e552e-797">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e552e-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e552e-798">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="e552e-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e552e-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e552e-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="e552e-800">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="e552e-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e552e-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e552e-801">Az.Dns</span></span>
* <span data-ttu-id="e552e-802">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="e552e-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e552e-803">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="e552e-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e552e-804">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="e552e-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e552e-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e552e-805">Az.FrontDoor</span></span>
* <span data-ttu-id="e552e-806">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e552e-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e552e-807">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="e552e-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e552e-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e552e-808">Az.HDInsight</span></span>
* <span data-ttu-id="e552e-809">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="e552e-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e552e-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e552e-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e552e-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e552e-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e552e-812">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e552e-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e552e-813">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="e552e-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e552e-814">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e552e-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e552e-815">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="e552e-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e552e-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-816">Az.Monitor</span></span>
* <span data-ttu-id="e552e-817">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="e552e-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e552e-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e552e-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e552e-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e552e-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e552e-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e552e-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e552e-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e552e-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e552e-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e552e-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e552e-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e552e-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e552e-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e552e-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e552e-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e552e-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e552e-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e552e-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e552e-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e552e-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e552e-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e552e-829">[Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="e552e-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e552e-830">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="e552e-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-831">Az.Network</span></span>
* <span data-ttu-id="e552e-832">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="e552e-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e552e-833">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-833">New cmdlets</span></span>
        - <span data-ttu-id="e552e-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="e552e-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e552e-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e552e-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e552e-838">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="e552e-838">Updated cmdlets</span></span>
        - <span data-ttu-id="e552e-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e552e-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e552e-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e552e-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e552e-841">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="e552e-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e552e-842">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e552e-843">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="e552e-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e552e-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="e552e-845">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e552e-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e552e-846">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="e552e-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e552e-847">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="e552e-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-849">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="e552e-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e552e-850">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e552e-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e552e-851">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e552e-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e552e-852">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e552e-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e552e-853">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="e552e-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e552e-854">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="e552e-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e552e-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e552e-855">Az.Relay</span></span>
* <span data-ttu-id="e552e-856">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="e552e-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e552e-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e552e-857">Az.ServiceBus</span></span>
* <span data-ttu-id="e552e-858">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="e552e-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-859">Az.Storage</span></span>
* <span data-ttu-id="e552e-860">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="e552e-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e552e-861">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="e552e-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e552e-862">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="e552e-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e552e-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="e552e-864">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="e552e-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e552e-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e552e-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e552e-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-868">Az.Websites</span></span>
* <span data-ttu-id="e552e-869">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e552e-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e552e-870">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="e552e-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e552e-871">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e552e-872">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="e552e-872">Highlights since the last major release</span></span>
* <span data-ttu-id="e552e-873">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="e552e-873">General availability of `Az` module</span></span>
* <span data-ttu-id="e552e-874">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e552e-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e552e-875">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e552e-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e552e-876">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e552e-877">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="e552e-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e552e-878">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e552e-879">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="e552e-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e552e-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-880">Az.Accounts</span></span>
* <span data-ttu-id="e552e-881">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="e552e-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e552e-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e552e-882">Az.Batch</span></span>
* <span data-ttu-id="e552e-883">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e552e-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e552e-884">Az.Cdn</span></span>
* <span data-ttu-id="e552e-885">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e552e-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e552e-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="e552e-887">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-888">Az.Compute</span></span>
* <span data-ttu-id="e552e-889">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="e552e-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e552e-890">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e552e-891">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="e552e-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-892">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-893">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="e552e-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-895">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e552e-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e552e-896">Az.EventGrid</span></span>
* <span data-ttu-id="e552e-897">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="e552e-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e552e-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e552e-898">Az.EventHub</span></span>
* <span data-ttu-id="e552e-899">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="e552e-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e552e-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e552e-900">Az.HDInsight</span></span>
* <span data-ttu-id="e552e-901">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e552e-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-902">Az.IotHub</span></span>
* <span data-ttu-id="e552e-903">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e552e-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-904">Az.KeyVault</span></span>
* <span data-ttu-id="e552e-905">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e552e-906">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="e552e-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e552e-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e552e-907">Az.MachineLearning</span></span>
* <span data-ttu-id="e552e-908">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e552e-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e552e-909">Az.Media</span></span>
* <span data-ttu-id="e552e-910">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e552e-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-911">Az.Monitor</span></span>
  * <span data-ttu-id="e552e-912">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="e552e-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e552e-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e552e-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e552e-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e552e-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e552e-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e552e-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e552e-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e552e-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e552e-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e552e-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e552e-918">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e552e-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-919">Az.Network</span></span>
* <span data-ttu-id="e552e-920">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e552e-921">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="e552e-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e552e-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e552e-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="e552e-923">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="e552e-925">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e552e-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e552e-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e552e-927">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-929">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e552e-930">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="e552e-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e552e-931">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e552e-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e552e-932">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="e552e-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e552e-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e552e-933">Az.RedisCache</span></span>
* <span data-ttu-id="e552e-934">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-935">Az.Resources</span></span>
* <span data-ttu-id="e552e-936">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="e552e-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-937">Az.Sql</span></span>
* <span data-ttu-id="e552e-938">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="e552e-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e552e-939">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e552e-940">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="e552e-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e552e-941">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="e552e-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e552e-942">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="e552e-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e552e-943">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="e552e-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e552e-944">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="e552e-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-945">Az.Websites</span></span>
* <span data-ttu-id="e552e-946">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="e552e-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e552e-947">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="e552e-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e552e-948">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="e552e-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e552e-949">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e552e-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e552e-950">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e552e-951">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="e552e-951">Highlights since the last major release</span></span>
* <span data-ttu-id="e552e-952">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="e552e-952">General availability of `Az` module</span></span>
* <span data-ttu-id="e552e-953">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e552e-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e552e-954">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e552e-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e552e-955">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e552e-956">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="e552e-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e552e-957">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e552e-958">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="e552e-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e552e-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-959">Az.Accounts</span></span>
* <span data-ttu-id="e552e-960">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e552e-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e552e-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e552e-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="e552e-962">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="e552e-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e552e-963">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="e552e-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-964">Az.Automation</span></span>
* <span data-ttu-id="e552e-965">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="e552e-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e552e-966">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="e552e-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e552e-967">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-968">Az.Compute</span></span>
* <span data-ttu-id="e552e-969">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e552e-970">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="e552e-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e552e-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="e552e-972">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="e552e-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-973">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-974">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e552e-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e552e-975">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e552e-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-976">Az.Resources</span></span>
* <span data-ttu-id="e552e-977">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="e552e-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e552e-978">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e552e-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e552e-979">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e552e-980">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e552e-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e552e-981">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="e552e-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e552e-982">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e552e-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-983">Az.Sql</span></span>
* <span data-ttu-id="e552e-984">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="e552e-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-985">Az.Storage</span></span>
* <span data-ttu-id="e552e-986">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="e552e-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e552e-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e552e-987">New-AzStorageContext</span></span>
* <span data-ttu-id="e552e-988">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="e552e-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e552e-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e552e-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e552e-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e552e-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e552e-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e552e-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e552e-993">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="e552e-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e552e-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e552e-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e552e-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e552e-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e552e-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e552e-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e552e-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e552e-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e552e-998">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e552e-999">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="e552e-999">Highlights since the last major release</span></span>
* <span data-ttu-id="e552e-1000">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="e552e-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="e552e-1001">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e552e-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e552e-1002">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e552e-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e552e-1003">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e552e-1004">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="e552e-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e552e-1005">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e552e-1006">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="e552e-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1007">Az.Automation</span></span>
* <span data-ttu-id="e552e-1008">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="e552e-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e552e-1009">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="e552e-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="e552e-1010">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="e552e-1010">Pre-Post script</span></span>
    * <span data-ttu-id="e552e-1011">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="e552e-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1012">Az.Compute</span></span>
* <span data-ttu-id="e552e-1013">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e552e-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e552e-1014">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e552e-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e552e-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-1015">Az.KeyVault</span></span>
* <span data-ttu-id="e552e-1016">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1017">Az.Network</span></span>
* <span data-ttu-id="e552e-1018">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e552e-1019">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="e552e-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-1021">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="e552e-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e552e-1022">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="e552e-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1023">Az.Resources</span></span>
* <span data-ttu-id="e552e-1024">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e552e-1025">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="e552e-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1026">Az.Sql</span></span>
* <span data-ttu-id="e552e-1027">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="e552e-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1028">Az.Storage</span></span>
* <span data-ttu-id="e552e-1029">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="e552e-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e552e-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e552e-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e552e-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e552e-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e552e-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e552e-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e552e-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e552e-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e552e-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1036">Az.Websites</span></span>
* <span data-ttu-id="e552e-1037">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="e552e-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e552e-1038">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1039">Az.Accounts</span></span>
* <span data-ttu-id="e552e-1040">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="e552e-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e552e-1041">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1042">Az.Automation</span></span>
* <span data-ttu-id="e552e-1043">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e552e-1044">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="e552e-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e552e-1045">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="e552e-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e552e-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e552e-1046">Az.Cdn</span></span>
* <span data-ttu-id="e552e-1047">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="e552e-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1048">Az.Compute</span></span>
* <span data-ttu-id="e552e-1049">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="e552e-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-1050">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-1051">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e552e-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e552e-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e552e-1052">Az.LogicApp</span></span>
* <span data-ttu-id="e552e-1053">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="e552e-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1054">Az.Network</span></span>
* <span data-ttu-id="e552e-1055">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-1057">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="e552e-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e552e-1058">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="e552e-1058">SDK Update</span></span>
* <span data-ttu-id="e552e-1059">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e552e-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e552e-1060">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e552e-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1061">Az.Resources</span></span>
* <span data-ttu-id="e552e-1062">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="e552e-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e552e-1063">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e552e-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e552e-1064">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e552e-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e552e-1065">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e552e-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e552e-1066">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e552e-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e552e-1067">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e552e-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1068">Az.Sql</span></span>
* <span data-ttu-id="e552e-1069">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="e552e-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e552e-1070">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="e552e-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1071">Az.Storage</span></span>
* <span data-ttu-id="e552e-1072">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e552e-1073">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e552e-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="e552e-1075">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="e552e-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1076">Az.Automation</span></span>
* <span data-ttu-id="e552e-1077">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e552e-1078">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e552e-1079">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e552e-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="e552e-1081">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="e552e-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1082">Az.Compute</span></span>
* <span data-ttu-id="e552e-1083">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="e552e-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e552e-1084">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="e552e-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e552e-1085">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e552e-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e552e-1086">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="e552e-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-1088">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="e552e-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e552e-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e552e-1089">Az.EventHub</span></span>
* <span data-ttu-id="e552e-1090">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="e552e-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e552e-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-1091">Az.KeyVault</span></span>
* <span data-ttu-id="e552e-1092">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e552e-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e552e-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e552e-1093">Az.LogicApp</span></span>
* <span data-ttu-id="e552e-1094">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="e552e-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e552e-1095">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="e552e-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e552e-1096">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="e552e-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e552e-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e552e-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e552e-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e552e-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e552e-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e552e-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e552e-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e552e-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e552e-1101">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="e552e-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e552e-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e552e-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e552e-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e552e-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e552e-1106">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e552e-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e552e-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-1107">Az.Monitor</span></span>
* <span data-ttu-id="e552e-1108">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="e552e-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1109">Az.Network</span></span>
* <span data-ttu-id="e552e-1110">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e552e-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="e552e-1112">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="e552e-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e552e-1113">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="e552e-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e552e-1114">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="e552e-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e552e-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1115">Az.Resources</span></span>
* <span data-ttu-id="e552e-1116">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e552e-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e552e-1117">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e552e-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e552e-1118">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e552e-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e552e-1119">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e552e-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1120">Az.Sql</span></span>
* <span data-ttu-id="e552e-1121">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="e552e-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e552e-1122">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="e552e-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1123">Az.Websites</span></span>
* <span data-ttu-id="e552e-1124">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e552e-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e552e-1125">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1126">Az.Accounts</span></span>
* <span data-ttu-id="e552e-1127">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e552e-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e552e-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="e552e-1129">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="e552e-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1130">Az.Compute</span></span>
* <span data-ttu-id="e552e-1131">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="e552e-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e552e-1132">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e552e-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e552e-1133">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e552e-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="e552e-1135">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="e552e-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1136">Az.Resources</span></span>
* <span data-ttu-id="e552e-1137">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="e552e-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e552e-1138">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e552e-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e552e-1139">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e552e-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e552e-1140">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e552e-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1141">Az.Sql</span></span>
* <span data-ttu-id="e552e-1142">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e552e-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e552e-1143">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="e552e-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e552e-1144">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e552e-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e552e-1145">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1146">Az.Accounts</span></span>
* <span data-ttu-id="e552e-1147">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="e552e-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e552e-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="e552e-1149">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="e552e-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="e552e-1151">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="e552e-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e552e-1152">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1153">Az.Accounts</span></span>
* <span data-ttu-id="e552e-1154">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="e552e-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e552e-1155">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e552e-1156">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e552e-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e552e-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e552e-1157">Az.Aks</span></span>
* <span data-ttu-id="e552e-1158">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e552e-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1159">Az.Automation</span></span>
* <span data-ttu-id="e552e-1160">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="e552e-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e552e-1161">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e552e-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e552e-1162">Az.Cdn</span></span>
* <span data-ttu-id="e552e-1163">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1164">Az.Compute</span></span>
* <span data-ttu-id="e552e-1165">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e552e-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e552e-1166">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e552e-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e552e-1167">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e552e-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e552e-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e552e-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e552e-1169">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e552e-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e552e-1170">Az.DataFactory</span></span>
* <span data-ttu-id="e552e-1171">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e552e-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-1173">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="e552e-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e552e-1174">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e552e-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e552e-1175">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e552e-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-1176">Az.IotHub</span></span>
* <span data-ttu-id="e552e-1177">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e552e-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e552e-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-1178">Az.KeyVault</span></span>
* <span data-ttu-id="e552e-1179">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1180">Az.Network</span></span>
* <span data-ttu-id="e552e-1181">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1182">Az.Resources</span></span>
* <span data-ttu-id="e552e-1183">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="e552e-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e552e-1184">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="e552e-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e552e-1185">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e552e-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e552e-1186">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e552e-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e552e-1187">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e552e-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e552e-1188">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="e552e-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e552e-1189">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e552e-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e552e-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-1191">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e552e-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e552e-1192">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e552e-1192">Fix some error messages.</span></span>
* <span data-ttu-id="e552e-1193">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="e552e-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e552e-1194">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="e552e-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e552e-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e552e-1195">Az.SignalR</span></span>
* <span data-ttu-id="e552e-1196">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1197">Az.Sql</span></span>
* <span data-ttu-id="e552e-1198">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e552e-1199">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="e552e-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e552e-1200">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="e552e-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e552e-1201">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="e552e-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1202">Az.Storage</span></span>
* <span data-ttu-id="e552e-1203">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e552e-1204">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="e552e-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e552e-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e552e-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e552e-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e552e-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e552e-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e552e-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="e552e-1208">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1209">Az.Websites</span></span>
* <span data-ttu-id="e552e-1210">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e552e-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e552e-1211">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="e552e-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e552e-1212">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="e552e-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e552e-1213">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="e552e-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e552e-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1214">Az.Accounts</span></span>
* <span data-ttu-id="e552e-1215">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e552e-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1216">Az.Compute</span></span>
* <span data-ttu-id="e552e-1217">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e552e-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e552e-1218">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="e552e-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e552e-1219">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-1221">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="e552e-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e552e-1222">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="e552e-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e552e-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e552e-1223">Az.EventGrid</span></span>
* <span data-ttu-id="e552e-1224">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e552e-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e552e-1225">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e552e-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e552e-1226">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="e552e-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e552e-1227">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="e552e-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e552e-1228">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="e552e-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e552e-1229">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="e552e-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e552e-1230">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="e552e-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e552e-1231">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="e552e-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e552e-1232">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="e552e-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e552e-1233">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="e552e-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="e552e-1234">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e552e-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e552e-1235">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e552e-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e552e-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-1236">Az.IotHub</span></span>
* <span data-ttu-id="e552e-1237">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="e552e-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e552e-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e552e-1238">Az.LogicApp</span></span>
* <span data-ttu-id="e552e-1239">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="e552e-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1240">Az.Resources</span></span>
* <span data-ttu-id="e552e-1241">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="e552e-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e552e-1242">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e552e-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e552e-1243">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e552e-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e552e-1244">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e552e-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e552e-1245">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="e552e-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e552e-1246">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e552e-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e552e-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e552e-1247">Az.SignalR</span></span>
* <span data-ttu-id="e552e-1248">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1249">Az.Sql</span></span>
* <span data-ttu-id="e552e-1250">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="e552e-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e552e-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1251">Az.Storage</span></span>
* <span data-ttu-id="e552e-1252">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="e552e-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e552e-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e552e-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="e552e-1254">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="e552e-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e552e-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e552e-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1256">Az.Websites</span></span>
* <span data-ttu-id="e552e-1257">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e552e-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e552e-1258">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e552e-1259">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e552e-1260">Généralités</span><span class="sxs-lookup"><span data-stu-id="e552e-1260">General</span></span>

- <span data-ttu-id="e552e-1261">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="e552e-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="e552e-1262">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="e552e-1262">Online help for each module</span></span>
- <span data-ttu-id="e552e-1263">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e552e-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e552e-1264">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="e552e-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e552e-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1265">Az.Accounts</span></span>
- <span data-ttu-id="e552e-1266">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e552e-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="e552e-1267">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="e552e-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e552e-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="e552e-1269">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="e552e-1269">Fixes for #7002</span></span>
- <span data-ttu-id="e552e-1270">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e552e-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e552e-1271">Az.Batch</span></span>
- <span data-ttu-id="e552e-1272">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e552e-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e552e-1273">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="e552e-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e552e-1274">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e552e-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e552e-1275">Az.Billing</span></span>
- <span data-ttu-id="e552e-1276">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e552e-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="e552e-1278">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e552e-1279">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e552e-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e552e-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="e552e-1281">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e552e-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e552e-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e552e-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e552e-1283">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="e552e-1285">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e552e-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e552e-1286">Az.Monitor</span></span>
- <span data-ttu-id="e552e-1287">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e552e-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e552e-1288">Az.KeyVault</span></span>
- <span data-ttu-id="e552e-1289">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="e552e-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e552e-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e552e-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="e552e-1291">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e552e-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e552e-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e552e-1292">Az.Media</span></span>
- <span data-ttu-id="e552e-1293">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e552e-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e552e-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1294">Az.Network</span></span>
<span data-ttu-id="e552e-1295">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e552e-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e552e-1296">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="e552e-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="e552e-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e552e-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e552e-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e552e-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e552e-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e552e-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e552e-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e552e-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e552e-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e552e-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e552e-1305">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e552e-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e552e-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e552e-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e552e-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e552e-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e552e-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e552e-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e552e-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e552e-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e552e-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="e552e-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e552e-1312">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e552e-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e552e-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e552e-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e552e-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e552e-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e552e-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e552e-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e552e-1316">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e552e-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e552e-1317">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e552e-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="e552e-1319">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e552e-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e552e-1320">Az.Profile</span></span>
- <span data-ttu-id="e552e-1321">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e552e-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="e552e-1323">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e552e-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1324">Az.Resources</span></span>
- <span data-ttu-id="e552e-1325">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e552e-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="e552e-1327">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="e552e-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e552e-1328">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e552e-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e552e-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="e552e-1330">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e552e-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e552e-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1331">Az.Sql</span></span>
- <span data-ttu-id="e552e-1332">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="e552e-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e552e-1333">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="e552e-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e552e-1334">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e552e-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1335">Az.Storage</span></span>
- <span data-ttu-id="e552e-1336">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e552e-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1337">Az.Websites</span></span>
- <span data-ttu-id="e552e-1338">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e552e-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e552e-1339">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e552e-1340">Généralités</span><span class="sxs-lookup"><span data-stu-id="e552e-1340">General</span></span>

* <span data-ttu-id="e552e-1341">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="e552e-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e552e-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1342">Az.Compute</span></span>

* <span data-ttu-id="e552e-1343">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="e552e-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="e552e-1345">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="e552e-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e552e-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e552e-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="e552e-1347">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="e552e-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="e552e-1348">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e552e-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e552e-1349">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e552e-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e552e-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="e552e-1351">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="e552e-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e552e-1352">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="e552e-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e552e-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1353">Az.Resources</span></span>

* <span data-ttu-id="e552e-1354">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e552e-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e552e-1355">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="e552e-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e552e-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1356">Az.Sql</span></span>

* <span data-ttu-id="e552e-1357">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="e552e-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e552e-1358">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="e552e-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e552e-1359">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="e552e-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e552e-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1360">Az.Storage</span></span>

* <span data-ttu-id="e552e-1361">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e552e-1362">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="e552e-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e552e-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e552e-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e552e-1364">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="e552e-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="e552e-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e552e-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e552e-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e552e-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e552e-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1367">Az.Websites</span></span>

* <span data-ttu-id="e552e-1368">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e552e-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e552e-1369">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="e552e-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e552e-1370">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="e552e-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e552e-1371">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e552e-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e552e-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="e552e-1373">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e552e-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e552e-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e552e-1374">Az.Automation</span></span>
* <span data-ttu-id="e552e-1375">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="e552e-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e552e-1376">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="e552e-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e552e-1377">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="e552e-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e552e-1378">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="e552e-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e552e-1379">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="e552e-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e552e-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1380">Az.Compute</span></span>
* <span data-ttu-id="e552e-1381">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e552e-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e552e-1382">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e552e-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e552e-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="e552e-1384">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e552e-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e552e-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e552e-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e552e-1386">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="e552e-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e552e-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1387">Az.Network</span></span>
* <span data-ttu-id="e552e-1388">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e552e-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e552e-1389">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="e552e-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e552e-1390">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="e552e-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e552e-1391">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e552e-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e552e-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e552e-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e552e-1393">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="e552e-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e552e-1394">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="e552e-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e552e-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e552e-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e552e-1396">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e552e-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e552e-1397">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e552e-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e552e-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e552e-1398">Az.Relay</span></span>
* <span data-ttu-id="e552e-1399">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e552e-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e552e-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1400">Az.Resources</span></span>
* <span data-ttu-id="e552e-1401">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e552e-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e552e-1402">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="e552e-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e552e-1403">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e552e-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e552e-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-1405">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="e552e-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e552e-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1406">Az.Sql</span></span>
* <span data-ttu-id="e552e-1407">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="e552e-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e552e-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e552e-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e552e-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e552e-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e552e-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e552e-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e552e-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e552e-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e552e-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e552e-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e552e-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e552e-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e552e-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e552e-1416">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="e552e-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e552e-1417">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="e552e-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e552e-1418">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="e552e-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e552e-1419">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e552e-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e552e-1420">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e552e-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e552e-1421">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e552e-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e552e-1422">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e552e-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e552e-1423">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="e552e-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e552e-1424">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e552e-1425">Généralités</span><span class="sxs-lookup"><span data-stu-id="e552e-1425">General</span></span>
* <span data-ttu-id="e552e-1426">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="e552e-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e552e-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e552e-1427">Az.Profile</span></span>
* <span data-ttu-id="e552e-1428">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e552e-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e552e-1429">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="e552e-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e552e-1430">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e552e-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e552e-1431">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="e552e-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e552e-1432">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="e552e-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e552e-1433">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="e552e-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e552e-1434">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="e552e-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e552e-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="e552e-1436">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e552e-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1437">Az.Compute</span></span>
* <span data-ttu-id="e552e-1438">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e552e-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e552e-1439">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e552e-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e552e-1440">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="e552e-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-1442">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e552e-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e552e-1443">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="e552e-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e552e-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e552e-1444">Az.Insights</span></span>
* <span data-ttu-id="e552e-1445">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="e552e-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e552e-1446">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="e552e-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e552e-1447">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="e552e-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e552e-1448">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="e552e-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1449">Az.Network</span></span>
* <span data-ttu-id="e552e-1450">Modification du type de peering en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="e552e-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e552e-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e552e-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e552e-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e552e-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e552e-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e552e-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e552e-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e552e-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e552e-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e552e-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e552e-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e552e-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e552e-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e552e-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="e552e-1458">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="e552e-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1459">Az.Resources</span></span>
* <span data-ttu-id="e552e-1460">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e552e-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e552e-1461">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="e552e-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e552e-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e552e-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="e552e-1463">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="e552e-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e552e-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e552e-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="e552e-1465">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="e552e-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e552e-1466">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="e552e-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e552e-1467">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e552e-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e552e-1468">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e552e-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e552e-1469">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="e552e-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e552e-1470">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e552e-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e552e-1471">Az.Profile</span></span>
* <span data-ttu-id="e552e-1472">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="e552e-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e552e-1473">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e552e-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1474">Az.Compute</span></span>
* <span data-ttu-id="e552e-1475">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="e552e-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e552e-1476">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="e552e-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e552e-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e552e-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="e552e-1478">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="e552e-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e552e-1479">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e552e-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e552e-1480">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="e552e-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e552e-1481">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="e552e-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e552e-1482">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e552e-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1483">Az.Network</span></span>
* <span data-ttu-id="e552e-1484">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="e552e-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e552e-1485">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="e552e-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1486">Az.Resources</span></span>
* <span data-ttu-id="e552e-1487">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="e552e-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e552e-1488">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="e552e-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e552e-1489">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e552e-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e552e-1490">Azure.Storage</span></span>
* <span data-ttu-id="e552e-1491">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="e552e-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e552e-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e552e-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e552e-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e552e-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e552e-1494">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="e552e-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e552e-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e552e-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e552e-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e552e-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="e552e-1497">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="e552e-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e552e-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e552e-1498">Az.Compute</span></span>
* <span data-ttu-id="e552e-1499">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="e552e-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e552e-1500">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e552e-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e552e-1501">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="e552e-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e552e-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e552e-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e552e-1503">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e552e-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e552e-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e552e-1504">Az.Network</span></span>
* <span data-ttu-id="e552e-1505">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="e552e-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e552e-1506">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="e552e-1506">new cmdlets added</span></span>
    - <span data-ttu-id="e552e-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e552e-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e552e-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e552e-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e552e-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e552e-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e552e-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e552e-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e552e-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e552e-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e552e-1513">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="e552e-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e552e-1514">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e552e-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e552e-1515">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e552e-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e552e-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e552e-1516">Az.RedisCache</span></span>
* <span data-ttu-id="e552e-1517">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="e552e-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e552e-1518">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e552e-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e552e-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e552e-1519">Az.Resources</span></span>
* <span data-ttu-id="e552e-1520">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e552e-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e552e-1521">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="e552e-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e552e-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e552e-1522">Az.Sql</span></span>
* <span data-ttu-id="e552e-1523">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="e552e-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e552e-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e552e-1524">Az.Websites</span></span>
* <span data-ttu-id="e552e-1525">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="e552e-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e552e-1526">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="e552e-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e552e-1527">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="e552e-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e552e-1528">Version initiale</span><span class="sxs-lookup"><span data-stu-id="e552e-1528">Initial Release</span></span>
