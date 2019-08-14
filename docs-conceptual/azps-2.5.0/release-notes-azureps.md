---
ms.openlocfilehash: 77cb28e47d8dddcf3936edff23f794de3b78442b
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861187"
---
## <a name="250---july-2019"></a><span data-ttu-id="1e2c0-101">2.5.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-102">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-103">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e2c0-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="1e2c0-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="1e2c0-105">Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-106">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-107">Correction d’une faute de frappe dans la chaîne de ressource</span><span class="sxs-lookup"><span data-stu-id="1e2c0-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e2c0-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e2c0-109">Prise en charge de NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-110">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-111">Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1e2c0-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e2c0-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1e2c0-113">Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication</span><span class="sxs-lookup"><span data-stu-id="1e2c0-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="1e2c0-114">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="1e2c0-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e2c0-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e2c0-115">Az.DataFactory</span></span>
* <span data-ttu-id="1e2c0-116">Mise à jour du SDK .NET ADF avec la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="1e2c0-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="1e2c0-117">Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e2c0-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-118">Az.EventHub</span></span>
* <span data-ttu-id="1e2c0-119">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1e2c0-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1e2c0-120">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="1e2c0-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e2c0-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-121">Az.KeyVault</span></span>
* <span data-ttu-id="1e2c0-122">Possibilité de spécifier KeySize pour les stratégies de certificat</span><span class="sxs-lookup"><span data-stu-id="1e2c0-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e2c0-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-123">Az.LogicApp</span></span>
* <span data-ttu-id="1e2c0-124">Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="1e2c0-125">Ajout d’un nouveau paramètre MapType pour le filtrage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="1e2c0-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-126">Az.ManagedServices</span></span>
* <span data-ttu-id="1e2c0-127">Ajout de la prise en charge de l’API version 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-128">Az.Network</span></span>
* <span data-ttu-id="1e2c0-129">Prise en charge d’un point de terminaison privé et du service de liaison privée</span><span class="sxs-lookup"><span data-stu-id="1e2c0-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="1e2c0-130">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-130">New cmdlets</span></span>
        - <span data-ttu-id="1e2c0-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2c0-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e2c0-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1e2c0-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e2c0-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e2c0-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e2c0-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="1e2c0-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="1e2c0-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="1e2c0-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="1e2c0-139">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1e2c0-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="1e2c0-140">Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="1e2c0-141">Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag pour activer ou désactiver l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="1e2c0-142">Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag pour activer ou désactiver l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="1e2c0-143">Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="1e2c0-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="1e2c0-144">Activation du protocole ICMP pour les configurations des règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="1e2c0-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="1e2c0-145">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="1e2c0-145">Updated cmdlets</span></span>
        - <span data-ttu-id="1e2c0-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1e2c0-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="1e2c0-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="1e2c0-149">Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="1e2c0-150">Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="1e2c0-151">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="1e2c0-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1e2c0-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="1e2c0-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="1e2c0-155">Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde</span><span class="sxs-lookup"><span data-stu-id="1e2c0-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="1e2c0-156">Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="1e2c0-157">Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e2c0-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e2c0-159">Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="1e2c0-160">Correction de la gestion des expressions régulières null des journaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="1e2c0-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-162">Mise à jour de « Get-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1e2c0-163">Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="1e2c0-164">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="1e2c0-165">Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="1e2c0-166">Mise à jour de « Set-AzRecoveryServicesVaultContext.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="1e2c0-167">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1e2c0-168">Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="1e2c0-169">Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="1e2c0-170">Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="1e2c0-171">Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-172">Az.Resources</span></span>
- <span data-ttu-id="1e2c0-173">Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="1e2c0-174">Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="1e2c0-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e2c0-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-175">Az.ServiceBus</span></span>
* <span data-ttu-id="1e2c0-176">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="1e2c0-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="1e2c0-177">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="1e2c0-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-178">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-179">Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1e2c0-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="1e2c0-180">Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="1e2c0-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="1e2c0-181">Correction d’une faute de frappe dans un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-182">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-183">Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="1e2c0-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1e2c0-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1e2c0-184">Az.StorageSync</span></span>
* <span data-ttu-id="1e2c0-185">Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="1e2c0-186">Résolution du problème 9551 pour honorer TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="1e2c0-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-187">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-188">Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="1e2c0-189">Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="1e2c0-190">Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="1e2c0-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="1e2c0-191">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-192">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-193">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="1e2c0-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="1e2c0-194">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="1e2c0-195">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e2c0-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="1e2c0-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-196">Az.Advisor</span></span>
* <span data-ttu-id="1e2c0-197">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="1e2c0-198">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="1e2c0-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="1e2c0-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-199">Az.ApiManagement</span></span>
* <span data-ttu-id="1e2c0-200">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="1e2c0-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="1e2c0-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="1e2c0-202">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="1e2c0-203">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="1e2c0-204">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="1e2c0-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="1e2c0-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="1e2c0-206">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-207">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-208">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-209">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-210">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e2c0-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e2c0-211">Az.DataFactory</span></span>
* <span data-ttu-id="1e2c0-212">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e2c0-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e2c0-213">Az.EventGrid</span></span>
* <span data-ttu-id="1e2c0-214">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e2c0-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-215">Az.IotHub</span></span>
* <span data-ttu-id="1e2c0-216">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-217">Az.Network</span></span>
* <span data-ttu-id="1e2c0-218">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="1e2c0-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="1e2c0-219">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e2c0-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e2c0-221">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="1e2c0-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="1e2c0-222">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="1e2c0-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e2c0-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e2c0-224">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="1e2c0-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-226">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="1e2c0-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-227">Az.Resources</span></span>
    - <span data-ttu-id="1e2c0-228">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="1e2c0-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="1e2c0-229">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="1e2c0-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="1e2c0-230">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="1e2c0-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="1e2c0-231">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="1e2c0-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e2c0-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-232">Az.ServiceBus</span></span>
