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
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038191"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="efbbd-103">Module AzureRM 2.5.0</span><span class="sxs-lookup"><span data-stu-id="efbbd-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="efbbd-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="efbbd-104">Requirements:</span></span>
<span data-ttu-id="efbbd-105">La version minimale d’Azure Stack prise en charge est 1904.</span><span class="sxs-lookup"><span data-stu-id="efbbd-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="efbbd-106">Remarque : Si vous utilisez une version antérieure, installez la version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="efbbd-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="efbbd-107">Installer</span><span class="sxs-lookup"><span data-stu-id="efbbd-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="efbbd-108">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="efbbd-108">Release Notes</span></span>
* <span data-ttu-id="efbbd-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="efbbd-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="efbbd-110">Nouveau module Resources prenant en charge la version d’API 2018-05-01 avec le profil 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="efbbd-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="efbbd-111">Les opérations PolicyDefinition(2016-12-01) et PolicyAssisgment(2017-06-01-preview) utilisent toujours d’anciennes versions d’API</span><span class="sxs-lookup"><span data-stu-id="efbbd-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="efbbd-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="efbbd-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="efbbd-113">Nouveau module Compute prenant en charge de la version d’API 2017-12-01.</span><span class="sxs-lookup"><span data-stu-id="efbbd-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="efbbd-114">Cette version correspond au profil d’API spécifique à azurestack 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="efbbd-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="efbbd-115">Tous les modules utilisent une dépendance supérieure ou égale sur le module AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="efbbd-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="efbbd-116">Les versions de l’API prises en charge par chacun des modules sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="efbbd-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="efbbd-117">Compute - 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="efbbd-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="efbbd-118">Réseau - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="efbbd-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="efbbd-119">Stockage - 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="efbbd-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="efbbd-120">Ressources - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="efbbd-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="efbbd-121">KeyVault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="efbbd-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="efbbd-122">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="efbbd-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="efbbd-123">Le mappage complet de la version de l’API pour chacun des types de ressources est disponible sur https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="efbbd-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="efbbd-124">Contenu :</span><span class="sxs-lookup"><span data-stu-id="efbbd-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="efbbd-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="efbbd-125">Azure Bridge</span></span>
<span data-ttu-id="efbbd-126">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="efbbd-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="efbbd-127">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="efbbd-127">Backup</span></span>
<span data-ttu-id="efbbd-128">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="efbbd-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="efbbd-129">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="efbbd-129">Configure where backups are stored</span></span>
- <span data-ttu-id="efbbd-130">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="efbbd-130">Perform backups</span></span>
- <span data-ttu-id="efbbd-131">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="efbbd-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="efbbd-132">Commerce</span><span class="sxs-lookup"><span data-stu-id="efbbd-132">Commerce</span></span>
<span data-ttu-id="efbbd-133">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="efbbd-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="efbbd-134">Calcul</span><span class="sxs-lookup"><span data-stu-id="efbbd-134">Compute</span></span>
<span data-ttu-id="efbbd-135">Préversion du module administrateur de calcul Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme, les disques managés et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="efbbd-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="efbbd-136">Structure</span><span class="sxs-lookup"><span data-stu-id="efbbd-136">Fabric</span></span>
<span data-ttu-id="efbbd-137">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="efbbd-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="efbbd-138">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="efbbd-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="efbbd-139">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="efbbd-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="efbbd-140">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="efbbd-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="efbbd-141">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="efbbd-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="efbbd-142">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="efbbd-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="efbbd-143">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="efbbd-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="efbbd-144">Galerie</span><span class="sxs-lookup"><span data-stu-id="efbbd-144">Gallery</span></span>
<span data-ttu-id="efbbd-145">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="efbbd-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="efbbd-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="efbbd-146">Infrastructure Insights</span></span>
<span data-ttu-id="efbbd-147">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="efbbd-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="efbbd-148">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="efbbd-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="efbbd-149">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="efbbd-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="efbbd-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="efbbd-150">KeyVault</span></span>
<span data-ttu-id="efbbd-151">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="efbbd-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="efbbd-152">Réseau</span><span class="sxs-lookup"><span data-stu-id="efbbd-152">Network</span></span>
<span data-ttu-id="efbbd-153">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="efbbd-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="efbbd-154">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="efbbd-154">Management of network quotas</span></span>
- <span data-ttu-id="efbbd-155">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="efbbd-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="efbbd-156">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="efbbd-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="efbbd-157">Stockage</span><span class="sxs-lookup"><span data-stu-id="efbbd-157">Storage</span></span>
<span data-ttu-id="efbbd-158">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="efbbd-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="efbbd-159">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="efbbd-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="efbbd-160">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="efbbd-160">Manage storage quotas</span></span>
- <span data-ttu-id="efbbd-161">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="efbbd-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="efbbd-162">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="efbbd-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="efbbd-163">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="efbbd-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="efbbd-164">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="efbbd-164">View information about the individual storage components</span></span>
- <span data-ttu-id="efbbd-165">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="efbbd-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="efbbd-166">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="efbbd-166">Subscription Admin</span></span>
<span data-ttu-id="efbbd-167">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="efbbd-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="efbbd-168">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="efbbd-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="efbbd-169">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="efbbd-169">Manage plans and offers</span></span>
- <span data-ttu-id="efbbd-170">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="efbbd-170">View usage and performance information</span></span>
- <span data-ttu-id="efbbd-171">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="efbbd-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="efbbd-172">Abonnement</span><span class="sxs-lookup"><span data-stu-id="efbbd-172">Subscription</span></span>
<span data-ttu-id="efbbd-173">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="efbbd-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="efbbd-174">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="efbbd-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="efbbd-175">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="efbbd-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="efbbd-176">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="efbbd-176">Update</span></span>
<span data-ttu-id="efbbd-177">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="efbbd-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="efbbd-178">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="efbbd-178">In this module administrators can:</span></span>
- <span data-ttu-id="efbbd-179">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="efbbd-179">List and install available updates</span></span>
- <span data-ttu-id="efbbd-180">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="efbbd-180">Resume interrupted updates</span></span>
- <span data-ttu-id="efbbd-181">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="efbbd-181">View installed updates</span></span>