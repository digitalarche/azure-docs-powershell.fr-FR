---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475258"
---
## <a name="160---march-2019"></a><span data-ttu-id="e8fb7-101">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e8fb7-102">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="e8fb7-102">Highlights since the last major release</span></span>
* <span data-ttu-id="e8fb7-103">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="e8fb7-103">General availability of `Az` module</span></span>
* <span data-ttu-id="e8fb7-104">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e8fb7-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e8fb7-105">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e8fb7-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e8fb7-106">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e8fb7-107">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="e8fb7-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e8fb7-108">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e8fb7-109">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e8fb7-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-110">Az.Automation</span></span>
* <span data-ttu-id="e8fb7-111">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8fb7-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e8fb7-112">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="e8fb7-112">Dynamic grouping</span></span>
    * <span data-ttu-id="e8fb7-113">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="e8fb7-113">Pre-Post script</span></span>
    * <span data-ttu-id="e8fb7-114">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-115">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-116">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e8fb7-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e8fb7-117">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e8fb7-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8fb7-118">Az.KeyVault</span></span>
* <span data-ttu-id="e8fb7-119">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8fb7-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-120">Az.Network</span></span>
* <span data-ttu-id="e8fb7-121">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="e8fb7-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e8fb7-122">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="e8fb7-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e8fb7-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="e8fb7-124">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="e8fb7-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e8fb7-125">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="e8fb7-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-126">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-127">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8fb7-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e8fb7-128">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="e8fb7-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-129">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-130">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e8fb7-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-131">Az.Storage</span></span>
* <span data-ttu-id="e8fb7-132">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e8fb7-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e8fb7-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e8fb7-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e8fb7-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e8fb7-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e8fb7-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e8fb7-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e8fb7-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e8fb7-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e8fb7-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-139">Az.Websites</span></span>
* <span data-ttu-id="e8fb7-140">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="e8fb7-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e8fb7-141">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e8fb7-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-142">Az.Accounts</span></span>
* <span data-ttu-id="e8fb7-143">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="e8fb7-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e8fb7-144">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e8fb7-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e8fb7-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-145">Az.Automation</span></span>
* <span data-ttu-id="e8fb7-146">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e8fb7-147">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e8fb7-148">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="e8fb7-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e8fb7-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e8fb7-149">Az.Cdn</span></span>
* <span data-ttu-id="e8fb7-150">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-151">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-152">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="e8fb7-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e8fb7-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8fb7-153">Az.DataFactory</span></span>
* <span data-ttu-id="e8fb7-154">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e8fb7-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e8fb7-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e8fb7-155">Az.LogicApp</span></span>
* <span data-ttu-id="e8fb7-156">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="e8fb7-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-157">Az.Network</span></span>
* <span data-ttu-id="e8fb7-158">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e8fb7-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="e8fb7-160">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="e8fb7-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e8fb7-161">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="e8fb7-161">SDK Update</span></span>
* <span data-ttu-id="e8fb7-162">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e8fb7-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e8fb7-163">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e8fb7-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-164">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-165">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="e8fb7-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e8fb7-166">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e8fb7-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e8fb7-167">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e8fb7-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e8fb7-168">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e8fb7-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e8fb7-169">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e8fb7-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e8fb7-170">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e8fb7-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-171">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-172">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e8fb7-173">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e8fb7-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-174">Az.Storage</span></span>
* <span data-ttu-id="e8fb7-175">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8fb7-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e8fb7-176">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e8fb7-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="e8fb7-178">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="e8fb7-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e8fb7-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-179">Az.Automation</span></span>
* <span data-ttu-id="e8fb7-180">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e8fb7-181">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e8fb7-182">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e8fb7-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="e8fb7-184">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-185">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-186">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="e8fb7-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e8fb7-187">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e8fb7-188">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e8fb7-189">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="e8fb7-191">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="e8fb7-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e8fb7-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e8fb7-192">Az.EventHub</span></span>
* <span data-ttu-id="e8fb7-193">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="e8fb7-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e8fb7-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8fb7-194">Az.KeyVault</span></span>
* <span data-ttu-id="e8fb7-195">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e8fb7-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e8fb7-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e8fb7-196">Az.LogicApp</span></span>
* <span data-ttu-id="e8fb7-197">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="e8fb7-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e8fb7-198">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="e8fb7-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e8fb7-199">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e8fb7-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e8fb7-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e8fb7-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e8fb7-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e8fb7-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e8fb7-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e8fb7-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e8fb7-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e8fb7-204">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e8fb7-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e8fb7-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e8fb7-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e8fb7-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e8fb7-209">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e8fb7-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e8fb7-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e8fb7-210">Az.Monitor</span></span>
* <span data-ttu-id="e8fb7-211">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="e8fb7-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-212">Az.Network</span></span>
* <span data-ttu-id="e8fb7-213">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e8fb7-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e8fb7-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e8fb7-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="e8fb7-215">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e8fb7-216">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e8fb7-217">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e8fb7-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-218">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-219">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e8fb7-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e8fb7-220">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e8fb7-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e8fb7-221">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e8fb7-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e8fb7-222">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e8fb7-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-223">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-224">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="e8fb7-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e8fb7-225">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e8fb7-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-226">Az.Websites</span></span>
* <span data-ttu-id="e8fb7-227">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e8fb7-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e8fb7-228">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e8fb7-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-229">Az.Accounts</span></span>
* <span data-ttu-id="e8fb7-230">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e8fb7-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e8fb7-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-231">Az.AnalysisServices</span></span>
<span data-ttu-id="e8fb7-232">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-233">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-234">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="e8fb7-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e8fb7-235">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e8fb7-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e8fb7-236">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e8fb7-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-237">Az.RecoveryServices</span></span>
<span data-ttu-id="e8fb7-238">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-239">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-240">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e8fb7-241">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e8fb7-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e8fb7-242">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e8fb7-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e8fb7-243">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e8fb7-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-244">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-245">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e8fb7-246">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="e8fb7-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e8fb7-247">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e8fb7-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e8fb7-248">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e8fb7-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-249">Az.Accounts</span></span>
* <span data-ttu-id="e8fb7-250">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="e8fb7-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e8fb7-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="e8fb7-252">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="e8fb7-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e8fb7-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="e8fb7-254">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="e8fb7-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e8fb7-255">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e8fb7-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-256">Az.Accounts</span></span>
* <span data-ttu-id="e8fb7-257">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="e8fb7-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e8fb7-258">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e8fb7-259">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e8fb7-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e8fb7-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e8fb7-260">Az.Aks</span></span>
* <span data-ttu-id="e8fb7-261">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e8fb7-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-262">Az.Automation</span></span>
* <span data-ttu-id="e8fb7-263">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="e8fb7-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e8fb7-264">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e8fb7-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e8fb7-265">Az.Cdn</span></span>
* <span data-ttu-id="e8fb7-266">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-267">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-268">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e8fb7-269">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e8fb7-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e8fb7-270">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8fb7-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e8fb7-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e8fb7-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e8fb7-272">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e8fb7-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e8fb7-273">Az.DataFactory</span></span>
* <span data-ttu-id="e8fb7-274">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e8fb7-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="e8fb7-276">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="e8fb7-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e8fb7-277">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e8fb7-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e8fb7-278">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e8fb7-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e8fb7-279">Az.IotHub</span></span>
* <span data-ttu-id="e8fb7-280">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e8fb7-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8fb7-281">Az.KeyVault</span></span>
* <span data-ttu-id="e8fb7-282">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-283">Az.Network</span></span>
* <span data-ttu-id="e8fb7-284">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-285">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-286">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e8fb7-287">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e8fb7-288">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e8fb7-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e8fb7-289">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e8fb7-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e8fb7-290">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e8fb7-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e8fb7-291">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e8fb7-292">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e8fb7-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e8fb7-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e8fb7-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="e8fb7-294">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e8fb7-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e8fb7-295">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-295">Fix some error messages.</span></span>
* <span data-ttu-id="e8fb7-296">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e8fb7-297">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e8fb7-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e8fb7-298">Az.SignalR</span></span>
* <span data-ttu-id="e8fb7-299">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-300">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-301">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e8fb7-302">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="e8fb7-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e8fb7-303">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="e8fb7-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e8fb7-304">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="e8fb7-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e8fb7-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-305">Az.Storage</span></span>
* <span data-ttu-id="e8fb7-306">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e8fb7-307">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e8fb7-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e8fb7-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e8fb7-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e8fb7-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e8fb7-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e8fb7-310">Az.TrafficManager</span></span>
* <span data-ttu-id="e8fb7-311">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e8fb7-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-312">Az.Websites</span></span>
* <span data-ttu-id="e8fb7-313">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="e8fb7-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e8fb7-314">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e8fb7-315">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="e8fb7-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e8fb7-316">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="e8fb7-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e8fb7-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-317">Az.Accounts</span></span>
* <span data-ttu-id="e8fb7-318">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e8fb7-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-319">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-320">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e8fb7-321">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="e8fb7-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e8fb7-322">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="e8fb7-324">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e8fb7-325">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="e8fb7-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e8fb7-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e8fb7-326">Az.EventGrid</span></span>
* <span data-ttu-id="e8fb7-327">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e8fb7-328">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e8fb7-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e8fb7-329">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="e8fb7-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e8fb7-330">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="e8fb7-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e8fb7-331">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="e8fb7-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e8fb7-332">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e8fb7-333">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="e8fb7-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e8fb7-334">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="e8fb7-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e8fb7-335">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="e8fb7-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e8fb7-336">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="e8fb7-337">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e8fb7-338">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e8fb7-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e8fb7-339">Az.IotHub</span></span>
* <span data-ttu-id="e8fb7-340">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="e8fb7-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e8fb7-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e8fb7-341">Az.LogicApp</span></span>
* <span data-ttu-id="e8fb7-342">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="e8fb7-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-343">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-344">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e8fb7-345">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e8fb7-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e8fb7-346">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e8fb7-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e8fb7-347">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e8fb7-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e8fb7-348">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e8fb7-349">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e8fb7-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e8fb7-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e8fb7-350">Az.SignalR</span></span>
* <span data-ttu-id="e8fb7-351">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-352">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-353">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e8fb7-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-354">Az.Storage</span></span>
* <span data-ttu-id="e8fb7-355">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="e8fb7-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e8fb7-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e8fb7-356">New-AzStorageContext</span></span>
* <span data-ttu-id="e8fb7-357">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="e8fb7-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e8fb7-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e8fb7-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e8fb7-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-359">Az.Websites</span></span>
* <span data-ttu-id="e8fb7-360">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e8fb7-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e8fb7-361">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e8fb7-362">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e8fb7-363">Généralités</span><span class="sxs-lookup"><span data-stu-id="e8fb7-363">General</span></span>

