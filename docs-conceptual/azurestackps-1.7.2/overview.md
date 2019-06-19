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
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037676"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="22c2a-103">Module Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="22c2a-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="22c2a-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="22c2a-104">Requirements:</span></span>

<span data-ttu-id="22c2a-105">La version minimale d’Azure Stack prise en charge est 1904.</span><span class="sxs-lookup"><span data-stu-id="22c2a-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="22c2a-106">Remarque : Pour les versions antérieures d’Azure Stack, consultez [Installer Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="22c2a-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="22c2a-107">Installer</span><span class="sxs-lookup"><span data-stu-id="22c2a-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="22c2a-108">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="22c2a-108">Release Notes</span></span>

* <span data-ttu-id="22c2a-109">Pris en charge avec la mise à jour 1904</span><span class="sxs-lookup"><span data-stu-id="22c2a-109">Supported with 1904 update</span></span>
* <span data-ttu-id="22c2a-110">Il s’agit d’une modification critique.</span><span class="sxs-lookup"><span data-stu-id="22c2a-110">This a breaking change release.</span></span> <span data-ttu-id="22c2a-111">Pour plus d’informations sur les modifications critiques, reportez-vous à <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="22c2a-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="22c2a-112">Changement cassant : Modifications concernant les sauvegardes dans le mode de chiffrement basé sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="22c2a-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="22c2a-113">La prise en charge des clés symétriques est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="22c2a-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="22c2a-114">Pour plus d’informations sur les modifications critiques, reportez-vous à https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="22c2a-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="22c2a-115">Module Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="22c2a-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="22c2a-116">Résolution de bogue - Le nouveau quota de stockage utilise les valeurs par défaut si aucune n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="22c2a-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
