---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: "Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-resource-manager
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5c8fa2a5a8f94cd24b66f42c237749a7b89af3b3
ms.sourcegitcommit: ec0b3565264ff7c9f03315ded182f3d5cce534fc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2017
---
# <a name="release-notes"></a><span data-ttu-id="c070c-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="c070c-103">Release notes</span></span>

<span data-ttu-id="c070c-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="c070c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-400"></a><span data-ttu-id="c070c-105">Version 4.0.0</span><span class="sxs-lookup"><span data-stu-id="c070c-105">Version 4.0.0</span></span>

* <span data-ttu-id="c070c-106">Cette version contient des modifications conséquentes.</span><span class="sxs-lookup"><span data-stu-id="c070c-106">This release contains breaking changes.</span></span> <span data-ttu-id="c070c-107">Consultez [le guide de migration](https://aka.ms/azps-migration-guide) pour connaître les détails des changements et leur impact sur les scripts existants.</span><span class="sxs-lookup"><span data-stu-id="c070c-107">Please see [the migration guide](https://aka.ms/azps-migration-guide) for change details and the impact on existing scripts.</span></span>
* <span data-ttu-id="c070c-108">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c070c-108">ApiManagement</span></span>
  - <span data-ttu-id="c070c-109">Prise en charge ajoutée pour la configuration de groupes externes dans New-AzureRmApiManagementGroup.</span><span class="sxs-lookup"><span data-stu-id="c070c-109">Added support for configuring external groups in New-AzureRmApiManagementGroup.</span></span>
* <span data-ttu-id="c070c-110">Facturation</span><span class="sxs-lookup"><span data-stu-id="c070c-110">Billing</span></span>
  - <span data-ttu-id="c070c-111">Nouvelle applet de commande Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="c070c-111">New Cmdlet Get-AzureRmBillingPeriod</span></span>
    + <span data-ttu-id="c070c-112">applet de commande pour récupérer les périodes de facturation Azure de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c070c-112">cmdlet to retrieve azure billing periods of the subscription.</span></span>
  - <span data-ttu-id="c070c-113">Mise à jour de l’applet de commande Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="c070c-113">Update Cmdlet Get-AzureRmBillingInvoice</span></span>
  - <span data-ttu-id="c070c-114">nouvelle propriété BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="c070c-114">new property BillingPeriodNames</span></span>
  - <span data-ttu-id="c070c-115">sortie dans affichage de liste</span><span class="sxs-lookup"><span data-stu-id="c070c-115">output in list view</span></span>
* <span data-ttu-id="c070c-116">Calcul</span><span class="sxs-lookup"><span data-stu-id="c070c-116">Compute</span></span>
  - <span data-ttu-id="c070c-117">Mise à jour des applets de commande Set-AzureRmVMAEMExtension et Test-AzureRmVMAEMExtension pour prendre en charge les disques gérés Premium</span><span class="sxs-lookup"><span data-stu-id="c070c-117">Updated Set-AzureRmVMAEMExtension and Test-AzureRmVMAEMExtension cmdlets to support Premium managed disks</span></span>
  - <span data-ttu-id="c070c-118">Paramètres de chiffrement de sauvegarde pour les machines virtuelles IaaS et restauration en cas d’échec</span><span class="sxs-lookup"><span data-stu-id="c070c-118">Backup encryption settings for IaaS VMs and restore on failure</span></span>
  - <span data-ttu-id="c070c-119">L’option ChefServiceInterval est renommée en ChefDaemonInterval maintenant.</span><span class="sxs-lookup"><span data-stu-id="c070c-119">ChefServiceInterval option is renamed to ChefDaemonInterval now.</span></span> <span data-ttu-id="c070c-120">L’ancien continuera à fonctionner, cependant.</span><span class="sxs-lookup"><span data-stu-id="c070c-120">Old one will continue to work however.</span></span>
  - <span data-ttu-id="c070c-121">Suppression des propriétés DataDiskNames et NetworkInterfaceIDs en double de l’objet de machine virtuelle PS.</span><span class="sxs-lookup"><span data-stu-id="c070c-121">Remove duplicated DataDiskNames and NetworkInterfaceIDs properties from PS VM object.</span></span>
  - <span data-ttu-id="c070c-122">Paramètres DataDiskNames et NetworkInterfaceIDs rendus facultatifs dans Remove-AzureRmVMDataDisk et Remove-AzureRmVMNetworkInterface, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c070c-122">Make DataDiskNames and NetworkInterfaceIDs parameters optional in Remove-AzureRmVMDataDisk and Remove-AzureRmVMNetworkInterface, respectively.</span></span>
  - <span data-ttu-id="c070c-123">Corrigez le problème de combinaison d’applets de commande Get quand les applets de commande Get retournent un objet de liste.</span><span class="sxs-lookup"><span data-stu-id="c070c-123">Fix the piping issue of Get cmdlets when the Get cmdlets return a list object.</span></span>
  - <span data-ttu-id="c070c-124">Les applets de commande qui sont en conflit avec les applets de commande RDFE ont été renommées.</span><span class="sxs-lookup"><span data-stu-id="c070c-124">Cmdlets that conflicted with RDFE cmdlets have been renamed.</span></span> <span data-ttu-id="c070c-125">Consultez la page du problème https://github.com/Azure/azure-powershell/issues/2917 pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="c070c-125">See issue https://github.com/Azure/azure-powershell/issues/2917 for more details</span></span>
    + <span data-ttu-id="c070c-126">`New-AzureVMSqlServerAutoBackupConfig` a été renommé en `New-AzureRmVMSqlServerAutoBackupConfig`</span><span class="sxs-lookup"><span data-stu-id="c070c-126">`New-AzureVMSqlServerAutoBackupConfig` has been renamed to `New-AzureRmVMSqlServerAutoBackupConfig`</span></span>
    + <span data-ttu-id="c070c-127">`New-AzureVMSqlServerAutoPatchingConfig` a été renommé en `New-AzureRmVMSqlServerAutoPatchingConfig`</span><span class="sxs-lookup"><span data-stu-id="c070c-127">`New-AzureVMSqlServerAutoPatchingConfig` has been renamed to `New-AzureRmVMSqlServerAutoPatchingConfig`</span></span>
    + <span data-ttu-id="c070c-128">`New-AzureVMSqlServerKeyVaultCredentialConfig` a été renommé en `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span><span class="sxs-lookup"><span data-stu-id="c070c-128">`New-AzureVMSqlServerKeyVaultCredentialConfig` has been renamed to `New-AzureRmVMSqlServerKeyVaultCredentialConfig`</span></span>
* <span data-ttu-id="c070c-129">Consommation</span><span class="sxs-lookup"><span data-stu-id="c070c-129">Consumption</span></span>
  - <span data-ttu-id="c070c-130">Nouvelle applet de commande Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="c070c-130">New Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>
    + <span data-ttu-id="c070c-131">applet de commande pour récupérer les détails de l’utilisation de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="c070c-131">cmdlet to retrieve usage details of the subscription.</span></span>
* <span data-ttu-id="c070c-132">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c070c-132">ContainerRegistry</span></span>
  - <span data-ttu-id="c070c-133">Ajout d’applets de commande PowerShell pour Azure Container Registry</span><span class="sxs-lookup"><span data-stu-id="c070c-133">Add PowerShell cmdlets for Azure Container Registry</span></span>
    + <span data-ttu-id="c070c-134">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c070c-134">New-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c070c-135">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c070c-135">Get-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c070c-136">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c070c-136">Update-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c070c-137">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c070c-137">Remove-AzureRmContainerRegistry</span></span>
    + <span data-ttu-id="c070c-138">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c070c-138">Get-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="c070c-139">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c070c-139">Update-AzureRmContainerRegistryCredential</span></span>
    + <span data-ttu-id="c070c-140">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c070c-140">Test-AzureRmContainerRegistryNameAvailability</span></span>
* <span data-ttu-id="c070c-141">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c070c-141">DataLakeAnalytics</span></span>
  - <span data-ttu-id="c070c-142">Ajout de la prise en charge des fonctions d’obtention et de récupération d’affichage de liste packages de catalogues</span><span class="sxs-lookup"><span data-stu-id="c070c-142">Add support for catalog package get and list</span></span>
  - <span data-ttu-id="c070c-143">Ajoutez la prise en charge de l’affichage de liste des éléments de catalogue suivants d’ancêtres plus en profondeur :</span><span class="sxs-lookup"><span data-stu-id="c070c-143">Add support for listing the following catalog items from deeper ancestors:</span></span>
    + <span data-ttu-id="c070c-144">Table</span><span class="sxs-lookup"><span data-stu-id="c070c-144">Table</span></span>
    + <span data-ttu-id="c070c-145">TVF</span><span class="sxs-lookup"><span data-stu-id="c070c-145">TVF</span></span>
    + <span data-ttu-id="c070c-146">Affichage</span><span class="sxs-lookup"><span data-stu-id="c070c-146">View</span></span>
    + <span data-ttu-id="c070c-147">Statistiques</span><span class="sxs-lookup"><span data-stu-id="c070c-147">Statistics</span></span>
* <span data-ttu-id="c070c-148">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c070c-148">DataLakeStore</span></span>
  - <span data-ttu-id="c070c-149">Pour `Import-AzureRMDataLakeStoreItem` et `Export-AzureRMDataLakeStoreItem`, la journalisation du suivi a été désactivée par défaut pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="c070c-149">For `Import-AzureRMDataLakeStoreItem` and `Export-AzureRMDataLakeStoreItem` trace logging has been disabled by default to improve performance.</span></span> <span data-ttu-id="c070c-150">Si la journalisation du suivi est souhaitée, veuillez utiliser les paramètres `-DiagnosticLogLevel` et `-DiagnosticLogPath`</span><span class="sxs-lookup"><span data-stu-id="c070c-150">If trace logging is desired please use the `-DiagnosticLogLevel` and `-DiagnosticLogPath` parameters</span></span>
  - <span data-ttu-id="c070c-151">Correction d’un bogue qui provoquait parfois le plantage de PowerShell lors du téléchargement d’un grand nombre de petits fichiers vers ADLS.</span><span class="sxs-lookup"><span data-stu-id="c070c-151">Fixed a bug that would sometimes cause PowerShell to crash when uploading lots of small file to ADLS.</span></span>
* <span data-ttu-id="c070c-152">Event Hub</span><span class="sxs-lookup"><span data-stu-id="c070c-152">EventHub</span></span>
  - <span data-ttu-id="c070c-153">Résolution de bogue :</span><span class="sxs-lookup"><span data-stu-id="c070c-153">Bug fix :</span></span>
    + <span data-ttu-id="c070c-154">Correction de l’erreur de l’applet de commande Set-AzureRmEventHubNamespace « Tier » ne peut pas avoir la valeur Null. Il doit être défini sur « SkuName »</span><span class="sxs-lookup"><span data-stu-id="c070c-154">Fix for Set-AzureRmEventHubNamespace cmdlet error  - 'Tier' cannot be null, where it should be 'SkuName'</span></span>
    + <span data-ttu-id="c070c-155">Set-AzureRmEventHub - Correction de l’erreur « La référence d'objet n'est pas définie à une instance d'un objet » lors de la mise à jour d’EventHub</span><span class="sxs-lookup"><span data-stu-id="c070c-155">Set-AzureRmEventHub - Fix 'Object reference not set to an instance of an object' error while updating EventHub</span></span>
* <span data-ttu-id="c070c-156">Insights</span><span class="sxs-lookup"><span data-stu-id="c070c-156">Insights</span></span>
  - <span data-ttu-id="c070c-157">Add-AzureRm*AlertRule</span><span class="sxs-lookup"><span data-stu-id="c070c-157">Add-AzureRm*AlertRule</span></span>
    + <span data-ttu-id="c070c-158">Renvoie un objet unique : newResource, statusCode, requestId</span><span class="sxs-lookup"><span data-stu-id="c070c-158">Returns a single object: newResource, statusCode, requestId</span></span>
  - <span data-ttu-id="c070c-159">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c070c-159">Get-AzureRmAlertRule</span></span>
    + <span data-ttu-id="c070c-160">La sortie est désormais énumérée au lieu d’être considérée comme un seul objet.</span><span class="sxs-lookup"><span data-stu-id="c070c-160">The output is now enumerated instead of considered a single object.</span></span> <span data-ttu-id="c070c-161">Son type n’a pas changé, il s’agit toujours d’une liste.</span><span class="sxs-lookup"><span data-stu-id="c070c-161">Its type did not change, it is still a list.</span></span>
  - <span data-ttu-id="c070c-162">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c070c-162">Remove-AzureRmAlertRule</span></span>
    + <span data-ttu-id="c070c-163">La valeur de statusCode suit le code d’état renvoyé par la requête (elle renvoyait toujours OK avant).</span><span class="sxs-lookup"><span data-stu-id="c070c-163">The statusCode follows the status code returned by the request, before it was Ok always.</span></span>
  - <span data-ttu-id="c070c-164">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c070c-164">Add-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="c070c-165">Renvoie désormais un statusCode contenant un objet unique (pas une liste comme avant), un requestId et la ressource nouvellement créée ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c070c-165">Returns now a single object (not a list as before) containing statusCode, requestId, and the newly created/updated resource.</span></span>
    + <span data-ttu-id="c070c-166">La valeur de statusCode suit l’état renvoyé par la requête (elle renvoyait toujours OK avant).</span><span class="sxs-lookup"><span data-stu-id="c070c-166">The status code follows the status returned by the request, before it was always Ok.</span></span>
  - <span data-ttu-id="c070c-167">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c070c-167">New-AzureRmAutoscaleRule</span></span>
    + <span data-ttu-id="c070c-168">Le paramètre ScaleActionType a été étendu, il reçoit désormais les valeurs suivantes : ChangeCount, PercentChangeCount, ExactCount.</span><span class="sxs-lookup"><span data-stu-id="c070c-168">The parameter ScaleActionType has been extended, it receives the following values now: ChangeCount, PercentChangeCount, ExactCount.</span></span>
  - <span data-ttu-id="c070c-169">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c070c-169">Remove-AzureRmAutoscaleSetting</span></span>
    + <span data-ttu-id="c070c-170">La valeur de statusCode dans la sortie suit le statusCode renvoyé par la demande.</span><span class="sxs-lookup"><span data-stu-id="c070c-170">The statusCode in the output follows the statusCode returned by the request.</span></span> <span data-ttu-id="c070c-171">Avant, la valeur était toujours OK.</span><span class="sxs-lookup"><span data-stu-id="c070c-171">Before it was always Ok.</span></span>
  - <span data-ttu-id="c070c-172">Get-AzureRMLogProfile</span><span class="sxs-lookup"><span data-stu-id="c070c-172">Get-AzureRMLogProfile</span></span>
    + <span data-ttu-id="c070c-173">La sortie est maintenant énumérée.</span><span class="sxs-lookup"><span data-stu-id="c070c-173">The output is now enumerated.</span></span> <span data-ttu-id="c070c-174">Avant, elle était considérée comme un seul objet.</span><span class="sxs-lookup"><span data-stu-id="c070c-174">Before it was considered a single object.</span></span> <span data-ttu-id="c070c-175">Le type de la sortie reste une liste, comme avant.</span><span class="sxs-lookup"><span data-stu-id="c070c-175">The type of the output remains a list as before.</span></span>
  - <span data-ttu-id="c070c-176">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="c070c-176">Remove-AzureRmLogProfile</span></span>
    + <span data-ttu-id="c070c-177">Le paramètre PassThru a été implémenté.</span><span class="sxs-lookup"><span data-stu-id="c070c-177">The PassThru parameter has been implemented.</span></span>
  - <span data-ttu-id="c070c-178">API de métriques</span><span class="sxs-lookup"><span data-stu-id="c070c-178">Metrics API</span></span>
    + <span data-ttu-id="c070c-179">Le kit de développement logiciel récupère maintenant les métriques depuis MDM.</span><span class="sxs-lookup"><span data-stu-id="c070c-179">The SDK now retrieves metrics from MDM.</span></span>
  - <span data-ttu-id="c070c-180">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="c070c-180">Get-AzureRmMetricDefinition</span></span>
    + <span data-ttu-id="c070c-181">La sortie est toujours une liste, mais la structure de la liste est modifiée.</span><span class="sxs-lookup"><span data-stu-id="c070c-181">The output is still a list, but the structure of the list changed.</span></span>
  - <span data-ttu-id="c070c-182">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="c070c-182">Get-AzureRmMetric</span></span>
    + <span data-ttu-id="c070c-183">L’appel a été modifié.</span><span class="sxs-lookup"><span data-stu-id="c070c-183">The call has changed.</span></span> <span data-ttu-id="c070c-184">Voici la nouvelle syntaxe : Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span><span class="sxs-lookup"><span data-stu-id="c070c-184">This is the new syntax: Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]</span></span>
    + <span data-ttu-id="c070c-185">La sortie est une liste, et la structure de ses éléments a changé.</span><span class="sxs-lookup"><span data-stu-id="c070c-185">The output is a list, and the structure of its elements has changed.</span></span>
* <span data-ttu-id="c070c-186">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c070c-186">KeyVault</span></span>
  - <span data-ttu-id="c070c-187">Ajout de prise en charge de la sauvegarde/restauration des secrets KeyVault</span><span class="sxs-lookup"><span data-stu-id="c070c-187">Adding backup/restore support for KeyVault secrets</span></span>
    + <span data-ttu-id="c070c-188">Les secrets peuvent être sauvegardés et restaurés, comme pour la fonctionnalité actuellement prise en charge pour les clés</span><span class="sxs-lookup"><span data-stu-id="c070c-188">Secrets can be backed up and restored, matching the functionality currently supported for Keys</span></span>

  - <span data-ttu-id="c070c-189">Les applets de commande de sauvegarde pour les clés et secrets acceptent désormais un objet correspondant en tant que paramètre d’entrée</span><span class="sxs-lookup"><span data-stu-id="c070c-189">Backup cmdlets for Keys and Secrets now accept a corresponding object as an input parameter</span></span>
    + <span data-ttu-id="c070c-190">L’appelant peut utiliser les opérations de sauvegarde et de récupération de chaîne : Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c070c-190">The caller may chain retrieval and backup operations: Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey</span></span>

  - <span data-ttu-id="c070c-191">Les applets de commande de sauvegarde prennent désormais en charge une option -Force pour remplacer un fichier existant</span><span class="sxs-lookup"><span data-stu-id="c070c-191">Backup cmdlets now support a -Force switch to overwrite an existing file</span></span>
    + <span data-ttu-id="c070c-192">Notez que la tentative de remplacer un fichier existant ne lèvera plus d’erreur, et que l’utilisateur se verra demander comment poursuivre à la place.</span><span class="sxs-lookup"><span data-stu-id="c070c-192">Note that attempting to overwrite an existing file will no longer throw, and will instead prompt the user for a choice on how to proceed.</span></span>
* <span data-ttu-id="c070c-193">LogicApp</span><span class="sxs-lookup"><span data-stu-id="c070c-193">LogicApp</span></span>
  - <span data-ttu-id="c070c-194">Nouveaux paramètres pour les applets de commande de récupération d’urgence de numéro de contrôle d’échange :</span><span class="sxs-lookup"><span data-stu-id="c070c-194">New parameters for Interchange Control Number disaster recovery cmdlets:</span></span>
    + <span data-ttu-id="c070c-195">Paramètre -AgreementType facultatif (« X12 », ou « Edifact ») pour spécifier les numéros de contrôle pertinents</span><span class="sxs-lookup"><span data-stu-id="c070c-195">Optional -AgreementType parameter ("X12", or "Edifact") to specify the relevant control numbers</span></span>
* <span data-ttu-id="c070c-196">MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c070c-196">MachineLearning</span></span>
  - <span data-ttu-id="c070c-197">Utiliser la nouvelle version du SDK Azure Machine Learning .NET et ajouter une nouvelle applet de commande</span><span class="sxs-lookup"><span data-stu-id="c070c-197">Consume new version of Azure Machine Learning .Net SDK and add a new cmdlet</span></span>
    + <span data-ttu-id="c070c-198">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="c070c-198">Add-AzureRmMlWebServiceRegionalProperty</span></span>
  - <span data-ttu-id="c070c-199">Corrections de texte mineures dans l’aide.</span><span class="sxs-lookup"><span data-stu-id="c070c-199">Minor wording fixes in help text.</span></span>
* <span data-ttu-id="c070c-200">Réseau</span><span class="sxs-lookup"><span data-stu-id="c070c-200">Network</span></span>
  - <span data-ttu-id="c070c-201">Applet de commande Test-AzureRmNetworkWatcherConnectivity ajoutée</span><span class="sxs-lookup"><span data-stu-id="c070c-201">Added Test-AzureRmNetworkWatcherConnectivity cmdlet</span></span>
    + <span data-ttu-id="c070c-202">Renvoie les informations de connexion pour une machine virtuelle source et une destination spécifiées</span><span class="sxs-lookup"><span data-stu-id="c070c-202">Returns connectivity information for a specified source VM and a destination</span></span>
    + <span data-ttu-id="c070c-203">Si la connectivité entre la source et la destination ne peut pas être établie, l’applet de commande renvoie les détails relatifs au problème</span><span class="sxs-lookup"><span data-stu-id="c070c-203">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue</span></span>
* <span data-ttu-id="c070c-204">Profil</span><span class="sxs-lookup"><span data-stu-id="c070c-204">Profile</span></span>
  - <span data-ttu-id="c070c-205">Ajout de l’applet de commande ’Send-Feedback’ : permet à un utilisateur de lancer un ensemble d’invites pour l’envoi de commentaires à l’équipe Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c070c-205">Added \`Send-Feedback' cmdlet: allows a user to initiate a set of prompts which sends feedback to the Azure PowerShell team.</span></span>
  - <span data-ttu-id="c070c-206">Les alias suivants ont été supprimés, car ils étaient en conflit avec des noms d’applet de commande existants dans le module Azure :</span><span class="sxs-lookup"><span data-stu-id="c070c-206">The following aliases have been removed as they conflicted with existing cmdlet names in the Azure module:</span></span>
    + <span data-ttu-id="c070c-207">`Enable-AzureDataCollection` (pris en charge par `Enable-AzureRmDataCollection`)</span><span class="sxs-lookup"><span data-stu-id="c070c-207">`Enable-AzureDataCollection` (supported by `Enable-AzureRmDataCollection`)</span></span>
    + <span data-ttu-id="c070c-208">`Disable-AzureDataCollection` (pris en charge par `Disable-AzureRmDataCollection`)</span><span class="sxs-lookup"><span data-stu-id="c070c-208">`Disable-AzureDataCollection` (supported by `Disable-AzureRmDataCollection`)</span></span>
* <span data-ttu-id="c070c-209">Relais</span><span class="sxs-lookup"><span data-stu-id="c070c-209">Relay</span></span>
  - <span data-ttu-id="c070c-210">Ajout à Azure Relay d’applets de commande qui permettent aux utilisateurs de créer et de gérer toutes les ressources Azure Relay.</span><span class="sxs-lookup"><span data-stu-id="c070c-210">Adds cmdlets for the Azure Relay which allows users to create and manage all Azure Relay resources.</span></span>
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* <span data-ttu-id="c070c-211">Ressources</span><span class="sxs-lookup"><span data-stu-id="c070c-211">Resources</span></span>
  - <span data-ttu-id="c070c-212">Prise en charge des déploiements sur plusieurs groupes de ressources pour New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c070c-212">Support cross-resource-group deployments for New-AzureRmResourceGroupDeployment</span></span>
    + <span data-ttu-id="c070c-213">Les utilisateurs peuvent désormais utiliser des déploiements imbriqués pour déployer sur différents groupes de ressources.</span><span class="sxs-lookup"><span data-stu-id="c070c-213">Users can now use nested deployments to deploy to different resource groups.</span></span>
* <span data-ttu-id="c070c-214">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c070c-214">ServiceBus</span></span>

  - <span data-ttu-id="c070c-215">Correctif de bogue : les valeurs de propriété de file d’attente de ServiceBus étaient définies sur null, l’objet est utilisé en tant que paramètre d’entrée dans l’applet de commande Set-AzureRmServiceBusQueue pour mettre à jour la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c070c-215">Bug Fix: ServiceBus Queue object property values were set to null, the object is used as input parameter in Set-AzureRmServiceBusQueue cmdlet to update Queue.</span></span>
   - <span data-ttu-id="c070c-216">Les propriétés affectées sont LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount et MessageCount</span><span class="sxs-lookup"><span data-stu-id="c070c-216">Properties affected are LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount and MessageCount</span></span>
* <span data-ttu-id="c070c-217">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c070c-217">ServiceFabric</span></span>

  - <span data-ttu-id="c070c-218">Applets de commande ajoutées pour Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c070c-218">Added cmdlets for service fabric</span></span>
    + <span data-ttu-id="c070c-219">Add-AzureRmServiceFabricApplicationCertificate       Ajout d’un certificat qui sera utilisé comme certificat d’application</span><span class="sxs-lookup"><span data-stu-id="c070c-219">Add-AzureRmServiceFabricApplicationCertificate       Add a certificate which will be used as application certificate</span></span>
    + <span data-ttu-id="c070c-220">Add-AzureRmServiceFabricClientCertificate       Ajout d’un nom ou d’une empreinte en commun pour les paramètres de cluster pour l’authentification client</span><span class="sxs-lookup"><span data-stu-id="c070c-220">Add-AzureRmServiceFabricClientCertificate       Add a common name or thumbprint to the cluster settings for client authentication</span></span>
    + <span data-ttu-id="c070c-221">Add-AzureRmServiceFabricClusterCertificate       Ajout d’un certificat de cluster secondaire au cluster pour régénérer le certificat existant</span><span class="sxs-lookup"><span data-stu-id="c070c-221">Add-AzureRmServiceFabricClusterCertificate       Add a secondary cluster certificate to the cluster for rolling over the existing certificate</span></span>
    + <span data-ttu-id="c070c-222">Add-AzureRmServiceFabricNodes       Ajout de nœuds/machines virtuelles d’un type de nœud spécifique à un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-222">Add-AzureRmServiceFabricNodes       Add nodes/VMs of a specific node type to a cluster</span></span>
    + <span data-ttu-id="c070c-223">Add-AzureRmServiceFabricNodeType       Ajout d’un type de nœud/de machines virtuelles à un cluster existant</span><span class="sxs-lookup"><span data-stu-id="c070c-223">Add-AzureRmServiceFabricNodeType       Add a node type/VMs to an existing cluster</span></span>
    + <span data-ttu-id="c070c-224">Get-AzureRmServiceFabricCluster       Récupération des détails de la ressource de cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-224">Get-AzureRmServiceFabricCluster       Get the details of the cluster resource</span></span>
    + <span data-ttu-id="c070c-225">New-AzureRmServiceFabricCluster Création d’un nouveau cluster ServiceFabric.</span><span class="sxs-lookup"><span data-stu-id="c070c-225">New-AzureRmServiceFabricCluster Create a new ServiceFabric cluster.</span></span> <span data-ttu-id="c070c-226">Cette commande a de nombreuses surcharges pour couvrir différents scénarios</span><span class="sxs-lookup"><span data-stu-id="c070c-226">This command has many overloads to cover various scenarios</span></span>
    + <span data-ttu-id="c070c-227">Remove-AzureRmServiceFabricClientCertificate       Empêche un certificat client d’être utilisé pour accéder à un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-227">Remove-AzureRmServiceFabricClientCertificate       Remove a client certificate from being used to access a cluster</span></span>
    + <span data-ttu-id="c070c-228">Remove-AzureRmServiceFabricClusterCertificate       Empêche un certificat de cluster d’être utilisé pour la sécurité du cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-228">Remove-AzureRmServiceFabricClusterCertificate       Remove a cluster certificate from being used for cluster security</span></span>
    + <span data-ttu-id="c070c-229">Remove-AzureRmServiceFabricNodes       Suppression de nœuds appartenant à un type spécifique d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-229">Remove-AzureRmServiceFabricNodes       Remove nodes from a specific node type from a cluster</span></span>
    + <span data-ttu-id="c070c-230">Remove-AzureRmServiceFabricNodeType       Suppression d’un type de nœud d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-230">Remove-AzureRmServiceFabricNodeType       Remove a node type from a cluster</span></span>
    + <span data-ttu-id="c070c-231">Remove-AzureRmServiceFabricSettings       Suppression d’un ou plusieurs paramètres ServiceFabric d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-231">Remove-AzureRmServiceFabricSettings       Remove one or more ServiceFabric settings from a cluster</span></span>
    + <span data-ttu-id="c070c-232">Set-AzureRmServiceFabricSettings       Ajout ou mise à jour d’un ou plusieurs paramètres ServiceFabric d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-232">Set-AzureRmServiceFabricSettings       Add or update one or more ServiceFabric settings of a cluster</span></span>
    + <span data-ttu-id="c070c-233">Set-AzureRmServiceFabricUpgradeType       Modification du type de mise à niveau de ServiceFabric d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-233">Set-AzureRmServiceFabricUpgradeType       Change the ServiceFabric upgrade type of a cluster</span></span>
    + <span data-ttu-id="c070c-234">Update-AzureRmServiceFabricDurability       Modification du niveau de durabilité d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-234">Update-AzureRmServiceFabricDurability       Change the durability tier of a cluster</span></span>
    + <span data-ttu-id="c070c-235">Update-AzureRmServiceFabricReliability       Modification du niveau de fiabilité d’un cluster</span><span class="sxs-lookup"><span data-stu-id="c070c-235">Update-AzureRmServiceFabricReliability       Change the reliability tier of a cluster</span></span>
* <span data-ttu-id="c070c-236">SQL</span><span class="sxs-lookup"><span data-stu-id="c070c-236">Sql</span></span>
  - <span data-ttu-id="c070c-237">Ajout du paramètre -SampleName à New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c070c-237">Added -SampleName parameter to New-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="c070c-238">Mises à jour des applets de commande de groupe de basculement</span><span class="sxs-lookup"><span data-stu-id="c070c-238">Updates to Failover Group cmdlets</span></span>
  - <span data-ttu-id="c070c-239">Suppression des paramètres ’Tag’</span><span class="sxs-lookup"><span data-stu-id="c070c-239">Remove 'Tag' parameters</span></span>
  - <span data-ttu-id="c070c-240">Suppression des paramètres 'PartnerResourceGroupName' et 'PartnerServerName' de l’applet de commande Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c070c-240">Remove 'PartnerResourceGroupName' and 'PartnerServerName' parameters from Remove-AzureRmSqlDatabaseFailoverGroup cmdlet</span></span>
  - <span data-ttu-id="c070c-241">Ajout d’un paramètre 'GracePeriodWithDataLossHours' aux applets de commande New- et Set-, qui finiront par remplacer « GracePeriodWithDataLossHour »</span><span class="sxs-lookup"><span data-stu-id="c070c-241">Add 'GracePeriodWithDataLossHours' parameter to New- and Set- cmdlets, which shall eventually replace 'GracePeriodWithDataLossHour'</span></span>
  - <span data-ttu-id="c070c-242">La documentation a été étoffée et mise à jour</span><span class="sxs-lookup"><span data-stu-id="c070c-242">Documentation has been fleshed out and updated</span></span>
  - <span data-ttu-id="c070c-243">Modification du format des objets retournés et correction des bogues à cause desquels les champs n’étaient pas toujours remplis</span><span class="sxs-lookup"><span data-stu-id="c070c-243">Change formatting of returned objects and fix some bugs where fields were not always populated</span></span>
  - <span data-ttu-id="c070c-244">Ajout des propriétés 'DatabaseNames' et 'PartnerLocation' à l’objet groupe de basculement</span><span class="sxs-lookup"><span data-stu-id="c070c-244">Add 'DatabaseNames' and 'PartnerLocation' properties to Failover Group object</span></span>
  - <span data-ttu-id="c070c-245">Correction du bogue qui faisait que l’applet de commande Switch- se terminait immédiatement au lieu d’attendre la fin de l’opération</span><span class="sxs-lookup"><span data-stu-id="c070c-245">Fix bug causing Switch- cmdlet to return immediately rather than waiting for operation to complete</span></span>
  - <span data-ttu-id="c070c-246">Correction du bogue de dépassement de capacité d’entier lorsque des valeurs de délai élevées étaient utilisées</span><span class="sxs-lookup"><span data-stu-id="c070c-246">Fix integer overflow bug when high grace period values are used</span></span>
  - <span data-ttu-id="c070c-247">Ajustement de la période de grâce à un minimum de 1 heure si une priorité plus faible est fournie</span><span class="sxs-lookup"><span data-stu-id="c070c-247">Adjust grace period to a minimum of 1 hour if a lower one is provided</span></span>
  - <span data-ttu-id="c070c-248">Suppression de « Usage_Anomaly » des valeurs acceptées pour le paramètre « ExcludedDetectionType » des applets de commande Set-AzureRmSqlDatabaseThreatDetectionPolicy et Set-AzureRmSqlServerThreatDetectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c070c-248">Remove "Usage_Anomaly" from the accepted values for "ExcludedDetectionType" parameter of Set-AzureRmSqlDatabaseThreatDetectionPolicy cmdlet and Set-AzureRmSqlServerThreatDetectionPolicy cmdlet.</span></span>
* <span data-ttu-id="c070c-249">Storage</span><span class="sxs-lookup"><span data-stu-id="c070c-249">Storage</span></span>
  - <span data-ttu-id="c070c-250">Mise à niveau du SDK SRP vers la version 6.3.0</span><span class="sxs-lookup"><span data-stu-id="c070c-250">Upgrade SRP SDK to 6.3.0</span></span>
  - <span data-ttu-id="c070c-251">New/Set-AzureRmStorageAccount : ajout d’un paramètre pour prendre en charge EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c070c-251">New/Set-AzureRmStorageAccount:Add a new parameter to support EnableHttpsTrafficOnly</span></span>
  - <span data-ttu-id="c070c-252">New/Set/Get-AzureRmStorageAccount : le compte de stockage renvoyé contient un nouvel attribut, EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="c070c-252">New/Set/Get-AzureRmStorageAccount: Returned Storage Account contains a new attribute EnableHttpsTrafficOnly</span></span>
* <span data-ttu-id="c070c-253">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c070c-253">Azure.Storage</span></span>
  - <span data-ttu-id="c070c-254">Mise à niveau vers Azure Storage Client Library 8.1.1 et Azure Storage DataMovement Library 0.5.1</span><span class="sxs-lookup"><span data-stu-id="c070c-254">Upgrade to Azure Storage Client Library 8.1.1 and Azure Storage DataMovement Library 0.5.1</span></span>
  - <span data-ttu-id="c070c-255">Ajout d’une nouvelle applet de commande pour prendre en charge la fonctionnalité de copie incrémentielle d’objet blob</span><span class="sxs-lookup"><span data-stu-id="c070c-255">Add a new cmdlet to support blob Incremental Copy feature</span></span>