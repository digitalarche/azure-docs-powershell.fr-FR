---
ms.openlocfilehash: 54d7a9da878e085e90479fb229876c9be6dafd74
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364042"
---
## <a name="170---april-2019"></a><span data-ttu-id="1c4e4-101">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-101">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1c4e4-102">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="1c4e4-102">Highlights since the last major release</span></span>
* <span data-ttu-id="1c4e4-103">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="1c4e4-103">General availability of `Az` module</span></span>
* <span data-ttu-id="1c4e4-104">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1c4e4-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1c4e4-105">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1c4e4-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1c4e4-106">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1c4e4-107">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1c4e4-108">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1c4e4-109">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1c4e4-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-110">Az.Accounts</span></span>
* <span data-ttu-id="1c4e4-111">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4e4-111">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1c4e4-112">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-112">Az.AnalysisServices</span></span>
* <span data-ttu-id="1c4e4-113">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="1c4e4-113">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1c4e4-114">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="1c4e4-114">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1c4e4-115">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-115">Az.Automation</span></span>
* <span data-ttu-id="1c4e4-116">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-116">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1c4e4-117">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-117">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1c4e4-118">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="1c4e4-118">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-119">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-120">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1c4e4-120">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1c4e4-121">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-121">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="1c4e4-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-122">Az.ContainerInstance</span></span>
* <span data-ttu-id="1c4e4-123">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="1c4e4-123">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1c4e4-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c4e4-124">Az.DataFactory</span></span>
* <span data-ttu-id="1c4e4-125">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="1c4e4-125">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1c4e4-126">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-126">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-127">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-127">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-128">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="1c4e4-128">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1c4e4-129">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="1c4e4-129">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1c4e4-130">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="1c4e4-130">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1c4e4-131">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1c4e4-131">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1c4e4-132">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="1c4e4-132">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1c4e4-133">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1c4e4-133">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-134">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-134">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-135">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-135">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1c4e4-136">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-136">Az.Storage</span></span>
* <span data-ttu-id="1c4e4-137">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="1c4e4-137">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1c4e4-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c4e4-138">New-AzStorageContext</span></span>
* <span data-ttu-id="1c4e4-139">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="1c4e4-139">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1c4e4-140">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1c4e4-140">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1c4e4-141">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1c4e4-141">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1c4e4-142">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-142">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1c4e4-143">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-143">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1c4e4-144">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="1c4e4-144">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1c4e4-145">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1c4e4-145">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1c4e4-146">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1c4e4-146">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1c4e4-147">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1c4e4-147">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1c4e4-148">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1c4e4-148">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1c4e4-149">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-149">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1c4e4-150">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="1c4e4-150">Highlights since the last major release</span></span>
* <span data-ttu-id="1c4e4-151">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="1c4e4-151">General availability of `Az` module</span></span>
* <span data-ttu-id="1c4e4-152">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1c4e4-152">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1c4e4-153">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1c4e4-153">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1c4e4-154">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-154">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1c4e4-155">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-155">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1c4e4-156">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-156">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1c4e4-157">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-157">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1c4e4-158">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-158">Az.Automation</span></span>
* <span data-ttu-id="1c4e4-159">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c4e4-159">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1c4e4-160">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="1c4e4-160">Dynamic grouping</span></span>
    * <span data-ttu-id="1c4e4-161">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="1c4e4-161">Pre-Post script</span></span>
    * <span data-ttu-id="1c4e4-162">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-162">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-163">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-163">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-164">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1c4e4-164">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1c4e4-165">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-165">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1c4e4-166">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1c4e4-166">Az.KeyVault</span></span>
