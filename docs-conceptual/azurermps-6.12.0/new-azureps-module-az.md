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
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574802"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Présentation du nouveau module Azure PowerShell Az

Le module Azure PowerShell `Az` est disponible en préversion publique complète à compter de novembre 2018.
Az propose de plus petites commandes, améliore la stabilité et prend en charge Windows, macOS et Linux. Az offre également une parité des fonctionnalités et un chemin de migration simple depuis AzureRM.

Az utilise la bibliothèque .NET Standard, ce qui signifie qu’il est exécuté sur PowerShell 5.x et PowerShell 6.x.
Comme PowerShell 6.x peut être exécuté sur Linux, macOS et Windows, cela signifie que Az est disponible pour toutes les plateformes.
L’utilisation de .NET Standard nous permet d’unifier la base de code d’Azure PowerShell en gardant un impact limité sur les utilisateurs.

Az étant un nouveau module, la version a été réinitialisée. La première version stable sera la version 1.0, mais, à compter de novembre 2018, le module dispose de la parité des fonctionnalités avec AzureRm.

## <a name="upgrade-to-az"></a>Mettre à niveau vers Az

Il est recommandé aux utilisateurs de mettre à niveau vers le nouveau module `Az`. Pour ce faire :

* [Désinstaller le module Azure PowerShell Azure RM](/powershell/azure/uninstall-azurerm-ps)
* [Installer le module Azure PowerShell Az](/powershell/azure/install-az-ps)
* Activez le mode de compatibilité pour AzureRM avec `Enable-AzureRMAlias` pendant que vous vous familiarisez avec le nouveau jeu de commandes.

## <a name="migrate-existing-scripts-to-az"></a>Migrer des scripts existants vers Az

D’importantes mises à jour peuvent entraîner des inconvénients. Toutefois, le module `Az` a un mode de compatibilité pour vous aider à utiliser des scripts existants en même temps que vous travaillez sur les mises à jour vers la nouvelle syntaxe. Utilisez la cmdlet `Enable-AzureRmAlias` pour activer le mode de compatibilité `AzureRM`. Cette cmdlet définit les noms de cmdlets `AzureRM` en tant qu’alias pour les nouveaux noms de cmdlets `Az`.

Les nouveaux noms de cmdlets ont été conçus pour être facile à apprendre. Plutôt que d’utiliser `AzureRm` ou `Azure` dans les noms de cmdlets, utilisez `Az`. Par exemple, l’ancienne commande `New-AzureRmVm` est devenue `New-AzVm`.

Pour obtenir une description complète du processus de migration, consultez [Migrer d’AzureRM vers Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>La prise en charge d’AzureRM dans le futur

Le module `AzureRM` existant ne recevra plus de nouvelles cmdlets ni de nouvelles fonctionnalités lorsque la version 1.0 `Az` sortira en décembre 2018. Toutefois, `AzureRM` est encore conservée officiellement et il recevra des correctifs de bogues. Pour vous tenir informé des derniers services et fonctionnalités d’Azure, nous vous conseillons de passer au module `Az`.