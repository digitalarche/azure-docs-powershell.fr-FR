---
title: Notes de publication Azure PowerShell
description: Découvrez toutes les dernières mises à jour des modules Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035759"
---
## <a name="280---october-2019"></a><span data-ttu-id="d00f0-103">2.8.0 - octobre 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d00f0-104">Généralités</span><span class="sxs-lookup"><span data-stu-id="d00f0-104">General</span></span>
* <span data-ttu-id="d00f0-105">Az.HealthcareApis 1.0.0 release</span><span class="sxs-lookup"><span data-stu-id="d00f0-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00f0-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-106">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-107">Mise à jour de la télémétrie et réécriture des URL pour les modules générés, correction des tests unitaires Windows.</span><span class="sxs-lookup"><span data-stu-id="d00f0-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00f0-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-108">Az.ApiManagement</span></span>
* <span data-ttu-id="d00f0-109">**Set-AzApiManagementApi** - Ajout de la prise en charge de la mise à jour d’Api dans ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d00f0-110">Corriger le problème https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="d00f0-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-111">Az.Automation</span></span>
* <span data-ttu-id="d00f0-112">Correction de l’applet de commande New-AzureAutomationSoftwareUpdateConfiguration pour le paramètre de définition de redémarrage Linux.</span><span class="sxs-lookup"><span data-stu-id="d00f0-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="d00f0-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00f0-113">Az.Batch</span></span>
* <span data-ttu-id="d00f0-114">**Get-AzBatchNodeAgentSku** est déprécié et va être remplacé par **Get-AzBatchSupportImage** dans la version 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="d00f0-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-115">Az.Compute</span></span>
* <span data-ttu-id="d00f0-116">Ajout des paramètres Priority, EvictionPolicy et MaxPrice aux applets de commande New-AzVM et New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00f0-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d00f0-117">Correction du message d’avertissement et du document d’aide pour les applets de commande Add-AzVMAdditionalUnattendContent et Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d00f0-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d00f0-118">Correction de l’exception Fix-skipVmBackup pour les machines virtuelles Linux avec des disques managés pour Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="d00f0-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="d00f0-119">Correction du bogue dans les paramètres de chiffrement de mise à jour dans Set-AzVMDiskEncryptionExtension, deux scénarios de réussite.</span><span class="sxs-lookup"><span data-stu-id="d00f0-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-120">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-121">Ajout des commandes CRUD pour le flux de données ADF V2 : Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow et Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d00f0-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d00f0-122">Ajout de commandes d’action pour la session de débogage de flux de données ADF V2 : Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand et Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d00f0-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d00f0-123">Mise à jour de la version du SDK .NET ADF vers la version 4.2.0</span><span class="sxs-lookup"><span data-stu-id="d00f0-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-125">Correction de la validation de compte afin que les comptes avec '-' puissent être passés sans domaine</span><span class="sxs-lookup"><span data-stu-id="d00f0-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d00f0-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d00f0-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="d00f0-127">Mise à jour de la version PowerShell vers 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d00f0-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d00f0-128">Mise à jour de la version du SDK vers 1.0.2</span><span class="sxs-lookup"><span data-stu-id="d00f0-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d00f0-129">Mise à jour dans les tests pour faire référence à la nouvelle version du SDK</span><span class="sxs-lookup"><span data-stu-id="d00f0-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d00f0-130">Mise à jour de la structure de sortie qui passe d’un état imbriqué à un état aplati.</span><span class="sxs-lookup"><span data-stu-id="d00f0-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00f0-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-131">Az.IotHub</span></span>
* <span data-ttu-id="d00f0-132">Ajout d’une nouvelle source de routage : DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="d00f0-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d00f0-133">Correctif de bogues mineurs : Get-AzIothub ne retourne pas subscriptionId</span><span class="sxs-lookup"><span data-stu-id="d00f0-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-134">Az.Monitor</span></span>
* <span data-ttu-id="d00f0-135">Nouveaux récepteurs de groupe d’actions ajoutés pour New-AzActionGroupReceiver :   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="d00f0-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d00f0-136">Utiliser le schéma d’alerte commun activé pour les récepteurs.</span><span class="sxs-lookup"><span data-stu-id="d00f0-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d00f0-137">Cela ne s’applique pas aux SMS, au push Azure App, à ITSM et aux systèmes vocaux</span><span class="sxs-lookup"><span data-stu-id="d00f0-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d00f0-138">Les webhooks prennent maintenant en charge l’authentification Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d00f0-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-139">Az.Network</span></span>
* <span data-ttu-id="d00f0-140">Ajout de la nouvelle applet de commande Get-AzAvailableServiceAlias qui peut être appelée pour obtenir des alias pouvant être utilisés pour les stratégies de point de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="d00f0-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d00f0-141">Ajout de la prise en charge des sélecteurs de trafic pour les connexions de passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="d00f0-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d00f0-142">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="d00f0-142">New cmdlets added:</span></span>
        - <span data-ttu-id="d00f0-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d00f0-144">Applets de commande mises à jour avec le paramètre facultatif -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="d00f0-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="d00f0-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="d00f0-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d00f0-147">Ajout de la prise en charge des protocoles ESP et AH dans les configurations de règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="d00f0-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d00f0-148">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="d00f0-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="d00f0-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00f0-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00f0-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d00f0-152">Amélioration de la gestion des exceptions dans les applets de commande cortex</span><span class="sxs-lookup"><span data-stu-id="d00f0-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d00f0-153">Nouvelles générations et références SKU pour VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="d00f0-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d00f0-154">Introduction de nouvelles générations pour VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d00f0-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d00f0-155">Introduction de nouvelles références SKU haut débit pour VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d00f0-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00f0-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00f0-156">Az.RedisCache</span></span>
* <span data-ttu-id="d00f0-157">Mise à jour de la documentation de référence 'Set-AzRedisCache' afin d’inclure les valeurs manquantes pour le paramètre '-Size'</span><span class="sxs-lookup"><span data-stu-id="d00f0-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-158">Az.Sql</span></span>
* <span data-ttu-id="d00f0-159">Ajout de la prise en charge de la définition de l’administrateur Active Directory sur Managed Instance</span><span class="sxs-lookup"><span data-stu-id="d00f0-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-160">Az.Storage</span></span>
* <span data-ttu-id="d00f0-161">Mise à niveau de la bibliothèque de client de stockage vers la version 11.1.0</span><span class="sxs-lookup"><span data-stu-id="d00f0-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d00f0-162">Listing des conteneurs avec l’API de plan de gestion, sera listé avec NextPageLink</span><span class="sxs-lookup"><span data-stu-id="d00f0-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d00f0-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d00f0-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d00f0-164">Listing des comptes de stockage de l’abonnement, sera listé avec NextPageLink</span><span class="sxs-lookup"><span data-stu-id="d00f0-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d00f0-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00f0-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00f0-166">Az.StorageSync</span></span>
* <span data-ttu-id="d00f0-167">Correction du problème 9810 dans Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="d00f0-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-168">Az.Websites</span></span>
* <span data-ttu-id="d00f0-169">Échec de la mise à jour Set-AzWebApp avec l’ASP d’une application</span><span class="sxs-lookup"><span data-stu-id="d00f0-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d00f0-170">2.7.0 - septembre 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d00f0-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-171">Az.ApiManagement</span></span>
* <span data-ttu-id="d00f0-172">Mise à jour de la description du paramètre « -Format » dans la documentation de référence de « Set-AzApiManagementPolicy »</span><span class="sxs-lookup"><span data-stu-id="d00f0-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d00f0-173">Suppression des références de la cmdlet dépréciée « Update-AzApiManagementDeployment » dans la documentation de référence.</span><span class="sxs-lookup"><span data-stu-id="d00f0-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d00f0-174">Utilisation de « Set-AzApiManagement » à la place.</span><span class="sxs-lookup"><span data-stu-id="d00f0-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-175">Az.Automation</span></span>
* <span data-ttu-id="d00f0-176">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Register-AzAutomationDscNode »</span><span class="sxs-lookup"><span data-stu-id="d00f0-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d00f0-177">Ajout d’une précision sur la restriction de système d’exploitation à Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="d00f0-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d00f0-178">Correction de l’exception de référence Null de la comdlet Start-AzAutomationRunbook pour l’option -Wait.</span><span class="sxs-lookup"><span data-stu-id="d00f0-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-179">Az.Compute</span></span>
* <span data-ttu-id="d00f0-180">Ajout du paramètre UploadSizeInBytes à New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d00f0-181">Ajout du paramètre Incremental à New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d00f0-182">Ajouter d’une fonctionnalité de machine virtuelle basse priorité :</span><span class="sxs-lookup"><span data-stu-id="d00f0-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d00f0-183">Les paramètres MaxPrice, EvictionPolicy et Priority sont ajoutés à New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d00f0-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d00f0-184">Le paramètre MaxPrice est ajouté aux cmdlets New-AzVmssConfig, Update-AzVM et Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d00f0-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d00f0-185">Correction du problème de référence de machine virtuelle pour la cmdlet AzAvailabilitySet quand elle liste tous les groupes à haute disponibilité inclus dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="d00f0-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d00f0-186">Correction de l’exception Null pour Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="d00f0-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d00f0-187">Correction de la méthode de recherche de disque dur virtuel pour la position relative de fin.</span><span class="sxs-lookup"><span data-stu-id="d00f0-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d00f0-188">Correction du problème UltraSSD pour New-AzVM et Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d00f0-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-189">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-190">Ajout de 3 nouvelles commandes pour ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription et Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d00f0-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d00f0-191">Mise à jour de la version du SDK .NET ADF vers la version 4.1.3</span><span class="sxs-lookup"><span data-stu-id="d00f0-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00f0-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00f0-192">Az.HDInsight</span></span>
* <span data-ttu-id="d00f0-193">Explication des changements cassants</span><span class="sxs-lookup"><span data-stu-id="d00f0-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00f0-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-194">Az.IotHub</span></span>
* <span data-ttu-id="d00f0-195">Ajout de la prise en charge pour appeler le basculement d’un IotHub vers la région de reprise d’activité géocouplée.</span><span class="sxs-lookup"><span data-stu-id="d00f0-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d00f0-196">Ajout de la prise en charge pour gérer l’enrichissement de message pour un IotHub.</span><span class="sxs-lookup"><span data-stu-id="d00f0-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d00f0-197">Les nouvelles cmdlets sont :</span><span class="sxs-lookup"><span data-stu-id="d00f0-197">New cmdlets are:</span></span>
    - <span data-ttu-id="d00f0-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00f0-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d00f0-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00f0-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d00f0-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00f0-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d00f0-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00f0-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-202">Az.Monitor</span></span>