- <span data-ttu-id="e8fb7-364">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="e8fb7-364">General Availability of Az Module</span></span>
- <span data-ttu-id="e8fb7-365">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="e8fb7-365">Online help for each module</span></span>
- <span data-ttu-id="e8fb7-366">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e8fb7-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e8fb7-367">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="e8fb7-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e8fb7-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-368">Az.Accounts</span></span>
- <span data-ttu-id="e8fb7-369">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="e8fb7-370">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="e8fb7-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e8fb7-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e8fb7-371">Az.ApiManagement</span></span>
- <span data-ttu-id="e8fb7-372">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="e8fb7-372">Fixes for #7002</span></span>
- <span data-ttu-id="e8fb7-373">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e8fb7-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e8fb7-374">Az.Batch</span></span>
- <span data-ttu-id="e8fb7-375">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e8fb7-376">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e8fb7-377">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e8fb7-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e8fb7-378">Az.Billing</span></span>
- <span data-ttu-id="e8fb7-379">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e8fb7-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-380">Az.CognitivServices</span></span>
- <span data-ttu-id="e8fb7-381">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e8fb7-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e8fb7-382">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e8fb7-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e8fb7-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e8fb7-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="e8fb7-384">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e8fb7-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e8fb7-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e8fb7-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e8fb7-386">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="e8fb7-388">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e8fb7-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e8fb7-389">Az.Monitor</span></span>
- <span data-ttu-id="e8fb7-390">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e8fb7-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e8fb7-391">Az.KeyVault</span></span>
- <span data-ttu-id="e8fb7-392">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="e8fb7-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e8fb7-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e8fb7-393">Az.MachineLearning</span></span>
- <span data-ttu-id="e8fb7-394">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e8fb7-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e8fb7-395">Az.Media</span></span>
- <span data-ttu-id="e8fb7-396">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e8fb7-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e8fb7-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-397">Az.Network</span></span>
<span data-ttu-id="e8fb7-398">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e8fb7-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e8fb7-399">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="e8fb7-399">New cmdlets added:</span></span>
        - <span data-ttu-id="e8fb7-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e8fb7-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e8fb7-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e8fb7-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e8fb7-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e8fb7-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e8fb7-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e8fb7-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e8fb7-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8fb7-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e8fb7-408">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e8fb7-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8fb7-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e8fb7-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8fb7-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e8fb7-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8fb7-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e8fb7-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8fb7-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e8fb7-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e8fb7-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e8fb7-414">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e8fb7-415">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e8fb7-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e8fb7-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fb7-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e8fb7-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fb7-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e8fb7-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fb7-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e8fb7-419">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e8fb7-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e8fb7-420">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e8fb7-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e8fb7-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="e8fb7-422">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e8fb7-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-423">Az.Profile</span></span>
