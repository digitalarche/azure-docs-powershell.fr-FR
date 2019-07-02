---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 17197b77e26ccf0e41b5faf3cbbde34338b28167
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037723"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="aa15b-103">Désinstaller le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa15b-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="aa15b-104">Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système.</span><span class="sxs-lookup"><span data-stu-id="aa15b-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="aa15b-105">Si vous choisissez de désinstaller complètement Azure PowerShell, faites-nous part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="aa15b-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="aa15b-106">Si vous rencontrez un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème lié à GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="aa15b-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="aa15b-107">Désinstaller Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="aa15b-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="aa15b-108">Si vous avez installé Azure PowerShell via le package MSI, vous devez le désinstaller via le système Windows et non via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa15b-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="aa15b-109">Plateforme</span><span class="sxs-lookup"><span data-stu-id="aa15b-109">Platform</span></span> | <span data-ttu-id="aa15b-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="aa15b-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="aa15b-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="aa15b-111">Windows 10</span></span> | <span data-ttu-id="aa15b-112">Démarrer > Paramètres > Applications</span><span class="sxs-lookup"><span data-stu-id="aa15b-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="aa15b-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa15b-113">Windows 7</span></span> </br><span data-ttu-id="aa15b-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aa15b-114">Windows 8</span></span> | <span data-ttu-id="aa15b-115">Démarrer > Panneau de configuration > Programmes > Désinstaller un programme</span><span class="sxs-lookup"><span data-stu-id="aa15b-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="aa15b-116">Une fois sur l’écran, vous devez voir __Azure PowerShell__ dans la liste des programmes.</span><span class="sxs-lookup"><span data-stu-id="aa15b-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="aa15b-117">Il s’agit de l’application à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="aa15b-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="aa15b-118">Désinstaller à partir de PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa15b-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="aa15b-119">Si vous avez installé Azure PowerShell à l’aide de PowerShellGet, vous pouvez utiliser la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="aa15b-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="aa15b-120">Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module.</span><span class="sxs-lookup"><span data-stu-id="aa15b-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="aa15b-121">Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement.</span><span class="sxs-lookup"><span data-stu-id="aa15b-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="aa15b-122">La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.</span><span class="sxs-lookup"><span data-stu-id="aa15b-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="aa15b-123">Pour vérifier quelles versions d’Azure PowerShell sont actuellement installées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="aa15b-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="aa15b-124">Le script suivant interroge PowerShell Gallery afin d’obtenir une liste de sous-modules dépendants.</span><span class="sxs-lookup"><span data-stu-id="aa15b-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="aa15b-125">Il désinstalle ensuite la bonne version de chaque sous-module.</span><span class="sxs-lookup"><span data-stu-id="aa15b-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="aa15b-126">Vous devez disposer d’un accès administrateur pour exécuter ce script dans une portée autre que `Process` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="aa15b-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="aa15b-127">Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa15b-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="aa15b-128">L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aa15b-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="aa15b-129">Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="aa15b-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="aa15b-130">Pour exécuter le script pour afficher uniquement ce qui serait supprimé, sans le supprimer, utilisez l’option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="aa15b-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="aa15b-131">Si ce script ne trouve pas de correspondance exacte avec une dépendance de même version à désinstaller, _aucune_ version de cette dépendance n’est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="aa15b-131">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="aa15b-132">En effet, d’autres versions du module cible sur votre système reposent peut-être sur ces dépendances.</span><span class="sxs-lookup"><span data-stu-id="aa15b-132">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="aa15b-133">Dans ce cas, les versions disponibles de la dépendance sont listées.</span><span class="sxs-lookup"><span data-stu-id="aa15b-133">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="aa15b-134">Vous pouvez ensuite supprimer les anciennes versions manuellement avec `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="aa15b-134">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="aa15b-135">Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller.</span><span class="sxs-lookup"><span data-stu-id="aa15b-135">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="aa15b-136">Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’AzureRM __à l’exception__ de la plus récente.</span><span class="sxs-lookup"><span data-stu-id="aa15b-136">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
