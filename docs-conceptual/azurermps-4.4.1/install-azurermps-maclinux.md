---
title: "Installer et configurer Azure PowerShell sur macOS et Linux │ Microsoft Docs"
description: "Comment installer et configurer Azure PowerShell pour la première utilisation sur macOS et Linux."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 20af779cd523c758d40e23d60eb989a4ef982d5c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Installer et configurer Azure PowerShell sur macOS et Linux

Il est désormais possible d’installer PowerShell Core v6 et Azure PowerShell sur des plateformes non Windows.
Le processus d’installation d’Azure PowerShell sur macOS et Linux est presque le même que sur Windows, sauf que vous devez d’abord installer PowerShell Core v6.

> [!NOTE]

> Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.
> La prise en charge de ces produits est limitée. Si vous rencontrez des problèmes ou que vous découvrez des bogues, vous pouvez nous les signaler dans GitHub.
>
> * [Problèmes pour PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problèmes pour Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Étape 1 : Installer PowerShell Core v6

Le processus d’installation de PowerShell Core v6 varie selon le système d’exploitation cible.
S’il est possible d’installer PowerShell Core v6 sur Windows, cet article est néanmoins centré sur macOS et Linux. Si vous voulez utiliser Azure PowerShell sur Windows, consultez l’article sur [l’installation](./install-azurerm-ps.md) pour Windows.

L’installation de **PowerShell Core v6** sur Linux ou macOS varie en fonction de la distribution Linux et de la version de système d’exploitation.
Vous trouverez des instructions détaillées dans l’article suivant :

- [Installing PowerShell Core on macOS and Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux) (Installation de PowerShell Core sur macOS et Linux

## <a name="step-2-install-azure-powershell-for-net-core"></a>Étape 2 : Installer Azure PowerShell pour .NET Core

PowerShell Core v6 est fourni avec le module PowerShellGet déjà installé. Ceci facilite l’installation de n’importe quel module publié dans PowerShell Gallery. Pour installer Azure PowerShell, ouvrez une nouvelle session PowerShell et exécutez la commande suivante :

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Étape 3 : Charger le module AzureRM.Netcore

Une fois le module installé, vous devez le charger dans votre session PowerShell. Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Une fois l’importation terminée, vous pouvez tester votre module nouvellement installé en essayant de vous connecter à Azure avec la commande suivante :

```powershell
Login-AzureRMAccount
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
