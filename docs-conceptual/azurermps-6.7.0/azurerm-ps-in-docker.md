---
title: Exécuter Azure PowerShell dans un conteneur Docker
description: Mode d’exécution d’Azure PowerShell dans un conteneur Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106416"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Exécuter Azure PowerShell dans un conteneur Docker

Pour faciliter l’exécution d’Azure PowerShell dans des environnements portables, Microsoft publie des images Docker avec Azure PowerShell préinstallé. Ces images offrent un invité Linux exécutant PowerShell Core ou un invité Windows avec PowerShell Core ou PowerShell 5.

| Environnement | Image Docker |
|-------------|--------------|
| PowerShell sur Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core sur Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core sur Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Pour exécuter une de ces conteneurs, vous utilisez `docker run -it $ImageName` pour obtenir un terminal interactif. Par exemple, pour exécuter PowerShell Core sur le conteneur Linux, utilisez :

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
