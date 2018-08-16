---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106410"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="c2567-103">Installer Azure PowerShell sur macOS ou Linux</span><span class="sxs-lookup"><span data-stu-id="c2567-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="c2567-104">Il est désormais possible d’exécuter Azure PowerShell dans PowerShell Core v6 pour des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="c2567-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="c2567-105">Cette version de PowerShell est conçue pour une utilisation sur n’importe quelle plateforme prenant en charge .NET Core.</span><span class="sxs-lookup"><span data-stu-id="c2567-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="c2567-106">Pour utiliser ces plateformes, une version .NET Core spéciale d’Azure PowerShell est disponible.</span><span class="sxs-lookup"><span data-stu-id="c2567-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="c2567-107">Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="c2567-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="c2567-108">La prise en charge de ces produits est limitée.</span><span class="sxs-lookup"><span data-stu-id="c2567-108">Support for these products is limited.</span></span> <span data-ttu-id="c2567-109">Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="c2567-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="c2567-110">Problèmes pour PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="c2567-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="c2567-111">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c2567-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="c2567-112">Installer PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="c2567-112">Install PowerShell Core</span></span>

<span data-ttu-id="c2567-113">Les instructions d’installation de PowerShell Core sont différentes sur macOS et la plupart des distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="c2567-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="c2567-114">Vous trouverez des instructions détaillées dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="c2567-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="c2567-115">Installer PowerShell Core sur macOS</span><span class="sxs-lookup"><span data-stu-id="c2567-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="c2567-116">Installer PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="c2567-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="c2567-117">Installer Azure PowerShell pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="c2567-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="c2567-118">PowerShell Core est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="c2567-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="c2567-119">L’installation des modules dans PowerShell nécessite des privilèges élevés. Vous devez donc démarrer votre session en tant que superutilisateur :</span><span class="sxs-lookup"><span data-stu-id="c2567-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="c2567-120">Pour installer Azure PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c2567-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="c2567-121">Le module `AzureRM` détaillé dans d’autres articles n’est pas conçu pour .NET Core et ne fonctionne pas avec PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="c2567-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="c2567-122">`AzureRM` et `AzureRM.NetCore` utilisent les mêmes noms de cmdlet. Ils se différencient par le nom du module cumulatif et par la version .NET sur laquelle ils ont été conçus.</span><span class="sxs-lookup"><span data-stu-id="c2567-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="c2567-123">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="c2567-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="c2567-124">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="c2567-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="c2567-125">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="c2567-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="c2567-126">Se connecter</span><span class="sxs-lookup"><span data-stu-id="c2567-126">Sign in</span></span>

<span data-ttu-id="c2567-127">Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM.Netcore` dans votre session PowerShell avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="c2567-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="c2567-128">L’importation d’un module ne nécessite __pas__ de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="c2567-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="c2567-129">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="c2567-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="c2567-130">L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="c2567-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="c2567-131">Sur macOS et Linux, vous devez utiliser votre profil via la variable d’environnement `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="c2567-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="c2567-132">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).</span><span class="sxs-lookup"><span data-stu-id="c2567-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="c2567-133">Applets de commande disponibles</span><span class="sxs-lookup"><span data-stu-id="c2567-133">Available cmdlets</span></span>

<span data-ttu-id="c2567-134">Les modules Azure PowerShell pour .NET Core sont en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="c2567-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="c2567-135">Ces modules ne fournissent pas l’ensemble des applets de commande qui sont disponibles pour la version Windows des modules.</span><span class="sxs-lookup"><span data-stu-id="c2567-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="c2567-136">Les fonctions suivantes sont implémentées dans les modules AzureRM.Netcore :</span><span class="sxs-lookup"><span data-stu-id="c2567-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="c2567-137">Account management</span><span class="sxs-lookup"><span data-stu-id="c2567-137">Account management</span></span>
  * <span data-ttu-id="c2567-138">Se connecter avec un compte Microsoft, un compte d’organisation ou un principal du service via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c2567-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="c2567-139">Enregistrer les informations d’identification sur disque avec Save-AzureRmContext et charger les informations d’identification enregistrées avec Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c2567-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="c2567-140">Environnement</span><span class="sxs-lookup"><span data-stu-id="c2567-140">Environment</span></span>
  * <span data-ttu-id="c2567-141">Obtenir les différents environnements Microsoft Azure prédéfinis</span><span class="sxs-lookup"><span data-stu-id="c2567-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="c2567-142">Ajouter/définir/supprimer des environnements personnalisés (comme vos environnements Azure Stack ou Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="c2567-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="c2567-143">Applets de commande de plan de gestion pour les services Azure avec les interfaces Resource Manager et Gestion des services.</span><span class="sxs-lookup"><span data-stu-id="c2567-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="c2567-144">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="c2567-144">Virtual Machine</span></span>
  * <span data-ttu-id="c2567-145">App Service (sites web)</span><span class="sxs-lookup"><span data-stu-id="c2567-145">App Service (Websites)</span></span>
  * <span data-ttu-id="c2567-146">Base de données SQL</span><span class="sxs-lookup"><span data-stu-id="c2567-146">SQL Database</span></span>
  * <span data-ttu-id="c2567-147">Stockage</span><span class="sxs-lookup"><span data-stu-id="c2567-147">Storage</span></span>
  * <span data-ttu-id="c2567-148">Réseau</span><span class="sxs-lookup"><span data-stu-id="c2567-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="c2567-149">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c2567-149">Next Steps</span></span>

<span data-ttu-id="c2567-150">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c2567-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
