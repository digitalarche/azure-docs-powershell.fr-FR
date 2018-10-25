---
title: Autres méthodes d’installation d’Azure PowerShell
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet à l’aide d’un fichier MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 52bcbe3f91600c96546c7d8ff5648977a7917ff9
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001709"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="d1e7e-103">Installer Azure PowerShell sur Windows avec un fichier MSI</span><span class="sxs-lookup"><span data-stu-id="d1e7e-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="d1e7e-104">Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un programme d’installation de MSI.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="d1e7e-105">Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="d1e7e-106">Il est recommandé d’installer Azure PowerShell sur Windows avec PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="d1e7e-107">Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="d1e7e-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d1e7e-108">La méthode d’installation avec Web Platform Installer n’est plus disponible pour les versions d’Azure PowerShell 6.x et plus récentes.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="d1e7e-109">Si vous devez utiliser Web Platform Installer, préférez l’utilisation d’un fichier MSI ou l’installation d’une version plus ancienne d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="d1e7e-110">Pour une installation sur des environnements Linux ou macOS, consultez [Installer Azure PowerShell sur macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="d1e7e-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="d1e7e-111">Installer ou mettre à jour sur Windows à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="d1e7e-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="d1e7e-112">Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="d1e7e-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="d1e7e-113">Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="d1e7e-114">Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="d1e7e-115">Les modules `AzureRM` et `Azure` sont installés.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="d1e7e-116">N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="d1e7e-117">Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-117">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="d1e7e-118">Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-118">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="d1e7e-119">L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="d1e7e-119">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="d1e7e-120">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, voir [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="d1e7e-120">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
