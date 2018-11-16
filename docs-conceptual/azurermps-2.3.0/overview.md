---
title: Vue d’ensemble d’Azure Stack PowerShell | Microsoft Docs
description: Une vue d’ensemble d’Azure Stack PowerShell avec des instructions sur les procédures d’installation et de configuration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51575414"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="43d77-103">Module AzureRM 2.3.0</span><span class="sxs-lookup"><span data-stu-id="43d77-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="43d77-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="43d77-104">Requirements:</span></span>
<span data-ttu-id="43d77-105">La version minimale d’Azure Stack prise en charge est la version 1808.</span><span class="sxs-lookup"><span data-stu-id="43d77-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="43d77-106">Remarque : si vous utilisez une version antérieure, installez la version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="43d77-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="43d77-107">Installer</span><span class="sxs-lookup"><span data-stu-id="43d77-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="43d77-108">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="43d77-108">Release Notes</span></span>
* <span data-ttu-id="43d77-109">La version 2.3.0 est fournie avec une liste de changements cassants.</span><span class="sxs-lookup"><span data-stu-id="43d77-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="43d77-110">Pour mettre à niveau à partir de la version 1.2.11, nous avons créé un guide de migration sur https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="43d77-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="43d77-111">Cette version correspond au profil d’api 2018-03-01 hybride azurestack spécifique</span><span class="sxs-lookup"><span data-stu-id="43d77-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="43d77-112">Tous les modules utilisent une dépendance supérieure ou égale sur le module AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="43d77-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="43d77-113">Les versions de l’API prises en charge par chacun des modules sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="43d77-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="43d77-114">Compute - 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="43d77-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="43d77-115">Réseau - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="43d77-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="43d77-116">Stockage - 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="43d77-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="43d77-117">Ressources - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="43d77-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="43d77-118">KeyVault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="43d77-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="43d77-119">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="43d77-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="43d77-120">Le mappage complet de la version de l’API pour chacun des types de ressources est disponible sur https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="43d77-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="43d77-121">Contenu :</span><span class="sxs-lookup"><span data-stu-id="43d77-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="43d77-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="43d77-122">Azure Bridge</span></span>
<span data-ttu-id="43d77-123">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="43d77-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="43d77-124">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="43d77-124">Backup</span></span>
<span data-ttu-id="43d77-125">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="43d77-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="43d77-126">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="43d77-126">Configure where backups are stored</span></span>
- <span data-ttu-id="43d77-127">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="43d77-127">Perform backups</span></span>
- <span data-ttu-id="43d77-128">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="43d77-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="43d77-129">Commerce</span><span class="sxs-lookup"><span data-stu-id="43d77-129">Commerce</span></span>
<span data-ttu-id="43d77-130">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="43d77-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="43d77-131">Calcul</span><span class="sxs-lookup"><span data-stu-id="43d77-131">Compute</span></span>
<span data-ttu-id="43d77-132">Préversion du module administrateur de calcul Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme, les disques managés et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="43d77-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="43d77-133">Structure</span><span class="sxs-lookup"><span data-stu-id="43d77-133">Fabric</span></span>
<span data-ttu-id="43d77-134">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="43d77-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="43d77-135">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="43d77-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="43d77-136">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="43d77-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="43d77-137">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="43d77-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="43d77-138">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="43d77-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="43d77-139">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="43d77-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="43d77-140">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="43d77-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="43d77-141">Galerie</span><span class="sxs-lookup"><span data-stu-id="43d77-141">Gallery</span></span>
<span data-ttu-id="43d77-142">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="43d77-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="43d77-143">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="43d77-143">Infrastructure Insights</span></span>
<span data-ttu-id="43d77-144">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="43d77-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="43d77-145">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="43d77-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="43d77-146">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="43d77-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="43d77-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="43d77-147">KeyVault</span></span>
<span data-ttu-id="43d77-148">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="43d77-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="43d77-149">Réseau</span><span class="sxs-lookup"><span data-stu-id="43d77-149">Network</span></span>
<span data-ttu-id="43d77-150">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="43d77-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="43d77-151">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="43d77-151">Management of network quotas</span></span>
- <span data-ttu-id="43d77-152">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="43d77-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="43d77-153">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="43d77-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="43d77-154">Stockage</span><span class="sxs-lookup"><span data-stu-id="43d77-154">Storage</span></span>
<span data-ttu-id="43d77-155">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="43d77-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="43d77-156">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="43d77-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="43d77-157">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="43d77-157">Manage storage quotas</span></span>
- <span data-ttu-id="43d77-158">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="43d77-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="43d77-159">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="43d77-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="43d77-160">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="43d77-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="43d77-161">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="43d77-161">View information about the individual storage components</span></span>
- <span data-ttu-id="43d77-162">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="43d77-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="43d77-163">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="43d77-163">Subscription Admin</span></span>
<span data-ttu-id="43d77-164">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="43d77-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="43d77-165">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="43d77-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="43d77-166">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="43d77-166">Manage plans and offers</span></span>
- <span data-ttu-id="43d77-167">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="43d77-167">View usage and performance information</span></span>
- <span data-ttu-id="43d77-168">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="43d77-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="43d77-169">Abonnement</span><span class="sxs-lookup"><span data-stu-id="43d77-169">Subscription</span></span>
<span data-ttu-id="43d77-170">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="43d77-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="43d77-171">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="43d77-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="43d77-172">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="43d77-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="43d77-173">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="43d77-173">Update</span></span>
<span data-ttu-id="43d77-174">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="43d77-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="43d77-175">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="43d77-175">In this module administrators can:</span></span>
- <span data-ttu-id="43d77-176">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="43d77-176">List and install available updates</span></span>
- <span data-ttu-id="43d77-177">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="43d77-177">Resume interrupted updates</span></span>
- <span data-ttu-id="43d77-178">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="43d77-178">View installed updates</span></span>