* <span data-ttu-id="d00f0-203">Pointage vers le dernier SDK Monitor, par exemple, 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="d00f0-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d00f0-204">Ajout de changements non cassants aux cmdlets Metrics, c.-à-d. que l’énumération Unit prend en charge plusieurs nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="d00f0-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d00f0-205">Il s’agit de cmdlets en lecture seule, donc aucune modification n’est apportée à leur entrée.</span><span class="sxs-lookup"><span data-stu-id="d00f0-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d00f0-206">La version d’API des demandes **ActionGroups** est désormais **2019-06-01**, auparavant il s’agissait de la version **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="d00f0-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d00f0-207">Les tests de scénario ont été mis à jour pour tenir compte de cette modification.</span><span class="sxs-lookup"><span data-stu-id="d00f0-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d00f0-208">Les constructeurs des classes **EmailReceiver** et **WebhookReceiver** ont un nouvel argument obligatoire, à savoir une valeur booléenne appelée **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="d00f0-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d00f0-209">Actuellement, la valeur est définie sur **false** pour masquer ce changement cassant par rapport aux cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d00f0-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d00f0-210">**REMARQUE** : Il s’agit d’une modification temporaire qui doit être validée par l’équipe des alertes.</span><span class="sxs-lookup"><span data-stu-id="d00f0-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d00f0-211">L’ordre des arguments pour le constructeur de la classe **Source** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="d00f0-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d00f0-212">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="d00f0-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d00f0-213">L’ordre des arguments pour le constructeur de la classe **AlertingAction** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent.</span><span class="sxs-lookup"><span data-stu-id="d00f0-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d00f0-214">Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.</span><span class="sxs-lookup"><span data-stu-id="d00f0-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d00f0-215">Prise en charge des critères de seuil dynamique pour l’alerte de métrique V2</span><span class="sxs-lookup"><span data-stu-id="d00f0-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d00f0-216">New-AzMetricAlertRuleV2Criteria : création de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="d00f0-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d00f0-217">Add-AzMetricAlertRuleV2 : acceptation de critères de seuil dynamique également</span><span class="sxs-lookup"><span data-stu-id="d00f0-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d00f0-218">Améliorations apportées aux cmdlets de règle de requête planifiée</span><span class="sxs-lookup"><span data-stu-id="d00f0-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d00f0-219">Les cmdlets acceptent le paramètre « location » dans les deux formats, à savoir l’emplacement (par exemple, usa-est) ou le nom d’affichage de l’emplacement (par exemple, USA Est)</span><span class="sxs-lookup"><span data-stu-id="d00f0-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d00f0-220">Illustration correcte du paramètre « Enabled » dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="d00f0-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d00f0-221">Ajout d’exemples pour le paramètre facultatif « ActionGroup »</span><span class="sxs-lookup"><span data-stu-id="d00f0-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d00f0-222">Amélioration globale des fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="d00f0-222">Overall improved help files</span></span>
* <span data-ttu-id="d00f0-223">Correction du bogue lié à la détermination du type d’étendue pour « Set-AzActionRule »</span><span class="sxs-lookup"><span data-stu-id="d00f0-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-224">Az.Network</span></span>
* <span data-ttu-id="d00f0-225">Correction de l’exemple incorrect dans la documentation de référence de « New-AzApplicationGateway »</span><span class="sxs-lookup"><span data-stu-id="d00f0-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="d00f0-226">Ajout d’une remarque à la documentation de référence de « Get-AzNetworkWatcherPacketCapturee » à propos de la récupération de toutes les propriétés d’une capture de paquets</span><span class="sxs-lookup"><span data-stu-id="d00f0-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d00f0-227">Correction de l’exemple dans la documentation de référence de « Test-AzNetworkWatcherIPFlow » pour énumérer correctement les cartes réseau</span><span class="sxs-lookup"><span data-stu-id="d00f0-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d00f0-228">Amélioration de l’analyse des exceptions cloud pour afficher des détails supplémentaires s’ils existent</span><span class="sxs-lookup"><span data-stu-id="d00f0-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d00f0-229">Amélioration de l’analyse des exceptions cloud pour gérer un type supplémentaire d’exception de SDK</span><span class="sxs-lookup"><span data-stu-id="d00f0-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d00f0-230">Correction du mappage incorrect des modèles de règle de sécurité</span><span class="sxs-lookup"><span data-stu-id="d00f0-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d00f0-231">Ajout de propriétés à une interface réseau pour la fonctionnalité d’adresse IP privée</span><span class="sxs-lookup"><span data-stu-id="d00f0-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d00f0-232">Ajout de la propriété « PrivateEndpoint » comme type de PSResourceId à PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d00f0-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d00f0-233">Ajout de la propriété « PrivateLinkConnectionProperties » comme type de PSIpConfigurationConnectivityInformation à PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d00f0-234">Ajout d’une nouvelle classe de modèle PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="d00f0-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d00f0-235">Ajout de « MSSQL » ApplicationRuleProtocolType pour la ressource du Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d00f0-236">Prise en charge de liaisons multiples dans Azure Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="d00f0-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d00f0-237">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-237">New cmdlets</span></span>
        - <span data-ttu-id="d00f0-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d00f0-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d00f0-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d00f0-240">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="d00f0-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00f0-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d00f0-241">New-VpnSite</span></span>
        - <span data-ttu-id="d00f0-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d00f0-242">Update-VpnSite</span></span>
        - <span data-ttu-id="d00f0-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-243">New-VpnConnection</span></span>
        - <span data-ttu-id="d00f0-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-244">Update-VpnConnection</span></span>
