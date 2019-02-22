---
title: Autres méthodes d’installation d’Azure PowerShell
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet à l’aide d’un fichier MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 0976fd51b26010702d200cee445d93269405416c
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153367"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="55abc-103">Installer Azure PowerShell sur Windows avec un fichier MSI</span><span class="sxs-lookup"><span data-stu-id="55abc-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="55abc-104">Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un programme d’installation de MSI.</span><span class="sxs-lookup"><span data-stu-id="55abc-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="55abc-105">Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système.</span><span class="sxs-lookup"><span data-stu-id="55abc-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="55abc-106">Il est recommandé d’installer Azure PowerShell sur Windows avec PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="55abc-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="55abc-107">Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="55abc-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="55abc-108">La méthode d’installation avec Web Platform Installer n’est plus disponible pour les versions d’Azure PowerShell 6.x et plus récentes.</span><span class="sxs-lookup"><span data-stu-id="55abc-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="55abc-109">Si vous devez utiliser Web Platform Installer, préférez l’utilisation d’un fichier MSI ou l’installation d’une version plus ancienne d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="55abc-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="55abc-110">Pour une installation sur des environnements Linux ou macOS, consultez [Installer Azure PowerShell sur macOS ou Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="55abc-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="55abc-111">Installer ou mettre à jour sur Windows à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="55abc-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="55abc-112">Azure PowerShell pour Windows PowerShell 5.x peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span><span class="sxs-lookup"><span data-stu-id="55abc-112">Azure PowerShell for Windows PowerShell 5.x can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span> <span data-ttu-id="55abc-113">Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="55abc-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="55abc-114">Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="55abc-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="55abc-115">Les modules `AzureRM` et `Azure` sont installés.</span><span class="sxs-lookup"><span data-stu-id="55abc-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="55abc-116">N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.</span><span class="sxs-lookup"><span data-stu-id="55abc-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="55abc-117">Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="55abc-117">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="55abc-118">Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="55abc-118">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="55abc-119">En raison de la structure du module, cette opération peut prendre quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="55abc-119">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="55abc-120">Vous devez répéter cette étape pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="55abc-120">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="55abc-121">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="55abc-121">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
