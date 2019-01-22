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
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240133"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="4b8b6-103">Module Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="4b8b6-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8b6-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="4b8b6-104">Requirements:</span></span>
<span data-ttu-id="4b8b6-105">La version minimale d’Azure Stack prise en charge est la version 1811.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="4b8b6-106">Remarque : Si vous utilisez une version antérieure, installez la version 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="4b8b6-107">Installer</span><span class="sxs-lookup"><span data-stu-id="4b8b6-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="4b8b6-108">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="4b8b6-108">Release Notes</span></span>
* <span data-ttu-id="4b8b6-109">Pris en charge avec la mise à jour 1811</span><span class="sxs-lookup"><span data-stu-id="4b8b6-109">Supported with 1811 update</span></span>
* <span data-ttu-id="4b8b6-110">Module Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="4b8b6-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="4b8b6-111">Correction du préfixe manquant Azs pour New-DataDiskObject et ajout de l’alias avec avertissement de dépréciation.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="4b8b6-112">Module Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="4b8b6-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="4b8b6-113">Ajout d’un avertissement pour conseiller l’exécution de Test-AzureStack avant Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="4b8b6-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="4b8b6-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="4b8b6-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="4b8b6-115">Nouvelle cmdlet (les fonctionnalités sont prises en charge par Azure Stack 1811+)</span><span class="sxs-lookup"><span data-stu-id="4b8b6-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="4b8b6-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="4b8b6-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="4b8b6-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="4b8b6-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="4b8b6-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="4b8b6-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="4b8b6-119">Dépréciation</span><span class="sxs-lookup"><span data-stu-id="4b8b6-119">Deprecation</span></span>
        * <span data-ttu-id="4b8b6-120">Get-AzsInfrastructureVolume est un alias de la cmdlet Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="4b8b6-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="4b8b6-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="4b8b6-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="4b8b6-122">Ajout d’une nouvelle cmdlet Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="4b8b6-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="4b8b6-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="4b8b6-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="4b8b6-124">Correction d’un bogue où les valeurs de quota par défaut ne sont pas utilisées</span><span class="sxs-lookup"><span data-stu-id="4b8b6-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="4b8b6-125">Module Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="4b8b6-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="4b8b6-126">Correction du préfixe manquant Azs pour New-AddonPlanDefinitionObject et ajout de l’alias avec avertissement de dépréciation.</span><span class="sxs-lookup"><span data-stu-id="4b8b6-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