* <span data-ttu-id="1c4e4-167">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="1c4e4-167">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-168">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-168">Az.Network</span></span>
* <span data-ttu-id="1c4e4-169">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="1c4e4-169">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1c4e4-170">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="1c4e4-170">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1c4e4-171">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-171">Az.RecoveryServices</span></span>
* <span data-ttu-id="1c4e4-172">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="1c4e4-172">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1c4e4-173">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="1c4e4-173">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-174">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-175">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1c4e4-175">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1c4e4-176">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="1c4e4-176">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-177">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-177">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-178">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-178">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1c4e4-179">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-179">Az.Storage</span></span>
* <span data-ttu-id="1c4e4-180">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-180">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1c4e4-181">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-181">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1c4e4-182">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-182">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1c4e4-183">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-183">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1c4e4-184">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1c4e4-184">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1c4e4-185">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1c4e4-185">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1c4e4-186">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1c4e4-186">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1c4e4-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-187">Az.Websites</span></span>
* <span data-ttu-id="1c4e4-188">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="1c4e4-188">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="1c4e4-189">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-189">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1c4e4-190">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-190">Az.Accounts</span></span>
* <span data-ttu-id="1c4e4-191">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="1c4e4-191">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1c4e4-192">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1c4e4-192">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1c4e4-193">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-193">Az.Automation</span></span>
* <span data-ttu-id="1c4e4-194">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-194">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1c4e4-195">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-195">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1c4e4-196">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="1c4e4-196">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1c4e4-197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1c4e4-197">Az.Cdn</span></span>
* <span data-ttu-id="1c4e4-198">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-198">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-199">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-200">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="1c4e4-200">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1c4e4-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c4e4-201">Az.DataFactory</span></span>
* <span data-ttu-id="1c4e4-202">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="1c4e4-202">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1c4e4-203">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1c4e4-203">Az.LogicApp</span></span>
* <span data-ttu-id="1c4e4-204">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="1c4e4-204">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-205">Az.Network</span></span>
* <span data-ttu-id="1c4e4-206">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-206">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1c4e4-207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-207">Az.RecoveryServices</span></span>
* <span data-ttu-id="1c4e4-208">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="1c4e4-208">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1c4e4-209">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="1c4e4-209">SDK Update</span></span>
* <span data-ttu-id="1c4e4-210">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1c4e4-210">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1c4e4-211">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1c4e4-211">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-212">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-213">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-213">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1c4e4-214">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="1c4e4-214">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1c4e4-215">Résolution du problème d’envoi du résultat de `Get-AzResource` à</span><span class="sxs-lookup"><span data-stu-id="1c4e4-215">Fix issue when piping the result of `Get-AzResource` to</span></span> `Set-AzResource`
    - <span data-ttu-id="1c4e4-216">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="1c4e4-216">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1c4e4-217">Résolution du problème de changement de type de données JSON lors de l’exécution de</span><span class="sxs-lookup"><span data-stu-id="1c4e4-217">Fix issue with JSON data type change when running</span></span> `Set-AzResource`
    - <span data-ttu-id="1c4e4-218">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="1c4e4-218">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-219">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-220">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-220">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1c4e4-221">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-221">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1c4e4-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-222">Az.Storage</span></span>
