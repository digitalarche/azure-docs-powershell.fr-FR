---
title: Autres méthodes d’installation d’Azure PowerShell
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet à l’aide d’un fichier MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 82375cc4267f468f562d138c4cdec6131e34ae32
ms.sourcegitcommit: bbd3f061cac3417ce588487c1ae4e0bc52c11d6a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2019
ms.locfileid: "65534518"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installer Azure PowerShell sur Windows avec un fichier MSI

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un programme d’installation de MSI.  
Utilisez ces méthodes d’installation uniquement si elles sont nécessaires pour votre système. Il est recommandé d’installer Azure PowerShell sur Windows avec PowerShellGet. Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> La méthode d’installation avec Web Platform Installer n’est plus disponible pour les versions d’Azure PowerShell 6.x et plus récentes. Si vous devez utiliser Web Platform Installer, préférez l’utilisation d’un fichier MSI ou l’installation d’une version plus ancienne d’Azure PowerShell.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installer ou mettre à jour sur Windows à l’aide du package MSI

Azure PowerShell pour Windows PowerShell 5.x peut être installé à l’aide du fichier MSI disponible sur [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018). Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement. Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`. Les modules `AzureRM` et `Azure` sont installés.

> [!NOTE]
> N’utilisez que le module `Azure` si vous utilisez le modèle de déploiement Azure Classic.

Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module AzureRM`. En raison de la structure du module, cette opération peut prendre quelques secondes.

Vous devez répéter cette étape pour chaque nouvelle session PowerShell que vous démarrez. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).
