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
# <a name="azure-stack-module-160"></a>Module Azure Stack 1.6.0

## <a name="requirements"></a>Requirements:
La version minimale d’Azure Stack prise en charge est la version 1811.

Remarque : Si vous utilisez une version antérieure, installez la version 1.6.0.

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

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Notes de publication
* Pris en charge avec la mise à jour 1811
* Module Azs.Compute.Admin
    * Correction du préfixe manquant Azs pour New-DataDiskObject et ajout de l’alias avec avertissement de dépréciation.
* Module Azs.Update.Admin
    * Ajout d’un avertissement pour conseiller l’exécution de Test-AzureStack avant Install-AzsUpdate
* Azs.Fabric.Admin
    * Nouvelle cmdlet (les fonctionnalités sont prises en charge par Azure Stack 1811+)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Dépréciation
        * Get-AzsInfrastructureVolume est un alias de la cmdlet Get-AzsVolume
* Azs.InfrastructureInsights.Admin
    *  Ajout d’une nouvelle cmdlet Repair-AzsAlert
* Azs.Storage.Admin
    * Correction d’un bogue où les valeurs de quota par défaut ne sont pas utilisées
* Module Azs.Subscriptions.Admin
    * Correction du préfixe manquant Azs pour New-AddonPlanDefinitionObject et ajout de l’alias avec avertissement de dépréciation.
