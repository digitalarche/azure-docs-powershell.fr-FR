## <a name="140---february-2019"></a><span data-ttu-id="b7630-101">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="b7630-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b7630-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7630-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="b7630-103">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="b7630-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7630-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7630-104">Az.Automation</span></span>
* <span data-ttu-id="b7630-105">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b7630-106">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b7630-107">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b7630-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7630-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7630-109">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b7630-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-110">Az.Compute</span></span>
* <span data-ttu-id="b7630-111">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="b7630-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b7630-112">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="b7630-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b7630-113">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b7630-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b7630-114">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="b7630-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7630-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7630-116">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="b7630-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b7630-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7630-117">Az.EventHub</span></span>
* <span data-ttu-id="b7630-118">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="b7630-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b7630-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7630-119">Az.KeyVault</span></span>
* <span data-ttu-id="b7630-120">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7630-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b7630-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7630-121">Az.LogicApp</span></span>
* <span data-ttu-id="b7630-122">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="b7630-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b7630-123">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="b7630-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b7630-124">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="b7630-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b7630-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7630-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b7630-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7630-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b7630-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7630-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b7630-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7630-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b7630-129">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="b7630-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b7630-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b7630-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b7630-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b7630-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b7630-134">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="b7630-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b7630-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b7630-135">Az.Monitor</span></span>
* <span data-ttu-id="b7630-136">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="b7630-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7630-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-137">Az.Network</span></span>
* <span data-ttu-id="b7630-138">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b7630-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b7630-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7630-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="b7630-140">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="b7630-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b7630-141">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="b7630-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b7630-142">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="b7630-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b7630-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-143">Az.Resources</span></span>
* <span data-ttu-id="b7630-144">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b7630-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b7630-145">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b7630-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b7630-146">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="b7630-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b7630-147">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="b7630-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7630-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-148">Az.Sql</span></span>
* <span data-ttu-id="b7630-149">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="b7630-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b7630-150">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="b7630-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7630-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7630-151">Az.Websites</span></span>
* <span data-ttu-id="b7630-152">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="b7630-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b7630-153">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="b7630-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7630-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-154">Az.Accounts</span></span>
* <span data-ttu-id="b7630-155">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b7630-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b7630-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7630-156">Az.AnalysisServices</span></span>
<span data-ttu-id="b7630-157">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="b7630-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-158">Az.Compute</span></span>
* <span data-ttu-id="b7630-159">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="b7630-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b7630-160">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="b7630-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b7630-161">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="b7630-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7630-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7630-162">Az.RecoveryServices</span></span>
<span data-ttu-id="b7630-163">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="b7630-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7630-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-164">Az.Resources</span></span>
* <span data-ttu-id="b7630-165">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="b7630-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b7630-166">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b7630-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b7630-167">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="b7630-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b7630-168">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b7630-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7630-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-169">Az.Sql</span></span>
* <span data-ttu-id="b7630-170">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7630-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b7630-171">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="b7630-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b7630-172">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="b7630-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b7630-173">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="b7630-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7630-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-174">Az.Accounts</span></span>
* <span data-ttu-id="b7630-175">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="b7630-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b7630-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7630-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="b7630-177">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="b7630-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7630-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7630-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="b7630-179">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="b7630-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b7630-180">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="b7630-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7630-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-181">Az.Accounts</span></span>
* <span data-ttu-id="b7630-182">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="b7630-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b7630-183">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7630-184">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="b7630-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b7630-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b7630-185">Az.Aks</span></span>
* <span data-ttu-id="b7630-186">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7630-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7630-187">Az.Automation</span></span>
* <span data-ttu-id="b7630-188">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="b7630-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b7630-189">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b7630-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b7630-190">Az.Cdn</span></span>
* <span data-ttu-id="b7630-191">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-192">Az.Compute</span></span>
* <span data-ttu-id="b7630-193">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="b7630-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b7630-194">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7630-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b7630-195">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b7630-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b7630-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b7630-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b7630-197">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b7630-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b7630-198">Az.DataFactory</span></span>
* <span data-ttu-id="b7630-199">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b7630-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7630-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7630-201">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="b7630-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b7630-202">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b7630-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b7630-203">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b7630-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7630-204">Az.IotHub</span></span>
* <span data-ttu-id="b7630-205">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b7630-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b7630-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7630-206">Az.KeyVault</span></span>
* <span data-ttu-id="b7630-207">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7630-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-208">Az.Network</span></span>
* <span data-ttu-id="b7630-209">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7630-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-210">Az.Resources</span></span>
* <span data-ttu-id="b7630-211">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="b7630-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b7630-212">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="b7630-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b7630-213">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7630-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b7630-214">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="b7630-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b7630-215">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="b7630-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b7630-216">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="b7630-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b7630-217">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b7630-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b7630-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7630-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="b7630-219">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b7630-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b7630-220">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7630-220">Fix some error messages.</span></span>
* <span data-ttu-id="b7630-221">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="b7630-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b7630-222">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="b7630-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b7630-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b7630-223">Az.SignalR</span></span>
* <span data-ttu-id="b7630-224">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7630-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-225">Az.Sql</span></span>
* <span data-ttu-id="b7630-226">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7630-227">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b7630-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b7630-228">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="b7630-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b7630-229">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="b7630-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7630-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7630-230">Az.Storage</span></span>
* <span data-ttu-id="b7630-231">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7630-232">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="b7630-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b7630-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b7630-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b7630-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b7630-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b7630-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7630-235">Az.TrafficManager</span></span>
* <span data-ttu-id="b7630-236">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7630-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7630-237">Az.Websites</span></span>
* <span data-ttu-id="b7630-238">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="b7630-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7630-239">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="b7630-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b7630-240">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="b7630-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b7630-241">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="b7630-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7630-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-242">Az.Accounts</span></span>
* <span data-ttu-id="b7630-243">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b7630-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-244">Az.Compute</span></span>
* <span data-ttu-id="b7630-245">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b7630-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b7630-246">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="b7630-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b7630-247">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7630-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7630-249">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="b7630-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b7630-250">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="b7630-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b7630-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b7630-251">Az.EventGrid</span></span>
* <span data-ttu-id="b7630-252">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="b7630-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b7630-253">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="b7630-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b7630-254">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="b7630-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b7630-255">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="b7630-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b7630-256">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="b7630-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b7630-257">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="b7630-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b7630-258">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="b7630-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b7630-259">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="b7630-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b7630-260">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="b7630-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b7630-261">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="b7630-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="b7630-262">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="b7630-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b7630-263">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7630-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b7630-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7630-264">Az.IotHub</span></span>
* <span data-ttu-id="b7630-265">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="b7630-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b7630-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7630-266">Az.LogicApp</span></span>
* <span data-ttu-id="b7630-267">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="b7630-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7630-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-268">Az.Resources</span></span>
* <span data-ttu-id="b7630-269">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="b7630-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b7630-270">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b7630-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b7630-271">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7630-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b7630-272">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="b7630-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b7630-273">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="b7630-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b7630-274">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b7630-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b7630-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b7630-275">Az.SignalR</span></span>
* <span data-ttu-id="b7630-276">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7630-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-277">Az.Sql</span></span>
* <span data-ttu-id="b7630-278">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="b7630-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7630-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7630-279">Az.Storage</span></span>
* <span data-ttu-id="b7630-280">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="b7630-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b7630-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7630-281">New-AzStorageContext</span></span>
* <span data-ttu-id="b7630-282">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="b7630-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b7630-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b7630-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7630-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7630-284">Az.Websites</span></span>
* <span data-ttu-id="b7630-285">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="b7630-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b7630-286">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b7630-287">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b7630-288">Généralités</span><span class="sxs-lookup"><span data-stu-id="b7630-288">General</span></span>

