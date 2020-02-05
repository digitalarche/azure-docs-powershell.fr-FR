---
title: Tous les changements d’AzureRM à Azure PowerShell Az 1.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: e5121d61b0f5f68ff3e1f33d774e3533adfeb64f
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002858"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="168bd-103">Changements cassants pour Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="168bd-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="168bd-104">Ce document fournit des informations détaillées sur les changements intervenus entre AzureRM 6.x et le nouveau module Az version 1.x et ultérieure.</span><span class="sxs-lookup"><span data-stu-id="168bd-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="168bd-105">La table des matières constitue un guide du parcours de migration complet, notamment en ce qui concerne les modifications spécifiques aux modules susceptibles d’affecter vos scripts.</span><span class="sxs-lookup"><span data-stu-id="168bd-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="168bd-106">Pour obtenir des conseils généraux sur la préparation d’une migration d’AzureRM vers Az, consultez [Démarrer la migration d’AzureRM vers Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="168bd-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="168bd-107">Des changements cassants ont également été introduits entre Az 1.0.0 et Az 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="168bd-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="168bd-108">Après avoir suivi ce guide pour la mise à jour d’AzureRM vers Az, consultez les [Changements cassants d’Az 2.0.0](migrate-az-2.0.0.md) pour savoir si vous devez apporter des modifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="168bd-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="168bd-109">Sommaire</span><span class="sxs-lookup"><span data-stu-id="168bd-109">Table of Contents</span></span>

- [<span data-ttu-id="168bd-110">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="168bd-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="168bd-111">Modifications des préfixes des noms des applets de commande</span><span class="sxs-lookup"><span data-stu-id="168bd-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="168bd-112">Modifications de nom de module</span><span class="sxs-lookup"><span data-stu-id="168bd-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="168bd-113">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="168bd-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="168bd-114">Windows PowerShell 5.1 et .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="168bd-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="168bd-115">Suppression temporaire de la connexion de l’utilisateur avec PSCredential</span><span class="sxs-lookup"><span data-stu-id="168bd-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="168bd-116">Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web</span><span class="sxs-lookup"><span data-stu-id="168bd-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="168bd-117">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="168bd-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="168bd-118">Az.ApiManagement (précédemment AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="168bd-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="168bd-119">Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="168bd-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="168bd-120">Az.CognitiveServices (précédemment AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="168bd-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="168bd-121">Az.Compute (précédemment AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="168bd-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="168bd-122">Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="168bd-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="168bd-123">Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="168bd-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="168bd-124">Az.DataLakeStore (précédemment AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="168bd-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="168bd-125">Az.KeyVault (précédemment AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="168bd-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="168bd-126">Az.Media (précédemment AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="168bd-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="168bd-127">Az.Monitor (précédemment AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="168bd-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="168bd-128">Az.Network (précédemment AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="168bd-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="168bd-129">Az.OperationalInsights (précédemment AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="168bd-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="168bd-130">Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="168bd-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="168bd-131">Az.Resources (précédemment AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="168bd-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="168bd-132">Az.ServiceFabric (précédemment AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="168bd-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="168bd-133">Az.Sql (précédemment AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="168bd-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="168bd-134">Az.Storage (précédemment Azure.Storage et AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="168bd-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="168bd-135">Az.Websites (précédemment AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="168bd-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="168bd-136">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="168bd-136">General breaking changes</span></span>

<span data-ttu-id="168bd-137">Cette section détaille les changements cassants généraux qui font partie de cette reconception du module Az.</span><span class="sxs-lookup"><span data-stu-id="168bd-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="168bd-138">Modifications de préfixe de nom de cmdlet</span><span class="sxs-lookup"><span data-stu-id="168bd-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="168bd-139">Dans le module AzureRM, les applets de commande utilisaient `AzureRM` ou `Azure` comme préfixes pour les noms.</span><span class="sxs-lookup"><span data-stu-id="168bd-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="168bd-140">Az simplifie et normalise les noms des applets de commande : elles utilisent dorénavant toutes « Az » comme préfixe pour leurs noms.</span><span class="sxs-lookup"><span data-stu-id="168bd-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="168bd-141">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="168bd-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="168bd-142">A été remplacé par :</span><span class="sxs-lookup"><span data-stu-id="168bd-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="168bd-143">Pour simplifier la transition vers ces nouveaux noms des applets de commande, Az introduit deux nouvelles applets de commande : [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) et [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="168bd-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="168bd-144">`Enable-AzureRmAlias` crée des alias pour les anciens noms des applets de commande dans AzureRM qui établissent la correspondance avec leurs nouveaux noms dans Az.</span><span class="sxs-lookup"><span data-stu-id="168bd-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="168bd-145">L’utilisation de l’argument `-Scope` avec `Enable-AzureRmAlias` vous permet de choisir où les alias sont activés.</span><span class="sxs-lookup"><span data-stu-id="168bd-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="168bd-146">Par exemple, le script suivant dans AzureRM :</span><span class="sxs-lookup"><span data-stu-id="168bd-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="168bd-147">Peut être exécuté avec des modifications minimes à l’aide de `Enable-AzureRmAlias` :</span><span class="sxs-lookup"><span data-stu-id="168bd-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="168bd-148">L’exécution de `Enable-AzureRmAlias -Scope CurrentUser` active les alias pour toutes les sessions PowerShell que vous ouvrez. Ainsi, après l’exécution de cette applet de commande, un script comme celui-ci ne nécessite aucune modification :</span><span class="sxs-lookup"><span data-stu-id="168bd-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="168bd-149">Pour plus d’informations sur l’utilisation des alias des applets de commande, consultez les [Informations de référence sur Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="168bd-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="168bd-150">Quand vous êtes prêt à désactiver les alias, `Disable-AzureRmAlias` supprime les alias créés.</span><span class="sxs-lookup"><span data-stu-id="168bd-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="168bd-151">Pour plus d’informations, consultez les [Informations de référence sur Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="168bd-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="168bd-152">Quand vous désactivez les alias, vérifiez qu’ils sont désactivés pour _toutes_ les étendues où les alias étaient activés.</span><span class="sxs-lookup"><span data-stu-id="168bd-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="168bd-153">Modifications de nom de module</span><span class="sxs-lookup"><span data-stu-id="168bd-153">Module Name Changes</span></span>

<span data-ttu-id="168bd-154">Les noms de module ont été modifiés de `AzureRM.*` vers `Az.*`, sauf pour les modules suivants :</span><span class="sxs-lookup"><span data-stu-id="168bd-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="168bd-155">Module AzureRM</span><span class="sxs-lookup"><span data-stu-id="168bd-155">AzureRM module</span></span> | <span data-ttu-id="168bd-156">Module Az</span><span class="sxs-lookup"><span data-stu-id="168bd-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="168bd-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="168bd-157">Azure.Storage</span></span> | <span data-ttu-id="168bd-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="168bd-158">Az.Storage</span></span> |
| <span data-ttu-id="168bd-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="168bd-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="168bd-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="168bd-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="168bd-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="168bd-161">AzureRM.Profile</span></span> | <span data-ttu-id="168bd-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="168bd-162">Az.Accounts</span></span> |
| <span data-ttu-id="168bd-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="168bd-163">AzureRM.Insights</span></span> | <span data-ttu-id="168bd-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="168bd-164">Az.Monitor</span></span> |
| <span data-ttu-id="168bd-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="168bd-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="168bd-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="168bd-166">Az.DataFactory</span></span> |
| <span data-ttu-id="168bd-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="168bd-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="168bd-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="168bd-168">Az.DataFactory</span></span> |
| <span data-ttu-id="168bd-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="168bd-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="168bd-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="168bd-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="168bd-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="168bd-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="168bd-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="168bd-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="168bd-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="168bd-173">AzureRM.Tags</span></span> | <span data-ttu-id="168bd-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="168bd-174">Az.Resources</span></span> |
| <span data-ttu-id="168bd-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="168bd-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="168bd-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="168bd-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="168bd-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="168bd-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="168bd-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="168bd-178">Az.Billing</span></span> |
| <span data-ttu-id="168bd-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="168bd-179">AzureRM.Consumption</span></span> | <span data-ttu-id="168bd-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="168bd-180">Az.Billing</span></span> |

<span data-ttu-id="168bd-181">Les modifications dans les noms de module signifient que n’importe quel script qui utilise `#Requires` ou `Import-Module` pour charger des modules spécifiques devra être modifié pour utiliser le nouveau module à la place.</span><span class="sxs-lookup"><span data-stu-id="168bd-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="168bd-182">Pour les modules où le suffixe des applets de commande n’a pas changé, cela signifie que, bien que le nom du module ait changé, le suffixe indiquant l’espace des opérations n’a _pas_ changé.</span><span class="sxs-lookup"><span data-stu-id="168bd-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="168bd-183">Migration des instructions #Requires et Import-Module</span><span class="sxs-lookup"><span data-stu-id="168bd-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="168bd-184">Les scripts qui utilisent `#Requires`ou `Import-Module` pour déclarer une dépendance vis-à-vis de modules AzureRM doivent être mis à jour de façon à utiliser les nouveaux noms des modules.</span><span class="sxs-lookup"><span data-stu-id="168bd-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="168bd-185">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="168bd-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="168bd-186">Doit être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="168bd-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="168bd-187">Pour `Import-Module` :</span><span class="sxs-lookup"><span data-stu-id="168bd-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="168bd-188">Doit être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="168bd-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="168bd-189">Migration des appels de cmdlet complets</span><span class="sxs-lookup"><span data-stu-id="168bd-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="168bd-190">Les scripts qui utilisent des appels d’applets de commande qualifiés par module, comme :</span><span class="sxs-lookup"><span data-stu-id="168bd-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="168bd-191">doivent être modifiés de façon à utiliser les nouveaux noms des modules et des applets de commande :</span><span class="sxs-lookup"><span data-stu-id="168bd-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="168bd-192">Migration des dépendances de manifeste de module</span><span class="sxs-lookup"><span data-stu-id="168bd-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="168bd-193">Pour les modules qui expriment des dépendances vis-à-vis de modules AzureRM via un fichier manifeste de module (.psd1), vous devez mettre à jour les noms des modules dans leur section `RequiredModules` :</span><span class="sxs-lookup"><span data-stu-id="168bd-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="168bd-194">Doit être remplacé par :</span><span class="sxs-lookup"><span data-stu-id="168bd-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="168bd-195">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="168bd-195">Removed modules</span></span>

<span data-ttu-id="168bd-196">Les modules suivants ont été supprimés :</span><span class="sxs-lookup"><span data-stu-id="168bd-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="168bd-197">Les outils pour ces services ne sont plus activement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="168bd-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="168bd-198">Les clients sont encouragés à choisir d’autres services dès que possible.</span><span class="sxs-lookup"><span data-stu-id="168bd-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="168bd-199">Windows PowerShell 5.1 et .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="168bd-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="168bd-200">L’utilisation d’Az avec PowerShell 5.1 pour Windows nécessite l’installation de .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="168bd-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="168bd-201">L’utilisation de PowerShell Core 6.x ou ultérieur ne nécessite pas le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="168bd-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="168bd-202">Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential</span><span class="sxs-lookup"><span data-stu-id="168bd-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="168bd-203">En raison de modifications dans le flux d’authentification pour .NET Standard, nous supprimons temporairement la connexion utilisateur via PSCredential.</span><span class="sxs-lookup"><span data-stu-id="168bd-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="168bd-204">Cette fonctionnalité sera réintroduite dans la version du 15/01/2019 pour PowerShell 5.1 pour Windows.</span><span class="sxs-lookup"><span data-stu-id="168bd-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="168bd-205">Les détails sont abordés dans [ce problème GitHub.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="168bd-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="168bd-206">Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web</span><span class="sxs-lookup"><span data-stu-id="168bd-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="168bd-207">En raison de modifications dans le flux d’authentification pour .NET Standard, nous utilisons la connexion à l’appareil en tant que flux de connexion par défaut lors de la connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="168bd-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="168bd-208">La connexion basée sur un navigateur web sera réintroduite pour PowerShell 5.1 pour Windows comme option par défaut dans la version du 15/01/2019.</span><span class="sxs-lookup"><span data-stu-id="168bd-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="168bd-209">À ce moment, les utilisateurs seront en mesure de se connecter à l’appareil à l’aide d’un paramètre de commutateur.</span><span class="sxs-lookup"><span data-stu-id="168bd-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="168bd-210">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="168bd-210">Module breaking changes</span></span>

<span data-ttu-id="168bd-211">Cette section détaille les changements cassants spécifiques à des applets de commande et des modules individuels.</span><span class="sxs-lookup"><span data-stu-id="168bd-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="168bd-212">Az.ApiManagement (précédemment AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="168bd-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="168bd-213">Les applets de commande suivantes ont été supprimées :</span><span class="sxs-lookup"><span data-stu-id="168bd-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="168bd-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="168bd-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="168bd-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="168bd-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="168bd-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="168bd-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="168bd-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="168bd-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="168bd-218">Utilisez à la place l’applet de commande **Set-AzApiManagement** pour définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="168bd-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="168bd-219">Les propriétés suivantes ont été supprimées :</span><span class="sxs-lookup"><span data-stu-id="168bd-219">Removed the following properties:</span></span>
  - <span data-ttu-id="168bd-220">Suppression des propriétés `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` et `ScmHostnameConfiguration` de type `PsApiManagementHostnameConfiguration` dans `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="168bd-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="168bd-221">À la place, utilisez `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` et `ScmCustomHostnameConfiguration` de type `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="168bd-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="168bd-222">Suppression de la propriété `StaticIPs` dans PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="168bd-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="168bd-223">La propriété a été divisée en `PublicIPAddresses` et `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="168bd-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="168bd-224">Suppression de la propriété obligatoire `Location` dans la cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="168bd-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="168bd-225">Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="168bd-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="168bd-226">Le paramètre `InvoiceName` a été supprimé de la cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="168bd-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="168bd-227">Les scripts doivent utiliser d’autres paramètres d’identité pour la facture.</span><span class="sxs-lookup"><span data-stu-id="168bd-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="168bd-228">Az.CognitiveServices (précédemment AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="168bd-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="168bd-229">Suppression du jeu de paramètres `GetSkusWithAccountParamSetName` dans la cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="168bd-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="168bd-230">Vous devez obtenir des références (SKU) par type de compte et emplacement, au lieu d’utiliser ResourceGroupName et le nom du compte.</span><span class="sxs-lookup"><span data-stu-id="168bd-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="168bd-231">Az.Compute (précédemment AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="168bd-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="168bd-232">`IdentityIds` sont supprimés de la propriété `Identity` dans les objets `PSVirtualMachine` et `PSVirtualMachineScaleSet`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="168bd-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="168bd-233">Le type de la propriété `InstanceView` de l’objet `PSVirtualMachineScaleSetVM` passe de `VirtualMachineInstanceView` à `VirtualMachineScaleSetVMInstanceView`.</span><span class="sxs-lookup"><span data-stu-id="168bd-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="168bd-234">Les propriétés `AutoOSUpgradePolicy` et `AutomaticOSUpgrade` sont supprimées de la propriété `UpgradePolicy`.</span><span class="sxs-lookup"><span data-stu-id="168bd-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="168bd-235">Le type de la propriété `Sku` de l’objet `PSSnapshotUpdate` passe de `DiskSku` à `SnapshotSku`.</span><span class="sxs-lookup"><span data-stu-id="168bd-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="168bd-236">`VmScaleSetVMParameterSet` est supprimé de la cmdlet `Add-AzVMDataDisk`. Vous ne pouvez plus ajouter un disque de données individuellement à une machine virtuelle ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="168bd-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="168bd-237">Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="168bd-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="168bd-238">Le paramètre `GatewayName` est devenu obligatoire dans la cmdlet `New-AzDataFactoryEncryptValue`.</span><span class="sxs-lookup"><span data-stu-id="168bd-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="168bd-239">Suppression de la cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="168bd-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="168bd-240">Paramètre `LinkedServiceName` supprimé de la cmdlet `Get-AzDataFactoryV2ActivityRun`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="168bd-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="168bd-241">Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="168bd-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="168bd-242">Suppression des cmdlets déconseillées : `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, et `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="168bd-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="168bd-243">Az.DataLakeStore (précédemment AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="168bd-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="168bd-244">Dans les cmdlets suivantes, le paramètre `Encoding` est passé du type `FileSystemCmdletProviderEncoding` à `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="168bd-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="168bd-245">Cette modification supprime les valeurs de codage `String` et `Oem`.</span><span class="sxs-lookup"><span data-stu-id="168bd-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="168bd-246">Toutes les autres valeurs de codage préalables demeurent identiques.</span><span class="sxs-lookup"><span data-stu-id="168bd-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="168bd-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="168bd-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="168bd-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="168bd-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="168bd-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="168bd-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="168bd-250">Suppression de l’alias de propriété `Tags` déconseillé dans les cmdlets `New-AzDataLakeStoreAccount` et `Set-AzDataLakeStoreAccount`.</span><span class="sxs-lookup"><span data-stu-id="168bd-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="168bd-251">Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="168bd-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="168bd-252">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="168bd-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="168bd-253">Suppression des propriétés déconseillées `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` et `FirewallAllowAzureIps` de l’objet `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="168bd-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="168bd-254">Aucun script utilisant l’élément `PSDatalakeStoreAccount` renvoyé par `Get-AzDataLakeStoreAccount` ne doit référencer ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="168bd-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="168bd-255">Az.KeyVault (précédemment AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="168bd-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="168bd-256">La propriété `PurgeDisabled` a été supprimée des objets `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` et `PSKeyVaultSecretAttributes`. Les scripts ne doivent plus faire référence à la propriété ```PurgeDisabled``` pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="168bd-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="168bd-257">Az.Media (précédemment AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="168bd-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="168bd-258">Suppression de l’alias de propriété `Tags` déconseillé de la cmdlet `New-AzMediaService`. Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="168bd-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="168bd-259">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="168bd-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="168bd-260">Az.Monitor (précédemment AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="168bd-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="168bd-261">Suppression des paramètres `Categories` et `Timegrains` avec des noms pluriels en faveur des noms de paramètre au singulier dans la cmdlet `Set-AzDiagnosticSetting`. Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="168bd-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="168bd-262">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="168bd-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="168bd-263">Az.Network (précédemment AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="168bd-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="168bd-264">Suppression du paramètre déconseillé `ResourceId` de la cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="168bd-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="168bd-265">Suppression de la propriété déconseillée `EnableVmProtection` de l’objet `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="168bd-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="168bd-266">Suppression de la cmdlet déconseillée `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="168bd-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="168bd-267">Les scripts ne doivent plus décider des traitements sur la base des valeurs de ces champs.</span><span class="sxs-lookup"><span data-stu-id="168bd-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="168bd-268">Az.OperationalInsights (précédemment AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="168bd-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="168bd-269">Le jeu de paramètres par défaut pour `Get-AzOperationalInsightsDataSource` est supprimé, et `ByWorkspaceNameByKind` est devenu le jeu de paramètres par défaut</span><span class="sxs-lookup"><span data-stu-id="168bd-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="168bd-270">Tout script qui répertorie des sources de données utilisant</span><span class="sxs-lookup"><span data-stu-id="168bd-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="168bd-271">Doit être modifié selon un type spécifique</span><span class="sxs-lookup"><span data-stu-id="168bd-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="168bd-272">Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="168bd-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="168bd-273">Suppression du paramètre `Encryption` dans la cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="168bd-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="168bd-274">Le paramètre `TargetStorageAccountName` est maintenant obligatoire pour les restaurations de disque managé dans la cmdlet `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="168bd-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="168bd-275">Suppression des paramètres `StorageAccountName` et `StorageAccountResourceGroupName` dans la cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="168bd-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="168bd-276">Suppression du paramètre `Name` dans la cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="168bd-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="168bd-277">Az.Resources (précédemment AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="168bd-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="168bd-278">Suppression du paramètre `Sku` dans la cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="168bd-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="168bd-279">Suppression du paramètre `Password` dans les cmdlets `New-AzADServicePrincipal` et `New-AzADSpCredential`. Les mots de passe sont automatiquement générés. Tout script qui a fourni le mot de passe :</span><span class="sxs-lookup"><span data-stu-id="168bd-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="168bd-280">Doit être changé de façon à récupérer le mot de passe à partir de la sortie :</span><span class="sxs-lookup"><span data-stu-id="168bd-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="168bd-281">Az.ServiceFabric (précédemment AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="168bd-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="168bd-282">Les types de retour de cmdlet suivants ont été modifiés :</span><span class="sxs-lookup"><span data-stu-id="168bd-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="168bd-283">La propriété `ServiceTypeHealthPolicies` de type `ApplicationHealthPolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="168bd-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="168bd-284">La propriété `ApplicationHealthPolicies` de type `ClusterUpgradeDeltaHealthPolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="168bd-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="168bd-285">La propriété `OverrideUserUpgradePolicy` de type `ClusterUpgradePolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="168bd-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="168bd-286">Ces modifications influent sur les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="168bd-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="168bd-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="168bd-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="168bd-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="168bd-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="168bd-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="168bd-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="168bd-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="168bd-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="168bd-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="168bd-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="168bd-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="168bd-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="168bd-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="168bd-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="168bd-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="168bd-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="168bd-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="168bd-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="168bd-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="168bd-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="168bd-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="168bd-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="168bd-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="168bd-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="168bd-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="168bd-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="168bd-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="168bd-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="168bd-301">Az.Sql (précédemment AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="168bd-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="168bd-302">Suppression des paramètres `State` et `ResourceId` dans la cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="168bd-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="168bd-303">Suppression des cmdlets déconseillées : `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="168bd-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="168bd-304">Suppression du paramètre déconseillé `Current` de la cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="168bd-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="168bd-305">Suppression du paramètre déconseillé `DatabaseName` de la cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="168bd-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="168bd-306">Suppression du paramètre déconseillé `PrivilegedLogin` de la cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="168bd-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="168bd-307">Az.Storage (précédemment Azure.Storage et AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="168bd-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="168bd-308">Pour prendre en charge la création d’un contexte de stockage Oauth avec uniquement le nom du compte de stockage, le jeu de paramètres par défaut a été remplacé par `OAuthParameterSet`.</span><span class="sxs-lookup"><span data-stu-id="168bd-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="168bd-309">Exemple : `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="168bd-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="168bd-310">Le paramètre `Location` est devenu obligatoire dans la cmdlet `Get-AzStorageUsage`.</span><span class="sxs-lookup"><span data-stu-id="168bd-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="168bd-311">Les méthodes d’API de stockage utilisent maintenant le modèle asynchrone basé sur des tâches (TAP), au lieu d’appels d’API synchrones.</span><span class="sxs-lookup"><span data-stu-id="168bd-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="168bd-312">Les exemples suivants montrent les nouvelles commandes asynchrones :</span><span class="sxs-lookup"><span data-stu-id="168bd-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="168bd-313">Instantané d’objet blob</span><span class="sxs-lookup"><span data-stu-id="168bd-313">Blob Snapshot</span></span>

<span data-ttu-id="168bd-314">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="168bd-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="168bd-315">Az :</span><span class="sxs-lookup"><span data-stu-id="168bd-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="168bd-316">Partager l’instantané</span><span class="sxs-lookup"><span data-stu-id="168bd-316">Share Snapshot</span></span>

<span data-ttu-id="168bd-317">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="168bd-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="168bd-318">Az :</span><span class="sxs-lookup"><span data-stu-id="168bd-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="168bd-319">Annuler la suppression d’un objet blob supprimé de manière réversible</span><span class="sxs-lookup"><span data-stu-id="168bd-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="168bd-320">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="168bd-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="168bd-321">Az :</span><span class="sxs-lookup"><span data-stu-id="168bd-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="168bd-322">Définir un niveau d’objet blob</span><span class="sxs-lookup"><span data-stu-id="168bd-322">Set Blob Tier</span></span>

<span data-ttu-id="168bd-323">AzureRM :</span><span class="sxs-lookup"><span data-stu-id="168bd-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="168bd-324">Az :</span><span class="sxs-lookup"><span data-stu-id="168bd-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="168bd-325">Az.Websites (précédemment AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="168bd-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="168bd-326">Suppression des propriétés déconseillées des objets `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` et `PSSite`.</span><span class="sxs-lookup"><span data-stu-id="168bd-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
