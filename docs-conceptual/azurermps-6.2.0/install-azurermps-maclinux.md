---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323167"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="eae0e-103">Installer Azure PowerShell sur macOS ou Linux</span><span class="sxs-lookup"><span data-stu-id="eae0e-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="eae0e-104">Il est désormais possible d’exécuter Azure PowerShell Core sur PowerShell Core v6 pour des plateformes non-Windows.</span><span class="sxs-lookup"><span data-stu-id="eae0e-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="eae0e-105">Contrairement au produit Azure PowerShell standard intégré à .NET Framework pour Windows, ce produit est conçu pour .NET Core et peut s’exécuter sur n’importe quelle plateforme prenant en charge le runtime .net Core.</span><span class="sxs-lookup"><span data-stu-id="eae0e-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="eae0e-106">Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.</span><span class="sxs-lookup"><span data-stu-id="eae0e-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="eae0e-107">La prise en charge de ces produits est limitée.</span><span class="sxs-lookup"><span data-stu-id="eae0e-107">Support for these products is limited.</span></span> <span data-ttu-id="eae0e-108">Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="eae0e-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="eae0e-109">Problèmes pour PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="eae0e-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="eae0e-110">Problèmes pour Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="eae0e-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="eae0e-111">Installer PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="eae0e-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="eae0e-112">L’installation de PowerShell Core v6 sur Linux ou macOS varie en fonction de la distribution Linux et de la version de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eae0e-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="eae0e-113">Vous trouverez des instructions détaillées dans les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="eae0e-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="eae0e-114">Installer PowerShell Core sur macOS</span><span class="sxs-lookup"><span data-stu-id="eae0e-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="eae0e-115">Installer PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="eae0e-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="eae0e-116">Installer Azure PowerShell pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="eae0e-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="eae0e-117">PowerShell Core v6 est fourni avec le module PowerShellGet déjà installé.</span><span class="sxs-lookup"><span data-stu-id="eae0e-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="eae0e-118">Ceci facilite l’installation de n’importe quel module publié dans PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="eae0e-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="eae0e-119">Pour installer Azure PowerShell, ouvrez une nouvelle session PowerShell et exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="eae0e-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="eae0e-120">Charger le module AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="eae0e-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="eae0e-121">Une fois le module installé, vous devez le charger dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eae0e-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="eae0e-122">Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :</span><span class="sxs-lookup"><span data-stu-id="eae0e-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="eae0e-123">Une fois l’importation terminée, vous pouvez tester votre module nouvellement installé en essayant de vous connecter à Azure avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="eae0e-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="eae0e-124">La commande ci-dessus vous invite à accéder à `https://aka.ms/devicelogin` et à entrer le code fourni.</span><span class="sxs-lookup"><span data-stu-id="eae0e-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="eae0e-125">Applets de commande disponibles</span><span class="sxs-lookup"><span data-stu-id="eae0e-125">Available cmdlets</span></span>

<span data-ttu-id="eae0e-126">Les modules Azure PowerShell pour .NET Standard sont en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="eae0e-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="eae0e-127">Ces modules ne fournissent pas l’ensemble des applets de commande qui sont disponibles pour la version Windows des modules.</span><span class="sxs-lookup"><span data-stu-id="eae0e-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="eae0e-128">Les fonctions suivantes sont implémentées dans les modules AzureRM.Netcore :</span><span class="sxs-lookup"><span data-stu-id="eae0e-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="eae0e-129">Account management</span><span class="sxs-lookup"><span data-stu-id="eae0e-129">Account management</span></span>
  - <span data-ttu-id="eae0e-130">Se connecter avec un compte Microsoft, un compte d’organisation ou un principal du service via Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eae0e-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="eae0e-131">Enregistrer les informations d’identification sur disque avec Save-AzureRmContext et charger les informations d’identification enregistrées avec Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="eae0e-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="eae0e-132">Environnement</span><span class="sxs-lookup"><span data-stu-id="eae0e-132">Environment</span></span>
  - <span data-ttu-id="eae0e-133">Obtenir les différents environnements Microsoft Azure prédéfinis</span><span class="sxs-lookup"><span data-stu-id="eae0e-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="eae0e-134">Ajouter/définir/supprimer des environnements personnalisés (comme vos environnements Azure Stack ou Windows Azure Pack)</span><span class="sxs-lookup"><span data-stu-id="eae0e-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="eae0e-135">Applets de commande de plan de gestion pour les services Azure avec les interfaces Resource Manager et Gestion des services.</span><span class="sxs-lookup"><span data-stu-id="eae0e-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="eae0e-136">Machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="eae0e-136">Virtual Machine</span></span>
  - <span data-ttu-id="eae0e-137">App Service (sites web)</span><span class="sxs-lookup"><span data-stu-id="eae0e-137">App Service (Websites)</span></span>
  - <span data-ttu-id="eae0e-138">Base de données SQL</span><span class="sxs-lookup"><span data-stu-id="eae0e-138">SQL Database</span></span>
  - <span data-ttu-id="eae0e-139">Stockage</span><span class="sxs-lookup"><span data-stu-id="eae0e-139">Storage</span></span>
  - <span data-ttu-id="eae0e-140">Réseau</span><span class="sxs-lookup"><span data-stu-id="eae0e-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="eae0e-141">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eae0e-141">Next Steps</span></span>

<span data-ttu-id="eae0e-142">Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="eae0e-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
