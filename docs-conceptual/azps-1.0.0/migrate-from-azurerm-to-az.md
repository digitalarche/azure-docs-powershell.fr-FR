---
title: Migrer des scripts Azure PowerShell depuis AzureRM vers Az
description: Découvrez les étapes et les outils pour effectuer une migration des scripts à partir du module AzureRM vers le nouveau module Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982941"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Migrer de AzureRM vers Azure PowerShell Az

Le module Az a la même parité des fonctionnalités que AzureRM, mais il utilise des noms de cmdlets plus courts et plus cohérents.
Les scripts écrits pour les cmdlets AzureRM ne fonctionnent pas automatiquement avec le nouveau module. Pour faciliter la transition, Az propose des outils qui vous permettent d’exécuter vos scripts existants à l’aide d’AzureRM. Il n’existe pas une migration vers un nouveau jeu de commandes qui soit pratique, mais cet article vous aide à bien démarrer la transition vers le nouveau module.

Pour obtenir la liste complète des changements cassants entre AzureRM et Az, consultez le [guide de migration pour Az 1.0.0](migrate-az-1.0.0.md).

## <a name="check-for-installed-versions-of-azurerm"></a>Rechercher les versions installées d’AzureRM

Le module Az peut être installé côte à côte avec le module AzureRM, mais cela n’est pas recommandé. Avant d’effectuer toutes les étapes de migration, vérifiez les versions d’AzureRM installées sur votre système. Vous pouvez ainsi vous assurer que les scripts s’exécutent déjà sur la dernière version et savoir si vous pouvez activer des alias de commande sans désinstaller AzureRM.

Pour vérifier quelles sont les versions d’AzureRM que vous avez installées, exécutez la commande :

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Assurez-vous que vos scripts existants fonctionnent avec la dernière version d’AzureRM

Il s’agit de l’étape la plus importante. Exécutez vos scripts existants et assurez-vous qu’ils fonctionnent avec la _dernière_ version d’AzureRM (__6.13.1__). Si vos scripts ne fonctionnent pas, veuillez lire le [guide de migration AzureRM](/powershell/azure/azurerm/migration-guide.6.0.0).

## <a name="install-the-azure-powershell-az-module"></a>Installer le module Azure PowerShell Az

La première étape consiste à installer le module Az sur votre plateforme. Lorsque vous installez Az, il est recommandé de désinstaller AzureRM. Dans les étapes suivantes, vous découvrez comment poursuivre l’exécution de vos scripts existants et activer la compatibilité pour les anciens noms de cmdlets.

Pour installer le module Azure PowerShell Az, suivez les étapes suivantes :

* __RECOMMANDÉ__ : [Désinstaller le module AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  Assurez-vous de supprimer _toutes les_ versions installées d’AzureRM, et non pas simplement la plus récente.
* [Installer le module Az](install-az-ps.md)

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>Activer les alias de compatibilité AzureRM 

> [!IMPORTANT]
>
> Activez uniquement le mode de compatibilité si vous avez désinstallé _toutes_ les versions d’AzureRM. L’activation du mode de compatibilité alors que les cmdlets AzureRM sont encore disponibles peut entraîner un comportement imprévisible. Ignorez cette étape si vous avez décidé de conserver l’installation d’AzureRM, mais n’oubliez pas que les cmdlets AzureRM utiliseront les anciens modules et n’appelleront pas appeler les cmdlets Az.

Une fois AzureRM désinstallé et vos scripts utilisant la dernière version d’AzureRM, vous pouvez procéder à l’activation du mode de compatibilité pour le module Az. La compatibilité est activée à l’aide de la commande :

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Les alias rendent possible l’utilisation des anciens noms de cmdlets avec le module Az installé. Ces alias sont écrits dans le profil utilisateur pour l’étendue sélectionnée. S’il n’en existe aucun, un profil utilisateur est créé.

> [!WARNING]
>
> Vous pouvez utiliser une autre `-Scope` pour cette commande, mais ce n’est pas conseillé ! Les alias sont écrits dans le profil utilisateur pour l’étendue sélectionnée. Ainsi, poursuivez leur activation pour une étendue aussi limitée que possible. L’activation des alias à l’échelle du système peut également entraîner des problèmes pour d’autres utilisateurs qui ont installé AzureRM dans leur étendue locale.

Une fois le mode alias activé, exécutez une nouvelle fois les scripts pour confirmer qu’ils fonctionnent toujours comme prévu. 

## <a name="change-module-imports-and-cmdlet-names"></a>Modifier les importations de modules et les noms de cmdlets

En règle générale, les noms de module ont été modifiés pour que `AzureRM` et `Azure` deviennent `Az`et il en va de même pour les cmdlets.
Par exemple, le module `AzureRM.Compute` a été renommé `Az.Compute`. `New-AzureRMVM` est devenu `New-AzVM` et `Get-AzureStorageBlob` est désormais `Get-AzStorageBlob`.

Il existe des exceptions à cette modification de dénomination que vous devez connaître. Certains modules ont été renommés ou fusionnés dans les modules existants sans incidence sur le suffixe de leurs cmdlets, à l’exception du remplacement de `AzureRM` ou `Azure` par `Az`. Sinon, le suffixe complet de la cmdlet a été modifié pour refléter le nouveau nom de module.

| Module AzureRM | Module Az | Suffixe de cmdlet modifié ? |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | Oui |
| AzureRM.Insights | Az.Monitor | Oui |
| AzureRM.DataFactories | Az.DataFactory | Oui |
| AzureRM.DataFactoryV2 | Az.DataFactory | Oui |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | Non  |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | Non  |
| AzureRM.Tags | Az.Resources | Non  |
| AzureRM.MachineLearningCompute | Az.MachineLearning | Non  |
| AzureRM.UsageAggregates | Az.Billing | Non  |
| AzureRM.Consumption | Az.Billing | Non  |

## <a name="summary"></a>Résumé

Suivez les étapes suivantes pour mettre à jour tous vos scripts existants et utiliser le nouveau module. Si vous avez des questions concernant ces étapes ou rencontrez des problèmes rendant la migration difficile, veuillez laisser un commentaire sur cet article afin que nous puissions améliorer les instructions.
