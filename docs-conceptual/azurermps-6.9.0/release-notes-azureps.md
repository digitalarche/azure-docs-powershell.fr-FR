---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 3cb71087a61a0fcd06c014394e8f9e5654d4c1a8
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47179001"
---
# <a name="release-notes"></a><span data-ttu-id="ad573-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="ad573-103">Release notes</span></span>

<span data-ttu-id="ad573-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad573-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="690---september-2018"></a><span data-ttu-id="ad573-105">6.9.0 - septembre 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-105">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad573-106">Généralités</span><span class="sxs-lookup"><span data-stu-id="ad573-106">General</span></span>
* <span data-ttu-id="ad573-107">AzureRM.SignalR a été ajouté au module Rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="ad573-107">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ad573-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-108">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-109">Modifications mineures du code commun de stockage</span><span class="sxs-lookup"><span data-stu-id="ad573-109">Minor changes to the storage common code</span></span>
* <span data-ttu-id="ad573-110">Mise à jour des fichiers d’aide pour inclure des types de paramètre complet.</span><span class="sxs-lookup"><span data-stu-id="ad573-110">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="ad573-111">Modification de -ServicePrincipal en non obligatoire dans l’ensemble de paramètres ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad573-111">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="ad573-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-112">Azure.Storage</span></span>
* <span data-ttu-id="ad573-113">Prise en charge du contexte de stockage avec OAuth.</span><span class="sxs-lookup"><span data-stu-id="ad573-113">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="ad573-114">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad573-114">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ad573-115">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad573-115">AzureRM.Cdn</span></span>
* <span data-ttu-id="ad573-116">Ajout de Standard_Microsoft dans la référence SKU de tarification d’un CDN.</span><span class="sxs-lookup"><span data-stu-id="ad573-116">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-117">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-117">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-118">Déplacement des dépendances du coffre de clés et du stockage vers les dépendances communes</span><span class="sxs-lookup"><span data-stu-id="ad573-118">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="ad573-119">Ajout de la prise en charge de plus de tailles de machine virtuelle aux cmdlets AEM</span><span class="sxs-lookup"><span data-stu-id="ad573-119">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="ad573-120">Ajout du paramètre PublicIPPrefix à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-120">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ad573-121">Ajout du paramètre ResourceId à la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ad573-121">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="ad573-122">Ajout de la cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ad573-122">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ad573-123">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ad573-123">AzureRM.Dns</span></span>
* <span data-ttu-id="ad573-124">Prise en charge de l’enregistrement d’alias pendant la création d’enregistrements DNS</span><span class="sxs-lookup"><span data-stu-id="ad573-124">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ad573-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ad573-125">AzureRM.Insights</span></span>
* <span data-ttu-id="ad573-126">Résolution des problèmes #6833 et #7102 (zone Paramètres de diagnostic)</span><span class="sxs-lookup"><span data-stu-id="ad573-126">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="ad573-127">Problèmes avec un nom par défaut, par exemple « service », lors de la création et l’obtention/le référencement des paramètres de diagnostic</span><span class="sxs-lookup"><span data-stu-id="ad573-127">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="ad573-128">Problèmes créant des paramètres de diagnostic avec des catégories</span><span class="sxs-lookup"><span data-stu-id="ad573-128">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="ad573-129">Ajout de message de désapprobation pour les paramètres de fragments de temps de métriques</span><span class="sxs-lookup"><span data-stu-id="ad573-129">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="ad573-130">Les paramètres Timegrains sont toujours acceptés (il s’agit d’une modification sans rupture,), mais ils sont ignorés dans le serveur principal dans la mesure où seul PT1M est valide</span><span class="sxs-lookup"><span data-stu-id="ad573-130">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-131">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-131">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-132">Modifications apportées aux cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad573-132">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="ad573-133">LoadBalancerInboundNatPoolConfig : ajout des paramètres IdleTimeoutInMinutes, EnableFloatingIp et EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ad573-133">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="ad573-134">LoadBalancerInboundNatRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ad573-134">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ad573-135">LoadBalancerRuleConfig : ajout du paramètre EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="ad573-135">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="ad573-136">LoadBalancerProbeConfig : ajout d’une prise en charge de la valeur « Https » pour le paramètre Protocole</span><span class="sxs-lookup"><span data-stu-id="ad573-136">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="ad573-137">Ajout de nouvelles commandes pour la sous-ressource OutboundRule du nouveau LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ad573-137">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="ad573-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-138">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ad573-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-139">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ad573-140">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-140">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ad573-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-141">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="ad573-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-142">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="ad573-143">Ajout d’une nouvelle propriété HostedWorkloads pour PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ad573-143">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="ad573-144">Ajouté de nouvelles cmdlets pour la fonctionnalité : Pare-feu Azure via ARM</span><span class="sxs-lookup"><span data-stu-id="ad573-144">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="ad573-145">Ajout de Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad573-145">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="ad573-146">Ajout de Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad573-146">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="ad573-147">Ajout de New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad573-147">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="ad573-148">Ajout de Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ad573-148">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="ad573-149">Ajout de New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad573-149">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="ad573-150">Ajout de New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ad573-150">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="ad573-151">Ajout de New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad573-151">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="ad573-152">Ajout de New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="ad573-152">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="ad573-153">Ajout de New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ad573-153">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="ad573-154">Ajout de New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ad573-154">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="ad573-155">Ajout de la prise en charge du certificat racine approuvé et de la configuration de mise à l’échelle automatique dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ad573-155">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="ad573-156">Nouvelles cmdlets ajoutées :</span><span class="sxs-lookup"><span data-stu-id="ad573-156">New Cmdlets added:</span></span>
      - <span data-ttu-id="ad573-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-157">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ad573-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-158">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ad573-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-159">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ad573-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-160">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ad573-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-161">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="ad573-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-162">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ad573-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-163">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ad573-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-164">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="ad573-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-165">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="ad573-166">Cmdlets mises à jour avec le paramètre facultatif -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-166">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="ad573-167">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad573-167">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ad573-168">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad573-168">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ad573-169">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ad573-169">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="ad573-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ad573-170">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="ad573-171">Cmdlets mises à jour avec le paramètre facultatif -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-171">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="ad573-172">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad573-172">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="ad573-173">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ad573-173">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="ad573-174">Ajout d’une cmdlet pour le point de terminaison d’interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad573-174">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="ad573-175">Ajout de la prise en charge de plusieurs préfixes d’adresse dans un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ad573-175">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="ad573-176">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="ad573-176">Updated cmdlets:</span></span>
  - <span data-ttu-id="ad573-177">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-177">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ad573-178">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-178">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ad573-179">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-179">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ad573-180">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-180">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="ad573-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-181">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="ad573-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-182">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ad573-183">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-183">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ad573-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-184">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="ad573-185">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-185">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ad573-186">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-186">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ad573-187">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-187">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="ad573-188">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-188">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ad573-189">New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-189">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="ad573-190">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-190">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ad573-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-191">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="ad573-192">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-192">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ad573-193">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-193">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ad573-194">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-194">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="ad573-195">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ad573-195">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="ad573-196">Ajout de cmdlets pour la délégation de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="ad573-196">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="ad573-197">New-AzureRmDelegation : crée une nouvelle délégation, celle-ci peut être ajoutée à un sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ad573-197">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="ad573-198">Remove-AzureRmDelegation : accepte un sous-réseau et supprime le nom de délégation fourni de ce sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ad573-198">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="ad573-199">Add-AzureRmDelegation : accepte un sous-réseau et ajoute le nom de service fourni en tant que délégation à ce sous-réseau</span><span class="sxs-lookup"><span data-stu-id="ad573-199">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="ad573-200">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ad573-200">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="ad573-201">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="ad573-201">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ad573-202">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad573-202">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ad573-203">Prise en charge de la gestion de disque managé</span><span class="sxs-lookup"><span data-stu-id="ad573-203">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ad573-204">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad573-204">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ad573-205">Mise à jour de la dépendance Insights.</span><span class="sxs-lookup"><span data-stu-id="ad573-205">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-206">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-206">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-207">Mise à jour de New-AzureRmResourceGroupDeployment avec le nouveau paramètre RollbackAction</span><span class="sxs-lookup"><span data-stu-id="ad573-207">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="ad573-208">Ajout de la prise en charge d’OnErrorDeployment avec le nouveau paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad573-208">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="ad573-209">Prise en charge des identités managées sur les affectations de stratégies.</span><span class="sxs-lookup"><span data-stu-id="ad573-209">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="ad573-210">Des paramètres avec des valeurs par défaut ne sont plus requis lors de l’affectation d’une stratégie avec « New-AzureRmPolicyAssignment »</span><span class="sxs-lookup"><span data-stu-id="ad573-210">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="ad573-211">Ajout de la nouvelle cmdlet Get-AzureRmPolicyAlias pour récupérer les alias de stratégie</span><span class="sxs-lookup"><span data-stu-id="ad573-211">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-212">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-212">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-213">Résolution du problème #7161</span><span class="sxs-lookup"><span data-stu-id="ad573-213">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="ad573-214">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="ad573-214">AzureRM.SignalR</span></span>
