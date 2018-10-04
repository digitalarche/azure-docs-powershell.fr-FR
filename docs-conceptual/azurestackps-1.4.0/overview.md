---
title: Vue d’ensemble d’Azure Stack PowerShell administrateur | Microsoft Docs
description: Une vue d’ensemble d’Azure Stack PowerShell administrateur avec des instructions sur les procédures d’installation et de configuration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47424851"
---
# <a name="azure-stack-module-140"></a><span data-ttu-id="7de78-103">Module Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="7de78-103">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="7de78-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="7de78-104">Requirements:</span></span>
<span data-ttu-id="7de78-105">La version minimale d’Azure Stack prise en charge est la version 1804.</span><span class="sxs-lookup"><span data-stu-id="7de78-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="7de78-106">Remarque : si vous utilisez une version antérieure, installez la version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="7de78-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="7de78-107">Problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="7de78-107">Known issues:</span></span>

- <span data-ttu-id="7de78-108">L’option Fermer l’alerte nécessite la version 1803 d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7de78-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="7de78-109">La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public.</span><span class="sxs-lookup"><span data-stu-id="7de78-109">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="7de78-110">La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.</span><span class="sxs-lookup"><span data-stu-id="7de78-110">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="7de78-111">Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.</span><span class="sxs-lookup"><span data-stu-id="7de78-111">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="7de78-112">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="7de78-112">Breaking Changes</span></span>
<span data-ttu-id="7de78-113">Il n’existe pas de changement cassant par rapport à la version 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="7de78-113">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="7de78-114">Tous les changements cassants liés à la migration à partir de la version 1.2.11 sont décrits ici : https://aka.ms/azspowershellmigration.</span><span class="sxs-lookup"><span data-stu-id="7de78-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="7de78-115">Installer</span><span class="sxs-lookup"><span data-stu-id="7de78-115">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="7de78-116">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="7de78-116">Release Notes</span></span>
    * <span data-ttu-id="7de78-117">La version 1.4.0 de Azurestack ne présente aucun changement cassant par rapport à la version 1.3.0 précédente</span><span class="sxs-lookup"><span data-stu-id="7de78-117">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="7de78-118">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-118">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="7de78-119">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-119">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-120">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-120">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="7de78-121">Ajout de nouveaux paramètres BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays dans la cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="7de78-121">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="7de78-122">Ajout d’une cmdlet New-EncyptionKeyBase64 pour faciliter la création de clé de chiffrement</span><span class="sxs-lookup"><span data-stu-id="7de78-122">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="7de78-123">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-124">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-124">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="7de78-125">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-125">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-126">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-126">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="7de78-127">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-127">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="7de78-128">Ajout d’une cmdlet Add-AzsScaleUnitNode pour permettre à l’administrateur d’ajouter de nouveaux nœuds d’unité d’échelle au tampon azurestack</span><span class="sxs-lookup"><span data-stu-id="7de78-128">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="7de78-129">Ajout de cmdlet et de New-AzsScaleUnitNodeObject pour faciliter les objets de paramètre de création d’unité d'échelle</span><span class="sxs-lookup"><span data-stu-id="7de78-129">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="7de78-130">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-130">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="7de78-131">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-132">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-132">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="7de78-133">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-134">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-134">Azs.Network.Admin</span></span>
        - <span data-ttu-id="7de78-135">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-136">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-136">Azs.Update.Admin</span></span>
        - <span data-ttu-id="7de78-137">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-138">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="7de78-138">Azs.Subscriptions</span></span>
        - <span data-ttu-id="7de78-139">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-139">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="7de78-140">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="7de78-140">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="7de78-141">Ajout d’une cmdlet Move-AzsSubscription pour déplacer des abonnements entre les offres de fournisseur délégué</span><span class="sxs-lookup"><span data-stu-id="7de78-141">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="7de78-142">Ajout d’une cmdlet Test-AzsMoveSubscription pour valider que les abonnements d’utilisateur peuvent être déplacés entre les offres de fournisseur délégué</span><span class="sxs-lookup"><span data-stu-id="7de78-142">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="7de78-143">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="7de78-143">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="7de78-144">Contenu :</span><span class="sxs-lookup"><span data-stu-id="7de78-144">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="7de78-145">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="7de78-145">Azure Bridge</span></span>
