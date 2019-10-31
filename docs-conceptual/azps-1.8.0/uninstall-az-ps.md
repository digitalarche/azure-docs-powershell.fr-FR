---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 10/22/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 772667032d421e32c6cd63abbcb686b4eab308e2
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2019
ms.locfileid: "72814346"
---
# <a name="uninstall-the-azure-powershell-module"></a>Désinstaller le module Azure PowerShell

Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système. Si vous choisissez de désinstaller complètement Azure PowerShell, faites-nous part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Si vous avez rencontré un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème GitHub](https://github.com/azure/azure-powershell/issues) pour permettre sa résolution.

## <a name="uninstall-azure-powershell-from-msi"></a>Désinstaller Azure PowerShell à partir de MSI

Si vous avez installé Azure PowerShell via le package MSI, vous devez le désinstaller via le système Windows et non via PowerShell.

| Plateforme | Instructions |
|----------|--------------|
| Windows 10 | Démarrer > Paramètres > Applications |
| Windows 7 </br>Windows 8 | Démarrer > Panneau de configuration > Programmes > Désinstaller un programme |

Une fois sur l’écran, vous devez voir __Azure PowerShell__ dans la liste des programmes. Il s’agit de l’application à désinstaller. Si vous ne voyez pas ce programme, c’est que vous l’avez installé via PowerShellGet. Par conséquent, vous devez suivre les instructions suivantes.

## <a name="uninstall-azure-powershell-from-powershell-get"></a>Désinstaller Azure PowerShell à partir de PowerShellGet

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

<a name="uninstall-script"/>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

> [!NOTE]
> Si ce script ne trouve pas de correspondance exacte avec une dépendance de même version à désinstaller, _aucune_ version de cette dépendance n’est désinstallée. En effet, d’autres versions du module cible sur votre système reposent peut-être sur ces dépendances. Dans ce cas, les versions disponibles de la dépendance sont listées.
> Vous pouvez ensuite supprimer les anciennes versions manuellement avec `Uninstall-Module`.

Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller. Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’Az __à l’exception__ de la plus récente.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Désinstaller le module AzureRM

Si le module Az est installé sur votre système et que vous souhaitez désinstaller AzureRM, il existe deux options qui ne nécessitent pas d’exécuter le script `Uninstall-AllModules` ci-dessus. La méthode à suivre dépend de la façon dont vous avez installé le module AzureRM.
Si vous n’êtes pas sûr de votre méthode d’installation d’origine, suivez d’abord les étapes de désinstallation d’un fichier MSI.

### <a name="uninstall-azure-powershell-msi"></a>Désinstaller Azure PowerShell MSI

Si vous avez installé des modules AzureRM Azure PowerShell via le package MSI, vous devez les désinstaller via le système Windows et non via PowerShell.

| Plateforme | Instructions |
|----------|--------------|
| Windows 10 | Démarrer > Paramètres > Applications |
| Windows 7 </br>Windows 8 | Démarrer > Panneau de configuration > Programmes > Désinstaller un programme |

Une fois sur l’écran, vous devez voir __Azure PowerShell__ dans la liste des programmes. Il s’agit de l’application à désinstaller. Si vous ne voyez pas ce programme, c’est que vous l’avez installé via PowerShellGet. Par conséquent, vous devez suivre les instructions suivantes.

### <a name="uninstall-from-powershell"></a>Désinstaller à partir de PowerShell

Si vous avez installé AzureRM avec PowerShellGet, vous pouvez supprimer les modules avec la commande [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponible dans le module `Az.Accounts`. Cette opération supprime _tous_ les modules AzureRM de votre ordinateur, mais elle nécessite des privilèges d’administrateur.

```powershell-interactive
Uninstall-AzureRm
```

Si vous ne pouvez pas exécuter correctement la commande `Uninstall-AzureRM`, utilisez le script [`Uninstall-AllModules`](#uninstall-script) fourni dans cet article avec l’appel suivant :

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```