- <span data-ttu-id="b7630-289">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="b7630-289">General Availability of Az Module</span></span>
- <span data-ttu-id="b7630-290">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="b7630-290">Online help for each module</span></span>
- <span data-ttu-id="b7630-291">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b7630-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b7630-292">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="b7630-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b7630-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-293">Az.Accounts</span></span>
- <span data-ttu-id="b7630-294">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7630-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="b7630-295">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="b7630-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b7630-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7630-296">Az.ApiManagement</span></span>
- <span data-ttu-id="b7630-297">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="b7630-297">Fixes for #7002</span></span>
- <span data-ttu-id="b7630-298">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b7630-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b7630-299">Az.Batch</span></span>
- <span data-ttu-id="b7630-300">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="b7630-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b7630-301">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="b7630-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b7630-302">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b7630-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b7630-303">Az.Billing</span></span>
- <span data-ttu-id="b7630-304">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b7630-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b7630-305">Az.CognitivServices</span></span>
- <span data-ttu-id="b7630-306">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7630-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b7630-307">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b7630-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b7630-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b7630-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="b7630-309">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b7630-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b7630-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b7630-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b7630-311">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b7630-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="b7630-313">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b7630-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b7630-314">Az.Monitor</span></span>
- <span data-ttu-id="b7630-315">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b7630-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7630-316">Az.KeyVault</span></span>
- <span data-ttu-id="b7630-317">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="b7630-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b7630-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b7630-318">Az.MachineLearning</span></span>
- <span data-ttu-id="b7630-319">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b7630-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b7630-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b7630-320">Az.Media</span></span>
- <span data-ttu-id="b7630-321">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b7630-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b7630-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-322">Az.Network</span></span>
<span data-ttu-id="b7630-323">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b7630-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b7630-324">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="b7630-324">New cmdlets added:</span></span>
        - <span data-ttu-id="b7630-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7630-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7630-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7630-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7630-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7630-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7630-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7630-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7630-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7630-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7630-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b7630-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b7630-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b7630-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b7630-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7630-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b7630-333">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7630-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b7630-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7630-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b7630-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7630-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b7630-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7630-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b7630-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7630-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b7630-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b7630-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b7630-339">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="b7630-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b7630-340">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7630-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b7630-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b7630-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b7630-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b7630-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b7630-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b7630-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b7630-344">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="b7630-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b7630-345">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b7630-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7630-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="b7630-347">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b7630-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7630-348">Az.Profile</span></span>
