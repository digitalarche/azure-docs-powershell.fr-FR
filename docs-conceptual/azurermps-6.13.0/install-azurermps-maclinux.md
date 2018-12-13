---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216668"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="9cbe2-103">Installer Azure PowerShell sur macOS ou Linux</span><span class="sxs-lookup"><span data-stu-id="9cbe2-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="9cbe2-104">Il est désormais possible d’exécuter Azure PowerShell dans PowerShell Core v6 pour des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="9cbe2-105">Cette version de PowerShell est conçue pour une utilisation sur n’importe quelle plateforme prenant en charge .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="9cbe2-106">Pour utiliser ces plateformes, une version .NET Standard d’Azure PowerShell est disponible.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="9cbe2-107">Actuellement, Azure PowerShell pour .NET Standard est toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="9cbe2-108">Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="9cbe2-109">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9cbe2-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="9cbe2-110">Installer PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="9cbe2-110">Install PowerShell Core</span></span>

<span data-ttu-id="9cbe2-111">Les instructions d’installation de PowerShell Core sont différentes sur macOS et la plupart des distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="9cbe2-112">Vous trouverez des instructions détaillées dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="9cbe2-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="9cbe2-113">Installer PowerShell Core sur macOS</span><span class="sxs-lookup"><span data-stu-id="9cbe2-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="9cbe2-114">Installer PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="9cbe2-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="9cbe2-115">Installer Azure PowerShell pour .NET Standard</span><span class="sxs-lookup"><span data-stu-id="9cbe2-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cbe2-116">Le module `AzureRM` détaillé dans d’autres articles ne fonctionne pas avec PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="9cbe2-117">Vous devez installer le module `Az` pour obtenir des fonctionnalités Azure PowerShell dans PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="9cbe2-118">PowerShell Core est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9cbe2-119">Démarrez PowerShell avec la commande :</span><span class="sxs-lookup"><span data-stu-id="9cbe2-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="9cbe2-120">Pour installer Azure PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9cbe2-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="9cbe2-121">Si vous rencontrez une erreur d’autorisations lorsque vous tentez d’installer le module, vous devrez peut-être exécuter PowerShell en mode superutilisateur pour installer les modules.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="9cbe2-122">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9cbe2-123">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="9cbe2-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9cbe2-124">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="9cbe2-125">Activer les alias</span><span class="sxs-lookup"><span data-stu-id="9cbe2-125">Enable aliases</span></span>

<span data-ttu-id="9cbe2-126">Pour la compatibilité avec le module `AzureRM` existant, le nouveau module `Az` a la possibilité de créer des alias à compatibilité descendante pour les cmdlets `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="9cbe2-127">Avant d’utiliser le module pour la première fois, configurez ces alias avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9cbe2-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="9cbe2-128">Cela configure l’alias pour l’utilisateur actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="9cbe2-129">Consultez l’aide de cmdlet pour les autres valeurs qui peuvent être fournies à `-Scope` pour configurer les alias.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="9cbe2-130">Si vous rencontrez une erreur relative à un emplacement de chemin d’accès, assurez-vous qu’il existe sur votre système local.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="9cbe2-131">Pour l’étendue `CurrentUser`, cette erreur peut être résolue en exécutant la commande suivante dans `bash` :</span><span class="sxs-lookup"><span data-stu-id="9cbe2-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="9cbe2-132">Se connecter</span><span class="sxs-lookup"><span data-stu-id="9cbe2-132">Sign in</span></span>

<span data-ttu-id="9cbe2-133">Pour commencer à utiliser Azure PowerShell, vous devez charger `Az` dans votre session PowerShell avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="9cbe2-134">L’importation d’un module ne nécessite __pas__ de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="9cbe2-135">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="9cbe2-136">L’importation automatique du module `Az` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="9cbe2-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="9cbe2-137">Sur macOS et Linux, vous devez utiliser votre profil via la variable d’environnement `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="9cbe2-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="9cbe2-138">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, voir [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9cbe2-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="9cbe2-139">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9cbe2-139">Next Steps</span></span>

<span data-ttu-id="9cbe2-140">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9cbe2-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
