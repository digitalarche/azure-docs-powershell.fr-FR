---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110481"
---
# <a name="release-notes"></a><span data-ttu-id="d4d6c-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="d4d6c-103">Release notes</span></span>

<span data-ttu-id="d4d6c-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="d4d6c-105">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d4d6c-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d4d6c-106">AzureRM.Profile</span></span>
* <span data-ttu-id="d4d6c-107">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d4d6c-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d4d6c-108">Azure.Storage</span></span>
* <span data-ttu-id="d4d6c-109">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="d4d6c-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="d4d6c-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d4d6c-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="d4d6c-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d4d6c-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d4d6c-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4d6c-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d4d6c-113">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="d4d6c-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="d4d6c-114">AzureRM.Automation</span></span>
* <span data-ttu-id="d4d6c-115">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d4d6c-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d4d6c-116">AzureRM.Compute</span></span>
* <span data-ttu-id="d4d6c-117">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d4d6c-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="d4d6c-118">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="d4d6c-119">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="d4d6c-120">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="d4d6c-121">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d4d6c-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4d6c-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="d4d6c-123">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="d4d6c-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d4d6c-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4d6c-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d4d6c-125">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d4d6c-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="d4d6c-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d4d6c-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="d4d6c-127">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d4d6c-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d4d6c-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d4d6c-128">AzureRM.Network</span></span>
* <span data-ttu-id="d4d6c-129">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d4d6c-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="d4d6c-130">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d4d6c-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="d4d6c-131">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="d4d6c-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="d4d6c-132">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d4d6c-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="d4d6c-133">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d4d6c-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="d4d6c-134">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="d4d6c-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="d4d6c-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="d4d6c-135">AzureRM.Relay</span></span>
* <span data-ttu-id="d4d6c-136">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="d4d6c-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d4d6c-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d4d6c-137">AzureRM.Resources</span></span>
* <span data-ttu-id="d4d6c-138">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="d4d6c-139">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="d4d6c-140">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d4d6c-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="d4d6c-141">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="d4d6c-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="d4d6c-142">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="d4d6c-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d4d6c-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4d6c-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d4d6c-144">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="d4d6c-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="d4d6c-145">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="d4d6c-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d4d6c-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d4d6c-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d4d6c-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d4d6c-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="d4d6c-151">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="d4d6c-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d4d6c-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4d6c-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d4d6c-153">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d4d6c-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d4d6c-154">AzureRM.Sql</span></span>
* <span data-ttu-id="d4d6c-155">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="d4d6c-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="d4d6c-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d4d6c-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="d4d6c-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d4d6c-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d4d6c-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d4d6c-158">AzureRM.Websites</span></span>
* <span data-ttu-id="d4d6c-159">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="d4d6c-160">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="d4d6c-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="d4d6c-161">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="d4d6c-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="d4d6c-162">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d4d6c-163">Généralités</span><span class="sxs-lookup"><span data-stu-id="d4d6c-163">General</span></span>
* <span data-ttu-id="d4d6c-164">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="d4d6c-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d4d6c-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d4d6c-165">AzureRM.Profile</span></span>
* <span data-ttu-id="d4d6c-166">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="d4d6c-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d4d6c-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d4d6c-167">AzureRM.Compute</span></span>
* <span data-ttu-id="d4d6c-168">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="d4d6c-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="d4d6c-169">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="d4d6c-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="d4d6c-170">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="d4d6c-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="d4d6c-171">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="d4d6c-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="d4d6c-172">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="d4d6c-173">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="d4d6c-174">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="d4d6c-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d4d6c-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="d4d6c-176">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="d4d6c-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4d6c-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="d4d6c-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4d6c-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="d4d6c-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4d6c-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d4d6c-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4d6c-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d4d6c-181">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="d4d6c-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="d4d6c-182">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="d4d6c-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d4d6c-183">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="d4d6c-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="d4d6c-184">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="d4d6c-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d4d6c-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d4d6c-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="d4d6c-186">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d4d6c-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="d4d6c-187">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="d4d6c-188">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="d4d6c-189">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d4d6c-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4d6c-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d4d6c-191">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="d4d6c-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d4d6c-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d4d6c-192">AzureRM.Network</span></span>
* <span data-ttu-id="d4d6c-193">Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone</span><span class="sxs-lookup"><span data-stu-id="d4d6c-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="d4d6c-194">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="d4d6c-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="d4d6c-195">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d4d6c-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="d4d6c-196">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d4d6c-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="d4d6c-197">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d4d6c-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d4d6c-198">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d4d6c-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d4d6c-199">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d4d6c-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d4d6c-200">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d4d6c-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d4d6c-201">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d4d6c-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d4d6c-202">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d4d6c-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d4d6c-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d4d6c-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d4d6c-204">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="d4d6c-205">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="d4d6c-206">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d4d6c-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d4d6c-207">AzureRM.Resources</span></span>
* <span data-ttu-id="d4d6c-208">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="d4d6c-209">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="d4d6c-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="d4d6c-210">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="d4d6c-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="d4d6c-211">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="d4d6c-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="d4d6c-212">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d4d6c-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="d4d6c-213">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="d4d6c-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="d4d6c-214">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="d4d6c-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="d4d6c-215">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d4d6c-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="d4d6c-216">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="d4d6c-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="d4d6c-217">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="d4d6c-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="d4d6c-218">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d4d6c-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="d4d6c-219">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d4d6c-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="d4d6c-220">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="d4d6c-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="d4d6c-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d4d6c-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d4d6c-222">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d4d6c-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d4d6c-223">AzureRM.Sql</span></span>
* <span data-ttu-id="d4d6c-224">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="d4d6c-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="d4d6c-225">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="d4d6c-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="d4d6c-226">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d4d6c-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d4d6c-227">AzureRM.Profile</span></span>
* <span data-ttu-id="d4d6c-228">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="d4d6c-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="d4d6c-229">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="d4d6c-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d4d6c-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d4d6c-230">Azure.Storage</span></span>
* <span data-ttu-id="d4d6c-231">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d4d6c-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d4d6c-232">AzureRM.Compute</span></span>
* <span data-ttu-id="d4d6c-233">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="d4d6c-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="d4d6c-234">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="d4d6c-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="d4d6c-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d4d6c-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="d4d6c-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="d4d6c-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="d4d6c-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d4d6c-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="d4d6c-238">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="d4d6c-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d4d6c-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="d4d6c-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d4d6c-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="d4d6c-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d4d6c-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="d4d6c-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d4d6c-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="d4d6c-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="d4d6c-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="d4d6c-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="d4d6c-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d4d6c-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="d4d6c-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="d4d6c-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="d4d6c-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="d4d6c-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="d4d6c-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="d4d6c-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d4d6c-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="d4d6c-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d4d6c-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="d4d6c-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="d4d6c-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="d4d6c-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d4d6c-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="d4d6c-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d4d6c-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="d4d6c-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="d4d6c-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="d4d6c-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d4d6c-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="d4d6c-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d4d6c-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="d4d6c-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d4d6c-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="d4d6c-259">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d4d6c-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4d6c-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d4d6c-261">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="d4d6c-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="d4d6c-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d4d6c-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="d4d6c-263">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="d4d6c-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="d4d6c-264">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="d4d6c-265">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="d4d6c-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d4d6c-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d4d6c-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d4d6c-267">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="d4d6c-268">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d4d6c-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d4d6c-269">AzureRM.Sql</span></span>
* <span data-ttu-id="d4d6c-270">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="d4d6c-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d4d6c-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d4d6c-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d4d6c-272">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d4d6c-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d4d6c-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d4d6c-273">AzureRM.Websites</span></span>
* <span data-ttu-id="d4d6c-274">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d4d6c-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="d4d6c-275">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d4d6c-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="d4d6c-276">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="d4d6c-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d4d6c-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="d4d6c-278">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="d4d6c-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="d4d6c-279">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d4d6c-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d4d6c-280">AzureRM.Profile</span></span>
* <span data-ttu-id="d4d6c-281">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="d4d6c-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d4d6c-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d4d6c-282">AzureRM.Compute</span></span>
* <span data-ttu-id="d4d6c-283">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="d4d6c-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="d4d6c-284">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="d4d6c-285">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d4d6c-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d4d6c-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d4d6c-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d4d6c-287">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="d4d6c-288">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="d4d6c-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="d4d6c-289">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="d4d6c-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="d4d6c-290">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="d4d6c-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="d4d6c-291">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="d4d6c-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="d4d6c-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d4d6c-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d4d6c-293">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="d4d6c-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="d4d6c-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d4d6c-294">AzureRM.Network</span></span>
* <span data-ttu-id="d4d6c-295">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="d4d6c-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d4d6c-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d4d6c-296">AzureRM.Resources</span></span>
* <span data-ttu-id="d4d6c-297">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="d4d6c-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="d4d6c-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="d4d6c-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="d4d6c-299">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="d4d6c-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="d4d6c-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d4d6c-300">AzureRM.Sql</span></span>
* <span data-ttu-id="d4d6c-301">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="d4d6c-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="d4d6c-302">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4d6c-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d4d6c-303">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d4d6c-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d4d6c-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d4d6c-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d4d6c-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d4d6c-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d4d6c-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4d6c-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d4d6c-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d4d6c-307">AzureRM.Websites</span></span>
* <span data-ttu-id="d4d6c-308">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="d4d6c-309">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="d4d6c-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d4d6c-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d4d6c-310">AzureRM.Profile</span></span>
* <span data-ttu-id="d4d6c-311">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="d4d6c-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d4d6c-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d4d6c-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d4d6c-313">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="d4d6c-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d4d6c-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d4d6c-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d4d6c-315">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="d4d6c-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="d4d6c-316">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4d6c-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="d4d6c-317">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="d4d6c-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="d4d6c-318">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="d4d6c-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="d4d6c-319">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="d4d6c-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="d4d6c-320">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="d4d6c-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="d4d6c-321">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="d4d6c-321">Added support for MSI identity</span></span>
* <span data-ttu-id="d4d6c-322">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="d4d6c-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="d4d6c-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="d4d6c-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="d4d6c-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="d4d6c-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="d4d6c-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="d4d6c-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="d4d6c-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="d4d6c-327">AzureRM.Batch</span></span>
* <span data-ttu-id="d4d6c-328">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="d4d6c-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="d4d6c-329">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="d4d6c-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="d4d6c-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="d4d6c-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="d4d6c-331">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="d4d6c-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d4d6c-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d4d6c-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d4d6c-333">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="d4d6c-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d4d6c-334">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4d6c-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="d4d6c-335">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d4d6c-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="d4d6c-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d4d6c-336">AzureRM.Network</span></span>
* <span data-ttu-id="d4d6c-337">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="d4d6c-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="d4d6c-338">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="d4d6c-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4d6c-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="d4d6c-340">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="d4d6c-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d4d6c-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d4d6c-342">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="d4d6c-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d4d6c-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d4d6c-344">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="d4d6c-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d4d6c-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d4d6c-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4d6c-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d4d6c-347">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="d4d6c-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d4d6c-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d4d6c-348">AzureRM.Sql</span></span>
* <span data-ttu-id="d4d6c-349">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d4d6c-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="d4d6c-350">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="d4d6c-351">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="d4d6c-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="d4d6c-352">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="d4d6c-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="d4d6c-353">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="d4d6c-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="d4d6c-354">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4d6c-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d4d6c-355">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d4d6c-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d4d6c-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d4d6c-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d4d6c-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d4d6c-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d4d6c-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4d6c-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d4d6c-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d4d6c-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d4d6c-360">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="d4d6c-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>