* <span data-ttu-id="d00f0-245">Correction des documents de certains exemples PowerShell pour utiliser des cmdlets Az à la place de cmdlets AzureRM</span><span class="sxs-lookup"><span data-stu-id="d00f0-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-247">Mise à jour de l’objet AzureVMpolicy avec l’attribut ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="d00f0-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d00f0-248">Ajout de tests pour la stratégie de machine virtuelle et la restauration du compte de stockage d’origine</span><span class="sxs-lookup"><span data-stu-id="d00f0-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-249">Az.Resources</span></span>
* <span data-ttu-id="d00f0-250">Correction du bogue qui empêchait l’appel de New-AzRoleAssignment sans paramètre d’étendue.</span><span class="sxs-lookup"><span data-stu-id="d00f0-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00f0-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-252">Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="d00f0-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d00f0-253">Ajout de nouvelles cmdlets pour gérer les applications et les services :</span><span class="sxs-lookup"><span data-stu-id="d00f0-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d00f0-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00f0-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00f0-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d00f0-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d00f0-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d00f0-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d00f0-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d00f0-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d00f0-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00f0-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00f0-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00f0-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00f0-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d00f0-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d00f0-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d00f0-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d00f0-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d00f0-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d00f0-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00f0-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00f0-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d00f0-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d00f0-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d00f0-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d00f0-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="d00f0-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d00f0-267">Mise à niveau du SDK Service Fabric vers la version 1.2.0 qui utilise la version d’API du fournisseur de ressources Service Fabric 2019-03-01.</span><span class="sxs-lookup"><span data-stu-id="d00f0-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00f0-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00f0-268">Az.SignalR</span></span>
* <span data-ttu-id="d00f0-269">Ajout de cmdlets Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="d00f0-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-270">Az.Sql</span></span>
* <span data-ttu-id="d00f0-271">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzSqlElasticPool »</span><span class="sxs-lookup"><span data-stu-id="d00f0-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d00f0-272">Ajout d’un exemple vCore à la création d’un pool élastique (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d00f0-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d00f0-273">Suppression de la validation de EmailAddresses et de la vérification que EmailAdmins n’a pas la valeur false quand EmailAddresses est vide dans Set-AzSqlServerAdvancedThreatProtectionPolicy et Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d00f0-274">Activation de la suppression des paramètres d’audit du serveur/de la base de données quand il existe plusieurs paramètres de diagnostic qui activent la catégorie d’audit.</span><span class="sxs-lookup"><span data-stu-id="d00f0-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d00f0-275">Correction de la validation des adresses e-mail dans plusieurs cmdlets d’évaluation des vulnérabilités SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting et Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d00f0-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-276">Az.Storage</span></span>
* <span data-ttu-id="d00f0-277">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzStorageAccountKey »</span><span class="sxs-lookup"><span data-stu-id="d00f0-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d00f0-278">Lors d’un chargement/téléchargement de fichier Azure, prise en charge de la conservation des propriétés SMB des fichiers sources (attributs du fichier, heure de création du fichier, heure de la dernière écriture du fichier) dans le fichier de destination</span><span class="sxs-lookup"><span data-stu-id="d00f0-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d00f0-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d00f0-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d00f0-281">Correction de l’échec de chargement de l’objet blob de blocs avec des propriétés/métadonnées sur ImmutabilityPolicy avec conteneur activé.</span><span class="sxs-lookup"><span data-stu-id="d00f0-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d00f0-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d00f0-283">Prise en charge de la gestion des partages de fichiers Azure avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="d00f0-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d00f0-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00f0-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d00f0-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00f0-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d00f0-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00f0-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d00f0-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00f0-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-288">Az.Websites</span></span>
* <span data-ttu-id="d00f0-289">Résolution du problème de suppression des balises webapp lors de la migration de l’application vers un nouvel ASP</span><span class="sxs-lookup"><span data-stu-id="d00f0-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d00f0-290">Correction de Publish-AzureWebapp pour un fonctionnement sur Linux et Windows</span><span class="sxs-lookup"><span data-stu-id="d00f0-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d00f0-291">Mise à jour de l’exemple dans la documentation de référence pour « Get-AzWebAppPublishingProfile »</span><span class="sxs-lookup"><span data-stu-id="d00f0-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d00f0-292">2.6.0 - Août 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d00f0-293">Généralités</span><span class="sxs-lookup"><span data-stu-id="d00f0-293">General</span></span>
* <span data-ttu-id="d00f0-294">Correction des fautes de frappe diverses dans de nombreux modules</span><span class="sxs-lookup"><span data-stu-id="d00f0-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00f0-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-295">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-296">Prise en charge de l’identité MSI affectée à l’utilisateur dans l’authentification Azure Functions (n° 9479)</span><span class="sxs-lookup"><span data-stu-id="d00f0-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00f0-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00f0-297">Az.Aks</span></span>
* <span data-ttu-id="d00f0-298">Résolution du problème relatif à la sortie de « Get-AzAks »</span><span class="sxs-lookup"><span data-stu-id="d00f0-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d00f0-299">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="d00f0-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00f0-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-300">Az.ApiManagement</span></span>
* <span data-ttu-id="d00f0-301">Corriger le problème https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="d00f0-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d00f0-302">Mise à jour de la version de .Net NuGet, qui n’applique pas de restrictions sur productId, apiId, groupId et userId</span><span class="sxs-lookup"><span data-stu-id="d00f0-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d00f0-303">**Get-AzApiManagementProduct** : ajout de la prise en charge de l’interrogation de produits à l’aide d’une API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d00f0-304">**New-AzApiManagementApiRevision** : résolution du problème où ApiRevisionDescription n’était pas défini lors de la création d’une révision d’API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="d00f0-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d00f0-305">Correction d’une faute de frappe dans le modèle « PsApiManagementOAuth2AuthrozationServer » remplacé par « PsApiManagementOAuth2AuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="d00f0-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00f0-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00f0-306">Az.Batch</span></span>
* <span data-ttu-id="d00f0-307">Correction d’une faute de frappe dans un message d’aide et la documentation pour mettre Windows en majuscules</span><span class="sxs-lookup"><span data-stu-id="d00f0-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00f0-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00f0-308">Az.Cdn</span></span>
* <span data-ttu-id="d00f0-309">Correction d’une faute de frappe dans l’application d’assistance du module CDN</span><span class="sxs-lookup"><span data-stu-id="d00f0-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-310">Az.Compute</span></span>
* <span data-ttu-id="d00f0-311">Ajout de VmssId à l’applet de commande New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d00f0-312">Ajout des paramètres TerminateScheduledEvents et TerminateScheduledEventNotBeforeTimeoutInMinutes à New-AzVmssConfig et Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00f0-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d00f0-313">Ajout de la propriété HyperVGeneration à l’objet image de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="d00f0-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d00f0-314">Ajout des fonctionnalités Host et HostGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d00f0-315">Nouvelles applets de commande :   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d00f0-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d00f0-316">Le paramètre HostId est ajouté à New-AzVMConfig et New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00f0-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d00f0-317">Mise à jour de l’exemple dans la documentation « Invoke-AzVMRunCommand » de manière utiliser le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="d00f0-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d00f0-318">Mise à jour de la description « -VolumeType » dans la documentation de référence de « Set-AzVMDiskEncryptionExtension » et de « Set-AzVmssDiskEncryptionExtension »</span><span class="sxs-lookup"><span data-stu-id="d00f0-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-319">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-320">Correction de la faute de frappe pour mettre « Windows » en majuscules dans la documentation de « New-AzDataFactoryEncryptValue »</span><span class="sxs-lookup"><span data-stu-id="d00f0-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d00f0-321">Mise à jour de la version du SDK .NET ADF vers la version 4.1.2</span><span class="sxs-lookup"><span data-stu-id="d00f0-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d00f0-322">Ajout des paramètres « DataProxyIntegrationRuntimeName », « DataProxyStagingLinkedServiceName » et « DataProxyStagingPath » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin de permettre la configuration du runtime d’intégration auto-hébergé comme proxy pour SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="d00f0-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d00f0-323">Mise à jour de PSTriggerRun pour afficher les pipelines déclenchés, le message et les propriétés, et de PSActivityRun pour afficher le type d’activité</span><span class="sxs-lookup"><span data-stu-id="d00f0-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-325">Correction de la suspension de Get-DataLakeStoreDeletedItem pour toutes les erreurs ou exceptions à distance.</span><span class="sxs-lookup"><span data-stu-id="d00f0-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00f0-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-326">Az.EventHub</span></span>
* <span data-ttu-id="d00f0-327">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNteworkRule dans Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d00f0-328">Résolution du problème n° 9558 : Set-AzEventHubNamespace utilise PATCH au lieu de PUT</span><span class="sxs-lookup"><span data-stu-id="d00f0-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d00f0-329">Ajout du paramètre EnableKafka à l’applet de commande Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d00f0-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d00f0-330">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="d00f0-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d00f0-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d00f0-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d00f0-332">Résolution de la faute de frappe où « Azure » était tout en minuscules dans la documentation</span><span class="sxs-lookup"><span data-stu-id="d00f0-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-333">Az.Monitor</span></span>
* <span data-ttu-id="d00f0-334">Correction du nom de paramètre incorrect dans la documentation</span><span class="sxs-lookup"><span data-stu-id="d00f0-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-335">Az.Network</span></span>
* <span data-ttu-id="d00f0-336">Mise à jour dans New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d00f0-337">Dépréciation du paramètre « PublicIpAddress », car il n’est jamais utilisé côté serveur.</span><span class="sxs-lookup"><span data-stu-id="d00f0-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d00f0-338">Ajout d’un paramètre facultatif « Primary » qui indique si la configuration IP actuelle est primaire ou non.</span><span class="sxs-lookup"><span data-stu-id="d00f0-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d00f0-339">Amélioration de la gestion de l’exception d’erreur de demande à partir du SDK : résolution du problème où les exceptions du SDK n’étaient précédemment pas gérées correctement, ce qui empêchait l’affichage des détails des erreurs de clé</span><span class="sxs-lookup"><span data-stu-id="d00f0-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d00f0-340">Ajustement de la logique de validation pour le préfixe IP IPv6 afin de rechercher la longueur de préfixe IPv6 appropriée.</span><span class="sxs-lookup"><span data-stu-id="d00f0-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="d00f0-341">Mise à jour de Get-AzVirtualNetworkSubnetConfig : Ajout d’un paramètre défini pour obtenir l’ID de ressource de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="d00f0-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d00f0-342">Mise à jour de la description du paramètre Location pour AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d00f0-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00f0-344">Mise à jour de la documentation pour « New-AzOperationalInsightsLinuxSyslogDataSource »</span><span class="sxs-lookup"><span data-stu-id="d00f0-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d00f0-345">Ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="d00f0-345">Added example</span></span>
    - <span data-ttu-id="d00f0-346">Mise à jour de la description du paramètre « -Name »</span><span class="sxs-lookup"><span data-stu-id="d00f0-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d00f0-347">Ajout d’un exemple pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d00f0-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d00f0-348">Changement de la description du paramètre -Name pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d00f0-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-350">Mise à jour de « Get-AzRecoveryServicesBackupJobDetail.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-351">Az.Resources</span></span>
* <span data-ttu-id="d00f0-352">Ajout de la prise en charge de la nouvelle API version 2019-05-10 pour Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="d00f0-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d00f0-353">Ajout de la prise en charge de « copy.count = 0 » pour les variables, les ressources et les propriétés</span><span class="sxs-lookup"><span data-stu-id="d00f0-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d00f0-354">Les ressources avec « condition = false » ou « copy.count = 0 » seront supprimées en mode Complet</span><span class="sxs-lookup"><span data-stu-id="d00f0-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d00f0-355">Ajout d’un exemple d’affectation de stratégie au niveau de l’abonnement à la documentation d’aide</span><span class="sxs-lookup"><span data-stu-id="d00f0-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00f0-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00f0-356">Az.ServiceBus</span></span>
* <span data-ttu-id="d00f0-357">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNetworkRule dans Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d00f0-358">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="d00f0-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d00f0-359">Ajout de la nouvelle commande « Test-AzServiceBusNameAvailability » afin de vérifier la disponibilité du nom pour la file d’attente et la rubrique</span><span class="sxs-lookup"><span data-stu-id="d00f0-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="d00f0-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-361">Correction des bogues relatifs à l’applet de commande add node type :</span><span class="sxs-lookup"><span data-stu-id="d00f0-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d00f0-362">bogue NullReferenceException quand un groupe de ressources avait d’autres groupes de machines virtuelles identiques non liés au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d00f0-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d00f0-363">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="d00f0-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d00f0-364">Correction du bogue où l’applet de commande échouait si virtualNetwork se trouvait dans un groupe de ressources différent de celui du cluster.</span><span class="sxs-lookup"><span data-stu-id="d00f0-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d00f0-365">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="d00f0-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d00f0-366">Dépréciation de l’applet de commande Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f0-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-367">Az.Sql</span></span>
* <span data-ttu-id="d00f0-368">Mise à jour de la documentation des anciennes applets de commande d’audit.</span><span class="sxs-lookup"><span data-stu-id="d00f0-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-369">Az.Storage</span></span>
* <span data-ttu-id="d00f0-370">Mise à jour de l’aide pour Get/Close-AzStorageFileHandle, en ajoutant d’autres scénarios aux exemples d’applets de commande et mise à jour des descriptions des paramètres</span><span class="sxs-lookup"><span data-stu-id="d00f0-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d00f0-371">Prise en charge de StandardBlobTier dans le chargement d’objet blob et la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="d00f0-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d00f0-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d00f0-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00f0-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d00f0-374">Prise en charge de la priorité de réalimentation dans la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="d00f0-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d00f0-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00f0-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-376">Az.Websites</span></span>
* <span data-ttu-id="d00f0-377">Ajout d’une clarification concernant le paramètre -AppSettings dans Set-AzWebApp et Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d00f0-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d00f0-378">2.5.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-379">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-380">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00f0-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d00f0-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d00f0-382">Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey »</span><span class="sxs-lookup"><span data-stu-id="d00f0-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="d00f0-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-383">Az.Automation</span></span>
* <span data-ttu-id="d00f0-384">Correction d’une faute de frappe dans la chaîne de ressource</span><span class="sxs-lookup"><span data-stu-id="d00f0-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00f0-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00f0-386">Prise en charge de NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="d00f0-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-387">Az.Compute</span></span>
* <span data-ttu-id="d00f0-388">Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d00f0-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d00f0-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d00f0-390">Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication</span><span class="sxs-lookup"><span data-stu-id="d00f0-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d00f0-391">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="d00f0-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-392">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-393">Mise à jour du SDK .NET ADF avec la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d00f0-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d00f0-394">Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »</span><span class="sxs-lookup"><span data-stu-id="d00f0-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00f0-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-395">Az.EventHub</span></span>
* <span data-ttu-id="d00f0-396">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d00f0-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d00f0-397">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="d00f0-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00f0-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-398">Az.KeyVault</span></span>
* <span data-ttu-id="d00f0-399">Possibilité de spécifier KeySize pour les stratégies de certificat</span><span class="sxs-lookup"><span data-stu-id="d00f0-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00f0-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-400">Az.LogicApp</span></span>
* <span data-ttu-id="d00f0-401">Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes</span><span class="sxs-lookup"><span data-stu-id="d00f0-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d00f0-402">Ajout d’un nouveau paramètre MapType pour le filtrage</span><span class="sxs-lookup"><span data-stu-id="d00f0-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d00f0-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-403">Az.ManagedServices</span></span>
* <span data-ttu-id="d00f0-404">Ajout de la prise en charge de l’API version 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="d00f0-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-405">Az.Network</span></span>
* <span data-ttu-id="d00f0-406">Prise en charge d’un point de terminaison privé et du service de liaison privée</span><span class="sxs-lookup"><span data-stu-id="d00f0-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d00f0-407">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-407">New cmdlets</span></span>
        - <span data-ttu-id="d00f0-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00f0-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00f0-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00f0-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00f0-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00f0-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00f0-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00f0-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00f0-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d00f0-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d00f0-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00f0-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d00f0-416">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d00f0-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d00f0-417">Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d00f0-418">Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="d00f0-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d00f0-419">Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="d00f0-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d00f0-420">Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="d00f0-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d00f0-421">Activation du protocole ICMP pour les configurations des règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="d00f0-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d00f0-422">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="d00f0-422">Updated cmdlets</span></span>
        - <span data-ttu-id="d00f0-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00f0-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00f0-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d00f0-426">Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d00f0-427">Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d00f0-428">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="d00f0-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00f0-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d00f0-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d00f0-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d00f0-432">Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde</span><span class="sxs-lookup"><span data-stu-id="d00f0-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d00f0-433">Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end.</span><span class="sxs-lookup"><span data-stu-id="d00f0-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d00f0-434">Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="d00f0-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00f0-436">Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="d00f0-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="d00f0-437">Correction de la gestion des expressions régulières null des journaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="d00f0-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-439">Mise à jour de « Get-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d00f0-440">Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d00f0-441">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d00f0-442">Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d00f0-443">Mise à jour de « Set-AzRecoveryServicesVaultContext.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d00f0-444">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d00f0-445">Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d00f0-446">Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d00f0-447">Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d00f0-448">Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »</span><span class="sxs-lookup"><span data-stu-id="d00f0-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-449">Az.Resources</span></span>
- <span data-ttu-id="d00f0-450">Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="d00f0-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d00f0-451">Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d00f0-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00f0-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00f0-452">Az.ServiceBus</span></span>
* <span data-ttu-id="d00f0-453">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d00f0-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d00f0-454">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="d00f0-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-455">Az.Sql</span></span>
* <span data-ttu-id="d00f0-456">Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d00f0-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d00f0-457">Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="d00f0-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d00f0-458">Correction d’une faute de frappe dans un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="d00f0-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-459">Az.Storage</span></span>
* <span data-ttu-id="d00f0-460">Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="d00f0-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00f0-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00f0-461">Az.StorageSync</span></span>
* <span data-ttu-id="d00f0-462">Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="d00f0-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d00f0-463">Résolution du problème 9551 pour honorer TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="d00f0-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-464">Az.Websites</span></span>
* <span data-ttu-id="d00f0-465">Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d00f0-466">Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d00f0-467">Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d00f0-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d00f0-468">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-469">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-470">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="d00f0-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d00f0-471">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="d00f0-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d00f0-472">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d00f0-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d00f0-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d00f0-473">Az.Advisor</span></span>
* <span data-ttu-id="d00f0-474">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d00f0-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d00f0-475">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="d00f0-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00f0-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-476">Az.ApiManagement</span></span>
* <span data-ttu-id="d00f0-477">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d00f0-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d00f0-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d00f0-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d00f0-479">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="d00f0-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d00f0-480">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="d00f0-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d00f0-481">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d00f0-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d00f0-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00f0-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d00f0-483">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-484">Az.Automation</span></span>
* <span data-ttu-id="d00f0-485">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="d00f0-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-486">Az.Compute</span></span>
* <span data-ttu-id="d00f0-487">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-488">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-489">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="d00f0-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00f0-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00f0-490">Az.EventGrid</span></span>
* <span data-ttu-id="d00f0-491">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="d00f0-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00f0-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-492">Az.IotHub</span></span>
* <span data-ttu-id="d00f0-493">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d00f0-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-494">Az.Network</span></span>
* <span data-ttu-id="d00f0-495">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="d00f0-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d00f0-496">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="d00f0-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00f0-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00f0-498">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d00f0-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d00f0-499">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d00f0-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00f0-501">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d00f0-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-503">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="d00f0-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-504">Az.Resources</span></span>
    - <span data-ttu-id="d00f0-505">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d00f0-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d00f0-506">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="d00f0-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d00f0-507">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="d00f0-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d00f0-508">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="d00f0-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00f0-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00f0-509">Az.ServiceBus</span></span>
* <span data-ttu-id="d00f0-510">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="d00f0-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-511">Az.Sql</span></span>
* <span data-ttu-id="d00f0-512">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="d00f0-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d00f0-513">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="d00f0-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d00f0-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d00f0-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d00f0-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d00f0-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d00f0-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d00f0-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d00f0-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d00f0-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d00f0-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d00f0-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d00f0-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d00f0-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d00f0-520">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d00f0-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-521">Az.Storage</span></span>
* <span data-ttu-id="d00f0-522">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="d00f0-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d00f0-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d00f0-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d00f0-524">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="d00f0-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d00f0-525">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="d00f0-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d00f0-526">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="d00f0-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d00f0-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d00f0-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d00f0-529">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="d00f0-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d00f0-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d00f0-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d00f0-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d00f0-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00f0-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00f0-532">Az.StorageSync</span></span>
* <span data-ttu-id="d00f0-533">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="d00f0-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d00f0-534">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-535">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-536">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="d00f0-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d00f0-537">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d00f0-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d00f0-538">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="d00f0-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d00f0-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d00f0-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d00f0-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d00f0-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-541">Az.Compute</span></span>
* <span data-ttu-id="d00f0-542">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d00f0-543">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="d00f0-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d00f0-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d00f0-544">Az.Dns</span></span>
* <span data-ttu-id="d00f0-545">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00f0-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00f0-546">Az.EventGrid</span></span>
* <span data-ttu-id="d00f0-547">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d00f0-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d00f0-548">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="d00f0-548">New cmdlets:</span></span>
    - <span data-ttu-id="d00f0-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d00f0-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d00f0-550">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="d00f0-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d00f0-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d00f0-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d00f0-552">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d00f0-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d00f0-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d00f0-554">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="d00f0-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d00f0-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d00f0-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d00f0-556">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="d00f0-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d00f0-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d00f0-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d00f0-558">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="d00f0-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d00f0-559">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d00f0-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d00f0-560">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="d00f0-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d00f0-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d00f0-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d00f0-562">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="d00f0-563">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d00f0-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d00f0-564">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="d00f0-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d00f0-565">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="d00f0-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="d00f0-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d00f0-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d00f0-567">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="d00f0-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d00f0-568">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="d00f0-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d00f0-569">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="d00f0-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d00f0-570">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="d00f0-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d00f0-571">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="d00f0-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d00f0-572">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="d00f0-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d00f0-573">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="d00f0-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d00f0-574">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="d00f0-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="d00f0-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="d00f0-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d00f0-576">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="d00f0-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d00f0-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d00f0-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d00f0-578">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="d00f0-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d00f0-579">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="d00f0-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00f0-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00f0-580">Az.FrontDoor</span></span>
* <span data-ttu-id="d00f0-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d00f0-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d00f0-582">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="d00f0-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d00f0-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d00f0-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d00f0-584">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="d00f0-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-585">Az.Network</span></span>
* <span data-ttu-id="d00f0-586">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="d00f0-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d00f0-587">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-587">New cmdlets</span></span>
        - <span data-ttu-id="d00f0-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d00f0-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d00f0-589">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d00f0-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d00f0-590">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-590">New cmdlets</span></span> 
        - <span data-ttu-id="d00f0-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d00f0-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d00f0-592">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00f0-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d00f0-593">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-593">New cmdlets</span></span> 
        - <span data-ttu-id="d00f0-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00f0-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="d00f0-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00f0-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00f0-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00f0-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00f0-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d00f0-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d00f0-599">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00f0-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d00f0-600">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-600">New cmdlets</span></span>
        - <span data-ttu-id="d00f0-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00f0-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00f0-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00f0-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00f0-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00f0-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00f0-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d00f0-605">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d00f0-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d00f0-606">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="d00f0-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d00f0-607">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="d00f0-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d00f0-608">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d00f0-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d00f0-609">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d00f0-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d00f0-610">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d00f0-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d00f0-611">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d00f0-612">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="d00f0-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d00f0-613">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d00f0-614">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="d00f0-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d00f0-615">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d00f0-616">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d00f0-617">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d00f0-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d00f0-618">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d00f0-619">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="d00f0-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d00f0-620">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="d00f0-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d00f0-621">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="d00f0-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d00f0-622">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="d00f0-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d00f0-623">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d00f0-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="d00f0-624">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="d00f0-625">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d00f0-626">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d00f0-627">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00f0-629">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="d00f0-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-630">Az.Resources</span></span>
* <span data-ttu-id="d00f0-631">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="d00f0-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d00f0-632">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d00f0-633">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d00f0-634">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="d00f0-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00f0-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-636">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-637">Az.Sql</span></span>
* <span data-ttu-id="d00f0-638">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d00f0-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d00f0-639">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="d00f0-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d00f0-640">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="d00f0-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d00f0-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d00f0-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d00f0-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d00f0-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d00f0-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d00f0-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d00f0-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d00f0-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d00f0-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d00f0-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-646">Az.Storage</span></span>
* <span data-ttu-id="d00f0-647">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="d00f0-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d00f0-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="d00f0-649">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="d00f0-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d00f0-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-651">Az.Websites</span></span>
* <span data-ttu-id="d00f0-652">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="d00f0-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d00f0-653">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d00f0-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d00f0-654">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d00f0-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00f0-655">Az.Cdn</span></span>
* <span data-ttu-id="d00f0-656">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="d00f0-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-657">Az.Compute</span></span>
* <span data-ttu-id="d00f0-658">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d00f0-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d00f0-659">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00f0-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00f0-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-660">Az.EventHub</span></span>
* <span data-ttu-id="d00f0-661">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="d00f0-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d00f0-662">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00f0-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-663">Az.Network</span></span>
* <span data-ttu-id="d00f0-664">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d00f0-665">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="d00f0-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00f0-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00f0-667">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d00f0-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-669">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="d00f0-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00f0-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00f0-670">Az.ServiceBus</span></span>
* <span data-ttu-id="d00f0-671">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00f0-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00f0-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-673">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="d00f0-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d00f0-674">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-675">Az.Sql</span></span>
* <span data-ttu-id="d00f0-676">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="d00f0-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d00f0-677">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d00f0-678">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="d00f0-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d00f0-679">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="d00f0-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-680">Az.Websites</span></span>
* <span data-ttu-id="d00f0-681">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="d00f0-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d00f0-682">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d00f0-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-683">Az.ApiManagement</span></span>
* <span data-ttu-id="d00f0-684">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d00f0-685">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d00f0-686">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d00f0-687">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="d00f0-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d00f0-688">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d00f0-689">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="d00f0-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d00f0-690">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d00f0-691">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d00f0-692">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="d00f0-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d00f0-693">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="d00f0-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d00f0-694">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="d00f0-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d00f0-695">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="d00f0-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d00f0-696">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="d00f0-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d00f0-697">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="d00f0-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d00f0-698">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="d00f0-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d00f0-699">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d00f0-700">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d00f0-701">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="d00f0-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d00f0-702">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d00f0-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="d00f0-703">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="d00f0-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d00f0-704">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="d00f0-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d00f0-705">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d00f0-706">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="d00f0-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d00f0-707">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="d00f0-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="d00f0-708">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="d00f0-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d00f0-709">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="d00f0-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d00f0-710">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d00f0-711">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d00f0-712">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d00f0-713">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="d00f0-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d00f0-714">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="d00f0-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="d00f0-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d00f0-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d00f0-716">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="d00f0-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d00f0-717">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00f0-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d00f0-718">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="d00f0-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d00f0-719">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="d00f0-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d00f0-720">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="d00f0-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d00f0-721">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="d00f0-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d00f0-722">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="d00f0-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d00f0-723">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00f0-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="d00f0-724">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d00f0-725">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="d00f0-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d00f0-726">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d00f0-727">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d00f0-728">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00f0-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d00f0-729">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d00f0-730">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="d00f0-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="d00f0-731">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d00f0-732">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="d00f0-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d00f0-733">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d00f0-734">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="d00f0-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d00f0-735">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="d00f0-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d00f0-736">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="d00f0-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d00f0-737">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="d00f0-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d00f0-738">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="d00f0-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d00f0-739">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="d00f0-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d00f0-740">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d00f0-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d00f0-741">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="d00f0-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d00f0-742">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="d00f0-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d00f0-743">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="d00f0-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d00f0-744">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d00f0-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d00f0-745">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="d00f0-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d00f0-746">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="d00f0-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d00f0-747">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="d00f0-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d00f0-748">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="d00f0-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d00f0-749">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="d00f0-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d00f0-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d00f0-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d00f0-751">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="d00f0-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d00f0-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d00f0-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d00f0-753">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="d00f0-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d00f0-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d00f0-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d00f0-755">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="d00f0-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d00f0-756">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="d00f0-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d00f0-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d00f0-758">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="d00f0-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="d00f0-759">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="d00f0-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d00f0-760">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="d00f0-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-761">Az.Automation</span></span>
* <span data-ttu-id="d00f0-762">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="d00f0-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d00f0-763">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d00f0-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d00f0-764">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d00f0-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d00f0-765">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="d00f0-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d00f0-766">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d00f0-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d00f0-767">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="d00f0-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d00f0-768">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="d00f0-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-769">Az.Compute</span></span>
* <span data-ttu-id="d00f0-770">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d00f0-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d00f0-771">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d00f0-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-773">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-774">Az.Monitor</span></span>
* <span data-ttu-id="d00f0-775">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="d00f0-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-776">Az.Network</span></span>
* <span data-ttu-id="d00f0-777">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="d00f0-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d00f0-778">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="d00f0-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00f0-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00f0-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d00f0-780">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f0-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-781">Az.Resources</span></span>
* <span data-ttu-id="d00f0-782">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="d00f0-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-783">Az.Sql</span></span>
* <span data-ttu-id="d00f0-784">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="d00f0-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d00f0-785">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-786">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-787">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="d00f0-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00f0-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00f0-789">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="d00f0-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d00f0-790">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="d00f0-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-791">Az.Compute</span></span>
* <span data-ttu-id="d00f0-792">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="d00f0-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d00f0-793">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d00f0-794">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d00f0-795">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d00f0-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d00f0-796">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d00f0-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d00f0-797">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00f0-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="d00f0-798">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="d00f0-798">Breaking changes</span></span>
    - <span data-ttu-id="d00f0-799">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d00f0-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d00f0-800">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d00f0-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d00f0-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d00f0-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="d00f0-802">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="d00f0-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d00f0-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d00f0-803">Az.Dns</span></span>
* <span data-ttu-id="d00f0-804">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="d00f0-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d00f0-805">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="d00f0-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d00f0-806">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="d00f0-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00f0-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00f0-807">Az.FrontDoor</span></span>
* <span data-ttu-id="d00f0-808">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00f0-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d00f0-809">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="d00f0-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d00f0-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00f0-810">Az.HDInsight</span></span>
* <span data-ttu-id="d00f0-811">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="d00f0-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d00f0-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00f0-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d00f0-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00f0-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d00f0-814">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00f0-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d00f0-815">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="d00f0-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d00f0-816">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="d00f0-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d00f0-817">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="d00f0-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-818">Az.Monitor</span></span>
* <span data-ttu-id="d00f0-819">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="d00f0-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="d00f0-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d00f0-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d00f0-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d00f0-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d00f0-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d00f0-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d00f0-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d00f0-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d00f0-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d00f0-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d00f0-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d00f0-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00f0-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00f0-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00f0-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00f0-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00f0-831">[Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="d00f0-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d00f0-832">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="d00f0-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-833">Az.Network</span></span>
* <span data-ttu-id="d00f0-834">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d00f0-835">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-835">New cmdlets</span></span>
        - <span data-ttu-id="d00f0-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="d00f0-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d00f0-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d00f0-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d00f0-840">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="d00f0-840">Updated cmdlets</span></span>
        - <span data-ttu-id="d00f0-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d00f0-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d00f0-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d00f0-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d00f0-843">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="d00f0-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d00f0-844">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d00f0-845">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="d00f0-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00f0-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00f0-847">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d00f0-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d00f0-848">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d00f0-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d00f0-849">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-851">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="d00f0-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d00f0-852">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d00f0-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d00f0-853">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d00f0-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d00f0-854">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d00f0-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d00f0-855">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="d00f0-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d00f0-856">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="d00f0-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d00f0-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d00f0-857">Az.Relay</span></span>
* <span data-ttu-id="d00f0-858">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="d00f0-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00f0-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00f0-859">Az.ServiceBus</span></span>
* <span data-ttu-id="d00f0-860">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="d00f0-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-861">Az.Storage</span></span>
* <span data-ttu-id="d00f0-862">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="d00f0-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d00f0-863">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="d00f0-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d00f0-864">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="d00f0-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d00f0-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="d00f0-866">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="d00f0-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d00f0-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d00f0-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d00f0-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-870">Az.Websites</span></span>
* <span data-ttu-id="d00f0-871">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d00f0-872">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="d00f0-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d00f0-873">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00f0-874">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="d00f0-874">Highlights since the last major release</span></span>
* <span data-ttu-id="d00f0-875">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="d00f0-875">General availability of `Az` module</span></span>
* <span data-ttu-id="d00f0-876">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d00f0-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d00f0-877">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d00f0-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d00f0-878">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d00f0-879">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="d00f0-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00f0-880">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d00f0-881">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="d00f0-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00f0-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-882">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-883">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="d00f0-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00f0-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00f0-884">Az.Batch</span></span>
* <span data-ttu-id="d00f0-885">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00f0-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00f0-886">Az.Cdn</span></span>
* <span data-ttu-id="d00f0-887">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00f0-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00f0-889">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-890">Az.Compute</span></span>
* <span data-ttu-id="d00f0-891">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="d00f0-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d00f0-892">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00f0-893">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="d00f0-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-894">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-895">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="d00f0-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-897">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00f0-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00f0-898">Az.EventGrid</span></span>
* <span data-ttu-id="d00f0-899">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="d00f0-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00f0-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-900">Az.EventHub</span></span>
* <span data-ttu-id="d00f0-901">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="d00f0-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d00f0-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00f0-902">Az.HDInsight</span></span>
* <span data-ttu-id="d00f0-903">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00f0-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-904">Az.IotHub</span></span>
* <span data-ttu-id="d00f0-905">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00f0-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-906">Az.KeyVault</span></span>
* <span data-ttu-id="d00f0-907">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00f0-908">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="d00f0-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d00f0-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d00f0-909">Az.MachineLearning</span></span>
* <span data-ttu-id="d00f0-910">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d00f0-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d00f0-911">Az.Media</span></span>
* <span data-ttu-id="d00f0-912">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-913">Az.Monitor</span></span>
  * <span data-ttu-id="d00f0-914">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="d00f0-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d00f0-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d00f0-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d00f0-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d00f0-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d00f0-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d00f0-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d00f0-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d00f0-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d00f0-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d00f0-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d00f0-920">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="d00f0-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-921">Az.Network</span></span>
* <span data-ttu-id="d00f0-922">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00f0-923">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="d00f0-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d00f0-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d00f0-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="d00f0-925">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00f0-927">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d00f0-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d00f0-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d00f0-929">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-931">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00f0-932">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="d00f0-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d00f0-933">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d00f0-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d00f0-934">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="d00f0-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00f0-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00f0-935">Az.RedisCache</span></span>
* <span data-ttu-id="d00f0-936">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-937">Az.Resources</span></span>
* <span data-ttu-id="d00f0-938">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="d00f0-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-939">Az.Sql</span></span>
* <span data-ttu-id="d00f0-940">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="d00f0-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d00f0-941">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00f0-942">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="d00f0-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d00f0-943">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="d00f0-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d00f0-944">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="d00f0-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d00f0-945">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="d00f0-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d00f0-946">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="d00f0-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-947">Az.Websites</span></span>
* <span data-ttu-id="d00f0-948">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="d00f0-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d00f0-949">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="d00f0-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00f0-950">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="d00f0-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d00f0-951">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d00f0-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d00f0-952">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00f0-953">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="d00f0-953">Highlights since the last major release</span></span>
* <span data-ttu-id="d00f0-954">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="d00f0-954">General availability of `Az` module</span></span>
* <span data-ttu-id="d00f0-955">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d00f0-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d00f0-956">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d00f0-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d00f0-957">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d00f0-958">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="d00f0-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00f0-959">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d00f0-960">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="d00f0-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00f0-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-961">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-962">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d00f0-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00f0-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00f0-964">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="d00f0-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d00f0-965">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="d00f0-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-966">Az.Automation</span></span>
* <span data-ttu-id="d00f0-967">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="d00f0-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d00f0-968">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="d00f0-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d00f0-969">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-970">Az.Compute</span></span>
* <span data-ttu-id="d00f0-971">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d00f0-972">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="d00f0-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d00f0-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="d00f0-974">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="d00f0-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-975">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-976">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="d00f0-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d00f0-977">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d00f0-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-978">Az.Resources</span></span>
* <span data-ttu-id="d00f0-979">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="d00f0-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d00f0-980">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00f0-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d00f0-981">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d00f0-982">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d00f0-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d00f0-983">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="d00f0-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d00f0-984">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d00f0-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-985">Az.Sql</span></span>
* <span data-ttu-id="d00f0-986">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="d00f0-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-987">Az.Storage</span></span>
* <span data-ttu-id="d00f0-988">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="d00f0-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d00f0-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d00f0-989">New-AzStorageContext</span></span>
* <span data-ttu-id="d00f0-990">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="d00f0-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d00f0-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d00f0-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d00f0-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d00f0-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d00f0-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d00f0-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d00f0-995">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="d00f0-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d00f0-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d00f0-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d00f0-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d00f0-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00f0-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d00f0-1000">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00f0-1001">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="d00f0-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="d00f0-1002">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="d00f0-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="d00f0-1003">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d00f0-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d00f0-1004">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d00f0-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d00f0-1005">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d00f0-1006">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="d00f0-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00f0-1007">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d00f0-1008">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1009">Az.Automation</span></span>
* <span data-ttu-id="d00f0-1010">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="d00f0-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d00f0-1011">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="d00f0-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="d00f0-1012">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="d00f0-1012">Pre-Post script</span></span>
    * <span data-ttu-id="d00f0-1013">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1014">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1015">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d00f0-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d00f0-1016">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00f0-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-1017">Az.KeyVault</span></span>
* <span data-ttu-id="d00f0-1018">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1019">Az.Network</span></span>
* <span data-ttu-id="d00f0-1020">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d00f0-1021">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="d00f0-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-1023">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="d00f0-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d00f0-1024">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="d00f0-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1025">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1026">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d00f0-1027">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="d00f0-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1028">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1029">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1030">Az.Storage</span></span>
* <span data-ttu-id="d00f0-1031">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d00f0-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d00f0-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d00f0-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d00f0-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d00f0-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d00f0-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d00f0-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d00f0-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1038">Az.Websites</span></span>
* <span data-ttu-id="d00f0-1039">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="d00f0-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d00f0-1040">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1041">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-1042">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="d00f0-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d00f0-1043">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1044">Az.Automation</span></span>
* <span data-ttu-id="d00f0-1045">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d00f0-1046">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d00f0-1047">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="d00f0-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00f0-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00f0-1048">Az.Cdn</span></span>
* <span data-ttu-id="d00f0-1049">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1050">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1051">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="d00f0-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-1052">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-1053">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="d00f0-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00f0-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-1054">Az.LogicApp</span></span>
* <span data-ttu-id="d00f0-1055">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="d00f0-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1056">Az.Network</span></span>
* <span data-ttu-id="d00f0-1057">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-1059">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="d00f0-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d00f0-1060">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="d00f0-1060">SDK Update</span></span>
* <span data-ttu-id="d00f0-1061">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d00f0-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d00f0-1062">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d00f0-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1063">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1064">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="d00f0-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d00f0-1065">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d00f0-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d00f0-1066">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d00f0-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d00f0-1067">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d00f0-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d00f0-1068">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d00f0-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d00f0-1069">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d00f0-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1070">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1071">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d00f0-1072">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1073">Az.Storage</span></span>
* <span data-ttu-id="d00f0-1074">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d00f0-1075">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d00f0-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00f0-1077">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="d00f0-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1078">Az.Automation</span></span>
* <span data-ttu-id="d00f0-1079">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d00f0-1080">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d00f0-1081">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00f0-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00f0-1083">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1084">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1085">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="d00f0-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d00f0-1086">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d00f0-1087">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d00f0-1088">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-1090">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="d00f0-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00f0-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-1091">Az.EventHub</span></span>
* <span data-ttu-id="d00f0-1092">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="d00f0-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d00f0-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-1093">Az.KeyVault</span></span>
* <span data-ttu-id="d00f0-1094">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d00f0-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00f0-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-1095">Az.LogicApp</span></span>
* <span data-ttu-id="d00f0-1096">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="d00f0-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d00f0-1097">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="d00f0-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d00f0-1098">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d00f0-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00f0-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d00f0-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00f0-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d00f0-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00f0-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d00f0-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00f0-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d00f0-1103">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d00f0-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d00f0-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d00f0-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d00f0-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d00f0-1108">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d00f0-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00f0-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-1109">Az.Monitor</span></span>
* <span data-ttu-id="d00f0-1110">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="d00f0-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1111">Az.Network</span></span>
* <span data-ttu-id="d00f0-1112">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d00f0-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00f0-1114">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d00f0-1115">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d00f0-1116">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d00f0-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1117">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1118">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d00f0-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d00f0-1119">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d00f0-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d00f0-1120">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d00f0-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d00f0-1121">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d00f0-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1122">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1123">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="d00f0-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d00f0-1124">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1125">Az.Websites</span></span>
* <span data-ttu-id="d00f0-1126">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="d00f0-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d00f0-1127">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1128">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-1129">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00f0-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00f0-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="d00f0-1131">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1132">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1133">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="d00f0-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d00f0-1134">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d00f0-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d00f0-1135">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="d00f0-1137">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1138">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1139">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d00f0-1140">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d00f0-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d00f0-1141">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="d00f0-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d00f0-1142">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d00f0-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1143">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1144">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d00f0-1145">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="d00f0-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d00f0-1146">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="d00f0-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d00f0-1147">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1148">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-1149">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="d00f0-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00f0-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00f0-1151">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="d00f0-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00f0-1153">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="d00f0-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d00f0-1154">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1155">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-1156">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="d00f0-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00f0-1157">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00f0-1158">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="d00f0-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00f0-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00f0-1159">Az.Aks</span></span>
* <span data-ttu-id="d00f0-1160">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00f0-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1161">Az.Automation</span></span>
* <span data-ttu-id="d00f0-1162">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="d00f0-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d00f0-1163">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00f0-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00f0-1164">Az.Cdn</span></span>
* <span data-ttu-id="d00f0-1165">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1166">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1167">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d00f0-1168">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00f0-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d00f0-1169">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00f0-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d00f0-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d00f0-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d00f0-1171">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00f0-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00f0-1172">Az.DataFactory</span></span>
* <span data-ttu-id="d00f0-1173">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d00f0-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-1175">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="d00f0-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d00f0-1176">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d00f0-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d00f0-1177">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00f0-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-1178">Az.IotHub</span></span>
* <span data-ttu-id="d00f0-1179">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00f0-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-1180">Az.KeyVault</span></span>
* <span data-ttu-id="d00f0-1181">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1182">Az.Network</span></span>
* <span data-ttu-id="d00f0-1183">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1184">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1185">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d00f0-1186">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d00f0-1187">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d00f0-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d00f0-1188">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d00f0-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d00f0-1189">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d00f0-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d00f0-1190">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d00f0-1191">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d00f0-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00f0-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-1193">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="d00f0-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d00f0-1194">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1194">Fix some error messages.</span></span>
* <span data-ttu-id="d00f0-1195">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d00f0-1196">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00f0-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00f0-1197">Az.SignalR</span></span>
* <span data-ttu-id="d00f0-1198">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1199">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1200">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00f0-1201">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d00f0-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d00f0-1202">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="d00f0-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d00f0-1203">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="d00f0-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1204">Az.Storage</span></span>
* <span data-ttu-id="d00f0-1205">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00f0-1206">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d00f0-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d00f0-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d00f0-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d00f0-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d00f0-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d00f0-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="d00f0-1210">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1211">Az.Websites</span></span>
* <span data-ttu-id="d00f0-1212">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="d00f0-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00f0-1213">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d00f0-1214">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="d00f0-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d00f0-1215">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="d00f0-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00f0-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1216">Az.Accounts</span></span>
* <span data-ttu-id="d00f0-1217">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="d00f0-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1218">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1219">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d00f0-1220">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="d00f0-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d00f0-1221">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-1223">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d00f0-1224">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="d00f0-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00f0-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00f0-1225">Az.EventGrid</span></span>
* <span data-ttu-id="d00f0-1226">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d00f0-1227">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d00f0-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d00f0-1228">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="d00f0-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d00f0-1229">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="d00f0-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d00f0-1230">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="d00f0-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d00f0-1231">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d00f0-1232">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="d00f0-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d00f0-1233">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="d00f0-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d00f0-1234">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="d00f0-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d00f0-1235">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="d00f0-1236">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d00f0-1237">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00f0-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-1238">Az.IotHub</span></span>
* <span data-ttu-id="d00f0-1239">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="d00f0-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00f0-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-1240">Az.LogicApp</span></span>
* <span data-ttu-id="d00f0-1241">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="d00f0-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1242">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1243">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d00f0-1244">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d00f0-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d00f0-1245">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d00f0-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d00f0-1246">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d00f0-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d00f0-1247">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d00f0-1248">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d00f0-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00f0-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00f0-1249">Az.SignalR</span></span>
* <span data-ttu-id="d00f0-1250">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1251">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1252">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00f0-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1253">Az.Storage</span></span>
* <span data-ttu-id="d00f0-1254">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="d00f0-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d00f0-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d00f0-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="d00f0-1256">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="d00f0-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d00f0-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d00f0-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1258">Az.Websites</span></span>
* <span data-ttu-id="d00f0-1259">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d00f0-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d00f0-1260">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d00f0-1261">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d00f0-1262">Généralités</span><span class="sxs-lookup"><span data-stu-id="d00f0-1262">General</span></span>

- <span data-ttu-id="d00f0-1263">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="d00f0-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="d00f0-1264">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="d00f0-1264">Online help for each module</span></span>
- <span data-ttu-id="d00f0-1265">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="d00f0-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d00f0-1266">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="d00f0-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d00f0-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1267">Az.Accounts</span></span>
- <span data-ttu-id="d00f0-1268">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="d00f0-1269">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="d00f0-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d00f0-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="d00f0-1271">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="d00f0-1271">Fixes for #7002</span></span>
- <span data-ttu-id="d00f0-1272">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d00f0-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00f0-1273">Az.Batch</span></span>
- <span data-ttu-id="d00f0-1274">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d00f0-1275">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d00f0-1276">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d00f0-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d00f0-1277">Az.Billing</span></span>
- <span data-ttu-id="d00f0-1278">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d00f0-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="d00f0-1280">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d00f0-1281">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="d00f0-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d00f0-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="d00f0-1283">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="d00f0-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d00f0-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d00f0-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d00f0-1285">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="d00f0-1287">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d00f0-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00f0-1288">Az.Monitor</span></span>
- <span data-ttu-id="d00f0-1289">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d00f0-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00f0-1290">Az.KeyVault</span></span>
- <span data-ttu-id="d00f0-1291">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="d00f0-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d00f0-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d00f0-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="d00f0-1293">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d00f0-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d00f0-1294">Az.Media</span></span>
- <span data-ttu-id="d00f0-1295">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d00f0-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d00f0-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1296">Az.Network</span></span>
<span data-ttu-id="d00f0-1297">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d00f0-1298">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="d00f0-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="d00f0-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00f0-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00f0-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00f0-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00f0-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00f0-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d00f0-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d00f0-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00f0-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d00f0-1307">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d00f0-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d00f0-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d00f0-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d00f0-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d00f0-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d00f0-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d00f0-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d00f0-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d00f0-1314">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d00f0-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d00f0-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f0-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d00f0-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f0-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d00f0-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d00f0-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d00f0-1318">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d00f0-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d00f0-1319">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d00f0-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="d00f0-1321">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d00f0-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1322">Az.Profile</span></span>
- <span data-ttu-id="d00f0-1323">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00f0-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="d00f0-1325">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d00f0-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1326">Az.Resources</span></span>
- <span data-ttu-id="d00f0-1327">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d00f0-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="d00f0-1329">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="d00f0-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d00f0-1330">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d00f0-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d00f0-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="d00f0-1332">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d00f0-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d00f0-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1333">Az.Sql</span></span>
- <span data-ttu-id="d00f0-1334">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="d00f0-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d00f0-1335">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="d00f0-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d00f0-1336">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d00f0-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1337">Az.Storage</span></span>
- <span data-ttu-id="d00f0-1338">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d00f0-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1339">Az.Websites</span></span>
- <span data-ttu-id="d00f0-1340">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="d00f0-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d00f0-1341">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d00f0-1342">Généralités</span><span class="sxs-lookup"><span data-stu-id="d00f0-1342">General</span></span>

* <span data-ttu-id="d00f0-1343">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="d00f0-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d00f0-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1344">Az.Compute</span></span>

* <span data-ttu-id="d00f0-1345">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="d00f0-1347">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="d00f0-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d00f0-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00f0-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="d00f0-1349">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="d00f0-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="d00f0-1350">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d00f0-1351">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d00f0-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="d00f0-1353">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d00f0-1354">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d00f0-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1355">Az.Resources</span></span>

* <span data-ttu-id="d00f0-1356">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="d00f0-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d00f0-1357">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d00f0-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1358">Az.Sql</span></span>

* <span data-ttu-id="d00f0-1359">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="d00f0-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d00f0-1360">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="d00f0-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d00f0-1361">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d00f0-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1362">Az.Storage</span></span>

* <span data-ttu-id="d00f0-1363">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d00f0-1364">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="d00f0-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d00f0-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d00f0-1366">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="d00f0-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="d00f0-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d00f0-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d00f0-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d00f0-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d00f0-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1369">Az.Websites</span></span>

* <span data-ttu-id="d00f0-1370">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d00f0-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d00f0-1371">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d00f0-1372">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d00f0-1373">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d00f0-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00f0-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="d00f0-1375">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="d00f0-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d00f0-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00f0-1376">Az.Automation</span></span>
* <span data-ttu-id="d00f0-1377">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="d00f0-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d00f0-1378">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="d00f0-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d00f0-1379">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="d00f0-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d00f0-1380">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d00f0-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d00f0-1381">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="d00f0-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d00f0-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1382">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1383">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d00f0-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d00f0-1384">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="d00f0-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d00f0-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="d00f0-1386">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="d00f0-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d00f0-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d00f0-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d00f0-1388">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="d00f0-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d00f0-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1389">Az.Network</span></span>
* <span data-ttu-id="d00f0-1390">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d00f0-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d00f0-1391">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="d00f0-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d00f0-1392">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d00f0-1393">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d00f0-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d00f0-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d00f0-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d00f0-1395">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d00f0-1396">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d00f0-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d00f0-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d00f0-1398">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d00f0-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d00f0-1399">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="d00f0-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d00f0-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d00f0-1400">Az.Relay</span></span>
* <span data-ttu-id="d00f0-1401">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d00f0-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1402">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1403">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="d00f0-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d00f0-1404">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="d00f0-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d00f0-1405">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d00f0-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d00f0-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-1407">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="d00f0-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d00f0-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1408">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1409">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="d00f0-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d00f0-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00f0-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00f0-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00f0-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00f0-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00f0-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00f0-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d00f0-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00f0-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d00f0-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00f0-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d00f0-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00f0-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d00f0-1418">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d00f0-1419">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d00f0-1420">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d00f0-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d00f0-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d00f0-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d00f0-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d00f0-1425">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d00f0-1426">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d00f0-1427">Généralités</span><span class="sxs-lookup"><span data-stu-id="d00f0-1427">General</span></span>
* <span data-ttu-id="d00f0-1428">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="d00f0-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d00f0-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1429">Az.Profile</span></span>
* <span data-ttu-id="d00f0-1430">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00f0-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d00f0-1431">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="d00f0-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d00f0-1432">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d00f0-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d00f0-1433">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="d00f0-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d00f0-1434">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="d00f0-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d00f0-1435">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="d00f0-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d00f0-1436">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="d00f0-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00f0-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00f0-1438">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1439">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1440">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d00f0-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d00f0-1441">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d00f0-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d00f0-1442">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-1444">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d00f0-1445">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d00f0-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d00f0-1446">Az.Insights</span></span>
* <span data-ttu-id="d00f0-1447">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="d00f0-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d00f0-1448">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="d00f0-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d00f0-1449">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="d00f0-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d00f0-1450">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="d00f0-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1451">Az.Network</span></span>
* <span data-ttu-id="d00f0-1452">Modification du type de peering en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="d00f0-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d00f0-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00f0-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d00f0-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d00f0-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d00f0-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d00f0-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d00f0-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d00f0-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d00f0-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00f0-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d00f0-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d00f0-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00f0-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00f0-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00f0-1460">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="d00f0-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1461">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1462">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="d00f0-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d00f0-1463">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00f0-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00f0-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="d00f0-1465">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00f0-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00f0-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00f0-1467">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d00f0-1468">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d00f0-1469">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d00f0-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d00f0-1470">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d00f0-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d00f0-1471">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d00f0-1472">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d00f0-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1473">Az.Profile</span></span>
* <span data-ttu-id="d00f0-1474">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="d00f0-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d00f0-1475">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00f0-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1476">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1477">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="d00f0-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d00f0-1478">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00f0-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00f0-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00f0-1480">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="d00f0-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d00f0-1481">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d00f0-1482">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d00f0-1483">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d00f0-1484">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1485">Az.Network</span></span>
* <span data-ttu-id="d00f0-1486">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d00f0-1487">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1488">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1489">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d00f0-1490">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="d00f0-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d00f0-1491">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d00f0-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1492">Azure.Storage</span></span>
* <span data-ttu-id="d00f0-1493">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="d00f0-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d00f0-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d00f0-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d00f0-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d00f0-1496">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d00f0-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d00f0-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d00f0-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00f0-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00f0-1499">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00f0-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00f0-1500">Az.Compute</span></span>
* <span data-ttu-id="d00f0-1501">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="d00f0-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d00f0-1502">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d00f0-1503">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="d00f0-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d00f0-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d00f0-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d00f0-1505">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00f0-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00f0-1506">Az.Network</span></span>
* <span data-ttu-id="d00f0-1507">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d00f0-1508">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="d00f0-1508">new cmdlets added</span></span>
    - <span data-ttu-id="d00f0-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00f0-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00f0-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00f0-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00f0-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00f0-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d00f0-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d00f0-1515">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="d00f0-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d00f0-1516">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d00f0-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d00f0-1517">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d00f0-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00f0-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00f0-1518">Az.RedisCache</span></span>
* <span data-ttu-id="d00f0-1519">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="d00f0-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d00f0-1520">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="d00f0-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00f0-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00f0-1521">Az.Resources</span></span>
* <span data-ttu-id="d00f0-1522">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d00f0-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d00f0-1523">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="d00f0-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00f0-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00f0-1524">Az.Sql</span></span>
* <span data-ttu-id="d00f0-1525">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="d00f0-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00f0-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00f0-1526">Az.Websites</span></span>
* <span data-ttu-id="d00f0-1527">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="d00f0-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d00f0-1528">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="d00f0-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d00f0-1529">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="d00f0-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d00f0-1530">Version initiale</span><span class="sxs-lookup"><span data-stu-id="d00f0-1530">Initial Release</span></span>
