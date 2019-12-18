---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 7f22a420068db87fa2c3c007bd36f515384162fb
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182228"
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

> [!WARNING]
> Vous __ne pouvez pas__ avoir en même temps les modules AzureRM et Az installés pour PowerShell 5.1 pour Windows installés. Si vous avez besoin de conserver AzureRM disponible sur votre système, installez le module Az pour PowerShell Core 6.x ou ultérieur. Pour cela, [installez PowerShell Core 6.x ou ultérieur](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) et suivez ces instructions dans un terminal PowerShell Core.

La méthode d’installation recommandée consiste seulement à installer pour l’utilisateur actif :

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Si vous souhaitez installer pour tous les utilisateurs d’un système, vous devez avoir des privilèges d’administrateur. À partir d’une session PowerShell avec élévation de privilèges, effectuez l’exécution en tant qu’administrateur ou avec la commande `sudo` sur MacOS ou Linux :

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
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

## <a name="install-offline"></a>Effectuer une installation hors connexion

Dans certains environnements, il n’est pas possible de se connecter à PowerShell Gallery. Dans ce cas, vous pouvez toujours effectuer une installation hors connexion à l’aide de l’une des méthodes suivantes :

* Téléchargez les modules dans un autre emplacement, puis utilisez ce dernier comme source d’installation sur votre réseau. Il peut s’agir d’un processus complexe, mais qui vous permet de mettre en cache les modules PowerShell d’un serveur ou partage de fichiers unique à déployer avec PowerShellGet sur tout système déconnecté. Découvrez comment configurer un dépôt local et l’installer sur des systèmes déconnectés en consultant [Utilisation de dépôts PowerShellGet locaux](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Téléchargez Azure PowerShell MSI](install-az-ps-msi.md) sur un ordinateur connecté au réseau, puis copiez le programme d’installation sur les systèmes ne disposant pas d’un accès à PowerShell Gallery. N’oubliez pas que le programme d’installation MSI ne fonctionne que pour PowerShell 5.1 sur Windows.
* Enregistrez le module avec [Save-module](/powershell/module/PowershellGet/Save-Module) dans un partage de fichiers, ou enregistrez-le dans une autre source et copiez-le manuellement sur d’autres ordinateurs :
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Résolution de problèmes

Voici quelques problèmes courants rencontrés lors de l’installation du module Azure PowerShell. Si vous rencontrez un problème qui n’est pas listé ici, [signalez ce problème sur GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Le proxy bloque la connexion

Si vous recevez des erreurs de `Install-Module` indiquant que PowerShell Gallery est inaccessible, vous êtes peut-être derrière un proxy. Les différents systèmes d’exploitation ont des exigences propres pour la configuration d’un proxy à l’échelle du système, qui ne sont pas abordées en détail ici. Contactez votre administrateur système pour vos paramètres de proxy et pour savoir comment les configurer pour votre système d’exploitation.

PowerShell lui-même peut ne pas être configuré pour utiliser ce proxy automatiquement. Avec PowerShell 5.1 et ultérieur, configurez le proxy à utiliser pour une session PowerShell avec la commande suivante :

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Si vos informations d’identification du système d’exploitation sont configurées correctement, ceci va router les demandes PowerShell via le proxy.
Pour conserver cette configuration entre les sessions, ajoutez la commande à un [profil PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Pour que l’installation du package soit possible, votre proxy doit autoriser les connexions HTTPS à l’adresse suivante :

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Si vous avez désactivé le chargement automatique de modules, importez manuellement le module avec `Import-Module Az`. En raison de la structure du module, cette opération peut prendre quelques secondes.

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Mise à jour du module Azure PowerShell

En raison de la façon dont le module Az est empaqueté, la commande [Update-Module](/powershell/module/powershellget/update-module) ne met pas correctement à jour votre installation. Quand vous installez le module Az, celui-ci collecte et installe en fait tous ses sous-modules dépendants, lesquels fournissent les applets de commande pour chaque service.
Cela signifie que pour mettre à jour le module Azure PowerShell, vous devez faire une __réinstallation__ au lieu d’une simple __mise à jour__. Cette opération s’effectue de la même façon que l’installation, mais il peut être nécessaire d’ajouter l’argument `-Force` :

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
