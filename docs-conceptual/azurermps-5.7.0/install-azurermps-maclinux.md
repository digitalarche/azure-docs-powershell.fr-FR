---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323252"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installer Azure PowerShell sur macOS ou Linux

Il est désormais possible d’exécuter Azure PowerShell Core sur PowerShell Core v6 pour des plateformes non-Windows. Contrairement au produit Azure PowerShell standard intégré à .NET Framework pour Windows, ce produit est conçu pour .NET Core et peut s’exécuter sur n’importe quelle plateforme prenant en charge le runtime .net Core.

> [!NOTE]
> Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.
> La prise en charge de ces produits est limitée. Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.
>
> * [Problèmes pour PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problèmes pour Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>Installer PowerShell Core v6

L’installation de PowerShell Core v6 sur Linux ou macOS varie en fonction de la distribution Linux et de la version de système d’exploitation.
Vous trouverez des instructions détaillées dans les articles suivants :

- [Installer PowerShell Core sur macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Installer PowerShell Core sur Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Installer Azure PowerShell pour .NET Core

PowerShell Core v6 est fourni avec le module PowerShellGet déjà installé. Ceci facilite l’installation de n’importe quel module publié dans PowerShell Gallery. Pour installer Azure PowerShell, ouvrez une nouvelle session PowerShell et exécutez la commande suivante :

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>Charger le module AzureRM.Netcore

Une fois le module installé, vous devez le charger dans votre session PowerShell. Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Une fois l’importation terminée, vous pouvez tester votre module nouvellement installé en essayant de vous connecter à Azure avec la commande suivante :

```powershell
Connect-AzureRmAccount
```

La commande ci-dessus vous invite à accéder à `https://aka.ms/devicelogin` et à entrer le code fourni.

## <a name="available-cmdlets"></a>Applets de commande disponibles

Les modules Azure PowerShell pour .NET Standard sont en cours de développement. Ces modules ne fournissent pas l’ensemble des applets de commande qui sont disponibles pour la version Windows des modules. Les fonctions suivantes sont implémentées dans les modules AzureRM.Netcore :

* Account management
  - Se connecter avec un compte Microsoft, un compte d’organisation ou un principal du service via Microsoft Azure Active Directory
  - Enregistrer les informations d’identification sur disque avec Save-AzureRmContext et charger les informations d’identification enregistrées avec Import-AzureRmContext
* Environnement
  - Obtenir les différents environnements Microsoft Azure prédéfinis
  - Ajouter/définir/supprimer des environnements personnalisés (comme vos environnements Azure Stack ou Windows Azure Pack)
* Applets de commande de plan de gestion pour les services Azure avec les interfaces Resource Manager et Gestion des services.
  - Machine virtuelle
  - App Service (sites web)
  - Base de données SQL
  - Stockage
  - Réseau

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).
