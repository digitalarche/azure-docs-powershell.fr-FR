---
title: Installer Azure PowerShell sur macOS ou Linux
description: Procédure d’installation d’Azure PowerShell sur macOS ou Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273801"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installer Azure PowerShell sur macOS ou Linux

Il est désormais possible d’exécuter Azure PowerShell dans PowerShell Core v6 pour des plateformes non-Windows. Cette version de PowerShell est conçue pour une utilisation sur n’importe quelle plateforme prenant en charge .NET Core. Pour utiliser ces plateformes, une version .NET Standard d’Azure PowerShell est disponible.

> [!NOTE]
> Actuellement, Azure PowerShell pour .NET Standard est toujours en version bêta.
> Si vous rencontrez des problèmes ou détectez des bogues, signalez-les sur GitHub.
>
> * [Problèmes pour Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Installer PowerShell Core

Les instructions d’installation de PowerShell Core sont différentes sur macOS et la plupart des distributions Linux.
Vous trouverez des instructions détaillées dans les articles suivants :

* [Installer PowerShell Core sur macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Installer PowerShell Core sur Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>Installer Azure PowerShell pour .NET Standard

> [!IMPORTANT]
> Le module `AzureRM` détaillé dans d’autres articles ne fonctionne pas avec PowerShell Core.
> Vous devez installer le module `Az` pour obtenir des fonctionnalités Azure PowerShell dans PowerShell Core.

PowerShell Core est fourni avec le module PowerShellGet déjà installé. Démarrez PowerShell avec la commande :

```bash
pwsh
```

Pour installer Azure PowerShell, exécutez la commande suivante :

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> Si vous rencontrez une erreur d’autorisations lorsque vous tentez d’installer le module, vous devrez peut-être exécuter PowerShell en mode superutilisateur pour installer les modules.
>
> ```bash
> sudo pwsh
> ```

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez `Yes` ou `Yes to All` pour procéder à l’installation.

## <a name="enable-aliases"></a>Activer les alias

Pour la compatibilité avec le module `AzureRM` existant, le nouveau module `Az` a la possibilité de créer des alias à compatibilité descendante pour les cmdlets `AzureRM`. Avant d’utiliser le module pour la première fois, configurez ces alias avec la commande suivante :

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Cela configure l’alias pour l’utilisateur actuel uniquement. Consultez l’aide de cmdlet pour les autres valeurs qui peuvent être fournies à `-Scope` pour configurer les alias.

> [!NOTE]
> Si vous rencontrez une erreur relative à un emplacement de chemin d’accès, assurez-vous qu’il existe sur votre système local. Pour l’étendue `CurrentUser`, cette erreur peut être résolue en exécutant la commande suivante dans `bash` :
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, vous devez charger `Az` dans votre session PowerShell avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure. L’importation d’un module ne nécessite __pas__ de privilèges élevés.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `Az` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Sur macOS et Linux, vous devez utiliser votre profil via la variable d’environnement `$Profile`. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, voir [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez l’article [Bien démarrer avec Azure PowerShell](get-started-azureps.md).
