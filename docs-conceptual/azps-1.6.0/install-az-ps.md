---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475329"
---
# <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet. Ces instructions s’appliquent aux plateformes Windows, macOS et Linux. Pour le module Az, actuellement aucune autre méthode d’installation n’est prise en charge.

## <a name="requirements"></a>Configuration requise

Azure PowerShell fonctionne avec PowerShell version 5.1.x ou ultérieure sur Windows, et avec PowerShell 6 sur n’importe quelle plateforme.
Pour vérifier votre version de PowerShell, exécutez la commande :

```powershell-interactive
$PSVersionTable.PSVersion
```

Si vous possédez une version obsolète ou que vous avez besoin d’installer PowerShell consultez [Installer plusieurs versions de PowerShell](/powershell/scripting/setup/installing-powershell). Les informations d’installation de votre plateforme sont liées à partir de cette page.

Si vous utilisez PowerShell 5 sur Windows, vous devez également avoir installé .NET Framework 4.7.2. Pour obtenir des instructions sur la mise à jour ou l’installation d’une nouvelle version de .NET Framework, consultez le [guide d’installation de .NET Framework](/dotnet/framework/install).

## <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

> [!IMPORTANT]
>
> Les modules AzureRM et Az peuvent être installés en même temps. Si c’est le cas, __n’activez pas les alias__.
> L’activation des alias entraînera des conflits entre les cmdlets AzureRM et les alias de commande Az, et peut entraîner des comportements inattendus.
> Nous vous recommandons de désinstaller AzureRM avant d’installer le module Az. Vous pouvez désinstaller AzureRM ou activer les alias à tout moment. Pour en savoir plus sur les alias de commande AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).
> Pour obtenir des instructions sur la désinstallation, consultez l’article [Désinstaller le module AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module). 

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

Le module Az est un module cumulatif pour les cmdlets Azure PowerShell. Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`. En raison de la structure du module, cette opération peut prendre quelques secondes.

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Mise à jour du module Azure PowerShell

Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module). Cette commande ne désinstalle __pas__ les anciennes versions.

```powershell-interactive
Update-Module -Name Az
```

Pour savoir comment supprimer d’anciennes versions d’Azure PowerShell de votre système, consultez l’article [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Utiliser plusieurs versions d’Azure PowerShell

Il est possible d’installer plusieurs versions d’Azure PowerShell. Pour vérifier si plusieurs versions d’Azure PowerShell sont installées, utilisez la commande suivante :

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Pour supprimer une version d’Azure PowerShell, consultez [Désinstaller le module Azure PowerShell](uninstall-az-ps.md).

Vous pouvez installer ou charger une version spécifique du module `Az` à l’aide de l’argument `-RequiredVersion` :

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Si plusieurs versions du module sont installées, la version la plus récente est chargée par défaut par `Import-Module` et le chargement automatique de module.

## <a name="provide-feedback"></a>Fournir des commentaires

Si vous rencontrez un bogue dans Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).
Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Étapes suivantes

Pour en savoir plus sur les modules PowerShell et leurs fonctionnalités, consultez l’article sur la [prise en main d’Azure PowerShell](get-started-azureps.md).
Si vous êtes familiarisé avec Azure PowerShell et devez effectuer une migration depuis AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).