* <span data-ttu-id="1e2c0-233">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-234">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-235">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="1e2c0-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="1e2c0-236">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="1e2c0-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1e2c0-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1e2c0-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="1e2c0-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1e2c0-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="1e2c0-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="1e2c0-243">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="1e2c0-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-244">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-245">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="1e2c0-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1e2c0-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="1e2c0-247">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="1e2c0-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="1e2c0-248">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="1e2c0-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="1e2c0-249">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="1e2c0-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="1e2c0-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="1e2c0-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="1e2c0-252">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="1e2c0-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="1e2c0-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1e2c0-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="1e2c0-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="1e2c0-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="1e2c0-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="1e2c0-255">Az.StorageSync</span></span>
* <span data-ttu-id="1e2c0-256">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="1e2c0-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="1e2c0-257">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-258">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-259">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="1e2c0-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="1e2c0-260">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="1e2c0-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="1e2c0-261">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="1e2c0-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="1e2c0-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1e2c0-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="1e2c0-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="1e2c0-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-264">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-265">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="1e2c0-266">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="1e2c0-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1e2c0-267">Az.Dns</span></span>
* <span data-ttu-id="1e2c0-268">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e2c0-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e2c0-269">Az.EventGrid</span></span>
* <span data-ttu-id="1e2c0-270">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="1e2c0-271">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-271">New cmdlets:</span></span>
    - <span data-ttu-id="1e2c0-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1e2c0-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1e2c0-273">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1e2c0-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1e2c0-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1e2c0-275">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="1e2c0-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="1e2c0-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="1e2c0-277">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1e2c0-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1e2c0-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1e2c0-279">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="1e2c0-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="1e2c0-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="1e2c0-281">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="1e2c0-282">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1e2c0-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1e2c0-283">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="1e2c0-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1e2c0-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="1e2c0-285">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="1e2c0-286">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="1e2c0-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="1e2c0-287">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="1e2c0-288">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="1e2c0-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1e2c0-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="1e2c0-290">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1e2c0-291">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="1e2c0-292">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="1e2c0-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="1e2c0-293">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="1e2c0-294">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="1e2c0-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="1e2c0-295">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="1e2c0-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="1e2c0-296">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="1e2c0-297">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="1e2c0-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="1e2c0-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="1e2c0-299">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="1e2c0-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="1e2c0-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="1e2c0-301">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="1e2c0-302">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e2c0-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-303">Az.FrontDoor</span></span>
* <span data-ttu-id="1e2c0-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1e2c0-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="1e2c0-305">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="1e2c0-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1e2c0-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="1e2c0-307">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="1e2c0-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-308">Az.Network</span></span>
* <span data-ttu-id="1e2c0-309">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="1e2c0-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="1e2c0-310">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-310">New cmdlets</span></span>
        - <span data-ttu-id="1e2c0-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="1e2c0-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="1e2c0-312">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1e2c0-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="1e2c0-313">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-313">New cmdlets</span></span> 
        - <span data-ttu-id="1e2c0-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="1e2c0-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="1e2c0-315">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="1e2c0-316">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-316">New cmdlets</span></span> 
        - <span data-ttu-id="1e2c0-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="1e2c0-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1e2c0-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="1e2c0-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="1e2c0-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="1e2c0-322">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2c0-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="1e2c0-323">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-323">New cmdlets</span></span>
        - <span data-ttu-id="1e2c0-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2c0-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e2c0-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2c0-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e2c0-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="1e2c0-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="1e2c0-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="1e2c0-328">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="1e2c0-329">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="1e2c0-330">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="1e2c0-331">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="1e2c0-332">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="1e2c0-333">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1e2c0-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="1e2c0-334">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="1e2c0-335">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="1e2c0-336">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="1e2c0-337">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="1e2c0-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="1e2c0-338">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="1e2c0-339">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="1e2c0-340">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="1e2c0-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="1e2c0-341">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="1e2c0-342">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="1e2c0-343">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="1e2c0-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="1e2c0-344">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="1e2c0-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="1e2c0-345">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="1e2c0-346">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1e2c0-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="1e2c0-347">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="1e2c0-348">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1e2c0-349">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="1e2c0-350">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e2c0-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e2c0-352">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-353">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-354">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="1e2c0-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="1e2c0-355">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1e2c0-356">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="1e2c0-357">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e2c0-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e2c0-359">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-360">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-361">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="1e2c0-362">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="1e2c0-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="1e2c0-363">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="1e2c0-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e2c0-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1e2c0-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e2c0-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1e2c0-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e2c0-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="1e2c0-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1e2c0-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="1e2c0-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="1e2c0-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-369">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-370">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="1e2c0-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="1e2c0-372">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="1e2c0-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="1e2c0-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-374">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-375">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="1e2c0-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="1e2c0-376">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1e2c0-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="1e2c0-377">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="1e2c0-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e2c0-378">Az.Cdn</span></span>