* <span data-ttu-id="ad573-215">Mise à jour des noms de référence SKU en Free_F1 et Standard_S1</span><span class="sxs-lookup"><span data-stu-id="ad573-215">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="ad573-216">Ajout d’un champ de version à l’objet PSSignalRResource et d’une chaîne de connexion à l’objet PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="ad573-216">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ad573-217">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-217">AzureRM.Storage</span></span>
* <span data-ttu-id="ad573-218">Prise en charge de la stratégie d’immuabilité dans AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-218">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="ad573-219">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ad573-219">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="ad573-220">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad573-220">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ad573-221">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad573-221">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ad573-222">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad573-222">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ad573-223">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ad573-223">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="ad573-224">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ad573-224">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ad573-225">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="ad573-225">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="ad573-226">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-226">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ad573-227">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-227">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ad573-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-228">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="ad573-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-229">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ad573-230">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ad573-230">AzureRM.Websites</span></span>
* <span data-ttu-id="ad573-231">Ajout de deux nouvelles cmdlets : Get-AzureRmDeletedWebApp et Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ad573-231">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="ad573-232">New-AzureRmAppServicePlan : le commutateur HyperV est ajouté pour créer un plan App Service avec conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="ad573-232">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="ad573-233">New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot : les nouveaux paramètres (la chaîne -ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) ajoutés pour créer et gérer l’application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="ad573-233">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="ad573-234">6.8.1 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-234">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad573-235">Généralités</span><span class="sxs-lookup"><span data-stu-id="ad573-235">General</span></span>
* <span data-ttu-id="ad573-236">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ad573-236">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ad573-237">Mise à jour des assemblys de runtime courants</span><span class="sxs-lookup"><span data-stu-id="ad573-237">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ad573-238">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad573-238">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ad573-239">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ad573-239">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ad573-240">Problème résolu https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="ad573-240">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="ad573-241">Les cmdlets Import-AzureRmApiManagementApi et \*-AzureRmApiManagementCertificate peuvent maintenant gérer les chemins d’accès relatifs</span><span class="sxs-lookup"><span data-stu-id="ad573-241">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="ad573-242">Problème résolu https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="ad573-242">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="ad573-243">CertificateInformation est une propriété définissable permettant à la cmdlet Set-AzureRmApiManagement de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="ad573-243">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="ad573-244">Résolu en passant au nuget 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="ad573-244">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="ad573-245">Problème résolu https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="ad573-245">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="ad573-246">Recherche par nom sur produit du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="ad573-246">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="ad573-247">Problème résolu https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="ad573-247">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="ad573-248">Recherche par nom sur Api du filtre Odata résolue</span><span class="sxs-lookup"><span data-stu-id="ad573-248">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="ad573-249">Ajout de la prise en charge de l’enregistreur d'événements AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="ad573-249">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="ad573-250">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-250">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-251">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ad573-251">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ad573-252">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="ad573-252">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ad573-253">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ad573-253">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="ad573-254">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="ad573-254">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-255">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-255">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-256">Modification de la présentation d’une sortie de cmdlet par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="ad573-256">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ad573-257">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ad573-257">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ad573-258">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="ad573-258">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="ad573-259">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-259">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-260">Résolution du problème de création d’applications managées depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ad573-260">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-261">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-261">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-262">Problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="ad573-262">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ad573-263">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad573-263">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ad573-264">Ajout de la prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ad573-264">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ad573-265">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ad573-265">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ad573-266">Ajout de la prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="ad573-266">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ad573-267">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad573-267">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ad573-268">Ajout de la prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="ad573-268">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ad573-269">Ajout de la prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="ad573-269">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ad573-270">Ajout de la prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad573-270">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="ad573-271">6.8.0 - Août 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-271">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad573-272">Généralités</span><span class="sxs-lookup"><span data-stu-id="ad573-272">General</span></span>
* <span data-ttu-id="ad573-273">Résolution du problème relatif aux groupes de ressources par défaut non définis.</span><span class="sxs-lookup"><span data-stu-id="ad573-273">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ad573-274">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-274">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-275">Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ad573-275">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-276">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-276">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-277">Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ad573-277">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="ad573-278">Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé</span><span class="sxs-lookup"><span data-stu-id="ad573-278">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="ad573-279">Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine</span><span class="sxs-lookup"><span data-stu-id="ad573-279">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ad573-280">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad573-280">AzureRM.IotHub</span></span>
* <span data-ttu-id="ad573-281">Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="ad573-281">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-282">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-282">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-283">Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table</span><span class="sxs-lookup"><span data-stu-id="ad573-283">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ad573-284">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ad573-284">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ad573-285">Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause</span><span class="sxs-lookup"><span data-stu-id="ad573-285">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-286">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-286">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-287">Résolution du problème de création d’application managée depuis le Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ad573-287">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-289">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="ad573-289">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ad573-290">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad573-290">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ad573-291">Prise en charge de la méthode de routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ad573-291">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="ad573-292">Nouveau paramètre « MaxReturn » pour le routage MultiValue</span><span class="sxs-lookup"><span data-stu-id="ad573-292">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="ad573-293">Prise en charge de la méthode de routage Subnet</span><span class="sxs-lookup"><span data-stu-id="ad573-293">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="ad573-294">Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad573-294">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="ad573-295">Prise en charge des en-têtes personnalisés dans les profils</span><span class="sxs-lookup"><span data-stu-id="ad573-295">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="ad573-296">Prise en charge des plages de codes avec l’état Attendu dans les profils</span><span class="sxs-lookup"><span data-stu-id="ad573-296">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="ad573-297">Prise en charge des en-têtes personnalisés dans les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ad573-297">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ad573-298">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ad573-298">AzureRM.Websites</span></span>
* <span data-ttu-id="ad573-299">Résolution du problème relatif aux groupes de ressources par défaut mal définis.</span><span class="sxs-lookup"><span data-stu-id="ad573-299">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="ad573-300">6.7.0 : août 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-300">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ad573-301">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-301">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-302">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-302">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ad573-303">Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.</span><span class="sxs-lookup"><span data-stu-id="ad573-303">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="ad573-304">Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.</span><span class="sxs-lookup"><span data-stu-id="ad573-304">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="ad573-305">Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="ad573-305">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="ad573-306">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-306">Azure.Storage</span></span>
* <span data-ttu-id="ad573-307">Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="ad573-307">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="ad573-308">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="ad573-308">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ad573-309">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad573-309">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ad573-310">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="ad573-311">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad573-311">Azure.AnalysisServices</span></span>
* <span data-ttu-id="ad573-312">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ad573-313">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad573-313">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ad573-314">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="ad573-315">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ad573-315">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="ad573-316">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-316">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ad573-317">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ad573-317">AzureRM.Automation</span></span>
* <span data-ttu-id="ad573-318">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-318">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="ad573-319">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="ad573-319">AzureRM.Backup</span></span>
* <span data-ttu-id="ad573-320">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-320">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ad573-321">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ad573-321">AzureRM.Batch</span></span>
* <span data-ttu-id="ad573-322">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-322">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="ad573-323">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="ad573-323">AzureRM.Billing</span></span>
* <span data-ttu-id="ad573-324">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-324">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="ad573-325">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="ad573-325">AzureRM.Cdn</span></span>
* <span data-ttu-id="ad573-326">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-326">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="ad573-327">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ad573-327">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="ad573-328">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-328">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-329">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-329">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-330">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-330">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ad573-331">Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="ad573-331">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="ad573-332">Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad573-332">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="ad573-333">Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.</span><span class="sxs-lookup"><span data-stu-id="ad573-333">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ad573-334">Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.</span><span class="sxs-lookup"><span data-stu-id="ad573-334">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ad573-335">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ad573-335">AzureRM.Consumption</span></span>
* <span data-ttu-id="ad573-336">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-336">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="ad573-337">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ad573-337">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="ad573-338">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-338">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="ad573-339">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad573-339">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="ad573-340">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-340">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="ad573-341">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="ad573-341">AzureRM.DataFactories</span></span>
* <span data-ttu-id="ad573-342">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-342">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ad573-343">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ad573-343">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ad573-344">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-344">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ad573-345">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ad573-345">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ad573-346">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-346">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ad573-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad573-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ad573-348">Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad573-348">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="ad573-349">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.</span><span class="sxs-lookup"><span data-stu-id="ad573-349">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ad573-350">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-350">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ad573-351">Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.</span><span class="sxs-lookup"><span data-stu-id="ad573-351">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="ad573-352">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="ad573-352">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="ad573-353">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-353">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="ad573-354">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="ad573-354">AzureRM.Dns</span></span>
* <span data-ttu-id="ad573-355">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-355">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ad573-356">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad573-356">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ad573-357">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-357">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ad573-358">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad573-358">AzureRM.EventHub</span></span>
* <span data-ttu-id="ad573-359">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-359">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="ad573-360">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ad573-360">AzureRM.HDInsight</span></span>
* <span data-ttu-id="ad573-361">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-361">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ad573-362">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ad573-362">AzureRM.Insights</span></span>
* <span data-ttu-id="ad573-363">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-363">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="ad573-364">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="ad573-364">AzureRM.IotHub</span></span>
* <span data-ttu-id="ad573-365">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-365">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ad573-366">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad573-366">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ad573-367">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-367">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ad573-368">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad573-368">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ad573-369">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-369">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="ad573-370">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ad573-370">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="ad573-371">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-371">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="ad573-372">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ad573-372">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="ad573-373">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-373">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="ad573-374">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ad573-374">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="ad573-375">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-375">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="ad573-376">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="ad573-376">AzureRM.Media</span></span>
* <span data-ttu-id="ad573-377">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-377">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-378">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-378">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-379">Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ad573-379">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="ad573-380">Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ad573-380">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ad573-381">Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ad573-381">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="ad573-382">Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ad573-382">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ad573-383">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.</span><span class="sxs-lookup"><span data-stu-id="ad573-383">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="ad573-384">Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="ad573-384">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ad573-385">Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.</span><span class="sxs-lookup"><span data-stu-id="ad573-385">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="ad573-386">Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ad573-386">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="ad573-387">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ad573-387">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="ad573-388">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="ad573-389">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad573-389">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ad573-390">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-390">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ad573-391">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad573-391">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ad573-392">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-392">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="ad573-393">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ad573-393">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="ad573-394">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-394">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="ad573-395">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ad573-395">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="ad573-396">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ad573-397">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ad573-397">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ad573-398">Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="ad573-398">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="ad573-399">La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.</span><span class="sxs-lookup"><span data-stu-id="ad573-399">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="ad573-400">Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="ad573-400">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="ad573-401">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-401">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="ad573-402">Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ad573-402">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="ad573-403">Groupe de ressources vers lequel les disques managés sont restaurés.</span><span class="sxs-lookup"><span data-stu-id="ad573-403">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="ad573-404">S’applique à la sauvegarde des machines virtuelles avec disques managés.</span><span class="sxs-lookup"><span data-stu-id="ad573-404">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="ad573-405">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad573-405">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ad573-406">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="ad573-407">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ad573-407">AzureRM.RedisCache</span></span>
* <span data-ttu-id="ad573-408">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-408">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ad573-409">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ad573-409">AzureRM.Relay</span></span>
* <span data-ttu-id="ad573-410">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-410">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-411">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-411">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-412">Prise en charge du déploiement de modèle à l’étendue de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad573-412">Support template deployment at subscription scope.</span></span> <span data-ttu-id="ad573-413">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="ad573-413">Add new Cmdlets:</span></span>
    - <span data-ttu-id="ad573-414">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-414">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="ad573-415">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-415">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="ad573-416">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-416">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="ad573-417">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-417">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="ad573-418">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-418">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="ad573-419">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ad573-419">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="ad573-420">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ad573-420">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="ad573-421">Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="ad573-421">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="ad573-422">Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="ad573-422">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="ad573-423">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ad573-424">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ad573-424">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ad573-425">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-426">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-426">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-427">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ad573-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad573-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ad573-429">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ad573-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-430">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-431">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ad573-432">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-432">AzureRM.Storage</span></span>
