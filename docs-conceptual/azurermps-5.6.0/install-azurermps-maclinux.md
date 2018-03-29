---
title: Installer et configurer Azure PowerShell sur macOS et Linux │ Microsoft Docs
description: Comment installer et configurer Azure PowerShell pour la première utilisation sur macOS et Linux.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 15bf69bf95eceb936b3a429e741add95c308826a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="6a3cd-103">Installer et configurer Azure PowerShell sur macOS et Linux</span><span class="sxs-lookup"><span data-stu-id="6a3cd-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="6a3cd-104">Il est désormais possible d’installer PowerShell Core v6 et Azure PowerShell sur des plateformes non Windows.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="6a3cd-105">Le processus d’installation d’Azure PowerShell sur macOS et Linux est presque le même que sur Windows, sauf que vous devez d’abord installer PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="6a3cd-106">Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="6a3cd-107">La prise en charge de ces produits est limitée.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-107">Support for these products is limited.</span></span> <span data-ttu-id="6a3cd-108">Si vous rencontrez des problèmes ou que vous découvrez des bogues, vous pouvez nous les signaler dans GitHub.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="6a3cd-109">Problèmes pour PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="6a3cd-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="6a3cd-110">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a3cd-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="6a3cd-111">Étape 1 : Installer PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="6a3cd-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="6a3cd-112">Le processus d’installation de PowerShell Core v6 varie selon le système d’exploitation cible.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="6a3cd-113">S’il est possible d’installer PowerShell Core v6 sur Windows, cet article est néanmoins centré sur macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="6a3cd-114">Si vous voulez utiliser Azure PowerShell sur Windows, consultez l’article sur [l’installation](./install-azurerm-ps.md) pour Windows.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="6a3cd-115">L’installation de **PowerShell Core v6** sur Linux ou macOS varie en fonction de la distribution Linux et de la version de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="6a3cd-116">Vous trouverez des instructions détaillées dans l’article suivant :</span><span class="sxs-lookup"><span data-stu-id="6a3cd-116">Detailed instructions can be found in the following article:</span></span>

- <span data-ttu-id="6a3cd-117">[Installing PowerShell Core on macOS and Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux) (Installation de PowerShell Core sur macOS et Linux</span><span class="sxs-lookup"><span data-stu-id="6a3cd-117">[Installing PowerShell Core on macOS and Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)</span></span>

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="6a3cd-118">Étape 2 : Installer Azure PowerShell pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="6a3cd-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="6a3cd-119">PowerShell Core v6 est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="6a3cd-120">Ceci facilite l’installation de n’importe quel module publié dans PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="6a3cd-121">Pour installer Azure PowerShell, ouvrez une nouvelle session PowerShell et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6a3cd-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="6a3cd-122">Étape 3 : Charger le module AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="6a3cd-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="6a3cd-123">Une fois le module installé, vous devez le charger dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="6a3cd-124">Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="6a3cd-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="6a3cd-125">Une fois l’importation terminée, vous pouvez tester votre module nouvellement installé en essayant de vous connecter à Azure avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6a3cd-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="6a3cd-126">La commande ci-dessus vous invite à accéder à `https://aka.ms/devicelogin` et à entrer le code fourni.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="6a3cd-127">Applets de commande disponibles</span><span class="sxs-lookup"><span data-stu-id="6a3cd-127">Available cmdlets</span></span>

<span data-ttu-id="6a3cd-128">Les modules Azure PowerShell pour .NET Standard sont en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="6a3cd-129">Ces modules ne fournissent pas l’ensemble des applets de commande qui sont disponibles pour la version Windows des modules.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="6a3cd-130">Les fonctions suivantes sont implémentées dans les modules AzureRM.Netcore :</span><span class="sxs-lookup"><span data-stu-id="6a3cd-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="6a3cd-131">Account management</span><span class="sxs-lookup"><span data-stu-id="6a3cd-131">Account management</span></span>
  - <span data-ttu-id="6a3cd-132">Se connecter avec un compte Microsoft, un compte d’organisation ou un principal du service via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="6a3cd-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="6a3cd-133">Enregistrer les informations d’identification sur disque avec Save-AzureRmContext et charger les informations d’identification enregistrées avec Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6a3cd-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="6a3cd-134">Environnement</span><span class="sxs-lookup"><span data-stu-id="6a3cd-134">Environment</span></span>
  - <span data-ttu-id="6a3cd-135">Obtenir les différents environnements Microsoft Azure prédéfinis</span><span class="sxs-lookup"><span data-stu-id="6a3cd-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="6a3cd-136">Ajouter/définir/supprimer des environnements personnalisés (comme vos environnements Azure Stack ou Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="6a3cd-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="6a3cd-137">Applets de commande de plan de gestion pour les services Azure avec les interfaces Resource Manager et Gestion des services.</span><span class="sxs-lookup"><span data-stu-id="6a3cd-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="6a3cd-138">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="6a3cd-138">Virtual Machine</span></span>
  - <span data-ttu-id="6a3cd-139">App Service (sites web)</span><span class="sxs-lookup"><span data-stu-id="6a3cd-139">App Service (Websites)</span></span>
  - <span data-ttu-id="6a3cd-140">Base de données SQL</span><span class="sxs-lookup"><span data-stu-id="6a3cd-140">SQL Database</span></span>
  - <span data-ttu-id="6a3cd-141">Stockage</span><span class="sxs-lookup"><span data-stu-id="6a3cd-141">Storage</span></span>
  - <span data-ttu-id="6a3cd-142">Réseau</span><span class="sxs-lookup"><span data-stu-id="6a3cd-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="6a3cd-143">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="6a3cd-143">Next Steps</span></span>

<span data-ttu-id="6a3cd-144">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="6a3cd-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
