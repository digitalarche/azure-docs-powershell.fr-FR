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
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="f6ea2-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="f6ea2-103">Release notes</span></span>
<a id="release-notes" class="xliff"></a>

<span data-ttu-id="f6ea2-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <span data-ttu-id="f6ea2-105">Version 3.8.0</span><span class="sxs-lookup"><span data-stu-id="f6ea2-105">Version 3.8.0</span></span>
<a id="version-380" class="xliff"></a>
* <span data-ttu-id="f6ea2-106">Calcul</span><span class="sxs-lookup"><span data-stu-id="f6ea2-106">Compute</span></span>
  - <span data-ttu-id="f6ea2-107">Correction d’un bogue dans les applets de commande Get-* pour permettre la récupération de plusieurs pages de données (plus de 120 éléments)</span><span class="sxs-lookup"><span data-stu-id="f6ea2-107">Fix bug in Get-* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="f6ea2-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f6ea2-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="f6ea2-109">Correction de l’aide de certaines commandes pour en améliorer la rédaction et les exemples.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="f6ea2-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f6ea2-110">DataLakeStore</span></span>
  - <span data-ttu-id="f6ea2-111">Ajout de la prise en charge du début et de la fin de l’applet de commande `Get-AzureRMDataLakeStoreItemContent`.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="f6ea2-112">Cela permet de retourner les N premières ou les N dernières nouvelles lignes à afficher.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="f6ea2-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f6ea2-113">HDInsight</span></span>
  - <span data-ttu-id="f6ea2-114">Ajout de la prise en charge du type de cluster RServer</span><span class="sxs-lookup"><span data-stu-id="f6ea2-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="f6ea2-115">La taille de machine virtuelle Edgenode peut être spécifiée pour le cluster RServer dans New-AzureRmHDInsightCluster ou New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f6ea2-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="f6ea2-116">RServer est désormais une option de configuration dans Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="f6ea2-117">Cela permet à l’indicateur RStudio d’indiquer que l’installation de R Studio doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="f6ea2-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="f6ea2-118">LogicApp</span></span>
  - <span data-ttu-id="f6ea2-119">Corrections des applets de commande Set-AzureRmIntegrationAccountSchema et Set-AzureRmIntegrationAccountMap pour le problème lié à contentlink (content et contentlink étaient tous deux définis, ce qui entraînait un échec de la mise à jour).</span><span class="sxs-lookup"><span data-stu-id="f6ea2-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="f6ea2-120">Réseau</span><span class="sxs-lookup"><span data-stu-id="f6ea2-120">Network</span></span>
  - <span data-ttu-id="f6ea2-121">Ajout de la prise en charge de nouvelles fonctionnalités de pare-feu d’applications web pour les passerelles d’application</span><span class="sxs-lookup"><span data-stu-id="f6ea2-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="f6ea2-122">Ajout de New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="f6ea2-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="f6ea2-123">Ajout de Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias : List-AzureRmApplicationGatewayAvailableWafRuleSets)</span><span class="sxs-lookup"><span data-stu-id="f6ea2-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="f6ea2-124">Mise à jour de New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration : ajout des paramètres -RuleSetType -RuleSetVersion et -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="f6ea2-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="f6ea2-125">Mise à jour de Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration : ajout des paramètres -RuleSetType -RuleSetVersion et -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="f6ea2-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="f6ea2-126">Ajout de la prise en charge des stratégies IPSec pour les connexions de passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="f6ea2-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="f6ea2-127">Ajout de New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f6ea2-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="f6ea2-128">Mise à jour de New-AzureRmVirtualNetworkGatewayConnection : ajout des paramètres -IpsecPolicies et -UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f6ea2-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="f6ea2-129">Profil</span><span class="sxs-lookup"><span data-stu-id="f6ea2-129">Profile</span></span>
  - <span data-ttu-id="f6ea2-130">*Obsolète* : Save-AzureRmProfile est renommé Save-AzureRmContext. Il existe un alias pour l’ancien nom de l’applet de commande, il sera supprimé dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="f6ea2-131">*Obsolète* : Select-AzureRmProfile est renommé Import-AzureRmContext. Il existe un alias pour l’ancien nom de l’applet de commande, il sera supprimé dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="f6ea2-132">Les types de sortie PSAzureContext et PSAzureProfile des applets de commande de profil seront changés dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="f6ea2-133">L’applet de commande Save-AzureRmContext n’aura aucun OutputType dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="f6ea2-134">Correction d’un bogue dans le code commun d’applet de commande permettant d’utiliser un algorithme FIPS pour les hachages de données : https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="f6ea2-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="f6ea2-135">SQL</span><span class="sxs-lookup"><span data-stu-id="f6ea2-135">Sql</span></span>
  - <span data-ttu-id="f6ea2-136">Résolution des bogues sur les applets de commande de groupe de basculement Azure</span><span class="sxs-lookup"><span data-stu-id="f6ea2-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="f6ea2-137">Correction de l’interrogation d’opération</span><span class="sxs-lookup"><span data-stu-id="f6ea2-137">Fix for operation polling</span></span>
  - <span data-ttu-id="f6ea2-138">Correction de la valeur GracePeriodWithDataLossHour pendant la définition de FailoverPolicy sur Manuel</span><span class="sxs-lookup"><span data-stu-id="f6ea2-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="f6ea2-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f6ea2-139">TrafficManager</span></span>
  - <span data-ttu-id="f6ea2-140">Prise en charge de la méthode de routage du trafic Géographique</span><span class="sxs-lookup"><span data-stu-id="f6ea2-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="f6ea2-141">Nouvelle valeur « Géographique » pour le paramètre TrafficRoutingMethod de New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6ea2-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="f6ea2-142">Nouveau paramètre « GeoMapping » pour New-AzureRmTrafficManagerEndpoint et Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f6ea2-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="f6ea2-143">Correction du piping pour l’applet de commande Get-AzureRmTrafficManagerProfile quand elle retourne une collection de profils</span><span class="sxs-lookup"><span data-stu-id="f6ea2-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="f6ea2-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="f6ea2-144">ServiceManagement</span></span>
  - <span data-ttu-id="f6ea2-145">Restart-AzureVM : Ajout du paramètre InitiateMaintenance pour effectuer la maintenance pendant le redémarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="f6ea2-146">Get-AzureVM : Ajout du champ d’état de la maintenance.</span><span class="sxs-lookup"><span data-stu-id="f6ea2-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="f6ea2-147">Ajout de nouvelles applets de commande pour prendre en charge la mise à niveau du coffre Recovery Services</span><span class="sxs-lookup"><span data-stu-id="f6ea2-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="f6ea2-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="f6ea2-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="f6ea2-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="f6ea2-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
