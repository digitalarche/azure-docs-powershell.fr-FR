---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365744"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="6dfcb-103">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6dfcb-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="6dfcb-104">Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="6dfcb-105">Ces instructions s’appliquent aux plateformes Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="6dfcb-106">Pour le module Az, actuellement aucune autre méthode d’installation n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dfcb-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dfcb-107">Requirements</span></span>

<span data-ttu-id="6dfcb-108">Azure PowerShell fonctionne avec PowerShell 5.1 ou ultérieur sur Windows, ou avec PowerShell 6.x et ultérieur sur toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="6dfcb-109">Si vous n’êtes pas sûr d’avoir PowerShell, ou si vous êtes sur Mac OS ou Linux, [installez la dernière version de PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="6dfcb-110">Pour vérifier votre version de PowerShell, exécutez la commande :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="6dfcb-111">Pour exécuter Azure PowerShell dans PowerShell 5.1 sur Windows :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="6dfcb-112">Mettrez à jour vers [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="6dfcb-113">Si vous êtes sur Windows 10, PowerShell 5.1 est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="6dfcb-114">Installez [.NET Framework 4.7.2 ou ultérieur](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="6dfcb-115">Il n’existe aucune exigence supplémentaire pour Azure PowerShell lors de l’utilisation de PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="6dfcb-116">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6dfcb-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="6dfcb-117">Les modules AzureRM et Az peuvent être installés en même temps.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="6dfcb-118">Si c’est le cas, __n’activez pas les alias__.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="6dfcb-119">L’activation des alias entraînera des conflits entre les cmdlets AzureRM et les alias de commande Az, et peut entraîner des comportements inattendus.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="6dfcb-120">Nous vous recommandons de désinstaller AzureRM avant d’installer le module Az.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="6dfcb-121">Vous pouvez désinstaller AzureRM ou activer les alias à tout moment.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="6dfcb-122">Pour en savoir plus sur les alias de commande AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="6dfcb-123">Pour obtenir des instructions sur la désinstallation, consultez l’article [Désinstaller le module AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="6dfcb-124">Pour installer des modules sur une étendue globale, il vous faut des privilèges élevés pour pouvoir installer des modules à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="6dfcb-125">Pour installer Azure PowerShell, exécutez la commande suivante dans une session avec élévation de privilèges (« Exécuter en tant qu’administrateur » sur Windows, ou avec des privilèges de superutilisateur sur macOS ou Linux) :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="6dfcb-126">Si vous n’avez pas accès aux privilèges d’administrateur, vous pouvez en installer pour l’utilisateur actuel en ajoutant l’argument `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="6dfcb-127">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="6dfcb-128">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="6dfcb-129">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="6dfcb-130">Le module Az est un module cumulatif pour les cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6dfcb-131">Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="6dfcb-132">Se connecter</span><span class="sxs-lookup"><span data-stu-id="6dfcb-132">Sign in</span></span>

<span data-ttu-id="6dfcb-133">Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="6dfcb-134">Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="6dfcb-135">En raison de la structure du module, cette opération peut prendre quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="6dfcb-136">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="6dfcb-137">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="6dfcb-138">Mise à jour du module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6dfcb-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="6dfcb-139">En raison de la façon dont le module Az est empaqueté, la commande [Update-Module](/powershell/module/powershellget/update-module) ne met pas correctement à jour votre installation.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="6dfcb-140">Techniquement, Az est un métamodule, qui inclut tous les sous-modules contenant des applets de commande pour interagir avec les services Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="6dfcb-141">Cela signifie que pour mettre à jour le module Azure PowerShell, vous devez faire une __réinstallation__ au lieu d’une simple __mise à jour__.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="6dfcb-142">Cette opération s’effectue de la même façon que l’installation, mais il peut être nécessaire d’ajouter l’argument `-Force` :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="6dfcb-143">Bien que cela puisse remplacer les modules installés, des versions plus anciennes peuvent néanmoins rester présentes sur votre système.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="6dfcb-144">Pour savoir comment supprimer d’anciennes versions d’Azure PowerShell de votre système, consultez l’article [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="6dfcb-145">Utiliser plusieurs versions d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6dfcb-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="6dfcb-146">Il est possible d’installer plusieurs versions d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="6dfcb-147">Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="6dfcb-148">Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="6dfcb-149">Vous pouvez installer ou charger une version spécifique du module `Az` à l’aide de l’argument `-RequiredVersion` :</span><span class="sxs-lookup"><span data-stu-id="6dfcb-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="6dfcb-150">Si plusieurs versions du module sont installées, la version la plus récente est chargée par défaut par `Import-Module` et le chargement automatique de module.</span><span class="sxs-lookup"><span data-stu-id="6dfcb-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="6dfcb-151">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="6dfcb-151">Provide feedback</span></span>

<span data-ttu-id="6dfcb-152">Si vous rencontrez un bogue dans Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="6dfcb-153">Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6dfcb-154">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6dfcb-154">Next Steps</span></span>

<span data-ttu-id="6dfcb-155">Pour en savoir plus sur les modules PowerShell et leurs fonctionnalités, consultez l’article sur la [prise en main d’Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="6dfcb-156">Si vous êtes familiarisé avec Azure PowerShell et devez effectuer une migration depuis AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="6dfcb-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
