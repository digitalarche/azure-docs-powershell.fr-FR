---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: "Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="6ed15-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="6ed15-103">Release notes</span></span>

<span data-ttu-id="6ed15-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="6ed15-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="6ed15-105">Version 1.7.0</span><span class="sxs-lookup"><span data-stu-id="6ed15-105">Version 1.7.0</span></span>

* <span data-ttu-id="6ed15-106">**Modification du comportement des paramètres -Force, –Confirm et $ConfirmPreference pour toutes les applets de commande. Nous modifions cette implémentation conformément aux directives PowerShell. Pour la plupart des applets de commande, cela implique de supprimer le paramètre Force et d’ignorer l’invite ShouldProcess, les utilisateurs doivent inclure le paramètre : « -Confirm:$false » dans leurs scripts PowerShell.**</span><span class="sxs-lookup"><span data-stu-id="6ed15-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="6ed15-107">Ces changements corrigent les problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="6ed15-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="6ed15-108">Implémentation correcte de la fonctionnalité –WhatIf, qui permet à un utilisateur de déterminer les effets d’une applet de commande ou d’un script sans apporter de modification réelle</span><span class="sxs-lookup"><span data-stu-id="6ed15-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="6ed15-109">Contrôle des invites à l’aide du paramètre $ConfirmPreference à l’échelle de la session. De cette façon, l’utilisateur est invité à confirmer l’action en fonction de l’impact d’une modification potentielle (comme indiqué dans le paramètre ConfirmImpact de l’applet de commande)</span><span class="sxs-lookup"><span data-stu-id="6ed15-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="6ed15-110">Contrôle des invites de confirmation propres à une applet de commande à l’aide du paramètre –Confirm</span><span class="sxs-lookup"><span data-stu-id="6ed15-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="6ed15-111">Utilisation cohérente de ShouldContinue et du paramètre –Force dans les applets de commande, uniquement pour les actions nécessitant la confirmation de l’utilisateur en raison de la nature particulière des modifications (par exemple, la suppression de fichiers cachés)</span><span class="sxs-lookup"><span data-stu-id="6ed15-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="6ed15-112">Cohérence avec les autres applets de commande PowerShell, pour que la connaissance des scripts PowerShell soit immédiatement applicable aux applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6ed15-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="6ed15-113">**Notez que dorénavant pour *ignorer automatiquement toutes les invites dans toutes les circonstances*, les applets de commande Azure PowerShell nécessitent que l’utilisateur fournisse deux paramètres :**</span><span class="sxs-lookup"><span data-stu-id="6ed15-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="6ed15-114">Calcul Azure</span><span class="sxs-lookup"><span data-stu-id="6ed15-114">Azure Compute</span></span>
  - <span data-ttu-id="6ed15-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6ed15-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="6ed15-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6ed15-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="6ed15-117">Paramètre -Redeploy pour Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6ed15-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="6ed15-118">Paramètre -Validate pour Move-AzureService, Move-AzureStorageAccount et Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ed15-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="6ed15-119">Les paramètres de nom et de version pour les applets de commande d’extension sont facultatifs comme auparavant.</span><span class="sxs-lookup"><span data-stu-id="6ed15-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="6ed15-120">New-AzureVM peut obtenir le type de licence d’un objet de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="6ed15-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="6ed15-121">Azure Storage</span><span class="sxs-lookup"><span data-stu-id="6ed15-121">Azure Storage</span></span>
  - <span data-ttu-id="6ed15-122">Changement du paramètre Tags en Tag et ajout de l’alias de paramètre Tags</span><span class="sxs-lookup"><span data-stu-id="6ed15-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="6ed15-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ed15-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="6ed15-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6ed15-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6ed15-125">Réseau Azure</span><span class="sxs-lookup"><span data-stu-id="6ed15-125">Azure Network</span></span>
  - <span data-ttu-id="6ed15-126">Ajout d’une nouvelle applet de commande pour l’appairage de réseaux virtuels</span><span class="sxs-lookup"><span data-stu-id="6ed15-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="6ed15-127">Cache Redis Azure</span><span class="sxs-lookup"><span data-stu-id="6ed15-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="6ed15-128">Ajout d’une nouvelle applet de commande pour Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ed15-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="6ed15-129">Ajout d’une nouvelle applet de commande pour Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ed15-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="6ed15-130">Ajout d’une nouvelle applet de commande pour Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ed15-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="6ed15-131">Modification de l’applet de commande New-AzureRmRedisCache pour inclure le changement de paramètre de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="6ed15-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="6ed15-132">Sauvegarde/restauration d’Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="6ed15-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="6ed15-133">Applets de commande pour la fonctionnalité de sauvegarde avec rétention à long terme</span><span class="sxs-lookup"><span data-stu-id="6ed15-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="6ed15-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="6ed15-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="6ed15-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed15-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="6ed15-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="6ed15-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="6ed15-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6ed15-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="6ed15-138">Restore-AzureRmSqlDatabase prend désormais en charge la limite de restauration dans le temps d’une base de données supprimée</span><span class="sxs-lookup"><span data-stu-id="6ed15-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="6ed15-139">Restore-AzureRmSqlDatabase prend désormais en charge la restauration à partir d’une sauvegarde avec rétention à long terme</span><span class="sxs-lookup"><span data-stu-id="6ed15-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="6ed15-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="6ed15-140">Azure LogicApp</span></span>
  - <span data-ttu-id="6ed15-141">Ajout des applets de commande des comptes d’intégration LogicApp.</span><span class="sxs-lookup"><span data-stu-id="6ed15-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="6ed15-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6ed15-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="6ed15-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="6ed15-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="6ed15-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ed15-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="6ed15-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6ed15-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="6ed15-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6ed15-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="6ed15-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6ed15-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="6ed15-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6ed15-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="6ed15-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6ed15-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="6ed15-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ed15-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="6ed15-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6ed15-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="6ed15-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6ed15-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="6ed15-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6ed15-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="6ed15-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6ed15-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="6ed15-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6ed15-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="6ed15-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ed15-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="6ed15-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6ed15-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="6ed15-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6ed15-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="6ed15-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6ed15-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="6ed15-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6ed15-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="6ed15-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="6ed15-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="6ed15-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6ed15-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="6ed15-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="6ed15-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="6ed15-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6ed15-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="6ed15-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6ed15-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="6ed15-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6ed15-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="6ed15-167">Azure Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6ed15-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="6ed15-168">Amélioration drastique des performances de téléchargement et de chargement de fichiers et de dossiers.</span><span class="sxs-lookup"><span data-stu-id="6ed15-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="6ed15-169">Cela inclut une légère modification des noms de paramètre pour le téléchargement ainsi que l’inclusion de deux nouveaux paramètres pour le chargement :</span><span class="sxs-lookup"><span data-stu-id="6ed15-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="6ed15-170">NumThreads -> PerFileThreadCount, utilisé pour indiquer le nombre de threads à utiliser dans un seul fichier</span><span class="sxs-lookup"><span data-stu-id="6ed15-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="6ed15-171">ConcurrentFileCount, utilisé pour indiquer le nombre de fichiers à charger/télécharger en parallèle pour le chargement/téléchargement de dossiers.</span><span class="sxs-lookup"><span data-stu-id="6ed15-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="6ed15-172">Les valeurs de thread par défaut sont maintenant conçues afin d’apporter un meilleur débit général pour la plupart des tailles de fichier.</span><span class="sxs-lookup"><span data-stu-id="6ed15-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="6ed15-173">Si les performances ne correspondent pas à ce que vous attendez, les valeurs ci-dessus peuvent être modifiées pour répondre aux exigences.</span><span class="sxs-lookup"><span data-stu-id="6ed15-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="6ed15-174">Service Analytique Azure Data Lake</span><span class="sxs-lookup"><span data-stu-id="6ed15-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="6ed15-175">L’applet de commande Get-AzureRMDataLakeAnalyticsDataSource retourne à présent toutes les sources de données quand elle est appelée sans argument.</span><span class="sxs-lookup"><span data-stu-id="6ed15-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="6ed15-176">Cette modification supprime également le paramètre de type de source de données de l’applet de commande.</span><span class="sxs-lookup"><span data-stu-id="6ed15-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="6ed15-177">Elle entraîne le retour d’un nouvel objet pour l’opération de liste avec les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ed15-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="6ed15-178">Type (type de source de données)</span><span class="sxs-lookup"><span data-stu-id="6ed15-178">Type, the type of data source</span></span>
    + <span data-ttu-id="6ed15-179">Nom (nom de la source de données)</span><span class="sxs-lookup"><span data-stu-id="6ed15-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="6ed15-180">IsDefault, défini sur true s’il s’agit de la source de données par défaut pour le compte</span><span class="sxs-lookup"><span data-stu-id="6ed15-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="6ed15-181">Correction de Get-AzureRMDataLakeAnalyticsJob pour la liste de certaines valeurs de décalage de date et d’heure pendant le filtrage sur submittedBefore et submittedAfter.</span><span class="sxs-lookup"><span data-stu-id="6ed15-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="6ed15-182">Web Apps</span><span class="sxs-lookup"><span data-stu-id="6ed15-182">Web Apps</span></span>
  - <span data-ttu-id="6ed15-183">Ajout de l’applet de commande Swap-AzureRmWebAppSlot pour l’échange normal et l’échange avec aperçu</span><span class="sxs-lookup"><span data-stu-id="6ed15-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="6ed15-184">Extension de l’applet de commande Set-AzureRmWebAppSlot pour prendre en charge l’échange automatique</span><span class="sxs-lookup"><span data-stu-id="6ed15-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="6ed15-185">Gestion des API Azure</span><span class="sxs-lookup"><span data-stu-id="6ed15-185">Azure API Management</span></span>
  - <span data-ttu-id="6ed15-186">Correction des applets de commande de déploiement de gestion des API Azure pour AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="6ed15-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="6ed15-187">Suppression de l’applet de commande Set-AzureRmApiManagementTenantGitAccess, car l’accès Git est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="6ed15-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="6ed15-188">Sauvegarde Azure Recovery Services</span><span class="sxs-lookup"><span data-stu-id="6ed15-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="6ed15-189">Ajout de la prise en charge de la charge de travail Azure SQL</span><span class="sxs-lookup"><span data-stu-id="6ed15-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="6ed15-190">Ajout de la prise en charge de la sauvegarde et de la restauration de machines virtuelles Azure chiffrées</span><span class="sxs-lookup"><span data-stu-id="6ed15-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="6ed15-191">Backup-AzureRmRecoveryServicesBackupItem - Ajout de la fonctionnalité facultative de durée de rétention pour les points de récupération</span><span class="sxs-lookup"><span data-stu-id="6ed15-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="6ed15-192">Résolution de bogues mineurs liés aux filtres dans les applets de commande Get-AzureRmRecoveryServicesBackupContainer et Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ed15-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="6ed15-193">Azure Automation</span><span class="sxs-lookup"><span data-stu-id="6ed15-193">Azure Automation</span></span>
  - <span data-ttu-id="6ed15-194">Ajout de Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="6ed15-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