- <span data-ttu-id="e8fb7-424">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e8fb7-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e8fb7-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="e8fb7-426">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e8fb7-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-427">Az.Resources</span></span>
- <span data-ttu-id="e8fb7-428">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e8fb7-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e8fb7-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="e8fb7-430">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="e8fb7-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e8fb7-431">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e8fb7-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e8fb7-432">Az.SIgnalR</span></span>
- <span data-ttu-id="e8fb7-433">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e8fb7-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e8fb7-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-434">Az.Sql</span></span>
- <span data-ttu-id="e8fb7-435">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="e8fb7-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e8fb7-436">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="e8fb7-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e8fb7-437">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e8fb7-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-438">Az.Storage</span></span>
- <span data-ttu-id="e8fb7-439">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e8fb7-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-440">Az.Websites</span></span>
- <span data-ttu-id="e8fb7-441">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e8fb7-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e8fb7-442">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e8fb7-443">Généralités</span><span class="sxs-lookup"><span data-stu-id="e8fb7-443">General</span></span>

* <span data-ttu-id="e8fb7-444">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="e8fb7-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e8fb7-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-445">Az.Compute</span></span>

* <span data-ttu-id="e8fb7-446">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="e8fb7-448">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="e8fb7-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e8fb7-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8fb7-449">Az.FrontDoor</span></span>

