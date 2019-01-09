---
title: Vue d’ensemble d’Azure PowerShell
description: Vue d’ensemble du module Az Azure PowerShell, avec des informations sur l’installation et la prise en main.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736458"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="668fd-103">Vue d’ensemble d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="668fd-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="668fd-104">Azure PowerShell fournit un ensemble d’applets de commande qui utilisent le modèle [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) pour gérer vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="668fd-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="668fd-105">Azure PowerShell utilise .NET Standard, permettant ainsi une disponibilité pour Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="668fd-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="668fd-106">Azure PowerShell est également disponible à partir d’Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="668fd-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="668fd-107">Utilisez [Azure Cloud Shell](/azure/cloud-shell/overview) pour exécuter Azure PowerShell dans votre navigateur ou [l’installer en local](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="668fd-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="668fd-108">Consultez l’article de [prise en main](get-started-azureps.md) pour découvrir les bases d’Azure PowerShell et la prise en main d’Azure.</span><span class="sxs-lookup"><span data-stu-id="668fd-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="668fd-109">Pour plus d’informations sur la dernière version d’Azure PowerShell, consultez les [notes de publication](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="668fd-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="668fd-110">À propos du nouveau module Az</span><span class="sxs-lookup"><span data-stu-id="668fd-110">About the new Az module</span></span>

<span data-ttu-id="668fd-111">Cette documentation décrit le nouveau module Az pour Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668fd-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="668fd-112">Ce nouveau module est entièrement écrit dans .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="668fd-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="668fd-113">L’utilisation de .NET Standard permet une exécution d’Azure PowerShell sous PowerShell 5.x sur Windows ou PowerShell 6 sur n’importe quelle plateforme.</span><span class="sxs-lookup"><span data-stu-id="668fd-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="668fd-114">Le module Az est maintenant le moyen d’interaction avec Azure via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="668fd-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="668fd-115">AzureRM continuera de bénéficier de correctifs de bogues, mais ne recevra plus de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="668fd-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="668fd-116">Obtenez plus d’informations sur le nouveau module, y compris la façon dont les commandes ont été renommées et les plans de maintenance pour AzureRM, dans la [présentation du module Az Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="668fd-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="668fd-117">Si vous souhaitez commencer à utiliser le nouveau module tout de suite, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="668fd-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="668fd-118">Une [documentation AzureRM](/powershell/azure/azurerm) est également disponible.</span><span class="sxs-lookup"><span data-stu-id="668fd-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="668fd-119">Bien que la documentation Azure ait été mise à jour pour refléter les nouveaux noms de cmdlet de module, les articles peuvent toujours utiliser les commandes AzureRM.</span><span class="sxs-lookup"><span data-stu-id="668fd-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="668fd-120">Après avoir installé le module Az, il est recommandé d’activer les alias de cmdlet AzureRM avec `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="668fd-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="668fd-121">Consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="668fd-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="668fd-122">Scénarios courants</span><span class="sxs-lookup"><span data-stu-id="668fd-122">Common scenarios</span></span>

<span data-ttu-id="668fd-123">Les exemples suivants peuvent vous aider à comprendre comment utiliser Azure PowerShell dans certains scénarios courants :</span><span class="sxs-lookup"><span data-stu-id="668fd-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="668fd-124">Machines virtuelles Linux</span><span class="sxs-lookup"><span data-stu-id="668fd-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="668fd-125">Machines virtuelles Windows</span><span class="sxs-lookup"><span data-stu-id="668fd-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="668fd-126">Web Apps</span><span class="sxs-lookup"><span data-stu-id="668fd-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="668fd-127">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="668fd-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="668fd-128">Découvrir les notions de base de PowerShell</span><span class="sxs-lookup"><span data-stu-id="668fd-128">Learn PowerShell basics</span></span>

<span data-ttu-id="668fd-129">Si vous n’êtes pas familiarisé avec PowerShell, une introduction à ce logiciel peut s’avérer opportune.</span><span class="sxs-lookup"><span data-stu-id="668fd-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="668fd-130">Installation de PowerShell</span><span class="sxs-lookup"><span data-stu-id="668fd-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="668fd-131">Scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="668fd-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="668fd-132">Vous pouvez également regarder cette vidéo : [Notions de base de PowerShell : (Première partie) Prise en main de PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="668fd-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="668fd-133">Ou bien participer la [Prise en main rapide de PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) de Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="668fd-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="668fd-134">Développer vos compétences avec Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="668fd-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="668fd-135">Automatiser des tâches Azure à l’aide de scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="668fd-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="668fd-136">Plus de formations interactives...</span><span class="sxs-lookup"><span data-stu-id="668fd-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="668fd-137">Autres modules Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="668fd-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="668fd-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="668fd-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="668fd-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="668fd-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="668fd-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="668fd-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="668fd-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="668fd-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
