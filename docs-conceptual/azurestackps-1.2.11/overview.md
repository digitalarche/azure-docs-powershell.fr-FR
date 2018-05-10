---
title: Vue d’ensemble d’Azure Stack PowerShell | Microsoft Docs
description: Vue d’ensemble de l’installation et de la configuration d’Azure Stack PowerShell.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

Azure Stack nécessite les deux modules PowerShell suivants :  

1. Le module **AzureRM** compatible Azure Stack qui est disponible en installant le profil de version d’API **2017-03-09-profile**. Les cmdlets installées à l’aide de ce profil peuvent servir aux opérateurs et aux utilisateurs Azure Stack.

2. La version la plus actuelle est la **1.2.11** du module **AzureStack**. Les applets de commande installées à l’aide de ce module peuvent servir uniquement aux opérateurs Azure Stack. Les opérateurs peuvent effectuer des opérations comme la gestion des offres, des plans, des services, des quotas, etc. à l’aide des cmdlets PowerShell fournies par ce module. Pour en savoir plus sur les applets de commande PowerShell disponibles dans ce module, consultez le contenu de référence sur [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) et [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).

## <a name="next-steps"></a>Étapes suivantes

* [Installer PowerShell pour Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [Configurer PowerShell pour une utilisation avec Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
