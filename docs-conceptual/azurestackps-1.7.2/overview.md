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
# <a name="azure-stack-module-172"></a>Module Azure Stack 1.7.2

## <a name="requirements"></a>Requirements:

La version minimale d’Azure Stack prise en charge est 1904.

Remarque : Pour les versions antérieures d’Azure Stack, consultez [Installer Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Installer

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Notes de publication

* Pris en charge avec la mise à jour 1904
* Il s’agit d’une modification critique. Pour plus d’informations sur les modifications critiques, reportez-vous à <https://aka.ms/azspshmigration170>.
* Changement cassant : Modifications concernant les sauvegardes dans le mode de chiffrement basé sur le certificat. La prise en charge des clés symétriques est dépréciée.
* Pour plus d’informations sur les modifications critiques, reportez-vous à https://aka.ms/azspshmigration170.
* Module Azs.Storage.Admin 
* Résolution de bogue - Le nouveau quota de stockage utilise les valeurs par défaut si aucune n’est spécifiée.
