---
title: Désinstaller Azure PowerShell
description: Procédure de désinstallation complète d’Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 3828a6f9d60a68c2837cc201a50d8707324f4f0a
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587225"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d6a19-103">Désinstaller le module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6a19-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="d6a19-104">Cet article vous explique comment désinstaller une ancienne version d’Azure PowerShell, ou comment la supprimer complètement de votre système.</span><span class="sxs-lookup"><span data-stu-id="d6a19-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d6a19-105">Si vous choisissez de désinstaller complètement Azure PowerShell, pensez à nous faire part de vos commentaires via la cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="d6a19-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="d6a19-106">Si vous avez rencontré un bogue, nous vous serions reconnaissants de bien vouloir [signaler un problème lié à GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d6a19-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="d6a19-107">Désinstaller MSI ou Web Platform Installer</span><span class="sxs-lookup"><span data-stu-id="d6a19-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="d6a19-108">Si vous avez installé Azure PowerShell via le package MSI ou Web Platform Installer, vous devez le désinstaller via le système Windows et non via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6a19-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="d6a19-109">Plateforme</span><span class="sxs-lookup"><span data-stu-id="d6a19-109">Platform</span></span> | <span data-ttu-id="d6a19-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="d6a19-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="d6a19-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d6a19-111">Windows 10</span></span> | <span data-ttu-id="d6a19-112">Démarrer > Paramètres > Applications</span><span class="sxs-lookup"><span data-stu-id="d6a19-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="d6a19-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6a19-113">Windows 7</span></span> </br><span data-ttu-id="d6a19-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d6a19-114">Windows 8</span></span> | <span data-ttu-id="d6a19-115">Démarrer > Panneau de configuration > Programmes > Désinstaller un programme</span><span class="sxs-lookup"><span data-stu-id="d6a19-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d6a19-116">Une fois sur l’écran, vous devez voir « Azure PowerShell » dans la liste des programmes. Vous pouvez le désinstaller depuis cette liste.</span><span class="sxs-lookup"><span data-stu-id="d6a19-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="d6a19-117">Désinstaller à partir de PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6a19-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="d6a19-118">Si vous avez installé Azure PowerShell à l’aide de PowerShellGet, vous pouvez utiliser la cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="d6a19-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d6a19-119">Toutefois, la cmdlet `Uninstall-Module` ne désinstalle qu’un module.</span><span class="sxs-lookup"><span data-stu-id="d6a19-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d6a19-120">Pour supprimer complètement Azure PowerShell, vous devez désinstaller chaque module individuellement.</span><span class="sxs-lookup"><span data-stu-id="d6a19-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d6a19-121">La désinstallation peut être compliquée si plusieurs versions d’Azure PowerShell sont installées.</span><span class="sxs-lookup"><span data-stu-id="d6a19-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="d6a19-122">Le script suivant peut être utilisé pour supprimer complètement une seule version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6a19-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="d6a19-123">Le script interroge PowerShell Gallery pour obtenir une liste des sous-modules dépendants.</span><span class="sxs-lookup"><span data-stu-id="d6a19-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d6a19-124">Il désinstalle ensuite la bonne version de chaque sous-module.</span><span class="sxs-lookup"><span data-stu-id="d6a19-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
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

<span data-ttu-id="d6a19-125">Pour utiliser cette fonction, copiez et collez le code dans votre session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6a19-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d6a19-126">L’exemple suivant montre comment exécuter la fonction afin de supprimer une ancienne version d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6a19-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="d6a19-127">Lors de l’exécution du script, ce dernier affichera le nom et la version de chaque sous-module en train d’être désinstallé.</span><span class="sxs-lookup"><span data-stu-id="d6a19-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="d6a19-128">Exécutez cette commande pour chaque version d’Azure PowerShell que vous souhaitez désinstaller.</span><span class="sxs-lookup"><span data-stu-id="d6a19-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>