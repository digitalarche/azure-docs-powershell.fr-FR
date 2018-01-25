---
title: "Utilisation des modules Azure PowerShell expérimentaux"
description: "Comprenez l’utilisation et la philosophie des modules Azure PowerShell expérimentaux."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: 7a01957040be7c0498ef4f0e9b8f7297119221a5
ms.sourcegitcommit: 9d2d35944106bdb6758853b050089bc804e6b9d2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2017
---
# <a name="using-experimental-azure-powershell-modules"></a><span data-ttu-id="16a11-103">Utilisation des modules Azure PowerShell expérimentaux</span><span class="sxs-lookup"><span data-stu-id="16a11-103">Using experimental Azure PowerShell modules</span></span>

<span data-ttu-id="16a11-104">En mettant l’accent sur les outils de développement (surtout les CLI) dans Azure, l’équipe Azure PowerShell peut apporter de nombreuses améliorations de l’expérience d’utilisation d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="16a11-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="16a11-105">Méthodologie d’expérimentation</span><span class="sxs-lookup"><span data-stu-id="16a11-105">Experimentation methodology</span></span>

<span data-ttu-id="16a11-106">Pour faciliter l’expérimentation, nous créons des modules Azure PowerShell qui implémentent les fonctionnalités existantes de Microsoft Azure SDK grâce à de nouvelles méthodes, plus simples.</span><span class="sxs-lookup"><span data-stu-id="16a11-106">To facilitate experimentation, we are creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="16a11-107">Dans la plupart des cas, les cmdlets reflètent exactement les cmdlets existantes.</span><span class="sxs-lookup"><span data-stu-id="16a11-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="16a11-108">Toutefois, les cmdlets expérimentales fournissent une notation abrégée et des valeurs par défaut plus intelligentes, qui facilitent la création et la gestion des ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="16a11-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="16a11-109">Ces modules peuvent être installés en parallèle avec des modules Azure PowerShell existants.</span><span class="sxs-lookup"><span data-stu-id="16a11-109">These modules can be installed side-by-side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="16a11-110">Les noms de cmdlet ont été raccourcis, de manière à éviter les conflits de noms avec des cmdlets existantes, non expérimentales.</span><span class="sxs-lookup"><span data-stu-id="16a11-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="16a11-111">Les modules expérimentaux utilisent la convention d’affectation de noms suivante :</span><span class="sxs-lookup"><span data-stu-id="16a11-111">The experimental modules use the following naming convention:</span></span>

- <span data-ttu-id="16a11-112">AzureRM.Compute.Experiments</span><span class="sxs-lookup"><span data-stu-id="16a11-112">AzureRM.Compute.Experiments</span></span>
- <span data-ttu-id="16a11-113">AzureRM.Websites.Experiments</span><span class="sxs-lookup"><span data-stu-id="16a11-113">AzureRM.Websites.Experiments</span></span>

<span data-ttu-id="16a11-114">Cette convention d’affectation de noms est similaire à la dénomination des modules de préversion : `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="16a11-114">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="16a11-115">Les modules de préversion diffèrent des modules expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="16a11-115">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="16a11-116">Ils implémentent de nouvelles fonctionnalités des services Azure qui sont uniquement disponibles en tant qu’offre de préversion.</span><span class="sxs-lookup"><span data-stu-id="16a11-116">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="16a11-117">Les modules de préversion remplacent les modules Azure PowerShell existants et utilisent les mêmes noms de paramètre et de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16a11-117">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="16a11-118">Comment installer un module expérimental</span><span class="sxs-lookup"><span data-stu-id="16a11-118">How to install an experimental module</span></span>

<span data-ttu-id="16a11-119">Les modules expérimentaux sont publiés dans PowerShell Gallery, comme les modules Azure PowerShell existants.</span><span class="sxs-lookup"><span data-stu-id="16a11-119">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="16a11-120">Pour consulter une liste de modules expérimentaux, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="16a11-120">To see a list of experimental modules, run the following command:</span></span>

```powershell
Find-Module AzureRM.*.Experiments
```

```Output
Version    Name                                Repository           Description
-------    ----                                ----------           -----------
1.0.0      AzureRM.Websites.Experiments        PSGallery            Create and deploy web applications using Azure Ap...
1.0.25     AzureRM.Compute.Experiments         PSGallery            Azure Compute experiments for VM creation
```

<span data-ttu-id="16a11-121">Pour installer le module expérimental, utilisez les commandes suivantes à partir d’une session PowerShell avec élévation de privilèges :</span><span class="sxs-lookup"><span data-stu-id="16a11-121">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```powershell
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="16a11-122">Documentation et support</span><span class="sxs-lookup"><span data-stu-id="16a11-122">Documentation and support</span></span>

