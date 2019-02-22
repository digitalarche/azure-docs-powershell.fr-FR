---
title: Vue d’ensemble d’Azure Stack PowerShell administrateur | Microsoft Docs
description: Une vue d’ensemble d’Azure Stack PowerShell administrateur avec des instructions sur les procédures d’installation et de configuration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153147"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="c7ac7-103">Module Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="c7ac7-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ac7-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="c7ac7-104">Requirements:</span></span>
<span data-ttu-id="c7ac7-105">La version minimale d’Azure Stack prise en charge est la version 1811.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="c7ac7-106">Remarque : Si vous utilisez une version antérieure, installez la version 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="c7ac7-107">Installer</span><span class="sxs-lookup"><span data-stu-id="c7ac7-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="c7ac7-108">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="c7ac7-108">Release Notes</span></span>
* <span data-ttu-id="c7ac7-109">Pris en charge avec la mise à jour 1811</span><span class="sxs-lookup"><span data-stu-id="c7ac7-109">Supported with 1811 update</span></span>
* <span data-ttu-id="c7ac7-110">Module Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="c7ac7-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="c7ac7-111">Correction du préfixe manquant Azs pour New-DataDiskObject et ajout de l’alias avec avertissement de dépréciation.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="c7ac7-112">Module Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="c7ac7-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="c7ac7-113">Ajout d’un avertissement pour conseiller l’exécution de Test-AzureStack avant Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="c7ac7-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="c7ac7-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="c7ac7-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="c7ac7-115">Nouvelle cmdlet (les fonctionnalités sont prises en charge par Azure Stack 1811+)</span><span class="sxs-lookup"><span data-stu-id="c7ac7-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="c7ac7-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="c7ac7-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="c7ac7-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="c7ac7-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="c7ac7-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c7ac7-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="c7ac7-119">Dépréciation</span><span class="sxs-lookup"><span data-stu-id="c7ac7-119">Deprecation</span></span>
        * <span data-ttu-id="c7ac7-120">Get-AzsInfrastructureVolume est un alias de la cmdlet Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="c7ac7-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="c7ac7-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="c7ac7-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="c7ac7-122">Ajout d’une nouvelle cmdlet Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="c7ac7-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="c7ac7-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="c7ac7-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="c7ac7-124">Correction d’un bogue où les valeurs de quota par défaut ne sont pas utilisées</span><span class="sxs-lookup"><span data-stu-id="c7ac7-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="c7ac7-125">Module Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="c7ac7-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="c7ac7-126">Correction du préfixe manquant Azs pour New-AddonPlanDefinitionObject et ajout de l’alias avec avertissement de dépréciation.</span><span class="sxs-lookup"><span data-stu-id="c7ac7-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
