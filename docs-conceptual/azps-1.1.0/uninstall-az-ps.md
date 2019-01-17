---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 9d1f1b6550c39b8c65662cf0150f477392747708
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342054"
---
# <a name="uninstall-the-azure-powershell-module"></a>Désinstaller le module Azure PowerShell

Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système. Si vous choisissez de désinstaller complètement Azure PowerShell, faites-nous part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Si vous rencontrez un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème lié à GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-the-az-module"></a>Désinstaller le module Az

Pour désinstaller les modules Az, utilisez la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module. Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement. La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.

Pour vérifier quelles versions d’Azure PowerShell sont actuellement installées, exécutez la commande suivante :

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

Le script suivant interroge PowerShell Gallery afin d’obtenir une liste de sous-modules dépendants. Il désinstalle ensuite la bonne version de chaque sous-module. Vous devez disposer d’un accès administrateur pour exécuter ce script dans une portée autre que `Process` ou `CurrentUser`.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell. L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé. Pour exécuter le script pour afficher uniquement ce qui serait supprimé, sans le supprimer, utilisez l’option `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller. Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’Az __à l’exception__ de la plus récente.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Désinstaller le module AzureRM

Si le module Az est installé sur votre système et que vous souhaitez désinstaller AzureRM, il existe deux options simples qui ne nécessitent pas d’exécuter le script `Uninstall-AllModules` ci-dessus. La méthode à suivre dépend de la façon dont vous avez installé AzureRM.
Si vous n’êtes pas sûr, vérifiez au préalable les étapes de désinstallation de MSI.

### <a name="uninstall-msi"></a>Désinstaller MSI

Si vous avez installé des modules AzureRM Azure PowerShell via le package MSI, vous devez les désinstaller via le système Windows et non via PowerShell.

| Plateforme | Instructions |
|----------|--------------|
| Windows 10 | Démarrer > Paramètres > Applications |
| Windows 7 </br>Windows 8 | Démarrer > Panneau de configuration > Programmes > Désinstaller un programme |

Une fois sur l’écran, vous devez voir « Azure PowerShell » dans la liste des programmes. Vous pouvez le désinstaller depuis cette liste.

### <a name="uninstall-from-powershell"></a>Désinstaller à partir de PowerShell

Si vous avez installé AzureRM à partir de PowerShellGet, vous pouvez supprimer les modules avec la nouvelle commande `Uninstall-AzureRM`. Cette opération supprime _tous_ les modules AzureRM de votre ordinateur, mais elle nécessite des privilèges d’administrateur.

```powershell-interactive
Uninstall-AzureRm
```

Si vous ne pouvez pas exécuter correctement la commande `Uninstall-AzureRM`, utilisez le script `Uninstall-AllModules` fourni dans cet article à la place.