* <span data-ttu-id="1c4e4-223">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c4e4-223">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1c4e4-224">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-224">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1c4e4-225">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-225">Az.AnalysisServices</span></span>
* <span data-ttu-id="1c4e4-226">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="1c4e4-226">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1c4e4-227">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-227">Az.Automation</span></span>
* <span data-ttu-id="1c4e4-228">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-228">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1c4e4-229">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-229">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1c4e4-230">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-230">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1c4e4-231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-231">Az.CognitiveServices</span></span>
* <span data-ttu-id="1c4e4-232">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-232">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-233">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-234">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="1c4e4-234">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1c4e4-235">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-235">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1c4e4-236">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-236">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1c4e4-237">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-237">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-238">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-238">Az.DataLakeStore</span></span>
* <span data-ttu-id="1c4e4-239">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="1c4e4-239">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1c4e4-240">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1c4e4-240">Az.EventHub</span></span>
* <span data-ttu-id="1c4e4-241">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="1c4e4-241">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="1c4e4-242">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1c4e4-242">Az.KeyVault</span></span>
* <span data-ttu-id="1c4e4-243">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1c4e4-243">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1c4e4-244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1c4e4-244">Az.LogicApp</span></span>
* <span data-ttu-id="1c4e4-245">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="1c4e4-245">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1c4e4-246">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="1c4e4-246">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1c4e4-247">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-247">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1c4e4-248">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1c4e4-248">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1c4e4-249">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1c4e4-249">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1c4e4-250">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1c4e4-250">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1c4e4-251">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1c4e4-251">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1c4e4-252">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-252">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1c4e4-253">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-253">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1c4e4-254">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-254">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1c4e4-255">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-255">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1c4e4-256">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-256">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1c4e4-257">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="1c4e4-257">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1c4e4-258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1c4e4-258">Az.Monitor</span></span>
* <span data-ttu-id="1c4e4-259">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="1c4e4-259">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-260">Az.Network</span></span>
* <span data-ttu-id="1c4e4-261">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1c4e4-261">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1c4e4-262">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1c4e4-262">Az.OperationalInsights</span></span>
* <span data-ttu-id="1c4e4-263">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-263">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1c4e4-264">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-264">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="1c4e4-265">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-265">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="1c4e4-266">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-266">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-267">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1c4e4-267">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1c4e4-268">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1c4e4-268">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1c4e4-269">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="1c4e4-269">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1c4e4-270">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="1c4e4-270">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-271">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-272">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="1c4e4-272">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1c4e4-273">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-273">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1c4e4-274">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-274">Az.Websites</span></span>
* <span data-ttu-id="1c4e4-275">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="1c4e4-275">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1c4e4-276">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-276">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1c4e4-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-277">Az.Accounts</span></span>
* <span data-ttu-id="1c4e4-278">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1c4e4-278">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1c4e4-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-279">Az.AnalysisServices</span></span>
<span data-ttu-id="1c4e4-280">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-280">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-281">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-282">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="1c4e4-282">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1c4e4-283">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1c4e4-283">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1c4e4-284">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-284">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1c4e4-285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-285">Az.RecoveryServices</span></span>
<span data-ttu-id="1c4e4-286">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-286">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-287">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-288">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-288">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="1c4e4-289">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1c4e4-289">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1c4e4-290">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="1c4e4-290">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="1c4e4-291">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1c4e4-291">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-292">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-292">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-293">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-293">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1c4e4-294">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="1c4e4-294">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1c4e4-295">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="1c4e4-295">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1c4e4-296">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-296">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1c4e4-297">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-297">Az.Accounts</span></span>
* <span data-ttu-id="1c4e4-298">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="1c4e4-298">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1c4e4-299">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-299">Az.AnalysisServices</span></span>
* <span data-ttu-id="1c4e4-300">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="1c4e4-300">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1c4e4-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="1c4e4-302">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="1c4e4-302">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1c4e4-303">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-303">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1c4e4-304">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-304">Az.Accounts</span></span>
* <span data-ttu-id="1c4e4-305">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-305">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1c4e4-306">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1c4e4-307">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="1c4e4-307">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1c4e4-308">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1c4e4-308">Az.Aks</span></span>
* <span data-ttu-id="1c4e4-309">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-309">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1c4e4-310">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-310">Az.Automation</span></span>
* <span data-ttu-id="1c4e4-311">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="1c4e4-311">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1c4e4-312">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-312">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1c4e4-313">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1c4e4-313">Az.Cdn</span></span>
* <span data-ttu-id="1c4e4-314">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-314">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-315">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-316">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-316">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1c4e4-317">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1c4e4-317">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1c4e4-318">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1c4e4-318">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1c4e4-319">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1c4e4-319">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1c4e4-320">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-320">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1c4e4-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1c4e4-321">Az.DataFactory</span></span>
* <span data-ttu-id="1c4e4-322">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="1c4e4-322">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="1c4e4-324">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="1c4e4-324">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1c4e4-325">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="1c4e4-325">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1c4e4-326">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-326">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1c4e4-327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1c4e4-327">Az.IotHub</span></span>
* <span data-ttu-id="1c4e4-328">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-328">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1c4e4-329">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1c4e4-329">Az.KeyVault</span></span>
* <span data-ttu-id="1c4e4-330">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-330">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-331">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-331">Az.Network</span></span>
* <span data-ttu-id="1c4e4-332">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-332">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-333">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-333">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-334">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-334">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1c4e4-335">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-335">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1c4e4-336">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1c4e4-336">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1c4e4-337">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="1c4e4-337">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1c4e4-338">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="1c4e4-338">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1c4e4-339">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-339">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1c4e4-340">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="1c4e4-340">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1c4e4-341">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1c4e4-341">Az.ServiceFabric</span></span>
* <span data-ttu-id="1c4e4-342">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="1c4e4-342">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1c4e4-343">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-343">Fix some error messages.</span></span>
* <span data-ttu-id="1c4e4-344">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-344">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1c4e4-345">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-345">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1c4e4-346">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1c4e4-346">Az.SignalR</span></span>
* <span data-ttu-id="1c4e4-347">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-347">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-348">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-348">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-349">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-349">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1c4e4-350">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1c4e4-350">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1c4e4-351">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="1c4e4-351">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1c4e4-352">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="1c4e4-352">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1c4e4-353">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-353">Az.Storage</span></span>
* <span data-ttu-id="1c4e4-354">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-354">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1c4e4-355">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-355">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1c4e4-356">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1c4e4-356">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1c4e4-357">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1c4e4-357">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1c4e4-358">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1c4e4-358">Az.TrafficManager</span></span>
* <span data-ttu-id="1c4e4-359">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-359">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1c4e4-360">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-360">Az.Websites</span></span>
* <span data-ttu-id="1c4e4-361">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1c4e4-361">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1c4e4-362">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-362">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1c4e4-363">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="1c4e4-363">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1c4e4-364">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="1c4e4-364">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1c4e4-365">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-365">Az.Accounts</span></span>
* <span data-ttu-id="1c4e4-366">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1c4e4-366">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-367">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-367">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-368">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-368">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1c4e4-369">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="1c4e4-369">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1c4e4-370">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-370">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-371">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-371">Az.DataLakeStore</span></span>
* <span data-ttu-id="1c4e4-372">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-372">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1c4e4-373">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="1c4e4-373">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1c4e4-374">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1c4e4-374">Az.EventGrid</span></span>
* <span data-ttu-id="1c4e4-375">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-375">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1c4e4-376">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="1c4e4-376">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1c4e4-377">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="1c4e4-377">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1c4e4-378">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="1c4e4-378">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1c4e4-379">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="1c4e4-379">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1c4e4-380">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-380">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1c4e4-381">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="1c4e4-381">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1c4e4-382">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="1c4e4-382">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1c4e4-383">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="1c4e4-383">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1c4e4-384">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-384">Dead letter endpoint.</span></span>
* <span data-ttu-id="1c4e4-385">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-385">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1c4e4-386">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-386">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1c4e4-387">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1c4e4-387">Az.IotHub</span></span>
* <span data-ttu-id="1c4e4-388">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="1c4e4-388">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1c4e4-389">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1c4e4-389">Az.LogicApp</span></span>
* <span data-ttu-id="1c4e4-390">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="1c4e4-390">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-391">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-391">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-392">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-392">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1c4e4-393">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="1c4e4-393">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1c4e4-394">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1c4e4-394">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1c4e4-395">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1c4e4-395">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1c4e4-396">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-396">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1c4e4-397">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="1c4e4-397">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1c4e4-398">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1c4e4-398">Az.SignalR</span></span>
* <span data-ttu-id="1c4e4-399">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-399">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-400">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-401">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-401">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1c4e4-402">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-402">Az.Storage</span></span>
* <span data-ttu-id="1c4e4-403">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="1c4e4-403">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1c4e4-404">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c4e4-404">New-AzStorageContext</span></span>
* <span data-ttu-id="1c4e4-405">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="1c4e4-405">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1c4e4-406">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1c4e4-406">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1c4e4-407">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-407">Az.Websites</span></span>
* <span data-ttu-id="1c4e4-408">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1c4e4-408">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1c4e4-409">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-409">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1c4e4-410">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-410">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1c4e4-411">Généralités</span><span class="sxs-lookup"><span data-stu-id="1c4e4-411">General</span></span>

