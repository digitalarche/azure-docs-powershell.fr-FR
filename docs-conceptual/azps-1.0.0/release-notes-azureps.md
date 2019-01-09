## <a name="100---december-2018"></a><span data-ttu-id="b25a5-101">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b25a5-102">Généralités</span><span class="sxs-lookup"><span data-stu-id="b25a5-102">General</span></span>

- <span data-ttu-id="b25a5-103">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="b25a5-103">General Availability of Az Module</span></span>
- <span data-ttu-id="b25a5-104">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="b25a5-104">Online help for each module</span></span>
- <span data-ttu-id="b25a5-105">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b25a5-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b25a5-106">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="b25a5-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b25a5-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b25a5-107">Az.Accounts</span></span>
- <span data-ttu-id="b25a5-108">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b25a5-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="b25a5-109">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="b25a5-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b25a5-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b25a5-110">Az.ApiManagement</span></span>
- <span data-ttu-id="b25a5-111">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="b25a5-111">Fixes for #7002</span></span>
- <span data-ttu-id="b25a5-112">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b25a5-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b25a5-113">Az.Batch</span></span>
- <span data-ttu-id="b25a5-114">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b25a5-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b25a5-115">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="b25a5-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b25a5-116">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b25a5-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b25a5-117">Az.Billing</span></span>
- <span data-ttu-id="b25a5-118">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b25a5-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b25a5-119">Az.CognitivServices</span></span>
- <span data-ttu-id="b25a5-120">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b25a5-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b25a5-121">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b25a5-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b25a5-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b25a5-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="b25a5-123">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b25a5-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b25a5-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b25a5-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b25a5-125">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b25a5-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b25a5-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="b25a5-127">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b25a5-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b25a5-128">Az.Monitor</span></span>
- <span data-ttu-id="b25a5-129">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b25a5-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b25a5-130">Az.KeyVault</span></span>
- <span data-ttu-id="b25a5-131">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="b25a5-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b25a5-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b25a5-132">Az.MachineLearning</span></span>
- <span data-ttu-id="b25a5-133">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b25a5-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b25a5-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b25a5-134">Az.Media</span></span>
- <span data-ttu-id="b25a5-135">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b25a5-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b25a5-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b25a5-136">Az.Network</span></span>
<span data-ttu-id="b25a5-137">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b25a5-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b25a5-138">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="b25a5-138">New cmdlets added:</span></span>
        - <span data-ttu-id="b25a5-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b25a5-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b25a5-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b25a5-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b25a5-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b25a5-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b25a5-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b25a5-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b25a5-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b25a5-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b25a5-147">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b25a5-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b25a5-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b25a5-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b25a5-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b25a5-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b25a5-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b25a5-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b25a5-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b25a5-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b25a5-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b25a5-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b25a5-153">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="b25a5-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b25a5-154">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b25a5-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b25a5-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b25a5-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b25a5-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b25a5-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b25a5-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b25a5-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b25a5-158">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b25a5-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b25a5-159">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b25a5-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b25a5-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="b25a5-161">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b25a5-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b25a5-162">Az.Profile</span></span>
- <span data-ttu-id="b25a5-163">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b25a5-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b25a5-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b25a5-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="b25a5-165">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b25a5-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b25a5-166">Az.Resources</span></span>
- <span data-ttu-id="b25a5-167">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b25a5-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b25a5-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="b25a5-169">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="b25a5-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b25a5-170">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b25a5-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b25a5-171">Az.SIgnalR</span></span>
- <span data-ttu-id="b25a5-172">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b25a5-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b25a5-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b25a5-173">Az.Sql</span></span>
- <span data-ttu-id="b25a5-174">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="b25a5-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b25a5-175">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="b25a5-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b25a5-176">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b25a5-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b25a5-177">Az.Storage</span></span>
- <span data-ttu-id="b25a5-178">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b25a5-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b25a5-179">Az.Websites</span></span>
- <span data-ttu-id="b25a5-180">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b25a5-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b25a5-181">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b25a5-182">Généralités</span><span class="sxs-lookup"><span data-stu-id="b25a5-182">General</span></span>

* <span data-ttu-id="b25a5-183">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="b25a5-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b25a5-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b25a5-184">Az.Compute</span></span>

