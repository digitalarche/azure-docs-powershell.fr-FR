---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8e63e3efb2671eef435498063010d5704c793060
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807505"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="caaac-103">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="caaac-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="caaac-104">Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="caaac-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="caaac-105">Ces instructions s’appliquent aux plateformes Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="caaac-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="caaac-106">Pour le module Az, actuellement aucune autre méthode d’installation n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="caaac-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="caaac-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caaac-107">Requirements</span></span>

<span data-ttu-id="caaac-108">Azure PowerShell fonctionne avec PowerShell 5.1 ou ultérieur sur Windows, ou avec PowerShell 6.x et ultérieur sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="caaac-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="caaac-109">Si vous n’êtes pas sûr d’avoir PowerShell, ou si vous êtes sur Mac OS ou Linux, [installez la dernière version de PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="caaac-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="caaac-110">Pour vérifier votre version de PowerShell, exécutez la commande :</span><span class="sxs-lookup"><span data-stu-id="caaac-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="caaac-111">Pour exécuter Azure PowerShell dans PowerShell 5.1 sur Windows :</span><span class="sxs-lookup"><span data-stu-id="caaac-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="caaac-112">Mettrez à jour vers [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="caaac-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="caaac-113">Si vous êtes sur Windows 10, PowerShell 5.1 est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="caaac-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="caaac-114">Installez [.NET Framework 4.7.2 ou ultérieur](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="caaac-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="caaac-115">Il n’existe aucune exigence supplémentaire pour Azure PowerShell lors de l’utilisation de PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="caaac-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="caaac-116">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="caaac-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="caaac-117">Vous __ne pouvez pas__ avoir en même temps les modules AzureRM et Az installés pour PowerShell 5.1 pour Windows installés.</span><span class="sxs-lookup"><span data-stu-id="caaac-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="caaac-118">Si vous avez besoin de conserver AzureRM disponible sur votre système, installez le module Az pour PowerShell Core 6.x ou ultérieur.</span><span class="sxs-lookup"><span data-stu-id="caaac-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="caaac-119">Pour cela, [installez PowerShell Core 6.x ou ultérieur](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) et suivez ces instructions dans un terminal PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="caaac-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="caaac-120">La méthode d’installation recommandée consiste seulement à installer pour l’utilisateur actif :</span><span class="sxs-lookup"><span data-stu-id="caaac-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="caaac-121">Si vous souhaitez installer pour tous les utilisateurs d’un système, vous devez avoir des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="caaac-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="caaac-122">À partir d’une session PowerShell avec élévation de privilèges, effectuez l’exécution en tant qu’administrateur ou avec la commande `sudo` sur MacOS ou Linux :</span><span class="sxs-lookup"><span data-stu-id="caaac-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="caaac-123">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="caaac-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="caaac-124">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="caaac-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="caaac-125">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="caaac-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="caaac-126">Le module Az est un module cumulatif pour les cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="caaac-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="caaac-127">Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.</span><span class="sxs-lookup"><span data-stu-id="caaac-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="caaac-128">Résolution de problèmes</span><span class="sxs-lookup"><span data-stu-id="caaac-128">Troubleshooting</span></span>

<span data-ttu-id="caaac-129">Voici quelques problèmes courants rencontrés lors de l’installation du module Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="caaac-129">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="caaac-130">Si vous rencontrez un problème qui n’est pas listé ici, [signalez ce problème sur GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="caaac-130">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="caaac-131">Le proxy bloque la connexion</span><span class="sxs-lookup"><span data-stu-id="caaac-131">Proxy blocks connection</span></span>

<span data-ttu-id="caaac-132">Si vous recevez des erreurs de `Install-Module` indiquant que PowerShell Gallery est inaccessible, vous êtes peut-être derrière un proxy.</span><span class="sxs-lookup"><span data-stu-id="caaac-132">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="caaac-133">Les différents systèmes d’exploitation ont des exigences propres pour la configuration d’un proxy à l’échelle du système, qui ne sont pas abordées en détail ici.</span><span class="sxs-lookup"><span data-stu-id="caaac-133">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="caaac-134">Contactez votre administrateur système pour vos paramètres de proxy et pour savoir comment les configurer pour votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="caaac-134">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="caaac-135">PowerShell lui-même peut ne pas être configuré pour utiliser ce proxy automatiquement.</span><span class="sxs-lookup"><span data-stu-id="caaac-135">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="caaac-136">Avec PowerShell 5.1 et ultérieur, configurez le proxy à utiliser pour une session PowerShell avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="caaac-136">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="caaac-137">Si vos informations d’identification du système d’exploitation sont configurées correctement, ceci va router les demandes PowerShell via le proxy.</span><span class="sxs-lookup"><span data-stu-id="caaac-137">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="caaac-138">Pour conserver cette configuration entre les sessions, ajoutez la commande à un [profil PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="caaac-138">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="caaac-139">Pour que l’installation du package soit possible, votre proxy doit autoriser les connexions HTTPS à l’adresse suivante :</span><span class="sxs-lookup"><span data-stu-id="caaac-139">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="caaac-140">Se connecter</span><span class="sxs-lookup"><span data-stu-id="caaac-140">Sign in</span></span>

<span data-ttu-id="caaac-141">Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="caaac-141">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="caaac-142">Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="caaac-142">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="caaac-143">En raison de la structure du module, cette opération peut prendre quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="caaac-143">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="caaac-144">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="caaac-144">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="caaac-145">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="caaac-145">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="caaac-146">Mise à jour du module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="caaac-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="caaac-147">En raison de la façon dont le module Az est empaqueté, la commande [Update-Module](/powershell/module/powershellget/update-module) ne met pas correctement à jour votre installation.</span><span class="sxs-lookup"><span data-stu-id="caaac-147">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="caaac-148">Techniquement, Az est un métamodule, qui inclut tous les sous-modules contenant des applets de commande pour interagir avec les services Azure.</span><span class="sxs-lookup"><span data-stu-id="caaac-148">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="caaac-149">Cela signifie que pour mettre à jour le module Azure PowerShell, vous devez faire une __réinstallation__ au lieu d’une simple __mise à jour__.</span><span class="sxs-lookup"><span data-stu-id="caaac-149">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="caaac-150">Cette opération s’effectue de la même façon que l’installation, mais il peut être nécessaire d’ajouter l’argument `-Force` :</span><span class="sxs-lookup"><span data-stu-id="caaac-150">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="caaac-151">Bien que cela puisse remplacer les modules installés, des versions plus anciennes peuvent néanmoins rester présentes sur votre système.</span><span class="sxs-lookup"><span data-stu-id="caaac-151">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="caaac-152">Pour savoir comment supprimer d’anciennes versions d’Azure PowerShell de votre système, consultez l’article [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="caaac-152">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="caaac-153">Utiliser plusieurs versions d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="caaac-153">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="caaac-154">Il est possible d’installer plusieurs versions d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="caaac-154">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="caaac-155">Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="caaac-155">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="caaac-156">Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="caaac-156">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="caaac-157">Vous pouvez installer ou charger une version spécifique du module `Az` à l’aide de l’argument `-RequiredVersion` :</span><span class="sxs-lookup"><span data-stu-id="caaac-157">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="caaac-158">Si plusieurs versions du module sont installées, la version la plus récente est chargée par défaut par `Import-Module` et le chargement automatique de module.</span><span class="sxs-lookup"><span data-stu-id="caaac-158">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="caaac-159">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="caaac-159">Provide feedback</span></span>

<span data-ttu-id="caaac-160">Si vous rencontrez un bogue dans Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="caaac-160">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="caaac-161">Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="caaac-161">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="caaac-162">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="caaac-162">Next Steps</span></span>

<span data-ttu-id="caaac-163">Pour en savoir plus sur les modules PowerShell et leurs fonctionnalités, consultez l’article sur la [prise en main d’Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="caaac-163">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="caaac-164">Si vous êtes familiarisé avec Azure PowerShell et devez effectuer une migration depuis AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="caaac-164">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
