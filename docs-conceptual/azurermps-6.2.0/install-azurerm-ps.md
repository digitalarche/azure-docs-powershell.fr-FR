---
title: Installer Azure PowerShell avec PowerShellGet
description: Procédure d’installation d’Azure PowerShell avec PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323099"
---
# <a name="install-azure-powershell-with-powershellget"></a>Installer Azure PowerShell avec PowerShellGet

Cet article explique les étapes permettant d’installer les modules Azure PowerShell dans un environnement Windows à l’aide de PowerShellGet.  Il s’agit de la meilleure façon d’installer Azure PowerShell. Toutefois, si vous préférez l’installer avec le package MSI ou Web Platform Installer, consultez [Autres méthodes d’installation](other-install.md).

Si vous voulez utiliser Azure PowerShell sur macOS ou Linux, consultez l’article suivant : [Installer et configurer Azure PowerShell sur macOS et Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Conditions requises pour le système

Azure PowerShell version 6.1.0 requiert la version 5.0 (ou une version ultérieure) de PowerShell. Pour plus d’informations sur la mise à niveau vers PowerShell 5.0, consultez [Mise à niveau du module Windows PowerShell existant](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

PowerShellGet est automatiquement inclus dans PowerShell 5.0.

## <a name="install-or-update-the-azure-powershell-module"></a>Installer ou mettre à jour le module Azure PowerShell

L’installation d’Azure PowerShell à partir de PowerShell Gallery nécessite des privilèges élevés. Exécutez la commande suivante à partir d’une session PowerShell avec élévation de privilèges :

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> Cette commande met à jour toute installation existante d’Azure PowerShell sur votre système. Si vous avez besoin d’installer plusieurs versions, consultez la réponse des FAQ correspondant à la question [Puis-je installer plusieurs versions d’Azure PowerShell ?](#multiple-versions)

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Répondez « Oui » ou « Oui pour tous » pour poursuivre l’installation.

> [!NOTE]
> Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.

Le module AzureRM est un module cumulatif pour les applets de commande Azure Resource Manager. Quand vous installez le module AzureRM, les autres modules Azure PowerShell qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.

## <a name="load-the-azure-powershell-module"></a>Charger le module Azure PowerShell

Une fois le module installé, vous devez le charger dans votre session PowerShell. Vous devez le faire dans une session PowerShell normale (sans élévation de privilèges). Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Signalement de problèmes et envoi de commentaires

Si vous rencontrez des bogues avec l’outil, veuillez [signaler un problème sur GitHub](https://github.com/Azure/azure-powershell/issues). Pour fournir des commentaires à partir de la ligne de commande, utilisez l’applet de commande `Send-Feedback`.

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez les articles suivants :

* [Prise en main d’Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Questions fréquentes (FAQ)

### <a id="helpmechoose"></a>Comment puis-je vérifier la version d’Azure PowerShell ?

Bien que nous vous encouragions à effectuer la mise à niveau vers la version la plus récente dès que possible, plusieurs versions d’Azure PowerShell sont prises en charge. Pour déterminer la version d’Azure PowerShell installée, exécutez `Get-Module AzureRM` à partir de la ligne de commande.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Puis-je utiliser Azure PowerShell pour des déploiements Azure classiques ?

Si vous avez des déploiements qui utilisent le modèle de déploiement Classic, vous pouvez installer la version Service Management d’Azure PowerShell. Pour plus d’informations, consultez [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps). Les modules Azure et AzureRM partagent des dépendances communes. Si vous utilisez des modules Azure et AzureRM, vous devez installer la même version de chaque package.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Puis-je installer plusieurs versions d’Azure PowerShell ?

PowerShellGet est la seule méthode d’installation prenant en charge plusieurs versions. Pour installer plusieurs versions, vous pouvez ajouter le paramètre `-RequiredVersion` à l’applet de commande `Install-Module`. Par exemple, pour installer les versions 6.1.0 et 1.2.9 :

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Une seule version du module peut être chargée dans une session PowerShell. Vous devez ouvrir une nouvelle fenêtre PowerShell et utiliser `Import-Module` pour importer une version spécifique du module Azure PowerShell.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Les versions 2.1.0 et 1.2.6 sont les premières versions de module conçues pour être installées et utilisées côte à côte. Lors du chargement d’une version antérieure d’Azure PowerShell, des versions incompatibles du module **AzureRM.Profile** sont chargées. Ainsi, les applets de commande vous invitent à vous connecter chaque fois que vous exécutez une applet de commande.
