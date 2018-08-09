---
title: Utilisation des modules Azure PowerShell expérimentaux
description: Comprenez l’utilisation et la philosophie des modules Azure PowerShell expérimentaux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: ac571363d79c83b268b5c25f65b14f16d4b86e71
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653659"
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="8c74c-103">Utilisation des modules Azure PowerShell expérimentaux</span><span class="sxs-lookup"><span data-stu-id="8c74c-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="8c74c-104">En mettant l’accent sur les outils de développement (surtout les CLI) dans Azure, l’équipe Azure PowerShell peut apporter de nombreuses améliorations de l’expérience d’utilisation d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c74c-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="8c74c-105">Méthodologie d’expérimentation</span><span class="sxs-lookup"><span data-stu-id="8c74c-105">Experimentation methodology</span></span>

<span data-ttu-id="8c74c-106">Pour faciliter l’expérimentation, nous créons des modules Azure PowerShell qui implémentent les fonctionnalités existantes de Microsoft Azure SDK grâce à de nouvelles méthodes, plus simples.</span><span class="sxs-lookup"><span data-stu-id="8c74c-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="8c74c-107">Dans la plupart des cas, les cmdlets reflètent exactement les cmdlets existantes.</span><span class="sxs-lookup"><span data-stu-id="8c74c-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="8c74c-108">Toutefois, les cmdlets expérimentales fournissent une notation abrégée et des valeurs par défaut plus intelligentes, qui facilitent la création et la gestion des ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="8c74c-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="8c74c-109">Ces modules peuvent être installés en parallèle avec des modules Azure PowerShell existants.</span><span class="sxs-lookup"><span data-stu-id="8c74c-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="8c74c-110">Les noms de cmdlet ont été raccourcis, de manière à éviter les conflits de noms avec des cmdlets existantes, non expérimentales.</span><span class="sxs-lookup"><span data-stu-id="8c74c-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="8c74c-111">Les modules expérimentaux utilisent la convention d’affectation de noms suivante : `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="8c74c-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="8c74c-112">Cette convention d’affectation de noms est similaire à la dénomination des modules de préversion : `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="8c74c-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="8c74c-113">Les modules de préversion diffèrent des modules expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="8c74c-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="8c74c-114">Ils implémentent de nouvelles fonctionnalités des services Azure qui sont uniquement disponibles en tant qu’offre de préversion.</span><span class="sxs-lookup"><span data-stu-id="8c74c-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="8c74c-115">Les modules de préversion remplacent les modules Azure PowerShell existants et utilisent les mêmes noms de paramètre et de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c74c-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="8c74c-116">Comment installer un module expérimental</span><span class="sxs-lookup"><span data-stu-id="8c74c-116">How to install an experimental module</span></span>

<span data-ttu-id="8c74c-117">Les modules expérimentaux sont publiés dans PowerShell Gallery, comme les modules Azure PowerShell existants.</span><span class="sxs-lookup"><span data-stu-id="8c74c-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="8c74c-118">Pour consulter une liste de modules expérimentaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8c74c-118">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="8c74c-119">Pour installer le module expérimental, utilisez les commandes suivantes à partir d’une session PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="8c74c-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="8c74c-120">Documentation et support</span><span class="sxs-lookup"><span data-stu-id="8c74c-120">Documentation and support</span></span>

<span data-ttu-id="8c74c-121">La documentation est incluse dans le package d’installation et est accessible à l’aide de la cmdlet `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="8c74c-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="8c74c-122">Aucune documentation officielle n’est publiée pour les modules expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="8c74c-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="8c74c-123">Nous vous encourageons à tester ces modules.</span><span class="sxs-lookup"><span data-stu-id="8c74c-123">We encourage you to test these modules.</span></span> <span data-ttu-id="8c74c-124">Vos commentaires nous permettent d’améliorer la facilité d’utilisation et de répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="8c74c-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="8c74c-125">Toutefois, comme il s’agit d’une fonctionnalité expérimentale, la prise en charge de ces modules est limitée.</span><span class="sxs-lookup"><span data-stu-id="8c74c-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="8c74c-126">Vous pouvez poser vos questions ou signaler des problèmes en créant un [problème](https://github.com/Azure/azure-powershell/issues) dans le référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="8c74c-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="8c74c-127">Expérimentation et domaines à améliorer</span><span class="sxs-lookup"><span data-stu-id="8c74c-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="8c74c-128">Ces améliorations ont été sélectionnées en fonction des principaux atouts des produits concurrents.</span><span class="sxs-lookup"><span data-stu-id="8c74c-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="8c74c-129">Par exemple, Azure CLI 2.0 s’efforce de baser ses commandes sur des _scénarios_ plutôt que sur _une surface d’exposition des API_.</span><span class="sxs-lookup"><span data-stu-id="8c74c-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="8c74c-130">Azure CLI 2.0 utilise différentes valeurs par défaut intelligentes, qui facilitent la compréhension des scénarios de démarrage par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="8c74c-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="8c74c-131">Améliorations principales</span><span class="sxs-lookup"><span data-stu-id="8c74c-131">Core improvements</span></span>

<span data-ttu-id="8c74c-132">Les améliorations principales sont considérées comme des optimisations de « bon sens », et l’implémentation de ces mises à jour requiert une expérimentation limitée.</span><span class="sxs-lookup"><span data-stu-id="8c74c-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="8c74c-133">Cmdlets basées sur des scénarios : - \**toutes* les cmdlets doivent être conçues sur la base de scénarios, et non du service REST Azure.</span><span class="sxs-lookup"><span data-stu-id="8c74c-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="8c74c-134">Noms plus courts : cela inclut les noms des cmdlets (par exemple, `New-AzureRmVM` => `New-AzVm`) et les noms des paramètres (par exemple, `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="8c74c-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="8c74c-135">Utilisez des alias pour assurer la compatibilité avec les « anciennes » cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8c74c-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="8c74c-136">Fournissez des ensembles de paramètres _à compatibilité descendante_.</span><span class="sxs-lookup"><span data-stu-id="8c74c-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="8c74c-137">Valeurs par défaut intelligentes : créez des valeurs par défaut intelligentes pour indiquer les informations « requises ».</span><span class="sxs-lookup"><span data-stu-id="8c74c-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="8c74c-138">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="8c74c-138">For example:</span></span>
  - <span data-ttu-id="8c74c-139">Groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="8c74c-139">Resource Group</span></span>
  - <span data-ttu-id="8c74c-140">Lieu</span><span class="sxs-lookup"><span data-stu-id="8c74c-140">Location</span></span>
  - <span data-ttu-id="8c74c-141">Ressources dépendantes</span><span class="sxs-lookup"><span data-stu-id="8c74c-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="8c74c-142">Améliorations expérimentales</span><span class="sxs-lookup"><span data-stu-id="8c74c-142">Experimental improvements</span></span>

<span data-ttu-id="8c74c-143">Les améliorations expérimentales présentent une modification importante que l’équipe souhaite valider à l’aide d’une expérimentation.</span><span class="sxs-lookup"><span data-stu-id="8c74c-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="8c74c-144">Types simples : les scénarios de création doivent s’éloigner des types et des objets de configuration complexes.</span><span class="sxs-lookup"><span data-stu-id="8c74c-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="8c74c-145">Simplifiez la configuration à un ou deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="8c74c-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="8c74c-146">« Création intelligente » : tous les scénarios de création qui implémentent la fonction de « création intelligente » ne disposent d’_aucun_ paramètre requis ; toutes les informations requises sont choisies par Azure PowerShell de manière répétée.</span><span class="sxs-lookup"><span data-stu-id="8c74c-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="8c74c-147">Paramètres « gris » : dans de nombreux cas, certains paramètres peuvent être « gris », ou semi-facultatifs.</span><span class="sxs-lookup"><span data-stu-id="8c74c-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="8c74c-148">Si le paramètre n’est pas spécifié, l’utilisateur est invité à indiquer s’il veut qu’il soit généré pour lui.</span><span class="sxs-lookup"><span data-stu-id="8c74c-148">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="8c74c-149">Il est également judicieux pour les paramètres « gris » de déduire une valeur en fonction du contexte, avec le consentement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c74c-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="8c74c-150">Par exemple, il peut être judicieux de faire en sorte que le paramètre « gris » suggère la valeur utilisée le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="8c74c-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="8c74c-151">Commutateur `-Auto` : le commutateur `-Auto` doit fournir une option d’abonnement pour permettre aux utilisateurs _de définir tous les éléments sur leur valeur par défaut_ tout en gérant l’intégrité des paramètres requis dans le chemin principal.</span><span class="sxs-lookup"><span data-stu-id="8c74c-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="8c74c-152">Commutateurs spécifiques aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="8c74c-152">Feature-specific switches</span></span>

<span data-ttu-id="8c74c-153">Par exemple, le scénario de « Création d’application web » peut avoir un commutateur `-Git` ou `-AddRemote` qui ajoutera automatiquement un élément « azure » distant à un référentiel git existant.</span><span class="sxs-lookup"><span data-stu-id="8c74c-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="8c74c-154">Valeurs par défaut définissables : les utilisateurs doivent être à même de définir certains paramètres omniprésents sur la valeur par défaut, tels que `-ResourceGroupName` et `-Location`.</span><span class="sxs-lookup"><span data-stu-id="8c74c-154">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="8c74c-155">Valeurs par défaut de la taille : les « tailles » des ressources peuvent être difficiles à comprendre pour les utilisateurs, car de nombreux fournisseurs de ressources utilisent des noms différents (par exemple, « Standard\_DS1\_v2 » ou « S1 »).</span><span class="sxs-lookup"><span data-stu-id="8c74c-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="8c74c-156">Toutefois, la plupart des utilisateurs se préoccupent surtout des coûts.</span><span class="sxs-lookup"><span data-stu-id="8c74c-156">However, most users care more about cost.</span></span> <span data-ttu-id="8c74c-157">Pour cette raison, il est judicieux de définir des tailles « universelles » selon un calendrier de tarification.</span><span class="sxs-lookup"><span data-stu-id="8c74c-157">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="8c74c-158">Les utilisateurs peuvent choisir une taille spécifique, ou laisser à Azure PowerShell le soin de choisir le _meilleure option_ en fonction de la ressource et du budget.</span><span class="sxs-lookup"><span data-stu-id="8c74c-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="8c74c-159">Format de sortie : actuellement, Azure PowerShell renvoie des éléments `PSObject` et la sortie de console est limitée.</span><span class="sxs-lookup"><span data-stu-id="8c74c-159">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="8c74c-160">Azure PowerShell peut avoir besoin d’afficher certaines informations à l’utilisateur concernant les « valeurs par défaut intelligentes » utilisées.</span><span class="sxs-lookup"><span data-stu-id="8c74c-160">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>
