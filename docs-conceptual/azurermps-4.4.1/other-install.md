---
title: Autres méthodes d’installation d’Azure PowerShell | Microsoft Docs
description: Comment installer Azure PowerShell à l’aide du package MSI ou de Web Platform Installer.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: 5016c7e768aba94308d0e78785481fafbac36c74
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51275552"
---
# <a name="other-installation-methods"></a>Autres méthodes d’installation

Azure PowerShell peut être installé selon plusieurs méthodes. La méthode recommandée est d’utiliser PowerShellGet avec PowerShell Gallery. Vous pouvez installer Azure PowerShell sur Windows à l’aide de Web Platform Installer (WebPI) ou du fichier MSI disponible sur GitHub.

## <a name="install-on-windows-using-the-web-platform-installer"></a>Installer sur Windows à l’aide de Web Platform Installer

L’installation de la dernière version d’Azure PowerShell à l’aide de WebPI s’effectue de la même façon que pour les versions précédentes.
Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation.

> [!NOTE]
> Si vous aviez précédemment installé les modules Azure à partir de PowerShell Gallery, le programme d’installation les supprime automatiquement. Cette méthode simplifie votre environnement, car elle garantit qu’une seule version d’Azure PowerShell est installée. Toutefois, certains scénarios peuvent nécessiter d’avoir plusieurs versions installées en même temps.
>
> PowerShell Gallery installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`. Le programme d’installation WebPI installe les modules Azure dans `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.
>
> Si une erreur se produit pendant l’installation, vous pouvez supprimer manuellement les dossiers Azure* de votre dossier `$env:ProgramFiles\WindowsPowerShell\Modules`, puis réessayer l’installation.

Une fois l’installation terminée, votre paramètre `$env:PSModulePath` doit inclure les répertoires contenant les applets de commande Azure PowerShell. Vous pouvez exécuter la commande suivante pour vérifier qu’Azure PowerShell a bien été installé.

```powershell-interactive
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> Un problème connu peut se produire quand vous effectuez l’installation à partir de WebPI. Si votre ordinateur nécessite d’être redémarré après des mises à jour du système ou d’autres installations, il se peut que le chemin `$env:PSModulePath` ne soit pas mis à jour avec le chemin d’installation d’Azure PowerShell.

Quand vous essayez de charger ou d’exécuter des applets de commande après l’installation, vous pouvez recevoir le message d’erreur suivant :

```output
PS C:\> Login-AzureRmAccount
Login-AzureRmAccount : The term 'Login-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Login-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Login-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

Vous pouvez résoudre cette erreur en redémarrant l’ordinateur ou en important le module avec le chemin d’accès complet. Par exemple : 

```powershell-interactive
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a>Installer sur Windows à l’aide du package MSI

Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Si vous avez installé des versions antérieures de modules Azure, le programme d’installation les supprime automatiquement. Le package MSI installe les modules dans `$env:ProgramFiles\WindowsPowerShell\Modules`, mais ne crée pas de dossiers spécifiques pour différentes versions.

