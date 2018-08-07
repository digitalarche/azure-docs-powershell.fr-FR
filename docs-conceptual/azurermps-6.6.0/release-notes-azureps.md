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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368175"
---
# <a name="release-notes"></a><span data-ttu-id="3a1c2-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="3a1c2-103">Release notes</span></span>

<span data-ttu-id="3a1c2-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="3a1c2-105">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3a1c2-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="3a1c2-106">General</span></span>
* <span data-ttu-id="3a1c2-107">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3a1c2-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-108">AzureRM.Profile</span></span>
* <span data-ttu-id="3a1c2-109">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="3a1c2-110">Par défaut, ce sont toujours de vraies ressources individuelles et elles remplacent la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="3a1c2-111">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3a1c2-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-112">Azure.Storage</span></span>
* <span data-ttu-id="3a1c2-113">Le support obtient le contexte de stockage à partir de DefaulfProfile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="3a1c2-114">Ajoute de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3a1c2-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a1c2-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3a1c2-116">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="3a1c2-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="3a1c2-117">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="3a1c2-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="3a1c2-118">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="3a1c2-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="3a1c2-119">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="3a1c2-120">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="3a1c2-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="3a1c2-121">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="3a1c2-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3a1c2-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3a1c2-122">AzureRM.Compute</span></span>
* <span data-ttu-id="3a1c2-123">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="3a1c2-124">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="3a1c2-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="3a1c2-125">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="3a1c2-126">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="3a1c2-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="3a1c2-127">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="3a1c2-128">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="3a1c2-129">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3a1c2-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="3a1c2-130">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="3a1c2-131">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="3a1c2-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="3a1c2-132">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3a1c2-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3a1c2-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3a1c2-134">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="3a1c2-135">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="3a1c2-136">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="3a1c2-137">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3a1c2-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a1c2-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3a1c2-139">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="3a1c2-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3a1c2-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a1c2-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="3a1c2-141">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="3a1c2-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3a1c2-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3a1c2-142">AzureRM.Insights</span></span>
* <span data-ttu-id="3a1c2-143">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="3a1c2-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="3a1c2-144">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a1c2-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3a1c2-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a1c2-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3a1c2-146">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3a1c2-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3a1c2-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3a1c2-147">AzureRM.Network</span></span>
* <span data-ttu-id="3a1c2-148">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3a1c2-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3a1c2-149">AzureRM.Resources</span></span>
* <span data-ttu-id="3a1c2-150">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="3a1c2-151">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3a1c2-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a1c2-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3a1c2-153">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="3a1c2-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="3a1c2-154">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="3a1c2-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="3a1c2-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3a1c2-155">AzureRM.Sql</span></span>
* <span data-ttu-id="3a1c2-156">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="3a1c2-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a1c2-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3a1c2-158">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="3a1c2-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="3a1c2-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="3a1c2-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="3a1c2-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="3a1c2-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="3a1c2-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="3a1c2-162">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3a1c2-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="3a1c2-163">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="3a1c2-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3a1c2-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-164">AzureRM.Storage</span></span>
* <span data-ttu-id="3a1c2-165">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a1c2-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="3a1c2-166">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="3a1c2-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="3a1c2-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a1c2-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3a1c2-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a1c2-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3a1c2-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a1c2-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3a1c2-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3a1c2-170">AzureRM.Tags</span></span>
* <span data-ttu-id="3a1c2-171">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="3a1c2-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="3a1c2-172">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3a1c2-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-173">AzureRM.Profile</span></span>
* <span data-ttu-id="3a1c2-174">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3a1c2-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-175">Azure.Storage</span></span>
* <span data-ttu-id="3a1c2-176">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="3a1c2-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="3a1c2-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a1c2-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="3a1c2-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a1c2-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3a1c2-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a1c2-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3a1c2-180">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3a1c2-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3a1c2-181">AzureRM.Automation</span></span>
* <span data-ttu-id="3a1c2-182">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3a1c2-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3a1c2-183">AzureRM.Compute</span></span>
* <span data-ttu-id="3a1c2-184">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3a1c2-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="3a1c2-185">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3a1c2-186">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3a1c2-187">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="3a1c2-188">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3a1c2-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a1c2-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="3a1c2-190">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="3a1c2-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3a1c2-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a1c2-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3a1c2-192">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3a1c2-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3a1c2-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a1c2-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3a1c2-194">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3a1c2-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3a1c2-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3a1c2-195">AzureRM.Network</span></span>
* <span data-ttu-id="3a1c2-196">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="3a1c2-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="3a1c2-197">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="3a1c2-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="3a1c2-198">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="3a1c2-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="3a1c2-199">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3a1c2-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="3a1c2-200">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3a1c2-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="3a1c2-201">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="3a1c2-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3a1c2-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3a1c2-202">AzureRM.Relay</span></span>
* <span data-ttu-id="3a1c2-203">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="3a1c2-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3a1c2-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3a1c2-204">AzureRM.Resources</span></span>
* <span data-ttu-id="3a1c2-205">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="3a1c2-206">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="3a1c2-207">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3a1c2-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="3a1c2-208">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="3a1c2-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="3a1c2-209">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="3a1c2-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3a1c2-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a1c2-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3a1c2-211">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="3a1c2-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="3a1c2-212">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="3a1c2-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3a1c2-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3a1c2-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3a1c2-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3a1c2-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="3a1c2-218">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="3a1c2-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3a1c2-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a1c2-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3a1c2-220">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3a1c2-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3a1c2-221">AzureRM.Sql</span></span>
* <span data-ttu-id="3a1c2-222">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="3a1c2-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="3a1c2-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1c2-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="3a1c2-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1c2-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3a1c2-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3a1c2-225">AzureRM.Websites</span></span>
* <span data-ttu-id="3a1c2-226">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="3a1c2-227">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="3a1c2-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="3a1c2-228">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="3a1c2-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="3a1c2-229">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3a1c2-230">Généralités</span><span class="sxs-lookup"><span data-stu-id="3a1c2-230">General</span></span>
* <span data-ttu-id="3a1c2-231">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="3a1c2-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3a1c2-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-232">AzureRM.Profile</span></span>
* <span data-ttu-id="3a1c2-233">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="3a1c2-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3a1c2-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3a1c2-234">AzureRM.Compute</span></span>
* <span data-ttu-id="3a1c2-235">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="3a1c2-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="3a1c2-236">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="3a1c2-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="3a1c2-237">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a1c2-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="3a1c2-238">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="3a1c2-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="3a1c2-239">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="3a1c2-240">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="3a1c2-241">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3a1c2-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3a1c2-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3a1c2-243">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="3a1c2-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3a1c2-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3a1c2-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3a1c2-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3a1c2-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3a1c2-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3a1c2-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a1c2-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3a1c2-248">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="3a1c2-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3a1c2-249">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="3a1c2-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3a1c2-250">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="3a1c2-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="3a1c2-251">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="3a1c2-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3a1c2-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a1c2-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="3a1c2-253">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3a1c2-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="3a1c2-254">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="3a1c2-255">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="3a1c2-256">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3a1c2-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a1c2-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3a1c2-258">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="3a1c2-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3a1c2-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3a1c2-259">AzureRM.Network</span></span>
* <span data-ttu-id="3a1c2-260">Exposer les nouvelles références SKU pour Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="3a1c2-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="3a1c2-261">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="3a1c2-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="3a1c2-262">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3a1c2-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3a1c2-263">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3a1c2-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3a1c2-264">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3a1c2-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3a1c2-265">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3a1c2-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3a1c2-266">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3a1c2-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3a1c2-267">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3a1c2-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3a1c2-268">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a1c2-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3a1c2-269">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a1c2-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3a1c2-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3a1c2-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3a1c2-271">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="3a1c2-272">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="3a1c2-273">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3a1c2-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3a1c2-274">AzureRM.Resources</span></span>
* <span data-ttu-id="3a1c2-275">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="3a1c2-276">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="3a1c2-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="3a1c2-277">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="3a1c2-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="3a1c2-278">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="3a1c2-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="3a1c2-279">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3a1c2-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="3a1c2-280">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="3a1c2-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3a1c2-281">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="3a1c2-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3a1c2-282">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3a1c2-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="3a1c2-283">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="3a1c2-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3a1c2-284">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="3a1c2-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3a1c2-285">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3a1c2-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="3a1c2-286">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3a1c2-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="3a1c2-287">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="3a1c2-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="3a1c2-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a1c2-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3a1c2-289">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3a1c2-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3a1c2-290">AzureRM.Sql</span></span>
* <span data-ttu-id="3a1c2-291">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="3a1c2-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="3a1c2-292">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a1c2-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="3a1c2-293">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3a1c2-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-294">AzureRM.Profile</span></span>
* <span data-ttu-id="3a1c2-295">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="3a1c2-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="3a1c2-296">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="3a1c2-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3a1c2-297">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-297">Azure.Storage</span></span>
* <span data-ttu-id="3a1c2-298">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3a1c2-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3a1c2-299">AzureRM.Compute</span></span>
* <span data-ttu-id="3a1c2-300">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="3a1c2-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="3a1c2-301">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="3a1c2-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="3a1c2-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3a1c2-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3a1c2-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3a1c2-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3a1c2-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3a1c2-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3a1c2-305">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="3a1c2-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a1c2-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="3a1c2-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a1c2-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="3a1c2-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a1c2-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="3a1c2-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3a1c2-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="3a1c2-310">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="3a1c2-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="3a1c2-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="3a1c2-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3a1c2-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="3a1c2-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3a1c2-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="3a1c2-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="3a1c2-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="3a1c2-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="3a1c2-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3a1c2-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="3a1c2-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3a1c2-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="3a1c2-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3a1c2-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3a1c2-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="3a1c2-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="3a1c2-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3a1c2-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3a1c2-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3a1c2-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="3a1c2-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3a1c2-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="3a1c2-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3a1c2-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3a1c2-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a1c2-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3a1c2-326">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3a1c2-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a1c2-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3a1c2-328">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="3a1c2-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3a1c2-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a1c2-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3a1c2-330">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="3a1c2-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="3a1c2-331">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="3a1c2-332">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="3a1c2-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3a1c2-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3a1c2-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3a1c2-334">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="3a1c2-335">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3a1c2-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3a1c2-336">AzureRM.Sql</span></span>
* <span data-ttu-id="3a1c2-337">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="3a1c2-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3a1c2-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3a1c2-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3a1c2-339">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3a1c2-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3a1c2-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3a1c2-340">AzureRM.Websites</span></span>
* <span data-ttu-id="3a1c2-341">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3a1c2-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="3a1c2-342">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3a1c2-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="3a1c2-343">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="3a1c2-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a1c2-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3a1c2-345">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="3a1c2-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="3a1c2-346">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3a1c2-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-347">AzureRM.Profile</span></span>
* <span data-ttu-id="3a1c2-348">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="3a1c2-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3a1c2-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3a1c2-349">AzureRM.Compute</span></span>
* <span data-ttu-id="3a1c2-350">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="3a1c2-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="3a1c2-351">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="3a1c2-352">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3a1c2-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3a1c2-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3a1c2-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3a1c2-354">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="3a1c2-355">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="3a1c2-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="3a1c2-356">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="3a1c2-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="3a1c2-357">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="3a1c2-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="3a1c2-358">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="3a1c2-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="3a1c2-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a1c2-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3a1c2-360">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="3a1c2-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="3a1c2-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3a1c2-361">AzureRM.Network</span></span>
* <span data-ttu-id="3a1c2-362">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="3a1c2-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3a1c2-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3a1c2-363">AzureRM.Resources</span></span>
* <span data-ttu-id="3a1c2-364">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="3a1c2-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3a1c2-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3a1c2-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3a1c2-366">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="3a1c2-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="3a1c2-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3a1c2-367">AzureRM.Sql</span></span>
* <span data-ttu-id="3a1c2-368">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="3a1c2-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="3a1c2-369">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a1c2-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3a1c2-370">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3a1c2-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3a1c2-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3a1c2-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3a1c2-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3a1c2-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3a1c2-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a1c2-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3a1c2-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3a1c2-374">AzureRM.Websites</span></span>
* <span data-ttu-id="3a1c2-375">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="3a1c2-376">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="3a1c2-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3a1c2-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3a1c2-377">AzureRM.Profile</span></span>
* <span data-ttu-id="3a1c2-378">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="3a1c2-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3a1c2-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a1c2-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3a1c2-380">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="3a1c2-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3a1c2-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a1c2-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3a1c2-382">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="3a1c2-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="3a1c2-383">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a1c2-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="3a1c2-384">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="3a1c2-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="3a1c2-385">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="3a1c2-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="3a1c2-386">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="3a1c2-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="3a1c2-387">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="3a1c2-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="3a1c2-388">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="3a1c2-388">Added support for MSI identity</span></span>
* <span data-ttu-id="3a1c2-389">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="3a1c2-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3a1c2-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="3a1c2-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="3a1c2-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3a1c2-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="3a1c2-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3a1c2-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3a1c2-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3a1c2-394">AzureRM.Batch</span></span>
* <span data-ttu-id="3a1c2-395">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="3a1c2-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="3a1c2-396">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="3a1c2-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3a1c2-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="3a1c2-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="3a1c2-398">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="3a1c2-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3a1c2-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a1c2-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3a1c2-400">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="3a1c2-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3a1c2-401">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3a1c2-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="3a1c2-402">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3a1c2-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="3a1c2-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3a1c2-403">AzureRM.Network</span></span>
* <span data-ttu-id="3a1c2-404">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="3a1c2-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="3a1c2-405">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="3a1c2-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a1c2-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="3a1c2-407">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="3a1c2-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a1c2-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3a1c2-409">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="3a1c2-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a1c2-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3a1c2-411">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="3a1c2-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3a1c2-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3a1c2-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a1c2-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3a1c2-414">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="3a1c2-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3a1c2-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3a1c2-415">AzureRM.Sql</span></span>
* <span data-ttu-id="3a1c2-416">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a1c2-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="3a1c2-417">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="3a1c2-418">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="3a1c2-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="3a1c2-419">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="3a1c2-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="3a1c2-420">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="3a1c2-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="3a1c2-421">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a1c2-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3a1c2-422">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3a1c2-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3a1c2-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3a1c2-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3a1c2-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3a1c2-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3a1c2-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3a1c2-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3a1c2-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3a1c2-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3a1c2-427">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="3a1c2-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>