* <span data-ttu-id="1e2c0-379">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-380">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-381">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="1e2c0-382">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e2c0-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e2c0-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-383">Az.EventHub</span></span>
* <span data-ttu-id="1e2c0-384">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="1e2c0-385">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2c0-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-386">Az.Network</span></span>
* <span data-ttu-id="1e2c0-387">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="1e2c0-388">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="1e2c0-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e2c0-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e2c0-390">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="1e2c0-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-392">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="1e2c0-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e2c0-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-393">Az.ServiceBus</span></span>
* <span data-ttu-id="1e2c0-394">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2c0-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e2c0-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e2c0-396">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="1e2c0-397">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-398">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-399">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="1e2c0-400">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="1e2c0-401">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="1e2c0-402">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-403">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-404">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="1e2c0-405">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="1e2c0-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-406">Az.ApiManagement</span></span>
* <span data-ttu-id="1e2c0-407">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="1e2c0-408">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="1e2c0-409">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="1e2c0-410">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="1e2c0-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="1e2c0-411">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="1e2c0-412">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="1e2c0-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="1e2c0-413">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="1e2c0-414">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="1e2c0-415">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="1e2c0-416">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="1e2c0-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="1e2c0-417">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="1e2c0-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="1e2c0-418">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="1e2c0-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="1e2c0-419">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="1e2c0-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="1e2c0-420">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="1e2c0-421">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="1e2c0-422">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="1e2c0-423">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="1e2c0-424">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="1e2c0-425">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="1e2c0-426">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="1e2c0-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="1e2c0-427">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="1e2c0-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="1e2c0-428">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="1e2c0-429">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="1e2c0-430">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="1e2c0-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="1e2c0-431">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="1e2c0-432">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="1e2c0-433">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="1e2c0-434">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="1e2c0-435">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="1e2c0-436">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="1e2c0-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="1e2c0-437">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="1e2c0-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="1e2c0-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="1e2c0-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="1e2c0-439">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="1e2c0-440">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1e2c0-441">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="1e2c0-442">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="1e2c0-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="1e2c0-443">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="1e2c0-444">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="1e2c0-445">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="1e2c0-446">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="1e2c0-447">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1e2c0-448">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="1e2c0-449">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="1e2c0-450">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="1e2c0-451">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="1e2c0-452">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="1e2c0-453">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="1e2c0-454">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="1e2c0-455">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="1e2c0-456">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="1e2c0-457">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="1e2c0-458">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="1e2c0-459">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="1e2c0-460">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="1e2c0-461">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="1e2c0-462">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="1e2c0-463">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1e2c0-464">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1e2c0-465">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1e2c0-466">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1e2c0-467">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="1e2c0-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="1e2c0-468">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="1e2c0-469">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="1e2c0-470">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="1e2c0-471">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="1e2c0-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="1e2c0-472">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="1e2c0-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="1e2c0-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="1e2c0-474">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="1e2c0-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="1e2c0-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="1e2c0-476">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="1e2c0-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="1e2c0-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="1e2c0-478">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="1e2c0-479">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="1e2c0-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="1e2c0-481">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="1e2c0-482">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="1e2c0-483">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-484">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-485">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="1e2c0-486">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="1e2c0-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="1e2c0-487">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="1e2c0-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="1e2c0-488">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="1e2c0-489">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="1e2c0-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="1e2c0-490">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="1e2c0-491">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-492">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-493">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="1e2c0-494">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-496">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e2c0-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-497">Az.Monitor</span></span>
* <span data-ttu-id="1e2c0-498">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="1e2c0-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-499">Az.Network</span></span>
* <span data-ttu-id="1e2c0-500">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="1e2c0-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="1e2c0-501">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="1e2c0-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e2c0-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="1e2c0-503">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1e2c0-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-504">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-505">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-506">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-507">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="1e2c0-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="1e2c0-508">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-509">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-510">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="1e2c0-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e2c0-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e2c0-512">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="1e2c0-513">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-514">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-515">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="1e2c0-516">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="1e2c0-517">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="1e2c0-518">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="1e2c0-519">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="1e2c0-520">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c0-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="1e2c0-521">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="1e2c0-521">Breaking changes</span></span>
    - <span data-ttu-id="1e2c0-522">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="1e2c0-523">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="1e2c0-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="1e2c0-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="1e2c0-525">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="1e2c0-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="1e2c0-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="1e2c0-526">Az.Dns</span></span>
