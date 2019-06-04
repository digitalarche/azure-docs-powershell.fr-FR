---
title: Installer Azure PowerShell sur Windows avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: e05a519fabe41f3c23ffd63a8ceea69a0e58d5e1
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534676"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installer Azure PowerShell sur Windows avec PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Cet article explique les étapes permettant d’installer les modules Azure PowerShell pour PowerShell 5.x dans un environnement Windows à l’aide de PowerShellGet. Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).

Le modèle de déploiement Azure Classic n’est pas pris en charge par cette version d’Azure PowerShell. Pour la prise en charge des déploiements Classic, suivez les instructions dans [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps).

> [!IMPORTANT]
> Le module AzureRM n’est pas pris en charge sur macOS ou Linux. Pour utiliser des applets de commande Azure PowerShell sur ces plateformes, [installez le module Az](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Configuration requise

Pour installer Azure PowerShell, il vous faut la version 1.1.2.0 ou plus récente de PowerShellGet. Pour savoir si elle est disponible sur votre système, exécutez la commande suivante :

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

Vous devez obtenir un graphique similaire à la sortie suivante :

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Si vous devez mettre à jour votre installation de PowerShellGet, exécutez la commande suivante :

```powershell-interactive
Install-Module PowerShellGet -Force
```

Si PowerShellGet n’est pas installé, suivez les instructions dans le tableau ci-dessous pour votre système.

|Scénario|Instructions d’installation|
|---|---|
|Windows 10<br/>Windows Server 2016|Intégré à Windows Management Framework (WMF) 5.0 inclus dans le système d’exploitation|
|Mise à niveau vers PowerShell 5| <ol><li>[Installer la dernière version de WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Exécutez la commande suivante :<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows avec PowerShell 3 ou PowerShell 4|<ol><il>[Obtenir les modules PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Exécutez la commande suivante :<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> L’utilisation de PowerShellGet nécessite une stratégie d’exécution pour exécuter les scripts. Pour plus d’informations sur la stratégie d’exécution de PowerShell, consultez [About Execution Policy](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (À propos des stratégies d’exécution).
>
> [!IMPORTANT]
> Le module décrit dans ce document, AzureRM, utilise .NET Framework. Cela le rend incompatible avec PowerShell 6.0, qui utilise .NET Core. Si vous utilisez PowerShell 6.0, suivez les [instructions d’installation pour macOS et Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Installer le module Azure PowerShell

Il vous faut des privilèges élevés pour installer des modules à partir de PowerShell Gallery. Pour installer Azure PowerShell, exécutez la commande ci-après dans une session avec élévation de privilèges :

```powershell-interactive
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
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez `Yes` ou `Yes to All` pour procéder à l’installation.

Le module `AzureRM` est un module cumulatif pour les cmdlets Azure PowerShell. Son installation permet de télécharger tous les modules Azure Resource Manager disponibles, et rend leurs cmdlets disponibles.

## <a name="sign-in"></a>Se connecter

Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).

## <a name="update-the-azure-powershell-module"></a>Mise à jour du module Azure PowerShell

Vous pouvez mettre à jour votre installation d’Azure PowerShell en exécutant [Update-Module](/powershell/module/powershellget/update-module). Cette commande ne désinstalle __pas__ des versions anciennes.

```powershell-interactive
Update-Module -Name AzureRM
```

Si vous voulez supprimer des versions anciennes d’Azure PowerShell de votre système, consultez [Désinstaller le module Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Utiliser plusieurs versions d’Azure PowerShell

Il est possible d’installer plusieurs versions d’Azure PowerShell. Il vous faudra peut-être plus d’une version si vous travaillez avec des ressources Azure Stack locales, si vous exécutez une version ancienne de Windows impossible à mettre à jour vers PowerShell 5.0, ou si vous utilisez un modèle de déploiement Azure Classic. Pour installer une version ancienne, fournissez l’argument `-RequiredVersion` lors de l’installation.

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

Si vous rencontrez un bogue lors de l’utilisation d’Azure Powershell, veuillez [signaler un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).
Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Étapes suivantes

Pour bien démarrer avec Azure PowerShell, consultez [Démarrer avec Azure PowerShell](get-started-azureps.md) pour en savoir plus sur le module et ses fonctionnalités.