* <span data-ttu-id="b25a5-185">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="b25a5-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b25a5-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b25a5-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="b25a5-187">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="b25a5-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b25a5-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b25a5-188">Az.FrontDoor</span></span>

* <span data-ttu-id="b25a5-189">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="b25a5-189">Fixed some broken links</span></span>
    - <span data-ttu-id="b25a5-190">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b25a5-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b25a5-191">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b25a5-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b25a5-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b25a5-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="b25a5-193">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="b25a5-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b25a5-194">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="b25a5-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b25a5-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b25a5-195">Az.Resources</span></span>

* <span data-ttu-id="b25a5-196">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b25a5-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b25a5-197">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="b25a5-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b25a5-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b25a5-198">Az.Sql</span></span>

* <span data-ttu-id="b25a5-199">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="b25a5-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b25a5-200">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="b25a5-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b25a5-201">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="b25a5-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b25a5-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b25a5-202">Az.Storage</span></span>

* <span data-ttu-id="b25a5-203">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b25a5-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b25a5-204">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="b25a5-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b25a5-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b25a5-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b25a5-206">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="b25a5-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="b25a5-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b25a5-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b25a5-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b25a5-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b25a5-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b25a5-209">Az.Websites</span></span>

* <span data-ttu-id="b25a5-210">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b25a5-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b25a5-211">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="b25a5-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b25a5-212">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="b25a5-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b25a5-213">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b25a5-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b25a5-214">Az.ApiManagement</span></span>
* <span data-ttu-id="b25a5-215">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b25a5-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b25a5-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b25a5-216">Az.Automation</span></span>
* <span data-ttu-id="b25a5-217">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="b25a5-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b25a5-218">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="b25a5-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b25a5-219">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="b25a5-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b25a5-220">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="b25a5-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b25a5-221">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="b25a5-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b25a5-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b25a5-222">Az.Compute</span></span>
* <span data-ttu-id="b25a5-223">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b25a5-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b25a5-224">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b25a5-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b25a5-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b25a5-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="b25a5-226">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b25a5-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b25a5-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b25a5-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b25a5-228">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="b25a5-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b25a5-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b25a5-229">Az.Network</span></span>
* <span data-ttu-id="b25a5-230">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b25a5-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b25a5-231">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="b25a5-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b25a5-232">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="b25a5-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b25a5-233">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b25a5-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b25a5-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b25a5-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b25a5-235">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="b25a5-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b25a5-236">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="b25a5-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b25a5-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b25a5-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b25a5-238">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b25a5-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b25a5-239">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b25a5-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b25a5-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b25a5-240">Az.Relay</span></span>
* <span data-ttu-id="b25a5-241">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b25a5-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b25a5-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b25a5-242">Az.Resources</span></span>
* <span data-ttu-id="b25a5-243">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="b25a5-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b25a5-244">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="b25a5-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b25a5-245">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="b25a5-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b25a5-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b25a5-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="b25a5-247">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="b25a5-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b25a5-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b25a5-248">Az.Sql</span></span>
* <span data-ttu-id="b25a5-249">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="b25a5-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b25a5-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b25a5-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b25a5-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b25a5-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b25a5-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b25a5-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b25a5-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b25a5-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b25a5-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b25a5-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b25a5-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b25a5-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b25a5-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b25a5-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b25a5-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b25a5-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b25a5-258">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="b25a5-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b25a5-259">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="b25a5-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b25a5-260">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="b25a5-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b25a5-261">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b25a5-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b25a5-262">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b25a5-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b25a5-263">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b25a5-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b25a5-264">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b25a5-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b25a5-265">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="b25a5-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b25a5-266">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b25a5-267">Généralités</span><span class="sxs-lookup"><span data-stu-id="b25a5-267">General</span></span>
* <span data-ttu-id="b25a5-268">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="b25a5-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b25a5-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b25a5-269">Az.Profile</span></span>
* <span data-ttu-id="b25a5-270">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b25a5-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b25a5-271">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="b25a5-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b25a5-272">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b25a5-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b25a5-273">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="b25a5-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b25a5-274">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="b25a5-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b25a5-275">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="b25a5-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b25a5-276">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="b25a5-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b25a5-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b25a5-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="b25a5-278">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b25a5-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b25a5-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b25a5-279">Az.Compute</span></span>
* <span data-ttu-id="b25a5-280">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b25a5-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b25a5-281">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b25a5-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b25a5-282">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="b25a5-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b25a5-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b25a5-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="b25a5-284">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b25a5-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b25a5-285">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="b25a5-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b25a5-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b25a5-286">Az.Insights</span></span>
* <span data-ttu-id="b25a5-287">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="b25a5-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b25a5-288">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="b25a5-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b25a5-289">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="b25a5-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b25a5-290">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="b25a5-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b25a5-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b25a5-291">Az.Network</span></span>
* <span data-ttu-id="b25a5-292">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="b25a5-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b25a5-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b25a5-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b25a5-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b25a5-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b25a5-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b25a5-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b25a5-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b25a5-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b25a5-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b25a5-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b25a5-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b25a5-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b25a5-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b25a5-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="b25a5-300">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="b25a5-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b25a5-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b25a5-301">Az.Resources</span></span>
* <span data-ttu-id="b25a5-302">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b25a5-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b25a5-303">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="b25a5-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b25a5-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b25a5-304">Az.ServiceBus</span></span>
* <span data-ttu-id="b25a5-305">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="b25a5-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b25a5-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b25a5-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="b25a5-307">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="b25a5-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b25a5-308">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="b25a5-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b25a5-309">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b25a5-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b25a5-310">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b25a5-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b25a5-311">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="b25a5-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b25a5-312">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b25a5-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b25a5-313">Az.Profile</span></span>
* <span data-ttu-id="b25a5-314">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="b25a5-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b25a5-315">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b25a5-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b25a5-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b25a5-316">Az.Compute</span></span>
* <span data-ttu-id="b25a5-317">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="b25a5-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b25a5-318">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="b25a5-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b25a5-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b25a5-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="b25a5-320">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="b25a5-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b25a5-321">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b25a5-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b25a5-322">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="b25a5-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b25a5-323">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="b25a5-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b25a5-324">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b25a5-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b25a5-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b25a5-325">Az.Network</span></span>
* <span data-ttu-id="b25a5-326">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="b25a5-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b25a5-327">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="b25a5-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b25a5-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b25a5-328">Az.Resources</span></span>
* <span data-ttu-id="b25a5-329">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="b25a5-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b25a5-330">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="b25a5-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b25a5-331">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b25a5-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b25a5-332">Azure.Storage</span></span>
* <span data-ttu-id="b25a5-333">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="b25a5-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b25a5-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b25a5-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b25a5-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b25a5-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b25a5-336">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="b25a5-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b25a5-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b25a5-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b25a5-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b25a5-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="b25a5-339">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="b25a5-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b25a5-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b25a5-340">Az.Compute</span></span>
* <span data-ttu-id="b25a5-341">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="b25a5-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b25a5-342">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b25a5-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b25a5-343">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="b25a5-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b25a5-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b25a5-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b25a5-345">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b25a5-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b25a5-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b25a5-346">Az.Network</span></span>
* <span data-ttu-id="b25a5-347">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="b25a5-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b25a5-348">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="b25a5-348">new cmdlets added</span></span>
    - <span data-ttu-id="b25a5-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b25a5-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b25a5-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b25a5-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b25a5-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b25a5-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b25a5-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b25a5-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b25a5-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b25a5-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b25a5-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b25a5-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b25a5-355">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="b25a5-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b25a5-356">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b25a5-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b25a5-357">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b25a5-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b25a5-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b25a5-358">Az.RedisCache</span></span>
* <span data-ttu-id="b25a5-359">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="b25a5-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b25a5-360">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="b25a5-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b25a5-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b25a5-361">Az.Resources</span></span>
* <span data-ttu-id="b25a5-362">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b25a5-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b25a5-363">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b25a5-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b25a5-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b25a5-364">Az.Sql</span></span>
* <span data-ttu-id="b25a5-365">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="b25a5-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b25a5-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b25a5-366">Az.Websites</span></span>
* <span data-ttu-id="b25a5-367">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="b25a5-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b25a5-368">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="b25a5-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b25a5-369">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="b25a5-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b25a5-370">Version initiale</span><span class="sxs-lookup"><span data-stu-id="b25a5-370">Initial Release</span></span>