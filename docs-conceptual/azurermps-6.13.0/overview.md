---
title: Vue d’ensemble d’Azure PowerShell | Microsoft Docs
description: Vue d’ensemble d’Azure PowerShell, avec des liens vers les procédures d’installation et de configuration.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: bdd8e69a2ea9df8b4fff100e1f3cc4c82d2d9d9d
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52827341"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="2256e-103">Vue d’ensemble d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2256e-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="2256e-104">Azure PowerShell fournit un ensemble d’applets de commande qui utilisent le modèle [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) pour gérer vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="2256e-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="2256e-105">Vous pouvez l’ouvrir dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou vous pouvez l’installer sur votre ordinateur local et l’utiliser dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2256e-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="2256e-106">Utilisez [Cloud Shell](/azure/cloud-shell/overview) pour exécuter Microsoft Azure PowerShell dans votre navigateur ou [l’installer](install-azurerm-ps.md) sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2256e-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="2256e-107">Lisez ensuite l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md) pour commencer à utiliser Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2256e-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="2256e-108">Pour plus d’informations sur la version la plus récente, consultez les [Notes de publication](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="2256e-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="2256e-109">Les exemples suivants peuvent vous aider à comprendre comment utiliser Azure PowerShell dans certains scénarios courants :</span><span class="sxs-lookup"><span data-stu-id="2256e-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="2256e-110">Machines virtuelles Linux</span><span class="sxs-lookup"><span data-stu-id="2256e-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="2256e-111">Machines virtuelles Windows</span><span class="sxs-lookup"><span data-stu-id="2256e-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="2256e-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="2256e-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="2256e-113">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="2256e-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

[!INCLUDE[az-replacing-azurerm](../includes/az-replacing-azurerm.md)]

## <a name="learn-powershell-basics"></a><span data-ttu-id="2256e-114">Découvrir les notions de base de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2256e-114">Learn PowerShell basics</span></span>

<span data-ttu-id="2256e-115">Si vous n’êtes pas familiarisé avec le logiciel PowerShell, une introduction à ce dernier peut s’avérer opportune.</span><span class="sxs-lookup"><span data-stu-id="2256e-115">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="2256e-116">Installation de PowerShell</span><span class="sxs-lookup"><span data-stu-id="2256e-116">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="2256e-117">Scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2256e-117">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="2256e-118">Vous pouvez également regarder la vidéo [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Notions de base de PowerShell : (Partie 1) Bien démarrer avec PowerShell).</span><span class="sxs-lookup"><span data-stu-id="2256e-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="2256e-119">Ou bien participer la [Prise en main rapide de PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) de Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="2256e-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="2256e-120">Développer vos compétences avec Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="2256e-120">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="2256e-121">Automatiser des tâches Azure à l’aide de scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="2256e-121">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="2256e-122">Plus de formations interactives...</span><span class="sxs-lookup"><span data-stu-id="2256e-122">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="2256e-123">Autres modules Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2256e-123">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="2256e-124">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2256e-124">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="2256e-125">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="2256e-125">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="2256e-126">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2256e-126">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="2256e-127">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="2256e-127">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
