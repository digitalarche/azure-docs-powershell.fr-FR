---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323099"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="1028a-103">Installer Azure PowerShell avec PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="1028a-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="1028a-104">Cet article explique les étapes permettant d’installer les modules Azure PowerShell dans un environnement Windows à l’aide de PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1028a-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="1028a-105">Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="1028a-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="1028a-106">Si vous voulez utiliser Azure PowerShell sur macOS ou Linux, consultez l’article suivant : [Installer et configurer Azure PowerShell sur macOS et Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="1028a-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="1028a-107">Conditions requises pour le système</span><span class="sxs-lookup"><span data-stu-id="1028a-107">System requirements</span></span>

<span data-ttu-id="1028a-108">Azure PowerShell version 6.1.0 requiert la version 5.0 (ou une version ultérieure) de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1028a-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="1028a-109">Pour plus d’informations sur la mise à niveau vers PowerShell 5.0, consultez [Mise à niveau du module Windows PowerShell existant](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="1028a-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="1028a-110">PowerShellGet est automatiquement inclus dans PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="1028a-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="1028a-111">Installer ou mettre à jour le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1028a-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="1028a-112">L’installation d’Azure PowerShell à partir de PowerShell Gallery nécessite des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="1028a-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="1028a-113">Exécutez la commande suivante à partir d’une session PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="1028a-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="1028a-114">Cette commande met à jour toute installation existante d’Azure PowerShell sur votre système.</span><span class="sxs-lookup"><span data-stu-id="1028a-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="1028a-115">Si vous avez besoin d’installer plusieurs versions, consultez la réponse des FAQ correspondant à la question [Puis-je installer plusieurs versions d’Azure PowerShell ?](#multiple-versions)</span><span class="sxs-lookup"><span data-stu-id="1028a-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="1028a-116">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1028a-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1028a-117">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="1028a-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1028a-118">Répondez « Oui » ou « Oui pour tous » pour poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="1028a-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="1028a-119">Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="1028a-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="1028a-120">Le module AzureRM est un module cumulatif pour les applets de commande Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="1028a-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="1028a-121">Quand vous installez le module AzureRM, les autres modules Azure PowerShell qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="1028a-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="1028a-122">Charger le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1028a-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="1028a-123">Une fois le module installé, vous devez le charger dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1028a-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="1028a-124">Vous devez le faire dans une session PowerShell normale (sans élévation de privilèges).</span><span class="sxs-lookup"><span data-stu-id="1028a-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="1028a-125">Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="1028a-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="1028a-126">Signalement de problèmes et envoi de commentaires</span><span class="sxs-lookup"><span data-stu-id="1028a-126">Reporting issues and feedback</span></span>

<span data-ttu-id="1028a-127">Si vous rencontrez des bogues avec l’outil, veuillez [signaler un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1028a-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="1028a-128">Pour fournir des commentaires à partir de la ligne de commande, utilisez l’applet de commande `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="1028a-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1028a-129">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1028a-129">Next Steps</span></span>

<span data-ttu-id="1028a-130">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="1028a-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="1028a-131">Prise en main d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1028a-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="1028a-132">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="1028a-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="1028a-133">Comment puis-je vérifier la version d’Azure PowerShell ?</span><span class="sxs-lookup"><span data-stu-id="1028a-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="1028a-134">Bien que nous vous encouragions à effectuer la mise à niveau vers la version la plus récente dès que possible, plusieurs versions d’Azure PowerShell sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1028a-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="1028a-135">Pour déterminer la version d’Azure PowerShell installée, exécutez `Get-Module AzureRM` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="1028a-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="1028a-136">Puis-je utiliser Azure PowerShell pour des déploiements Azure classiques ?</span><span class="sxs-lookup"><span data-stu-id="1028a-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="1028a-137">Si vous avez des déploiements qui utilisent le modèle de déploiement Classic, vous pouvez installer la version Service Management d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1028a-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="1028a-138">Pour plus d’informations, consultez [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="1028a-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="1028a-139">Les modules Azure et AzureRM partagent des dépendances communes.</span><span class="sxs-lookup"><span data-stu-id="1028a-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="1028a-140">Si vous utilisez des modules Azure et AzureRM, vous devez installer la même version de chaque package.</span><span class="sxs-lookup"><span data-stu-id="1028a-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="1028a-141"><a name="multiple-versions"/>Puis-je installer plusieurs versions d’Azure PowerShell ?</span><span class="sxs-lookup"><span data-stu-id="1028a-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="1028a-142">PowerShellGet est la seule méthode d’installation prenant en charge plusieurs versions.</span><span class="sxs-lookup"><span data-stu-id="1028a-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="1028a-143">Pour installer plusieurs versions, vous pouvez ajouter le paramètre `-RequiredVersion` à l’applet de commande `Install-Module`.</span><span class="sxs-lookup"><span data-stu-id="1028a-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="1028a-144">Par exemple, pour installer les versions 6.1.0 et 1.2.9 :</span><span class="sxs-lookup"><span data-stu-id="1028a-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="1028a-145">Une seule version du module peut être chargée dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1028a-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="1028a-146">Vous devez ouvrir une nouvelle fenêtre PowerShell et utiliser `Import-Module` pour importer une version spécifique du module Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1028a-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="1028a-147">Les versions 2.1.0 et 1.2.6 sont les premières versions de module conçues pour être installées et utilisées côte à côte.</span><span class="sxs-lookup"><span data-stu-id="1028a-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="1028a-148">Lors du chargement d’une version antérieure d’Azure PowerShell, des versions incompatibles du module **AzureRM.Profile** sont chargées.</span><span class="sxs-lookup"><span data-stu-id="1028a-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="1028a-149">Ainsi, les applets de commande vous invitent à vous connecter chaque fois que vous exécutez une applet de commande.</span><span class="sxs-lookup"><span data-stu-id="1028a-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
