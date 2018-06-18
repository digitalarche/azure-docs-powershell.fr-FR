---
title: Autres méthodes d’installation d’Azure PowerShell
description: Comment installer Azure PowerShell à l’aide du package MSI ou de Web Platform Installer.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323269"
---
# <a name="other-installation-methods"></a><span data-ttu-id="de356-103">Autres méthodes d’installation</span><span class="sxs-lookup"><span data-stu-id="de356-103">Other installation methods</span></span>

<span data-ttu-id="de356-104">Cet article explique comment installer Azure PowerShell à l’aide d’un fichier MSI ou d’un Web Platform Installer (WebPI).</span><span class="sxs-lookup"><span data-stu-id="de356-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="de356-105">Vous pouvez également exécuter Azure PowerShell depuis un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="de356-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="de356-106">Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système.</span><span class="sxs-lookup"><span data-stu-id="de356-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="de356-107">L’installation canonique d’Azure PowerShell s’effectue via PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="de356-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="de356-108">Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="de356-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="de356-109">Pour une installation sur des environnements Linux ou macOS, consultez [Installer Azure PowerShell sur macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="de356-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="de356-110">Installer ou mettre à jour sur Windows à l’aide de Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="de356-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="de356-111">L’installation de la dernière version d’Azure PowerShell à l’aide de WebPI s’effectue de la même façon que pour les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="de356-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="de356-112">Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation.</span><span class="sxs-lookup"><span data-stu-id="de356-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="de356-113">Si vous aviez précédemment installé les modules Azure à partir de PowerShell Gallery, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="de356-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="de356-114">Cette méthode simplifie votre environnement, car elle garantit qu’une seule version d’Azure PowerShell est installée.</span><span class="sxs-lookup"><span data-stu-id="de356-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="de356-115">Toutefois, certains scénarios peuvent nécessiter d’avoir plusieurs versions installées en même temps.</span><span class="sxs-lookup"><span data-stu-id="de356-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="de356-116">PowerShell Gallery installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="de356-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="de356-117">Le programme d’installation WebPI installe les modules Azure dans `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="de356-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="de356-118">Si une erreur se produit pendant l’installation, vous pouvez supprimer manuellement les dossiers `Azure*` de votre dossier `$env:ProgramFiles\WindowsPowerShell\Modules`, puis réessayer l’installation.</span><span class="sxs-lookup"><span data-stu-id="de356-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="de356-119">Une fois l’installation terminée, votre paramètre `$env:PSModulePath` doit inclure les répertoires contenant les applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de356-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="de356-120">Vous pouvez exécuter la commande suivante pour vérifier qu’Azure PowerShell a bien été installé :</span><span class="sxs-lookup"><span data-stu-id="de356-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="de356-121">Un problème connu peut se produire quand vous effectuez l’installation à partir de WebPI.</span><span class="sxs-lookup"><span data-stu-id="de356-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="de356-122">Si votre ordinateur nécessite d’être redémarré après des mises à jour du système ou d’autres installations, il se peut que le chemin `$env:PSModulePath` ne soit pas mis à jour avec le chemin d’installation d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de356-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="de356-123">Quand vous essayez de charger ou d’exécuter des applets de commande après l’installation, vous pouvez recevoir le message d’erreur suivant :</span><span class="sxs-lookup"><span data-stu-id="de356-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

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

<span data-ttu-id="de356-124">Vous pouvez résoudre cette erreur en redémarrant l’ordinateur ou en important le module avec le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="de356-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="de356-125">Installer ou mettre à jour sur Windows à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="de356-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="de356-126">Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="de356-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="de356-127">Si vous avez installé des versions antérieures de modules Azure, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="de356-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="de356-128">Le package MSI installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`, mais ne crée pas de dossiers spécifiques pour différentes versions.</span><span class="sxs-lookup"><span data-stu-id="de356-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="de356-129">Exécution dans un conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="de356-129">Run in a Docker container</span></span>

<span data-ttu-id="de356-130">Nous tenons à jour un ensemble d’images Docker préconfigurées avec Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="de356-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="de356-131">Il existe deux types de conteneurs disponibles : ceux exécutant PowerShell de manière classique sur Windows et un conteneur exécutant PowerShell Core sur Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="de356-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="de356-132">Environnement</span><span class="sxs-lookup"><span data-stu-id="de356-132">Environment</span></span> | <span data-ttu-id="de356-133">Image Docker</span><span class="sxs-lookup"><span data-stu-id="de356-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="de356-134">PowerShell sur Windows</span><span class="sxs-lookup"><span data-stu-id="de356-134">PowerShell on Windows</span></span> | [<span data-ttu-id="de356-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="de356-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="de356-136">PowerShell Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="de356-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="de356-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="de356-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="de356-138">PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="de356-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="de356-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="de356-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="de356-140">Pour exécuter une de ces conteneurs, vous utilisez `docker run -it $ImageName` pour obtenir un terminal interactif.</span><span class="sxs-lookup"><span data-stu-id="de356-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="de356-141">Par exemple, pour exécuter PowerShell Core sur le conteneur Linux, utilisez :</span><span class="sxs-lookup"><span data-stu-id="de356-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="de356-142">Pour exécuter un conteneur Windows dans Docker, votre système d’exploitation hôte doit être Windows et Docker doit être défini de manière à exécuter des conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="de356-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="de356-143">Pour en savoir plus sur le basculement entre des environnements Windows et Linux dans Docker, consultez la documentation Docker [Basculer entre les conteneurs Windows et Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="de356-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>