---
title: Installer et configurer Azure PowerShell sur macOS et Linux │ Microsoft Docs
description: Comment installer et configurer Azure PowerShell pour la première utilisation sur macOS et Linux.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: e2d73f78563b550403e9fd8b66beeef431a384b6
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461767"
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="9e781-103">Installer et configurer Azure PowerShell sur macOS et Linux</span><span class="sxs-lookup"><span data-stu-id="9e781-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="9e781-104">Il est désormais possible d’installer PowerShell Core v6 et Azure PowerShell sur des plateformes non Windows.</span><span class="sxs-lookup"><span data-stu-id="9e781-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="9e781-105">Le processus d’installation d’Azure PowerShell sur macOS et Linux est presque le même que sur Windows, sauf que vous devez d’abord installer PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="9e781-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="9e781-106">Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="9e781-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="9e781-107">La prise en charge de ces produits est limitée.</span><span class="sxs-lookup"><span data-stu-id="9e781-107">Support for these products is limited.</span></span> <span data-ttu-id="9e781-108">Si vous rencontrez des problèmes ou que vous découvrez des bogues, vous pouvez nous les signaler dans GitHub.</span><span class="sxs-lookup"><span data-stu-id="9e781-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="9e781-109">Problèmes pour PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="9e781-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="9e781-110">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e781-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="9e781-111">Étape 1 : Installer PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="9e781-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="9e781-112">Le processus d’installation de PowerShell Core v6 varie selon le système d’exploitation cible.</span><span class="sxs-lookup"><span data-stu-id="9e781-112">The process of installing PowerShell Core v6 varies depending on the target operating system.</span></span>
<span data-ttu-id="9e781-113">S’il est possible d’installer PowerShell Core v6 sur Windows, cet article est néanmoins centré sur macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="9e781-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="9e781-114">Si vous voulez utiliser Azure PowerShell sur Windows, consultez l’article sur [l’installation](./install-azurerm-ps.md) pour Windows.</span><span class="sxs-lookup"><span data-stu-id="9e781-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="9e781-115">L’installation de **PowerShell Core v6** sur Linux ou macOS varie en fonction de la distribution Linux et de la version de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9e781-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="9e781-116">Vous trouverez des instructions détaillées dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="9e781-116">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="9e781-117">Installation de PowerShell Core sous macOS</span><span class="sxs-lookup"><span data-stu-id="9e781-117">Installing PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="9e781-118">Installation de PowerShell Core sous Linux</span><span class="sxs-lookup"><span data-stu-id="9e781-118">Installing PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="9e781-119">Étape 2 : Installer Azure PowerShell pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="9e781-119">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="9e781-120">PowerShell Core v6 est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="9e781-120">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9e781-121">Ceci facilite l’installation de n’importe quel module publié dans PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="9e781-121">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="9e781-122">Pour installer Azure PowerShell, ouvrez une nouvelle session PowerShell et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9e781-122">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="9e781-123">Étape 3 : Charger le module AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="9e781-123">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="9e781-124">Une fois le module installé, vous devez le charger dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9e781-124">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9e781-125">Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="9e781-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="9e781-126">Une fois l’importation terminée, vous pouvez tester votre module nouvellement installé en essayant de vous connecter à Azure avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9e781-126">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="9e781-127">La commande ci-dessus vous invite à accéder à `https://aka.ms/devicelogin` et à entrer le code fourni.</span><span class="sxs-lookup"><span data-stu-id="9e781-127">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="9e781-128">Applets de commande disponibles</span><span class="sxs-lookup"><span data-stu-id="9e781-128">Available cmdlets</span></span>

<span data-ttu-id="9e781-129">Les modules Azure PowerShell pour .NET Standard sont en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="9e781-129">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="9e781-130">Ces modules ne fournissent pas l’ensemble des applets de commande qui sont disponibles pour la version Windows des modules.</span><span class="sxs-lookup"><span data-stu-id="9e781-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="9e781-131">Les fonctions suivantes sont implémentées dans les modules AzureRM.Netcore :</span><span class="sxs-lookup"><span data-stu-id="9e781-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="9e781-132">Account management</span><span class="sxs-lookup"><span data-stu-id="9e781-132">Account management</span></span>
  - <span data-ttu-id="9e781-133">Se connecter avec un compte Microsoft, un compte d’organisation ou un principal du service via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9e781-133">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="9e781-134">Enregistrer les informations d’identification sur disque avec Save-AzureRmContext et charger les informations d’identification enregistrées avec Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9e781-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="9e781-135">Environnement</span><span class="sxs-lookup"><span data-stu-id="9e781-135">Environment</span></span>
  - <span data-ttu-id="9e781-136">Obtenir les différents environnements Microsoft Azure prédéfinis</span><span class="sxs-lookup"><span data-stu-id="9e781-136">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="9e781-137">Ajouter/définir/supprimer des environnements personnalisés (comme vos environnements Azure Stack ou Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="9e781-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="9e781-138">Applets de commande de plan de gestion pour les services Azure avec les interfaces Resource Manager et Gestion des services.</span><span class="sxs-lookup"><span data-stu-id="9e781-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="9e781-139">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="9e781-139">Virtual Machine</span></span>
  - <span data-ttu-id="9e781-140">App Service (sites web)</span><span class="sxs-lookup"><span data-stu-id="9e781-140">App Service (Websites)</span></span>
  - <span data-ttu-id="9e781-141">Base de données SQL</span><span class="sxs-lookup"><span data-stu-id="9e781-141">SQL Database</span></span>
  - <span data-ttu-id="9e781-142">Stockage</span><span class="sxs-lookup"><span data-stu-id="9e781-142">Storage</span></span>
  - <span data-ttu-id="9e781-143">Réseau</span><span class="sxs-lookup"><span data-stu-id="9e781-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="9e781-144">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9e781-144">Next Steps</span></span>

<span data-ttu-id="9e781-145">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9e781-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
