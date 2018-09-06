# <a name="azure-stack-module-140"></a><span data-ttu-id="f3b42-101">Module Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="f3b42-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b42-102">Requirements:</span><span class="sxs-lookup"><span data-stu-id="f3b42-102">Requirements:</span></span>
<span data-ttu-id="f3b42-103">La version minimale d’Azure Stack prise en charge est la version 1804.</span><span class="sxs-lookup"><span data-stu-id="f3b42-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="f3b42-104">Remarque : si vous utilisez une version antérieure, installez la version 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="f3b42-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="f3b42-105">Problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="f3b42-105">Known issues:</span></span>

- <span data-ttu-id="f3b42-106">L’option Fermer l’alerte nécessite la version 1803 d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="f3b42-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="f3b42-107">La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public.</span><span class="sxs-lookup"><span data-stu-id="f3b42-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="f3b42-108">La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.</span><span class="sxs-lookup"><span data-stu-id="f3b42-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="f3b42-109">Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.</span><span class="sxs-lookup"><span data-stu-id="f3b42-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="f3b42-110">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="f3b42-110">Breaking Changes</span></span>
<span data-ttu-id="f3b42-111">Il n’existe pas de changement cassant par rapport à la version 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="f3b42-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="f3b42-112">Tous les changements cassants liés à la migration à partir de la version 1.2.11 sont décrits ici : https://aka.ms/azspowershellmigration.</span><span class="sxs-lookup"><span data-stu-id="f3b42-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="f3b42-113">Installer</span><span class="sxs-lookup"><span data-stu-id="f3b42-113">Install</span></span>
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
## <a name="release-notes"></a><span data-ttu-id="f3b42-114">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="f3b42-114">Release Notes</span></span>
    * <span data-ttu-id="f3b42-115">La version 1.4.0 de Azurestack ne présente aucun changement cassant par rapport à la version 1.3.0 précédente</span><span class="sxs-lookup"><span data-stu-id="f3b42-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="f3b42-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="f3b42-117">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="f3b42-119">Ajout de nouveaux paramètres BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays dans la cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="f3b42-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="f3b42-120">Ajout d’une cmdlet New-EncyptionKeyBase64 pour faciliter la création de clé de chiffrement</span><span class="sxs-lookup"><span data-stu-id="f3b42-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="f3b42-121">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="f3b42-123">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="f3b42-125">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="f3b42-126">Ajout d’une cmdlet Add-AzsScaleUnitNode pour permettre à l’administrateur d’ajouter de nouveaux nœuds d’unité d’échelle au tampon azurestack</span><span class="sxs-lookup"><span data-stu-id="f3b42-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="f3b42-127">Ajout de cmdlet et de New-AzsScaleUnitNodeObject pour faciliter les objets de paramètre de création d’unité d'échelle</span><span class="sxs-lookup"><span data-stu-id="f3b42-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="f3b42-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="f3b42-129">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="f3b42-131">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="f3b42-133">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="f3b42-135">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="f3b42-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="f3b42-137">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="f3b42-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="f3b42-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="f3b42-139">Ajout d’une cmdlet Move-AzsSubscription pour déplacer des abonnements entre les offres de fournisseur délégué</span><span class="sxs-lookup"><span data-stu-id="f3b42-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="f3b42-140">Ajout d’une cmdlet Test-AzsMoveSubscription pour valider que les abonnements d’utilisateur peuvent être déplacés entre les offres de fournisseur délégué</span><span class="sxs-lookup"><span data-stu-id="f3b42-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="f3b42-141">Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés</span><span class="sxs-lookup"><span data-stu-id="f3b42-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="f3b42-142">Contenu :</span><span class="sxs-lookup"><span data-stu-id="f3b42-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="f3b42-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="f3b42-143">Azure Bridge</span></span>
