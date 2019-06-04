---
title: Autres méthodes d’installation d’Azure PowerShell
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: fe35fccd7994d7c3c3587096263a50af598e8651
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65535037"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>Installer Azure PowerShell sur Windows avec un fichier MSI ou Web Platform Installer

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un fichier MSI ou de Web Platform Installer (WebPI).  
Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système. Il est recommandé d’installer Azure PowerShell sur Windows avec PowerShellGet. Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installer ou mettre à jour sur Windows à l’aide du package MSI

Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018). Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement. Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`. Les modules `AzureRM` et `Azure` sont installés.

> [!NOTE]
> N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.

Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Installer ou mettre à jour sur Windows à l’aide de Web Platform Installer

Téléchargez le [package Azure PowerShell WebPI](http://aka.ms/webpi-azps) et démarrez l’installation. Si vous avez installé des versions antérieures de modules Azure à partir d’un fichier MSI ou avec WebPi, le programme d’installation les supprime automatiquement. Les modules sont installés dans `${env:ProgramFiles}\WindowsPowerShell\Modules`. Les modules `AzureRM` et `Azure` sont installés.

> [!NOTE]
> N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.

Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).