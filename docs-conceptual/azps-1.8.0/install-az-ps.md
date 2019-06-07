---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365744"
---
# <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

Cet article vous indique comment installer les modules Azure PowerShell à l’aide de PowerShellGet. Ces instructions s’appliquent aux plateformes Windows, macOS et Linux. Pour le module Az, actuellement aucune autre méthode d’installation n’est prise en charge.

## <a name="requirements"></a>Configuration requise

Azure PowerShell fonctionne avec PowerShell 5.1 ou ultérieur sur Windows, ou avec PowerShell 6.x et ultérieur sur toutes les plateformes. Si vous n’êtes pas sûr d’avoir PowerShell, ou si vous êtes sur Mac OS ou Linux, [installez la dernière version de PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Pour vérifier votre version de PowerShell, exécutez la commande :

```powershell-interactive
$PSVersionTable.PSVersion
```

Pour exécuter Azure PowerShell dans PowerShell 5.1 sur Windows :

1. Mettrez à jour vers [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) si nécessaire. Si vous êtes sur Windows 10, PowerShell 5.1 est déjà installé.
2. Installez [.NET Framework 4.7.2 ou ultérieur](/dotnet/framework/install).

Il n’existe aucune exigence supplémentaire pour Azure PowerShell lors de l’utilisation de PowerShell Core.

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

En raison de la façon dont le module Az est empaqueté, la commande [Update-Module](/powershell/module/powershellget/update-module) ne met pas correctement à jour votre installation. Techniquement, Az est un métamodule, qui inclut tous les sous-modules contenant des applets de commande pour interagir avec les services Azure. Cela signifie que pour mettre à jour le module Azure PowerShell, vous devez faire une __réinstallation__ au lieu d’une simple __mise à jour__. Cette opération s’effectue de la même façon que l’installation, mais il peut être nécessaire d’ajouter l’argument `-Force` :

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Bien que cela puisse remplacer les modules installés, des versions plus anciennes peuvent néanmoins rester présentes sur votre système.
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