* <span data-ttu-id="1e2c0-527">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="1e2c0-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="1e2c0-528">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="1e2c0-529">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="1e2c0-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-530">Az.FrontDoor</span></span>
* <span data-ttu-id="1e2c0-531">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="1e2c0-532">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="1e2c0-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1e2c0-533">Az.HDInsight</span></span>
* <span data-ttu-id="1e2c0-534">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="1e2c0-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e2c0-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="1e2c0-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e2c0-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1e2c0-537">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1e2c0-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="1e2c0-538">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="1e2c0-539">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="1e2c0-540">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e2c0-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-541">Az.Monitor</span></span>
* <span data-ttu-id="1e2c0-542">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="1e2c0-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="1e2c0-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="1e2c0-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="1e2c0-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="1e2c0-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="1e2c0-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="1e2c0-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="1e2c0-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="1e2c0-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="1e2c0-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="1e2c0-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e2c0-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e2c0-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e2c0-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e2c0-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="1e2c0-554">[Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="1e2c0-554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="1e2c0-555">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-556">Az.Network</span></span>
* <span data-ttu-id="1e2c0-557">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="1e2c0-558">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-558">New cmdlets</span></span>
        - <span data-ttu-id="1e2c0-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="1e2c0-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="1e2c0-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="1e2c0-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="1e2c0-563">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="1e2c0-563">Updated cmdlets</span></span>
        - <span data-ttu-id="1e2c0-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1e2c0-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="1e2c0-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="1e2c0-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="1e2c0-566">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="1e2c0-567">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="1e2c0-568">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e2c0-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e2c0-570">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="1e2c0-571">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="1e2c0-572">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-574">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="1e2c0-575">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="1e2c0-576">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="1e2c0-577">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="1e2c0-578">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="1e2c0-579">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="1e2c0-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1e2c0-580">Az.Relay</span></span>
* <span data-ttu-id="1e2c0-581">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="1e2c0-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e2c0-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-582">Az.ServiceBus</span></span>
* <span data-ttu-id="1e2c0-583">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="1e2c0-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-584">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-585">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="1e2c0-586">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="1e2c0-587">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="1e2c0-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="1e2c0-589">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="1e2c0-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="1e2c0-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="1e2c0-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-593">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-594">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="1e2c0-595">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="1e2c0-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="1e2c0-596">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e2c0-597">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-597">Highlights since the last major release</span></span>
* <span data-ttu-id="1e2c0-598">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="1e2c0-598">General availability of `Az` module</span></span>
* <span data-ttu-id="1e2c0-599">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1e2c0-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1e2c0-600">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1e2c0-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1e2c0-601">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1e2c0-602">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e2c0-603">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1e2c0-604">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-605">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-606">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="1e2c0-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="1e2c0-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e2c0-607">Az.Batch</span></span>
* <span data-ttu-id="1e2c0-608">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e2c0-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e2c0-609">Az.Cdn</span></span>
* <span data-ttu-id="1e2c0-610">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e2c0-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e2c0-612">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-613">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-614">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="1e2c0-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="1e2c0-615">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e2c0-616">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="1e2c0-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e2c0-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e2c0-617">Az.DataFactory</span></span>
* <span data-ttu-id="1e2c0-618">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-620">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e2c0-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e2c0-621">Az.EventGrid</span></span>
* <span data-ttu-id="1e2c0-622">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e2c0-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-623">Az.EventHub</span></span>
* <span data-ttu-id="1e2c0-624">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="1e2c0-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="1e2c0-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1e2c0-625">Az.HDInsight</span></span>
* <span data-ttu-id="1e2c0-626">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e2c0-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-627">Az.IotHub</span></span>
* <span data-ttu-id="1e2c0-628">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e2c0-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-629">Az.KeyVault</span></span>
* <span data-ttu-id="1e2c0-630">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e2c0-631">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="1e2c0-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="1e2c0-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1e2c0-632">Az.MachineLearning</span></span>
* <span data-ttu-id="1e2c0-633">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="1e2c0-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1e2c0-634">Az.Media</span></span>
* <span data-ttu-id="1e2c0-635">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e2c0-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-636">Az.Monitor</span></span>
  * <span data-ttu-id="1e2c0-637">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="1e2c0-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="1e2c0-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="1e2c0-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="1e2c0-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="1e2c0-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1e2c0-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="1e2c0-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="1e2c0-643">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="1e2c0-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-644">Az.Network</span></span>
