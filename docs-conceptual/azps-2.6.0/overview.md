---
title: Vue d’ensemble d’Azure PowerShell
description: Vue d’ensemble du module Az Azure PowerShell, avec des informations sur l’installation et la prise en main.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052615"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="9d308-103">Vue d’ensemble d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d308-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="9d308-104">Azure PowerShell fournit un ensemble d’applets de commande qui utilisent le modèle [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) pour gérer vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="9d308-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="9d308-105">Azure PowerShell utilise .NET Standard, permettant ainsi une disponibilité pour Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="9d308-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="9d308-106">Azure PowerShell est également disponible sur Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9d308-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="9d308-107">À propos du nouveau module Az</span><span class="sxs-lookup"><span data-stu-id="9d308-107">About the new Az module</span></span>

<span data-ttu-id="9d308-108">Cette documentation décrit le nouveau module Az pour Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d308-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="9d308-109">Ce nouveau module est entièrement écrit dans .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="9d308-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="9d308-110">L’utilisation de .NET Standard permet à Azure PowerShell de s’exécuter sous PowerShell 5.1 sur Windows, ou sous PowerShell Core 6.x et ultérieur, sur n’importe quelle plateforme.</span><span class="sxs-lookup"><span data-stu-id="9d308-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="9d308-111">Le module Az est maintenant le moyen d’interaction avec Azure via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d308-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="9d308-112">AzureRM continuera de bénéficier de correctifs de bogues, mais ne recevra plus de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9d308-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="9d308-113">Obtenez plus d’informations sur le nouveau module, y compris la façon dont les commandes ont été renommées et les plans de maintenance pour AzureRM, dans la [présentation du module Az Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="9d308-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="9d308-114">Si vous souhaitez commencer à utiliser le nouveau module tout de suite, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9d308-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="9d308-115">Une [documentation AzureRM](/powershell/azure/azurerm) est également disponible.</span><span class="sxs-lookup"><span data-stu-id="9d308-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9d308-116">Bien que la documentation Azure ait été mise à jour pour refléter les nouveaux noms de cmdlet de module, les articles peuvent toujours utiliser les commandes AzureRM.</span><span class="sxs-lookup"><span data-stu-id="9d308-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="9d308-117">Après avoir installé le module Az, il est recommandé d’activer les alias de cmdlet AzureRM avec `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="9d308-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="9d308-118">Consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9d308-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="9d308-119">Exécuter ou installer</span><span class="sxs-lookup"><span data-stu-id="9d308-119">Run or install</span></span>

<span data-ttu-id="9d308-120">Vous pouvez installer Azure PowerShell sur PowerShell 5.1 ou ultérieur sur Windows, ou sur PowerShell Core 6.x et ultérieur sur n’importe quelle plateforme. Vous pouvez également l’exécuter dans Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9d308-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="9d308-121">Pour l’exécuter dans votre navigateur avec Azure Cloud Shell, consultez le [guide de démarrage rapide de PowerShell dans Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="9d308-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="9d308-122">Pour installer Azure PowerShell sur votre système, consultez [Installer Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="9d308-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="9d308-123">Pour plus d’informations sur la dernière version d’Azure PowerShell, consultez les [notes de publication](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9d308-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="9d308-124">Prise en main</span><span class="sxs-lookup"><span data-stu-id="9d308-124">Get Started</span></span>

<span data-ttu-id="9d308-125">Consultez l’article de [Prise en main d’Azure PowerShell](get-started-azureps.md) pour découvrir les bases d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d308-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="9d308-126">Si vous n’êtes pas familiarisé avec PowerShell, une introduction à ce logiciel peut s’avérer opportune :</span><span class="sxs-lookup"><span data-stu-id="9d308-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="9d308-127">Installer PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d308-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="9d308-128">Scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d308-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="9d308-129">Notions de base de PowerShell : (Première partie) Prise en main de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d308-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

<span data-ttu-id="9d308-130">Les exemples suivants peuvent vous aider pour certaines utilisations courantes d’Azure :</span><span class="sxs-lookup"><span data-stu-id="9d308-130">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="9d308-131">Machines virtuelles Linux</span><span class="sxs-lookup"><span data-stu-id="9d308-131">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9d308-132">Machines virtuelles Windows</span><span class="sxs-lookup"><span data-stu-id="9d308-132">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9d308-133">Web Apps</span><span class="sxs-lookup"><span data-stu-id="9d308-133">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9d308-134">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="9d308-134">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="9d308-135">Développer vos compétences avec Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="9d308-135">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="9d308-136">Automatiser des tâches Azure à l’aide de scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d308-136">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="9d308-137">Plus de formations interactives...</span><span class="sxs-lookup"><span data-stu-id="9d308-137">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="9d308-138">Autres modules Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9d308-138">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="9d308-139">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9d308-139">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="9d308-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9d308-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="9d308-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="9d308-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
