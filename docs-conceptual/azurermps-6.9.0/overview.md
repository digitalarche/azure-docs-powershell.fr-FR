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
ms.openlocfilehash: f03243f6f560407b63aff154494cf164d670d810
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178661"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="624ba-103">Vue d’ensemble d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="624ba-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="624ba-104">Azure PowerShell fournit un ensemble d’applets de commande qui utilisent le modèle [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) pour gérer vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="624ba-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="624ba-105">Vous pouvez l’ouvrir dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou vous pouvez l’installer sur votre ordinateur local et l’utiliser dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="624ba-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="624ba-106">Utilisez [Cloud Shell](/azure/cloud-shell/overview) pour exécuter Microsoft Azure PowerShell dans votre navigateur ou [l’installer](install-azurerm-ps.md) sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="624ba-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="624ba-107">Lisez ensuite l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md) pour commencer à utiliser Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="624ba-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="624ba-108">Pour plus d’informations sur la version la plus récente, consultez les [notes de publication](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="624ba-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="624ba-109">Les exemples suivants peuvent vous aider à comprendre comment utiliser Azure PowerShell dans certains scénarios courants :</span><span class="sxs-lookup"><span data-stu-id="624ba-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="624ba-110">Machines virtuelles Linux</span><span class="sxs-lookup"><span data-stu-id="624ba-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="624ba-111">Machines virtuelles Windows</span><span class="sxs-lookup"><span data-stu-id="624ba-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="624ba-112">Web Apps</span><span class="sxs-lookup"><span data-stu-id="624ba-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="624ba-113">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="624ba-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="624ba-114">Si vous avez des déploiements qui utilisent le modèle de déploiement Classic non convertible, vous pouvez installer la version Service Management d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="624ba-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="624ba-115">Pour plus d’informations, consultez [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="624ba-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="624ba-116">Découvrir les notions de base de PowerShell</span><span class="sxs-lookup"><span data-stu-id="624ba-116">Learn PowerShell basics</span></span>

<span data-ttu-id="624ba-117">Si vous n’êtes pas familiarisé avec le logiciel PowerShell, une introduction à ce dernier peut s’avérer opportune.</span><span class="sxs-lookup"><span data-stu-id="624ba-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="624ba-118">Installation de PowerShell</span><span class="sxs-lookup"><span data-stu-id="624ba-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="624ba-119">Scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="624ba-119">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="624ba-120">Vous pouvez également regarder la vidéo [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Notions de base de PowerShell : (Partie 1) Bien démarrer avec PowerShell).</span><span class="sxs-lookup"><span data-stu-id="624ba-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="624ba-121">Ou bien participer la [Prise en main rapide de PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) de Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="624ba-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="624ba-122">Développer vos compétences avec Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="624ba-122">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="624ba-123">Automatiser des tâches Azure à l’aide de scripts avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="624ba-123">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="624ba-124">Plus de formations interactives...</span><span class="sxs-lookup"><span data-stu-id="624ba-124">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="624ba-125">Autres modules Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="624ba-125">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="624ba-126">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="624ba-126">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="624ba-127">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="624ba-127">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="624ba-128">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="624ba-128">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="624ba-129">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="624ba-129">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