<span data-ttu-id="16a11-123">La documentation est incluse dans le package d’installation et est accessible à l’aide de la cmdlet `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="16a11-123">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="16a11-124">Aucune documentation officielle n’est publiée pour les modules expérimentaux.</span><span class="sxs-lookup"><span data-stu-id="16a11-124">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="16a11-125">Nous vous encourageons à tester ces modules.</span><span class="sxs-lookup"><span data-stu-id="16a11-125">We encourage you to test these modules.</span></span> <span data-ttu-id="16a11-126">Vos commentaires nous permettent d’améliorer la facilité d’utilisation et de répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="16a11-126">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="16a11-127">Toutefois, comme il s’agit d’une fonctionnalité expérimentale, la prise en charge de ces modules est limitée.</span><span class="sxs-lookup"><span data-stu-id="16a11-127">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="16a11-128">Vous pouvez poser vos questions ou signaler des problèmes en créant un [problème](https://github.com/Azure/azure-powershell/issues) dans le référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="16a11-128">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="16a11-129">Expérimentation et domaines à améliorer</span><span class="sxs-lookup"><span data-stu-id="16a11-129">Experiments and areas of improvement</span></span>

<span data-ttu-id="16a11-130">Ces améliorations ont été sélectionnées en fonction des principaux atouts des produits concurrents.</span><span class="sxs-lookup"><span data-stu-id="16a11-130">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="16a11-131">Par exemple, Azure CLI 2.0 s’efforce de baser ses commandes sur des _scénarios_ plutôt que sur _une surface d’exposition des API_.</span><span class="sxs-lookup"><span data-stu-id="16a11-131">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="16a11-132">Azure CLI 2.0 utilise différentes valeurs par défaut intelligentes, qui facilitent la compréhension des scénarios de démarrage par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="16a11-132">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="16a11-133">Améliorations principales</span><span class="sxs-lookup"><span data-stu-id="16a11-133">Core improvements</span></span>

<span data-ttu-id="16a11-134">Les améliorations principales sont considérées comme des optimisations de « bon sens », et l’implémentation de ces mises à jour requiert une expérimentation limitée.</span><span class="sxs-lookup"><span data-stu-id="16a11-134">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="16a11-135">Cmdlets basées sur des scénarios : - **toutes* les cmdlets doivent être conçues sur la base de scénarios, et non du service REST Azure.</span><span class="sxs-lookup"><span data-stu-id="16a11-135">Scenario-based Cmdlets - **All*- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="16a11-136">Noms plus courts : cela inclut les noms des cmdlets (par exemple, `New-AzureRmVM` => `New-AzVm`) et les noms des paramètres (par exemple, `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="16a11-136">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="16a11-137">Utilisez des alias pour assurer la compatibilité avec les « anciennes » cmdlets.</span><span class="sxs-lookup"><span data-stu-id="16a11-137">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="16a11-138">Fournissez des ensembles de paramètres _à compatibilité descendante_.</span><span class="sxs-lookup"><span data-stu-id="16a11-138">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="16a11-139">Valeurs par défaut intelligentes : créez des valeurs par défaut intelligentes pour indiquer les informations « requises ».</span><span class="sxs-lookup"><span data-stu-id="16a11-139">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="16a11-140">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="16a11-140">For example:</span></span>
  - <span data-ttu-id="16a11-141">Groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="16a11-141">Resource Group</span></span>
  - <span data-ttu-id="16a11-142">Lieu</span><span class="sxs-lookup"><span data-stu-id="16a11-142">Location</span></span>
  - <span data-ttu-id="16a11-143">Ressources dépendantes</span><span class="sxs-lookup"><span data-stu-id="16a11-143">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="16a11-144">Améliorations expérimentales</span><span class="sxs-lookup"><span data-stu-id="16a11-144">Experimental improvements</span></span>

