---
title: Autres méthodes d’installation d’Azure PowerShell | Microsoft Docs
description: Comment installer Azure PowerShell à l’aide du package MSI ou de Web Platform Installer.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: fd5263a327fa8e4b70418bf6fa7702d8c5383733
ms.sourcegitcommit: 8376e0bc5f862d382d7283ba72990e3707591e7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2018
---
# <a name="other-installation-methods"></a><span data-ttu-id="1ebb7-103">Autres méthodes d’installation</span><span class="sxs-lookup"><span data-stu-id="1ebb7-103">Other installation methods</span></span>

<span data-ttu-id="1ebb7-104">Azure PowerShell peut être installé selon plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="1ebb7-105">La méthode recommandée est d’utiliser PowerShellGet avec PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="1ebb7-106">Vous pouvez installer Azure PowerShell sur Windows à l’aide de Web Platform Installer (WebPI) ou du fichier MSI disponible sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="1ebb7-107">Vous pouvez aussi installer Azure PowerShell dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="1ebb7-108">Installer sur Windows à l’aide de Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="1ebb7-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="1ebb7-109">L’installation de la dernière version d’Azure PowerShell à l’aide de WebPI s’effectue de la même façon que pour les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="1ebb7-110">Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="1ebb7-111">Si vous aviez précédemment installé les modules Azure à partir de PowerShell Gallery, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="1ebb7-112">Cette méthode simplifie votre environnement, car elle garantit qu’une seule version d’Azure PowerShell est installée.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="1ebb7-113">Toutefois, certains scénarios peuvent nécessiter d’avoir plusieurs versions installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="1ebb7-114">PowerShell Gallery installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="1ebb7-115">Le programme d’installation WebPI installe les modules Azure dans `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="1ebb7-116">Si une erreur se produit pendant l’installation, vous pouvez supprimer manuellement les dossiers Azure\* de votre dossier `$env:ProgramFiles\WindowsPowerShell\Modules`, puis réessayer l’installation.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="1ebb7-117">Une fois l’installation terminée, votre paramètre `$env:PSModulePath` doit inclure les répertoires contenant les applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1ebb7-118">Vous pouvez exécuter la commande suivante pour vérifier qu’Azure PowerShell a bien été installé.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="1ebb7-119">Un problème connu peut se produire quand vous effectuez l’installation à partir de WebPI.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="1ebb7-120">Si votre ordinateur nécessite d’être redémarré après des mises à jour du système ou d’autres installations, il se peut que le chemin `$env:PSModulePath` ne soit pas mis à jour avec le chemin d’installation d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="1ebb7-121">Quand vous essayez de charger ou d’exécuter des applets de commande après l’installation, vous pouvez recevoir le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="1ebb7-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="1ebb7-122">Vous pouvez résoudre cette erreur en redémarrant l’ordinateur ou en important le module avec le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="1ebb7-123">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="1ebb7-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="1ebb7-124">Installer sur Windows à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="1ebb7-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="1ebb7-125">Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="1ebb7-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="1ebb7-126">Si vous avez installé des versions antérieures de modules Azure, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="1ebb7-127">Le package MSI installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`, mais ne crée pas de dossiers spécifiques pour différentes versions.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="1ebb7-128">Installer dans un conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="1ebb7-128">Install in a Docker container</span></span>

<span data-ttu-id="1ebb7-129">Nous tenons à jour une image Docker préconfigurée avec Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="1ebb7-130">Exécutez le conteneur avec `docker run`.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="1ebb7-131">Nous tenons également à jour une partie des applets de commande en tant que conteneur PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="1ebb7-132">Pour Mac/Linux, utilisez l’image `latest`.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="1ebb7-133">Pour Windows, utilisez l’image `nanoserver`.</span><span class="sxs-lookup"><span data-stu-id="1ebb7-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="1ebb7-134">Azure PowerShell est installé sur l’image via `Install-Module` à partir de [PowerShell Gallery](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="1ebb7-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>
