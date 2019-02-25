---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 11a0a1e524d40bd723bff8b41fb2f97093b7abf6
ms.sourcegitcommit: 0b5b0434fba7a752b0199256e04fa34f06aaf33a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56464908"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="3e8f7-103">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e8f7-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="3e8f7-104">Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="3e8f7-105">Ces instructions s’appliquent aux plateformes Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="3e8f7-106">Pour le module Az, actuellement aucune autre méthode d’installation n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8f7-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e8f7-107">Requirements</span></span>

<span data-ttu-id="3e8f7-108">Azure PowerShell fonctionne avec PowerShell 5.1.x ou version supérieure sur Windows ou sur PowerShell 6.x sur n’importe quelle plateforme.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6.x on any platform.</span></span>
<span data-ttu-id="3e8f7-109">Pour vérifier votre version de PowerShell, exécutez la commande :</span><span class="sxs-lookup"><span data-stu-id="3e8f7-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="3e8f7-110">Si vous possédez une version obsolète ou que vous avez besoin d’installer PowerShell consultez [Installer plusieurs versions de PowerShell](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="3e8f7-111">Les informations d’installation de votre plateforme sont liées à partir de cette page.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="3e8f7-112">Si vous utilisez PowerShell 5.x sur Windows, vous devez également avoir installé .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-112">If you are using PowerShell 5.x on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="3e8f7-113">Pour obtenir des instructions sur la mise à jour ou l’installation d’une nouvelle version de .NET Framework, consultez le [guide d’installation de .NET Framework](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="3e8f7-114">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e8f7-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="3e8f7-115">Les modules AzureRM et Az peuvent être installés en même temps.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="3e8f7-116">Si c’est le cas, __n’activez pas les alias__.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="3e8f7-117">L’activation des alias entraînera des conflits entre les cmdlets AzureRM et les alias de commande Az, et peut entraîner des comportements inattendus.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="3e8f7-118">Nous vous recommandons de désinstaller AzureRM avant d’installer le module Az.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="3e8f7-119">Vous pouvez désinstaller AzureRM ou activer les alias à tout moment.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="3e8f7-120">Pour en savoir plus sur les alias de commande AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="3e8f7-121">Pour obtenir des instructions sur la désinstallation, consultez l’article [Désinstaller le module AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="3e8f7-122">Pour installer des modules sur une étendue globale, il vous faut des privilèges élevés pour pouvoir installer des modules à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="3e8f7-123">Pour installer Azure PowerShell, exécutez la commande suivante dans une session avec élévation de privilèges (« Exécuter en tant qu’administrateur » sur Windows, ou avec des privilèges de superutilisateur sur macOS ou Linux) :</span><span class="sxs-lookup"><span data-stu-id="3e8f7-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="3e8f7-124">Si vous n’avez pas accès aux privilèges d’administrateur, vous pouvez en installer pour l’utilisateur actuel en ajoutant l’argument `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="3e8f7-125">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="3e8f7-126">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="3e8f7-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="3e8f7-127">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="3e8f7-128">Le module Az est un module cumulatif pour les cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="3e8f7-129">Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="3e8f7-130">Se connecter</span><span class="sxs-lookup"><span data-stu-id="3e8f7-130">Sign in</span></span>

<span data-ttu-id="3e8f7-131">Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="3e8f7-132">Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="3e8f7-133">En raison de la structure du module, cette opération peut prendre quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="3e8f7-134">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="3e8f7-135">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="3e8f7-136">Mise à jour du module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e8f7-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="3e8f7-137">Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="3e8f7-138">Cette commande ne désinstalle __pas__ les anciennes versions.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="3e8f7-139">Pour savoir comment supprimer d’anciennes versions d’Azure PowerShell de votre système, consultez l’article [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="3e8f7-140">Utiliser plusieurs versions d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e8f7-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="3e8f7-141">Il est possible d’installer plusieurs versions d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="3e8f7-142">Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="3e8f7-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="3e8f7-143">Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="3e8f7-144">Vous pouvez installer ou charger une version spécifique du module `Az` à l’aide de l’argument `-RequiredVersion` :</span><span class="sxs-lookup"><span data-stu-id="3e8f7-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="3e8f7-145">Si plusieurs versions du module sont installées, la version la plus récente est chargée par défaut par `Import-Module` et le chargement automatique de module.</span><span class="sxs-lookup"><span data-stu-id="3e8f7-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="3e8f7-146">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="3e8f7-146">Provide feedback</span></span>

<span data-ttu-id="3e8f7-147">Si vous rencontrez un bogue dans Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="3e8f7-148">Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3e8f7-149">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="3e8f7-149">Next Steps</span></span>

<span data-ttu-id="3e8f7-150">Pour en savoir plus sur les modules PowerShell et leurs fonctionnalités, consultez l’article sur la [prise en main d’Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="3e8f7-151">Si vous êtes familiarisé avec Azure PowerShell et devez effectuer une migration depuis AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="3e8f7-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
