---
title: Installer Azure PowerShell avec un fichier MSI
description: Procédure d’installation d’Azure PowerShell sans PowerShellGet à l’aide d’un fichier MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 566ea4b9ac9398b063cc3567c482a67834de36f5
ms.sourcegitcommit: ad7677d703a8512d371d3123dc7e541156b95cb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2019
ms.locfileid: "72821501"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installer Azure PowerShell sur Windows avec un fichier MSI

Cet article explique comment installer Azure PowerShell sur Windows à l’aide d’un programme d’installation de MSI. Le programme d’installation MSI est fourni pour les environnements dans lesquels PowerShell Gallery risque d’être bloqué par un pare-feu ou quand un programme d’installation hors connexion est nécessaire. Il est recommandé d’installer Azure PowerShell avec PowerShellGet. Pour obtenir des instructions sur l’utilisation de PowerShellGet pour installer Azure PowerShell, consultez [Installer Azure PowerShell avec PowerShellGet](install-az-ps.md).

## <a name="requirements"></a>Configuration requise

Le programme d’installation MSI pour Azure PowerShell fonctionne __uniquement__ pour PowerShell 5.1 sur Windows. Pour une installation sur des plateformes non Windows ou des versions ultérieures de PowerShell, effectuez l’[installation avec PowerShellGet](install-az-ps.md).
Pour vérifier votre version de PowerShell, exécutez la commande :

```powershell-interactive
$PSVersionTable.PSVersion
```

Pour utiliser Azure PowerShell dans PowerShell 5.1, vous devez :

1. Mettrez à jour vers [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) si nécessaire. Si vous êtes sur Windows 10, PowerShell 5.1 est déjà installé.
2. Installez [.NET Framework 4.7.2 ou ultérieur](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installer ou mettre à jour sur Windows à l’aide du package MSI

Azure PowerShell pour Windows est installé avec le fichier MSI disponible à partir de [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019). Si vous avez installé des versions antérieures de modules Azure en tant que fichier MSI, le programme d’installation les supprime automatiquement. Le package MSI installe les modules dans `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Pour commencer à utiliser Azure PowerShell, connectez-vous à l’aide de vos informations d’identification Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
>
> Si vous avez désactivé le chargement automatique de modules, vous devez importer manuellement le module avec `Import-Module Az`. En raison de la structure du module, cette opération peut prendre jusqu’à une minute.

Vous devez répéter cette étape pour chaque nouvelle session PowerShell que vous démarrez. Pour savoir comment conserver votre connexion Azure sur plusieurs sessions PowerShell, consultez [Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell](context-persistence.md).

## <a name="provide-feedback"></a>Fournir des commentaires

Si vous rencontrez un bogue dans Azure PowerShell, [signalez un problème sur GitHub](https://github.com/Azure/azure-powershell/issues).
Pour fournir des commentaires à partir de la ligne de commande, utilisez la cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Étapes suivantes

Pour en savoir plus sur les modules PowerShell et leurs fonctionnalités, consultez l’article sur la [prise en main d’Azure PowerShell](get-started-azureps.md).
Si vous êtes familiarisé avec Azure PowerShell et devez effectuer une migration depuis AzureRM, consultez l’article sur la [migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).
