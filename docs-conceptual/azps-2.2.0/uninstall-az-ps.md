---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: eaabd8014368f7ea8f4c9504e58d920dad8a6518
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498622"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="a3dee-103">Désinstaller le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3dee-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="a3dee-104">Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système.</span><span class="sxs-lookup"><span data-stu-id="a3dee-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="a3dee-105">Si vous choisissez de désinstaller complètement Azure PowerShell, faites-nous part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="a3dee-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="a3dee-106">Si vous avez rencontré un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème GitHub](https://github.com/azure/azure-powershell/issues) pour permettre sa résolution.</span><span class="sxs-lookup"><span data-stu-id="a3dee-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="a3dee-107">Désinstaller le module Az</span><span class="sxs-lookup"><span data-stu-id="a3dee-107">Uninstall the Az module</span></span>

<span data-ttu-id="a3dee-108">Pour désinstaller les modules Az, utilisez la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="a3dee-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="a3dee-109">Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module.</span><span class="sxs-lookup"><span data-stu-id="a3dee-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="a3dee-110">Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement.</span><span class="sxs-lookup"><span data-stu-id="a3dee-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="a3dee-111">La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.</span><span class="sxs-lookup"><span data-stu-id="a3dee-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="a3dee-112">Pour vérifier quelles versions d’Azure PowerShell sont actuellement installées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a3dee-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

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

<span data-ttu-id="a3dee-113">Le script suivant interroge PowerShell Gallery afin d’obtenir une liste de sous-modules dépendants.</span><span class="sxs-lookup"><span data-stu-id="a3dee-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="a3dee-114">Il désinstalle ensuite la bonne version de chaque sous-module.</span><span class="sxs-lookup"><span data-stu-id="a3dee-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="a3dee-115">Vous devez disposer d’un accès administrateur pour exécuter ce script dans une portée autre que `Process` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="a3dee-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="a3dee-116">Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a3dee-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="a3dee-117">L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a3dee-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="a3dee-118">Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="a3dee-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="a3dee-119">Pour exécuter le script pour afficher uniquement ce qui serait supprimé, sans le supprimer, utilisez l’option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="a3dee-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="a3dee-120">Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller.</span><span class="sxs-lookup"><span data-stu-id="a3dee-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="a3dee-121">Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’Az __à l’exception__ de la plus récente.</span><span class="sxs-lookup"><span data-stu-id="a3dee-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="a3dee-122">Désinstaller le module AzureRM</span><span class="sxs-lookup"><span data-stu-id="a3dee-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="a3dee-123">Si le module Az est installé sur votre système et que vous souhaitez désinstaller AzureRM, il existe deux options qui ne nécessitent pas d’exécuter le script `Uninstall-AllModules` ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a3dee-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="a3dee-124">La méthode à suivre dépend de la façon dont vous avez installé le module AzureRM.</span><span class="sxs-lookup"><span data-stu-id="a3dee-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="a3dee-125">Si vous n’êtes pas sûr de votre méthode d’installation d’origine, suivez d’abord les étapes de désinstallation d’un fichier MSI.</span><span class="sxs-lookup"><span data-stu-id="a3dee-125">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="a3dee-126">Désinstaller Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="a3dee-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="a3dee-127">Si vous avez installé des modules AzureRM Azure PowerShell via le package MSI, vous devez les désinstaller via le système Windows et non via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a3dee-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="a3dee-128">Plateforme</span><span class="sxs-lookup"><span data-stu-id="a3dee-128">Platform</span></span> | <span data-ttu-id="a3dee-129">Instructions</span><span class="sxs-lookup"><span data-stu-id="a3dee-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="a3dee-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a3dee-130">Windows 10</span></span> | <span data-ttu-id="a3dee-131">Démarrer > Paramètres > Applications</span><span class="sxs-lookup"><span data-stu-id="a3dee-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="a3dee-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a3dee-132">Windows 7</span></span> </br><span data-ttu-id="a3dee-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3dee-133">Windows 8</span></span> | <span data-ttu-id="a3dee-134">Démarrer > Panneau de configuration > Programmes > Désinstaller un programme</span><span class="sxs-lookup"><span data-stu-id="a3dee-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="a3dee-135">Une fois sur l’écran, vous devez voir __Azure PowerShell__ dans la liste des programmes.</span><span class="sxs-lookup"><span data-stu-id="a3dee-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="a3dee-136">Il s’agit de l’application à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="a3dee-136">This is the app to uninstall.</span></span> <span data-ttu-id="a3dee-137">Si vous ne voyez pas ce programme, c’est que vous l’avez installé via PowerShellGet. Par conséquent, vous devez suivre les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3dee-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="a3dee-138">Désinstaller à partir de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a3dee-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="a3dee-139">Si vous avez installé AzureRM avec PowerShellGet, vous pouvez supprimer les modules avec la commande [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponible dans le module `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="a3dee-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="a3dee-140">Cette opération supprime _tous_ les modules AzureRM de votre ordinateur, mais elle nécessite des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="a3dee-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="a3dee-141">Si vous ne pouvez pas exécuter correctement la commande `Uninstall-AzureRM`, utilisez le script [`Uninstall-AllModules`](#uninstall-script) fourni dans cet article avec l’appel suivant :</span><span class="sxs-lookup"><span data-stu-id="a3dee-141">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```