# <a name="azure-stack-module-130"></a><span data-ttu-id="59d5f-101">Module Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="59d5f-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="59d5f-102">Requirements:</span><span class="sxs-lookup"><span data-stu-id="59d5f-102">Requirements:</span></span>
<span data-ttu-id="59d5f-103">La version minimale d’Azure Stack prise en charge est la version 1804.</span><span class="sxs-lookup"><span data-stu-id="59d5f-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="59d5f-104">Remarque : si vous utilisez une version antérieure, installez la version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="59d5f-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="59d5f-105">Problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="59d5f-105">Known issues:</span></span>

- <span data-ttu-id="59d5f-106">L’option Fermer l’alerte nécessite la version 1803 d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="59d5f-107">Certaines cmdlets de Stockage nécessitent la version 1804 d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="59d5f-108">La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public.</span><span class="sxs-lookup"><span data-stu-id="59d5f-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="59d5f-109">La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.</span><span class="sxs-lookup"><span data-stu-id="59d5f-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="59d5f-110">Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.</span><span class="sxs-lookup"><span data-stu-id="59d5f-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="59d5f-111">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="59d5f-111">Breaking Changes</span></span>
<span data-ttu-id="59d5f-112">Tous les changements cassants liés à la migration à partir de la version 1.2.11 sont décrits ici : https://aka.ms/azspowershellmigration.</span><span class="sxs-lookup"><span data-stu-id="59d5f-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="59d5f-113">Installer</span><span class="sxs-lookup"><span data-stu-id="59d5f-113">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="59d5f-114">Contenu :</span><span class="sxs-lookup"><span data-stu-id="59d5f-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="59d5f-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="59d5f-115">Azure Bridge</span></span>
<span data-ttu-id="59d5f-116">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="59d5f-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="59d5f-117">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="59d5f-117">Backup</span></span>
<span data-ttu-id="59d5f-118">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="59d5f-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="59d5f-119">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="59d5f-119">Configure where backups are stored</span></span>
- <span data-ttu-id="59d5f-120">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="59d5f-120">Perform backups</span></span>
- <span data-ttu-id="59d5f-121">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="59d5f-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="59d5f-122">Commerce</span><span class="sxs-lookup"><span data-stu-id="59d5f-122">Commerce</span></span>
<span data-ttu-id="59d5f-123">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="59d5f-124">Calcul</span><span class="sxs-lookup"><span data-stu-id="59d5f-124">Compute</span></span>
<span data-ttu-id="59d5f-125">Préversion du module administrateur Calcul d’Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="59d5f-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="59d5f-126">Structure</span><span class="sxs-lookup"><span data-stu-id="59d5f-126">Fabric</span></span>
<span data-ttu-id="59d5f-127">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="59d5f-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="59d5f-128">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="59d5f-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="59d5f-129">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="59d5f-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="59d5f-130">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="59d5f-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="59d5f-131">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="59d5f-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="59d5f-132">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="59d5f-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="59d5f-133">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="59d5f-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="59d5f-134">Galerie</span><span class="sxs-lookup"><span data-stu-id="59d5f-134">Gallery</span></span>
<span data-ttu-id="59d5f-135">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="59d5f-136">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="59d5f-136">Infrastructure Insights</span></span>
<span data-ttu-id="59d5f-137">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="59d5f-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="59d5f-138">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="59d5f-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="59d5f-139">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="59d5f-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="59d5f-140">KeyVault</span><span class="sxs-lookup"><span data-stu-id="59d5f-140">KeyVault</span></span>
<span data-ttu-id="59d5f-141">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="59d5f-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="59d5f-142">Réseau</span><span class="sxs-lookup"><span data-stu-id="59d5f-142">Network</span></span>
<span data-ttu-id="59d5f-143">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="59d5f-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="59d5f-144">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="59d5f-144">Management of network quotas</span></span>
- <span data-ttu-id="59d5f-145">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="59d5f-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="59d5f-146">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="59d5f-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="59d5f-147">Stockage</span><span class="sxs-lookup"><span data-stu-id="59d5f-147">Storage</span></span>
<span data-ttu-id="59d5f-148">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="59d5f-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="59d5f-149">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="59d5f-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="59d5f-150">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="59d5f-150">Manage storage quotas</span></span>
- <span data-ttu-id="59d5f-151">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="59d5f-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="59d5f-152">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="59d5f-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="59d5f-153">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="59d5f-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="59d5f-154">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="59d5f-154">View information about the individual storage components</span></span>
- <span data-ttu-id="59d5f-155">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="59d5f-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="59d5f-156">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="59d5f-156">Subscription Admin</span></span>
<span data-ttu-id="59d5f-157">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="59d5f-158">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="59d5f-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="59d5f-159">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="59d5f-159">Manage plans and offers</span></span>
- <span data-ttu-id="59d5f-160">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="59d5f-160">View usage and performance information</span></span>
- <span data-ttu-id="59d5f-161">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="59d5f-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="59d5f-162">Abonnement</span><span class="sxs-lookup"><span data-stu-id="59d5f-162">Subscription</span></span>
<span data-ttu-id="59d5f-163">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="59d5f-164">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="59d5f-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="59d5f-165">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="59d5f-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="59d5f-166">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="59d5f-166">Update</span></span>
<span data-ttu-id="59d5f-167">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="59d5f-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="59d5f-168">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="59d5f-168">In this module administrators can:</span></span>
- <span data-ttu-id="59d5f-169">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="59d5f-169">List and install available updates</span></span>
- <span data-ttu-id="59d5f-170">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="59d5f-170">Resume interrupted updates</span></span>
- <span data-ttu-id="59d5f-171">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="59d5f-171">View installed updates</span></span>
