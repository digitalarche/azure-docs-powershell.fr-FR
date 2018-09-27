---
title: Utilisation des modules Azure PowerShell expérimentaux
description: Comprenez l’utilisation et la philosophie des modules Azure PowerShell expérimentaux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: cb1c49682ea1bfd5fa43baafe4cb0f7fc0c46020
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560437"
---
# <a name="use-experimental-azure-powershell-modules"></a><span data-ttu-id="a4db0-103">Utiliser des modules Azure PowerShell expérimentaux</span><span class="sxs-lookup"><span data-stu-id="a4db0-103">Use experimental Azure PowerShell modules</span></span>

<span data-ttu-id="a4db0-104">En mettant l’accent sur les outils de développement (surtout les CLI) dans Azure, l’équipe Azure PowerShell peut apporter de nombreuses améliorations de l’expérience d’utilisation d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4db0-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="a4db0-105">Méthodologie d’expérimentation</span><span class="sxs-lookup"><span data-stu-id="a4db0-105">Experimentation methodology</span></span>

<span data-ttu-id="a4db0-106">Pour faciliter l’expérimentation, nous créons des modules Azure PowerShell qui implémentent des fonctionnalités déjà existantes de Microsoft Azure SDK avec de nouvelles méthodes, plus simples d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a4db0-106">To facilitate experimentation, we're creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="a4db0-107">Dans la plupart des cas, les cmdlets reflètent exactement les cmdlets existantes.</span><span class="sxs-lookup"><span data-stu-id="a4db0-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="a4db0-108">Toutefois, les cmdlets expérimentales fournissent une notation abrégée et des valeurs par défaut plus intelligentes, qui facilitent la création et la gestion des ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="a4db0-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="a4db0-109">Ces modules peuvent être installés côte à côte avec des modules Azure PowerShell existants.</span><span class="sxs-lookup"><span data-stu-id="a4db0-109">These modules can be installed side by side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="a4db0-110">Les noms de cmdlet ont été raccourcis, de manière à éviter les conflits de noms avec des cmdlets existantes, non expérimentales.</span><span class="sxs-lookup"><span data-stu-id="a4db0-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="a4db0-111">Les modules expérimentaux utilisent la convention d’affectation de noms suivante : `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="a4db0-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="a4db0-112">Cette convention d’affectation de noms est similaire à la dénomination des modules de préversion : `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="a4db0-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="a4db0-113">Les modules de préversion diffèrent des modules expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="a4db0-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="a4db0-114">Ils implémentent de nouvelles fonctionnalités des services Azure qui sont uniquement disponibles en tant qu’offre de préversion.</span><span class="sxs-lookup"><span data-stu-id="a4db0-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="a4db0-115">Les modules de préversion remplacent les modules Azure PowerShell existants et utilisent les mêmes noms de paramètre et de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4db0-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="a4db0-116">Comment installer un module expérimental</span><span class="sxs-lookup"><span data-stu-id="a4db0-116">How to install an experimental module</span></span>

<span data-ttu-id="a4db0-117">Les modules expérimentaux sont publiés dans PowerShell Gallery, comme les modules Azure PowerShell existants.</span><span class="sxs-lookup"><span data-stu-id="a4db0-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="a4db0-118">Pour consulter une liste de modules expérimentaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a4db0-118">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="a4db0-119">Pour installer le module expérimental, utilisez les commandes suivantes à partir d’une session PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="a4db0-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="a4db0-120">Documentation et support</span><span class="sxs-lookup"><span data-stu-id="a4db0-120">Documentation and support</span></span>

<span data-ttu-id="a4db0-121">La documentation est incluse dans le package d’installation et est accessible à l’aide de la cmdlet `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="a4db0-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="a4db0-122">Aucune documentation officielle n’est publiée pour les modules expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="a4db0-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="a4db0-123">Nous vous encourageons à tester ces modules.</span><span class="sxs-lookup"><span data-stu-id="a4db0-123">We encourage you to test these modules.</span></span> <span data-ttu-id="a4db0-124">Vos commentaires nous permettent d’améliorer la facilité d’utilisation et de répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a4db0-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="a4db0-125">Toutefois, comme il s’agit d’une fonctionnalité expérimentale, la prise en charge de ces modules est limitée.</span><span class="sxs-lookup"><span data-stu-id="a4db0-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="a4db0-126">Vous pouvez poser vos questions ou signaler des problèmes en créant un [problème](https://github.com/Azure/azure-powershell/issues) dans le référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="a4db0-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="a4db0-127">Expérimentation et domaines à améliorer</span><span class="sxs-lookup"><span data-stu-id="a4db0-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="a4db0-128">Ces améliorations ont été sélectionnées en fonction des principaux atouts des produits concurrents.</span><span class="sxs-lookup"><span data-stu-id="a4db0-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="a4db0-129">Par exemple, Azure CLI 2.0 s’efforce de baser ses commandes sur des _scénarios_ plutôt que sur _une surface d’exposition des API_.</span><span class="sxs-lookup"><span data-stu-id="a4db0-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="a4db0-130">Azure CLI 2.0 utilise différentes valeurs par défaut intelligentes, qui facilitent la compréhension des scénarios de démarrage par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a4db0-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="a4db0-131">Améliorations principales</span><span class="sxs-lookup"><span data-stu-id="a4db0-131">Core improvements</span></span>

<span data-ttu-id="a4db0-132">Les améliorations principales sont considérées comme des optimisations de « bon sens », et l’implémentation de ces mises à jour requiert une expérimentation limitée.</span><span class="sxs-lookup"><span data-stu-id="a4db0-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="a4db0-133">Cmdlets basées sur des scénarios : - \**toutes* les cmdlets doivent être conçues sur la base de scénarios, et non du service REST Azure.</span><span class="sxs-lookup"><span data-stu-id="a4db0-133">Scenario-based Cmdlets - \**All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="a4db0-134">Noms plus courts : cela inclut les noms des cmdlets (par exemple, `New-AzureRmVM` => `New-AzVm`) et les noms des paramètres (par exemple, `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="a4db0-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="a4db0-135">Utilisez des alias pour assurer la compatibilité avec les « anciennes » cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a4db0-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="a4db0-136">Fournissez des ensembles de paramètres _à compatibilité descendante_.</span><span class="sxs-lookup"><span data-stu-id="a4db0-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="a4db0-137">Valeurs par défaut intelligentes : créez des valeurs par défaut intelligentes pour indiquer les informations « requises ».</span><span class="sxs-lookup"><span data-stu-id="a4db0-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="a4db0-138">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="a4db0-138">For example:</span></span>
  - <span data-ttu-id="a4db0-139">Groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="a4db0-139">Resource Group</span></span>
  - <span data-ttu-id="a4db0-140">Lieu</span><span class="sxs-lookup"><span data-stu-id="a4db0-140">Location</span></span>
  - <span data-ttu-id="a4db0-141">Ressources dépendantes</span><span class="sxs-lookup"><span data-stu-id="a4db0-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="a4db0-142">Améliorations expérimentales</span><span class="sxs-lookup"><span data-stu-id="a4db0-142">Experimental improvements</span></span>

