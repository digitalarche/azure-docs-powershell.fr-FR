---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342018"
---
## <a name="110---january-2019"></a><span data-ttu-id="3c280-101">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="3c280-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3c280-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3c280-102">Az.Accounts</span></span>
* <span data-ttu-id="3c280-103">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="3c280-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3c280-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3c280-104">Az.Compute</span></span>
* <span data-ttu-id="3c280-105">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3c280-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3c280-106">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="3c280-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3c280-107">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3c280-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3c280-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c280-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="3c280-109">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="3c280-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3c280-110">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="3c280-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3c280-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3c280-111">Az.EventGrid</span></span>
* <span data-ttu-id="3c280-112">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="3c280-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3c280-113">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="3c280-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3c280-114">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="3c280-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3c280-115">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="3c280-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3c280-116">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="3c280-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3c280-117">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="3c280-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3c280-118">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="3c280-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3c280-119">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="3c280-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3c280-120">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="3c280-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3c280-121">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="3c280-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="3c280-122">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="3c280-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3c280-123">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c280-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3c280-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3c280-124">Az.IotHub</span></span>
* <span data-ttu-id="3c280-125">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="3c280-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3c280-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3c280-126">Az.LogicApp</span></span>
* <span data-ttu-id="3c280-127">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="3c280-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3c280-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-128">Az.Resources</span></span>
* <span data-ttu-id="3c280-129">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="3c280-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3c280-130">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3c280-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3c280-131">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3c280-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3c280-132">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3c280-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3c280-133">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="3c280-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3c280-134">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3c280-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3c280-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3c280-135">Az.SignalR</span></span>
* <span data-ttu-id="3c280-136">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3c280-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3c280-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3c280-137">Az.Sql</span></span>
* <span data-ttu-id="3c280-138">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="3c280-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3c280-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3c280-139">Az.Storage</span></span>
* <span data-ttu-id="3c280-140">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="3c280-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3c280-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c280-141">New-AzStorageContext</span></span>
* <span data-ttu-id="3c280-142">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="3c280-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3c280-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3c280-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3c280-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3c280-144">Az.Websites</span></span>
* <span data-ttu-id="3c280-145">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3c280-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3c280-146">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3c280-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3c280-147">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3c280-148">Généralités</span><span class="sxs-lookup"><span data-stu-id="3c280-148">General</span></span>

- <span data-ttu-id="3c280-149">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="3c280-149">General Availability of Az Module</span></span>
- <span data-ttu-id="3c280-150">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="3c280-150">Online help for each module</span></span>
- <span data-ttu-id="3c280-151">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="3c280-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3c280-152">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="3c280-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3c280-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3c280-153">Az.Accounts</span></span>
- <span data-ttu-id="3c280-154">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3c280-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="3c280-155">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="3c280-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3c280-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c280-156">Az.ApiManagement</span></span>
- <span data-ttu-id="3c280-157">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="3c280-157">Fixes for #7002</span></span>
- <span data-ttu-id="3c280-158">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3c280-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3c280-159">Az.Batch</span></span>
- <span data-ttu-id="3c280-160">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="3c280-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3c280-161">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="3c280-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3c280-162">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3c280-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3c280-163">Az.Billing</span></span>
- <span data-ttu-id="3c280-164">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3c280-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3c280-165">Az.CognitivServices</span></span>
- <span data-ttu-id="3c280-166">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3c280-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3c280-167">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="3c280-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3c280-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3c280-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="3c280-169">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="3c280-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3c280-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3c280-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3c280-171">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3c280-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c280-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="3c280-173">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3c280-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3c280-174">Az.Monitor</span></span>
- <span data-ttu-id="3c280-175">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3c280-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3c280-176">Az.KeyVault</span></span>
- <span data-ttu-id="3c280-177">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="3c280-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3c280-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3c280-178">Az.MachineLearning</span></span>
- <span data-ttu-id="3c280-179">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="3c280-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3c280-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3c280-180">Az.Media</span></span>
- <span data-ttu-id="3c280-181">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3c280-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3c280-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3c280-182">Az.Network</span></span>
<span data-ttu-id="3c280-183">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3c280-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3c280-184">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="3c280-184">New cmdlets added:</span></span>
        - <span data-ttu-id="3c280-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c280-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3c280-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c280-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3c280-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c280-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3c280-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c280-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3c280-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c280-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3c280-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3c280-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3c280-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3c280-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3c280-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c280-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3c280-193">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3c280-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3c280-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c280-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3c280-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3c280-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3c280-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3c280-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3c280-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3c280-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3c280-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3c280-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3c280-199">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="3c280-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3c280-200">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3c280-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3c280-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3c280-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3c280-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3c280-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3c280-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3c280-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3c280-204">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3c280-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3c280-205">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3c280-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3c280-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="3c280-207">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3c280-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3c280-208">Az.Profile</span></span>
