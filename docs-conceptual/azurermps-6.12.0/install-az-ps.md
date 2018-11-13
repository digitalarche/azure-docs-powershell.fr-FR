---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51276038"
---
# <a name="install-azure-powershell-with-powershellget"></a>Installer Azure PowerShell avec PowerShellGet

Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet. Pour la version préliminaire Az, aucune autre méthode d’installation n’est prise en charge. 

## <a name="requirements"></a>Configuration requise

Azure PowerShell fonctionne avec PowerShell 5.x sur Windows ou PowerShell 6.x sur n’importe quelle plateforme. Pour vérifier la version de PowerShell que vous exécutez sur votre machine, utilisez la commande suivante :

```powershell-interactive
$PSVersionTable.PSVersion
```

Si vous possédez une version obsolète ou que vous avez besoin d’installer PowerShell consultez [Installer plusieurs versions de PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). Les informations d’installation de votre plateforme sont liées à partir de cette page.

## <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

> [!IMPORTANT]
>
> Nous vous déconseillons d’avoir les modules `AzureRM` et `Az` installés sur un système en même temps. Pour installer le module `Az`, il faut désinstaller `AzureRM`. Pour obtenir des instructions sur la marche à suivre, consultez [Désinstaller le module Azure PowerShell (AzureRM)](uninstall-azurerm-ps.md).

Pour installer des modules sur une étendue globale, il vous faut des privilèges élevés pour pouvoir installer des modules à partir de PowerShell Gallery. Pour installer Azure PowerShell, exécutez la commande suivante dans une session avec élévation de privilèges (« Exécuter en tant qu’administrateur » sur Windows, ou avec des privilèges de superutilisateur sur macOS ou Linux) :

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Si vous n’avez pas accès aux privilèges d’administrateur, vous pouvez en installer pour l’utilisateur actuel en ajoutant l’argument `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez `Yes` ou `Yes to All` pour procéder à l’installation.

Le module `Az` est un module cumulatif pour les cmdlets Azure PowerShell. Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, vous devez charger `Az` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `Az` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, voir [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Mise à jour du module Azure PowerShell

Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module). Cette commande ne désinstalle __pas__ des versions anciennes.

```powershell-interactive
Update-Module -Name Az
```

Si vous voulez supprimer des versions anciennes d’Azure PowerShell de votre système, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Utiliser plusieurs versions d’Azure PowerShell

Il est possible d’installer plusieurs versions d’Azure PowerShell. Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).

Vous pouvez charger une version spécifique du module `Az` à l’aide de l’argument `-RequiredVersion` avec `Install-Module` ou `Import-Module` :

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Si vous avez plus d’une version du module installé, la version la plus récente est chargée par défaut lors de l’importation.

## <a name="provide-feedback"></a>Fournir des commentaires

Si vous rencontrez un bogue lors de l’utilisation d’Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).
Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).

## <a name="next-steps"></a>Étapes suivantes

Pour bien démarrer avec Azure PowerShell, consultez [Démarrer avec Azure PowerShell](get-started-azureps.md) pour en savoir plus sur le module et ses fonctionnalités.