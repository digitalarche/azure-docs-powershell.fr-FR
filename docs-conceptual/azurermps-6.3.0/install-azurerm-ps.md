---
title: Installer Azure PowerShell sur Windows avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 0d8019a7acaf2ba3baaa0772a76285ec497c991c
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091467"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installer Azure PowerShell sur Windows avec PowerShellGet

Cet article explique les étapes permettant d’installer les modules Azure PowerShell dans un environnement Windows à l’aide de PowerShellGet. Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).

Pour obtenir des instructions sur l’installation d’Azure PowerShell sur d’autres plateformes, consultez [Installation et configuration d’Azure PowerShell sur macOS et Linux](install-azurermps-maclinux.md).

Le modèle de déploiement Azure Classic n’est pas pris en charge par cette version d’Azure PowerShell. Pour la prise en charge des déploiements Classic, suivez les instructions dans [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).

## <a name="requirements"></a>Configuration requise

À compter de la version 6.0, Azure PowerShell nécessite la version 5.0 ou une version plus récente de PowerShell sur Windows. Pour vérifier la version de PowerShell que vous exécutez sur votre machine, utilisez la commande suivante :

```powershell
$PSVersionTable.PSVersion
```

Si votre version est obsolète, consultez [Mise à niveau des instances Windows PowerShell existantes](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

## <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

Il vous faut des privilèges élevés pour installer des modules à partir de PowerShell Gallery. Pour installer Azure PowerShell, exécutez la commande ci-après dans une session avec élévation de privilèges :

```powershell
Install-Module -Name AzureRM
```

> [!NOTE]
> Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez `Yes` ou `Yes to All` pour procéder à l’installation.

Le module `AzureRM` est un module cumulatif pour les cmdlets PowerShell. Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d'identification Azure.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d'identification d’utilisateur sur plusieurs sessions PowerShell).

## <a name="update-the-azure-powershell-module"></a>Mise à jour du module Azure PowerShell

Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module). Cette commande ne désinstalle __pas__ des versions anciennes.

```powershell
Update-Module -Name AzureRM
```

Si vous voulez supprimer des versions anciennes d’Azure PowerShell de votre système, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Utiliser plusieurs versions d’Azure PowerShell

Il est possible d’installer plusieurs versions d’Azure PowerShell. Il vous faudra peut-être plus d’une version si vous travaillez avec des ressources Azure Stack locales, si vous exécutez une version ancienne de Windows impossible à mettre à jour vers PowerShell 5.0, ou si vous utilisez un modèle de déploiement Azure Classic. Pour installer une version ancienne, fournissez l’argument `-RequiredVersion` lors de l’installation.

```powershell
# Install version 1.2.9 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Lors du chargement du module Azure PowerShell, la version ancienne est chargée par défaut. Pour charger une autre version, fournissez l’argument `-RequiredVersion`.

```powershell
# Load version 1.2.9 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

## <a name="provide-feedback"></a>Fournir des commentaires

Si vous rencontrez un bogue lors de l’utilisation d’Azure Powershell, veuillez [signaler un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).
Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Étapes suivantes

Pour bien démarrer avec Azure PowerShell, consultez [Démarrer avec Azure PowerShell](get-started-azureps.md) pour en savoir plus sur le module et ses fonctionnalités.