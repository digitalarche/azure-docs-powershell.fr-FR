---
title: Installer et configurer Azure PowerShell | Microsoft Docs
description: Comment installer et configurer Azure PowerShell pour la première utilisation.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 7b099fead7cb985fc8f7e6fed55b8c1107caa0d9
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75720376"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="45bed-103">Installer Azure PowerShell sur Windows avec PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="45bed-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="45bed-104">Cet article explique les étapes permettant d’installer les modules Azure PowerShell pour PowerShell 5.x dans un environnement Windows à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="45bed-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="45bed-105">Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="45bed-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="45bed-106">Le modèle de déploiement Azure Classic n’est pas pris en charge par cette version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="45bed-107">Pour la prise en charge des déploiements Classic, suivez les instructions dans [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="45bed-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45bed-108">Le module AzureRM n’est pas pris en charge sur macOS ou Linux.</span><span class="sxs-lookup"><span data-stu-id="45bed-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="45bed-109">Pour utiliser des applets de commande Azure PowerShell sur ces plateformes, [installez le module Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="45bed-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="45bed-110">Étape 1 : Installer PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="45bed-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="45bed-111">Pour installer des éléments à partir de PowerShell Gallery, vous avez besoin du module PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="45bed-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="45bed-112">Vérifiez que votre système a la version appropriée de PowerShellGet et qu’il présente toute la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="45bed-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="45bed-113">Exécutez la commande suivante pour vérifier que PowerShellGet est installé sur votre système.</span><span class="sxs-lookup"><span data-stu-id="45bed-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="45bed-114">Vous devez obtenir un graphique similaire à la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="45bed-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="45bed-115">Vous avez besoin de PowerShellGet version 1.1.2.0 ou versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="45bed-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="45bed-116">Pour mettre à jour PowerShellGet, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="45bed-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="45bed-117">Si PowerShellGet n’est pas installé, consultez la section [Comment obtenir PowerShellGet](#how-to-get-powershellget) dans cet article.</span><span class="sxs-lookup"><span data-stu-id="45bed-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="45bed-118">L’utilisation de PowerShellGet nécessite une stratégie d’exécution pour exécuter les scripts.</span><span class="sxs-lookup"><span data-stu-id="45bed-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="45bed-119">Pour plus d’informations sur la stratégie d’exécution de PowerShell, consultez [About Execution Policy](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (À propos des stratégies d’exécution).</span><span class="sxs-lookup"><span data-stu-id="45bed-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="45bed-120">Le module décrit dans ce document, AzureRM, utilise .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="45bed-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="45bed-121">Cela le rend incompatible avec PowerShell 6.0, qui utilise .NET Core.</span><span class="sxs-lookup"><span data-stu-id="45bed-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="45bed-122">Si vous utilisez PowerShell 6.0, suivez les [instructions d’installation pour macOS et Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="45bed-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="45bed-123">Étape 2 : Installation d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="45bed-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="45bed-124">L’installation d’Azure PowerShell à partir de PowerShell Gallery nécessite des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="45bed-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="45bed-125">Exécutez la commande suivante à partir d’une session PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="45bed-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="45bed-126">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="45bed-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="45bed-127">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="45bed-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="45bed-128">Répondez « Oui » ou « Oui pour tous » pour poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="45bed-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="45bed-129">Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="45bed-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="45bed-130">Le module AzureRM est un module cumulatif pour les applets de commande Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="45bed-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="45bed-131">Quand vous installez le module AzureRM, les autres modules Azure qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="45bed-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="45bed-132">Si vous disposez d’une version précédente d’Azure PowerShell, vous pourriez recevoir une erreur.</span><span class="sxs-lookup"><span data-stu-id="45bed-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="45bed-133">Pour résoudre ce problème, consultez la section [Mise à jour vers une nouvelle version d’Azure PowerShell](#update-azps) de cet article.</span><span class="sxs-lookup"><span data-stu-id="45bed-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="45bed-134">Étape 3 : Charger le module AzureRM</span><span class="sxs-lookup"><span data-stu-id="45bed-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="45bed-135">Une fois le module installé, vous devez le charger dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="45bed-136">Vous devez le faire dans une session PowerShell normale (sans élévation de privilèges).</span><span class="sxs-lookup"><span data-stu-id="45bed-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="45bed-137">Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="45bed-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="45bed-138">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="45bed-138">Next Steps</span></span>

<span data-ttu-id="45bed-139">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="45bed-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="45bed-140">Prise en main d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="45bed-140">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="45bed-141">Signalement de problèmes et envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="45bed-141">Reporting issues and feedback</span></span>

<span data-ttu-id="45bed-142">Si vous rencontrez des bogues en utilisant l’outil, signalez un problème dans la section [Issues](https://github.com/Azure/azure-powershell/issues) (Problèmes) de notre référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="45bed-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="45bed-143">Pour fournir des commentaires à partir de la ligne de commande, utilisez l’applet de commande `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="45bed-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="45bed-144">Forum aux questions</span><span class="sxs-lookup"><span data-stu-id="45bed-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="45bed-145">Comment obtenir PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="45bed-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="45bed-146">Version du SE</span><span class="sxs-lookup"><span data-stu-id="45bed-146">OS Version</span></span>|<span data-ttu-id="45bed-147">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="45bed-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="45bed-148">J’ai Windows 10 ou Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45bed-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="45bed-149">Intégré à Windows Management Framework (WMF) 5.0 inclus dans le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="45bed-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="45bed-150">Je veux effectuer la mise à niveau vers PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="45bed-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="45bed-151">Installer la dernière version de WMF</span><span class="sxs-lookup"><span data-stu-id="45bed-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|
|<span data-ttu-id="45bed-152">Mon ordinateur exécute une version de Windows avec PowerShell 3 ou 4</span><span class="sxs-lookup"><span data-stu-id="45bed-152">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="45bed-153">Obtenir les modules PackageManagement</span><span class="sxs-lookup"><span data-stu-id="45bed-153">Get the PackageManagement modules</span></span>](https://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="45bed-154">Vérification de la version d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="45bed-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="45bed-155">Bien que nous vous encouragions à effectuer la mise à niveau vers la version la plus récente dès que possible, plusieurs versions d’Azure PowerShell sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="45bed-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="45bed-156">Pour déterminer la version d’Azure PowerShell installée, exécutez `Get-InstalledModule AzureRM` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="45bed-156">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="45bed-157">Prise en charge des méthodes de déploiement classiques</span><span class="sxs-lookup"><span data-stu-id="45bed-157">Support for classic deployment methods</span></span>

<span data-ttu-id="45bed-158">Si vous avez des déploiements qui utilisent le modèle de déploiement Classic, vous pouvez installer la version Service Management d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="45bed-159">Pour plus d’informations, consultez [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="45bed-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="45bed-160">Les modules Azure et AzureRM partagent des dépendances communes.</span><span class="sxs-lookup"><span data-stu-id="45bed-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="45bed-161">Si vous utilisez des modules Azure et AzureRM, vous devez installer la même version de chaque package.</span><span class="sxs-lookup"><span data-stu-id="45bed-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="45bed-162">Mise à jour vers une nouvelle version d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="45bed-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="45bed-163">Si vous avez une version précédente d’Azure PowerShell installée qui inclut le module Gestion des services, vous pourriez recevoir l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="45bed-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="45bed-164">Comme le message d’erreur l’indique, vous devez utiliser le paramètre -AllowClobber pour installer le module.</span><span class="sxs-lookup"><span data-stu-id="45bed-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="45bed-165">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="45bed-165">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="45bed-166">Pour plus d’informations, consultez la rubrique pour [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="45bed-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="45bed-167">Installation de versions de modules côte à côte</span><span class="sxs-lookup"><span data-stu-id="45bed-167">Installing module versions side by side</span></span>

<span data-ttu-id="45bed-168">La méthode d’installation avec PowerShellGet est la seule qui prend en charge l’installation de plusieurs versions.</span><span class="sxs-lookup"><span data-stu-id="45bed-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="45bed-169">Utilisez-la, par exemple, si vous avez des scripts écrits à l’aide d’une version précédente d’Azure PowerShell et que vous n’avez pas le temps ou les ressources pour les mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="45bed-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="45bed-170">Les commandes suivantes illustrent l’installation de plusieurs versions d’Azure PowerShell :</span><span class="sxs-lookup"><span data-stu-id="45bed-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="45bed-171">Une seule version du module peut être chargée dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45bed-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="45bed-172">Vous devez ouvrir une nouvelle fenêtre PowerShell et utiliser `Import-Module` pour importer une version spécifique des applets de commande AzureRM :</span><span class="sxs-lookup"><span data-stu-id="45bed-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="45bed-173">Les versions 2.1.0 et 1.2.6 sont les premières versions de module conçues pour être installées et utilisées côte à côte.</span><span class="sxs-lookup"><span data-stu-id="45bed-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="45bed-174">Lors du chargement d’une version antérieure d’Azure PowerShell, des versions incompatibles du module **AzureRM.Profile** sont chargées.</span><span class="sxs-lookup"><span data-stu-id="45bed-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="45bed-175">Ainsi, les applets de commande vous invitent à vous connecter chaque fois que vous exécutez une applet de commande.</span><span class="sxs-lookup"><span data-stu-id="45bed-175">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="45bed-176">Autres méthodes d’installation</span><span class="sxs-lookup"><span data-stu-id="45bed-176">Other installation methods</span></span>

<span data-ttu-id="45bed-177">Pour plus d’informations sur l’installation à l’aide de Web Platform Installer ou du package MSI, consultez [Autres méthodes d’installation](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="45bed-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
