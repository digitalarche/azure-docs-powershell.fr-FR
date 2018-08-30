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
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250316"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="73f7a-103">Exécuter Azure PowerShell dans un conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="73f7a-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="73f7a-104">Pour faciliter l’exécution d’Azure PowerShell dans des environnements portables, Microsoft publie des images Docker avec Azure PowerShell préinstallé.</span><span class="sxs-lookup"><span data-stu-id="73f7a-104">To make running Azure PowerShell in portable environments easy, Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="73f7a-105">Ces images offrent un invité Linux exécutant PowerShell Core ou un invité Windows avec PowerShell Core ou PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="73f7a-105">These images offer a Linux guest running PowerShell Core, or a Windows guest with either PowerShell Core or PowerShell 5.</span></span>

| <span data-ttu-id="73f7a-106">Environnement</span><span class="sxs-lookup"><span data-stu-id="73f7a-106">Environment</span></span> | <span data-ttu-id="73f7a-107">Image Docker</span><span class="sxs-lookup"><span data-stu-id="73f7a-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="73f7a-108">PowerShell sur Windows</span><span class="sxs-lookup"><span data-stu-id="73f7a-108">PowerShell on Windows</span></span> | [<span data-ttu-id="73f7a-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="73f7a-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="73f7a-110">PowerShell Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="73f7a-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="73f7a-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="73f7a-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="73f7a-112">PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="73f7a-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="73f7a-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="73f7a-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="73f7a-114">Pour exécuter une de ces conteneurs, vous utilisez `docker run -it $ImageName` pour obtenir un terminal interactif.</span><span class="sxs-lookup"><span data-stu-id="73f7a-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="73f7a-115">Par exemple, pour exécuter PowerShell Core sur le conteneur Linux, utilisez :</span><span class="sxs-lookup"><span data-stu-id="73f7a-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="73f7a-116">Pour exécuter un conteneur Windows dans Docker, votre système d’exploitation hôte doit être Windows et Docker doit être défini de manière à exécuter des conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="73f7a-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="73f7a-117">Pour en savoir plus sur le basculement entre des environnements Windows et Linux dans Docker, consultez la documentation Docker [Basculer entre les conteneurs Windows et Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="73f7a-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="73f7a-118">Utiliser un conteneur PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="73f7a-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="73f7a-119">Les conteneurs PowerShell Core sont fournis avec PowerShell Core v6 et le module `AzureRM.NetCore` préinstallé.</span><span class="sxs-lookup"><span data-stu-id="73f7a-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="73f7a-120">Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :</span><span class="sxs-lookup"><span data-stu-id="73f7a-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="73f7a-121">Utiliser le conteneur Windows avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="73f7a-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="73f7a-122">Le conteneur Windows dispose du module `AzureRM` préinstallé.</span><span class="sxs-lookup"><span data-stu-id="73f7a-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="73f7a-123">Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :</span><span class="sxs-lookup"><span data-stu-id="73f7a-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
