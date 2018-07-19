---
title: Installer et configurer Azure PowerShell | Microsoft Docs
description: Comment installer et configurer Azure PowerShell pour la première utilisation.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 2444abc6f6f2280645c77c3effcd02db74f4f997
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100237"
---
# <a name="install-and-configure-azure-powershell"></a>Installation et configuration d'Azure PowerShell

Cet article explique les étapes permettant d’installer les modules Azure PowerShell dans un environnement Windows.
Si vous voulez utiliser Azure PowerShell sur macOS ou Linux, consultez l’article suivant : [Installer et configurer Azure PowerShell sur macOS et Linux](install-azurermps-maclinux.md).

La méthode recommandée est d’installer Azure PowerShell à partir de PowerShell Gallery.

## <a name="step-1-install-powershellget"></a>Étape 1 : Installer PowerShellGet

Pour installer des éléments à partir de PowerShell Gallery, vous avez besoin du module PowerShellGet. Vérifiez que votre système a la version appropriée de PowerShellGet et qu’il présente toute la configuration requise. Exécutez la commande suivante pour vérifier que PowerShellGet est installé sur votre système.

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Vous devez obtenir un graphique similaire à la sortie suivante :

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Vous avez besoin de PowerShellGet version 1.1.2.0 ou versions ultérieures. Pour mettre à jour PowerShellGet, utilisez la commande suivante :

```powershell
Install-Module PowerShellGet -Force
```

Si PowerShellGet n’est pas installé, consultez la section [Comment obtenir PowerShellGet](#how-to-get-powershellget) dans cet article.

> [!NOTE]
> L’utilisation de PowerShellGet nécessite une stratégie d’exécution pour exécuter les scripts. Pour plus d’informations sur la stratégie d’exécution de PowerShell, consultez [About Execution Policy](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (À propos des stratégies d’exécution).

> [!IMPORTANT]
> Le module décrit dans ce document, AzureRM, utilise .NET Framework. Cela le rend incompatible avec PowerShell 6.0, qui utilise .NET Core. Si vous utilisez PowerShell 6.0, suivez les [instructions d’installation pour macOS et Linux](install-azurermps-maclinux.md). 

## <a name="step-2-install-azure-powershell"></a>Étape 2 : Installer Azure PowerShell

L’installation d’Azure PowerShell à partir de PowerShell Gallery nécessite des privilèges élevés. Exécutez la commande suivante à partir d’une session PowerShell avec élévation de privilèges :

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Par défaut, la galerie PowerShell n’est pas configurée comme un référentiel de confiance pour PowerShellGet. La première fois que vous utilisez PSGallery, le message suivant s’affiche :

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Répondez « Oui » ou « Oui pour tous » pour poursuivre l’installation.

> [!NOTE]
> Si votre version de NuGet est antérieure à 2.8.5.201, vous êtes invité à télécharger et installer la dernière version de NuGet.

Le module AzureRM est un module cumulatif pour les applets de commande Azure Resource Manager. Quand vous installez le module AzureRM, les autres modules Azure qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.

Si vous disposez d’une version précédente d’Azure PowerShell, vous pourriez recevoir une erreur. Pour résoudre ce problème, consultez la section [Mise à jour vers une nouvelle version d’Azure PowerShell](#update-azps) de cet article.

## <a name="step-3-load-the-azurerm-module"></a>Étape 3 : Charger le module AzureRM
Une fois le module installé, vous devez le charger dans votre session PowerShell. Vous devez le faire dans une session PowerShell normale (sans élévation de privilèges). Les modules sont chargés à l’aide de l’applet de commande `Import-Module`, comme suit :

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Étapes suivantes

Pour plus d’informations sur l’utilisation d’Azure PowerShell, consultez les articles suivants :

* [Prise en main d’Azure PowerShell](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Signalement de problèmes et envoi de commentaires

Si vous rencontrez des bogues en utilisant l’outil, signalez un problème dans la section [Issues](https://github.com/Azure/azure-powershell/issues) (Problèmes) de notre référentiel GitHub. Pour fournir des commentaires à partir de la ligne de commande, utilisez l’applet de commande `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Questions fréquentes (FAQ)

### <a name="how-to-get-powershellget"></a>Comment obtenir PowerShellGet

|Version du SE|Instructions d’installation|
|---|---|
|J’ai Windows 10 ou Windows Server 2016|Intégré à Windows Management Framework (WMF) 5.0 inclus dans le système d’exploitation|
|Je veux effectuer la mise à niveau vers PowerShell 5|[Installer la dernière version de WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Mon ordinateur exécute une version de Windows avec PowerShell 3 ou 4|[Obtenir les modules PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Vérification de la version d’Azure PowerShell

Bien que nous vous encouragions à effectuer la mise à niveau vers la version la plus récente dès que possible, plusieurs versions d’Azure PowerShell sont prises en charge. Pour déterminer la version d’Azure PowerShell installée, exécutez `Get-Module AzureRM` à partir de la ligne de commande.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Prise en charge des méthodes de déploiement classiques

Si vous avez des déploiements qui utilisent le modèle de déploiement Classic, vous pouvez installer la version Service Management d’Azure PowerShell. Pour plus d’informations, consultez [Installer le module Azure PowerShell Service Management](/powershell/azure/servicemanagement/install-azure-ps). Les modules Azure et AzureRM partagent des dépendances communes. Si vous utilisez des modules Azure et AzureRM, vous devez installer la même version de chaque package.

### <a id="update-azps"></a>Mise à jour vers une nouvelle version d’Azure PowerShell

Si vous avez une version précédente d’Azure PowerShell installée qui inclut le module Gestion des services, vous pourriez recevoir l’erreur suivante :

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Comme le message d’erreur l’indique, vous devez utiliser le paramètre -AllowClobber pour installer le module. Utilisez la commande suivante :

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Pour plus d’informations, consultez la rubrique pour [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Installation de versions de modules côte à côte

La méthode d’installation avec PowerShellGet est la seule qui prend en charge l’installation de plusieurs versions. Utilisez-la, par exemple, si vous avez des scripts écrits à l’aide d’une version précédente d’Azure PowerShell et que vous n’avez pas le temps ou les ressources pour les mettre à jour. Les commandes suivantes illustrent l’installation de plusieurs versions d’Azure PowerShell :

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Une seule version du module peut être chargée dans une session PowerShell. Vous devez ouvrir une nouvelle fenêtre PowerShell et utiliser `Import-Module` pour importer une version spécifique des applets de commande AzureRM :

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Les versions 2.1.0 et 1.2.6 sont les premières versions de module conçues pour être installées et utilisées côte à côte. Lors du chargement d’une version antérieure d’Azure PowerShell, des versions incompatibles du module **AzureRM.Profile** sont chargées. Ainsi, les applets de commande vous invitent à vous connecter chaque fois que vous exécutez une applet de commande.

### <a name="other-installation-methods"></a>Autres méthodes d’installation

Pour plus d’informations sur l’installation à l’aide de Web Platform Installer ou du package MSI, consultez [Autres méthodes d’installation](other-install.md)
