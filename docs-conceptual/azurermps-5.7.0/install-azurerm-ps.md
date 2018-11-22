---
title: Installer Azure PowerShell sur Windows avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: a868a62bd7bb2f39775a3b7878e2c8484c50438d
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52258551"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="888d1-103">Installer Azure PowerShell sur Windows avec PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="888d1-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="888d1-104">Cet article explique les étapes permettant d’installer les modules Azure PowerShell dans un environnement Windows à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="888d1-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="888d1-105">Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="888d1-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="888d1-106">Pour obtenir des instructions sur l’installation d’Azure PowerShell sur d’autres plateformes, consultez [Installation et configuration d’Azure PowerShell sur macOS et Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="888d1-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="888d1-107">Le modèle de déploiement Azure Classic n’est pas pris en charge par cette version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="888d1-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="888d1-108">Pour la prise en charge des déploiements Classic, suivez les instructions dans [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="888d1-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="888d1-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="888d1-109">Requirements</span></span>

<span data-ttu-id="888d1-110">Pour installer Azure PowerShell, il vous faut la version 1.1.2.0 ou plus récente de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="888d1-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="888d1-111">Pour savoir si elle est disponible sur votre système, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="888d1-111">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="888d1-112">Vous devez obtenir un graphique similaire à la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="888d1-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="888d1-113">Si vous devez mettre à jour votre installation de PowerShellGet, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="888d1-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="888d1-114">Si PowerShellGet n’est pas installé, suivez les instructions dans le tableau ci-dessous pour votre système.</span><span class="sxs-lookup"><span data-stu-id="888d1-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="888d1-115">Scénario</span><span class="sxs-lookup"><span data-stu-id="888d1-115">Scenario</span></span>|<span data-ttu-id="888d1-116">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="888d1-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="888d1-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="888d1-117">Windows 10</span></span><br/><span data-ttu-id="888d1-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="888d1-118">Windows Server 2016</span></span>|<span data-ttu-id="888d1-119">Intégré à Windows Management Framework (WMF) 5.0 inclus dans le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="888d1-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="888d1-120">Mise à niveau vers PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="888d1-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="888d1-121">Installer la dernière version de WMF</span><span class="sxs-lookup"><span data-stu-id="888d1-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="888d1-122">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="888d1-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="888d1-123">Windows avec PowerShell 3 ou PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="888d1-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="888d1-124"><il>[Obtenir les modules PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="888d1-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="888d1-125">Exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="888d1-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="888d1-126">L’utilisation de PowerShellGet nécessite une stratégie d’exécution pour exécuter les scripts.</span><span class="sxs-lookup"><span data-stu-id="888d1-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="888d1-127">Pour plus d’informations sur la stratégie d’exécution de PowerShell, consultez [About Execution Policy](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (À propos des stratégies d’exécution).</span><span class="sxs-lookup"><span data-stu-id="888d1-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="888d1-128">Le module décrit dans ce document, AzureRM, utilise .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="888d1-128">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="888d1-129">Cela le rend incompatible avec PowerShell 6.0, qui utilise .NET Core.</span><span class="sxs-lookup"><span data-stu-id="888d1-129">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="888d1-130">Si vous utilisez PowerShell 6.0, suivez les [instructions d’installation pour macOS et Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="888d1-130">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="888d1-131">Installer le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="888d1-131">Install the Azure PowerShell module</span></span>

<span data-ttu-id="888d1-132">Il vous faut des privilèges élevés pour installer des modules à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="888d1-132">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="888d1-133">Pour installer Azure PowerShell, exécutez la commande ci-après dans une session avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="888d1-133">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="888d1-134">Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="888d1-134">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="888d1-135">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="888d1-135">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="888d1-136">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="888d1-136">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="888d1-137">Répondez `Yes` ou `Yes to All` pour procéder à l’installation.</span><span class="sxs-lookup"><span data-stu-id="888d1-137">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="888d1-138">Le module `AzureRM` est un module cumulatif pour les cmdlets Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="888d1-138">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="888d1-139">Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.</span><span class="sxs-lookup"><span data-stu-id="888d1-139">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="888d1-140">Se connecter</span><span class="sxs-lookup"><span data-stu-id="888d1-140">Sign in</span></span>

<span data-ttu-id="888d1-141">Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="888d1-141">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="888d1-142">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="888d1-142">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="888d1-143">L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="888d1-143">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="888d1-144">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).</span><span class="sxs-lookup"><span data-stu-id="888d1-144">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="888d1-145">Mise à jour du module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="888d1-145">Update the Azure PowerShell module</span></span>

<span data-ttu-id="888d1-146">Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="888d1-146">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="888d1-147">Cette commande ne désinstalle __pas__ des versions anciennes.</span><span class="sxs-lookup"><span data-stu-id="888d1-147">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="888d1-148">Si vous voulez supprimer des versions anciennes d’Azure PowerShell de votre système, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="888d1-148">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="888d1-149">Utiliser plusieurs versions d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="888d1-149">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="888d1-150">Il est possible d’installer plusieurs versions d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="888d1-150">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="888d1-151">Il vous faudra peut-être plus d’une version si vous travaillez avec des ressources Azure Stack locales, si vous exécutez une version ancienne de Windows impossible à mettre à jour vers PowerShell 5.0, ou si vous utilisez un modèle de déploiement Azure Classic.</span><span class="sxs-lookup"><span data-stu-id="888d1-151">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="888d1-152">Pour installer une version ancienne, fournissez l’argument `-RequiredVersion` lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="888d1-152">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="888d1-153">Lors du chargement du module Azure PowerShell, la version ancienne est chargée par défaut.</span><span class="sxs-lookup"><span data-stu-id="888d1-153">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="888d1-154">Pour charger une autre version, fournissez l’argument `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="888d1-154">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a><span data-ttu-id="888d1-155">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="888d1-155">Provide feedback</span></span>

<span data-ttu-id="888d1-156">Si vous rencontrez un bogue lors de l’utilisation d’Azure Powershell, veuillez [signaler un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="888d1-156">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="888d1-157">Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="888d1-157">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="888d1-158">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="888d1-158">Next Steps</span></span>

<span data-ttu-id="888d1-159">Pour bien démarrer avec Azure PowerShell, consultez [Démarrer avec Azure PowerShell](get-started-azureps.md) pour en savoir plus sur le module et ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="888d1-159">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>