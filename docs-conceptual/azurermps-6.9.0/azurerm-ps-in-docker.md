---
title: Exécuter Azure PowerShell dans un conteneur Docker
description: Mode d’exécution d’Azure PowerShell dans un conteneur Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178559"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Exécuter Azure PowerShell dans un conteneur Docker

Microsoft publie des images Docker avec Azure PowerShell préinstallé. Ces images vous permettent d’expérimenter avec Azure PowerShell ou de l’exécuter dans un environnement isolé. Certaines images exécutent à la fois PowerShell Core et PowerShell 5. 

| Environnement | Image Docker |
|-------------|--------------|
| PowerShell sur Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core sur Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core sur Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Pour exécuter n’importe lequel de ces conteneurs, utilisez la commande `docker run -it $ImageName` afin d’obtenir un terminal interactif. Par exemple, pour exécuter un conteneur Linux avec PowerShell Core :

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Pour exécuter un conteneur Windows dans Docker, votre système d’exploitation hôte doit être Windows et Docker doit être défini de manière à exécuter des conteneurs Windows. Pour en savoir plus sur le basculement entre des environnements Windows et Linux dans Docker, consultez la documentation Docker [Basculer entre les conteneurs Windows et Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).

## <a name="use-a-powershell-core-container"></a>Utiliser un conteneur PowerShell Core

Les conteneurs PowerShell Core sont fournis avec PowerShell Core v6 et le module `AzureRM.NetCore` préinstallé. Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>Utiliser le conteneur Windows avec PowerShell

Le conteneur Windows dispose du module `AzureRM` préinstallé. Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