- <span data-ttu-id="1c4e4-412">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="1c4e4-412">General Availability of Az Module</span></span>
- <span data-ttu-id="1c4e4-413">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="1c4e4-413">Online help for each module</span></span>
- <span data-ttu-id="1c4e4-414">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="1c4e4-414">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1c4e4-415">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="1c4e4-415">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1c4e4-416">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-416">Az.Accounts</span></span>
- <span data-ttu-id="1c4e4-417">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-417">Changed from Az.Profile</span></span>
- <span data-ttu-id="1c4e4-418">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="1c4e4-418">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1c4e4-419">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-419">Az.ApiManagement</span></span>
- <span data-ttu-id="1c4e4-420">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="1c4e4-420">Fixes for #7002</span></span>
- <span data-ttu-id="1c4e4-421">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-421">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1c4e4-422">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1c4e4-422">Az.Batch</span></span>
- <span data-ttu-id="1c4e4-423">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-423">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1c4e4-424">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-424">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1c4e4-425">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-425">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1c4e4-426">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1c4e4-426">Az.Billing</span></span>
- <span data-ttu-id="1c4e4-427">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-427">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1c4e4-428">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-428">Az.CognitivServices</span></span>
- <span data-ttu-id="1c4e4-429">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1c4e4-429">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1c4e4-430">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="1c4e4-430">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1c4e4-431">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-431">Az.ContainerInstance</span></span>
- <span data-ttu-id="1c4e4-432">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c4e4-432">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1c4e4-433">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1c4e4-433">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1c4e4-434">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-434">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-435">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-435">Az.DataLakeStore</span></span>
- <span data-ttu-id="1c4e4-436">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-436">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1c4e4-437">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1c4e4-437">Az.Monitor</span></span>
- <span data-ttu-id="1c4e4-438">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-438">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1c4e4-439">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1c4e4-439">Az.KeyVault</span></span>
- <span data-ttu-id="1c4e4-440">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="1c4e4-440">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1c4e4-441">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1c4e4-441">Az.MachineLearning</span></span>
- <span data-ttu-id="1c4e4-442">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-442">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1c4e4-443">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1c4e4-443">Az.Media</span></span>
- <span data-ttu-id="1c4e4-444">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1c4e4-444">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1c4e4-445">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-445">Az.Network</span></span>
<span data-ttu-id="1c4e4-446">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1c4e4-446">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1c4e4-447">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="1c4e4-447">New cmdlets added:</span></span>
        - <span data-ttu-id="1c4e4-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-448">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1c4e4-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-449">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1c4e4-450">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-450">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1c4e4-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-451">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1c4e4-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-452">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1c4e4-453">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1c4e4-453">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1c4e4-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-454">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1c4e4-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c4e4-455">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1c4e4-456">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-456">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1c4e4-457">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1c4e4-457">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1c4e4-458">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1c4e4-458">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1c4e4-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1c4e4-459">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1c4e4-460">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1c4e4-460">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1c4e4-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1c4e4-461">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1c4e4-462">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-462">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1c4e4-463">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1c4e4-463">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1c4e4-464">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1c4e4-464">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1c4e4-465">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1c4e4-465">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1c4e4-466">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1c4e4-466">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1c4e4-467">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c4e4-467">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1c4e4-468">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-468">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1c4e4-469">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1c4e4-469">Az.OperationalInsights</span></span>
