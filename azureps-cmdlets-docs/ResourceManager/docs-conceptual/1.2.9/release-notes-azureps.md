---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: "Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="78902-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="78902-103">Release notes</span></span>

<span data-ttu-id="78902-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="78902-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="78902-105">Version 1.2.9</span><span class="sxs-lookup"><span data-stu-id="78902-105">Version 1.2.9</span></span>

<span data-ttu-id="78902-106">Modifications apportées à cette version</span><span class="sxs-lookup"><span data-stu-id="78902-106">Changes This Release</span></span>

* <span data-ttu-id="78902-107">Module AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="78902-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="78902-108">Modifications de l’applet de commande Add-AzureRmResourceProviderRegistration pour la prise en charge de la séparation entre l’administrateur et le locataire Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="78902-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="78902-109">Ajout d’un nouveau paramètre -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="78902-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="78902-110">Suppression des paramètres -AdminUri, -ApiVersion, -SubscriptionId et -Token dans chaque applet de commande.</span><span class="sxs-lookup"><span data-stu-id="78902-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="78902-111">Nous avions publié des avertissements indiquant que ces paramètres allaient être déconseillés, ils sont désormais supprimés.</span><span class="sxs-lookup"><span data-stu-id="78902-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="78902-112">Module AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="78902-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="78902-113">Ajout de nouvelles applets de commande pour prendre en charge les scénarios de migration de conteneur.</span><span class="sxs-lookup"><span data-stu-id="78902-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="78902-114">Suppression des applets de commande faisant référence aux composants internes et aux fonctionnalités sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="78902-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="78902-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="78902-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="78902-116">Création d’un module pour gérer les versions des applets de commande Azure PowerShell par le biais de l’utilisation des profils de version</span><span class="sxs-lookup"><span data-stu-id="78902-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>