* <span data-ttu-id="ad573-433">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="ad573-434">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="ad573-434">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="ad573-435">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ad573-436">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ad573-436">AzureRM.Tags</span></span>
* <span data-ttu-id="ad573-437">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ad573-438">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad573-438">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ad573-439">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-439">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="ad573-440">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="ad573-440">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="ad573-441">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-441">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ad573-442">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ad573-442">AzureRM.Websites</span></span>
* <span data-ttu-id="ad573-443">Mise à jour vers la dernière version d’Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-443">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="ad573-444">6.6.0 - juillet 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-444">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad573-445">Généralités</span><span class="sxs-lookup"><span data-stu-id="ad573-445">General</span></span>
* <span data-ttu-id="ad573-446">Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.</span><span class="sxs-lookup"><span data-stu-id="ad573-446">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ad573-447">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-447">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-448">Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.</span><span class="sxs-lookup"><span data-stu-id="ad573-448">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="ad573-449">Ajout des types ps1xml à Common.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-449">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ad573-450">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-450">Azure.Storage</span></span>
* <span data-ttu-id="ad573-451">Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.</span><span class="sxs-lookup"><span data-stu-id="ad573-451">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="ad573-452">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ad573-452">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ad573-453">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad573-453">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ad573-454">Problème résolu https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="ad573-454">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="ad573-455">Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract</span><span class="sxs-lookup"><span data-stu-id="ad573-455">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="ad573-456">Problème résolu https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="ad573-456">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="ad573-457">Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage</span><span class="sxs-lookup"><span data-stu-id="ad573-457">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="ad573-458">Problème résolu https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="ad573-458">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="ad573-459">Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId</span><span class="sxs-lookup"><span data-stu-id="ad573-459">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-460">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-460">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-461">Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="ad573-461">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="ad573-462">Correction de la cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="ad573-462">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="ad573-463">Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad573-463">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="ad573-464">(La paramètre ResouceGroupName est désormais facultatif.)</span><span class="sxs-lookup"><span data-stu-id="ad573-464">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="ad573-465">Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.</span><span class="sxs-lookup"><span data-stu-id="ad573-465">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="ad573-466">Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ad573-466">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="ad573-467">Mise à jour de l’exemple pour New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ad573-467">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="ad573-468">Ajout d’un exemple pour « New-AzureRmVM »</span><span class="sxs-lookup"><span data-stu-id="ad573-468">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="ad573-469">Mise à jour de la description pour Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="ad573-469">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="ad573-470">Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe.</span><span class="sxs-lookup"><span data-stu-id="ad573-470">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ad573-471">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ad573-471">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ad573-472">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="ad573-472">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="ad573-473">Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.</span><span class="sxs-lookup"><span data-stu-id="ad573-473">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="ad573-474">Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-474">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="ad573-475">Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="ad573-475">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ad573-476">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad573-476">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ad573-477">Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9</span><span class="sxs-lookup"><span data-stu-id="ad573-477">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ad573-478">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad573-478">AzureRM.EventHub</span></span>
* <span data-ttu-id="ad573-479">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="ad573-479">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="ad573-480">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="ad573-480">AzureRM.Insights</span></span>
* <span data-ttu-id="ad573-481">Correction de mise en forme de OutputType dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="ad573-481">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="ad573-482">À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor</span><span class="sxs-lookup"><span data-stu-id="ad573-482">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ad573-483">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad573-483">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ad573-484">Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-484">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-485">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-485">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-486">Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="ad573-486">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-487">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-487">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-488">Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="ad573-488">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="ad573-489">Correction du scénario de redirection avec « Set-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="ad573-489">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-490">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-490">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-491">Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression</span><span class="sxs-lookup"><span data-stu-id="ad573-491">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="ad573-492">quelques problèmes résolus</span><span class="sxs-lookup"><span data-stu-id="ad573-492">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="ad573-493">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-493">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-494">Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad573-494">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="ad573-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-495">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ad573-496">Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad573-496">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="ad573-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="ad573-497">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="ad573-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="ad573-498">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="ad573-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="ad573-499">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="ad573-500">Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ad573-500">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="ad573-501">Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="ad573-501">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="ad573-502">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-502">AzureRM.Storage</span></span>
* <span data-ttu-id="ad573-503">Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets</span><span class="sxs-lookup"><span data-stu-id="ad573-503">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="ad573-504">Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau</span><span class="sxs-lookup"><span data-stu-id="ad573-504">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="ad573-505">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad573-505">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ad573-506">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad573-506">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="ad573-507">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ad573-507">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="ad573-508">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="ad573-508">AzureRM.Tags</span></span>
* <span data-ttu-id="ad573-509">Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="ad573-509">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="ad573-510">6.5.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-510">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ad573-511">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-511">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-512">Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »</span><span class="sxs-lookup"><span data-stu-id="ad573-512">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ad573-513">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-513">Azure.Storage</span></span>
* <span data-ttu-id="ad573-514">Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule</span><span class="sxs-lookup"><span data-stu-id="ad573-514">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="ad573-515">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ad573-515">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="ad573-516">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ad573-516">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ad573-517">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad573-517">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ad573-518">Ajout de la propriété ResourceGroupName requise au système autonome.</span><span class="sxs-lookup"><span data-stu-id="ad573-518">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="ad573-519">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="ad573-519">AzureRM.Automation</span></span>
* <span data-ttu-id="ad573-520">Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »</span><span class="sxs-lookup"><span data-stu-id="ad573-520">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-521">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-522">Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad573-522">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="ad573-523">Ajout d’un exemple pour « Add-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="ad573-523">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ad573-524">Ajout d’exemples pour « Remove-AzureRmVmssExtension »</span><span class="sxs-lookup"><span data-stu-id="ad573-524">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="ad573-525">Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »</span><span class="sxs-lookup"><span data-stu-id="ad573-525">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="ad573-526">Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.</span><span class="sxs-lookup"><span data-stu-id="ad573-526">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ad573-527">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad573-527">AzureRM.EventHub</span></span>
* <span data-ttu-id="ad573-528">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="ad573-528">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ad573-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad573-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ad573-530">Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad573-530">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="ad573-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ad573-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="ad573-532">Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ad573-532">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-533">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-534">Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ad573-534">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="ad573-535">Mise à jour des applets de commande ci-dessous pour Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ad573-535">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="ad573-536">New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="ad573-536">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="ad573-537">New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ad573-537">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="ad573-538">Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2</span><span class="sxs-lookup"><span data-stu-id="ad573-538">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="ad573-539">Régénération des applets de commande RouteTable avec la dernière version du Générateur</span><span class="sxs-lookup"><span data-stu-id="ad573-539">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="ad573-540">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="ad573-540">AzureRM.Relay</span></span>
* <span data-ttu-id="ad573-541">Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple</span><span class="sxs-lookup"><span data-stu-id="ad573-541">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-542">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-542">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-543">Mise à jour des applets de commande Roleassignment et Roledefinition :</span><span class="sxs-lookup"><span data-stu-id="ad573-543">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="ad573-544">Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.</span><span class="sxs-lookup"><span data-stu-id="ad573-544">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="ad573-545">Correction de l’applet de commande Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad573-545">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="ad573-546">Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="ad573-546">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="ad573-547">Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="ad573-547">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-548">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-548">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-549">Ajout des paramètres Top et Skip à la liste des applets de commande</span><span class="sxs-lookup"><span data-stu-id="ad573-549">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="ad573-550">Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :</span><span class="sxs-lookup"><span data-stu-id="ad573-550">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="ad573-551">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ad573-551">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ad573-552">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ad573-552">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ad573-553">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ad573-553">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ad573-554">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ad573-554">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="ad573-555">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ad573-555">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="ad573-556">Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication</span><span class="sxs-lookup"><span data-stu-id="ad573-556">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ad573-557">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad573-557">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ad573-558">Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »</span><span class="sxs-lookup"><span data-stu-id="ad573-558">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ad573-559">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-559">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-560">Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée</span><span class="sxs-lookup"><span data-stu-id="ad573-560">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="ad573-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-561">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="ad573-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-562">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ad573-563">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ad573-563">AzureRM.Websites</span></span>
* <span data-ttu-id="ad573-564">Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.</span><span class="sxs-lookup"><span data-stu-id="ad573-564">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="ad573-565">Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour</span><span class="sxs-lookup"><span data-stu-id="ad573-565">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="ad573-566">`Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide</span><span class="sxs-lookup"><span data-stu-id="ad573-566">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="ad573-567">6.4.0 - Juillet 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-567">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ad573-568">Généralités</span><span class="sxs-lookup"><span data-stu-id="ad573-568">General</span></span>
* <span data-ttu-id="ad573-569">Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules</span><span class="sxs-lookup"><span data-stu-id="ad573-569">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="ad573-570">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-570">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-571">Ajout de l’attribut Ps1Xml aux types de sortie de base</span><span class="sxs-lookup"><span data-stu-id="ad573-571">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-572">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-572">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-573">Fonctionnalité IP Tag pour VMSS</span><span class="sxs-lookup"><span data-stu-id="ad573-573">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="ad573-574">La cmdlet New-AzureRmVmssIpTagConfig est ajoutée</span><span class="sxs-lookup"><span data-stu-id="ad573-574">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="ad573-575">Ajout du paramètre IpTag à New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-575">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="ad573-576">Fonctionnalité de restauration du système d’exploitation automatique pour VMSS</span><span class="sxs-lookup"><span data-stu-id="ad573-576">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="ad573-577">Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-577">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="ad573-578">Fonctionnalité OS Upgrade History pour Vmss</span><span class="sxs-lookup"><span data-stu-id="ad573-578">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="ad573-579">Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-579">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="ad573-580">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ad573-580">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="ad573-581">Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad573-581">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="ad573-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ad573-582">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ad573-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ad573-583">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="ad573-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ad573-584">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ad573-585">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad573-585">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ad573-586">Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="ad573-586">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="ad573-587">Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ad573-587">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ad573-588">Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives</span><span class="sxs-lookup"><span data-stu-id="ad573-588">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="ad573-589">Correction de l’emplacement du test des applets de commande DataLake</span><span class="sxs-lookup"><span data-stu-id="ad573-589">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="ad573-590">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="ad573-590">AzureRM.EventHub</span></span>
* <span data-ttu-id="ad573-591">Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ad573-591">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="ad573-592">Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub.</span><span class="sxs-lookup"><span data-stu-id="ad573-592">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="ad573-593">Jeu de paramètres par défaut fourni.</span><span class="sxs-lookup"><span data-stu-id="ad573-593">Provided Default Parameter set.</span></span>
* <span data-ttu-id="ad573-594">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ad573-594">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ad573-595">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad573-595">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ad573-596">Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="ad573-596">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-597">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-597">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-598">Exposer les nouvelles références SKU pour Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ad573-598">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="ad573-599">Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="ad573-599">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="ad573-600">Ajout de Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ad573-600">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ad573-601">Ajout de Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ad573-601">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="ad573-602">Ajout de Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ad573-602">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ad573-603">Ajout de Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ad573-603">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ad573-604">Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ad573-604">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="ad573-605">Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ad573-605">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ad573-606">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ad573-606">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ad573-607">Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ad573-607">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ad573-608">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ad573-608">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ad573-609">Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="ad573-609">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="ad573-610">Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad573-610">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="ad573-611">Si un tel coffre existe, la cmdlet sort les informations du coffre.</span><span class="sxs-lookup"><span data-stu-id="ad573-611">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-612">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-612">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-613">Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :</span><span class="sxs-lookup"><span data-stu-id="ad573-613">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="ad573-614">Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="ad573-614">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="ad573-615">Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion</span><span class="sxs-lookup"><span data-stu-id="ad573-615">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="ad573-616">Ajouter les commutateurs -Effective et -All au paramètre de contrôle</span><span class="sxs-lookup"><span data-stu-id="ad573-616">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="ad573-617">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ad573-617">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="ad573-618">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="ad573-618">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ad573-619">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="ad573-619">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ad573-620">Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ad573-620">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="ad573-621">Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné</span><span class="sxs-lookup"><span data-stu-id="ad573-621">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="ad573-622">Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné</span><span class="sxs-lookup"><span data-stu-id="ad573-622">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="ad573-623">Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-623">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="ad573-624">Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ad573-624">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="ad573-625">Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande</span><span class="sxs-lookup"><span data-stu-id="ad573-625">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="ad573-626">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ad573-626">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="ad573-627">Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ad573-627">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ad573-628">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-628">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-629">Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ad573-629">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="ad573-630">Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets</span><span class="sxs-lookup"><span data-stu-id="ad573-630">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="ad573-631">6.3.0 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-631">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ad573-632">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-632">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-633">Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="ad573-633">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="ad573-634">Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent</span><span class="sxs-lookup"><span data-stu-id="ad573-634">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="ad573-635">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ad573-635">Azure.Storage</span></span>
* <span data-ttu-id="ad573-636">Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.</span><span class="sxs-lookup"><span data-stu-id="ad573-636">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-637">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-637">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-638">Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données</span><span class="sxs-lookup"><span data-stu-id="ad573-638">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="ad573-639">Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes</span><span class="sxs-lookup"><span data-stu-id="ad573-639">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="ad573-640">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ad573-640">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ad573-641">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ad573-641">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ad573-642">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="ad573-642">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="ad573-643">Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :</span><span class="sxs-lookup"><span data-stu-id="ad573-643">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="ad573-644">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad573-644">Start-AzureRmVM</span></span>
    - <span data-ttu-id="ad573-645">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad573-645">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="ad573-646">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad573-646">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="ad573-647">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ad573-647">Set-AzureRmVM</span></span>
    - <span data-ttu-id="ad573-648">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="ad573-648">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="ad573-649">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-649">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="ad573-650">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ad573-650">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="ad573-651">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="ad573-651">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="ad573-652">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-652">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="ad573-653">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-653">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="ad573-654">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-654">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="ad573-655">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ad573-655">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="ad573-656">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ad573-656">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="ad573-657">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ad573-657">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="ad573-658">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad573-658">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="ad573-659">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="ad573-659">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="ad573-660">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ad573-660">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="ad573-661">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="ad573-661">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="ad573-662">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad573-662">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="ad573-663">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ad573-663">AzureRM.EventGrid</span></span>
* <span data-ttu-id="ad573-664">Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ad573-664">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="ad573-665">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad573-665">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ad573-666">Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée</span><span class="sxs-lookup"><span data-stu-id="ad573-666">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="ad573-667">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ad573-667">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="ad573-668">Version publique des cmdlets Policy Insights</span><span class="sxs-lookup"><span data-stu-id="ad573-668">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="ad573-669">Utiliser l’API de version du 04/04/2018</span><span class="sxs-lookup"><span data-stu-id="ad573-669">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="ad573-670">Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="ad573-670">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="ad573-671">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ad573-671">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ad573-672">Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="ad573-672">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="ad573-673">Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="ad573-673">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ad573-674">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-674">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-675">Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="ad573-675">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ad573-676">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad573-676">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ad573-677">Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-677">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ad573-678">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ad573-678">AzureRM.Websites</span></span>
* <span data-ttu-id="ad573-679">Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ad573-679">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="ad573-680">Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad573-680">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="ad573-681">6.2.1 - juin 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-681">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="ad573-682">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ad573-682">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="ad573-683">Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre</span><span class="sxs-lookup"><span data-stu-id="ad573-683">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="ad573-684">6.2.0 - Juin 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-684">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ad573-685">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-685">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-686">Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module</span><span class="sxs-lookup"><span data-stu-id="ad573-686">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="ad573-687">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="ad573-687">AzureRM.Compute</span></span>
* <span data-ttu-id="ad573-688">Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)</span><span class="sxs-lookup"><span data-stu-id="ad573-688">VMSS VM Update feature</span></span>
    - <span data-ttu-id="ad573-689">Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »</span><span class="sxs-lookup"><span data-stu-id="ad573-689">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="ad573-690">Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ad573-690">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="ad573-691">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ad573-691">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="ad573-692">Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad573-692">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="ad573-693">Ajout de l’opération de référentiel de configuration de fabrique</span><span class="sxs-lookup"><span data-stu-id="ad573-693">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="ad573-694">Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret</span><span class="sxs-lookup"><span data-stu-id="ad573-694">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="ad573-695">Mise à jour de plusieurs types de modèle de SecretBase à l’objet</span><span class="sxs-lookup"><span data-stu-id="ad573-695">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="ad573-696">Ajout d’un déclencheur d’événements d’objet Blob</span><span class="sxs-lookup"><span data-stu-id="ad573-696">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="ad573-697">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad573-697">AzureRM.KeyVault</span></span>
* <span data-ttu-id="ad573-698">Mise à jour de la documentation avec l’exemple de sortie</span><span class="sxs-lookup"><span data-stu-id="ad573-698">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="ad573-699">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-699">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-700">Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher</span><span class="sxs-lookup"><span data-stu-id="ad573-700">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="ad573-701">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="ad573-701">AzureRM.Resources</span></span>
* <span data-ttu-id="ad573-702">Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »</span><span class="sxs-lookup"><span data-stu-id="ad573-702">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="ad573-703">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="ad573-703">AzureRM.Scheduler</span></span>
* <span data-ttu-id="ad573-704">Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification</span><span class="sxs-lookup"><span data-stu-id="ad573-704">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="ad573-705">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-705">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-706">Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType</span><span class="sxs-lookup"><span data-stu-id="ad573-706">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="ad573-707">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad573-707">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ad573-708">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ad573-708">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ad573-709">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ad573-709">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ad573-710">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ad573-710">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ad573-711">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad573-711">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="ad573-712">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="ad573-712">AzureRM.Websites</span></span>
* <span data-ttu-id="ad573-713">« New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.</span><span class="sxs-lookup"><span data-stu-id="ad573-713">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="ad573-714">6.1.0 - Mai 2018</span><span class="sxs-lookup"><span data-stu-id="ad573-714">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="ad573-715">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad573-715">AzureRM.Profile</span></span>
* <span data-ttu-id="ad573-716">Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom</span><span class="sxs-lookup"><span data-stu-id="ad573-716">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="ad573-717">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ad573-717">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="ad573-718">Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes</span><span class="sxs-lookup"><span data-stu-id="ad573-718">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="ad573-719">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ad573-719">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="ad573-720">Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="ad573-720">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="ad573-721">Ajout de la prise en charge du principal ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad573-721">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="ad573-722">Ajout de la prise en charge de l’enregistreur d’événements Application Insights</span><span class="sxs-lookup"><span data-stu-id="ad573-722">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="ad573-723">Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api</span><span class="sxs-lookup"><span data-stu-id="ad573-723">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="ad573-724">Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification</span><span class="sxs-lookup"><span data-stu-id="ad573-724">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="ad573-725">Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy</span><span class="sxs-lookup"><span data-stu-id="ad573-725">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="ad573-726">Ajout de la prise en charge de l’identité MSI</span><span class="sxs-lookup"><span data-stu-id="ad573-726">Added support for MSI identity</span></span>
* <span data-ttu-id="ad573-727">Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :</span><span class="sxs-lookup"><span data-stu-id="ad573-727">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="ad573-728">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="ad573-728">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="ad573-729">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-729">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="ad573-730">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="ad573-730">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="ad573-731">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="ad573-731">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="ad573-732">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="ad573-732">AzureRM.Batch</span></span>
* <span data-ttu-id="ad573-733">Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="ad573-733">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="ad573-734">Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="ad573-734">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="ad573-735">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="ad573-735">AzureRM.Consumption</span></span>
* <span data-ttu-id="ad573-736">Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="ad573-736">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="ad573-737">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ad573-737">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="ad573-738">Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="ad573-738">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="ad573-739">Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ad573-739">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="ad573-740">Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ad573-740">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="ad573-741">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="ad573-741">AzureRM.Network</span></span>
* <span data-ttu-id="ad573-742">Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="ad573-742">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="ad573-743">Ajout d’une cmdlet pour créer une configuration de protocole :</span><span class="sxs-lookup"><span data-stu-id="ad573-743">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="ad573-744">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad573-744">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="ad573-745">Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="ad573-745">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="ad573-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-746">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ad573-747">Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :</span><span class="sxs-lookup"><span data-stu-id="ad573-747">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="ad573-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-748">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="ad573-749">Ajout d’une cmdlet pour récupérer une connexion de circuit :</span><span class="sxs-lookup"><span data-stu-id="ad573-749">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="ad573-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ad573-750">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="ad573-751">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ad573-751">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="ad573-752">Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)</span><span class="sxs-lookup"><span data-stu-id="ad573-752">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="ad573-753">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="ad573-753">AzureRM.Sql</span></span>
* <span data-ttu-id="ad573-754">Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ad573-754">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="ad573-755">Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span><span class="sxs-lookup"><span data-stu-id="ad573-755">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="ad573-756">Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).</span><span class="sxs-lookup"><span data-stu-id="ad573-756">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="ad573-757">Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.</span><span class="sxs-lookup"><span data-stu-id="ad573-757">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="ad573-758">Les cmdlets mises à jour incluent :</span><span class="sxs-lookup"><span data-stu-id="ad573-758">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="ad573-759">New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad573-759">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="ad573-760">New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ad573-760">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="ad573-761">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ad573-761">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="ad573-762">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ad573-762">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="ad573-763">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ad573-763">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="ad573-764">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ad573-764">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="ad573-765">Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name</span><span class="sxs-lookup"><span data-stu-id="ad573-765">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
