---
title: "Autres méthodes d’installation d’Azure PowerShell | Microsoft Docs"
description: "Comment installer Azure PowerShell à l’aide du package MSI ou de Web Platform Installer."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9cee582f74b7f3260c6ae167a8ac358d360ad8ab
ms.sourcegitcommit: 45587b5091293288e16cfae8ac412e0d42f8f450
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2017
---
# <a name="other-installation-methods"></a><span data-ttu-id="a5867-103">Autres méthodes d’installation</span><span class="sxs-lookup"><span data-stu-id="a5867-103">Other installation methods</span></span>

<span data-ttu-id="a5867-104">Azure PowerShell peut être installé selon plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="a5867-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="a5867-105">La méthode recommandée est d’utiliser PowerShellGet avec PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="a5867-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="a5867-106">Azure PowerShell peut également être installé à l’aide de Web Platform Installer (WebPI) ou du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="a5867-106">Azure PowerShell can be installed using the Web Platform Installer (WebPI) or by using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span>

## <a name="docker"></a><span data-ttu-id="a5867-107">Docker</span><span class="sxs-lookup"><span data-stu-id="a5867-107">Docker</span></span>

<span data-ttu-id="a5867-108">Nous tenons à jour une image Docker préconfigurée avec Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="a5867-108">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="a5867-109">Exécutez le conteneur avec `docker run`.</span><span class="sxs-lookup"><span data-stu-id="a5867-109">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="a5867-110">Nous tenons également à jour une partie des applets de commande en tant que conteneur PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a5867-110">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="a5867-111">Pour Mac/Linux, utilisez l’image `latest`.</span><span class="sxs-lookup"><span data-stu-id="a5867-111">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="a5867-112">Pour Windows, utilisez l’image `nanoserver`.</span><span class="sxs-lookup"><span data-stu-id="a5867-112">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="a5867-113">Azure PowerShell est installé sur l’image via `Install-Module` à partir de [PowerShell Gallery](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="a5867-113">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>

## <a name="install-using-the-web-platform-installer"></a><span data-ttu-id="a5867-114">Installation à l’aide de Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="a5867-114">Install using the Web Platform Installer</span></span>

<span data-ttu-id="a5867-115">L’installation de la dernière version d’Azure PowerShell à l’aide de WebPI s’effectue de la même façon que pour les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="a5867-115">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="a5867-116">Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation.</span><span class="sxs-lookup"><span data-stu-id="a5867-116">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="a5867-117">Si vous aviez précédemment installé les modules Azure à partir de PowerShell Gallery, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a5867-117">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="a5867-118">Cette méthode simplifie votre environnement, car elle garantit qu’une seule version d’Azure PowerShell est installée.</span><span class="sxs-lookup"><span data-stu-id="a5867-118">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="a5867-119">Toutefois, certains scénarios peuvent nécessiter d’avoir plusieurs versions installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="a5867-119">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="a5867-120">PowerShell Gallery installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="a5867-120">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="a5867-121">Le programme d’installation WebPI installe les modules Azure dans `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="a5867-121">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="a5867-122">Si une erreur se produit pendant l’installation, vous pouvez supprimer manuellement les dossiers Azure* de votre dossier `$env:ProgramFiles\WindowsPowerShell\Modules`, puis réessayer l’installation.</span><span class="sxs-lookup"><span data-stu-id="a5867-122">If an error occurs during install, you can manually remove the Azure* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="a5867-123">Une fois l’installation terminée, votre paramètre `$env:PSModulePath` doit inclure les répertoires contenant les applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5867-123">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a5867-124">Vous pouvez exécuter la commande suivante pour vérifier qu’Azure PowerShell a bien été installé.</span><span class="sxs-lookup"><span data-stu-id="a5867-124">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="a5867-125">Un problème connu peut se produire quand vous effectuez l’installation à partir de WebPI.</span><span class="sxs-lookup"><span data-stu-id="a5867-125">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="a5867-126">Si votre ordinateur nécessite d’être redémarré après des mises à jour du système ou d’autres installations, il se peut que le chemin `$env:PSModulePath` ne soit pas mis à jour avec le chemin d’installation d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5867-126">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="a5867-127">Quand vous essayez de charger ou d’exécuter des applets de commande après l’installation, vous pouvez recevoir le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="a5867-127">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="a5867-128">Vous pouvez résoudre cette erreur en redémarrant l’ordinateur ou en important le module avec le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="a5867-128">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="a5867-129">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a5867-129">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-using-the-msi-package"></a><span data-ttu-id="a5867-130">Installation à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="a5867-130">Install using the MSI Package</span></span>

<span data-ttu-id="a5867-131">Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="a5867-131">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="a5867-132">Si vous avez installé des versions antérieures de modules Azure, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a5867-132">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="a5867-133">Le package MSI installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`, mais ne crée pas de dossiers spécifiques pour différentes versions.</span><span class="sxs-lookup"><span data-stu-id="a5867-133">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>
