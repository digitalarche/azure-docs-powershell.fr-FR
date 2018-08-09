---
title: Exécuter Azure PowerShell dans un conteneur Docker
description: Mode d’exécution d’Azure PowerShell dans un conteneur Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653931"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="f41bd-103">Exécuter Azure PowerShell dans un conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="f41bd-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="f41bd-104">Un ensemble d’images Docker préconfigurées est disponible avec Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="f41bd-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="f41bd-105">Deux types de conteneurs sont disponibles : ceux exécutant PowerShell de manière classique sur Windows et un conteneur exécutant PowerShell Core sur Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="f41bd-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="f41bd-106">Environnement</span><span class="sxs-lookup"><span data-stu-id="f41bd-106">Environment</span></span> | <span data-ttu-id="f41bd-107">Image Docker</span><span class="sxs-lookup"><span data-stu-id="f41bd-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="f41bd-108">PowerShell sur Windows</span><span class="sxs-lookup"><span data-stu-id="f41bd-108">PowerShell on Windows</span></span> | [<span data-ttu-id="f41bd-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="f41bd-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="f41bd-110">PowerShell Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="f41bd-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="f41bd-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="f41bd-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="f41bd-112">PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="f41bd-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="f41bd-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="f41bd-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="f41bd-114">Pour exécuter une de ces conteneurs, vous utilisez `docker run -it $ImageName` pour obtenir un terminal interactif.</span><span class="sxs-lookup"><span data-stu-id="f41bd-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="f41bd-115">Par exemple, pour exécuter PowerShell Core sur le conteneur Linux, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f41bd-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="f41bd-116">Pour exécuter un conteneur Windows dans Docker, votre système d’exploitation hôte doit être Windows et Docker doit être défini de manière à exécuter des conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="f41bd-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="f41bd-117">Pour en savoir plus sur le basculement entre des environnements Windows et Linux dans Docker, consultez la documentation Docker [Basculer entre les conteneurs Windows et Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="f41bd-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="f41bd-118">Utiliser un conteneur PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="f41bd-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="f41bd-119">Les conteneurs PowerShell Core sont fournis avec PowerShell Core v6 et le module `AzureRM.NetCore` préinstallé.</span><span class="sxs-lookup"><span data-stu-id="f41bd-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="f41bd-120">Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :</span><span class="sxs-lookup"><span data-stu-id="f41bd-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="f41bd-121">Utiliser le conteneur Windows avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="f41bd-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="f41bd-122">Le conteneur Windows dispose du module `AzureRM` préinstallé.</span><span class="sxs-lookup"><span data-stu-id="f41bd-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="f41bd-123">Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :</span><span class="sxs-lookup"><span data-stu-id="f41bd-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```