- <span data-ttu-id="b7630-349">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7630-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b7630-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7630-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="b7630-351">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b7630-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-352">Az.Resources</span></span>
- <span data-ttu-id="b7630-353">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b7630-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7630-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="b7630-355">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="b7630-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b7630-356">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b7630-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b7630-357">Az.SIgnalR</span></span>
- <span data-ttu-id="b7630-358">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b7630-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b7630-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-359">Az.Sql</span></span>
- <span data-ttu-id="b7630-360">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="b7630-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b7630-361">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="b7630-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b7630-362">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b7630-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7630-363">Az.Storage</span></span>
- <span data-ttu-id="b7630-364">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b7630-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7630-365">Az.Websites</span></span>
- <span data-ttu-id="b7630-366">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="b7630-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b7630-367">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b7630-368">Généralités</span><span class="sxs-lookup"><span data-stu-id="b7630-368">General</span></span>

* <span data-ttu-id="b7630-369">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="b7630-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b7630-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-370">Az.Compute</span></span>

* <span data-ttu-id="b7630-371">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="b7630-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b7630-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="b7630-373">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="b7630-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b7630-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b7630-374">Az.FrontDoor</span></span>

* <span data-ttu-id="b7630-375">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="b7630-375">Fixed some broken links</span></span>
    - <span data-ttu-id="b7630-376">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="b7630-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b7630-377">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="b7630-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b7630-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7630-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="b7630-379">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="b7630-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b7630-380">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="b7630-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b7630-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-381">Az.Resources</span></span>

* <span data-ttu-id="b7630-382">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b7630-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b7630-383">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="b7630-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b7630-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-384">Az.Sql</span></span>

* <span data-ttu-id="b7630-385">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="b7630-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b7630-386">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="b7630-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b7630-387">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="b7630-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b7630-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7630-388">Az.Storage</span></span>

* <span data-ttu-id="b7630-389">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7630-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b7630-390">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="b7630-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b7630-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b7630-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b7630-392">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="b7630-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="b7630-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b7630-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b7630-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b7630-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b7630-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7630-395">Az.Websites</span></span>

