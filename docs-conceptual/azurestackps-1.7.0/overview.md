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
# <a name="azure-stack-module-170"></a>Azure Stack Module 1.7.0

## <a name="requirements"></a>Requirements:
La version minimale d’Azure Stack prise en charge est la version 1901.

Remarque : Si vous utilisez une version antérieure, installez la version 1.7.0

## <a name="install"></a>Installer
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
## <a name="release-notes"></a>Notes de publication
* Pris en charge avec la mise à jour 1901
* Il s’agit d’une modification critique. Pour plus d’informations sur les modifications critiques, reportez-vous à https://aka.ms/azspshmigration170.
* Modification critique apportée à Azs.Backup.Admin Module * : Modifications concernant les sauvegardes dans le mode de chiffrement basé sur le certificat. La prise en charge des clés symétriques est dépréciée.
* Module Azs.Fabric.Admin       * Déconseillé           * Get-AzsInfrastructureVolume a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsVolume           * Get-AzsStorageSystem a été déconseillé, nous fournissons une nouvelle applet de commande Get-AzsStorageSubSystem           * Get-AzsStoragePool a été déconseillé, l’objet StorageSubSystem dispose d’une propriété de capacité
* Module Azs.Compute.Admin           * Résolution de bogue : Add-AzsPlatformImage, Get-AzsPlatformImage : Appel de ConvertTo-PlatformImageObject uniquement dans le chemin de réussite           * Résolution de bogue : Add-AzsVmExtension, Get-AzsVmExtension : Appel de ConvertTo-VmExtensionObject uniquement dans le chemin de réussite
* Azs.Storage.Admin Module           * Résolution de bogue : le nouveau quota de stockage utilise les valeurs par défaut si aucune n’est spécifiée.

