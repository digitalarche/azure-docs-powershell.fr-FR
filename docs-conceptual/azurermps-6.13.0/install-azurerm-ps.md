---
title: Installer Azure PowerShell sur Windows avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 97f79c01cce90d92febfd9d36f9c112918b48599
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982808"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installer Azure PowerShell sur Windows avec PowerShellGet

Cet article explique les étapes permettant d’installer les modules Azure PowerShell pour PowerShell 5.x dans un environnement Windows à l’aide de PowerShellGet. Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).

Pour obtenir des instructions sur l’installation d’Azure PowerShell sur d’autres plateformes, consultez [Installation et configuration d’Azure PowerShell sur macOS et Linux](install-azurermps-maclinux.md).

Le modèle de déploiement Azure Classic n’est pas pris en charge par cette version d’Azure PowerShell. Pour la prise en charge des déploiements Classic, suivez les instructions dans [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).

## <a name="requirements"></a>Configuration requise

À partir de Azure PowerShell version 6.0, Azure PowerShell requiert PowerShell version 5.0. Pour vérifier la version de PowerShell que vous exécutez sur votre machine, utilisez la commande suivante :

```powershell-interactive
$PSVersionTable.PSVersion
```

Si votre version est obsolète, consultez [Mise à niveau des instances Windows PowerShell existantes](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

> [!IMPORTANT]
> Le module décrit dans ce document, AzureRM, utilise .NET Framework. Cela le rend incompatible avec PowerShell 6.0, qui utilise .NET Core. Si vous utilisez PowerShell 6.0, suivez les [instructions d’installation pour macOS et Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

Il vous faut des privilèges élevés pour installer des modules à partir de PowerShell Gallery. Pour installer Azure PowerShell, exécutez la commande ci-après dans une session avec élévation de privilèges :

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez `Yes` ou `Yes to All` pour procéder à l’installation.

Le module `AzureRM` est un module cumulatif pour les cmdlets Azure PowerShell. Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module AzureRM`. En raison de la structure du module, cette opération peut prendre quelques secondes.


Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Mise à jour du module Azure PowerShell

Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module). Cette commande ne désinstalle __pas__ des versions anciennes.

```powershell-interactive
Update-Module -Name AzureRM
```

Si vous voulez supprimer des versions anciennes d’Azure PowerShell de votre système, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Utiliser plusieurs versions d’Azure PowerShell

Il est possible d’installer plusieurs versions d’Azure PowerShell. Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).

Il vous faudra peut-être plus d’une version si vous travaillez avec des ressources Azure Stack locales, si vous exécutez une version plus ancienne de Windows, ou si vous utilisez un modèle de déploiement classique Azure. Pour installer une version ancienne, fournissez l’argument `-RequiredVersion` lors de l’installation.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Lors du chargement du module Azure PowerShell, la version ancienne est chargée par défaut. Pour charger une autre version, fournissez l’argument `-RequiredVersion`.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Fournir des commentaires

Si vous rencontrez un bogue lors de l’utilisation d’Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).
Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Étapes suivantes

Pour bien démarrer avec Azure PowerShell, consultez [Démarrer avec Azure PowerShell](get-started-azureps.md) pour en savoir plus sur le module et ses fonctionnalités.
