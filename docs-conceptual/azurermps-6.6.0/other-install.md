---
title: Autres méthodes d’installation d’Azure PowerShell
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet à l’aide d’un fichier MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: add4d1843cf3fe791f3a734f43b0fb065629e899
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018742"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installer Azure PowerShell sur Windows avec un fichier MSI

Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un programme d’installation de MSI.  
Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système. Il est recommandé d’installer Azure PowerShell sur Windows avec PowerShellGet. Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> La méthode d’installation avec Web Platform Installer n’est plus disponible pour les versions d’Azure PowerShell 6.x et plus récentes. Si vous devez utiliser Web Platform Installer, préférez l’utilisation d’un fichier MSI ou l’installation d’une version plus ancienne d’Azure PowerShell.

Pour exécuter Azure PowerShell dans un conteneur Docker, consultez [Exécuter Azure PowerShell dans Docker](azurerm-ps-in-docker.md).

Pour une installation sur des environnements Linux ou macOS, consultez [Installer Azure PowerShell sur macOS ou Linux](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installer ou mettre à jour sur Windows à l’aide du package MSI

Azure PowerShell peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement. Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`. Les modules `AzureRM` et `Azure` sont installés.

> [!NOTE]
> N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.

Pour commencer à utiliser Azure PowerShell, vous devez charger `AzureRM` dans votre session PowerShell actuelle avec la cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), puis vous connecter avec vos informations d’identification Azure.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Vous devez répéter ces étapes pour chaque nouvelle session PowerShell que vous démarrez. L’importation automatique du module `AzureRM` nécessite la configuration d’un profil PowerShell. Pour en savoir plus, consultez [À propos des profils](/powershell/module/microsoft.powershell.core/about/about_profiles).
Pour savoir comment conserver votre connexion Azure sur plusieurs sessions, consultez [Persist user credentials across PowerShell sessions](context-persistence.md) (Conserver ses informations d’identification d’utilisateur sur plusieurs sessions PowerShell).