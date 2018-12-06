---
title: Présentation du module Azure PowerShell Az
description: Présentation du nouveau module Azure PowerShell Az, en remplacement du module AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828108"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="4c200-103">Présentation du nouveau module Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="4c200-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="4c200-104">Le module Azure PowerShell `Az` est disponible en préversion publique complète à compter de novembre 2018.</span><span class="sxs-lookup"><span data-stu-id="4c200-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="4c200-105">Az propose de plus petites commandes, améliore la stabilité et prend en charge Windows, macOS et Linux.</span><span class="sxs-lookup"><span data-stu-id="4c200-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="4c200-106">Az offre également une parité des fonctionnalités et un chemin de migration simple depuis AzureRM.</span><span class="sxs-lookup"><span data-stu-id="4c200-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="4c200-107">Az utilise la bibliothèque .NET Standard, ce qui signifie qu’il est exécuté sur PowerShell 5.x et PowerShell 6.x.</span><span class="sxs-lookup"><span data-stu-id="4c200-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="4c200-108">Comme PowerShell 6.x peut être exécuté sur Linux, macOS et Windows, cela signifie que Az est disponible pour toutes les plateformes.</span><span class="sxs-lookup"><span data-stu-id="4c200-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="4c200-109">L’utilisation de .NET Standard nous permet d’unifier la base de code d’Azure PowerShell en gardant un impact limité sur les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4c200-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="4c200-110">Az étant un nouveau module, la version a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="4c200-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="4c200-111">La première version stable sera la version 1.0, mais, à compter de novembre 2018, le module dispose de la parité des fonctionnalités avec AzureRm.</span><span class="sxs-lookup"><span data-stu-id="4c200-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="4c200-112">Mettre à niveau vers Az</span><span class="sxs-lookup"><span data-stu-id="4c200-112">Upgrade to Az</span></span>

<span data-ttu-id="4c200-113">Il est recommandé aux utilisateurs de mettre à niveau vers le nouveau module `Az`.</span><span class="sxs-lookup"><span data-stu-id="4c200-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="4c200-114">Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="4c200-114">To do so:</span></span>

* [<span data-ttu-id="4c200-115">Désinstaller le module Azure PowerShell Azure RM</span><span class="sxs-lookup"><span data-stu-id="4c200-115">Uninstall the Azure PowerShell AzureRM module</span></span>](/powershell/azure/uninstall-azurerm-ps)
* [<span data-ttu-id="4c200-116">Installer le module Azure PowerShell Az</span><span class="sxs-lookup"><span data-stu-id="4c200-116">Install the Azure PowerShell Az module</span></span>](/powershell/azure/install-az-ps)
* <span data-ttu-id="4c200-117">Activez le mode de compatibilité pour AzureRM avec `Enable-AzureRMAlias` pendant que vous vous familiarisez avec le nouveau jeu de commandes.</span><span class="sxs-lookup"><span data-stu-id="4c200-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="4c200-118">Migrer des scripts existants vers Az</span><span class="sxs-lookup"><span data-stu-id="4c200-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="4c200-119">D’importantes mises à jour peuvent entraîner des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="4c200-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="4c200-120">Toutefois, le module `Az` a un mode de compatibilité pour vous aider à utiliser des scripts existants en même temps que vous travaillez sur les mises à jour vers la nouvelle syntaxe.</span><span class="sxs-lookup"><span data-stu-id="4c200-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="4c200-121">Utilisez la cmdlet `Enable-AzureRmAlias` pour activer le mode de compatibilité `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="4c200-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="4c200-122">Cette cmdlet définit les noms de cmdlets `AzureRM` en tant qu’alias pour les nouveaux noms de cmdlets `Az`.</span><span class="sxs-lookup"><span data-stu-id="4c200-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="4c200-123">Les nouveaux noms de cmdlets ont été conçus pour être facile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="4c200-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="4c200-124">Plutôt que d’utiliser `AzureRm` ou `Azure` dans les noms de cmdlets, utilisez `Az`.</span><span class="sxs-lookup"><span data-stu-id="4c200-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="4c200-125">Par exemple, l’ancienne commande `New-AzureRmVm` est devenue `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="4c200-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="4c200-126">Pour obtenir une description complète du processus de migration, consultez [Migrer d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="4c200-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="4c200-127">La prise en charge d’AzureRM dans le futur</span><span class="sxs-lookup"><span data-stu-id="4c200-127">The future of support for AzureRM</span></span>

<span data-ttu-id="4c200-128">Le module `AzureRM` existant ne recevra plus de nouvelles cmdlets ni de nouvelles fonctionnalités lorsque la version 1.0 `Az` sortira en décembre 2018.</span><span class="sxs-lookup"><span data-stu-id="4c200-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="4c200-129">Toutefois, `AzureRM` est encore conservée officiellement et il recevra des correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="4c200-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="4c200-130">Pour vous tenir informé des derniers services et fonctionnalités d’Azure, nous vous conseillons de passer au module `Az`.</span><span class="sxs-lookup"><span data-stu-id="4c200-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>