- <span data-ttu-id="1c4e4-470">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-470">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1c4e4-471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-471">Az.Profile</span></span>
- <span data-ttu-id="1c4e4-472">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1c4e4-472">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1c4e4-473">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-473">Az.RecoveryServices</span></span>
- <span data-ttu-id="1c4e4-474">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-474">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1c4e4-475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-475">Az.Resources</span></span>
- <span data-ttu-id="1c4e4-476">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-476">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1c4e4-477">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1c4e4-477">Az.ServiceFabric</span></span>
- <span data-ttu-id="1c4e4-478">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="1c4e4-478">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1c4e4-479">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-479">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1c4e4-480">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1c4e4-480">Az.SIgnalR</span></span>
- <span data-ttu-id="1c4e4-481">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1c4e4-481">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1c4e4-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-482">Az.Sql</span></span>
- <span data-ttu-id="1c4e4-483">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="1c4e4-483">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1c4e4-484">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="1c4e4-484">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1c4e4-485">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-485">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1c4e4-486">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-486">Az.Storage</span></span>
- <span data-ttu-id="1c4e4-487">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-487">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1c4e4-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-488">Az.Websites</span></span>
- <span data-ttu-id="1c4e4-489">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1c4e4-489">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1c4e4-490">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-490">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1c4e4-491">Généralités</span><span class="sxs-lookup"><span data-stu-id="1c4e4-491">General</span></span>

