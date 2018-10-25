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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001046"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="c4462-103">Module Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="c4462-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="c4462-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="c4462-104">Requirements:</span></span>
<span data-ttu-id="c4462-105">La version minimale d’Azure Stack prise en charge est la version 1804.</span><span class="sxs-lookup"><span data-stu-id="c4462-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="c4462-106">Remarque : si vous utilisez une version antérieure, installez la version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="c4462-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="c4462-107">Problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="c4462-107">Known issues:</span></span>

- <span data-ttu-id="c4462-108">L’option Fermer l’alerte nécessite la version 1803 d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="c4462-109">Certaines cmdlets de Stockage nécessitent la version 1804 d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="c4462-110">La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public.</span><span class="sxs-lookup"><span data-stu-id="c4462-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="c4462-111">La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.</span><span class="sxs-lookup"><span data-stu-id="c4462-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="c4462-112">Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.</span><span class="sxs-lookup"><span data-stu-id="c4462-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="c4462-113">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="c4462-113">Breaking Changes</span></span>
<span data-ttu-id="c4462-114">Tous les changements cassants liés à la migration à partir de la version 1.2.11 sont décrits ici : https://aka.ms/azspowershellmigration.</span><span class="sxs-lookup"><span data-stu-id="c4462-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="c4462-115">Installer</span><span class="sxs-lookup"><span data-stu-id="c4462-115">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="c4462-116">Contenu :</span><span class="sxs-lookup"><span data-stu-id="c4462-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="c4462-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="c4462-117">Azure Bridge</span></span>
<span data-ttu-id="c4462-118">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="c4462-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="c4462-119">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="c4462-119">Backup</span></span>
<span data-ttu-id="c4462-120">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="c4462-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="c4462-121">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="c4462-121">Configure where backups are stored</span></span>
- <span data-ttu-id="c4462-122">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="c4462-122">Perform backups</span></span>
- <span data-ttu-id="c4462-123">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="c4462-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="c4462-124">Commerce</span><span class="sxs-lookup"><span data-stu-id="c4462-124">Commerce</span></span>
<span data-ttu-id="c4462-125">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="c4462-126">Calcul</span><span class="sxs-lookup"><span data-stu-id="c4462-126">Compute</span></span>
<span data-ttu-id="c4462-127">Préversion du module administrateur Calcul d’Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="c4462-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="c4462-128">Structure</span><span class="sxs-lookup"><span data-stu-id="c4462-128">Fabric</span></span>
<span data-ttu-id="c4462-129">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="c4462-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="c4462-130">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="c4462-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="c4462-131">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="c4462-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="c4462-132">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="c4462-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="c4462-133">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="c4462-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="c4462-134">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="c4462-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="c4462-135">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="c4462-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="c4462-136">Galerie</span><span class="sxs-lookup"><span data-stu-id="c4462-136">Gallery</span></span>
<span data-ttu-id="c4462-137">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="c4462-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="c4462-138">Infrastructure Insights</span></span>
<span data-ttu-id="c4462-139">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="c4462-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="c4462-140">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="c4462-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="c4462-141">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="c4462-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="c4462-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="c4462-142">KeyVault</span></span>
<span data-ttu-id="c4462-143">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="c4462-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="c4462-144">Réseau</span><span class="sxs-lookup"><span data-stu-id="c4462-144">Network</span></span>
<span data-ttu-id="c4462-145">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="c4462-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="c4462-146">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="c4462-146">Management of network quotas</span></span>
- <span data-ttu-id="c4462-147">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="c4462-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="c4462-148">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="c4462-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="c4462-149">Stockage</span><span class="sxs-lookup"><span data-stu-id="c4462-149">Storage</span></span>
<span data-ttu-id="c4462-150">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="c4462-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="c4462-151">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="c4462-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="c4462-152">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="c4462-152">Manage storage quotas</span></span>
- <span data-ttu-id="c4462-153">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="c4462-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="c4462-154">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="c4462-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="c4462-155">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="c4462-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="c4462-156">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="c4462-156">View information about the individual storage components</span></span>
- <span data-ttu-id="c4462-157">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="c4462-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="c4462-158">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="c4462-158">Subscription Admin</span></span>
<span data-ttu-id="c4462-159">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="c4462-160">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="c4462-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="c4462-161">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="c4462-161">Manage plans and offers</span></span>
- <span data-ttu-id="c4462-162">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="c4462-162">View usage and performance information</span></span>
- <span data-ttu-id="c4462-163">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="c4462-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="c4462-164">Abonnement</span><span class="sxs-lookup"><span data-stu-id="c4462-164">Subscription</span></span>
<span data-ttu-id="c4462-165">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="c4462-166">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="c4462-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="c4462-167">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="c4462-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="c4462-168">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="c4462-168">Update</span></span>
<span data-ttu-id="c4462-169">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="c4462-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="c4462-170">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="c4462-170">In this module administrators can:</span></span>
- <span data-ttu-id="c4462-171">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="c4462-171">List and install available updates</span></span>
- <span data-ttu-id="c4462-172">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="c4462-172">Resume interrupted updates</span></span>
- <span data-ttu-id="c4462-173">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="c4462-173">View installed updates</span></span>
