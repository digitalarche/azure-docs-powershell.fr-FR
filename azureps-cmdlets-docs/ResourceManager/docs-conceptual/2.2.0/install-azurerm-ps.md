---
title: "Installation et configuration d’Azure PowerShell │ Microsoft Docs"
description: "Comment installer et configurer Azure PowerShell pour la première utilisation."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/17/2017
ms.openlocfilehash: 0c1500a8748a3aa4546c6ce1e8d16a635b056edb
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="625dc-103">Installation et configuration d'Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="625dc-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="625dc-104">La méthode recommandée est d’installer Azure PowerShell à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="625dc-104">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="625dc-105">Étape 1 : Installer PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="625dc-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="625dc-106">Pour installer des éléments à partir de PowerShell Gallery, vous avez besoin du module PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="625dc-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="625dc-107">Vérifiez que votre système a la version appropriée de PowerShellGet et qu’il présente toute la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="625dc-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="625dc-108">Exécutez la commande suivante pour vérifier que PowerShellGet est installé sur votre système.</span><span class="sxs-lookup"><span data-stu-id="625dc-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="625dc-109">Vous devez obtenir un graphique similaire à la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="625dc-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="625dc-110">Si PowerShellGet n’est pas installé, consultez la section [Comment obtenir PowerShellGet](#how-to-get-powershellget) dans cet article.</span><span class="sxs-lookup"><span data-stu-id="625dc-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="625dc-111">L’utilisation de PowerShellGet nécessite une stratégie d’exécution pour exécuter les scripts.</span><span class="sxs-lookup"><span data-stu-id="625dc-111">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="625dc-112">Pour plus d’informations sur la stratégie d’exécution de PowerShell, consultez [About Execution Policy](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies) (À propos des stratégies d’exécution).</span><span class="sxs-lookup"><span data-stu-id="625dc-112">For more information about PowerShell's Execution Policy, see [About Execution Policies](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="625dc-113">Étape 2 : Installer Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="625dc-113">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="625dc-114">L’installation d’Azure PowerShell à partir de PowerShell Gallery nécessite des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="625dc-114">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="625dc-115">Exécutez la commande suivante à partir d’une session PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="625dc-115">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM
```

<span data-ttu-id="625dc-116">Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="625dc-116">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="625dc-117">La première fois que vous utilisez PSGallery, le message suivant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="625dc-117">The first time you use the PSGallery you see the following prompt:</span></span>

```
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="625dc-118">Répondez « Oui » ou « Oui pour tous » pour poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="625dc-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="625dc-119">Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="625dc-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="625dc-120">Le module AzureRM est un module cumulatif pour les applets de commande Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="625dc-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="625dc-121">Quand vous installez le module AzureRM, les autres modules Azure qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="625dc-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="625dc-122">Si vous disposez d’une version précédente d’Azure PowerShell, vous pourriez recevoir une erreur.</span><span class="sxs-lookup"><span data-stu-id="625dc-122">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="625dc-123">Pour résoudre ce problème, consultez la section [Mise à jour vers une nouvelle version d’Azure PowerShell](#update-azps) de cet article.</span><span class="sxs-lookup"><span data-stu-id="625dc-123">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="625dc-124">Étape 3 : Charger le module AzureRM</span><span class="sxs-lookup"><span data-stu-id="625dc-124">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="625dc-125">Une fois le module installé, vous devez le charger dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="625dc-125">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="625dc-126">Vous devez le faire dans une session PowerShell normale (sans élévation de privilèges).</span><span class="sxs-lookup"><span data-stu-id="625dc-126">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="625dc-127">Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="625dc-127">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="625dc-128">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="625dc-128">Next Steps</span></span>

<span data-ttu-id="625dc-129">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="625dc-129">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="625dc-130">Prise en main d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="625dc-130">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="625dc-131">Forum Aux Questions</span><span class="sxs-lookup"><span data-stu-id="625dc-131">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="625dc-132">Comment obtenir PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="625dc-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="625dc-133">Version du SE</span><span class="sxs-lookup"><span data-stu-id="625dc-133">OS Version</span></span>|<span data-ttu-id="625dc-134">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="625dc-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="625dc-135">J’ai Windows 10 ou Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="625dc-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="625dc-136">Intégré à Windows Management Framework (WMF) 5.0 inclus dans le système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="625dc-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="625dc-137">Je veux effectuer la mise à niveau vers PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="625dc-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="625dc-138">Installer la dernière version de WMF</span><span class="sxs-lookup"><span data-stu-id="625dc-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="625dc-139">Mon ordinateur exécute une version de Windows avec PowerShell 3 ou 4</span><span class="sxs-lookup"><span data-stu-id="625dc-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="625dc-140">Obtenir les modules PackageManagement</span><span class="sxs-lookup"><span data-stu-id="625dc-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="625dc-141">Vérification de la version d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="625dc-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="625dc-142">Bien que nous vous encouragions à effectuer la mise à niveau vers la version la plus récente dès que possible, plusieurs versions d’Azure PowerShell sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="625dc-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="625dc-143">Pour déterminer la version d’Azure PowerShell installée, exécutez `Get-Module AzureRM` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="625dc-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="625dc-144">Prise en charge des méthodes de déploiement classiques</span><span class="sxs-lookup"><span data-stu-id="625dc-144">Support for classic deployment methods</span></span>

<span data-ttu-id="625dc-145">Si vous avez des déploiements qui utilisent le modèle de déploiement Classic, vous pouvez installer la version Service Management d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="625dc-145">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="625dc-146">Pour plus d’informations, consultez [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="625dc-146">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="625dc-147">Les modules Azure et AzureRM partagent des dépendances communes.</span><span class="sxs-lookup"><span data-stu-id="625dc-147">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="625dc-148">Si vous utilisez des modules Azure et AzureRM, vous devez installer la même version de chaque package.</span><span class="sxs-lookup"><span data-stu-id="625dc-148">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <span data-ttu-id="625dc-149"><a id="update-azps"></a>Mise à jour vers une nouvelle version d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="625dc-149"><a id="update-azps"></a>Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="625dc-150">Si vous avez une version précédente d’Azure PowerShell installée qui inclut le module Gestion des services, vous pourriez recevoir l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="625dc-150">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="625dc-151">Comme le message d’erreur l’indique, vous devez utiliser le paramètre -AllowClobber pour installer le module.</span><span class="sxs-lookup"><span data-stu-id="625dc-151">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="625dc-152">Utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="625dc-152">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module AzureRM -AllowClobber
```

<span data-ttu-id="625dc-153">Pour plus d’informations, consultez la rubrique pour [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="625dc-153">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="625dc-154">Installation de versions de modules côte à côte</span><span class="sxs-lookup"><span data-stu-id="625dc-154">Installing module versions side by side</span></span>

<span data-ttu-id="625dc-155">La méthode d’installation avec PowerShellGet est la seule qui prend en charge l’installation de plusieurs versions.</span><span class="sxs-lookup"><span data-stu-id="625dc-155">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="625dc-156">Utilisez-la, par exemple, si vous avez des scripts écrits à l’aide d’une version précédente d’Azure PowerShell et que vous n’avez pas le temps ou les ressources pour les mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="625dc-156">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="625dc-157">Les commandes suivantes illustrent l’installation de plusieurs versions d’Azure PowerShell :</span><span class="sxs-lookup"><span data-stu-id="625dc-157">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="625dc-158">Une seule version du module peut être chargée dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="625dc-158">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="625dc-159">Vous devez ouvrir une nouvelle fenêtre PowerShell et utiliser `Import-Module` pour importer une version spécifique des applets de commande AzureRM :</span><span class="sxs-lookup"><span data-stu-id="625dc-159">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="625dc-160">Les versions 2.1.0 et 1.2.6 sont les premières versions de module conçues pour être installées et utilisées côte à côte.</span><span class="sxs-lookup"><span data-stu-id="625dc-160">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="625dc-161">Lors du chargement d’une version antérieure d’Azure PowerShell, des versions incompatibles du module **AzureRM.Profile** sont chargées.</span><span class="sxs-lookup"><span data-stu-id="625dc-161">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="625dc-162">Ainsi, les applets de commande vous invitent à vous connecter chaque fois que vous exécutez une applet de commande.</span><span class="sxs-lookup"><span data-stu-id="625dc-162">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="625dc-163">Autres méthodes d’installation</span><span class="sxs-lookup"><span data-stu-id="625dc-163">Other installation methods</span></span>

<span data-ttu-id="625dc-164">Pour plus d’informations sur l’installation à l’aide de Web Platform Installer ou du package MSI, consultez [Autres méthodes d’installation](other-install.md)</span><span class="sxs-lookup"><span data-stu-id="625dc-164">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
