---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853013"
---
# <a name="release-notes"></a><span data-ttu-id="8fed1-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="8fed1-103">Release notes</span></span>

<span data-ttu-id="8fed1-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="8fed1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="8fed1-105">Version 1.2.9</span><span class="sxs-lookup"><span data-stu-id="8fed1-105">Version 1.2.9</span></span>

<span data-ttu-id="8fed1-106">Modifications apportées à cette version</span><span class="sxs-lookup"><span data-stu-id="8fed1-106">Changes This Release</span></span>

* <span data-ttu-id="8fed1-107">Module AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="8fed1-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="8fed1-108">Modifications de l’applet de commande Add-AzureRmResourceProviderRegistration pour la prise en charge de la séparation entre l’administrateur et le locataire Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8fed1-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="8fed1-109">Ajout d’un nouveau paramètre -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="8fed1-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="8fed1-110">Suppression des paramètres -AdminUri, -ApiVersion, -SubscriptionId et -Token dans chaque applet de commande.</span><span class="sxs-lookup"><span data-stu-id="8fed1-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="8fed1-111">Nous avions publié des avertissements indiquant que ces paramètres allaient être déconseillés, ils sont désormais supprimés.</span><span class="sxs-lookup"><span data-stu-id="8fed1-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="8fed1-112">Module AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="8fed1-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="8fed1-113">Ajout de nouvelles applets de commande pour prendre en charge les scénarios de migration de conteneur.</span><span class="sxs-lookup"><span data-stu-id="8fed1-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="8fed1-114">Suppression des applets de commande faisant référence aux composants internes et aux fonctionnalités sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="8fed1-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="8fed1-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="8fed1-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="8fed1-116">Création d’un module pour gérer les versions des applets de commande Azure PowerShell par le biais de l’utilisation des profils de version</span><span class="sxs-lookup"><span data-stu-id="8fed1-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>