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
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="e9fdf-103">Exécuter Azure PowerShell dans un conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="e9fdf-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="e9fdf-104">Microsoft publie des images Docker avec Azure PowerShell préinstallé.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="e9fdf-105">Ces images vous permettent d’expérimenter avec Azure PowerShell ou de l’exécuter dans un environnement isolé.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="e9fdf-106">Certaines images exécutent à la fois PowerShell Core et PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="e9fdf-107">Environnement</span><span class="sxs-lookup"><span data-stu-id="e9fdf-107">Environment</span></span> | <span data-ttu-id="e9fdf-108">Image Docker</span><span class="sxs-lookup"><span data-stu-id="e9fdf-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="e9fdf-109">PowerShell sur Windows</span><span class="sxs-lookup"><span data-stu-id="e9fdf-109">PowerShell on Windows</span></span> | [<span data-ttu-id="e9fdf-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="e9fdf-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="e9fdf-111">PowerShell Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="e9fdf-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="e9fdf-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="e9fdf-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="e9fdf-113">PowerShell Core sur Linux</span><span class="sxs-lookup"><span data-stu-id="e9fdf-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="e9fdf-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="e9fdf-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="e9fdf-115">Pour exécuter n’importe lequel de ces conteneurs, utilisez la commande `docker run -it $ImageName` afin d’obtenir un terminal interactif.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="e9fdf-116">Par exemple, pour exécuter un conteneur Linux avec PowerShell Core :</span><span class="sxs-lookup"><span data-stu-id="e9fdf-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="e9fdf-117">Pour exécuter un conteneur Windows dans Docker, votre système d’exploitation hôte doit être Windows et Docker doit être défini de manière à exécuter des conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="e9fdf-118">Pour en savoir plus sur le basculement entre des environnements Windows et Linux dans Docker, consultez la documentation Docker [Basculer entre les conteneurs Windows et Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="e9fdf-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="e9fdf-119">Utiliser un conteneur PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="e9fdf-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="e9fdf-120">Les conteneurs PowerShell Core sont fournis avec PowerShell Core v6 et le module `AzureRM.NetCore` préinstallé.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="e9fdf-121">Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :</span><span class="sxs-lookup"><span data-stu-id="e9fdf-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="e9fdf-122">Utiliser le conteneur Windows avec PowerShell</span><span class="sxs-lookup"><span data-stu-id="e9fdf-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="e9fdf-123">Le conteneur Windows dispose du module `AzureRM` préinstallé.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="e9fdf-124">Exécutez la cmdlet [Import-Module](/powershell/module/microsoft.powershell.core/import-module) puis connectez-vous à votre compte Azure :</span><span class="sxs-lookup"><span data-stu-id="e9fdf-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
