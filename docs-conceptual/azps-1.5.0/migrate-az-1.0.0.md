---
title: Dernières modifications de Microsoft Azure PowerShell Az 1.0.0
description: Ce guide de migration contient une liste des dernières modifications apportées à Azure PowerShell dans la version Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882310"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="a0872-103">Guide de migration pour Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="a0872-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="a0872-104">Ce document décrit les modifications apportées entre les versions 6.x d’AzureRM et la version Az 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="a0872-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="a0872-105">Sommaire</span><span class="sxs-lookup"><span data-stu-id="a0872-105">Table of Contents</span></span>
- [<span data-ttu-id="a0872-106">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="a0872-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="a0872-107">Modifications de préfixe de nom de cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0872-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="a0872-108">Modifications de nom de module</span><span class="sxs-lookup"><span data-stu-id="a0872-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="a0872-109">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="a0872-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="a0872-110">Windows PowerShell 5.1 et .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="a0872-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="a0872-111">Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential</span><span class="sxs-lookup"><span data-stu-id="a0872-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="a0872-112">Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web</span><span class="sxs-lookup"><span data-stu-id="a0872-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="a0872-113">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="a0872-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="a0872-114">Az.ApiManagement (précédemment AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="a0872-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="a0872-115">Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="a0872-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="a0872-116">Az.CognitiveServices (précédemment AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="a0872-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="a0872-117">Az.Compute (précédemment AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="a0872-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="a0872-118">Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="a0872-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="a0872-119">Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="a0872-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="a0872-120">Az.DataLakeStore (précédemment AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="a0872-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="a0872-121">Az.KeyVault (précédemment AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="a0872-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="a0872-122">Az.Media (précédemment AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="a0872-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="a0872-123">Az.Monitor (précédemment AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="a0872-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="a0872-124">Az.Network (précédemment AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="a0872-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="a0872-125">Az.OperationalInsights (précédemment AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="a0872-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="a0872-126">Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="a0872-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="a0872-127">Az.Resources (précédemment AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="a0872-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="a0872-128">Az.ServiceFabric (précédemment AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="a0872-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="a0872-129">Az.Sql (précédemment AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="a0872-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="a0872-130">Az.Storage (précédemment Azure.Storage et AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="a0872-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="a0872-131">Az.Websites (précédemment AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="a0872-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="a0872-132">Dernières modifications générales</span><span class="sxs-lookup"><span data-stu-id="a0872-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="a0872-133">Modifications de préfixe de nom de cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0872-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="a0872-134">Dans AzureRM, les cmdlets utilisaient « AzureRM » ou « Azure » comme préfixe de nom.</span><span class="sxs-lookup"><span data-stu-id="a0872-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="a0872-135">Az simplifie et normalise les noms de cmdlet, afin qu’elles utilisent toutes « Az » comme nom de préfixe de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0872-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="a0872-136">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="a0872-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="a0872-137">est devenu</span><span class="sxs-lookup"><span data-stu-id="a0872-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="a0872-138">Pour simplifier la transition vers ces nouveaux noms de cmdlet, Az introduit deux nouvelles cmdlets : ```Enable-AzureRmAlias``` et ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="a0872-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="a0872-139">```Enable-AzureRmAlias``` crée des alias pour les noms de cmdlet Az récents à partir des anciens noms de cmdlet dans AzureRM.</span><span class="sxs-lookup"><span data-stu-id="a0872-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="a0872-140">La cmdlet permet de créer des alias dans la session active, ou dans toutes les sessions en modifiant le profil de l’ordinateur ou de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0872-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="a0872-141">Par exemple, le script suivant dans AzureRM :</span><span class="sxs-lookup"><span data-stu-id="a0872-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="a0872-142">Peut être exécuté avec des modifications minimes à l’aide de ```Enable-AzureRmAlias``` :</span><span class="sxs-lookup"><span data-stu-id="a0872-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="a0872-143">L’exécution de ```Enable-AzureRmAlias -Scope CurrentUser``` activera les alias pour toutes les sessions PowerShell que vous ouvrez. Ainsi, après l’exécution de cette cmdlet, il serait inutile de modifier un tel script :</span><span class="sxs-lookup"><span data-stu-id="a0872-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="a0872-144">Pour plus d’informations sur l’utilisation des cmdlets d’alias, exécutez ```Get-Help -Online Enable-AzureRmAlias``` à partir de l’invite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a0872-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="a0872-145">```Disable-AzureRmAlias``` supprime les alias de cmdlet AzureRM créés par ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="a0872-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="a0872-146">Pour plus d’informations, exécutez ```Get-Help -Online Disable-AzureRmAlias``` à partir de l’invite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a0872-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="a0872-147">Modifications de nom de module</span><span class="sxs-lookup"><span data-stu-id="a0872-147">Module Name Changes</span></span>
- <span data-ttu-id="a0872-148">Les noms de module ont été modifiés de `AzureRM.*` vers `Az.*`, sauf pour les modules suivants :</span><span class="sxs-lookup"><span data-stu-id="a0872-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="a0872-149">Les modifications dans les noms de module signifient que n’importe quel script qui utilise ```#Requires``` ou ```Import-Module``` pour charger des modules spécifiques devra être modifié pour utiliser le nouveau module à la place.</span><span class="sxs-lookup"><span data-stu-id="a0872-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="a0872-150">Migration des instructions #Requires</span><span class="sxs-lookup"><span data-stu-id="a0872-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="a0872-151">Les scripts qui utilisent #Requires pour déclarer une dépendance sur les modules AzureRM doiventt être mis à jour pour utiliser les nouveaux noms de module.</span><span class="sxs-lookup"><span data-stu-id="a0872-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="a0872-152">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="a0872-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="a0872-153">Migration des instructions Import-Module</span><span class="sxs-lookup"><span data-stu-id="a0872-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="a0872-154">Les scripts qui utilisent ```Import-Module``` pour charger les modules AzureRM devront être mis à jour pour refléter les nouveaux noms de module.</span><span class="sxs-lookup"><span data-stu-id="a0872-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="a0872-155">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="a0872-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="a0872-156">Migration des appels de cmdlet complets</span><span class="sxs-lookup"><span data-stu-id="a0872-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="a0872-157">Les scripts qui utilisent des appels de cmdlet complets par un module, comme</span><span class="sxs-lookup"><span data-stu-id="a0872-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="a0872-158">doivent être modifiés pour utiliser les nouveaux noms de module et de cmdlet</span><span class="sxs-lookup"><span data-stu-id="a0872-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="a0872-159">Migration des dépendances de manifeste de module</span><span class="sxs-lookup"><span data-stu-id="a0872-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="a0872-160">Les modules qui expriment les dépendances sur les modules AzureRM via un manifeste de module (.psd1) doivent mettre à jour les noms de module dans la section « RequiredModules ».</span><span class="sxs-lookup"><span data-stu-id="a0872-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="a0872-161">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="a0872-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="a0872-162">Modules supprimés</span><span class="sxs-lookup"><span data-stu-id="a0872-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="a0872-163">Les outils destinés à ces services ne sont plus activement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a0872-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="a0872-164">Les clients sont encouragés à choisir d’autres services dès que possible.</span><span class="sxs-lookup"><span data-stu-id="a0872-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="a0872-165">Windows PowerShell 5.1 et .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="a0872-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="a0872-166">L’utilisation d’Az avec Windows PowerShell 5.1 nécessite l’installation de .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="a0872-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="a0872-167">Toutefois, l’utilisation d’Az avec PowerShell Core ne nécessite pas .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="a0872-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="a0872-168">Suppression temporaire de la connexion de l’utilisateur à l’aide de PSCredential</span><span class="sxs-lookup"><span data-stu-id="a0872-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="a0872-169">En raison de modifications dans le flux d’authentification pour .NET Standard, nous supprimons temporairement la connexion utilisateur via PSCredential.</span><span class="sxs-lookup"><span data-stu-id="a0872-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="a0872-170">Cette fonctionnalité sera réintroduite dans la version du 15/1/2019 pour Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="a0872-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="a0872-171">Les détails sont abordés dans [ce problème.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="a0872-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="a0872-172">Connexion via le code d’appareil par défaut au lieu de l’invite du navigateur web</span><span class="sxs-lookup"><span data-stu-id="a0872-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="a0872-173">En raison de modifications dans le flux d’authentification pour .NET Standard, nous utilisons la connexion à l’appareil en tant que flux de connexion par défaut lors de la connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="a0872-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="a0872-174">La connexion basée sur un navigateur Web sera réintroduite pour Windows PowerShell 5.1 en tant que mode par défaut dans la version 15/1/2019.</span><span class="sxs-lookup"><span data-stu-id="a0872-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="a0872-175">À ce moment, les utilisateurs seront en mesure de se connecter à l’appareil à l’aide d’un paramètre de commutateur.</span><span class="sxs-lookup"><span data-stu-id="a0872-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="a0872-176">Changements cassants de module</span><span class="sxs-lookup"><span data-stu-id="a0872-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="a0872-177">Az.ApiManagement (précédemment AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="a0872-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="a0872-178">Suppression des cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0872-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="a0872-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0872-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="a0872-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a0872-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="a0872-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a0872-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="a0872-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a0872-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="a0872-183">Utilisez la cmdlet **Set-AzApiManagement** pour définir ces propriétés à la place.</span><span class="sxs-lookup"><span data-stu-id="a0872-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="a0872-184">Les propriétés suivantes ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="a0872-184">Following properties were removed</span></span>
  - <span data-ttu-id="a0872-185">Suppression des propriétés `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` et `ScmHostnameConfiguration` de type `PsApiManagementHostnameConfiguration` dans `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="a0872-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="a0872-186">À la place, utilisez `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` et `ScmCustomHostnameConfiguration` de type `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="a0872-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="a0872-187">Suppression de la propriété `StaticIPs` dans PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a0872-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="a0872-188">La propriété a été divisée en `PublicIPAddresses` et `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="a0872-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="a0872-189">Suppression de la propriété obligatoire `Location` dans la cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="a0872-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="a0872-190">Az.Billing (précédemment AzureRM.Billing, AzureRM.Consumption et AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="a0872-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="a0872-191">Le paramètre `InvoiceName` a été supprimé de la cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="a0872-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="a0872-192">Les scripts doivent utiliser d’autres paramètres d’identité pour la facture.</span><span class="sxs-lookup"><span data-stu-id="a0872-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="a0872-193">Az.CognitiveServices (précédemment AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="a0872-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="a0872-194">Suppression du jeu de paramètres `GetSkusWithAccountParamSetName` dans la cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="a0872-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="a0872-195">Vous devez obtenir des références (SKU) par type de compte et emplacement, au lieu d’utiliser ResourceGroupName et le nom du compte.</span><span class="sxs-lookup"><span data-stu-id="a0872-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="a0872-196">Az.Compute (précédemment AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="a0872-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="a0872-197">`IdentityIds` sont supprimés de la propriété `Identity` dans les objets `PSVirtualMachine` et `PSVirtualMachineScaleSet`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="a0872-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="a0872-198">Le type de la propriété `InstanceView` de l’objet `PSVirtualMachineScaleSetVM` passe de `VirtualMachineInstanceView` à `VirtualMachineScaleSetVMInstanceView`.</span><span class="sxs-lookup"><span data-stu-id="a0872-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="a0872-199">Les propriétés `AutoOSUpgradePolicy` et `AutomaticOSUpgrade` sont supprimées de la propriété `UpgradePolicy`.</span><span class="sxs-lookup"><span data-stu-id="a0872-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="a0872-200">Le type de la propriété `Sku` de l’objet `PSSnapshotUpdate` passe de `DiskSku` à `SnapshotSku`.</span><span class="sxs-lookup"><span data-stu-id="a0872-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="a0872-201">`VmScaleSetVMParameterSet` est supprimé de la cmdlet `Add-AzVMDataDisk`. Vous ne pouvez plus ajouter un disque de données individuellement à une machine virtuelle ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="a0872-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="a0872-202">Az.DataFactory (précédemment AzureRM.DataFactories et AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="a0872-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="a0872-203">Le paramètre `GatewayName` est devenu obligatoire dans la cmdlet `New-AzDataFactoryEncryptValue`.</span><span class="sxs-lookup"><span data-stu-id="a0872-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="a0872-204">Suppression de la cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="a0872-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="a0872-205">Paramètre `LinkedServiceName` supprimé de la cmdlet `Get-AzDataFactoryV2ActivityRun`. Les scripts ne doivent plus utiliser la valeur de ce champ pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="a0872-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="a0872-206">Az.DataLakeAnalytics (précédemment AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="a0872-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="a0872-207">Suppression des cmdlets déconseillées : `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, et `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="a0872-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="a0872-208">Az.DataLakeStore (précédemment AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="a0872-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="a0872-209">Dans les cmdlets suivantes, le paramètre `Encoding` est passé du type `FileSystemCmdletProviderEncoding` à `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="a0872-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="a0872-210">Cette modification supprime les valeurs de codage `String` et `Oem`.</span><span class="sxs-lookup"><span data-stu-id="a0872-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="a0872-211">Toutes les autres valeurs de codage préalables demeurent identiques.</span><span class="sxs-lookup"><span data-stu-id="a0872-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="a0872-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a0872-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="a0872-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a0872-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="a0872-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a0872-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="a0872-215">Suppression de l’alias de propriété `Tags` déconseillé dans les cmdlets `New-AzDataLakeStoreAccount` et `Set-AzDataLakeStoreAccount`.</span><span class="sxs-lookup"><span data-stu-id="a0872-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="a0872-216">Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="a0872-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="a0872-217">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="a0872-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="a0872-218">Suppression des propriétés déconseillées ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` et ```FirewallAllowAzureIps``` de l’objet ```PSDataLakeStoreAccountBasic```.</span><span class="sxs-lookup"><span data-stu-id="a0872-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="a0872-219">Aucun script utilisant l’élément ```PSDatalakeStoreAccount``` renvoyé par ```Get-AzDataLakeStoreAccount``` ne doit référencer ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a0872-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="a0872-220">Az.KeyVault (précédemment AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="a0872-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="a0872-221">La propriété `PurgeDisabled` a été supprimée des objets `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` et `PSKeyVaultSecretAttributes`. Les scripts ne doivent plus faire référence à la propriété ```PurgeDisabled``` pour prendre des décisions de traitement.</span><span class="sxs-lookup"><span data-stu-id="a0872-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="a0872-222">Az.Media (précédemment AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="a0872-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="a0872-223">Suppression de l’alias de propriété `Tags` déconseillé de la cmdlet `New-AzMediaService`. Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="a0872-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="a0872-224">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="a0872-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="a0872-225">Az.Monitor (précédemment AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="a0872-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="a0872-226">Suppression des paramètres `Categories` et `Timegrains` avec des noms pluriels en faveur des noms de paramètre au singulier dans la cmdlet `Set-AzDiagnosticSetting`. Tout script utilisant</span><span class="sxs-lookup"><span data-stu-id="a0872-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="a0872-227">Doit être remplacé par</span><span class="sxs-lookup"><span data-stu-id="a0872-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="a0872-228">Az.Network (précédemment AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="a0872-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="a0872-229">Suppression du paramètre déconseillé `ResourceId` de la cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="a0872-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="a0872-230">Suppression de la propriété déconseillée `EnableVmProtection` de l’objet `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="a0872-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="a0872-231">Suppression de la cmdlet déconseillée `Set-AzVirtualNetworkGatewayVpnClientConfig`</span><span class="sxs-lookup"><span data-stu-id="a0872-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="a0872-232">Les scripts ne doivent plus prendre de décisions de traitement reposant sur les valeurs de ces champs.</span><span class="sxs-lookup"><span data-stu-id="a0872-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="a0872-233">Az.OperationalInsights (précédemment AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="a0872-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="a0872-234">Le jeu de paramètres par défaut pour `Get-AzOperationalInsightsDataSource` est supprimé, et `ByWorkspaceNameByKind` est devenu le jeu de paramètres par défaut</span><span class="sxs-lookup"><span data-stu-id="a0872-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="a0872-235">Tout script qui répertorie des sources de données utilisant</span><span class="sxs-lookup"><span data-stu-id="a0872-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="a0872-236">Doit être modifié selon un type spécifique</span><span class="sxs-lookup"><span data-stu-id="a0872-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="a0872-237">Az.RecoveryServices (précédemment AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup et AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="a0872-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="a0872-238">Suppression du paramètre `Encryption` dans la cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="a0872-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="a0872-239">Le paramètre `TargetStorageAccountName` est maintenant obligatoire pour les restaurations de disque managé dans la cmdlet `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="a0872-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="a0872-240">Suppression des paramètres `StorageAccountName` et `StorageAccountResourceGroupName` dans la cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="a0872-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="a0872-241">Suppression du paramètre `Name` dans la cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="a0872-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="a0872-242">Az.Resources (précédemment AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="a0872-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="a0872-243">Suppression du paramètre `Sku` dans la cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a0872-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="a0872-244">Suppression du paramètre `Password` dans les cmdlets `New-AzADServicePrincipal` et `New-AzADSpCredential`. Les mots de passe sont automatiquement générés. Tout script qui a fourni le mot de passe :</span><span class="sxs-lookup"><span data-stu-id="a0872-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="a0872-245">Doit être modifié par récupérer le mot de passe à partir de la sortie :</span><span class="sxs-lookup"><span data-stu-id="a0872-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="a0872-246">Az.ServiceFabric (précédemment AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="a0872-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="a0872-247">Les types de retour de cmdlet suivants ont été modifiés :</span><span class="sxs-lookup"><span data-stu-id="a0872-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="a0872-248">La propriété `SerivceTypeHealthPolicies` de type `ApplicationHealthPolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="a0872-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="a0872-249">La propriété `ApplicationHealthPolicies` de type `ClusterUpgradeDeltaHealthPolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="a0872-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="a0872-250">La propriété `OverrideUserUpgradePolicy` de type `ClusterUpgradePolicy` a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="a0872-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="a0872-251">Ces modifications influent sur les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0872-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="a0872-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a0872-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="a0872-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a0872-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="a0872-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a0872-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="a0872-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a0872-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="a0872-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="a0872-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="a0872-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a0872-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="a0872-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="a0872-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="a0872-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a0872-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="a0872-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a0872-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="a0872-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a0872-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="a0872-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a0872-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="a0872-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a0872-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="a0872-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a0872-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="a0872-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="a0872-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="a0872-266">Az.Sql (précédemment AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="a0872-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="a0872-267">Suppression des paramètres `State` et `ResourceId` dans la cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="a0872-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="a0872-268">Suppression des cmdlets déconseillées : `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="a0872-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="a0872-269">Suppression du paramètre déconseillé `Current` de la cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="a0872-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="a0872-270">Suppression du paramètre déconseillé `DatabaseName` de la cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="a0872-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="a0872-271">Suppression du paramètre déconseillé `PrivilegedLogin` de la cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="a0872-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="a0872-272">Az.Storage (précédemment Azure.Storage et AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="a0872-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="a0872-273">Pour prendre en charge la création d’un contexte de stockage Oauth avec uniquement le nom du compte de stockage, le jeu de paramètres par défaut a été remplacé par `OAuthParameterSet`.</span><span class="sxs-lookup"><span data-stu-id="a0872-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="a0872-274">Exemple : `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="a0872-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="a0872-275">Le paramètre `Location` est devenu obligatoire dans la cmdlet `Get-AzStorageUsage`.</span><span class="sxs-lookup"><span data-stu-id="a0872-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="a0872-276">Les méthodes d’API de stockage utilisent maintenant le modèle asynchrone basé sur des tâches (TAP), au lieu d’appels d’API synchrones.</span><span class="sxs-lookup"><span data-stu-id="a0872-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="a0872-277">1. Instantané d’objet blob</span><span class="sxs-lookup"><span data-stu-id="a0872-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="a0872-278">Avant :</span><span class="sxs-lookup"><span data-stu-id="a0872-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="a0872-279">Après :</span><span class="sxs-lookup"><span data-stu-id="a0872-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="a0872-280">2. Partager l’instantané</span><span class="sxs-lookup"><span data-stu-id="a0872-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="a0872-281">Avant :</span><span class="sxs-lookup"><span data-stu-id="a0872-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="a0872-282">Après :</span><span class="sxs-lookup"><span data-stu-id="a0872-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="a0872-283">3. Restaurer un objet blob après une suppression réversible</span><span class="sxs-lookup"><span data-stu-id="a0872-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="a0872-284">Avant :</span><span class="sxs-lookup"><span data-stu-id="a0872-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="a0872-285">Après :</span><span class="sxs-lookup"><span data-stu-id="a0872-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="a0872-286">4. Définir un niveau d’objet blob</span><span class="sxs-lookup"><span data-stu-id="a0872-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="a0872-287">Avant :</span><span class="sxs-lookup"><span data-stu-id="a0872-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="a0872-288">Après :</span><span class="sxs-lookup"><span data-stu-id="a0872-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="a0872-289">Az.Websites (précédemment AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="a0872-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="a0872-290">Suppression des propriétés déconseillées des objets `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` et `PSSite`.</span><span class="sxs-lookup"><span data-stu-id="a0872-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>