* <span data-ttu-id="1e2c0-645">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e2c0-646">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="1e2c0-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="1e2c0-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="1e2c0-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="1e2c0-648">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e2c0-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e2c0-650">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="1e2c0-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="1e2c0-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="1e2c0-652">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-654">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e2c0-655">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="1e2c0-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="1e2c0-656">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="1e2c0-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="1e2c0-657">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="1e2c0-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1e2c0-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1e2c0-658">Az.RedisCache</span></span>
* <span data-ttu-id="1e2c0-659">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-660">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-661">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="1e2c0-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-662">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-663">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="1e2c0-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="1e2c0-664">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e2c0-665">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="1e2c0-666">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="1e2c0-667">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="1e2c0-668">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="1e2c0-669">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="1e2c0-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-670">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-671">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="1e2c0-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="1e2c0-672">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="1e2c0-673">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="1e2c0-674">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="1e2c0-675">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e2c0-676">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-676">Highlights since the last major release</span></span>
* <span data-ttu-id="1e2c0-677">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="1e2c0-677">General availability of `Az` module</span></span>
* <span data-ttu-id="1e2c0-678">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1e2c0-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1e2c0-679">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1e2c0-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1e2c0-680">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1e2c0-681">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e2c0-682">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1e2c0-683">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-684">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-685">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1e2c0-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1e2c0-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="1e2c0-687">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="1e2c0-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="1e2c0-688">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="1e2c0-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-689">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-690">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="1e2c0-691">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="1e2c0-692">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-693">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-694">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="1e2c0-695">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="1e2c0-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="1e2c0-697">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="1e2c0-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e2c0-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e2c0-698">Az.DataFactory</span></span>
* <span data-ttu-id="1e2c0-699">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="1e2c0-700">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-701">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-702">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="1e2c0-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="1e2c0-703">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="1e2c0-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="1e2c0-704">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="1e2c0-705">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1e2c0-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="1e2c0-706">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="1e2c0-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="1e2c0-707">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="1e2c0-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-708">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-709">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-710">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-711">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="1e2c0-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="1e2c0-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e2c0-712">New-AzStorageContext</span></span>
* <span data-ttu-id="1e2c0-713">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="1e2c0-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="1e2c0-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1e2c0-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1e2c0-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1e2c0-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="1e2c0-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="1e2c0-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="1e2c0-718">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="1e2c0-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="1e2c0-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1e2c0-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1e2c0-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="1e2c0-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="1e2c0-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1e2c0-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="1e2c0-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="1e2c0-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="1e2c0-723">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="1e2c0-724">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-724">Highlights since the last major release</span></span>
* <span data-ttu-id="1e2c0-725">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="1e2c0-725">General availability of `Az` module</span></span>
* <span data-ttu-id="1e2c0-726">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="1e2c0-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="1e2c0-727">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="1e2c0-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="1e2c0-728">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="1e2c0-729">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e2c0-730">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="1e2c0-731">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-732">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-733">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="1e2c0-734">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="1e2c0-734">Dynamic grouping</span></span>
    * <span data-ttu-id="1e2c0-735">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="1e2c0-735">Pre-Post script</span></span>
    * <span data-ttu-id="1e2c0-736">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-737">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-738">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="1e2c0-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="1e2c0-739">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e2c0-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-740">Az.KeyVault</span></span>
