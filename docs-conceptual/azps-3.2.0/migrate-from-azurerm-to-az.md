---
title: Migrer des scripts Azure PowerShell depuis AzureRM vers Az
description: Découvrez les étapes et les outils pour effectuer une migration des scripts à partir du module AzureRM vers le nouveau module Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182143"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Migrer Azure PowerShell depuis AzureRM vers Az

Le module Az a la même parité des fonctionnalités que AzureRM, mais il utilise des noms de cmdlets plus courts et plus cohérents.
Les scripts écrits pour les cmdlets AzureRM ne fonctionnent pas automatiquement avec le nouveau module. Pour faciliter la transition, Az propose des outils qui vous permettent d’exécuter vos scripts existants à l’aide d’AzureRM. Il n’existe pas une migration vers un nouveau jeu de commandes qui soit pratique, mais cet article vous aide à bien démarrer la transition vers le nouveau module.

Pour obtenir la liste complète des changements cassants entre AzureRM et Az, consultez les [Modifications entre AzureRM et Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Vérifier que les scripts existants fonctionnent avec la dernière version d’AzureRM

Avant d’effectuer toutes les étapes de migration, vérifiez les versions d’AzureRM installées sur votre système. Vous pouvez ainsi vérifier que les scripts s’exécutent déjà sur la dernière version et savoir quelles versions d’AzureRM doivent être désinstallées.

Pour vérifier quelles sont les versions d’AzureRM que vous avez installées, exécutez la commande :

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

La version disponible __la plus récente__ d’AzureRM est __6.13.1__. Si cette version n’est pas installée, vos scripts existants peuvent nécessiter des modifications supplémentaires pour fonctionner avec le module Az, qui vont au-delà de ce qui est décrit ici et dans la [liste des changements cassants](migrate-az-1.0.0.md).

Si vos scripts ne fonctionnent pas avec AzureRM 6.13.1, mettez-les à jour conformément au [Guide de migration d’AzureRM 5.x vers 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).
Si vous utilisez une version antérieure du module AzureRM, consultez les guides de migration disponibles pour chaque version majeure.

## <a name="uninstall-azurerm"></a>Désinstaller AzureRM

La compatibilité du module Az avec les installations existantes d’AzureRM dans PowerShell 5.1 pour Windows n’est pas garantie. Avant d’installer le module Az, [désinstallez AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Si vous n’êtes pas prêt à supprimer le module AzureRM de votre système, vous pouvez à la place installer le module Az pour [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x ou ultérieur. PowerShell Core et PowerShell 5.1 pour Windows utilisent des bibliothèques de module différentes : il n’y aura donc pas de conflits. Vous pouvez toujours [activer les alias](#enable-azurerm-compatibility-aliases) dans PowerShell Core.

## <a name="install-the-azure-powershell-az-module"></a>Installer le module Azure PowerShell Az

La première étape consiste à installer le module Az sur votre plateforme. Lorsque vous installez Az, il est recommandé de désinstaller AzureRM. Dans les étapes suivantes, vous découvrez comment poursuivre l’exécution de vos scripts existants et activer la compatibilité pour les anciens noms de cmdlets.

Pour installer le module Az d’Azure PowerShell, suivez les instructions de [Installer le module Az](install-az-ps.md).

> [!NOTE]
> À ce stade, vous pouvez exécuter l’applet de commande [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) fournie dans le module Az, simplement pour vérifier que toutes les versions d’AzureRM ont été désinstallées et ne vont pas provoquer de conflits.

## <a name="enable-azurerm-compatibility-aliases"></a>Activer les alias de compatibilité AzureRM

Une fois AzureRM désinstallé et vos scripts utilisant la dernière version d’AzureRM, vous pouvez procéder à l’activation du mode de compatibilité pour le module Az. La compatibilité est activée à l’aide de la commande :

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Les alias rendent possible l’utilisation des anciens noms de cmdlets avec le module Az installé. Ces alias sont écrits dans le profil pour l’étendue sélectionnée. S’il n’en existe pas, un profil est créé.
Lors de l’utilisation d’une étendue (`-Scope`) plus grande que `CurrentUser`, les autorisations appropriées sont nécessaires pour créer ou mettre à jour le fichier de profil correspondant.

> [!IMPORTANT]
> __Seuls__ les noms des applets de commande reçoivent un alias : les noms de module n’en reçoivent pas ! Si vous utilisez `#Requires`, `Import-Module`, des listes de dépendances dans un fichier `.psd1` ou des noms d’applet de commande complets, veillez à les migrer à ce stade en suivant la procédure décrite dans la [liste des changements cassants](migrate-az-1.0.0.md) pour les noms de module.

> [!WARNING]
>
> Vous pouvez utiliser une autre `-Scope` pour cette commande, mais ce n’est pas conseillé ! Les alias sont écrits dans le profil utilisateur pour l’étendue sélectionnée. Ainsi, poursuivez leur activation pour une étendue aussi limitée que possible. L’activation des alias à l’échelle du système peut également entraîner des problèmes pour d’autres utilisateurs qui ont installé AzureRM dans leur étendue locale.

Une fois le mode alias activé, exécutez une nouvelle fois les scripts pour confirmer qu’ils fonctionnent toujours comme prévu.
Certains noms de paramètre ont été changés ou ajoutés, ou sont devenus obligatoires pour le module Az. Les types de sortie des applets de commande peuvent également avoir changé. Ces modifications sont détaillées dans la [liste des changements cassants](migrate-az-1.0.0.md).

## <a name="update-cmdlets-modules-and-parameters"></a>Mettre à jour les applets de commande, les modules et les paramètres

Avec des scripts mis à jour et s’exécutant avec des alias, vous pouvez prendre votre temps pour les mettre à jour de façon à ce qu’ils utilisent les nouvelles applets de commande et tirent parti des autres modifications, comme les nouvelles fonctionnalités. Pour la plupart des scripts, vous devez seulement mettre à jour les noms des applets de commande, [d’après le nouveau schéma de nommage des applets de commande dans Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes). D’autres modifications peuvent être nécessaires pour que vos scripts fonctionnent, selon ce qu’ils font et selon les fonctionnalités Azure PowerShell qu’ils utilisent.

Par exemple, les [applets de commande de Stockage Blob](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage) ont été entièrement reprises de façon à utiliser un nouveau modèle asynchrone : les scripts qui les utilisent vous demanderont donc plus de travail de mise à jour que ceux où les modifications portent seulement sur les noms des applets de commande.

Même si vous n’avez dû faire que de petites modifications simples dans vos scripts, ou même s’ils fonctionnent sans autres modifications quand les alias sont activés, lisez [la liste complète des changements cassants dans Az 1.0.0](migrate-az-1.0.0.md) pour être sûr que vous ne vous appuyez pas sur le comportement « transparent » des alias qui pourrait disparaître une fois que vous avez changé les noms des applets de commande et que vous avez désactivé les alias.

## <a name="disable-aliases"></a>Désactiver les alias

Une fois que vous avez effectué votre migration et que vous ne vous appuyez plus sur le comportement dû aux alias, il est recommandé de désactiver les alias. Vous faites cela avec l’applet de commande [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Lors de l’exécution de cette applet de commande, __veillez__ à l’appeler pour chaque `-Scope` pour laquelle `Enable-AzureRmAlias` a été appelée ; sinon, il pourrait rester des scripts sur votre système qui s’appuient sur le comportement dû aux alias.
