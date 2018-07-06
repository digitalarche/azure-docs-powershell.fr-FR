---
title: Exécuter Azure PowerShell dans un conteneur Docker
description: Mode d’exécution d’Azure PowerShell dans un conteneur Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091596"
---
## <a name="run-azure-powershell-in-a-docker-container"></a>Exécuter Azure PowerShell dans un conteneur Docker

Un ensemble d’images Docker préconfigurées est disponible avec Azure Powershell. Deux types de conteneurs sont disponibles : ceux exécutant PowerShell de manière classique sur Windows et un conteneur exécutant PowerShell Core sur Windows ou Linux.

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