- <span data-ttu-id="3c280-209">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3c280-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3c280-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3c280-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="3c280-211">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3c280-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-212">Az.Resources</span></span>
- <span data-ttu-id="3c280-213">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3c280-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c280-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="3c280-215">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="3c280-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3c280-216">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3c280-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3c280-217">Az.SIgnalR</span></span>
- <span data-ttu-id="3c280-218">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3c280-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3c280-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3c280-219">Az.Sql</span></span>
- <span data-ttu-id="3c280-220">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="3c280-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3c280-221">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="3c280-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3c280-222">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3c280-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3c280-223">Az.Storage</span></span>
- <span data-ttu-id="3c280-224">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3c280-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3c280-225">Az.Websites</span></span>
- <span data-ttu-id="3c280-226">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="3c280-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3c280-227">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3c280-228">Généralités</span><span class="sxs-lookup"><span data-stu-id="3c280-228">General</span></span>

* <span data-ttu-id="3c280-229">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="3c280-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3c280-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3c280-230">Az.Compute</span></span>

* <span data-ttu-id="3c280-231">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="3c280-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3c280-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c280-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="3c280-233">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="3c280-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3c280-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3c280-234">Az.FrontDoor</span></span>

* <span data-ttu-id="3c280-235">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="3c280-235">Fixed some broken links</span></span>
    - <span data-ttu-id="3c280-236">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="3c280-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3c280-237">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="3c280-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3c280-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3c280-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="3c280-239">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="3c280-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3c280-240">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="3c280-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3c280-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-241">Az.Resources</span></span>

* <span data-ttu-id="3c280-242">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="3c280-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3c280-243">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="3c280-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3c280-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3c280-244">Az.Sql</span></span>

* <span data-ttu-id="3c280-245">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="3c280-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3c280-246">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="3c280-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3c280-247">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="3c280-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3c280-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3c280-248">Az.Storage</span></span>

* <span data-ttu-id="3c280-249">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c280-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3c280-250">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="3c280-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3c280-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3c280-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3c280-252">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="3c280-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="3c280-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3c280-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3c280-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3c280-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3c280-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3c280-255">Az.Websites</span></span>

