---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912001"
---
# <a name="release-notes"></a><span data-ttu-id="7f1b4-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="7f1b4-103">Release notes</span></span>

<span data-ttu-id="7f1b4-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="7f1b4-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="7f1b4-105">6.0.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="7f1b4-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="7f1b4-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="7f1b4-106">General</span></span>
* <span data-ttu-id="7f1b4-107">Configurer la dépendance minimale des modules sur PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="7f1b4-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="7f1b4-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7f1b4-108">Azure.Storage</span></span>
* <span data-ttu-id="7f1b4-109">Support comme nom du conteneur d’objets blob du stockage Azure</span><span class="sxs-lookup"><span data-stu-id="7f1b4-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="7f1b4-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7f1b4-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="7f1b4-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7f1b4-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="7f1b4-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7f1b4-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="7f1b4-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7f1b4-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="7f1b4-114">Corrige le fait qu’une sortie d’échec d’applets de commande de stockage ne contient pas les informations détaillées de l’échec</span><span class="sxs-lookup"><span data-stu-id="7f1b4-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="7f1b4-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7f1b4-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="7f1b4-116">Introduit plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-117">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="7f1b4-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="7f1b4-118">AzureRM.Automation</span></span>
* <span data-ttu-id="7f1b4-119">Retrait des alias des « balises » déconseillées des applets de commande</span><span class="sxs-lookup"><span data-stu-id="7f1b4-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="7f1b4-120">'Set-AzureRmAutomationRunbook'</span><span class="sxs-lookup"><span data-stu-id="7f1b4-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="7f1b4-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="7f1b4-121">AzureRM.Batch</span></span>
* <span data-ttu-id="7f1b4-122">Mise à jour de la documentation sur New-AzureBatchPool pour supprimer l’exemple déconseillé</span><span class="sxs-lookup"><span data-stu-id="7f1b4-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="7f1b4-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="7f1b4-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="7f1b4-124">Introduit plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-125">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="7f1b4-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7f1b4-126">AzureRM.Compute</span></span>
* <span data-ttu-id="7f1b4-127">« New-AzureRmVm » et « New-AzureRmVmss » prennent en charge la sortie détaillée des paramètres</span><span class="sxs-lookup"><span data-stu-id="7f1b4-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="7f1b4-128">« New-AzureRmVm » et « New-AzureRmVmss » (ensemble de paramètres simples) prennent en charge l’attribution d’identités définies par le système et/ou d’identités définies par l’utilisateur pour les machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="7f1b4-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="7f1b4-129">Fonction Redeploy et PerformMaintenance de VMSS</span><span class="sxs-lookup"><span data-stu-id="7f1b4-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="7f1b4-130">Ajoute un nouveau paramètre de commutateur-Redeploy et -PerformMaintenance à « Set-AzureRmVmss » et « Set-AzureRmVmssVM »</span><span class="sxs-lookup"><span data-stu-id="7f1b4-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="7f1b4-131">Ajoute un paramètre de commutateur DisableVMAgent à l’applet de commande « Set-AzureRmVMOperatingSystem »</span><span class="sxs-lookup"><span data-stu-id="7f1b4-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="7f1b4-132">« New-AzureRmVm » et « New-AzureRmVmss » (ensemble de paramètres simples) prennent en charge une image « Win10 ».</span><span class="sxs-lookup"><span data-stu-id="7f1b4-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="7f1b4-133">L’applet de commande « Repair-AzureRmVmssServiceFabricUpdateDomain » est ajouté.</span><span class="sxs-lookup"><span data-stu-id="7f1b4-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="7f1b4-134">Introduit plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-135">Pour plus de détails, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="7f1b4-136">« Set-AzureRmVmDiskEncryptionExtension » rend les paramètres AAD facultatifs</span><span class="sxs-lookup"><span data-stu-id="7f1b4-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="7f1b4-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="7f1b4-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="7f1b4-138">Retrait des alias des « balises » déconseillées des applets de commande</span><span class="sxs-lookup"><span data-stu-id="7f1b4-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="7f1b4-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="7f1b4-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7f1b4-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7f1b4-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7f1b4-141">La mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.7.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f1b4-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="7f1b4-142">Ajout des paramètres d’exécution et de la propriété des gestionnaires de connexion sur l’activité ExecuteSSISPackage</span><span class="sxs-lookup"><span data-stu-id="7f1b4-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="7f1b4-143">Mise à jour du service lié PostgreSql et MySql pour utiliser une chaîne de connexion complète au lieu d’un serveur, d’une base de données, d’un schéma, d’un nom d’utilisateur et d’un mot de passe</span><span class="sxs-lookup"><span data-stu-id="7f1b4-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="7f1b4-144">Retrait du schéma du service lié D2B</span><span class="sxs-lookup"><span data-stu-id="7f1b4-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="7f1b4-145">Retrait de la propriété du schéma du service lié Teradata</span><span class="sxs-lookup"><span data-stu-id="7f1b4-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="7f1b4-146">Ajout de service lié, jeu de données, copie source pour Responsys</span><span class="sxs-lookup"><span data-stu-id="7f1b4-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="7f1b4-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7f1b4-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="7f1b4-148">Retrait des alias des « balises » déconseillées des applets de commande</span><span class="sxs-lookup"><span data-stu-id="7f1b4-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="7f1b4-149">«New-AzureRmDataLakeAnalyticsAccount»</span><span class="sxs-lookup"><span data-stu-id="7f1b4-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="7f1b4-150">«Set-AzureRmDataLakeAnalyticsAccount»</span><span class="sxs-lookup"><span data-stu-id="7f1b4-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="7f1b4-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7f1b4-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7f1b4-152">Ajout d’une nouvelle fonctionnalité de changements ACL récursifs à Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="7f1b4-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="7f1b4-153">Ajout d’un nouvel applet de commande pour la récupération du résumé du contenu dans un répertoire</span><span class="sxs-lookup"><span data-stu-id="7f1b4-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="7f1b4-154">Ajout d’un nouvel applet de commande pour récupérer le vidage des ACL et l’utilisation du disque</span><span class="sxs-lookup"><span data-stu-id="7f1b4-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="7f1b4-155">Type de retour correct de Set-AzureRmDataLakeStoreItemAcl bool sur IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="7f1b4-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="7f1b4-156">Type de retour correct de Set-AzureRmDataLakeStoreItemAclEntry bool sur IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="7f1b4-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="7f1b4-157">Changements cassant dans Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f1b4-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="7f1b4-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="7f1b4-158">AzureRM.Dns</span></span>
* <span data-ttu-id="7f1b4-159">Introduit plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-160">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="7f1b4-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="7f1b4-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="7f1b4-162">Mise à jour de l’aide pour les applets de commande ayant des exemples manquants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="7f1b4-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="7f1b4-163">AzureRM.Insights</span></span>
* <span data-ttu-id="7f1b4-164">Introduction de plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-165">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="7f1b4-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="7f1b4-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="7f1b4-167">Activation des balises et de la référence SKU de base sur IotHub</span><span class="sxs-lookup"><span data-stu-id="7f1b4-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="7f1b4-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7f1b4-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7f1b4-169">Changements cassants pour la prise en charge des scénarios de redirection</span><span class="sxs-lookup"><span data-stu-id="7f1b4-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="7f1b4-170">Ajout de nouveaux applets de commande : Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, et Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="7f1b4-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="7f1b4-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7f1b4-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="7f1b4-172">Retrait des alias des « balises » déconseillées des applets de commande</span><span class="sxs-lookup"><span data-stu-id="7f1b4-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="7f1b4-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7f1b4-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="7f1b4-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="7f1b4-174">AzureRM.Media</span></span>
* <span data-ttu-id="7f1b4-175">Retrait des alias des « balises » déconseillées des applets de commande</span><span class="sxs-lookup"><span data-stu-id="7f1b4-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="7f1b4-176">«Set-AzureRmMediaService»</span><span class="sxs-lookup"><span data-stu-id="7f1b4-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="7f1b4-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7f1b4-177">AzureRM.Network</span></span>
* <span data-ttu-id="7f1b4-178">Ajout de la prise en charge de la ressource de plan de protection DDoS</span><span class="sxs-lookup"><span data-stu-id="7f1b4-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="7f1b4-179">Introduction de plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-180">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="7f1b4-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7f1b4-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="7f1b4-182">Introduit plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-183">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="7f1b4-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7f1b4-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="7f1b4-185">Introduit plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-186">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="7f1b4-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7f1b4-187">AzureRM.Profile</span></span>
* <span data-ttu-id="7f1b4-188">Activation par défaut de l’enregistrement automatique du contexte</span><span class="sxs-lookup"><span data-stu-id="7f1b4-188">Enable context autosave by default</span></span>
* <span data-ttu-id="7f1b4-189">Ajout des propriétés Add USGovernmentOperationalInsightsEndpoint et USGovernmentOperationalInsightsEndpointResourceId à l’environnement Azure pour le gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="7f1b4-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="7f1b4-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7f1b4-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7f1b4-191">En-tête d’authentification corrigé dans les scénarios SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7f1b4-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="7f1b4-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7f1b4-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="7f1b4-193">Introduction de plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-194">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="7f1b4-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7f1b4-195">AzureRM.Resources</span></span>
* <span data-ttu-id="7f1b4-196">Suppression d’un paramètre obsolète -AtScopeAndBelow à partir de l’appel Get-AzureRmRoledefinition</span><span class="sxs-lookup"><span data-stu-id="7f1b4-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="7f1b4-197">Affectations incluses aux utilisateurs/groupes/principaux de service supprimés dans les résultats de Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7f1b4-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="7f1b4-198">Ajout des compléments d’onglet pour Scope et ResourceType</span><span class="sxs-lookup"><span data-stu-id="7f1b4-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="7f1b4-199">Ajout d’un applet de commande de commodité pour la création des principaux de service</span><span class="sxs-lookup"><span data-stu-id="7f1b4-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="7f1b4-200">Fusion des fonctionnalités Get - et Find- dans Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="7f1b4-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="7f1b4-201">Ajout des applets de commande AD :</span><span class="sxs-lookup"><span data-stu-id="7f1b4-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="7f1b4-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="7f1b4-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="7f1b4-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="7f1b4-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="7f1b4-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="7f1b4-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="7f1b4-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="7f1b4-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="7f1b4-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7f1b4-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="7f1b4-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7f1b4-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="7f1b4-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7f1b4-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="7f1b4-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7f1b4-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="7f1b4-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7f1b4-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="7f1b4-211">Mise à jour de la référence SKU par défaut de la version de l’image Linux</span><span class="sxs-lookup"><span data-stu-id="7f1b4-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="7f1b4-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span><span class="sxs-lookup"><span data-stu-id="7f1b4-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="7f1b4-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="7f1b4-213">AzureRM.Storage</span></span>
* <span data-ttu-id="7f1b4-214">Introduction de plusieurs changements cassants</span><span class="sxs-lookup"><span data-stu-id="7f1b4-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="7f1b4-215">Pour plus d’informations, reportez-vous au guide de migration</span><span class="sxs-lookup"><span data-stu-id="7f1b4-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="7f1b4-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7f1b4-216">AzureRM.Websites</span></span>
* <span data-ttu-id="7f1b4-217">Mise à jour vers la dernière version du Kit de développement logiciel des sites web</span><span class="sxs-lookup"><span data-stu-id="7f1b4-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="7f1b4-218">Ajout des propriétés -AssignIdentity et -Httpsonly pour Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7f1b4-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="7f1b4-219">Ajout de deux nouveaux applets de commande : Get-AzureRmWebAppSnapshots et Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7f1b4-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
