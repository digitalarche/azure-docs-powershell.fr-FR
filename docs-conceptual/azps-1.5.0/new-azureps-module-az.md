---
title: Présentation du module Azure PowerShell Az
description: Présentation du nouveau module Azure PowerShell Az, en remplacement du module AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882290"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Présentation du nouveau module Azure PowerShell Az

À compter de décembre 2018, le module Azure PowerShell Az est en version générale et désormais le module PowerShell prévu pour interagir avec Azure. Az propose des commandes plus courtes, améliore la stabilité et prend en charge plusieurs plateformes. Az offre également une parité des fonctionnalités et un chemin de migration simple depuis AzureRM.

Az utilise la bibliothèque .NET Standard, ce qui signifie qu’il est exécuté sur PowerShell 5 et sur PowerShell 6.
Comme PowerShell 6 peut être exécuté sur Linux, macOS et Windows, Azure PowerShell est maintenant disponible pour toutes les plateformes.
L’utilisation de .NET Standard nous permet d’unifier la base de code d’Azure PowerShell en gardant un impact limité sur les utilisateurs.

Az étant un nouveau module, la version a été réinitialisée sur 1.0.0.

## <a name="upgrade-to-az"></a>Mettre à niveau vers Az

Il est recommandé à tous les utilisateurs d’effectuer la mise à niveau vers le nouveau module Az. Pour ce faire :

* __RECOMMANDÉ__ : [Désinstaller le module Azure PowerShell Azure RM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
* [Installer le module Azure PowerShell Az](/powershell/azure/install-az-ps)
* Activez le mode de compatibilité afin d’ajouter des alias pour les cmdlets AzureRM avec `Enable-AzureRMAlias` pendant que vous vous familiarisez avec le nouveau jeu de commandes. Activez __uniquement__ les alias si vous n’avez pas installé AzureRM.

## <a name="migrate-existing-scripts-to-az"></a>Migrer des scripts existants vers Az

D’importantes mises à jour peuvent entraîner des inconvénients. Toutefois, le module Az a un mode de compatibilité pour vous aider à utiliser des scripts existants lorsque vous travaillez sur les mises à jour vers la nouvelle syntaxe. Utilisez la cmdlet `Enable-AzureRmAlias` pour activer le mode de compatibilité AzureRM. Cette cmdlet définit les noms de cmdlets AzureRM en tant qu’alias pour les nouveaux noms de cmdlets AzureRM.

Les nouveaux noms de cmdlets ont été conçus pour être facile à apprendre. Plutôt que d’utiliser `AzureRm` ou `Azure` dans les noms de cmdlets, utilisez `Az`. Par exemple, l’ancienne commande `New-AzureRMVm` est devenue `New-AzVm`.

Pour obtenir une description complète du processus de migration, consultez [Migrer d’AzureRM vers Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>La prise en charge d’AzureRM dans le futur

Le module AzureRM existant ne recevra plus les nouvelles fonctionnalités ou cmdlets. Toutefois, AzureRM dispose encore d’une maintenance officielle et recevra des corrections de bogues jusqu’en décembre 2020. Pour vous tenir informé des derniers services et fonctionnalités d’Azure, passez au module Az.
