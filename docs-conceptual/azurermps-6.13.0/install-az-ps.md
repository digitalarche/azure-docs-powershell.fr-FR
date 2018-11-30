---
title: Installer Azure PowerShell « Az » avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet sur Windows, macOS et Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588177"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="1ef1b-103">Installer le module Azure PowerShell « Az »</span><span class="sxs-lookup"><span data-stu-id="1ef1b-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="1ef1b-104">Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="1ef1b-105">Ces instructions s’appliquent aux plateformes Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="1ef1b-106">Pour la version préliminaire Az, aucune autre méthode d’installation n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="1ef1b-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ef1b-107">Requirements</span></span>

<span data-ttu-id="1ef1b-108">Azure PowerShell fonctionne avec PowerShell 5.x sur Windows ou PowerShell 6.x sur n’importe quelle plateforme.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="1ef1b-109">Pour vérifier la version de PowerShell que vous exécutez sur votre machine, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1ef1b-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="1ef1b-110">Si vous possédez une version obsolète ou que vous avez besoin d’installer PowerShell consultez [Installer plusieurs versions de PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="1ef1b-111">Les informations d’installation de votre plateforme sont liées à partir de cette page.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="1ef1b-112">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ef1b-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1ef1b-113">Les modules `AzureRM` et `Az` peuvent être installés en même temps.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="1ef1b-114">Si c’est le cas, __n’activez pas les alias__.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="1ef1b-115">L’activation des alias entraînera des conflits entre les cmdlets `AzureRM` et les alias de commande `Az`, et peut entraîner des comportements inattendus.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="1ef1b-116">Nous vous recommandons de désinstaller `AzureRM` avant d’installer le module `Az`.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="1ef1b-117">Vous pouvez désinstaller `AzureRM` ou activer les alias à tout moment.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="1ef1b-118">Pour obtenir des instructions sur la désinstallation, consultez [Désinstaller le module Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="1ef1b-119">Pour installer des modules sur une étendue globale, il vous faut des privilèges élevés pour pouvoir installer des modules à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="1ef1b-120">Pour installer Azure PowerShell, exécutez la commande suivante dans une session avec élévation de privilèges (« Exécuter en tant qu’administrateur » sur Windows, ou avec des privilèges de superutilisateur sur macOS ou Linux) :</span><span class="sxs-lookup"><span data-stu-id="1ef1b-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="1ef1b-121">Si vous n’avez pas accès aux privilèges d’administrateur, vous pouvez en installer pour l’utilisateur actuel en ajoutant l’argument `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="1ef1b-122">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1ef1b-123">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1ef1b-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1ef1b-124">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="1ef1b-125">Le module `Az` est un module cumulatif pour les cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1ef1b-126">Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="1ef1b-127">Se connecter</span><span class="sxs-lookup"><span data-stu-id="1ef1b-127">Sign in</span></span>

<span data-ttu-id="1ef1b-128">Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="1ef1b-129">Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="1ef1b-130">En raison de la structure du module, cette opération peut prendre quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="1ef1b-131">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1ef1b-132">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="1ef1b-133">Mise à jour du module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ef1b-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="1ef1b-134">Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="1ef1b-135">Cette commande ne désinstalle __pas__ des versions anciennes.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="1ef1b-136">Si vous voulez supprimer des versions anciennes d’Azure PowerShell de votre système, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="1ef1b-137">Utiliser plusieurs versions d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ef1b-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="1ef1b-138">Il est possible d’installer plusieurs versions d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="1ef1b-139">Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1ef1b-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="1ef1b-140">Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="1ef1b-141">Vous pouvez charger une version spécifique du module `Az` à l’aide de l’argument `-RequiredVersion` avec `Install-Module` et `Import-Module` :</span><span class="sxs-lookup"><span data-stu-id="1ef1b-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="1ef1b-142">Si vous avez plusieurs versions du module installées, la version la plus récente est chargée par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="1ef1b-143">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="1ef1b-143">Provide feedback</span></span>

<span data-ttu-id="1ef1b-144">Si vous rencontrez un bogue lors de l’utilisation d’Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="1ef1b-145">Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="1ef1b-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1ef1b-146">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1ef1b-146">Next Steps</span></span>

<span data-ttu-id="1ef1b-147">Pour bien démarrer avec Azure PowerShell, consultez [Démarrer avec Azure PowerShell](get-started-azureps.md) pour en savoir plus sur le module et ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="1ef1b-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
