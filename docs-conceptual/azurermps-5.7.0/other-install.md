---
title: Autres méthodes d’installation d’Azure PowerShell
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 2fcd2307667d1f810fbcb3fe4d14e3b0def537ed
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737490"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="2c1e5-103">Installer Azure PowerShell sur Windows avec un fichier MSI ou Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="2c1e5-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="2c1e5-104">Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un fichier MSI ou de Web Platform Installer (WebPI).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="2c1e5-105">Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="2c1e5-106">Il est recommandé d’installer Azure PowerShell sur Windows avec PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="2c1e5-107">Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="2c1e5-108">Pour une installation sur des environnements Linux ou macOS, consultez [Installer Azure PowerShell sur macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="2c1e5-109">Installer ou mettre à jour sur Windows à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="2c1e5-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="2c1e5-110">Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="2c1e5-111">Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="2c1e5-112">Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="2c1e5-113">Les modules `AzureRM` et `Azure` sont installés.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="2c1e5-114">N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="2c1e5-115">Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="2c1e5-116">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="2c1e5-117">L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="2c1e5-118">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="2c1e5-119">Installer ou mettre à jour sur Windows à l’aide de Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="2c1e5-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="2c1e5-120">Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="2c1e5-121">Si vous avez installé des versions antérieures de modules Azure à partir d’un fichier MSI ou avec WebPi, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="2c1e5-122">Les modules sont installés dans `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="2c1e5-123">Les modules `AzureRM` et `Azure` sont installés.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="2c1e5-124">N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="2c1e5-125">Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="2c1e5-126">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="2c1e5-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="2c1e5-127">L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="2c1e5-128">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).</span><span class="sxs-lookup"><span data-stu-id="2c1e5-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
