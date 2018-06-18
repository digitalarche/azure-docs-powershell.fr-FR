---
title: Autres méthodes d’installation d’Azure PowerShell
description: Comment installer Azure PowerShell à l’aide du package MSI ou de Web Platform Installer.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323320"
---
# <a name="other-installation-methods"></a>Autres méthodes d’installation

Cet article explique comment installer Azure PowerShell à l’aide d’un fichier MSI ou d’un Web Platform Installer (WebPI). Vous pouvez également exécuter Azure PowerShell depuis un conteneur Docker. Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système. L’installation canonique d’Azure PowerShell s’effectue via PowerShellGet. Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).

Pour une installation sur des environnements Linux ou macOS, consultez [Installer Azure PowerShell sur macOS ou Linux](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Installer ou mettre à jour sur Windows à l’aide de Web Platform Installer

L’installation de la dernière version d’Azure PowerShell à l’aide de WebPI s’effectue de la même façon que pour les versions précédentes.
Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation.

> [!NOTE]
> Si vous aviez précédemment installé les modules Azure à partir de PowerShell Gallery, le programme d’installation les supprime automatiquement. Cette méthode simplifie votre environnement, car elle garantit qu’une seule version d’Azure PowerShell est installée. Toutefois, certains scénarios peuvent nécessiter d’avoir plusieurs versions installées en même temps.
>
> PowerShell Gallery installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`. Le programme d’installation WebPI installe les modules Azure dans `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Si une erreur se produit pendant l’installation, vous pouvez supprimer manuellement les dossiers `Azure*` de votre dossier `$env:ProgramFiles\WindowsPowerShell\Modules`, puis réessayer l’installation.

Une fois l’installation terminée, votre paramètre `$env:PSModulePath` doit inclure les répertoires contenant les applets de commande Azure PowerShell. Vous pouvez exécuter la commande suivante pour vérifier qu’Azure PowerShell a bien été installé :

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Un problème connu peut se produire quand vous effectuez l’installation à partir de WebPI. Si votre ordinateur nécessite d’être redémarré après des mises à jour du système ou d’autres installations, il se peut que le chemin `$env:PSModulePath` ne soit pas mis à jour avec le chemin d’installation d’Azure PowerShell.

Quand vous essayez de charger ou d’exécuter des applets de commande après l’installation, vous pouvez recevoir le message d’erreur suivant :

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Vous pouvez résoudre cette erreur en redémarrant l’ordinateur ou en important le module avec le chemin d’accès complet.

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installer ou mettre à jour sur Windows à l’aide du package MSI

Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://aka.ms/azps-release). Si vous avez installé des versions antérieures de modules Azure, le programme d’installation les supprime automatiquement. Le package MSI installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`, mais ne crée pas de dossiers spécifiques pour différentes versions.

## <a name="run-in-a-docker-container"></a>Exécution dans un conteneur Docker

Nous tenons à jour un ensemble d’images Docker préconfigurées avec Azure Powershell. Il existe deux types de conteneurs disponibles : ceux exécutant PowerShell de manière classique sur Windows et un conteneur exécutant PowerShell Core sur Windows ou Linux.

| Environnement | Image Docker |
|-------------|--------------|
| PowerShell sur Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core sur Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core sur Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Pour exécuter une de ces conteneurs, vous utilisez `docker run -it $ImageName` pour obtenir un terminal interactif. Par exemple, pour exécuter PowerShell Core sur le conteneur Linux, utilisez :

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Pour exécuter un conteneur Windows dans Docker, votre système d’exploitation hôte doit être Windows et Docker doit être défini de manière à exécuter des conteneurs Windows. Pour en savoir plus sur le basculement entre des environnements Windows et Linux dans Docker, consultez la documentation Docker [Basculer entre les conteneurs Windows et Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).