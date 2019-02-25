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
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240517"
---
# <a name="azure-stack-module-170"></a><span data-ttu-id="594dd-103">Azure Stack Module 1.7.0</span><span class="sxs-lookup"><span data-stu-id="594dd-103">Azure Stack Module 1.7.0</span></span>

## <a name="requirements"></a><span data-ttu-id="594dd-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="594dd-104">Requirements:</span></span>
<span data-ttu-id="594dd-105">La version minimale d’Azure Stack prise en charge est la version 1901.</span><span class="sxs-lookup"><span data-stu-id="594dd-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="594dd-106">Remarque : Si vous utilisez une version antérieure, installez la version 1.7.0</span><span class="sxs-lookup"><span data-stu-id="594dd-106">Note: If you are using an earlier version install version 1.7.0</span></span>

## <a name="install"></a><span data-ttu-id="594dd-107">Installer</span><span class="sxs-lookup"><span data-stu-id="594dd-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a><span data-ttu-id="594dd-108">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="594dd-108">Release Notes</span></span>
* <span data-ttu-id="594dd-109">Pris en charge avec la mise à jour 1901</span><span class="sxs-lookup"><span data-stu-id="594dd-109">Supported with 1901 update</span></span>
* <span data-ttu-id="594dd-110">Il s’agit d’une modification critique.</span><span class="sxs-lookup"><span data-stu-id="594dd-110">This a breaking change release.</span></span> <span data-ttu-id="594dd-111">Pour plus d’informations sur les modifications critiques, reportez-vous à https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="594dd-111">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="594dd-112">Modification critique apportée à Azs.Backup.Admin Module \* : Modifications concernant les sauvegardes dans le mode de chiffrement basé sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="594dd-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="594dd-113">La prise en charge des clés symétriques est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="594dd-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="594dd-114">Module Azs.Fabric.Admin       \* Déconseillé           \* Get-AzsInfrastructureVolume a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsVolume           \* Get-AzsStorageSystem a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsStorageSubSystem           \* Get-AzsStoragePool a été déconseillé, l’objet StorageSubSystem dispose d’une propriété de capacité</span><span class="sxs-lookup"><span data-stu-id="594dd-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="594dd-115">Module Azs.Compute.Admin           \* Résolution de bogue : Add-AzsPlatformImage, Get-AzsPlatformImage : Appel de ConvertTo-PlatformImageObject uniquement dans le chemin de réussite           \* Résolution de bogue : Add-AzsVmExtension, Get-AzsVmExtension : Appel de ConvertTo-VmExtensionObject uniquement dans le chemin de réussite</span><span class="sxs-lookup"><span data-stu-id="594dd-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="594dd-116">Azs.Storage.Admin Module           \* Résolution de bogue : le nouveau quota de stockage utilise les valeurs par défaut si aucune n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="594dd-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>

