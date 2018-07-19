---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 6e7d447ea9672c174e3f1d103bc56c11a7f37192
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024917"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installer Azure PowerShell sur macOS ou Linux

Il est désormais possible d’exécuter Azure PowerShell dans PowerShell Core v6 pour des plateformes non-Windows. Cette version de PowerShell est conçue pour une utilisation sur n’importe quelle plateforme prenant en charge .NET Core. Pour utiliser ces plateformes, une version .NET Core spéciale d’Azure PowerShell est disponible.

> [!NOTE]
> Actuellement, PowerShell Core v6 et Azure PowerShell pour .NET Core sont toujours en version bêta.
> La prise en charge de ces produits est limitée. Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.
>
> * [Problèmes pour PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problèmes pour Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Installer PowerShell Core

Les instructions d’installation de PowerShell Core sont différentes sur macOS et la plupart des distributions Linux.
Vous trouverez des instructions détaillées dans les articles suivants :

* [Installer PowerShell Core sur macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Installer PowerShell Core sur Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Installer Azure PowerShell pour .NET Core

PowerShell Core est fourni avec le module PowerShellGet déjà installé. L’installation des modules dans PowerShell nécessite des privilèges élevés. Vous devez donc démarrer votre session en tant que superutilisateur :

```bash
sudo pwsh
```

Pour installer Azure PowerShell, exécutez la commande suivante :

```powershell
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> Le module `AzureRM` détaillé dans d’autres articles n’est pas conçu pour .NET Core et ne fonctionne pas avec PowerShell Core. `AzureRM` et `AzureRM.NetCore` utilisent les mêmes noms de cmdlet. Ils se différencient par le nom du module cumulatif et par la version .NET sur laquelle ils ont été conçus.

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez `Yes` ou `Yes to All` pour procéder à l’installation.

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM.Netcore` dans votre session PowerShell avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure. L’importation d’un module ne nécessite __pas__ de privilèges élevés.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Sur macOS et Linux, vous devez utiliser votre profil via la variable d’environnement `$Profile`. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).

## <a name="available-cmdlets"></a>Applets de commande disponibles

Les modules Azure PowerShell pour .NET Core sont en cours de développement. Ces modules ne fournissent pas l’ensemble des applets de commande qui sont disponibles pour la version Windows des modules. Les fonctions suivantes sont implémentées dans les modules AzureRM.Netcore :

* Account management
  * Se connecter avec un compte Microsoft, un compte d’organisation ou un principal du service via Microsoft Azure Active Directory
  * Enregistrer les informations d’identification sur disque avec Save-AzureRmContext et charger les informations d’identification enregistrées avec Import-AzureRmContext
* Environnement
  * Obtenir les différents environnements Microsoft Azure prédéfinis
  * Ajouter/définir/supprimer des environnements personnalisés (comme vos environnements Azure Stack ou Windows Azure Pack)
* Applets de commande de plan de gestion pour les services Azure avec les interfaces Resource Manager et Gestion des services.
  * Machine virtuelle
  * App Service (sites web)
  * SQL Database
  * Stockage
  * Réseau

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).
