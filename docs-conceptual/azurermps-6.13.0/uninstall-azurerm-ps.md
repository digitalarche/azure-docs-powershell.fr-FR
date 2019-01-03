---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 7456e45fe9a94d3c1e809dfd075a090448001607
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982813"
---
# <a name="uninstall-the-azure-powershell-module"></a>Désinstaller le module Azure PowerShell

Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système. Si vous choisissez de désinstaller complètement Azure PowerShell, faites-nous part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Si vous rencontrez un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème lié à GitHub](https://github.com/azure/azure-powershell/issues).


## <a name="uninstall-msi"></a>Désinstaller MSI

Si vous avez installé Azure PowerShell via le package MSI, vous devez le désinstaller via le système Windows et non via PowerShell.

| Plateforme | Instructions |
|----------|--------------|
| Windows 10 | Démarrer > Paramètres > Applications |
| Windows 7 </br>Windows 8 | Démarrer > Panneau de configuration > Programmes > Désinstaller un programme |

Une fois sur l’écran, vous devez voir « Azure PowerShell » dans la liste des programmes. Vous pouvez le désinstaller depuis cette liste.

## <a name="uninstall-from-powershell"></a>Désinstaller à partir de PowerShell

Si vous avez installé Azure PowerShell à l’aide de PowerShellGet, vous pouvez utiliser la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module. Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement. La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.

Pour vérifier quelles versions d’Azure PowerShell sont actuellement installées, exécutez la commande suivante :

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
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
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé. Pour exécuter le script pour afficher uniquement ce qui serait supprimé, sans le supprimer, utilisez l’option `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller. Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’AzureRM __à l’exception__ de la plus récente.

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