<span data-ttu-id="a4db0-143">Les améliorations expérimentales présentent une modification importante que l’équipe souhaite valider à l’aide d’une expérimentation.</span><span class="sxs-lookup"><span data-stu-id="a4db0-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="a4db0-144">Types simples : les scénarios de création doivent s’éloigner des types et des objets de configuration complexes.</span><span class="sxs-lookup"><span data-stu-id="a4db0-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="a4db0-145">Simplifiez la configuration à un ou deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="a4db0-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="a4db0-146">« Création intelligente » : tous les scénarios de création qui implémentent la fonction de « création intelligente » ne disposent d’_aucun_ paramètre requis ; toutes les informations requises sont choisies par Azure PowerShell de manière répétée.</span><span class="sxs-lookup"><span data-stu-id="a4db0-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="a4db0-147">Paramètres « gris » : dans de nombreux cas, certains paramètres peuvent être « gris », ou semi-facultatifs.</span><span class="sxs-lookup"><span data-stu-id="a4db0-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="a4db0-148">Si le paramètre n’est pas spécifié, l’utilisateur est invité à indiquer s’il souhaite qu’il soit généré pour lui.</span><span class="sxs-lookup"><span data-stu-id="a4db0-148">If the parameter isn't specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="a4db0-149">Il est également judicieux pour les paramètres « gris » de déduire une valeur en fonction du contexte, avec le consentement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a4db0-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="a4db0-150">Par exemple, il peut être judicieux de faire en sorte que le paramètre « gris » suggère la valeur utilisée le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="a4db0-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="a4db0-151">Commutateur `-Auto` : le commutateur `-Auto` doit fournir une option d’abonnement pour permettre aux utilisateurs _de définir tous les éléments sur leur valeur par défaut_ tout en gérant l’intégrité des paramètres requis dans le chemin principal.</span><span class="sxs-lookup"><span data-stu-id="a4db0-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="a4db0-152">Commutateurs spécifiques aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a4db0-152">Feature-specific switches</span></span>

<span data-ttu-id="a4db0-153">Par exemple, le scénario de « Création d’application web » peut avoir un commutateur `-Git` ou `-AddRemote` qui ajoutera automatiquement un élément « azure » distant à un référentiel git existant.</span><span class="sxs-lookup"><span data-stu-id="a4db0-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="a4db0-154">Valeurs par défaut définissables : les utilisateurs doivent être en mesure de définir les valeurs par défaut pour les paramètres communs tels que `-ResourceGroupName` et `-Location`.</span><span class="sxs-lookup"><span data-stu-id="a4db0-154">Settable Defaults - Users should be able to set defaults for common parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="a4db0-155">Valeurs par défaut de la taille : les « tailles » des ressources peuvent être difficiles à comprendre pour les utilisateurs, car de nombreux fournisseurs de ressources utilisent des noms différents (par exemple, « Standard\_DS1\_v2 » ou « S1 »).</span><span class="sxs-lookup"><span data-stu-id="a4db0-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="a4db0-156">Toutefois, la plupart des utilisateurs se préoccupent surtout des coûts.</span><span class="sxs-lookup"><span data-stu-id="a4db0-156">However, most users care more about cost.</span></span> <span data-ttu-id="a4db0-157">C’est pourquoi il est judicieux de définir des tailles « universelles » basées sur un programme de tarification.</span><span class="sxs-lookup"><span data-stu-id="a4db0-157">So it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="a4db0-158">Les utilisateurs peuvent choisir une taille spécifique, ou laisser à Azure PowerShell le soin de choisir le _meilleure option_ en fonction de la ressource et du budget.</span><span class="sxs-lookup"><span data-stu-id="a4db0-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="a4db0-159">Format de sortie : Azure PowerShell renvoie actuellement des éléments `PSObject` et la sortie de console est limitée.</span><span class="sxs-lookup"><span data-stu-id="a4db0-159">Output Format - Azure PowerShell currently returns `PSObject`s and there's little console output.</span></span> <span data-ttu-id="a4db0-160">Azure PowerShell peut avoir besoin d’afficher certaines informations à l’utilisateur concernant les « valeurs par défaut intelligentes » utilisées.</span><span class="sxs-lookup"><span data-stu-id="a4db0-160">Azure PowerShell may need to display some information to the user about the "smart defaults" used.</span></span>
