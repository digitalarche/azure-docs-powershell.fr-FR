---
title: "Vue d’ensemble d’Azure Stack PowerShell | Microsoft Docs"
description: "Vue d’ensemble de l’installation et de la configuration d’Azure Stack PowerShell."
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 2a03697e0f3e80d63c48f2dc5615f6c99b9ef716
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell 

Azure Stack nécessite les deux modules PowerShell suivants :  

1. Le module **AzureRM** compatible Azure Stack qui est disponible en installant le profil de version d’API **2017-03-09-profile**. Les applets de commande installées à l’aide de ce profil peuvent servir aux administrateurs et aux locataires du cloud Azure Stack. Pour en savoir plus sur les applets de commande PowerShell disponibles dans ce profil, consultez le contenu de référence PowerShell pour la [version 1.2.9 du module AzureRM](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9).  

2. Version **1.2.9** du module **AzureStack**. Les applets de commande installées à l’aide de ce module peuvent servir uniquement aux administrateurs du cloud Azure Stack. L’administrateur peut effectuer des opérations comme la gestion des offres, des plans, des services, des quotas, etc. à l’aide des applets de commande PowerShell fournies par ce module. Pour en savoir plus sur les applets de commande PowerShell disponibles dans ce module, consultez le contenu de référence sur [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) et [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage).

## <a name="next-steps"></a>Étapes suivantes

* [Installer PowerShell pour Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [Configurer PowerShell pour une utilisation avec Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)


