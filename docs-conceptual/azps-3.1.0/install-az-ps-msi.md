---
title: Installer Azure PowerShell avec un fichier MSI
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet à l’aide d’un fichier MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: d16aea3fa2059cd32f584134e2da43e01e3def31
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537248"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="5fe64-103">Installer Azure PowerShell sur Windows avec un fichier MSI</span><span class="sxs-lookup"><span data-stu-id="5fe64-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="5fe64-104">Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un programme d’installation de MSI.</span><span class="sxs-lookup"><span data-stu-id="5fe64-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="5fe64-105">Le programme d’installation MSI est fourni pour les environnements dans lesquels PowerShell Gallery risque d’être bloqué par un pare-feu ou quand un programme d’installation hors connexion est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5fe64-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="5fe64-106">Il est recommandé d’installer Azure PowerShell avec PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="5fe64-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="5fe64-107">Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5fe64-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe64-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fe64-108">Requirements</span></span>

<span data-ttu-id="5fe64-109">Le programme d’installation MSI pour Azure PowerShell fonctionne __uniquement__ pour PowerShell 5.1 sur Windows.</span><span class="sxs-lookup"><span data-stu-id="5fe64-109">The MSI installer for Azure PowerShell works __only__ for PowerShell 5.1 on Windows.</span></span> <span data-ttu-id="5fe64-110">Pour une installation sur des plateformes non Windows ou des versions ultérieures de PowerShell, effectuez l’[installation avec PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5fe64-110">For installation on non-Windows platforms or later versions of powershell, [Install with PowerShellGet](install-az-ps.md).</span></span>
<span data-ttu-id="5fe64-111">Pour vérifier votre version de PowerShell, exécutez la commande :</span><span class="sxs-lookup"><span data-stu-id="5fe64-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="5fe64-112">Pour utiliser Azure PowerShell dans PowerShell 5.1, vous devez :</span><span class="sxs-lookup"><span data-stu-id="5fe64-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="5fe64-113">Mettrez à jour vers [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5fe64-113">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="5fe64-114">Si vous êtes sur Windows 10, PowerShell 5.1 est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="5fe64-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="5fe64-115">Installez [.NET Framework 4.7.2 ou ultérieur](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="5fe64-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="5fe64-116">Installer ou mettre à jour sur Windows à l’aide du package MSI</span><span class="sxs-lookup"><span data-stu-id="5fe64-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="5fe64-117">Azure PowerShell pour Windows est installé avec le fichier MSI disponible à partir de [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019).</span><span class="sxs-lookup"><span data-stu-id="5fe64-117">Azure PowerShell for Windows is installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v2.8.0-October2019).</span></span> <span data-ttu-id="5fe64-118">Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5fe64-118">If you have installed earlier versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="5fe64-119">Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="5fe64-119">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="5fe64-120">Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe64-120">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="5fe64-121">Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="5fe64-121">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="5fe64-122">En raison de la structure du module, cette opération peut prendre jusqu’à une minute.</span><span class="sxs-lookup"><span data-stu-id="5fe64-122">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="5fe64-123">Vous devez répéter cette étape pour chaque nouvelle session PowerShell que vous démarrez.</span><span class="sxs-lookup"><span data-stu-id="5fe64-123">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="5fe64-124">Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5fe64-124">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="5fe64-125">Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="5fe64-125">Provide feedback</span></span>

<span data-ttu-id="5fe64-126">Si vous rencontrez un bogue dans Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="5fe64-126">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="5fe64-127">Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="5fe64-127">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5fe64-128">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5fe64-128">Next Steps</span></span>

<span data-ttu-id="5fe64-129">Pour en savoir plus sur les modules PowerShell et leurs fonctionnalités, consultez l’article sur la [prise en main d’Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5fe64-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="5fe64-130">Si vous êtes familiarisé avec Azure PowerShell et devez effectuer une migration depuis AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="5fe64-130">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