<span data-ttu-id="7de78-146">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="7de78-146">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="7de78-147">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="7de78-147">Backup</span></span>
<span data-ttu-id="7de78-148">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="7de78-148">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="7de78-149">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="7de78-149">Configure where backups are stored</span></span>
- <span data-ttu-id="7de78-150">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="7de78-150">Perform backups</span></span>
- <span data-ttu-id="7de78-151">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="7de78-151">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="7de78-152">Commerce</span><span class="sxs-lookup"><span data-stu-id="7de78-152">Commerce</span></span>
<span data-ttu-id="7de78-153">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7de78-153">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="7de78-154">Calcul</span><span class="sxs-lookup"><span data-stu-id="7de78-154">Compute</span></span>
<span data-ttu-id="7de78-155">Préversion du module administrateur Calcul d’Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="7de78-155">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="7de78-156">Structure</span><span class="sxs-lookup"><span data-stu-id="7de78-156">Fabric</span></span>
<span data-ttu-id="7de78-157">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="7de78-157">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="7de78-158">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="7de78-158">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="7de78-159">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="7de78-159">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="7de78-160">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="7de78-160">Repair of scale unit nodes</span></span>
- <span data-ttu-id="7de78-161">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="7de78-161">Restart of Infrastructure role</span></span>
- <span data-ttu-id="7de78-162">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="7de78-162">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="7de78-163">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="7de78-163">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="7de78-164">Galerie</span><span class="sxs-lookup"><span data-stu-id="7de78-164">Gallery</span></span>
<span data-ttu-id="7de78-165">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7de78-165">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="7de78-166">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="7de78-166">Infrastructure Insights</span></span>
<span data-ttu-id="7de78-167">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="7de78-167">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="7de78-168">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="7de78-168">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="7de78-169">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="7de78-169">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="7de78-170">KeyVault</span><span class="sxs-lookup"><span data-stu-id="7de78-170">KeyVault</span></span>
<span data-ttu-id="7de78-171">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="7de78-171">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="7de78-172">Réseau</span><span class="sxs-lookup"><span data-stu-id="7de78-172">Network</span></span>
<span data-ttu-id="7de78-173">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="7de78-173">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="7de78-174">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="7de78-174">Management of network quotas</span></span>
- <span data-ttu-id="7de78-175">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="7de78-175">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="7de78-176">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="7de78-176">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="7de78-177">Stockage</span><span class="sxs-lookup"><span data-stu-id="7de78-177">Storage</span></span>
<span data-ttu-id="7de78-178">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="7de78-178">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="7de78-179">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="7de78-179">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="7de78-180">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="7de78-180">Manage storage quotas</span></span>
- <span data-ttu-id="7de78-181">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="7de78-181">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="7de78-182">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="7de78-182">Restore deleted storage accounts</span></span>
- <span data-ttu-id="7de78-183">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="7de78-183">Migrate containers from one share to another</span></span>
- <span data-ttu-id="7de78-184">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="7de78-184">View information about the individual storage components</span></span>
- <span data-ttu-id="7de78-185">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="7de78-185">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="7de78-186">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="7de78-186">Subscription Admin</span></span>
<span data-ttu-id="7de78-187">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7de78-187">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="7de78-188">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="7de78-188">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="7de78-189">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="7de78-189">Manage plans and offers</span></span>
- <span data-ttu-id="7de78-190">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="7de78-190">View usage and performance information</span></span>
- <span data-ttu-id="7de78-191">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="7de78-191">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="7de78-192">Abonnement</span><span class="sxs-lookup"><span data-stu-id="7de78-192">Subscription</span></span>
<span data-ttu-id="7de78-193">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7de78-193">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="7de78-194">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="7de78-194">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="7de78-195">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="7de78-195">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="7de78-196">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="7de78-196">Update</span></span>
<span data-ttu-id="7de78-197">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="7de78-197">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="7de78-198">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="7de78-198">In this module administrators can:</span></span>
- <span data-ttu-id="7de78-199">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="7de78-199">List and install available updates</span></span>
- <span data-ttu-id="7de78-200">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="7de78-200">Resume interrupted updates</span></span>
- <span data-ttu-id="7de78-201">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="7de78-201">View installed updates</span></span>
