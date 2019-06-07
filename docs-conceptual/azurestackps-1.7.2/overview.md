---
title: Vue d’ensemble d’Azure Stack PowerShell administrateur | Microsoft Docs
description: Une vue d’ensemble d’Azure Stack PowerShell administrateur avec des instructions sur les procédures d’installation et de configuration.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855786"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="39c11-103">Module Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="39c11-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="39c11-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="39c11-104">Requirements:</span></span>

<span data-ttu-id="39c11-105">La version minimale d’Azure Stack prise en charge est 1904.</span><span class="sxs-lookup"><span data-stu-id="39c11-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="39c11-106">Remarque : Pour les versions antérieures d’Azure Stack, consultez [Installer Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="39c11-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="39c11-107">Installer PowerShell pour Azure Stack</span><span class="sxs-lookup"><span data-stu-id="39c11-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="39c11-108">L’installation comporte trois étapes :</span><span class="sxs-lookup"><span data-stu-id="39c11-108">Installation has three steps:</span></span>

1. <span data-ttu-id="39c11-109">Installer Azure Stack PowerShell selon votre version d’Azure Stack</span><span class="sxs-lookup"><span data-stu-id="39c11-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="39c11-110">Activer les fonctionnalités de stockage supplémentaire</span><span class="sxs-lookup"><span data-stu-id="39c11-110">Enable additional storage features</span></span>
3. <span data-ttu-id="39c11-111">Confirmer l’installation de PowerShell</span><span class="sxs-lookup"><span data-stu-id="39c11-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="39c11-112">Installer Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="39c11-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="39c11-113">Activer les fonctionnalités de stockage supplémentaire</span><span class="sxs-lookup"><span data-stu-id="39c11-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="39c11-114">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="39c11-114">Release Notes</span></span>

* <span data-ttu-id="39c11-115">Pris en charge avec la mise à jour 1904</span><span class="sxs-lookup"><span data-stu-id="39c11-115">Supported with 1904 update</span></span>
* <span data-ttu-id="39c11-116">Il s’agit d’une modification critique.</span><span class="sxs-lookup"><span data-stu-id="39c11-116">This a breaking change release.</span></span> <span data-ttu-id="39c11-117">Pour plus d’informations sur les modifications critiques, reportez-vous à <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="39c11-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="39c11-118">Modification critique apportée à Azs.Backup.Admin Module \* : Modifications concernant les sauvegardes dans le mode de chiffrement basé sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="39c11-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="39c11-119">La prise en charge des clés symétriques est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="39c11-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="39c11-120">Module Azs.Fabric.Admin       \* Déconseillé           \* Get-AzsInfrastructureVolume a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsVolume           \* Get-AzsStorageSystem a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsStorageSubSystem           \* Get-AzsStoragePool a été déconseillé, l’objet StorageSubSystem dispose d’une propriété de capacité</span><span class="sxs-lookup"><span data-stu-id="39c11-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="39c11-121">Module Azs.Compute.Admin           \* Résolution de bogue : Add-AzsPlatformImage, Get-AzsPlatformImage : Appel de ConvertTo-PlatformImageObject uniquement dans le chemin de réussite           \* Résolution de bogue : Add-AzsVmExtension, Get-AzsVmExtension : Appel de ConvertTo-VmExtensionObject uniquement dans le chemin de réussite</span><span class="sxs-lookup"><span data-stu-id="39c11-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="39c11-122">Azs.Storage.Admin Module           \* Résolution de bogue : le nouveau quota de stockage utilise les valeurs par défaut si aucune n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="39c11-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
