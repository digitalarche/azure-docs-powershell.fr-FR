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
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062052"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="cd8dd-103">Désinstaller le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd8dd-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="cd8dd-104">Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="cd8dd-105">Si vous choisissez de désinstaller complètement Azure PowerShell, faites-nous part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="cd8dd-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="cd8dd-106">Si vous avez rencontré un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème GitHub](https://github.com/azure/azure-powershell/issues) pour permettre sa résolution.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="cd8dd-107">Désinstaller Azure PowerShell à partir de MSI</span><span class="sxs-lookup"><span data-stu-id="cd8dd-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="cd8dd-108">Si vous avez installé Azure PowerShell via le package MSI, vous devez le désinstaller via le système Windows et non via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="cd8dd-109">Plateforme</span><span class="sxs-lookup"><span data-stu-id="cd8dd-109">Platform</span></span> | <span data-ttu-id="cd8dd-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="cd8dd-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="cd8dd-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd8dd-111">Windows 10</span></span> | <span data-ttu-id="cd8dd-112">Démarrer > Paramètres > Applications</span><span class="sxs-lookup"><span data-stu-id="cd8dd-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="cd8dd-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd8dd-113">Windows 7</span></span> </br><span data-ttu-id="cd8dd-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd8dd-114">Windows 8</span></span> | <span data-ttu-id="cd8dd-115">Démarrer > Panneau de configuration > Programmes > Désinstaller un programme</span><span class="sxs-lookup"><span data-stu-id="cd8dd-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="cd8dd-116">Une fois sur l’écran, vous devez voir __Azure PowerShell__ dans la liste des programmes.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="cd8dd-117">Il s’agit de l’application à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-117">This is the app to uninstall.</span></span> <span data-ttu-id="cd8dd-118">Si vous ne voyez pas ce programme, c’est que vous l’avez installé via PowerShellGet. Par conséquent, vous devez suivre les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="cd8dd-119">Désinstaller Azure PowerShell à partir de PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="cd8dd-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="cd8dd-120">Pour désinstaller les modules Az, utilisez la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="cd8dd-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="cd8dd-121">Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="cd8dd-122">Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="cd8dd-123">La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="cd8dd-124">Pour vérifier quelles versions d’Azure PowerShell sont actuellement installées, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="cd8dd-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

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

<span data-ttu-id="cd8dd-125">Le script suivant interroge PowerShell Gallery afin d’obtenir une liste de sous-modules dépendants.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="cd8dd-126">Il désinstalle ensuite la bonne version de chaque sous-module.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="cd8dd-127">Vous devez disposer d’un accès administrateur pour exécuter ce script dans une portée autre que `Process` ou `CurrentUser`.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="cd8dd-128">Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="cd8dd-129">L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="cd8dd-130">Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="cd8dd-131">Pour exécuter le script pour afficher uniquement ce qui serait supprimé, sans le supprimer, utilisez l’option `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="cd8dd-132">Si ce script ne trouve pas de correspondance exacte avec une dépendance de même version à désinstaller, _aucune_ version de cette dépendance n’est désinstallée.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="cd8dd-133">En effet, d’autres versions du module cible sur votre système reposent peut-être sur ces dépendances.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="cd8dd-134">Dans ce cas, les versions disponibles de la dépendance sont listées.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="cd8dd-135">Vous pouvez ensuite supprimer les anciennes versions manuellement avec `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="cd8dd-136">Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="cd8dd-137">Pour des raisons pratiques, le script suivant désinstallera toutes les versions d’Az __à l’exception__ de la plus récente.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="cd8dd-138">Désinstaller le module AzureRM</span><span class="sxs-lookup"><span data-stu-id="cd8dd-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="cd8dd-139">Si le module Az est installé sur votre système et que vous souhaitez désinstaller AzureRM, il existe deux options qui ne nécessitent pas d’exécuter le script `Uninstall-AllModules` ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="cd8dd-140">La méthode à suivre dépend de la façon dont vous avez installé le module AzureRM.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="cd8dd-141">Si vous n’êtes pas sûr de votre méthode d’installation d’origine, suivez d’abord les étapes de désinstallation d’un fichier MSI.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="cd8dd-142">Désinstaller Azure PowerShell MSI</span><span class="sxs-lookup"><span data-stu-id="cd8dd-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="cd8dd-143">Si vous avez installé des modules AzureRM Azure PowerShell via le package MSI, vous devez les désinstaller via le système Windows et non via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="cd8dd-144">Plateforme</span><span class="sxs-lookup"><span data-stu-id="cd8dd-144">Platform</span></span> | <span data-ttu-id="cd8dd-145">Instructions</span><span class="sxs-lookup"><span data-stu-id="cd8dd-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="cd8dd-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd8dd-146">Windows 10</span></span> | <span data-ttu-id="cd8dd-147">Démarrer > Paramètres > Applications</span><span class="sxs-lookup"><span data-stu-id="cd8dd-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="cd8dd-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd8dd-148">Windows 7</span></span> </br><span data-ttu-id="cd8dd-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd8dd-149">Windows 8</span></span> | <span data-ttu-id="cd8dd-150">Démarrer > Panneau de configuration > Programmes > Désinstaller un programme</span><span class="sxs-lookup"><span data-stu-id="cd8dd-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="cd8dd-151">Une fois sur cet écran, vous devez voir __Azure PowerShell__ ou __Microsoft Azure PowerShell - Month Year__ dans la liste des programmes.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-151">Once on this screen you should see __Azure PowerShell__ or __Microsoft Azure PowerShell - Month Year__ in the program listing.</span></span> <span data-ttu-id="cd8dd-152">Il s’agit de l’application à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-152">This is the app to uninstall.</span></span> <span data-ttu-id="cd8dd-153">Si vous ne voyez pas ce programme, c’est que vous l’avez installé via PowerShellGet. Par conséquent, vous devez suivre les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="cd8dd-154">Désinstaller à partir de PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd8dd-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="cd8dd-155">Si vous avez installé AzureRM avec PowerShellGet, vous pouvez supprimer les modules avec la commande [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponible dans le module `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="cd8dd-156">Cette opération supprime _tous_ les modules AzureRM de votre ordinateur, mais elle nécessite des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="cd8dd-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="cd8dd-157">Si vous ne pouvez pas exécuter correctement la commande `Uninstall-AzureRM`, utilisez le script [`Uninstall-AllModules`](#uninstall-script) fourni dans cet article avec l’appel suivant :</span><span class="sxs-lookup"><span data-stu-id="cd8dd-157">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
