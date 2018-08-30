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
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018799"
---
# <a name="release-notes"></a><span data-ttu-id="6da7a-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="6da7a-103">Release notes</span></span>

<span data-ttu-id="6da7a-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="6da7a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="6da7a-105">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6da7a-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="6da7a-106">General</span></span>
* <span data-ttu-id="6da7a-107">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="6da7a-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6da7a-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6da7a-108">AzureRM.Profile</span></span>
* <span data-ttu-id="6da7a-109">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="6da7a-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="6da7a-110">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="6da7a-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6da7a-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6da7a-111">Azure.Storage</span></span>
* <span data-ttu-id="6da7a-112">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="6da7a-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="6da7a-113">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6da7a-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6da7a-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6da7a-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6da7a-115">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="6da7a-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="6da7a-116">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="6da7a-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="6da7a-117">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="6da7a-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="6da7a-118">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="6da7a-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="6da7a-119">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="6da7a-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="6da7a-120">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="6da7a-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6da7a-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6da7a-121">AzureRM.Compute</span></span>
* <span data-ttu-id="6da7a-122">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="6da7a-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="6da7a-123">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="6da7a-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="6da7a-124">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="6da7a-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="6da7a-125">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="6da7a-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="6da7a-126">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="6da7a-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="6da7a-127">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="6da7a-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="6da7a-128">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6da7a-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="6da7a-129">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="6da7a-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="6da7a-130">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6da7a-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="6da7a-131">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="6da7a-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6da7a-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6da7a-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6da7a-133">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="6da7a-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="6da7a-134">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="6da7a-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="6da7a-135">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6da7a-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="6da7a-136">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="6da7a-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6da7a-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6da7a-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6da7a-138">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="6da7a-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6da7a-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6da7a-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="6da7a-140">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="6da7a-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="6da7a-141">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="6da7a-141">AzureRM.Insights</span></span>
* <span data-ttu-id="6da7a-142">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="6da7a-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="6da7a-143">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="6da7a-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6da7a-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6da7a-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6da7a-145">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6da7a-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6da7a-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6da7a-146">AzureRM.Network</span></span>
* <span data-ttu-id="6da7a-147">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="6da7a-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6da7a-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6da7a-148">AzureRM.Resources</span></span>
* <span data-ttu-id="6da7a-149">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="6da7a-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="6da7a-150">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="6da7a-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6da7a-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6da7a-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6da7a-152">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="6da7a-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="6da7a-153">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="6da7a-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="6da7a-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6da7a-154">AzureRM.Sql</span></span>
* <span data-ttu-id="6da7a-155">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="6da7a-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="6da7a-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6da7a-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6da7a-157">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="6da7a-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="6da7a-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="6da7a-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="6da7a-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="6da7a-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="6da7a-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="6da7a-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="6da7a-161">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6da7a-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="6da7a-162">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="6da7a-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="6da7a-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="6da7a-163">AzureRM.Storage</span></span>
* <span data-ttu-id="6da7a-164">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="6da7a-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="6da7a-165">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="6da7a-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="6da7a-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6da7a-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6da7a-167">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6da7a-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="6da7a-168">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6da7a-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="6da7a-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="6da7a-169">AzureRM.Tags</span></span>
* <span data-ttu-id="6da7a-170">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="6da7a-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="6da7a-171">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6da7a-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6da7a-172">AzureRM.Profile</span></span>
* <span data-ttu-id="6da7a-173">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="6da7a-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6da7a-174">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6da7a-174">Azure.Storage</span></span>
* <span data-ttu-id="6da7a-175">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="6da7a-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="6da7a-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6da7a-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="6da7a-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6da7a-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6da7a-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6da7a-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6da7a-179">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="6da7a-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="6da7a-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="6da7a-180">AzureRM.Automation</span></span>
* <span data-ttu-id="6da7a-181">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="6da7a-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6da7a-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6da7a-182">AzureRM.Compute</span></span>
* <span data-ttu-id="6da7a-183">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6da7a-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="6da7a-184">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="6da7a-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6da7a-185">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="6da7a-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="6da7a-186">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="6da7a-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="6da7a-187">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="6da7a-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6da7a-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6da7a-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="6da7a-189">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="6da7a-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6da7a-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6da7a-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6da7a-191">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6da7a-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="6da7a-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6da7a-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="6da7a-193">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6da7a-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6da7a-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6da7a-194">AzureRM.Network</span></span>
* <span data-ttu-id="6da7a-195">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6da7a-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="6da7a-196">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6da7a-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="6da7a-197">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="6da7a-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="6da7a-198">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6da7a-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="6da7a-199">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="6da7a-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="6da7a-200">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="6da7a-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="6da7a-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="6da7a-201">AzureRM.Relay</span></span>
* <span data-ttu-id="6da7a-202">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="6da7a-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6da7a-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6da7a-203">AzureRM.Resources</span></span>
* <span data-ttu-id="6da7a-204">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="6da7a-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="6da7a-205">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="6da7a-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="6da7a-206">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6da7a-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="6da7a-207">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="6da7a-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="6da7a-208">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="6da7a-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="6da7a-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6da7a-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6da7a-210">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="6da7a-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="6da7a-211">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="6da7a-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="6da7a-212">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6da7a-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6da7a-213">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6da7a-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6da7a-214">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6da7a-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6da7a-215">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6da7a-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="6da7a-216">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="6da7a-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="6da7a-217">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="6da7a-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6da7a-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6da7a-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6da7a-219">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="6da7a-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6da7a-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6da7a-220">AzureRM.Sql</span></span>
* <span data-ttu-id="6da7a-221">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="6da7a-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="6da7a-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6da7a-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="6da7a-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="6da7a-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6da7a-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6da7a-224">AzureRM.Websites</span></span>
* <span data-ttu-id="6da7a-225">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="6da7a-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="6da7a-226">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="6da7a-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="6da7a-227">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="6da7a-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="6da7a-228">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6da7a-229">Généralités</span><span class="sxs-lookup"><span data-stu-id="6da7a-229">General</span></span>
* <span data-ttu-id="6da7a-230">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="6da7a-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="6da7a-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6da7a-231">AzureRM.Profile</span></span>
* <span data-ttu-id="6da7a-232">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="6da7a-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6da7a-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6da7a-233">AzureRM.Compute</span></span>
* <span data-ttu-id="6da7a-234">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="6da7a-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="6da7a-235">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="6da7a-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="6da7a-236">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="6da7a-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="6da7a-237">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="6da7a-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="6da7a-238">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="6da7a-239">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="6da7a-240">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="6da7a-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6da7a-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="6da7a-242">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6da7a-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="6da7a-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6da7a-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6da7a-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6da7a-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="6da7a-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6da7a-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6da7a-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6da7a-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6da7a-247">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6da7a-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="6da7a-248">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6da7a-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6da7a-249">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="6da7a-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="6da7a-250">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="6da7a-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="6da7a-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="6da7a-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="6da7a-252">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6da7a-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="6da7a-253">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="6da7a-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="6da7a-254">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="6da7a-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="6da7a-255">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6da7a-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6da7a-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6da7a-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6da7a-257">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="6da7a-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="6da7a-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6da7a-258">AzureRM.Network</span></span>
* <span data-ttu-id="6da7a-259">Exposer les nouvelles références SKU pour Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6da7a-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="6da7a-260">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="6da7a-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="6da7a-261">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6da7a-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6da7a-262">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6da7a-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="6da7a-263">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6da7a-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6da7a-264">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6da7a-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6da7a-265">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6da7a-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="6da7a-266">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6da7a-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6da7a-267">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6da7a-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6da7a-268">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6da7a-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6da7a-269">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6da7a-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6da7a-270">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="6da7a-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="6da7a-271">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="6da7a-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="6da7a-272">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="6da7a-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6da7a-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6da7a-273">AzureRM.Resources</span></span>
* <span data-ttu-id="6da7a-274">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="6da7a-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="6da7a-275">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="6da7a-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="6da7a-276">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="6da7a-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="6da7a-277">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="6da7a-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="6da7a-278">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6da7a-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="6da7a-279">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="6da7a-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6da7a-280">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="6da7a-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6da7a-281">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="6da7a-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="6da7a-282">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="6da7a-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="6da7a-283">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="6da7a-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="6da7a-284">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6da7a-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="6da7a-285">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6da7a-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="6da7a-286">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="6da7a-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="6da7a-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6da7a-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="6da7a-288">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6da7a-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6da7a-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6da7a-289">AzureRM.Sql</span></span>
* <span data-ttu-id="6da7a-290">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="6da7a-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="6da7a-291">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="6da7a-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="6da7a-292">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6da7a-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6da7a-293">AzureRM.Profile</span></span>
* <span data-ttu-id="6da7a-294">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="6da7a-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="6da7a-295">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="6da7a-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="6da7a-296">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6da7a-296">Azure.Storage</span></span>
* <span data-ttu-id="6da7a-297">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="6da7a-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6da7a-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6da7a-298">AzureRM.Compute</span></span>
* <span data-ttu-id="6da7a-299">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="6da7a-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="6da7a-300">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="6da7a-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="6da7a-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6da7a-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6da7a-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6da7a-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6da7a-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="6da7a-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="6da7a-304">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="6da7a-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="6da7a-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6da7a-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="6da7a-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6da7a-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="6da7a-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6da7a-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="6da7a-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6da7a-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="6da7a-309">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="6da7a-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="6da7a-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="6da7a-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="6da7a-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="6da7a-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="6da7a-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="6da7a-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="6da7a-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="6da7a-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="6da7a-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6da7a-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="6da7a-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6da7a-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="6da7a-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="6da7a-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="6da7a-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6da7a-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="6da7a-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6da7a-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="6da7a-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6da7a-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="6da7a-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="6da7a-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="6da7a-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6da7a-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="6da7a-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6da7a-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="6da7a-325">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6da7a-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="6da7a-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6da7a-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6da7a-327">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="6da7a-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="6da7a-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6da7a-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="6da7a-329">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="6da7a-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="6da7a-330">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="6da7a-331">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6da7a-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="6da7a-332">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6da7a-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6da7a-333">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="6da7a-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="6da7a-334">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="6da7a-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6da7a-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6da7a-335">AzureRM.Sql</span></span>
* <span data-ttu-id="6da7a-336">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="6da7a-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6da7a-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6da7a-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6da7a-338">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6da7a-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6da7a-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6da7a-339">AzureRM.Websites</span></span>
* <span data-ttu-id="6da7a-340">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="6da7a-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="6da7a-341">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6da7a-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="6da7a-342">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="6da7a-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6da7a-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="6da7a-344">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="6da7a-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="6da7a-345">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6da7a-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6da7a-346">AzureRM.Profile</span></span>
* <span data-ttu-id="6da7a-347">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="6da7a-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="6da7a-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="6da7a-348">AzureRM.Compute</span></span>
* <span data-ttu-id="6da7a-349">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="6da7a-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="6da7a-350">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="6da7a-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="6da7a-351">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="6da7a-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="6da7a-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6da7a-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="6da7a-353">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="6da7a-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="6da7a-354">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="6da7a-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="6da7a-355">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="6da7a-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="6da7a-356">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="6da7a-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="6da7a-357">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="6da7a-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="6da7a-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6da7a-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="6da7a-359">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="6da7a-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="6da7a-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6da7a-360">AzureRM.Network</span></span>
* <span data-ttu-id="6da7a-361">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="6da7a-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="6da7a-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="6da7a-362">AzureRM.Resources</span></span>
* <span data-ttu-id="6da7a-363">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="6da7a-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="6da7a-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="6da7a-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="6da7a-365">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="6da7a-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="6da7a-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6da7a-366">AzureRM.Sql</span></span>
* <span data-ttu-id="6da7a-367">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="6da7a-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="6da7a-368">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6da7a-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6da7a-369">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6da7a-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6da7a-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6da7a-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6da7a-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6da7a-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6da7a-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6da7a-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="6da7a-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="6da7a-373">AzureRM.Websites</span></span>
* <span data-ttu-id="6da7a-374">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="6da7a-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="6da7a-375">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="6da7a-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6da7a-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6da7a-376">AzureRM.Profile</span></span>
* <span data-ttu-id="6da7a-377">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="6da7a-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6da7a-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6da7a-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6da7a-379">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="6da7a-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6da7a-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6da7a-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6da7a-381">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="6da7a-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6da7a-382">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6da7a-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6da7a-383">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="6da7a-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6da7a-384">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="6da7a-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6da7a-385">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="6da7a-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6da7a-386">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="6da7a-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6da7a-387">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="6da7a-387">Added support for MSI identity</span></span>
* <span data-ttu-id="6da7a-388">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="6da7a-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6da7a-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6da7a-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6da7a-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6da7a-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6da7a-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6da7a-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6da7a-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6da7a-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6da7a-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6da7a-393">AzureRM.Batch</span></span>
* <span data-ttu-id="6da7a-394">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6da7a-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6da7a-395">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6da7a-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6da7a-396">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6da7a-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="6da7a-397">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="6da7a-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6da7a-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6da7a-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6da7a-399">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="6da7a-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6da7a-400">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6da7a-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6da7a-401">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="6da7a-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6da7a-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6da7a-402">AzureRM.Network</span></span>
* <span data-ttu-id="6da7a-403">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="6da7a-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6da7a-404">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="6da7a-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6da7a-405">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6da7a-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6da7a-406">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="6da7a-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6da7a-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6da7a-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6da7a-408">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="6da7a-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6da7a-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6da7a-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6da7a-410">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="6da7a-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6da7a-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6da7a-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6da7a-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6da7a-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6da7a-413">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="6da7a-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6da7a-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6da7a-414">AzureRM.Sql</span></span>
* <span data-ttu-id="6da7a-415">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="6da7a-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6da7a-416">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="6da7a-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6da7a-417">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="6da7a-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6da7a-418">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="6da7a-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6da7a-419">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="6da7a-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6da7a-420">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6da7a-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6da7a-421">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6da7a-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6da7a-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6da7a-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6da7a-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6da7a-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6da7a-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6da7a-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6da7a-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6da7a-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6da7a-426">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="6da7a-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
