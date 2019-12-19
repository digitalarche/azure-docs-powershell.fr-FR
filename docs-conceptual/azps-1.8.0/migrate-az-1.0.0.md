---
title: Tous les changements d’AzureRM à Azure PowerShell Az 1.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: ea7593cf2b753b210ff2955b7bd450030ad83596
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035827"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="85436-103">Changements cassants pour Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="85436-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="85436-104">Ce document fournit des informations détaillées sur les changements intervenus entre AzureRM 6.x et le nouveau module Az version 1.x et ultérieure.</span><span class="sxs-lookup"><span data-stu-id="85436-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="85436-105">La table des matières constitue un guide du parcours de migration complet, notamment en ce qui concerne les modifications spécifiques aux modules susceptibles d’affecter vos scripts.</span><span class="sxs-lookup"><span data-stu-id="85436-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="85436-106">Pour obtenir des conseils généraux sur la préparation d’une migration d’AzureRM vers Az, consultez [Démarrer la migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="85436-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="85436-107">Sommaire</span><span class="sxs-lookup"><span data-stu-id="85436-107">Table of Contents</span></span>

- [<span data-ttu-id="85436-108">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="85436-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="85436-109">Modifications des préfixes des noms des applets de commande</span><span class="sxs-lookup"><span data-stu-id="85436-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="85436-110">Modifications de nom de module</span><span class="sxs-lookup"><span data-stu-id="85436-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="85436-111">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="85436-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="85436-112">Windows PowerShell 5.1 et .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="85436-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="85436-113">Suppression temporaire de la connexion de l’utilisateur avec PSCredential</span><span class="sxs-lookup"><span data-stu-id="85436-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="85436-114">Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web</span><span class="sxs-lookup"><span data-stu-id="85436-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="85436-115">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="85436-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="85436-116">Az.ApiManagement (précédemment AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="85436-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="85436-117">Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="85436-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="85436-118">Az.CognitiveServices (précédemment AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="85436-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="85436-119">Az.Compute (précédemment AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="85436-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="85436-120">Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="85436-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="85436-121">Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="85436-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="85436-122">Az.DataLakeStore (précédemment AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="85436-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="85436-123">Az.KeyVault (précédemment AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="85436-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="85436-124">Az.Media (précédemment AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="85436-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="85436-125">Az.Monitor (précédemment AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="85436-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="85436-126">Az.Network (précédemment AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="85436-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="85436-127">Az.OperationalInsights (précédemment AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="85436-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="85436-128">Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="85436-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="85436-129">Az.Resources (précédemment AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="85436-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="85436-130">Az.ServiceFabric (précédemment AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="85436-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="85436-131">Az.Sql (précédemment AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="85436-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="85436-132">Az.Storage (précédemment Azure.Storage et AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="85436-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="85436-133">Az.Websites (précédemment AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="85436-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="85436-134">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="85436-134">General breaking changes</span></span>

<span data-ttu-id="85436-135">Cette section détaille les changements cassants généraux qui font partie de cette reconception du module Az.</span><span class="sxs-lookup"><span data-stu-id="85436-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="85436-136">Modifications de préfixe de nom de cmdlet</span><span class="sxs-lookup"><span data-stu-id="85436-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="85436-137">Dans le module AzureRM, les applets de commande utilisaient `AzureRM` ou `Azure` comme préfixes pour les noms.</span><span class="sxs-lookup"><span data-stu-id="85436-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="85436-138">Az simplifie et normalise les noms des applets de commande : elles utilisent dorénavant toutes « Az » comme préfixe pour leurs noms.</span><span class="sxs-lookup"><span data-stu-id="85436-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="85436-139">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="85436-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="85436-140">A été remplacé par :</span><span class="sxs-lookup"><span data-stu-id="85436-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="85436-141">Pour simplifier la transition vers ces nouveaux noms des applets de commande, Az introduit deux nouvelles applets de commande : [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) et [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="85436-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="85436-142">`Enable-AzureRmAlias` crée des alias pour les anciens noms des applets de commande dans AzureRM qui établissent la correspondance avec leurs nouveaux noms dans Az.</span><span class="sxs-lookup"><span data-stu-id="85436-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="85436-143">L’utilisation de l’argument `-Scope` avec `Enable-AzureRmAlias` vous permet de choisir où les alias sont activés.</span><span class="sxs-lookup"><span data-stu-id="85436-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="85436-144">Par exemple, le script suivant dans AzureRM :</span><span class="sxs-lookup"><span data-stu-id="85436-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="85436-145">Peut être exécuté avec des modifications minimes à l’aide de `Enable-AzureRmAlias` :</span><span class="sxs-lookup"><span data-stu-id="85436-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="85436-146">L’exécution de `Enable-AzureRmAlias -Scope CurrentUser` active les alias pour toutes les sessions PowerShell que vous ouvrez. Ainsi, après l’exécution de cette applet de commande, un script comme celui-ci ne nécessite aucune modification :</span><span class="sxs-lookup"><span data-stu-id="85436-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="85436-147">Pour plus d’informations sur l’utilisation des alias des applets de commande, consultez les [Informations de référence sur Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="85436-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="85436-148">Quand vous êtes prêt à désactiver les alias, `Disable-AzureRmAlias` supprime les alias créés.</span><span class="sxs-lookup"><span data-stu-id="85436-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="85436-149">Pour plus d’informations, consultez les [Informations de référence sur Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="85436-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85436-150">Quand vous désactivez les alias, vérifiez qu’ils sont désactivés pour _toutes_ les étendues où les alias étaient activés.</span><span class="sxs-lookup"><span data-stu-id="85436-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="85436-151">Modifications de nom de module</span><span class="sxs-lookup"><span data-stu-id="85436-151">Module Name Changes</span></span>

<span data-ttu-id="85436-152">Les noms de module ont été modifiés de `AzureRM.*` vers `Az.*`, sauf pour les modules suivants :</span><span class="sxs-lookup"><span data-stu-id="85436-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="85436-153">Module AzureRM</span><span class="sxs-lookup"><span data-stu-id="85436-153">AzureRM module</span></span> | <span data-ttu-id="85436-154">Module Az</span><span class="sxs-lookup"><span data-stu-id="85436-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="85436-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="85436-155">Azure.Storage</span></span> | <span data-ttu-id="85436-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="85436-156">Az.Storage</span></span> |
| <span data-ttu-id="85436-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85436-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="85436-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="85436-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="85436-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="85436-159">AzureRM.Profile</span></span> | <span data-ttu-id="85436-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="85436-160">Az.Accounts</span></span> |
| <span data-ttu-id="85436-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="85436-161">AzureRM.Insights</span></span> | <span data-ttu-id="85436-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="85436-162">Az.Monitor</span></span> |
| <span data-ttu-id="85436-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="85436-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="85436-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85436-164">Az.DataFactory</span></span> |
| <span data-ttu-id="85436-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="85436-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="85436-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="85436-166">Az.DataFactory</span></span> |
| <span data-ttu-id="85436-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="85436-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="85436-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85436-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="85436-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="85436-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="85436-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="85436-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="85436-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="85436-171">AzureRM.Tags</span></span> | <span data-ttu-id="85436-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="85436-172">Az.Resources</span></span> |
| <span data-ttu-id="85436-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="85436-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="85436-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="85436-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="85436-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="85436-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="85436-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="85436-176">Az.Billing</span></span> |
| <span data-ttu-id="85436-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="85436-177">AzureRM.Consumption</span></span> | <span data-ttu-id="85436-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="85436-178">Az.Billing</span></span> |

<span data-ttu-id="85436-179">Les modifications dans les noms de module signifient que n’importe quel script qui utilise `#Requires` ou `Import-Module` pour charger des modules spécifiques devra être modifié pour utiliser le nouveau module à la place.</span><span class="sxs-lookup"><span data-stu-id="85436-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="85436-180">Pour les modules où le suffixe des applets de commande n’a pas changé, cela signifie que, bien que le nom du module ait changé, le suffixe indiquant l’espace des opérations n’a _pas_ changé.</span><span class="sxs-lookup"><span data-stu-id="85436-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="85436-181">Migration des instructions #Requires et Import-Module</span><span class="sxs-lookup"><span data-stu-id="85436-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="85436-182">Les scripts qui utilisent `#Requires`ou `Import-Module` pour déclarer une dépendance vis-à-vis de modules AzureRM doivent être mis à jour de façon à utiliser les nouveaux noms des modules.</span><span class="sxs-lookup"><span data-stu-id="85436-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="85436-183">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="85436-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="85436-184">Doit être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="85436-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="85436-185">Pour `Import-Module` :</span><span class="sxs-lookup"><span data-stu-id="85436-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="85436-186">Doit être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="85436-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="85436-187">Migration des appels de cmdlet complets</span><span class="sxs-lookup"><span data-stu-id="85436-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="85436-188">Les scripts qui utilisent des appels d’applets de commande qualifiés par module, comme :</span><span class="sxs-lookup"><span data-stu-id="85436-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="85436-189">doivent être modifiés de façon à utiliser les nouveaux noms des modules et des applets de commande :</span><span class="sxs-lookup"><span data-stu-id="85436-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="85436-190">Migration des dépendances de manifeste de module</span><span class="sxs-lookup"><span data-stu-id="85436-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="85436-191">Pour les modules qui expriment des dépendances vis-à-vis de modules AzureRM via un fichier manifeste de module (.psd1), vous devez mettre à jour les noms des modules dans leur section `RequiredModules` :</span><span class="sxs-lookup"><span data-stu-id="85436-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="85436-192">Doit être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="85436-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="85436-193">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="85436-193">Removed modules</span></span>

<span data-ttu-id="85436-194">Les modules suivants ont été supprimés :</span><span class="sxs-lookup"><span data-stu-id="85436-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="85436-195">Les outils pour ces services ne sont plus activement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="85436-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="85436-196">Les clients sont encouragés à choisir d’autres services dès que possible.</span><span class="sxs-lookup"><span data-stu-id="85436-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="85436-197">Windows PowerShell 5.1 et .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="85436-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="85436-198">L’utilisation d’Az avec PowerShell 5.1 pour Windows nécessite l’installation de .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="85436-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="85436-199">L’utilisation de PowerShell Core 6.x ou ultérieur ne nécessite pas le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="85436-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="85436-200">Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential</span><span class="sxs-lookup"><span data-stu-id="85436-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="85436-201">En raison de modifications dans le flux d’authentification pour .NET Standard, nous supprimons temporairement la connexion utilisateur via PSCredential.</span><span class="sxs-lookup"><span data-stu-id="85436-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="85436-202">Cette fonctionnalité sera réintroduite dans la version du 15/01/2019 pour PowerShell 5.1 pour Windows.</span><span class="sxs-lookup"><span data-stu-id="85436-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="85436-203">Les détails sont abordés dans [ce problème GitHub.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="85436-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="85436-204">Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web</span><span class="sxs-lookup"><span data-stu-id="85436-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="85436-205">En raison de modifications dans le flux d’authentification pour .NET Standard, nous utilisons la connexion à l’appareil en tant que flux de connexion par défaut lors de la connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="85436-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="85436-206">La connexion basée sur un navigateur web sera réintroduite pour PowerShell 5.1 pour Windows comme option par défaut dans la version du 15/01/2019.</span><span class="sxs-lookup"><span data-stu-id="85436-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="85436-207">À ce moment, les utilisateurs seront en mesure de se connecter à l’appareil à l’aide d’un paramètre de commutateur.</span><span class="sxs-lookup"><span data-stu-id="85436-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="85436-208">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="85436-208">Module breaking changes</span></span>

<span data-ttu-id="85436-209">Cette section détaille les changements cassants spécifiques à des applets de commande et des modules individuels.</span><span class="sxs-lookup"><span data-stu-id="85436-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="85436-210">Az.ApiManagement (précédemment AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="85436-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="85436-211">Les applets de commande suivantes ont été supprimées :</span><span class="sxs-lookup"><span data-stu-id="85436-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="85436-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="85436-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="85436-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="85436-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="85436-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="85436-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="85436-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="85436-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="85436-216">Utilisez à la place l’applet de commande **Set-AzApiManagement** pour définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="85436-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="85436-217">Les propriétés suivantes ont été supprimées :</span><span class="sxs-lookup"><span data-stu-id="85436-217">Removed the following properties:</span></span>
  - <span data-ttu-id="85436-218">Suppression des propriétés `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` et `ScmHostnameConfiguration` de type `PsApiManagementHostnameConfiguration` dans `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="85436-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="85436-219">À la place, utilisez `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` et `ScmCustomHostnameConfiguration` de type `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="85436-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="85436-220">Suppression de la propriété `StaticIPs` dans PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="85436-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="85436-221">La propriété a été divisée en `PublicIPAddresses` et `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="85436-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="85436-222">Suppression de la propriété obligatoire `Location` dans la cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="85436-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="85436-223">Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="85436-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="85436-224">Le paramètre `InvoiceName` a été supprimé de la cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="85436-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="85436-225">Les scripts doivent utiliser d’autres paramètres d’identité pour la facture.</span><span class="sxs-lookup"><span data-stu-id="85436-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="85436-226">Az.CognitiveServices (précédemment AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="85436-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="85436-227">Suppression du jeu de paramètres `GetSkusWithAccountParamSetName` dans la cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="85436-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="85436-228">Vous devez obtenir des références (SKU) par type de compte et emplacement, au lieu d’utiliser ResourceGroupName et le nom du compte.</span><span class="sxs-lookup"><span data-stu-id="85436-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="85436-229">Az.Compute (précédemment AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="85436-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="85436-230">`IdentityIds` sont supprimés de la propriété `Identity` dans les objets `PSVirtualMachine` et `PSVirtualMachineScaleSet`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="85436-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="85436-231">Le type de la propriété `InstanceView` de l’objet `PSVirtualMachineScaleSetVM` passe de `VirtualMachineInstanceView` à `VirtualMachineScaleSetVMInstanceView`.</span><span class="sxs-lookup"><span data-stu-id="85436-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="85436-232">Les propriétés `AutoOSUpgradePolicy` et `AutomaticOSUpgrade` sont supprimées de la propriété `UpgradePolicy`.</span><span class="sxs-lookup"><span data-stu-id="85436-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="85436-233">Le type de la propriété `Sku` de l’objet `PSSnapshotUpdate` passe de `DiskSku` à `SnapshotSku`.</span><span class="sxs-lookup"><span data-stu-id="85436-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="85436-234">`VmScaleSetVMParameterSet` est supprimé de la cmdlet `Add-AzVMDataDisk`. Vous ne pouvez plus ajouter un disque de données individuellement à une machine virtuelle ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="85436-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="85436-235">Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="85436-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="85436-236">Le paramètre `GatewayName` est devenu obligatoire dans la cmdlet `New-AzDataFactoryEncryptValue`.</span><span class="sxs-lookup"><span data-stu-id="85436-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="85436-237">Suppression de la cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="85436-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="85436-238">Paramètre `LinkedServiceName` supprimé de la cmdlet `Get-AzDataFactoryV2ActivityRun`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="85436-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="85436-239">Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="85436-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="85436-240">Suppression des cmdlets déconseillées : `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, et `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="85436-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="85436-241">Az.DataLakeStore (précédemment AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="85436-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="85436-242">Dans les cmdlets suivantes, le paramètre `Encoding` est passé du type `FileSystemCmdletProviderEncoding` à `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="85436-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="85436-243">Cette modification supprime les valeurs de codage `String` et `Oem`.</span><span class="sxs-lookup"><span data-stu-id="85436-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="85436-244">Toutes les autres valeurs de codage préalables demeurent identiques.</span><span class="sxs-lookup"><span data-stu-id="85436-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="85436-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="85436-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="85436-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="85436-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="85436-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="85436-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="85436-248">Suppression de l’alias de propriété `Tags` déconseillé dans les cmdlets `New-AzDataLakeStoreAccount` et `Set-AzDataLakeStoreAccount`.</span><span class="sxs-lookup"><span data-stu-id="85436-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="85436-249">Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="85436-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="85436-250">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="85436-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="85436-251">Suppression des propriétés déconseillées `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` et `FirewallAllowAzureIps` de l’objet `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="85436-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="85436-252">Aucun script utilisant l’élément `PSDatalakeStoreAccount` renvoyé par `Get-AzDataLakeStoreAccount` ne doit référencer ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="85436-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="85436-253">Az.KeyVault (précédemment AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="85436-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="85436-254">La propriété `PurgeDisabled` a été supprimée des objets `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` et `PSKeyVaultSecretAttributes`. Les scripts ne doivent plus faire référence à la propriété ```PurgeDisabled``` pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="85436-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="85436-255">Az.Media (précédemment AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="85436-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="85436-256">Suppression de l’alias de propriété `Tags` déconseillé de la cmdlet `New-AzMediaService`. Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="85436-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="85436-257">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="85436-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="85436-258">Az.Monitor (précédemment AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="85436-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="85436-259">Suppression des paramètres `Categories` et `Timegrains` avec des noms pluriels en faveur des noms de paramètre au singulier dans la cmdlet `Set-AzDiagnosticSetting`. Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="85436-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="85436-260">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="85436-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="85436-261">Az.Network (précédemment AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="85436-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="85436-262">Suppression du paramètre déconseillé `ResourceId` de la cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="85436-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="85436-263">Suppression de la propriété déconseillée `EnableVmProtection` de l’objet `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="85436-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="85436-264">Suppression de la cmdlet déconseillée `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="85436-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="85436-265">Les scripts ne doivent plus décider des traitements sur la base des valeurs de ces champs.</span><span class="sxs-lookup"><span data-stu-id="85436-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="85436-266">Az.OperationalInsights (précédemment AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="85436-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="85436-267">Le jeu de paramètres par défaut pour `Get-AzOperationalInsightsDataSource` est supprimé, et `ByWorkspaceNameByKind` est devenu le jeu de paramètres par défaut</span><span class="sxs-lookup"><span data-stu-id="85436-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="85436-268">Tout script qui répertorie des sources de données utilisant</span><span class="sxs-lookup"><span data-stu-id="85436-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="85436-269">Doit être modifié selon un type spécifique</span><span class="sxs-lookup"><span data-stu-id="85436-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="85436-270">Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="85436-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="85436-271">Suppression du paramètre `Encryption` dans la cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="85436-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="85436-272">Le paramètre `TargetStorageAccountName` est maintenant obligatoire pour les restaurations de disque managé dans la cmdlet `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="85436-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="85436-273">Suppression des paramètres `StorageAccountName` et `StorageAccountResourceGroupName` dans la cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="85436-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="85436-274">Suppression du paramètre `Name` dans la cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="85436-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="85436-275">Az.Resources (précédemment AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="85436-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="85436-276">Suppression du paramètre `Sku` dans la cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="85436-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="85436-277">Suppression du paramètre `Password` dans les cmdlets `New-AzADServicePrincipal` et `New-AzADSpCredential`. Les mots de passe sont automatiquement générés. Tout script qui a fourni le mot de passe :</span><span class="sxs-lookup"><span data-stu-id="85436-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="85436-278">Doit être changé de façon à récupérer le mot de passe à partir de la sortie :</span><span class="sxs-lookup"><span data-stu-id="85436-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="85436-279">Az.ServiceFabric (précédemment AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="85436-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="85436-280">Les types de retour de cmdlet suivants ont été modifiés :</span><span class="sxs-lookup"><span data-stu-id="85436-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="85436-281">La propriété `ServiceTypeHealthPolicies` de type `ApplicationHealthPolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="85436-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="85436-282">La propriété `ApplicationHealthPolicies` de type `ClusterUpgradeDeltaHealthPolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="85436-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="85436-283">La propriété `OverrideUserUpgradePolicy` de type `ClusterUpgradePolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="85436-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="85436-284">Ces modifications influent sur les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="85436-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="85436-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="85436-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="85436-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="85436-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="85436-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="85436-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="85436-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="85436-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="85436-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="85436-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="85436-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="85436-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="85436-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="85436-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="85436-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="85436-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="85436-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="85436-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="85436-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="85436-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="85436-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="85436-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="85436-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="85436-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="85436-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="85436-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="85436-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="85436-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="85436-299">Az.Sql (précédemment AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="85436-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="85436-300">Suppression des paramètres `State` et `ResourceId` dans la cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="85436-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="85436-301">Suppression des cmdlets déconseillées : `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="85436-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="85436-302">Suppression du paramètre déconseillé `Current` de la cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="85436-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="85436-303">Suppression du paramètre déconseillé `DatabaseName` de la cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="85436-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="85436-304">Suppression du paramètre déconseillé `PrivilegedLogin` de la cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="85436-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="85436-305">Az.Storage (précédemment Azure.Storage et AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="85436-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="85436-306">Pour prendre en charge la création d’un contexte de stockage Oauth avec uniquement le nom du compte de stockage, le jeu de paramètres par défaut a été remplacé par `OAuthParameterSet`.</span><span class="sxs-lookup"><span data-stu-id="85436-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="85436-307">Exemple : `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="85436-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="85436-308">Le paramètre `Location` est devenu obligatoire dans la cmdlet `Get-AzStorageUsage`.</span><span class="sxs-lookup"><span data-stu-id="85436-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="85436-309">Les méthodes d’API de stockage utilisent maintenant le modèle asynchrone basé sur des tâches (TAP), au lieu d’appels d’API synchrones.</span><span class="sxs-lookup"><span data-stu-id="85436-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="85436-310">Les exemples suivants montrent les nouvelles commandes asynchrones :</span><span class="sxs-lookup"><span data-stu-id="85436-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="85436-311">Instantané d’objet blob</span><span class="sxs-lookup"><span data-stu-id="85436-311">Blob Snapshot</span></span>

<span data-ttu-id="85436-312">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="85436-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="85436-313">Az :</span><span class="sxs-lookup"><span data-stu-id="85436-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="85436-314">Partager l’instantané</span><span class="sxs-lookup"><span data-stu-id="85436-314">Share Snapshot</span></span>

<span data-ttu-id="85436-315">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="85436-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="85436-316">Az :</span><span class="sxs-lookup"><span data-stu-id="85436-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="85436-317">Annuler la suppression d’un objet blob supprimé de manière réversible</span><span class="sxs-lookup"><span data-stu-id="85436-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="85436-318">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="85436-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="85436-319">Az :</span><span class="sxs-lookup"><span data-stu-id="85436-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="85436-320">Définir un niveau d’objet blob</span><span class="sxs-lookup"><span data-stu-id="85436-320">Set Blob Tier</span></span>

<span data-ttu-id="85436-321">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="85436-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="85436-322">Az :</span><span class="sxs-lookup"><span data-stu-id="85436-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="85436-323">Az.Websites (précédemment AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="85436-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="85436-324">Suppression des propriétés déconseillées des objets `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` et `PSSite`.</span><span class="sxs-lookup"><span data-stu-id="85436-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
