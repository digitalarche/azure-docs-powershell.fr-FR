---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037699"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="46dd4-103">Désinstaller le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="46dd4-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="46dd4-104">Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système.</span><span class="sxs-lookup"><span data-stu-id="46dd4-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="46dd4-105">Si vous choisissez de désinstaller complètement Azure PowerShell, pensez à nous faire part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="46dd4-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="46dd4-106">Si vous avez rencontré un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème lié à GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="46dd4-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="46dd4-107">Désinstaller MSI ou Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="46dd4-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="46dd4-108">Si vous avez installé Azure PowerShell via le package MSI ou Web Platform Installer, vous devez le désinstaller via le système Windows et non via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46dd4-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="46dd4-109">Plateforme</span><span class="sxs-lookup"><span data-stu-id="46dd4-109">Platform</span></span> | <span data-ttu-id="46dd4-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="46dd4-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="46dd4-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="46dd4-111">Windows 10</span></span> | <span data-ttu-id="46dd4-112">Démarrer > Paramètres > Applications</span><span class="sxs-lookup"><span data-stu-id="46dd4-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="46dd4-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46dd4-113">Windows 7</span></span> </br><span data-ttu-id="46dd4-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="46dd4-114">Windows 8</span></span> | <span data-ttu-id="46dd4-115">Démarrer > Panneau de configuration > Programmes > Désinstaller un programme</span><span class="sxs-lookup"><span data-stu-id="46dd4-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="46dd4-116">Une fois sur l’écran, vous devez voir « Azure PowerShell » dans la liste des programmes. Vous pouvez le désinstaller depuis cette liste.</span><span class="sxs-lookup"><span data-stu-id="46dd4-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="46dd4-117">Désinstaller à partir de PowerShell</span><span class="sxs-lookup"><span data-stu-id="46dd4-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="46dd4-118">Si vous avez installé Azure PowerShell à l’aide de PowerShellGet, vous pouvez utiliser la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="46dd4-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="46dd4-119">Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module.</span><span class="sxs-lookup"><span data-stu-id="46dd4-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="46dd4-120">Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement.</span><span class="sxs-lookup"><span data-stu-id="46dd4-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="46dd4-121">La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.</span><span class="sxs-lookup"><span data-stu-id="46dd4-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="46dd4-122">Le script suivant peut être utilisé pour supprimer complètement une seule version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46dd4-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="46dd4-123">Le script interroge PowerShell Gallery pour obtenir une liste des sous-modules dépendants.</span><span class="sxs-lookup"><span data-stu-id="46dd4-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="46dd4-124">Il désinstalle ensuite la bonne version de chaque sous-module.</span><span class="sxs-lookup"><span data-stu-id="46dd4-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="46dd4-125">Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46dd4-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="46dd4-126">L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46dd4-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="46dd4-127">Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="46dd4-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="46dd4-128">Pour exécuter le script pour afficher uniquement ce qui serait supprimé, sans le supprimer, utilisez l’option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="46dd4-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="46dd4-129">Si ce script ne trouve pas de correspondance exacte avec une dépendance de même version à désinstaller, _aucune_ version de cette dépendance n’est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="46dd4-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="46dd4-130">En effet, d’autres versions du module cible sur votre système reposent peut-être sur ces dépendances.</span><span class="sxs-lookup"><span data-stu-id="46dd4-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="46dd4-131">Dans ce cas, les versions disponibles de la dépendance sont listées.</span><span class="sxs-lookup"><span data-stu-id="46dd4-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="46dd4-132">Vous pouvez ensuite supprimer les anciennes versions manuellement avec `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="46dd4-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="46dd4-133">Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller.</span><span class="sxs-lookup"><span data-stu-id="46dd4-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="46dd4-134">Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’AzureRM __à l’exception__ de la plus récente.</span><span class="sxs-lookup"><span data-stu-id="46dd4-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