<span data-ttu-id="16a11-145">Les améliorations expérimentales présentent une modification importante que l’équipe souhaite valider à l’aide d’une expérimentation.</span><span class="sxs-lookup"><span data-stu-id="16a11-145">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="16a11-146">Types simples : les scénarios de création doivent s’éloigner des types et des objets de configuration complexes.</span><span class="sxs-lookup"><span data-stu-id="16a11-146">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="16a11-147">Simplifiez la configuration à un ou deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="16a11-147">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="16a11-148">« Création intelligente » : tous les scénarios de création qui implémentent la fonction de « création intelligente » ne disposent d’_aucun_ paramètre requis ; toutes les informations requises sont choisies par Azure PowerShell de manière répétée.</span><span class="sxs-lookup"><span data-stu-id="16a11-148">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="16a11-149">Paramètres « gris » : dans de nombreux cas, certains paramètres peuvent être « gris », ou semi-facultatifs.</span><span class="sxs-lookup"><span data-stu-id="16a11-149">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="16a11-150">Si le paramètre n’est pas spécifié, l’utilisateur est invité à indiquer s’il veut qu’il soit généré pour lui.</span><span class="sxs-lookup"><span data-stu-id="16a11-150">If the parameter is not specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="16a11-151">Il est également judicieux pour les paramètres « gris » de déduire une valeur en fonction du contexte, avec le consentement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16a11-151">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="16a11-152">Par exemple, il peut être judicieux de faire en sorte que le paramètre « gris » suggère la valeur utilisée le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="16a11-152">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="16a11-153">Commutateur `-Auto` : le commutateur `-Auto` doit fournir une option d’abonnement pour permettre aux utilisateurs _de définir tous les éléments sur leur valeur par défaut_ tout en gérant l’intégrité des paramètres requis dans le chemin principal.</span><span class="sxs-lookup"><span data-stu-id="16a11-153">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="16a11-154">Commutateurs spécifiques aux fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="16a11-154">Feature-specific switches</span></span>

<span data-ttu-id="16a11-155">Par exemple, le scénario de « Création d’application web » peut avoir un commutateur `-Git` ou `-AddRemote` qui ajoutera automatiquement un élément « azure » distant à un référentiel git existant.</span><span class="sxs-lookup"><span data-stu-id="16a11-155">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="16a11-156">Valeurs par défaut définissables : les utilisateurs doivent être à même de définir certains paramètres omniprésents sur la valeur par défaut, tels que `-ResourceGroupName` et `-Location`.</span><span class="sxs-lookup"><span data-stu-id="16a11-156">Settable Defaults - Users should have the ability to default certain ubiquitous parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="16a11-157">Valeurs par défaut de la taille : les « tailles » des ressources peuvent être difficiles à comprendre pour les utilisateurs, car de nombreux fournisseurs de ressources utilisent des noms différents (par exemple, « Standard\_DS1\_v2 » ou « S1 »).</span><span class="sxs-lookup"><span data-stu-id="16a11-157">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="16a11-158">Toutefois, la plupart des utilisateurs se préoccupent surtout des coûts.</span><span class="sxs-lookup"><span data-stu-id="16a11-158">However, most users care more about cost.</span></span> <span data-ttu-id="16a11-159">Pour cette raison, il est judicieux de définir des tailles « universelles » selon un calendrier de tarification.</span><span class="sxs-lookup"><span data-stu-id="16a11-159">Therefore, it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="16a11-160">Les utilisateurs peuvent choisir une taille spécifique, ou laisser à Azure PowerShell le soin de choisir le _meilleure option_ en fonction de la ressource et du budget.</span><span class="sxs-lookup"><span data-stu-id="16a11-160">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="16a11-161">Format de sortie : actuellement, Azure PowerShell renvoie des éléments `PSObject` et la sortie de console est limitée.</span><span class="sxs-lookup"><span data-stu-id="16a11-161">Output Format - Azure PowerShell currently returns `PSObject`s and there is little console output.</span></span> <span data-ttu-id="16a11-162">Azure PowerShell peut avoir besoin d’afficher certaines informations à l’utilisateur concernant les « valeurs par défaut intelligentes » utilisées.</span><span class="sxs-lookup"><span data-stu-id="16a11-162">Azure PowerShell may need to display some information to the user regarding the "smart defaults" used.</span></span>

## <a name="try-using-the-experiments"></a><span data-ttu-id="16a11-163">Essayez de tirer parti des expériences</span><span class="sxs-lookup"><span data-stu-id="16a11-163">Try using the experiments</span></span>

### <a name="install"></a><span data-ttu-id="16a11-164">Installer</span><span class="sxs-lookup"><span data-stu-id="16a11-164">Install</span></span>

```powershell
Install-Module AzureRM.Compute.Experiments
```

### <a name="create-a-vm"></a><span data-ttu-id="16a11-165">Créer une machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="16a11-165">Create a VM</span></span>

```powershell
$job = New-AzVm -Name MyVm -AsJob
Receive-Job $job
```

### <a name="send-us-feedback"></a><span data-ttu-id="16a11-166">Envoyez-nous des commentaires</span><span class="sxs-lookup"><span data-stu-id="16a11-166">Send us feedback</span></span>

```powershell
Send-Feedback
```

### <a name="uninstall-the-experimental-modules"></a><span data-ttu-id="16a11-167">Désinstaller les modules expérimentaux</span><span class="sxs-lookup"><span data-stu-id="16a11-167">Uninstall the experimental modules</span></span>

```powershell
Uninstall-Module AzureRM.Compute.Experiments
```