* <span data-ttu-id="1e2c0-741">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-742">Az.Network</span></span>
* <span data-ttu-id="1e2c0-743">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="1e2c0-744">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-746">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="1e2c0-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="1e2c0-747">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="1e2c0-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-748">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-749">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="1e2c0-750">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="1e2c0-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-751">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-752">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-753">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-754">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="1e2c0-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1e2c0-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1e2c0-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="1e2c0-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="1e2c0-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="1e2c0-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="1e2c0-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="1e2c0-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-761">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-762">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="1e2c0-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="1e2c0-763">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-764">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-765">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="1e2c0-766">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-767">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-768">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="1e2c0-769">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="1e2c0-770">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="1e2c0-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e2c0-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e2c0-771">Az.Cdn</span></span>
* <span data-ttu-id="1e2c0-772">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-773">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-774">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="1e2c0-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e2c0-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e2c0-775">Az.DataFactory</span></span>
* <span data-ttu-id="1e2c0-776">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="1e2c0-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e2c0-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-777">Az.LogicApp</span></span>
* <span data-ttu-id="1e2c0-778">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="1e2c0-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-779">Az.Network</span></span>
* <span data-ttu-id="1e2c0-780">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-782">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="1e2c0-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="1e2c0-783">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="1e2c0-783">SDK Update</span></span>
* <span data-ttu-id="1e2c0-784">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1e2c0-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="1e2c0-785">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1e2c0-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-786">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-787">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="1e2c0-788">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="1e2c0-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="1e2c0-789">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="1e2c0-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="1e2c0-790">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="1e2c0-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="1e2c0-791">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="1e2c0-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="1e2c0-792">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="1e2c0-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-793">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-794">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="1e2c0-795">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-796">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-797">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="1e2c0-798">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="1e2c0-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="1e2c0-800">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="1e2c0-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-801">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-802">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="1e2c0-803">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="1e2c0-804">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e2c0-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e2c0-806">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-807">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-808">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="1e2c0-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="1e2c0-809">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="1e2c0-810">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="1e2c0-811">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-813">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="1e2c0-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="1e2c0-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-814">Az.EventHub</span></span>
* <span data-ttu-id="1e2c0-815">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="1e2c0-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-816">Az.KeyVault</span></span>
* <span data-ttu-id="1e2c0-817">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1e2c0-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e2c0-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-818">Az.LogicApp</span></span>
* <span data-ttu-id="1e2c0-819">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="1e2c0-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="1e2c0-820">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="1e2c0-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="1e2c0-821">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="1e2c0-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e2c0-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1e2c0-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e2c0-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1e2c0-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e2c0-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="1e2c0-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="1e2c0-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="1e2c0-826">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="1e2c0-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1e2c0-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1e2c0-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="1e2c0-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="1e2c0-831">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="1e2c0-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="1e2c0-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-832">Az.Monitor</span></span>
* <span data-ttu-id="1e2c0-833">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-834">Az.Network</span></span>
* <span data-ttu-id="1e2c0-835">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1e2c0-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="1e2c0-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="1e2c0-837">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="1e2c0-838">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="1e2c0-839">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="1e2c0-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-840">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-841">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1e2c0-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1e2c0-842">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1e2c0-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="1e2c0-843">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="1e2c0-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="1e2c0-844">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="1e2c0-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-845">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-846">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="1e2c0-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="1e2c0-847">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-848">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-849">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="1e2c0-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="1e2c0-850">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-851">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-852">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e2c0-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1e2c0-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-853">Az.AnalysisServices</span></span>
<span data-ttu-id="1e2c0-854">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-855">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-856">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="1e2c0-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="1e2c0-857">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e2c0-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="1e2c0-858">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-859">Az.RecoveryServices</span></span>
<span data-ttu-id="1e2c0-860">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-861">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-862">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="1e2c0-863">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="1e2c0-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="1e2c0-864">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="1e2c0-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="1e2c0-865">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="1e2c0-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-866">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-867">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="1e2c0-868">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="1e2c0-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="1e2c0-869">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="1e2c0-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="1e2c0-870">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-871">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-872">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="1e2c0-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="1e2c0-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="1e2c0-874">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="1e2c0-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="1e2c0-876">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="1e2c0-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="1e2c0-877">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-878">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-879">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="1e2c0-880">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e2c0-881">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="1e2c0-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="1e2c0-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="1e2c0-882">Az.Aks</span></span>
* <span data-ttu-id="1e2c0-883">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="1e2c0-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-884">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-885">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="1e2c0-886">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="1e2c0-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="1e2c0-887">Az.Cdn</span></span>
* <span data-ttu-id="1e2c0-888">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-889">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-890">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="1e2c0-891">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1e2c0-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="1e2c0-892">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1e2c0-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="1e2c0-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e2c0-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="1e2c0-894">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="1e2c0-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="1e2c0-895">Az.DataFactory</span></span>
* <span data-ttu-id="1e2c0-896">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="1e2c0-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-898">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="1e2c0-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="1e2c0-899">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="1e2c0-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="1e2c0-900">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e2c0-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-901">Az.IotHub</span></span>
* <span data-ttu-id="1e2c0-902">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="1e2c0-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-903">Az.KeyVault</span></span>
* <span data-ttu-id="1e2c0-904">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-905">Az.Network</span></span>
* <span data-ttu-id="1e2c0-906">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-907">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-908">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="1e2c0-909">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="1e2c0-910">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e2c0-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="1e2c0-911">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="1e2c0-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="1e2c0-912">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="1e2c0-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="1e2c0-913">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="1e2c0-914">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="1e2c0-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e2c0-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e2c0-916">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="1e2c0-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="1e2c0-917">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-917">Fix some error messages.</span></span>
* <span data-ttu-id="1e2c0-918">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="1e2c0-919">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1e2c0-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1e2c0-920">Az.SignalR</span></span>
* <span data-ttu-id="1e2c0-921">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-922">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-923">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e2c0-924">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1e2c0-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="1e2c0-925">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="1e2c0-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="1e2c0-926">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="1e2c0-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-927">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-928">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e2c0-929">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="1e2c0-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1e2c0-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="1e2c0-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="1e2c0-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="1e2c0-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1e2c0-932">Az.TrafficManager</span></span>
* <span data-ttu-id="1e2c0-933">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-934">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-935">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="1e2c0-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="1e2c0-936">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="1e2c0-937">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="1e2c0-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="1e2c0-938">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="1e2c0-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="1e2c0-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-939">Az.Accounts</span></span>
* <span data-ttu-id="1e2c0-940">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="1e2c0-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-941">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-942">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="1e2c0-943">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="1e2c0-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="1e2c0-944">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-946">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="1e2c0-947">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="1e2c0-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="1e2c0-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="1e2c0-948">Az.EventGrid</span></span>
* <span data-ttu-id="1e2c0-949">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="1e2c0-950">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="1e2c0-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="1e2c0-951">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1e2c0-952">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="1e2c0-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1e2c0-953">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="1e2c0-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1e2c0-954">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="1e2c0-955">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="1e2c0-956">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="1e2c0-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="1e2c0-957">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="1e2c0-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="1e2c0-958">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="1e2c0-959">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="1e2c0-960">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="1e2c0-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-961">Az.IotHub</span></span>
* <span data-ttu-id="1e2c0-962">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="1e2c0-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="1e2c0-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-963">Az.LogicApp</span></span>
* <span data-ttu-id="1e2c0-964">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="1e2c0-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-965">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-966">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="1e2c0-967">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="1e2c0-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="1e2c0-968">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e2c0-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1e2c0-969">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1e2c0-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="1e2c0-970">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="1e2c0-971">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="1e2c0-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="1e2c0-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="1e2c0-972">Az.SignalR</span></span>
* <span data-ttu-id="1e2c0-973">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-974">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-975">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="1e2c0-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-976">Az.Storage</span></span>
* <span data-ttu-id="1e2c0-977">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="1e2c0-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="1e2c0-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e2c0-978">New-AzStorageContext</span></span>
* <span data-ttu-id="1e2c0-979">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="1e2c0-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="1e2c0-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="1e2c0-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-981">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-982">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e2c0-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="1e2c0-983">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="1e2c0-984">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="1e2c0-985">Généralités</span><span class="sxs-lookup"><span data-stu-id="1e2c0-985">General</span></span>

