---
title: Migrer des scripts Azure PowerShell depuis AzureRM vers Az
description: Découvrez les étapes et les outils pour effectuer une migration des scripts à partir du module AzureRM vers le nouveau module Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 720387ec1b23f10ddf2b153cf0705b2b6d1b7b82
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587701"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrer de AzureRM vers Azure PowerShell Az

Le module Az a la même parité des fonctionnalités que AzureRM, mais il utilise des noms de cmdlets plus courts et plus cohérents.
Les scripts écrits pour les cmdlets AzureRM ne fonctionnent pas automatiquement avec le nouveau module. Pour faciliter la transition, Az propose des outils qui vous permettent d’exécuter vos scripts existants à l’aide d’AzureRM. Il n’existe pas une migration vers un nouveau jeu de commandes qui soit pratique, mais cet article vous aide à bien démarrer la transition vers le nouveau module.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Assurez-vous que vos scripts existants fonctionnent avec la dernière version d’AzureRM

Il s’agit de l’étape la plus importante. Exécutez vos scripts existants et assurez-vous qu’ils fonctionnent avec la _dernière_ version d’AzureRM (__6.13.0__). Si vos scripts ne fonctionnent pas, veuillez lire le [guide de migration AzureRM](migration-guide.6.0.0.md).

## <a name="install-the-azure-powershell-az-module"></a>Installer le module Azure PowerShell Az

La première étape consiste à installer le module Az sur votre plateforme. Pour installer Az, vous devez désinstaller AzureRM.
Dans les étapes suivantes, vous découvrez comment poursuivre l’exécution de vos scripts existants et activer la compatibilité pour les anciens noms de cmdlets.

Pour installer le module Azure PowerShell Az, suivez les étapes suivantes :

* [Désinstaller le module AzureRM](uninstall-azurerm-ps.md). Assurez-vous de supprimer _toutes les_ versions installées d’AzureRM, et non pas simplement la plus récente.
* [Installer le module Az](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>Activer le mode alias d’AzureRM

Une fois AzureRM désinstallé et vos scripts compatibles avec la dernière version d’AzureRM, vous pouvez procéder à l’activation du mode de compatibilité pour le module Az. La compatibilité est activée à l’aide de la commande :

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Les alias rendent possible l’utilisation des anciens noms de cmdlets avec le module `Az` installé. Ces alias sont écrits dans le profil utilisateur pour l’étendue sélectionnée. S’il n’en existe aucun, un profil utilisateur est créé.

> [!WARNING]
>
> Vous pouvez utiliser une autre `-Scope` pour cette commande, mais ce n’est pas conseillé ! Les alias sont écrits dans le profil utilisateur pour l’étendue sélectionnée. Ainsi, poursuivez leur activation pour une étendue aussi limitée que possible. L’activation des alias à l’échelle du système peut également entraîner des problèmes pour d’autres utilisateurs qui ont installé `AzureRM` dans leur étendue locale.

Une fois le mode alias activé, exécutez une nouvelle fois les scripts pour confirmer qu’ils fonctionnent toujours comme prévu. 

## <a name="change-module-imports-and-cmdlet-names"></a>Modifier les importations de modules et les noms de cmdlets

En règle générale, les noms de module ont été modifiés pour que `AzureRM` et `Azure` deviennent `Az`et il en va de même pour les cmdlets.
Par exemple, le module `AzureRM.Compute` a été renommé `Az.Compute`. `New-AzureRmVM` est devenu `New-AzVM` et `Get-AzureStorageBlob` est désormais `Get-AzStorageBlob`.

Il existe des exceptions à cette modification de dénomination que vous devez connaître avant de renommer quoi que ce soit :

| Module AzureRM | Module Az |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>Résumé

Suivez les étapes suivantes pour mettre à jour tous vos scripts existants et utiliser le nouveau module. Si vous avez des questions concernant ces étapes ou rencontrez des problèmes rendant la migration difficile, veuillez laisser un commentaire sur cet article afin que nous puissions améliorer les instructions.