* <span data-ttu-id="3c280-256">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3c280-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="3c280-257">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="3c280-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3c280-258">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="3c280-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3c280-259">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3c280-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c280-260">Az.ApiManagement</span></span>
* <span data-ttu-id="3c280-261">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="3c280-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3c280-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3c280-262">Az.Automation</span></span>
* <span data-ttu-id="3c280-263">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="3c280-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3c280-264">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="3c280-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3c280-265">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="3c280-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3c280-266">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="3c280-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3c280-267">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="3c280-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3c280-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3c280-268">Az.Compute</span></span>
* <span data-ttu-id="3c280-269">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="3c280-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3c280-270">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="3c280-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3c280-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3c280-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="3c280-272">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="3c280-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3c280-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3c280-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3c280-274">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="3c280-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3c280-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3c280-275">Az.Network</span></span>
* <span data-ttu-id="3c280-276">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3c280-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3c280-277">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c280-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3c280-278">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="3c280-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="3c280-279">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3c280-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3c280-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3c280-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3c280-281">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="3c280-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3c280-282">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="3c280-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3c280-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3c280-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3c280-284">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3c280-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3c280-285">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="3c280-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3c280-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3c280-286">Az.Relay</span></span>
* <span data-ttu-id="3c280-287">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="3c280-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3c280-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-288">Az.Resources</span></span>
* <span data-ttu-id="3c280-289">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="3c280-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3c280-290">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="3c280-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3c280-291">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="3c280-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3c280-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c280-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="3c280-293">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="3c280-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3c280-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3c280-294">Az.Sql</span></span>
* <span data-ttu-id="3c280-295">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="3c280-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3c280-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3c280-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3c280-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3c280-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3c280-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3c280-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3c280-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3c280-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3c280-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3c280-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3c280-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3c280-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3c280-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3c280-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3c280-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3c280-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3c280-304">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="3c280-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3c280-305">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="3c280-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3c280-306">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="3c280-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3c280-307">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3c280-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3c280-308">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3c280-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3c280-309">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3c280-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3c280-310">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3c280-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3c280-311">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="3c280-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3c280-312">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3c280-313">Généralités</span><span class="sxs-lookup"><span data-stu-id="3c280-313">General</span></span>
* <span data-ttu-id="3c280-314">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="3c280-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3c280-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3c280-315">Az.Profile</span></span>
* <span data-ttu-id="3c280-316">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3c280-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3c280-317">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="3c280-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3c280-318">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="3c280-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3c280-319">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="3c280-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3c280-320">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="3c280-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3c280-321">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="3c280-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3c280-322">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="3c280-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3c280-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3c280-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="3c280-324">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="3c280-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3c280-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3c280-325">Az.Compute</span></span>
* <span data-ttu-id="3c280-326">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3c280-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3c280-327">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="3c280-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3c280-328">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="3c280-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3c280-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c280-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="3c280-330">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="3c280-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3c280-331">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="3c280-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3c280-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3c280-332">Az.Insights</span></span>
* <span data-ttu-id="3c280-333">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="3c280-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3c280-334">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="3c280-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3c280-335">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="3c280-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3c280-336">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="3c280-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3c280-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3c280-337">Az.Network</span></span>
* <span data-ttu-id="3c280-338">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="3c280-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3c280-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c280-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3c280-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3c280-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3c280-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3c280-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3c280-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3c280-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3c280-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3c280-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3c280-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3c280-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3c280-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3c280-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="3c280-346">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="3c280-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3c280-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-347">Az.Resources</span></span>
* <span data-ttu-id="3c280-348">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="3c280-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3c280-349">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="3c280-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3c280-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3c280-350">Az.ServiceBus</span></span>
* <span data-ttu-id="3c280-351">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="3c280-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3c280-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3c280-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="3c280-353">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="3c280-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3c280-354">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="3c280-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3c280-355">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3c280-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3c280-356">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3c280-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3c280-357">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="3c280-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3c280-358">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3c280-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3c280-359">Az.Profile</span></span>
* <span data-ttu-id="3c280-360">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="3c280-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3c280-361">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3c280-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3c280-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3c280-362">Az.Compute</span></span>
* <span data-ttu-id="3c280-363">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="3c280-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3c280-364">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="3c280-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3c280-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3c280-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="3c280-366">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="3c280-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3c280-367">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c280-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3c280-368">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="3c280-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3c280-369">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="3c280-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3c280-370">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3c280-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3c280-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3c280-371">Az.Network</span></span>
* <span data-ttu-id="3c280-372">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="3c280-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3c280-373">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="3c280-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3c280-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-374">Az.Resources</span></span>
* <span data-ttu-id="3c280-375">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="3c280-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3c280-376">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="3c280-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3c280-377">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3c280-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3c280-378">Azure.Storage</span></span>
* <span data-ttu-id="3c280-379">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3c280-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3c280-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3c280-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3c280-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3c280-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3c280-382">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="3c280-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3c280-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3c280-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="3c280-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3c280-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="3c280-385">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="3c280-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3c280-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3c280-386">Az.Compute</span></span>
* <span data-ttu-id="3c280-387">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="3c280-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3c280-388">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="3c280-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3c280-389">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="3c280-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3c280-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3c280-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3c280-391">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="3c280-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3c280-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3c280-392">Az.Network</span></span>
* <span data-ttu-id="3c280-393">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="3c280-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3c280-394">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="3c280-394">new cmdlets added</span></span>
    - <span data-ttu-id="3c280-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c280-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3c280-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c280-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3c280-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c280-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3c280-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3c280-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3c280-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3c280-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3c280-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3c280-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3c280-401">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="3c280-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3c280-402">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3c280-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3c280-403">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3c280-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3c280-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3c280-404">Az.RedisCache</span></span>
* <span data-ttu-id="3c280-405">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="3c280-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3c280-406">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="3c280-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3c280-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3c280-407">Az.Resources</span></span>
* <span data-ttu-id="3c280-408">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3c280-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3c280-409">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="3c280-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3c280-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3c280-410">Az.Sql</span></span>
* <span data-ttu-id="3c280-411">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="3c280-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3c280-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3c280-412">Az.Websites</span></span>
* <span data-ttu-id="3c280-413">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="3c280-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3c280-414">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="3c280-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3c280-415">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="3c280-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3c280-416">Version initiale</span><span class="sxs-lookup"><span data-stu-id="3c280-416">Initial Release</span></span>