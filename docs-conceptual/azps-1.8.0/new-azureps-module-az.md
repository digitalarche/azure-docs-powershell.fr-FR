---
title: Présentation du module Azure PowerShell Az
description: Présentation du nouveau module Azure PowerShell Az, en remplacement du module AzureRM.
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 8dc5a7d3b47870455213aa01aebc1d215ad640a7
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807486"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Présentation du nouveau module Azure PowerShell Az

À compter de décembre 2018, le module Azure PowerShell Az est en version générale et désormais le module PowerShell prévu pour interagir avec Azure. Az propose des commandes plus courtes, améliore la stabilité et prend en charge plusieurs plateformes. AZ dispose également des mêmes fonctionnalités qu’AzureRM, ce qui vous donne une voie de migration facile.

Avec le module Az, Azure PowerShell est désormais compatible avec PowerShell 5.1 sur Windows, et avec PowerShell Core 6.x et ultérieur, sur toutes les plateformes prises en charge,notamment Windows, macOS et Linux.

Az étant un nouveau module, la version a été réinitialisée sur 1.0.0.

## <a name="why-a-new-module"></a>Pourquoi un nouveau module ?

Les mises à jour majeures peuvent poser des problèmes : il est donc important pour vous de savoir pourquoi la décision a été prise d’introduire un nouvel ensemble de modules, avec de nouvelles applets de commande, pour interagir avec Azure à partir de PowerShell.

Le plus gros changement, et aussi le plus important, est que PowerShell est devenu un produit multiplateforme depuis l’introduction de [PowerShell Core 6.x](/powershell/scripting/overview), basé sur la bibliothèque .NET Standard.
Nous sommes attachés à fournir la prise en charge d’Azure sur toutes les plateformes, ce qui signifie que les modules Azure PowerShell devaient être mis à jour de façon à utiliser .NET Standard et à être compatible avec PowerShell Core. Au lieu de prendre le module AzureRM existant et d’y introduire des modifications complexes pour ajouter cette prise en charge, nous avons créé le module Az.

La création d’un nouveau module a également donné à nos ingénieurs l’occasion de mettre en cohérence la conception et le nommage des applets de commande et des modules. Les noms de tous les modules commencent désormais par le préfixe `Az.` et les applets de commande utilisent toutes la forme _Verbe_-`Az`_Nom_. Auparavant, les noms des applets de commande n’étaient pas seulement plus longs : il s’y trouvait aussi des incohérences.

Le nombre de modules a également été réduit : Certains modules qui fonctionnaient avec les mêmes services ont été regroupés ensemble, et les applets de commande de plan de gestion et de plan de données sont désormais contenues dans des modules uniques pour leurs services. Pour ceux d’entre vous qui gèrent manuellement les dépendances et les importations, ceci rend les choses beaucoup plus simples.

En faisant ces modifications importantes nécessitant la création d’un nouveau module Azure PowerShell, l’équipe s’est attachée à rendre plus facile que jamais, et sur plus de plateformes qu’auparavant, l’utilisation d’Azure avec des applets de commande PowerShell.

## <a name="upgrade-to-az"></a>Mettre à niveau vers Az

Pour bénéficier des dernières fonctionnalités d’Azure dans PowerShell, vous devez migrer vers le module Az dès que possible. Si vous n’êtes pas prêt à installer le module Az en remplacement d’AzureRM, vous disposez de deux des options pour faire des essais avec Az :

* Utilisez un environnement `PowerShell` avec [Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview).
  Azure Cloud Shell est un environnement shell basé sur un navigateur, qui est fourni avec le module Az installé et les alias de compatibilité de `Enable-AzureRM` activés.
* Conservez le module AzureRM installé avec PowerShell 5.1 pour Windows, mais installez le module Az pour PowerShell Core 6.x ou ultérieur. PowerShell 5.1 pour Windows et PowerShell Core utilisent des collections distinctes de modules. Suivez les instructions pour [installer PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows), puis [installez le module Az](install-az-ps.md) à partir d’un terminal PowerShell Core.

Pour mettre à niveau à partir d’une installation existante d’AzureRM :

1. [Désinstaller le module Azure PowerShell Azure RM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
2. [Installer le module Azure PowerShell Az](install-az-ps.md)
3. __FACULTATIF__ : Activez le mode de compatibilité afin d’ajouter des alias pour les applets de commande AzureRM avec [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) pendant la période où vous vous familiarisez avec le nouveau jeu de commandes. Pour plus d’informations, consultez la section suivante ou [Démarrer la migration depuis AzureRM vers Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Migrer des scripts existants vers Az

Les nouveaux noms de cmdlets ont été conçus pour être facile à apprendre. Plutôt que d’utiliser `AzureRm` ou `Azure` dans les noms de cmdlets, utilisez `Az`. Par exemple, l’ancienne commande `New-AzureRMVm` est devenue `New-AzVm`.
La migration ne consiste cependant pas seulement à vous familiariser avec les nouveaux noms des applets de commande : Des modules et des paramètres ont été renommés, et il y a d’autres changements importants.

Pour vous aider dans le processus de migration depuis AzureRM vers Az, vous disposez de plusieurs ressources :

* [Bien démarrer avec la migration depuis AzureRM vers Az](migrate-from-azurerm-to-az.md)
* [Liste complète des changements cassants d’AzureRM à Az 1.0.0](migrate-az-1.0.0.md)
* L’applet de commande [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

Le module Az a un mode de compatibilité pour vous aider à utiliser des scripts existants quand vous faites la mise à jour vers la nouvelle syntaxe. L’applet de commande [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) active un mode de compatibilité via des alias, pour vous permettre d’utiliser des scripts existants avec des modifications minimales pendant la période où vous travaillez à une migration complète vers Az.

> [!IMPORTANT]
> Même si les noms des applets de commande sont associés à des alias, il peut néanmoins y avoir de nouveaux paramètres (ou des paramètres renommés) ou des changements dans les valeurs retournées pour les applets de commande Az. Ne pensez donc pas que la simple activation des alias va prendre soin de la migration pour vous ! Consultez la [liste complète des changements cassants](migrate-az-1.0.0.md) pour voir où vos scripts peuvent nécessiter des mises à jour.

## <a name="continued-support-for-azurerm"></a>Poursuite du support d’AzureRM

AzureRM ne recevra plus les nouvelles fonctionnalités ou applets de commande. Toutefois, le module AzureRM dispose encore d’une maintenance officielle et recevra des correctifs de bogues jusqu’en décembre 2020.