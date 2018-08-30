---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 92af0fdd8db451e2f0f092d66a3e296ad8d6a09e
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250187"
---
# <a name="uninstall-the-azure-powershell-module"></a>Désinstaller le module Azure PowerShell

Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système. Si vous choisissez de désinstaller complètement Azure PowerShell, pensez à nous faire part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Si vous avez rencontré un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème lié à GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi"></a>Désinstaller MSI

Si vous avez installé Azure PowerShell via le package MSI, vous devez le désinstaller via le système Windows et non via PowerShell.

| Plateforme | Instructions |
|----------|--------------|
| Windows 10 | Démarrer > Paramètres > Applications |
| Windows 7 </br>Windows 8 | Démarrer > Panneau de configuration > Programmes > Désinstaller un programme |

Une fois sur l’écran, vous devez voir « Azure PowerShell » dans la liste des programmes. Vous pouvez le désinstaller depuis cette liste.

## <a name="uninstall-from-powershell"></a>Désinstaller à partir de PowerShell

Si vous avez installé Azure PowerShell à l’aide de PowerShellGet, vous pouvez utiliser la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module. Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement. La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.

Le script suivant peut être utilisé pour supprimer complètement une seule version d’Azure PowerShell. Le script interroge PowerShell Gallery pour obtenir une liste des sous-modules dépendants. Il désinstalle ensuite la bonne version de chaque sous-module.

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell. L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller.
