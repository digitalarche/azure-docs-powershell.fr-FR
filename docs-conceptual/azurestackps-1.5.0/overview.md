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
ms.openlocfilehash: 18861f0e5232e0b505767aa9609099afe88f9477
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399431"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="a776e-103">Module Azure Stack 1.5.0</span><span class="sxs-lookup"><span data-stu-id="a776e-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="a776e-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="a776e-104">Requirements:</span></span>
<span data-ttu-id="a776e-105">La version minimale d’Azure Stack prise en charge est la version 1808.</span><span class="sxs-lookup"><span data-stu-id="a776e-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="a776e-106">Remarque : si vous utilisez une version antérieure, installez la version 1.4.0</span><span class="sxs-lookup"><span data-stu-id="a776e-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="a776e-107">Problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="a776e-107">Known issues:</span></span>

- <span data-ttu-id="a776e-108">La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public.</span><span class="sxs-lookup"><span data-stu-id="a776e-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="a776e-109">La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.</span><span class="sxs-lookup"><span data-stu-id="a776e-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="a776e-110">Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.</span><span class="sxs-lookup"><span data-stu-id="a776e-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="a776e-111">Installer</span><span class="sxs-lookup"><span data-stu-id="a776e-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

##<a name="release-notes"></a><span data-ttu-id="a776e-112">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="a776e-112">Release Notes</span></span>
* <span data-ttu-id="a776e-113">Tous les modules Azure Stack administrateurs sont mis à jour pour une dépendance supérieure ou égale sur le module AzureRm.Profile</span><span class="sxs-lookup"><span data-stu-id="a776e-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="a776e-114">Prise en charge de la gestion des noms de ressource imbriquée dans tous les modules</span><span class="sxs-lookup"><span data-stu-id="a776e-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="a776e-115">Correction de bogue dans tous les modules où l’état de ErrorActionPreference est remplacé par Arrêter</span><span class="sxs-lookup"><span data-stu-id="a776e-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="a776e-116">Module Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="a776e-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="a776e-117">De nouvelles propriétés de quota ont été ajoutées pour la prise en charge des disques managés</span><span class="sxs-lookup"><span data-stu-id="a776e-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="a776e-118">Ajout de cmdlets associées à la migration de disque</span><span class="sxs-lookup"><span data-stu-id="a776e-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="a776e-119">Propriétés supplémentaires dans les images de plateforme et les objets d’extension de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="a776e-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="a776e-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="a776e-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="a776e-121">Nouvelle cmdlet pour l’ajout de nœud d’unité d’échelle</span><span class="sxs-lookup"><span data-stu-id="a776e-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="a776e-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="a776e-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="a776e-123">Set-AzsBackupShare est à présent un alias pour la cmdlet Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a776e-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="a776e-124">Get-AzsBackupShare est à présent un alias pour la cmdlet Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a776e-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="a776e-125">Set-AzsBackupConfiguration, le paramètre BackupShare est à présent un alias pour le chemin d’accès de paramètre</span><span class="sxs-lookup"><span data-stu-id="a776e-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="a776e-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="a776e-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="a776e-127">Get-AzsDelegatedProviderOffer, le paramètre OfferName est à présent un alias pour Offer</span><span class="sxs-lookup"><span data-stu-id="a776e-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="a776e-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="a776e-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="a776e-129">Get-AzsDelegatedProviderOffer, le paramètre OfferName est à présent un alias pour Offer</span><span class="sxs-lookup"><span data-stu-id="a776e-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="a776e-130">Contenu :</span><span class="sxs-lookup"><span data-stu-id="a776e-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="a776e-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="a776e-131">Azure Bridge</span></span>
<span data-ttu-id="a776e-132">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="a776e-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="a776e-133">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="a776e-133">Backup</span></span>
<span data-ttu-id="a776e-134">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="a776e-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="a776e-135">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="a776e-135">Configure where backups are stored</span></span>
- <span data-ttu-id="a776e-136">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="a776e-136">Perform backups</span></span>
- <span data-ttu-id="a776e-137">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="a776e-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="a776e-138">Commerce</span><span class="sxs-lookup"><span data-stu-id="a776e-138">Commerce</span></span>
<span data-ttu-id="a776e-139">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="a776e-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="a776e-140">Calcul</span><span class="sxs-lookup"><span data-stu-id="a776e-140">Compute</span></span>
<span data-ttu-id="a776e-141">Préversion du module administrateur de calcul Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme, les disques managés et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="a776e-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="a776e-142">Structure</span><span class="sxs-lookup"><span data-stu-id="a776e-142">Fabric</span></span>
<span data-ttu-id="a776e-143">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="a776e-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="a776e-144">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="a776e-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="a776e-145">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="a776e-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="a776e-146">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="a776e-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="a776e-147">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="a776e-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="a776e-148">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="a776e-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="a776e-149">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="a776e-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="a776e-150">Galerie</span><span class="sxs-lookup"><span data-stu-id="a776e-150">Gallery</span></span>
<span data-ttu-id="a776e-151">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="a776e-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="a776e-152">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="a776e-152">Infrastructure Insights</span></span>
<span data-ttu-id="a776e-153">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="a776e-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="a776e-154">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="a776e-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="a776e-155">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="a776e-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="a776e-156">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a776e-156">KeyVault</span></span>
<span data-ttu-id="a776e-157">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="a776e-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="a776e-158">Réseau</span><span class="sxs-lookup"><span data-stu-id="a776e-158">Network</span></span>
<span data-ttu-id="a776e-159">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="a776e-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="a776e-160">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="a776e-160">Management of network quotas</span></span>
- <span data-ttu-id="a776e-161">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="a776e-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="a776e-162">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="a776e-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="a776e-163">Stockage</span><span class="sxs-lookup"><span data-stu-id="a776e-163">Storage</span></span>
<span data-ttu-id="a776e-164">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="a776e-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="a776e-165">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="a776e-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="a776e-166">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="a776e-166">Manage storage quotas</span></span>
- <span data-ttu-id="a776e-167">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="a776e-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="a776e-168">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="a776e-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="a776e-169">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="a776e-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="a776e-170">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="a776e-170">View information about the individual storage components</span></span>
- <span data-ttu-id="a776e-171">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="a776e-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="a776e-172">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="a776e-172">Subscription Admin</span></span>
<span data-ttu-id="a776e-173">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="a776e-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="a776e-174">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="a776e-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="a776e-175">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="a776e-175">Manage plans and offers</span></span>
- <span data-ttu-id="a776e-176">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="a776e-176">View usage and performance information</span></span>
- <span data-ttu-id="a776e-177">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="a776e-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="a776e-178">Abonnement</span><span class="sxs-lookup"><span data-stu-id="a776e-178">Subscription</span></span>
<span data-ttu-id="a776e-179">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="a776e-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="a776e-180">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="a776e-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="a776e-181">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="a776e-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="a776e-182">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="a776e-182">Update</span></span>
<span data-ttu-id="a776e-183">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="a776e-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="a776e-184">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="a776e-184">In this module administrators can:</span></span>
- <span data-ttu-id="a776e-185">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="a776e-185">List and install available updates</span></span>
- <span data-ttu-id="a776e-186">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="a776e-186">Resume interrupted updates</span></span>
- <span data-ttu-id="a776e-187">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="a776e-187">View installed updates</span></span>