* <span data-ttu-id="e8fb7-450">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="e8fb7-450">Fixed some broken links</span></span>
    - <span data-ttu-id="e8fb7-451">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e8fb7-452">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e8fb7-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="e8fb7-454">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e8fb7-455">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e8fb7-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-456">Az.Resources</span></span>

* <span data-ttu-id="e8fb7-457">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e8fb7-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e8fb7-458">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e8fb7-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-459">Az.Sql</span></span>

* <span data-ttu-id="e8fb7-460">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="e8fb7-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e8fb7-461">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="e8fb7-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e8fb7-462">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e8fb7-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-463">Az.Storage</span></span>

* <span data-ttu-id="e8fb7-464">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8fb7-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e8fb7-465">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="e8fb7-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e8fb7-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e8fb7-467">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="e8fb7-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="e8fb7-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e8fb7-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e8fb7-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e8fb7-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e8fb7-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-470">Az.Websites</span></span>

* <span data-ttu-id="e8fb7-471">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e8fb7-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e8fb7-472">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e8fb7-473">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e8fb7-474">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e8fb7-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e8fb7-475">Az.ApiManagement</span></span>
* <span data-ttu-id="e8fb7-476">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e8fb7-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e8fb7-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e8fb7-477">Az.Automation</span></span>
* <span data-ttu-id="e8fb7-478">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="e8fb7-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e8fb7-479">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="e8fb7-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e8fb7-480">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="e8fb7-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e8fb7-481">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="e8fb7-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e8fb7-482">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="e8fb7-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e8fb7-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-483">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-484">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e8fb7-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e8fb7-485">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e8fb7-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e8fb7-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e8fb7-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="e8fb7-487">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e8fb7-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e8fb7-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e8fb7-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e8fb7-489">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="e8fb7-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e8fb7-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-490">Az.Network</span></span>
* <span data-ttu-id="e8fb7-491">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e8fb7-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e8fb7-492">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8fb7-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e8fb7-493">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e8fb7-494">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e8fb7-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e8fb7-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e8fb7-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e8fb7-496">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e8fb7-497">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e8fb7-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e8fb7-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e8fb7-499">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e8fb7-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e8fb7-500">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="e8fb7-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e8fb7-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e8fb7-501">Az.Relay</span></span>
* <span data-ttu-id="e8fb7-502">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e8fb7-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-503">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-504">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e8fb7-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e8fb7-505">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="e8fb7-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e8fb7-506">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e8fb7-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e8fb7-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e8fb7-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="e8fb7-508">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="e8fb7-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e8fb7-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-509">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-510">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="e8fb7-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e8fb7-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e8fb7-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e8fb7-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e8fb7-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e8fb7-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e8fb7-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e8fb7-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e8fb7-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e8fb7-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e8fb7-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e8fb7-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e8fb7-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e8fb7-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e8fb7-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e8fb7-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e8fb7-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e8fb7-519">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e8fb7-520">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e8fb7-521">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e8fb7-522">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e8fb7-523">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e8fb7-524">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e8fb7-525">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e8fb7-526">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e8fb7-527">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e8fb7-528">Généralités</span><span class="sxs-lookup"><span data-stu-id="e8fb7-528">General</span></span>
* <span data-ttu-id="e8fb7-529">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="e8fb7-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e8fb7-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-530">Az.Profile</span></span>
* <span data-ttu-id="e8fb7-531">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e8fb7-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e8fb7-532">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="e8fb7-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e8fb7-533">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e8fb7-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e8fb7-534">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="e8fb7-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e8fb7-535">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="e8fb7-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e8fb7-536">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="e8fb7-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e8fb7-537">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="e8fb7-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e8fb7-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="e8fb7-539">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-540">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-541">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e8fb7-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e8fb7-542">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e8fb7-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e8fb7-543">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="e8fb7-545">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e8fb7-546">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e8fb7-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e8fb7-547">Az.Insights</span></span>
* <span data-ttu-id="e8fb7-548">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="e8fb7-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e8fb7-549">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="e8fb7-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e8fb7-550">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="e8fb7-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e8fb7-551">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="e8fb7-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-552">Az.Network</span></span>
* <span data-ttu-id="e8fb7-553">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="e8fb7-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e8fb7-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8fb7-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e8fb7-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e8fb7-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e8fb7-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e8fb7-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e8fb7-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e8fb7-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e8fb7-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8fb7-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e8fb7-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e8fb7-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e8fb7-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e8fb7-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="e8fb7-561">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="e8fb7-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-562">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-563">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e8fb7-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e8fb7-564">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e8fb7-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e8fb7-565">Az.ServiceBus</span></span>
* <span data-ttu-id="e8fb7-566">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e8fb7-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e8fb7-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="e8fb7-568">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e8fb7-569">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e8fb7-570">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e8fb7-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e8fb7-571">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e8fb7-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e8fb7-572">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e8fb7-573">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e8fb7-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-574">Az.Profile</span></span>
* <span data-ttu-id="e8fb7-575">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="e8fb7-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e8fb7-576">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e8fb7-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-577">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-578">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="e8fb7-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e8fb7-579">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e8fb7-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e8fb7-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="e8fb7-581">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="e8fb7-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e8fb7-582">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e8fb7-583">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e8fb7-584">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e8fb7-585">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-586">Az.Network</span></span>
* <span data-ttu-id="e8fb7-587">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e8fb7-588">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-589">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-590">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e8fb7-591">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="e8fb7-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e8fb7-592">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e8fb7-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-593">Azure.Storage</span></span>
* <span data-ttu-id="e8fb7-594">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="e8fb7-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e8fb7-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e8fb7-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e8fb7-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e8fb7-597">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e8fb7-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e8fb7-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e8fb7-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e8fb7-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="e8fb7-600">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e8fb7-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e8fb7-601">Az.Compute</span></span>
* <span data-ttu-id="e8fb7-602">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="e8fb7-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e8fb7-603">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e8fb7-604">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="e8fb7-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e8fb7-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8fb7-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e8fb7-606">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e8fb7-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e8fb7-607">Az.Network</span></span>
* <span data-ttu-id="e8fb7-608">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e8fb7-609">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="e8fb7-609">new cmdlets added</span></span>
    - <span data-ttu-id="e8fb7-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e8fb7-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e8fb7-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e8fb7-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e8fb7-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e8fb7-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e8fb7-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e8fb7-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e8fb7-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e8fb7-616">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="e8fb7-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e8fb7-617">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e8fb7-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e8fb7-618">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e8fb7-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e8fb7-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e8fb7-619">Az.RedisCache</span></span>
* <span data-ttu-id="e8fb7-620">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e8fb7-621">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e8fb7-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e8fb7-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e8fb7-622">Az.Resources</span></span>
* <span data-ttu-id="e8fb7-623">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e8fb7-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e8fb7-624">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="e8fb7-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e8fb7-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e8fb7-625">Az.Sql</span></span>
* <span data-ttu-id="e8fb7-626">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="e8fb7-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e8fb7-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e8fb7-627">Az.Websites</span></span>
* <span data-ttu-id="e8fb7-628">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="e8fb7-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e8fb7-629">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="e8fb7-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e8fb7-630">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="e8fb7-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e8fb7-631">Version initiale</span><span class="sxs-lookup"><span data-stu-id="e8fb7-631">Initial Release</span></span>