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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406292"
---
# <a name="release-notes"></a><span data-ttu-id="a4137-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="a4137-103">Release notes</span></span>

<span data-ttu-id="a4137-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="a4137-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="a4137-105">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="a4137-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a4137-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="a4137-106">General</span></span>
* <span data-ttu-id="a4137-107">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="a4137-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a4137-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a4137-108">AzureRM.Profile</span></span>
* <span data-ttu-id="a4137-109">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="a4137-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a4137-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a4137-110">AzureRM.Compute</span></span>
* <span data-ttu-id="a4137-111">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="a4137-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a4137-112">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="a4137-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a4137-113">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="a4137-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a4137-114">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="a4137-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a4137-115">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a4137-116">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="a4137-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a4137-117">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a4137-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a4137-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a4137-119">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4137-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a4137-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a4137-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a4137-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a4137-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a4137-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a4137-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a4137-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a4137-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a4137-124">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="a4137-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a4137-125">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="a4137-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a4137-126">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="a4137-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a4137-127">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="a4137-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a4137-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a4137-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="a4137-129">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a4137-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a4137-130">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="a4137-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a4137-131">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="a4137-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a4137-132">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a4137-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a4137-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a4137-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a4137-134">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="a4137-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a4137-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a4137-135">AzureRM.Network</span></span>
* <span data-ttu-id="a4137-136">Exposer les nouvelles références SKU pour Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a4137-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a4137-137">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="a4137-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a4137-138">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a4137-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a4137-139">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a4137-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a4137-140">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a4137-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a4137-141">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a4137-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a4137-142">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a4137-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a4137-143">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a4137-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a4137-144">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a4137-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a4137-145">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a4137-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a4137-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a4137-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a4137-147">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="a4137-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a4137-148">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4137-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a4137-149">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="a4137-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a4137-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a4137-150">AzureRM.Resources</span></span>
* <span data-ttu-id="a4137-151">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="a4137-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a4137-152">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="a4137-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a4137-153">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="a4137-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a4137-154">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="a4137-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a4137-155">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a4137-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a4137-156">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="a4137-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a4137-157">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="a4137-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a4137-158">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a4137-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a4137-159">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="a4137-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a4137-160">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="a4137-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a4137-161">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4137-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a4137-162">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a4137-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a4137-163">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="a4137-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a4137-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a4137-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a4137-165">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a4137-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a4137-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a4137-166">AzureRM.Sql</span></span>
* <span data-ttu-id="a4137-167">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a4137-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a4137-168">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="a4137-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a4137-169">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="a4137-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a4137-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a4137-170">AzureRM.Profile</span></span>
* <span data-ttu-id="a4137-171">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="a4137-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a4137-172">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="a4137-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a4137-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a4137-173">Azure.Storage</span></span>
* <span data-ttu-id="a4137-174">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="a4137-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a4137-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a4137-175">AzureRM.Compute</span></span>
* <span data-ttu-id="a4137-176">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="a4137-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a4137-177">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="a4137-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a4137-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a4137-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a4137-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a4137-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a4137-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a4137-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a4137-181">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="a4137-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a4137-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4137-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a4137-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4137-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a4137-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4137-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a4137-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4137-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a4137-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="a4137-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a4137-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a4137-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a4137-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a4137-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a4137-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a4137-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a4137-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a4137-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a4137-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a4137-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a4137-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a4137-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a4137-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a4137-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a4137-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a4137-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a4137-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a4137-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a4137-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a4137-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a4137-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a4137-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a4137-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a4137-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a4137-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a4137-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a4137-202">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a4137-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a4137-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a4137-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a4137-204">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="a4137-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a4137-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a4137-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a4137-206">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="a4137-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a4137-207">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="a4137-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a4137-208">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="a4137-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a4137-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a4137-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a4137-210">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="a4137-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a4137-211">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="a4137-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a4137-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a4137-212">AzureRM.Sql</span></span>
* <span data-ttu-id="a4137-213">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="a4137-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a4137-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a4137-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a4137-215">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a4137-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a4137-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a4137-216">AzureRM.Websites</span></span>
* <span data-ttu-id="a4137-217">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a4137-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a4137-218">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a4137-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a4137-219">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="a4137-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a4137-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a4137-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a4137-221">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="a4137-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a4137-222">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="a4137-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a4137-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a4137-223">AzureRM.Profile</span></span>
* <span data-ttu-id="a4137-224">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="a4137-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a4137-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a4137-225">AzureRM.Compute</span></span>
* <span data-ttu-id="a4137-226">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="a4137-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a4137-227">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="a4137-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a4137-228">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a4137-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a4137-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a4137-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a4137-230">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4137-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a4137-231">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="a4137-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a4137-232">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="a4137-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a4137-233">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="a4137-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a4137-234">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="a4137-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a4137-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a4137-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a4137-236">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="a4137-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a4137-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a4137-237">AzureRM.Network</span></span>
* <span data-ttu-id="a4137-238">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="a4137-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a4137-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a4137-239">AzureRM.Resources</span></span>
* <span data-ttu-id="a4137-240">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="a4137-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a4137-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a4137-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a4137-242">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="a4137-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a4137-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a4137-243">AzureRM.Sql</span></span>
* <span data-ttu-id="a4137-244">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="a4137-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a4137-245">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4137-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a4137-246">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a4137-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a4137-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a4137-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a4137-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a4137-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a4137-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4137-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a4137-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a4137-250">AzureRM.Websites</span></span>
* <span data-ttu-id="a4137-251">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="a4137-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a4137-252">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="a4137-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a4137-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="a4137-253">AzureRM.Profile</span></span>
* <span data-ttu-id="a4137-254">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="a4137-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a4137-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a4137-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a4137-256">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="a4137-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a4137-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a4137-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a4137-258">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="a4137-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a4137-259">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a4137-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a4137-260">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="a4137-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a4137-261">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="a4137-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a4137-262">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="a4137-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a4137-263">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="a4137-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a4137-264">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="a4137-264">Added support for MSI identity</span></span>
* <span data-ttu-id="a4137-265">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="a4137-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a4137-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a4137-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a4137-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4137-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a4137-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a4137-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a4137-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a4137-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a4137-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a4137-270">AzureRM.Batch</span></span>
* <span data-ttu-id="a4137-271">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="a4137-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a4137-272">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="a4137-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a4137-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a4137-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="a4137-274">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="a4137-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a4137-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a4137-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a4137-276">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="a4137-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a4137-277">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a4137-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a4137-278">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a4137-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a4137-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a4137-279">AzureRM.Network</span></span>
* <span data-ttu-id="a4137-280">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="a4137-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a4137-281">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="a4137-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a4137-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4137-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a4137-283">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="a4137-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a4137-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a4137-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a4137-285">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="a4137-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a4137-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a4137-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a4137-287">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="a4137-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a4137-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a4137-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a4137-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a4137-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a4137-290">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="a4137-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a4137-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a4137-291">AzureRM.Sql</span></span>
* <span data-ttu-id="a4137-292">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="a4137-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a4137-293">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="a4137-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a4137-294">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="a4137-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a4137-295">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="a4137-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a4137-296">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="a4137-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a4137-297">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4137-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a4137-298">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a4137-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a4137-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a4137-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a4137-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a4137-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a4137-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4137-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a4137-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a4137-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a4137-303">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="a4137-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>