* <span data-ttu-id="1c4e4-492">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="1c4e4-492">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1c4e4-493">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-493">Az.Compute</span></span>

* <span data-ttu-id="1c4e4-494">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-494">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-495">Az.DataLakeStore</span></span>

* <span data-ttu-id="1c4e4-496">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="1c4e4-496">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1c4e4-497">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1c4e4-497">Az.FrontDoor</span></span>

* <span data-ttu-id="1c4e4-498">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="1c4e4-498">Fixed some broken links</span></span>
    - <span data-ttu-id="1c4e4-499">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-499">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1c4e4-500">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-500">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1c4e4-501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-501">Az.RecoveryServices</span></span>

* <span data-ttu-id="1c4e4-502">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-502">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1c4e4-503">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-503">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1c4e4-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-504">Az.Resources</span></span>

* <span data-ttu-id="1c4e4-505">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="1c4e4-505">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1c4e4-506">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-506">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1c4e4-507">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-507">Az.Sql</span></span>

* <span data-ttu-id="1c4e4-508">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="1c4e4-508">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1c4e4-509">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="1c4e4-509">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1c4e4-510">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-510">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1c4e4-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-511">Az.Storage</span></span>

* <span data-ttu-id="1c4e4-512">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1c4e4-512">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1c4e4-513">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="1c4e4-513">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1c4e4-514">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-514">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1c4e4-515">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="1c4e4-515">Support Static Website configuration</span></span>
    - <span data-ttu-id="1c4e4-516">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1c4e4-516">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1c4e4-517">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1c4e4-517">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1c4e4-518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-518">Az.Websites</span></span>

