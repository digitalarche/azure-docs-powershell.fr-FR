---
title: Vue d’ensemble d’Azure PowerShell
description: Vue d’ensemble du module Az Azure PowerShell, avec des informations sur l’installation et la prise en main.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068810"
---
# <a name="overview-of-azure-powershell"></a>Vue d’ensemble d’Azure PowerShell

Azure PowerShell fournit un ensemble d’applets de commande qui utilisent le modèle [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) pour gérer vos ressources Azure. Azure PowerShell utilise .NET Standard, permettant ainsi une disponibilité pour Windows, macOS et Linux.
Azure PowerShell est également disponible sur Azure Cloud Shell.

## <a name="about-the-new-az-module"></a>À propos du nouveau module Az

Cette documentation décrit le nouveau module Az pour Azure PowerShell. Ce nouveau module est entièrement écrit dans .NET Standard. L’utilisation de .NET Standard permet d’exécuter Azure PowerShell avec PowerShell 5 sur Windows, et avec PowerShell 6 sur n’importe quelle plateforme. Le module Az est maintenant le moyen d’interaction avec Azure via PowerShell.
AzureRM continuera de bénéficier de correctifs de bogues, mais ne recevra plus de nouvelles fonctionnalités.

Obtenez plus d’informations sur le nouveau module, y compris la façon dont les commandes ont été renommées et les plans de maintenance pour AzureRM, dans la [présentation du module Az Azure PowerShell](new-azureps-module-az.md). Si vous souhaitez commencer à utiliser le nouveau module tout de suite, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).

Une [documentation AzureRM](/powershell/azure/azurerm) est également disponible.

> [!IMPORTANT]
>
> Bien que la documentation Azure ait été mise à jour pour refléter les nouveaux noms de cmdlet de module, les articles peuvent toujours utiliser les commandes AzureRM. Après avoir installé le module Az, il est recommandé d’activer les alias de cmdlet AzureRM avec `Enable-AzureRmAlias`. Consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md) pour plus d’informations.

## <a name="run-or-install"></a>Exécuter ou installer

Vous pouvez installer Azure PowerShell avec PowerShell version 5.1 ou ultérieure sur Windows ou avec PowerShell 6 sur n’importe quelle plateforme. Vous pouvez également l’exécuter dans Azure Cloud Shell.

* Pour l’exécuter dans votre navigateur avec Azure Cloud Shell, consultez le [guide de démarrage rapide de PowerShell dans Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Pour installer Azure PowerShell sur votre système, consultez [Installer Azure PowerShell](install-az-ps.md).

Pour plus d’informations sur la dernière version d’Azure PowerShell, consultez les [notes de publication](release-notes-azureps.md).

## <a name="get-started"></a>Prise en main

Consultez l’article de [Prise en main d’Azure PowerShell](get-started-azureps.md) pour découvrir les bases d’Azure PowerShell. Si vous n’êtes pas familiarisé avec PowerShell, une introduction à ce logiciel peut s’avérer opportune :

* [Installer PowerShell](/powershell/scripting/install/installing-powershell)
* [Scripts avec PowerShell](/powershell/scripting/powershell-scripting)
* [Notions de base de PowerShell : (Première partie) Prise en main de PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* [Prise en main rapide de PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) de Microsoft Virtual Academy

Les exemples suivants peuvent vous aider pour certaines utilisations courantes d’Azure :

* [Machines virtuelles Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Machines virtuelles Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [Bases de données SQL](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Développer vos compétences avec Microsoft Learn

- [Automatiser des tâches Azure à l’aide de scripts avec PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Plus de formations interactives...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Autres modules Azure PowerShell

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
