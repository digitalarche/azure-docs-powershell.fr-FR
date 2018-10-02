---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560114"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="2f9e0-103">Installer Azure PowerShell sur macOS ou Linux</span><span class="sxs-lookup"><span data-stu-id="2f9e0-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="2f9e0-104">Il est désormais possible d’exécuter Azure PowerShell dans PowerShell Core v6 pour des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="2f9e0-105">Cette version de PowerShell est conçue pour une utilisation sur n’importe quelle plateforme prenant en charge .NET Core.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="2f9e0-106">Pour utiliser ces plateformes, une version .NET Standard d’Azure PowerShell est disponible.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="2f9e0-107">Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="2f9e0-108">La prise en charge de ces produits est limitée.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-108">Support for these products is limited.</span></span> <span data-ttu-id="2f9e0-109">Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="2f9e0-110">Problèmes pour PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="2f9e0-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="2f9e0-111">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f9e0-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="2f9e0-112">Installer PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="2f9e0-112">Install PowerShell Core</span></span>

<span data-ttu-id="2f9e0-113">Les instructions d’installation de PowerShell Core sont différentes sur macOS et la plupart des distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="2f9e0-114">Vous trouverez des instructions détaillées dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="2f9e0-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="2f9e0-115">Installer PowerShell Core sur macOS</span><span class="sxs-lookup"><span data-stu-id="2f9e0-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="2f9e0-116">Installer PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="2f9e0-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="2f9e0-117">Installer Azure PowerShell pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="2f9e0-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="2f9e0-118">PowerShell Core est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="2f9e0-119">L’installation des modules dans PowerShell nécessite des privilèges élevés. Vous devez donc démarrer votre session en tant que superutilisateur :</span><span class="sxs-lookup"><span data-stu-id="2f9e0-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="2f9e0-120">Pour installer Azure PowerShell, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="2f9e0-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="2f9e0-121">Le module `AzureRM` détaillé dans d’autres articles n’est pas conçu pour .NET Core et ne fonctionne pas avec PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="2f9e0-122">Les modules `Az` contiennent des alias de commande pour toutes les cmdlets `AzureRM`, par conséquent, toute la documentation pour `AzureRM` s’applique.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="2f9e0-123">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="2f9e0-124">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="2f9e0-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="2f9e0-125">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="2f9e0-126">Se connecter</span><span class="sxs-lookup"><span data-stu-id="2f9e0-126">Sign in</span></span>

<span data-ttu-id="2f9e0-127">Pour commencer à utiliser Azure PowerShell, vous devez charger `Az` dans votre session PowerShell avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="2f9e0-128">L’importation d’un module ne nécessite __pas__ de privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="2f9e0-129">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="2f9e0-130">L’importation automatique du module `Az` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="2f9e0-131">Sur macOS et Linux, vous devez utiliser votre profil via la variable d’environnement `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="2f9e0-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="2f9e0-132">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, voir [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="2f9e0-133">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="2f9e0-133">Next Steps</span></span>

<span data-ttu-id="2f9e0-134">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="2f9e0-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
