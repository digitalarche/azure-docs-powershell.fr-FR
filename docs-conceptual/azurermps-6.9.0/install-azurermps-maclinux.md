---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/24/2018
ms.openlocfilehash: 05e86d96b345455f3d3bb3fe6dedf933fff6187c
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179239"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="0b3ae-103">Installer Azure PowerShell sur macOS ou Linux</span><span class="sxs-lookup"><span data-stu-id="0b3ae-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="0b3ae-104">Il est désormais possible d’exécuter Azure PowerShell dans PowerShell Core v6 pour des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="0b3ae-105">Cette version de PowerShell est conçue pour une utilisation sur n’importe quelle plateforme prenant en charge .NET Core.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="0b3ae-106">Pour utiliser ces plateformes, une version .NET Standard d’Azure PowerShell est disponible.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="0b3ae-107">Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Standard sont toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Standard are still in beta.</span></span>
> <span data-ttu-id="0b3ae-108">La prise en charge de ces produits est limitée.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-108">Support for these products is limited.</span></span> <span data-ttu-id="0b3ae-109">Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="0b3ae-110">Problèmes pour PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="0b3ae-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="0b3ae-111">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b3ae-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="0b3ae-112">Installer PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="0b3ae-112">Install PowerShell Core</span></span>

<span data-ttu-id="0b3ae-113">Les instructions d’installation de PowerShell Core sont différentes sur macOS et la plupart des distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="0b3ae-114">Vous trouverez des instructions détaillées dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="0b3ae-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="0b3ae-115">Installer PowerShell Core sur macOS</span><span class="sxs-lookup"><span data-stu-id="0b3ae-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="0b3ae-116">Installer PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="0b3ae-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="0b3ae-117">Installer Azure PowerShell pour .NET Standard</span><span class="sxs-lookup"><span data-stu-id="0b3ae-117">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b3ae-118">Le module `AzureRM` détaillé dans d’autres articles ne fonctionne pas avec PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-118">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="0b3ae-119">Vous devez installer le module `Az` pour obtenir des fonctionnalités Azure PowerShell dans PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-119">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="0b3ae-120">PowerShell Core est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-120">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="0b3ae-121">Démarrez PowerShell avec la commande :</span><span class="sxs-lookup"><span data-stu-id="0b3ae-121">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="0b3ae-122">Pour installer Azure PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0b3ae-122">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="0b3ae-123">Si vous rencontrez une erreur d’autorisations lorsque vous tentez d’installer le module, vous devrez peut-être exécuter PowerShell en mode superutilisateur pour installer les modules.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-123">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="0b3ae-124">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-124">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="0b3ae-125">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="0b3ae-125">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="0b3ae-126">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-126">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="0b3ae-127">Activer les alias</span><span class="sxs-lookup"><span data-stu-id="0b3ae-127">Enable aliases</span></span>

<span data-ttu-id="0b3ae-128">Pour la compatibilité avec le module `AzureRM` existant, le nouveau module `Az` a la possibilité de créer des alias à compatibilité descendante pour les cmdlets `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-128">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="0b3ae-129">Avant d’utiliser le module pour la première fois, configurez ces alias avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0b3ae-129">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="0b3ae-130">Cela configure l’alias pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-130">This sets up aliases for the current user only.</span></span> <span data-ttu-id="0b3ae-131">Consultez l’aide de cmdlet pour les autres valeurs qui peuvent être fournies à `-Scope` pour configurer les alias.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-131">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="0b3ae-132">Si vous rencontrez une erreur relative à un emplacement de chemin d’accès, assurez-vous qu’il existe sur votre système local.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-132">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="0b3ae-133">Pour l’étendue `CurrentUser`, cette erreur peut être résolue en exécutant la commande suivante dans `bash` :</span><span class="sxs-lookup"><span data-stu-id="0b3ae-133">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="0b3ae-134">Se connecter</span><span class="sxs-lookup"><span data-stu-id="0b3ae-134">Sign in</span></span>

<span data-ttu-id="0b3ae-135">Pour commencer à utiliser Azure PowerShell, vous devez charger `Az` dans votre session PowerShell avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-135">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="0b3ae-136">L’importation d’un module ne nécessite __pas__ de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-136">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="0b3ae-137">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-137">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="0b3ae-138">L’importation automatique du module `Az` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="0b3ae-138">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="0b3ae-139">Sur macOS et Linux, vous devez utiliser votre profil via la variable d’environnement `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="0b3ae-139">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="0b3ae-140">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, voir [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0b3ae-140">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="0b3ae-141">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0b3ae-141">Next Steps</span></span>

<span data-ttu-id="0b3ae-142">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0b3ae-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