- <span data-ttu-id="1e2c0-986">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="1e2c0-986">General Availability of Az Module</span></span>
- <span data-ttu-id="1e2c0-987">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="1e2c0-987">Online help for each module</span></span>
- <span data-ttu-id="1e2c0-988">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="1e2c0-989">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="1e2c0-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="1e2c0-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-990">Az.Accounts</span></span>
- <span data-ttu-id="1e2c0-991">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="1e2c0-992">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="1e2c0-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1e2c0-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-993">Az.ApiManagement</span></span>
- <span data-ttu-id="1e2c0-994">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="1e2c0-994">Fixes for #7002</span></span>
- <span data-ttu-id="1e2c0-995">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="1e2c0-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="1e2c0-996">Az.Batch</span></span>
- <span data-ttu-id="1e2c0-997">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="1e2c0-998">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="1e2c0-999">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="1e2c0-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1000">Az.Billing</span></span>
- <span data-ttu-id="1e2c0-1001">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="1e2c0-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="1e2c0-1003">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="1e2c0-1004">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1e2c0-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="1e2c0-1006">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="1e2c0-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="1e2c0-1008">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="1e2c0-1010">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="1e2c0-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1011">Az.Monitor</span></span>
- <span data-ttu-id="1e2c0-1012">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="1e2c0-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1013">Az.KeyVault</span></span>
- <span data-ttu-id="1e2c0-1014">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="1e2c0-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="1e2c0-1016">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="1e2c0-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1017">Az.Media</span></span>
- <span data-ttu-id="1e2c0-1018">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1e2c0-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1019">Az.Network</span></span>
<span data-ttu-id="1e2c0-1020">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="1e2c0-1021">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="1e2c0-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e2c0-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e2c0-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e2c0-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e2c0-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="1e2c0-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="1e2c0-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="1e2c0-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="1e2c0-1030">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="1e2c0-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="1e2c0-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1e2c0-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="1e2c0-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="1e2c0-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="1e2c0-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="1e2c0-1037">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="1e2c0-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1e2c0-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="1e2c0-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="1e2c0-1041">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="1e2c0-1042">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="1e2c0-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="1e2c0-1044">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="1e2c0-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1045">Az.Profile</span></span>
- <span data-ttu-id="1e2c0-1046">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="1e2c0-1048">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="1e2c0-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1049">Az.Resources</span></span>
- <span data-ttu-id="1e2c0-1050">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1e2c0-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="1e2c0-1052">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="1e2c0-1053">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="1e2c0-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="1e2c0-1055">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="1e2c0-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1056">Az.Sql</span></span>
- <span data-ttu-id="1e2c0-1057">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="1e2c0-1058">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="1e2c0-1059">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="1e2c0-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1060">Az.Storage</span></span>
- <span data-ttu-id="1e2c0-1061">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1e2c0-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1062">Az.Websites</span></span>
- <span data-ttu-id="1e2c0-1063">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="1e2c0-1064">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="1e2c0-1065">Généralités</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1065">General</span></span>

* <span data-ttu-id="1e2c0-1066">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="1e2c0-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1067">Az.Compute</span></span>

* <span data-ttu-id="1e2c0-1068">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="1e2c0-1070">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="1e2c0-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="1e2c0-1072">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="1e2c0-1073">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="1e2c0-1074">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="1e2c0-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="1e2c0-1076">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="1e2c0-1077">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="1e2c0-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1078">Az.Resources</span></span>

* <span data-ttu-id="1e2c0-1079">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="1e2c0-1080">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="1e2c0-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1081">Az.Sql</span></span>

* <span data-ttu-id="1e2c0-1082">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="1e2c0-1083">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="1e2c0-1084">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="1e2c0-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1085">Az.Storage</span></span>

* <span data-ttu-id="1e2c0-1086">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="1e2c0-1087">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="1e2c0-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1e2c0-1089">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="1e2c0-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="1e2c0-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="1e2c0-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1092">Az.Websites</span></span>