* <span data-ttu-id="b7630-396">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b7630-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b7630-397">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="b7630-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b7630-398">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="b7630-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b7630-399">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b7630-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7630-400">Az.ApiManagement</span></span>
* <span data-ttu-id="b7630-401">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b7630-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b7630-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7630-402">Az.Automation</span></span>
* <span data-ttu-id="b7630-403">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="b7630-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b7630-404">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="b7630-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b7630-405">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="b7630-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b7630-406">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="b7630-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b7630-407">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="b7630-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b7630-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-408">Az.Compute</span></span>
* <span data-ttu-id="b7630-409">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="b7630-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b7630-410">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b7630-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b7630-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b7630-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="b7630-412">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b7630-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b7630-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b7630-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b7630-414">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="b7630-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b7630-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-415">Az.Network</span></span>
* <span data-ttu-id="b7630-416">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b7630-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b7630-417">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7630-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b7630-418">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="b7630-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b7630-419">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b7630-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b7630-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7630-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7630-421">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="b7630-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b7630-422">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="b7630-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b7630-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b7630-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b7630-424">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b7630-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b7630-425">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="b7630-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b7630-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b7630-426">Az.Relay</span></span>
* <span data-ttu-id="b7630-427">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b7630-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b7630-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-428">Az.Resources</span></span>
* <span data-ttu-id="b7630-429">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="b7630-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b7630-430">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="b7630-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b7630-431">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="b7630-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b7630-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7630-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="b7630-433">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="b7630-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b7630-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-434">Az.Sql</span></span>
* <span data-ttu-id="b7630-435">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="b7630-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b7630-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7630-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7630-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7630-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7630-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7630-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7630-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7630-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7630-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7630-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b7630-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7630-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b7630-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7630-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b7630-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7630-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b7630-444">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="b7630-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b7630-445">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="b7630-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b7630-446">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="b7630-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b7630-447">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b7630-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b7630-448">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="b7630-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b7630-449">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b7630-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b7630-450">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="b7630-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b7630-451">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="b7630-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b7630-452">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7630-453">Généralités</span><span class="sxs-lookup"><span data-stu-id="b7630-453">General</span></span>
* <span data-ttu-id="b7630-454">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="b7630-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b7630-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7630-455">Az.Profile</span></span>
* <span data-ttu-id="b7630-456">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b7630-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b7630-457">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="b7630-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b7630-458">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="b7630-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b7630-459">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="b7630-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b7630-460">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="b7630-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b7630-461">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="b7630-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b7630-462">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="b7630-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b7630-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7630-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7630-464">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="b7630-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-465">Az.Compute</span></span>
* <span data-ttu-id="b7630-466">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b7630-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b7630-467">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b7630-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b7630-468">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="b7630-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7630-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7630-470">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="b7630-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b7630-471">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="b7630-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b7630-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b7630-472">Az.Insights</span></span>
* <span data-ttu-id="b7630-473">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="b7630-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b7630-474">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="b7630-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b7630-475">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="b7630-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b7630-476">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="b7630-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7630-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-477">Az.Network</span></span>
* <span data-ttu-id="b7630-478">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="b7630-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b7630-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7630-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b7630-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b7630-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b7630-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7630-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b7630-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b7630-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b7630-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7630-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b7630-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7630-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b7630-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b7630-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="b7630-486">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="b7630-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7630-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-487">Az.Resources</span></span>
* <span data-ttu-id="b7630-488">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b7630-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b7630-489">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="b7630-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b7630-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7630-490">Az.ServiceBus</span></span>
* <span data-ttu-id="b7630-491">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="b7630-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b7630-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7630-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="b7630-493">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="b7630-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b7630-494">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="b7630-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b7630-495">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="b7630-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b7630-496">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="b7630-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b7630-497">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="b7630-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b7630-498">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b7630-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7630-499">Az.Profile</span></span>
* <span data-ttu-id="b7630-500">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="b7630-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b7630-501">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b7630-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-502">Az.Compute</span></span>
* <span data-ttu-id="b7630-503">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="b7630-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b7630-504">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="b7630-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7630-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7630-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7630-506">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="b7630-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b7630-507">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7630-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b7630-508">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7630-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b7630-509">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7630-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b7630-510">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b7630-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7630-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-511">Az.Network</span></span>
* <span data-ttu-id="b7630-512">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="b7630-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b7630-513">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="b7630-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7630-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-514">Az.Resources</span></span>
* <span data-ttu-id="b7630-515">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="b7630-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b7630-516">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="b7630-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b7630-517">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b7630-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b7630-518">Azure.Storage</span></span>
* <span data-ttu-id="b7630-519">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="b7630-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b7630-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b7630-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b7630-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b7630-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b7630-522">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="b7630-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b7630-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b7630-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b7630-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7630-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7630-525">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="b7630-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7630-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7630-526">Az.Compute</span></span>
* <span data-ttu-id="b7630-527">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="b7630-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b7630-528">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="b7630-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b7630-529">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="b7630-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b7630-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7630-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b7630-531">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="b7630-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7630-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7630-532">Az.Network</span></span>
* <span data-ttu-id="b7630-533">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="b7630-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b7630-534">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="b7630-534">new cmdlets added</span></span>
    - <span data-ttu-id="b7630-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7630-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7630-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7630-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7630-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7630-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7630-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7630-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7630-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b7630-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b7630-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7630-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b7630-541">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="b7630-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b7630-542">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b7630-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b7630-543">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b7630-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b7630-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b7630-544">Az.RedisCache</span></span>
* <span data-ttu-id="b7630-545">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="b7630-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b7630-546">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="b7630-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7630-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7630-547">Az.Resources</span></span>
* <span data-ttu-id="b7630-548">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7630-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b7630-549">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b7630-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7630-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7630-550">Az.Sql</span></span>
* <span data-ttu-id="b7630-551">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="b7630-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7630-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7630-552">Az.Websites</span></span>
* <span data-ttu-id="b7630-553">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="b7630-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b7630-554">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="b7630-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b7630-555">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="b7630-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b7630-556">Version initiale</span><span class="sxs-lookup"><span data-stu-id="b7630-556">Initial Release</span></span>