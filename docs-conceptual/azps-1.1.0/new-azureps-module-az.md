---
title: Présentation du module Azure PowerShell Az
description: Présentation du nouveau module Azure PowerShell Az, en remplacement du module AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: d08bca962b6ff65d25135150824b7c24fbd20103
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342422"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="ae4c0-103">Présentation du nouveau module Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="ae4c0-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="ae4c0-104">À compter de décembre 2018, le module Azure PowerShell Az est en version générale et désormais le module PowerShell prévu pour interagir avec Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="ae4c0-105">Az propose des commandes plus courtes, améliore la stabilité et prend en charge plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="ae4c0-106">Az offre également une parité des fonctionnalités et un chemin de migration simple depuis AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="ae4c0-107">Az utilise la bibliothèque .NET Standard, ce qui signifie qu’il est exécuté sur PowerShell 5.x et PowerShell 6.x.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="ae4c0-108">Comme PowerShell 6.x peut être exécuté sur Linux, macOS et Windows, Azure PowerShell est maintenant disponible pour toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="ae4c0-109">L’utilisation de .NET Standard nous permet d’unifier la base de code d’Azure PowerShell en gardant un impact limité sur les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="ae4c0-110">Az étant un nouveau module, la version a été réinitialisée sur 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="ae4c0-111">Mettre à niveau vers Az</span><span class="sxs-lookup"><span data-stu-id="ae4c0-111">Upgrade to Az</span></span>

<span data-ttu-id="ae4c0-112">Il est recommandé à tous les utilisateurs d’effectuer la mise à niveau vers le nouveau module Az.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="ae4c0-113">Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="ae4c0-113">To do so:</span></span>

* <span data-ttu-id="ae4c0-114">__RECOMMANDÉ__ : [Désinstaller le module Azure PowerShell Azure RM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span><span class="sxs-lookup"><span data-stu-id="ae4c0-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* [<span data-ttu-id="ae4c0-115">Installer le module Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="ae4c0-115">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="ae4c0-116">Activez le mode de compatibilité afin d’ajouter des alias pour les cmdlets AzureRM avec `Enable-AzureRMAlias` pendant que vous vous familiarisez avec le nouveau jeu de commandes.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="ae4c0-117">Activez __uniquement__ les alias si vous n’avez pas installé AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="ae4c0-118">Migrer des scripts existants vers Az</span><span class="sxs-lookup"><span data-stu-id="ae4c0-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="ae4c0-119">D’importantes mises à jour peuvent entraîner des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="ae4c0-120">Toutefois, le module Az a un mode de compatibilité pour vous aider à utiliser des scripts existants lorsque vous travaillez sur les mises à jour vers la nouvelle syntaxe.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="ae4c0-121">Utilisez la cmdlet `Enable-AzureRmAlias` pour activer le mode de compatibilité AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="ae4c0-122">Cette cmdlet définit les noms de cmdlets AzureRM en tant qu’alias pour les nouveaux noms de cmdlets AzureRM.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="ae4c0-123">Les nouveaux noms de cmdlets ont été conçus pour être facile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="ae4c0-124">Plutôt que d’utiliser `AzureRm` ou `Azure` dans les noms de cmdlets, utilisez `Az`.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="ae4c0-125">Par exemple, l’ancienne commande `New-AzureRMVm` est devenue `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="ae4c0-126">Pour obtenir une description complète du processus de migration, consultez [Migrer d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="ae4c0-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="ae4c0-127">La prise en charge d’AzureRM dans le futur</span><span class="sxs-lookup"><span data-stu-id="ae4c0-127">The future of support for AzureRM</span></span>

<span data-ttu-id="ae4c0-128">Le module AzureRM existant ne recevra plus les nouvelles fonctionnalités ou cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="ae4c0-129">Toutefois, AzureRM dispose encore d’une maintenance officielle et recevra des corrections de bogues jusqu’en décembre 2020.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="ae4c0-130">Pour vous tenir informé des derniers services et fonctionnalités d’Azure, passez au module Az.</span><span class="sxs-lookup"><span data-stu-id="ae4c0-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
