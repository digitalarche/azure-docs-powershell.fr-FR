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
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237687"
---
# <a name="release-notes"></a><span data-ttu-id="093ea-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="093ea-103">Release notes</span></span>

<span data-ttu-id="093ea-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="093ea-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="093ea-105">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="093ea-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="093ea-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="093ea-106">AzureRM.Profile</span></span>
* <span data-ttu-id="093ea-107">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="093ea-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="093ea-108">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande « Connect-AzureRmAccount » sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="093ea-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="093ea-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="093ea-109">Azure.Storage</span></span>
* <span data-ttu-id="093ea-110">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="093ea-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="093ea-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="093ea-111">AzureRM.Compute</span></span>
* <span data-ttu-id="093ea-112">« Get-AzureRmVmDiskEncryptionStatus » résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="093ea-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="093ea-113">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="093ea-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="093ea-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="093ea-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="093ea-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="093ea-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="093ea-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="093ea-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="093ea-117">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="093ea-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="093ea-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="093ea-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="093ea-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="093ea-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="093ea-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="093ea-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="093ea-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="093ea-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="093ea-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="093ea-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="093ea-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="093ea-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="093ea-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="093ea-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="093ea-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="093ea-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="093ea-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="093ea-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="093ea-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="093ea-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="093ea-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="093ea-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="093ea-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="093ea-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="093ea-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="093ea-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="093ea-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="093ea-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="093ea-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="093ea-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="093ea-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="093ea-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="093ea-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="093ea-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="093ea-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="093ea-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="093ea-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="093ea-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="093ea-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="093ea-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="093ea-138">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="093ea-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="093ea-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="093ea-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="093ea-140">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="093ea-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="093ea-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="093ea-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="093ea-142">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="093ea-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="093ea-143">Utiliser l'API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="093ea-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="093ea-144">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="093ea-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="093ea-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="093ea-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="093ea-146">Ajout de paramètre de coffre aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="093ea-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="093ea-147">Lorsqu’envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="093ea-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="093ea-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="093ea-148">AzureRM.Sql</span></span>
* <span data-ttu-id="093ea-149">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="093ea-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="093ea-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="093ea-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="093ea-151">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="093ea-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="093ea-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="093ea-152">AzureRM.Websites</span></span>
* <span data-ttu-id="093ea-153">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="093ea-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="093ea-154">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="093ea-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="093ea-155">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="093ea-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="093ea-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="093ea-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="093ea-157">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="093ea-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="093ea-158">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="093ea-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="093ea-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="093ea-159">AzureRM.Profile</span></span>
* <span data-ttu-id="093ea-160">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="093ea-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="093ea-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="093ea-161">AzureRM.Compute</span></span>
* <span data-ttu-id="093ea-162">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="093ea-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="093ea-163">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="093ea-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="093ea-164">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="093ea-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="093ea-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="093ea-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="093ea-166">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="093ea-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="093ea-167">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="093ea-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="093ea-168">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="093ea-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="093ea-169">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="093ea-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="093ea-170">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="093ea-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="093ea-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="093ea-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="093ea-172">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="093ea-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="093ea-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="093ea-173">AzureRM.Network</span></span>
* <span data-ttu-id="093ea-174">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="093ea-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="093ea-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="093ea-175">AzureRM.Resources</span></span>
* <span data-ttu-id="093ea-176">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="093ea-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="093ea-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="093ea-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="093ea-178">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="093ea-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="093ea-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="093ea-179">AzureRM.Sql</span></span>
* <span data-ttu-id="093ea-180">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="093ea-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="093ea-181">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="093ea-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="093ea-182">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="093ea-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="093ea-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="093ea-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="093ea-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="093ea-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="093ea-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="093ea-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="093ea-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="093ea-186">AzureRM.Websites</span></span>
* <span data-ttu-id="093ea-187">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="093ea-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="093ea-188">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="093ea-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="093ea-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="093ea-189">AzureRM.Profile</span></span>
* <span data-ttu-id="093ea-190">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="093ea-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="093ea-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="093ea-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="093ea-192">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="093ea-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="093ea-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="093ea-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="093ea-194">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="093ea-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="093ea-195">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="093ea-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="093ea-196">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="093ea-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="093ea-197">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="093ea-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="093ea-198">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="093ea-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="093ea-199">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="093ea-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="093ea-200">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="093ea-200">Added support for MSI identity</span></span>
* <span data-ttu-id="093ea-201">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="093ea-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="093ea-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="093ea-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="093ea-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="093ea-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="093ea-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="093ea-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="093ea-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="093ea-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="093ea-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="093ea-206">AzureRM.Batch</span></span>
* <span data-ttu-id="093ea-207">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="093ea-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="093ea-208">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="093ea-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="093ea-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="093ea-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="093ea-210">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="093ea-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="093ea-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="093ea-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="093ea-212">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="093ea-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="093ea-213">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="093ea-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="093ea-214">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="093ea-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="093ea-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="093ea-215">AzureRM.Network</span></span>
* <span data-ttu-id="093ea-216">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="093ea-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="093ea-217">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="093ea-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="093ea-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="093ea-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="093ea-219">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="093ea-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="093ea-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="093ea-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="093ea-221">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="093ea-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="093ea-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="093ea-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="093ea-223">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="093ea-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="093ea-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="093ea-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="093ea-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="093ea-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="093ea-226">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="093ea-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="093ea-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="093ea-227">AzureRM.Sql</span></span>
* <span data-ttu-id="093ea-228">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="093ea-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="093ea-229">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="093ea-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="093ea-230">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="093ea-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="093ea-231">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="093ea-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="093ea-232">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="093ea-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="093ea-233">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="093ea-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="093ea-234">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="093ea-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="093ea-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="093ea-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="093ea-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="093ea-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="093ea-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="093ea-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="093ea-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="093ea-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="093ea-239">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="093ea-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>