<span data-ttu-id="f3b42-144">Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b42-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="f3b42-145">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="f3b42-145">Backup</span></span>
<span data-ttu-id="f3b42-146">Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="f3b42-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="f3b42-147">Configurer l’emplacement de stockage des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="f3b42-147">Configure where backups are stored</span></span>
- <span data-ttu-id="f3b42-148">Effectuer des sauvegardes</span><span class="sxs-lookup"><span data-stu-id="f3b42-148">Perform backups</span></span>
- <span data-ttu-id="f3b42-149">Répertorier et restaurer les sauvegardes terminées</span><span class="sxs-lookup"><span data-stu-id="f3b42-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="f3b42-150">Commerce</span><span class="sxs-lookup"><span data-stu-id="f3b42-150">Commerce</span></span>
<span data-ttu-id="f3b42-151">Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="f3b42-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="f3b42-152">Calcul</span><span class="sxs-lookup"><span data-stu-id="f3b42-152">Compute</span></span>
<span data-ttu-id="f3b42-153">Préversion du module administrateur Calcul d’Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme et les extensions de machine virtuelle de calcul.</span><span class="sxs-lookup"><span data-stu-id="f3b42-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="f3b42-154">Structure</span><span class="sxs-lookup"><span data-stu-id="f3b42-154">Fabric</span></span>
<span data-ttu-id="f3b42-155">Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :</span><span class="sxs-lookup"><span data-stu-id="f3b42-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="f3b42-156">Démarrage, arrêt et fermeture des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="f3b42-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="f3b42-157">Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU</span><span class="sxs-lookup"><span data-stu-id="f3b42-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="f3b42-158">Réparation des nœuds d’unités d’échelle</span><span class="sxs-lookup"><span data-stu-id="f3b42-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="f3b42-159">Redémarrage du rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="f3b42-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="f3b42-160">Démarrage, arrêt et fermeture des instances de rôle d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="f3b42-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="f3b42-161">Création de nouveaux pools d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="f3b42-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="f3b42-162">Galerie</span><span class="sxs-lookup"><span data-stu-id="f3b42-162">Gallery</span></span>
<span data-ttu-id="f3b42-163">Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="f3b42-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="f3b42-164">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="f3b42-164">Infrastructure Insights</span></span>
<span data-ttu-id="f3b42-165">Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="f3b42-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="f3b42-166">Afficher l’intégrité de leurs ressources de piles Azure Stack</span><span class="sxs-lookup"><span data-stu-id="f3b42-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="f3b42-167">Afficher et gérer les alertes</span><span class="sxs-lookup"><span data-stu-id="f3b42-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="f3b42-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="f3b42-168">KeyVault</span></span>
<span data-ttu-id="f3b42-169">Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.</span><span class="sxs-lookup"><span data-stu-id="f3b42-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="f3b42-170">Réseau</span><span class="sxs-lookup"><span data-stu-id="f3b42-170">Network</span></span>
<span data-ttu-id="f3b42-171">Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="f3b42-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="f3b42-172">Gérer les quotas réseau</span><span class="sxs-lookup"><span data-stu-id="f3b42-172">Management of network quotas</span></span>
- <span data-ttu-id="f3b42-173">Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge</span><span class="sxs-lookup"><span data-stu-id="f3b42-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="f3b42-174">Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration</span><span class="sxs-lookup"><span data-stu-id="f3b42-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="f3b42-175">Stockage</span><span class="sxs-lookup"><span data-stu-id="f3b42-175">Storage</span></span>
<span data-ttu-id="f3b42-176">Préversion du module administrateur Stockage d’Azure Stack,</span><span class="sxs-lookup"><span data-stu-id="f3b42-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="f3b42-177">qui fournit des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="f3b42-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="f3b42-178">Gérer les quotas de stockage</span><span class="sxs-lookup"><span data-stu-id="f3b42-178">Manage storage quotas</span></span>
- <span data-ttu-id="f3b42-179">Nettoyer de la mémoire les ressources de stockage supprimées</span><span class="sxs-lookup"><span data-stu-id="f3b42-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="f3b42-180">Restaurer les comptes de stockage supprimés</span><span class="sxs-lookup"><span data-stu-id="f3b42-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="f3b42-181">Migrer des conteneurs d’un partage vers un autre</span><span class="sxs-lookup"><span data-stu-id="f3b42-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="f3b42-182">Afficher des informations sur les composants de stockage individuels</span><span class="sxs-lookup"><span data-stu-id="f3b42-182">View information about the individual storage components</span></span>
- <span data-ttu-id="f3b42-183">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="f3b42-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="f3b42-184">Administration des abonnements</span><span class="sxs-lookup"><span data-stu-id="f3b42-184">Subscription Admin</span></span>
<span data-ttu-id="f3b42-185">Préversion du module Administration des abonnements d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="f3b42-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="f3b42-186">Ce module fournit aux administrateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="f3b42-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="f3b42-187">Gérer les plans et les offres</span><span class="sxs-lookup"><span data-stu-id="f3b42-187">Manage plans and offers</span></span>
- <span data-ttu-id="f3b42-188">Afficher des informations sur l’utilisation et les performances</span><span class="sxs-lookup"><span data-stu-id="f3b42-188">View usage and performance information</span></span>
- <span data-ttu-id="f3b42-189">Gérer RBAC</span><span class="sxs-lookup"><span data-stu-id="f3b42-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="f3b42-190">Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3b42-190">Subscription</span></span>
<span data-ttu-id="f3b42-191">Préversion du module Abonnement d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="f3b42-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="f3b42-192">Ce module fournit aux utilisateurs des fonctionnalités pour :</span><span class="sxs-lookup"><span data-stu-id="f3b42-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="f3b42-193">Créer, supprimer et mettre à jour des abonnements</span><span class="sxs-lookup"><span data-stu-id="f3b42-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="f3b42-194">Mettre à jour</span><span class="sxs-lookup"><span data-stu-id="f3b42-194">Update</span></span>
<span data-ttu-id="f3b42-195">Préversion du module administrateur Mise à jour d’Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="f3b42-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="f3b42-196">À l’aide de ce module, les administrateurs peuvent :</span><span class="sxs-lookup"><span data-stu-id="f3b42-196">In this module administrators can:</span></span>
- <span data-ttu-id="f3b42-197">Répertorier et installer les mises à jour disponibles</span><span class="sxs-lookup"><span data-stu-id="f3b42-197">List and install available updates</span></span>
- <span data-ttu-id="f3b42-198">Reprendre les mises à jour interrompues</span><span class="sxs-lookup"><span data-stu-id="f3b42-198">Resume interrupted updates</span></span>
- <span data-ttu-id="f3b42-199">Afficher les mises à jour installées</span><span class="sxs-lookup"><span data-stu-id="f3b42-199">View installed updates</span></span>