* <span data-ttu-id="1e2c0-1093">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="1e2c0-1094">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="1e2c0-1095">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="1e2c0-1096">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="1e2c0-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="1e2c0-1098">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="1e2c0-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1099">Az.Automation</span></span>
* <span data-ttu-id="1e2c0-1100">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="1e2c0-1101">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="1e2c0-1102">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="1e2c0-1103">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="1e2c0-1104">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="1e2c0-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1105">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-1106">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="1e2c0-1107">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="1e2c0-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="1e2c0-1109">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="1e2c0-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="1e2c0-1111">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="1e2c0-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1112">Az.Network</span></span>
* <span data-ttu-id="1e2c0-1113">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="1e2c0-1114">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="1e2c0-1115">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="1e2c0-1116">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="1e2c0-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="1e2c0-1118">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="1e2c0-1119">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="1e2c0-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="1e2c0-1121">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="1e2c0-1122">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="1e2c0-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1123">Az.Relay</span></span>
* <span data-ttu-id="1e2c0-1124">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="1e2c0-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1125">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-1126">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="1e2c0-1127">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="1e2c0-1128">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="1e2c0-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e2c0-1130">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="1e2c0-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1131">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-1132">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="1e2c0-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e2c0-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e2c0-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e2c0-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="1e2c0-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1e2c0-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1e2c0-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="1e2c0-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="1e2c0-1141">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="1e2c0-1142">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="1e2c0-1143">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="1e2c0-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1e2c0-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="1e2c0-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="1e2c0-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="1e2c0-1148">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="1e2c0-1149">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="1e2c0-1150">Généralités</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1150">General</span></span>
* <span data-ttu-id="1e2c0-1151">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="1e2c0-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1152">Az.Profile</span></span>
* <span data-ttu-id="1e2c0-1153">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="1e2c0-1154">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="1e2c0-1155">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="1e2c0-1156">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="1e2c0-1157">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="1e2c0-1158">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="1e2c0-1159">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="1e2c0-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e2c0-1161">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1162">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-1163">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="1e2c0-1164">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="1e2c0-1165">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-1167">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="1e2c0-1168">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="1e2c0-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1169">Az.Insights</span></span>
* <span data-ttu-id="1e2c0-1170">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="1e2c0-1171">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="1e2c0-1172">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="1e2c0-1173">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1174">Az.Network</span></span>
* <span data-ttu-id="1e2c0-1175">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="1e2c0-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="1e2c0-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="1e2c0-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="1e2c0-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="1e2c0-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="1e2c0-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="1e2c0-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="1e2c0-1183">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1184">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-1185">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="1e2c0-1186">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="1e2c0-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="1e2c0-1188">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="1e2c0-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="1e2c0-1190">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="1e2c0-1191">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="1e2c0-1192">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="1e2c0-1193">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="1e2c0-1194">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="1e2c0-1195">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="1e2c0-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1196">Az.Profile</span></span>
* <span data-ttu-id="1e2c0-1197">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="1e2c0-1198">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1199">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-1200">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="1e2c0-1201">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="1e2c0-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="1e2c0-1203">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="1e2c0-1204">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="1e2c0-1205">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1e2c0-1206">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="1e2c0-1207">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1208">Az.Network</span></span>
* <span data-ttu-id="1e2c0-1209">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="1e2c0-1210">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1211">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-1212">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="1e2c0-1213">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="1e2c0-1214">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="1e2c0-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1215">Azure.Storage</span></span>
* <span data-ttu-id="1e2c0-1216">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="1e2c0-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="1e2c0-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="1e2c0-1219">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="1e2c0-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="1e2c0-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="1e2c0-1222">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="1e2c0-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1223">Az.Compute</span></span>
* <span data-ttu-id="1e2c0-1224">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="1e2c0-1225">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="1e2c0-1226">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="1e2c0-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="1e2c0-1228">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="1e2c0-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1229">Az.Network</span></span>
* <span data-ttu-id="1e2c0-1230">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="1e2c0-1231">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1231">new cmdlets added</span></span>
    - <span data-ttu-id="1e2c0-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e2c0-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e2c0-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e2c0-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="1e2c0-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="1e2c0-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="1e2c0-1238">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="1e2c0-1239">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="1e2c0-1240">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="1e2c0-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1241">Az.RedisCache</span></span>
* <span data-ttu-id="1e2c0-1242">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="1e2c0-1243">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="1e2c0-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1244">Az.Resources</span></span>
* <span data-ttu-id="1e2c0-1245">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="1e2c0-1246">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="1e2c0-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1247">Az.Sql</span></span>
* <span data-ttu-id="1e2c0-1248">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="1e2c0-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1249">Az.Websites</span></span>
* <span data-ttu-id="1e2c0-1250">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="1e2c0-1251">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="1e2c0-1252">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="1e2c0-1253">Version initiale</span><span class="sxs-lookup"><span data-stu-id="1e2c0-1253">Initial Release</span></span>