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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58808054"
---
# <a name="azure-stack-module-171"></a>Module Azure Stack 1.7.1

## <a name="requirements"></a>Requirements:

La version minimale d’Azure Stack prise en charge est la version 1901.

Remarque : Pour les versions antérieures d’Azure Stack, consultez [Installer Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installer

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Notes de publication

* Pris en charge avec la mise à jour 1901
* Il s’agit d’une modification critique. Pour plus d’informations sur les modifications critiques, reportez-vous à <https://aka.ms/azspshmigration170>.
* Modification critique apportée à Azs.Backup.Admin Module * : Modifications concernant les sauvegardes dans le mode de chiffrement basé sur le certificat. La prise en charge des clés symétriques est dépréciée.
* Module Azs.Fabric.Admin       * Déconseillé           * Get-AzsInfrastructureVolume a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsVolume           * Get-AzsStorageSystem a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsStorageSubSystem           * Get-AzsStoragePool a été déconseillé, l’objet StorageSubSystem dispose d’une propriété de capacité
* Module Azs.Compute.Admin           * Résolution de bogue : Add-AzsPlatformImage, Get-AzsPlatformImage : Appel de ConvertTo-PlatformImageObject uniquement dans le chemin de réussite           * Résolution de bogue : Add-AzsVmExtension, Get-AzsVmExtension : Appel de ConvertTo-VmExtensionObject uniquement dans le chemin de réussite
* Azs.Storage.Admin Module           * Résolution de bogue : le nouveau quota de stockage utilise les valeurs par défaut si aucune n’est spécifiée.