* <span data-ttu-id="1c4e4-519">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1c4e4-519">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="1c4e4-520">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-520">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1c4e4-521">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-521">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1c4e4-522">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-522">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1c4e4-523">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-523">Az.ApiManagement</span></span>
* <span data-ttu-id="1c4e4-524">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1c4e4-524">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1c4e4-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1c4e4-525">Az.Automation</span></span>
* <span data-ttu-id="1c4e4-526">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="1c4e4-526">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1c4e4-527">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="1c4e4-527">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1c4e4-528">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="1c4e4-528">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1c4e4-529">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1c4e4-529">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1c4e4-530">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="1c4e4-530">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1c4e4-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-531">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-532">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="1c4e4-532">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1c4e4-533">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1c4e4-533">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1c4e4-534">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-534">Az.ContainerInstance</span></span>
* <span data-ttu-id="1c4e4-535">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1c4e4-535">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1c4e4-536">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1c4e4-536">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1c4e4-537">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="1c4e4-537">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1c4e4-538">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-538">Az.Network</span></span>
* <span data-ttu-id="1c4e4-539">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1c4e4-539">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1c4e4-540">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c4e4-540">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1c4e4-541">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-541">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="1c4e4-542">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1c4e4-542">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1c4e4-543">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1c4e4-543">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1c4e4-544">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-544">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1c4e4-545">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-545">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1c4e4-546">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1c4e4-546">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1c4e4-547">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1c4e4-547">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1c4e4-548">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1c4e4-548">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1c4e4-549">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1c4e4-549">Az.Relay</span></span>
* <span data-ttu-id="1c4e4-550">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-550">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1c4e4-551">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-551">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-552">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et</span><span class="sxs-lookup"><span data-stu-id="1c4e4-552">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and</span></span> `Set-AzureRmPolicyAssignment`
* <span data-ttu-id="1c4e4-553">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="1c4e4-553">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1c4e4-554">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="1c4e4-554">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1c4e4-555">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1c4e4-555">Az.ServiceFabric</span></span>
* <span data-ttu-id="1c4e4-556">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="1c4e4-556">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1c4e4-557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-557">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-558">Ajout de nouvelles cmdlets pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="1c4e4-558">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1c4e4-559">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-559">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1c4e4-560">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-560">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1c4e4-561">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-561">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1c4e4-562">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1c4e4-562">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1c4e4-563">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1c4e4-563">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1c4e4-564">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1c4e4-564">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1c4e4-565">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1c4e4-565">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1c4e4-566">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1c4e4-566">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1c4e4-567">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-567">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1c4e4-568">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-568">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1c4e4-569">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-569">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1c4e4-570">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-570">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1c4e4-571">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-571">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1c4e4-572">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-572">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1c4e4-573">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-573">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1c4e4-574">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-574">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1c4e4-575">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-575">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1c4e4-576">Généralités</span><span class="sxs-lookup"><span data-stu-id="1c4e4-576">General</span></span>
* <span data-ttu-id="1c4e4-577">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="1c4e4-577">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1c4e4-578">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-578">Az.Profile</span></span>
* <span data-ttu-id="1c4e4-579">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1c4e4-579">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1c4e4-580">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="1c4e4-580">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1c4e4-581">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1c4e4-581">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1c4e4-582">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="1c4e4-582">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1c4e4-583">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="1c4e4-583">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1c4e4-584">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="1c4e4-584">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1c4e4-585">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="1c4e4-585">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1c4e4-586">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-586">Az.CognitiveServices</span></span>
* <span data-ttu-id="1c4e4-587">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-587">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-588">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-588">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-589">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1c4e4-589">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1c4e4-590">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="1c4e4-590">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1c4e4-591">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-591">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-592">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-592">Az.DataLakeStore</span></span>
* <span data-ttu-id="1c4e4-593">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-593">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1c4e4-594">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-594">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1c4e4-595">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1c4e4-595">Az.Insights</span></span>
* <span data-ttu-id="1c4e4-596">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="1c4e4-596">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1c4e4-597">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="1c4e4-597">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1c4e4-598">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="1c4e4-598">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1c4e4-599">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="1c4e4-599">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-600">Az.Network</span></span>
* <span data-ttu-id="1c4e4-601">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="1c4e4-601">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1c4e4-602">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c4e4-602">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1c4e4-603">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1c4e4-603">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1c4e4-604">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1c4e4-604">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1c4e4-605">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1c4e4-605">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1c4e4-606">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c4e4-606">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1c4e4-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1c4e4-607">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1c4e4-608">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1c4e4-608">Az.PolicyInsights</span></span>
* <span data-ttu-id="1c4e4-609">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="1c4e4-609">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-610">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-611">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="1c4e4-611">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1c4e4-612">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-612">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1c4e4-613">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1c4e4-613">Az.ServiceBus</span></span>
* <span data-ttu-id="1c4e4-614">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-614">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1c4e4-615">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1c4e4-615">Az.ServiceFabric</span></span>
* <span data-ttu-id="1c4e4-616">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-616">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1c4e4-617">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-617">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1c4e4-618">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="1c4e4-618">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1c4e4-619">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1c4e4-619">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1c4e4-620">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-620">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1c4e4-621">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-621">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1c4e4-622">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-622">Az.Profile</span></span>
* <span data-ttu-id="1c4e4-623">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="1c4e4-623">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1c4e4-624">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1c4e4-624">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-625">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-625">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-626">Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="1c4e4-626">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1c4e4-627">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-627">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1c4e4-628">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1c4e4-628">Az.DataLakeStore</span></span>
* <span data-ttu-id="1c4e4-629">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="1c4e4-629">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1c4e4-630">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-630">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1c4e4-631">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-631">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1c4e4-632">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-632">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1c4e4-633">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-633">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-634">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-634">Az.Network</span></span>
* <span data-ttu-id="1c4e4-635">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-635">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1c4e4-636">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-636">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-637">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-638">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-638">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1c4e4-639">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="1c4e4-639">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1c4e4-640">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-640">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1c4e4-641">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-641">Azure.Storage</span></span>
* <span data-ttu-id="1c4e4-642">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1c4e4-642">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1c4e4-643">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-643">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1c4e4-644">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1c4e4-644">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1c4e4-645">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-645">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1c4e4-646">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1c4e4-646">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="1c4e4-647">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1c4e4-647">Az.CognitiveServices</span></span>
* <span data-ttu-id="1c4e4-648">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-648">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1c4e4-649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1c4e4-649">Az.Compute</span></span>
* <span data-ttu-id="1c4e4-650">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="1c4e4-650">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1c4e4-651">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-651">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1c4e4-652">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="1c4e4-652">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1c4e4-653">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1c4e4-653">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1c4e4-654">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-654">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1c4e4-655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1c4e4-655">Az.Network</span></span>
* <span data-ttu-id="1c4e4-656">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-656">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1c4e4-657">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="1c4e4-657">new cmdlets added</span></span>
    - <span data-ttu-id="1c4e4-658">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-658">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1c4e4-659">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-659">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1c4e4-660">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-660">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1c4e4-661">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1c4e4-661">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1c4e4-662">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1c4e4-662">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1c4e4-663">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1c4e4-663">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1c4e4-664">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="1c4e4-664">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1c4e4-665">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1c4e4-665">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1c4e4-666">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1c4e4-666">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1c4e4-667">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1c4e4-667">Az.RedisCache</span></span>
* <span data-ttu-id="1c4e4-668">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="1c4e4-668">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1c4e4-669">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="1c4e4-669">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1c4e4-670">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1c4e4-670">Az.Resources</span></span>
* <span data-ttu-id="1c4e4-671">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1c4e4-671">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1c4e4-672">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c4e4-672">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1c4e4-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1c4e4-673">Az.Sql</span></span>
* <span data-ttu-id="1c4e4-674">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="1c4e4-674">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1c4e4-675">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1c4e4-675">Az.Websites</span></span>
* <span data-ttu-id="1c4e4-676">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="1c4e4-676">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1c4e4-677">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="1c4e4-677">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1c4e4-678">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="1c4e4-678">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1c4e4-679">Version initiale</span><span class="sxs-lookup"><span data-stu-id="1c4e4-679">Initial Release</span></span>