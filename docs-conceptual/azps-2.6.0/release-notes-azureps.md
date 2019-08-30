---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052632"
---
## <a name="260---august-2019"></a><span data-ttu-id="35a12-101">2.6.0 - Août 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="35a12-102">Généralités</span><span class="sxs-lookup"><span data-stu-id="35a12-102">General</span></span>
* <span data-ttu-id="35a12-103">Correction des fautes de frappe diverses dans de nombreux modules</span><span class="sxs-lookup"><span data-stu-id="35a12-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35a12-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-104">Az.Accounts</span></span>
* <span data-ttu-id="35a12-105">Prise en charge de l’identité MSI affectée à l’utilisateur dans l’authentification Azure Functions (n° 9479)</span><span class="sxs-lookup"><span data-stu-id="35a12-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="35a12-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="35a12-106">Az.Aks</span></span>
* <span data-ttu-id="35a12-107">Résolution du problème relatif à la sortie de « Get-AzAks »</span><span class="sxs-lookup"><span data-stu-id="35a12-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="35a12-108">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="35a12-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35a12-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35a12-109">Az.ApiManagement</span></span>
* <span data-ttu-id="35a12-110">Corriger le problème https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="35a12-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="35a12-111">Mise à jour de la version de .Net NuGet, qui n’applique pas de restrictions sur productId, apiId, groupId et userId</span><span class="sxs-lookup"><span data-stu-id="35a12-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="35a12-112">**Get-AzApiManagementProduct** : ajout de la prise en charge de l’interrogation de produits à l’aide d’une API.</span><span class="sxs-lookup"><span data-stu-id="35a12-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="35a12-113">**New-AzApiManagementApiRevision** : résolution du problème où ApiRevisionDescription n’était pas défini lors de la création d’une révision d’API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="35a12-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="35a12-114">Correction d’une faute de frappe dans le modèle « PsApiManagementOAuth2AuthrozationServer » remplacé par « PsApiManagementOAuth2AuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="35a12-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35a12-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35a12-115">Az.Batch</span></span>
* <span data-ttu-id="35a12-116">Correction d’une faute de frappe dans un message d’aide et la documentation pour mettre Windows en majuscules</span><span class="sxs-lookup"><span data-stu-id="35a12-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35a12-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35a12-117">Az.Cdn</span></span>
* <span data-ttu-id="35a12-118">Correction d’une faute de frappe dans l’application d’assistance du module CDN</span><span class="sxs-lookup"><span data-stu-id="35a12-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-119">Az.Compute</span></span>
* <span data-ttu-id="35a12-120">Ajout de VmssId à l’applet de commande New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="35a12-121">Ajout des paramètres TerminateScheduledEvents et TerminateScheduledEventNotBeforeTimeoutInMinutes à New-AzVmssConfig et Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35a12-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="35a12-122">Ajout de la propriété HyperVGeneration à l’objet image de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="35a12-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="35a12-123">Ajout des fonctionnalités Host et HostGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="35a12-124">Nouvelles applets de commande :   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="35a12-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="35a12-125">Le paramètre HostId est ajouté à New-AzVMConfig et New-AzVM</span><span class="sxs-lookup"><span data-stu-id="35a12-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="35a12-126">Mise à jour de l’exemple dans la documentation « Invoke-AzVMRunCommand » de manière utiliser le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="35a12-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="35a12-127">Mise à jour de la description « -VolumeType » dans la documentation de référence de « Set-AzVMDiskEncryptionExtension » et de « Set-AzVmssDiskEncryptionExtension »</span><span class="sxs-lookup"><span data-stu-id="35a12-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-128">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-129">Correction de la faute de frappe pour mettre « Windows » en majuscules dans la documentation de « New-AzDataFactoryEncryptValue »</span><span class="sxs-lookup"><span data-stu-id="35a12-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="35a12-130">Mise à jour de la version du SDK .NET ADF vers la version 4.1.2</span><span class="sxs-lookup"><span data-stu-id="35a12-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="35a12-131">Ajout des paramètres « DataProxyIntegrationRuntimeName », « DataProxyStagingLinkedServiceName » et « DataProxyStagingPath » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin de permettre la configuration du runtime d’intégration auto-hébergé comme proxy pour SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="35a12-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="35a12-132">Mise à jour de PSTriggerRun pour afficher les pipelines déclenchés, le message et les propriétés, et de PSActivityRun pour afficher le type d’activité</span><span class="sxs-lookup"><span data-stu-id="35a12-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-134">Correction de la suspension de Get-DataLakeStoreDeletedItem pour toutes les erreurs ou exceptions à distance.</span><span class="sxs-lookup"><span data-stu-id="35a12-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35a12-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35a12-135">Az.EventHub</span></span>
* <span data-ttu-id="35a12-136">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNteworkRule dans Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="35a12-137">Résolution du problème n° 9558 : Set-AzEventHubNamespace utilise PATCH au lieu de PUT</span><span class="sxs-lookup"><span data-stu-id="35a12-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="35a12-138">Ajout du paramètre EnableKafka à l’applet de commande Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="35a12-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="35a12-139">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="35a12-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="35a12-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="35a12-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="35a12-141">Résolution de la faute de frappe où « Azure » était tout en minuscules dans la documentation</span><span class="sxs-lookup"><span data-stu-id="35a12-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35a12-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35a12-142">Az.Monitor</span></span>
* <span data-ttu-id="35a12-143">Correction du nom de paramètre incorrect dans la documentation</span><span class="sxs-lookup"><span data-stu-id="35a12-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-144">Az.Network</span></span>
* <span data-ttu-id="35a12-145">Mise à jour dans New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="35a12-146">Dépréciation du paramètre « PublicIpAddress », car il n’est jamais utilisé côté serveur.</span><span class="sxs-lookup"><span data-stu-id="35a12-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="35a12-147">Ajout d’un paramètre facultatif « Primary » qui indique si la configuration IP actuelle est primaire ou non.</span><span class="sxs-lookup"><span data-stu-id="35a12-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="35a12-148">Amélioration de la gestion de l’exception d’erreur de demande à partir du SDK : résolution du problème où les exceptions du SDK n’étaient précédemment pas gérées correctement, ce qui empêchait l’affichage des détails des erreurs de clé</span><span class="sxs-lookup"><span data-stu-id="35a12-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="35a12-149">Ajustement de la logique de validation pour le préfixe IP IPv6 afin de rechercher la longueur de préfixe IPv6 appropriée.</span><span class="sxs-lookup"><span data-stu-id="35a12-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="35a12-150">Mise à jour de Get-AzVirtualNetworkSubnetConfig : Ajout d’un paramètre défini pour obtenir l’ID de ressource de sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="35a12-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="35a12-151">Mise à jour de la description du paramètre Location pour AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="35a12-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="35a12-153">Mise à jour de la documentation pour « New-AzOperationalInsightsLinuxSyslogDataSource »</span><span class="sxs-lookup"><span data-stu-id="35a12-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="35a12-154">Ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="35a12-154">Added example</span></span>
    - <span data-ttu-id="35a12-155">Mise à jour de la description du paramètre « -Name »</span><span class="sxs-lookup"><span data-stu-id="35a12-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="35a12-156">Ajout d’un exemple pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="35a12-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="35a12-157">Changement de la description du paramètre -Name pour New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="35a12-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-159">Mise à jour de « Get-AzRecoveryServicesBackupJobDetail.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-160">Az.Resources</span></span>
* <span data-ttu-id="35a12-161">Ajout de la prise en charge de la nouvelle API version 2019-05-10 pour Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="35a12-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="35a12-162">Ajout de la prise en charge de « copy.count = 0 » pour les variables, les ressources et les propriétés</span><span class="sxs-lookup"><span data-stu-id="35a12-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="35a12-163">Les ressources avec « condition = false » ou « copy.count = 0 » seront supprimées en mode Complet</span><span class="sxs-lookup"><span data-stu-id="35a12-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="35a12-164">Ajout d’un exemple d’affectation de stratégie au niveau de l’abonnement à la documentation d’aide</span><span class="sxs-lookup"><span data-stu-id="35a12-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35a12-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35a12-165">Az.ServiceBus</span></span>
* <span data-ttu-id="35a12-166">Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNetworkRule dans Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="35a12-167">Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement</span><span class="sxs-lookup"><span data-stu-id="35a12-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="35a12-168">Ajout de la nouvelle commande « Test-AzServiceBusNameAvailability » afin de vérifier la disponibilité du nom pour la file d’attente et la rubrique</span><span class="sxs-lookup"><span data-stu-id="35a12-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="35a12-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="35a12-170">Correction des bogues relatifs à l’applet de commande add node type :</span><span class="sxs-lookup"><span data-stu-id="35a12-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="35a12-171">bogue NullReferenceException quand un groupe de ressources avait d’autres groupes de machines virtuelles identiques non liés au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="35a12-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="35a12-172">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="35a12-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="35a12-173">Correction du bogue où l’applet de commande échouait si virtualNetwork se trouvait dans un groupe de ressources différent de celui du cluster.</span><span class="sxs-lookup"><span data-stu-id="35a12-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="35a12-174">Résolution du problème : https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="35a12-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="35a12-175">Dépréciation de l’applet de commande Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="35a12-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-176">Az.Sql</span></span>
* <span data-ttu-id="35a12-177">Mise à jour de la documentation des anciennes applets de commande d’audit.</span><span class="sxs-lookup"><span data-stu-id="35a12-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-178">Az.Storage</span></span>
* <span data-ttu-id="35a12-179">Mise à jour de l’aide pour Get/Close-AzStorageFileHandle, en ajoutant d’autres scénarios aux exemples d’applets de commande et mise à jour des descriptions des paramètres</span><span class="sxs-lookup"><span data-stu-id="35a12-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="35a12-180">Prise en charge de StandardBlobTier dans le chargement d’objet blob et la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="35a12-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="35a12-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35a12-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="35a12-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="35a12-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="35a12-183">Prise en charge de la priorité de réalimentation dans la copie d’objet blob</span><span class="sxs-lookup"><span data-stu-id="35a12-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="35a12-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="35a12-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-185">Az.Websites</span></span>
* <span data-ttu-id="35a12-186">Ajout d’une clarification concernant le paramètre -AppSettings dans Set-AzWebApp et Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="35a12-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="35a12-187">2.5.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-188">Az.Accounts</span></span>
* <span data-ttu-id="35a12-189">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="35a12-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="35a12-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="35a12-191">Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey »</span><span class="sxs-lookup"><span data-stu-id="35a12-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="35a12-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-192">Az.Automation</span></span>
* <span data-ttu-id="35a12-193">Correction d’une faute de frappe dans la chaîne de ressource</span><span class="sxs-lookup"><span data-stu-id="35a12-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="35a12-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35a12-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="35a12-195">Prise en charge de NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="35a12-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-196">Az.Compute</span></span>
* <span data-ttu-id="35a12-197">Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="35a12-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35a12-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="35a12-199">Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication</span><span class="sxs-lookup"><span data-stu-id="35a12-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="35a12-200">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="35a12-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-201">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-202">Mise à jour du SDK .NET ADF avec la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="35a12-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="35a12-203">Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »</span><span class="sxs-lookup"><span data-stu-id="35a12-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35a12-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35a12-204">Az.EventHub</span></span>
* <span data-ttu-id="35a12-205">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="35a12-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="35a12-206">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="35a12-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35a12-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-207">Az.KeyVault</span></span>
* <span data-ttu-id="35a12-208">Possibilité de spécifier KeySize pour les stratégies de certificat</span><span class="sxs-lookup"><span data-stu-id="35a12-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35a12-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35a12-209">Az.LogicApp</span></span>
* <span data-ttu-id="35a12-210">Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes</span><span class="sxs-lookup"><span data-stu-id="35a12-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="35a12-211">Ajout d’un nouveau paramètre MapType pour le filtrage</span><span class="sxs-lookup"><span data-stu-id="35a12-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="35a12-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="35a12-212">Az.ManagedServices</span></span>
* <span data-ttu-id="35a12-213">Ajout de la prise en charge de l’API version 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="35a12-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-214">Az.Network</span></span>
* <span data-ttu-id="35a12-215">Prise en charge d’un point de terminaison privé et du service de liaison privée</span><span class="sxs-lookup"><span data-stu-id="35a12-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="35a12-216">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-216">New cmdlets</span></span>
        - <span data-ttu-id="35a12-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35a12-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35a12-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35a12-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35a12-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35a12-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35a12-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35a12-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="35a12-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="35a12-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="35a12-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35a12-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="35a12-225">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="35a12-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="35a12-226">Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="35a12-227">Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag pour activer ou désactiver l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="35a12-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="35a12-228">Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag pour activer ou désactiver l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="35a12-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="35a12-229">Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante</span><span class="sxs-lookup"><span data-stu-id="35a12-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="35a12-230">Activation du protocole ICMP pour les configurations des règles de sécurité réseau</span><span class="sxs-lookup"><span data-stu-id="35a12-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="35a12-231">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="35a12-231">Updated cmdlets</span></span>
        - <span data-ttu-id="35a12-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="35a12-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="35a12-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="35a12-235">Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="35a12-236">Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="35a12-237">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="35a12-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="35a12-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="35a12-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="35a12-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="35a12-241">Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde</span><span class="sxs-lookup"><span data-stu-id="35a12-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="35a12-242">Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end.</span><span class="sxs-lookup"><span data-stu-id="35a12-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="35a12-243">Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="35a12-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="35a12-245">Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="35a12-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="35a12-246">Correction de la gestion des expressions régulières null des journaux personnalisés</span><span class="sxs-lookup"><span data-stu-id="35a12-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-248">Mise à jour de « Get-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="35a12-249">Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="35a12-250">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="35a12-251">Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="35a12-252">Mise à jour de « Set-AzRecoveryServicesVaultContext.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="35a12-253">Mise à jour de « Get-AzRecoveryServicesVault.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="35a12-254">Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="35a12-255">Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="35a12-256">Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure</span><span class="sxs-lookup"><span data-stu-id="35a12-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="35a12-257">Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »</span><span class="sxs-lookup"><span data-stu-id="35a12-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-258">Az.Resources</span></span>
- <span data-ttu-id="35a12-259">Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="35a12-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="35a12-260">Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="35a12-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35a12-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35a12-261">Az.ServiceBus</span></span>
* <span data-ttu-id="35a12-262">Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="35a12-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="35a12-263">Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté</span><span class="sxs-lookup"><span data-stu-id="35a12-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-264">Az.Sql</span></span>
* <span data-ttu-id="35a12-265">Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="35a12-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="35a12-266">Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="35a12-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="35a12-267">Correction d’une faute de frappe dans un message d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="35a12-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-268">Az.Storage</span></span>
* <span data-ttu-id="35a12-269">Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié</span><span class="sxs-lookup"><span data-stu-id="35a12-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="35a12-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="35a12-270">Az.StorageSync</span></span>
* <span data-ttu-id="35a12-271">Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="35a12-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="35a12-272">Résolution du problème 9551 pour honorer TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="35a12-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-273">Az.Websites</span></span>
* <span data-ttu-id="35a12-274">Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="35a12-275">Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="35a12-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="35a12-276">Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="35a12-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="35a12-277">2.4.0 - Juillet 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-278">Az.Accounts</span></span>
* <span data-ttu-id="35a12-279">Ajout de la prise en charge des applets de commande de profil</span><span class="sxs-lookup"><span data-stu-id="35a12-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="35a12-280">Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées</span><span class="sxs-lookup"><span data-stu-id="35a12-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="35a12-281">Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="35a12-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="35a12-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="35a12-282">Az.Advisor</span></span>
* <span data-ttu-id="35a12-283">Mise à la disposition générale de Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="35a12-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="35a12-284">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="35a12-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="35a12-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35a12-285">Az.ApiManagement</span></span>
* <span data-ttu-id="35a12-286">Corriger le problème https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="35a12-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="35a12-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="35a12-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="35a12-288">Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit</span><span class="sxs-lookup"><span data-stu-id="35a12-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="35a12-289">Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »</span><span class="sxs-lookup"><span data-stu-id="35a12-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="35a12-290">Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="35a12-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="35a12-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="35a12-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="35a12-292">Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API</span><span class="sxs-lookup"><span data-stu-id="35a12-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-293">Az.Automation</span></span>
* <span data-ttu-id="35a12-294">Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.</span><span class="sxs-lookup"><span data-stu-id="35a12-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-295">Az.Compute</span></span>
* <span data-ttu-id="35a12-296">Ajout du paramètre HyperVGeneration à New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-297">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-298">Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.</span><span class="sxs-lookup"><span data-stu-id="35a12-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35a12-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35a12-299">Az.EventGrid</span></span>
* <span data-ttu-id="35a12-300">Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »</span><span class="sxs-lookup"><span data-stu-id="35a12-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35a12-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35a12-301">Az.IotHub</span></span>
* <span data-ttu-id="35a12-302">Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="35a12-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-303">Az.Network</span></span>
* <span data-ttu-id="35a12-304">Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques</span><span class="sxs-lookup"><span data-stu-id="35a12-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="35a12-305">Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »</span><span class="sxs-lookup"><span data-stu-id="35a12-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35a12-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="35a12-307">Correction d’un problème de référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="35a12-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="35a12-308">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="35a12-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="35a12-310">Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="35a12-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-312">Correction de la commande get-policy pour IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="35a12-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-313">Az.Resources</span></span>
    - <span data-ttu-id="35a12-314">Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="35a12-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="35a12-315">Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="35a12-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="35a12-316">Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="35a12-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="35a12-317">Mise à jour des documents et des exemples pour les applets de commande de stratégie</span><span class="sxs-lookup"><span data-stu-id="35a12-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35a12-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35a12-318">Az.ServiceBus</span></span>
* <span data-ttu-id="35a12-319">Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="35a12-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-320">Az.Sql</span></span>
* <span data-ttu-id="35a12-321">Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique</span><span class="sxs-lookup"><span data-stu-id="35a12-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="35a12-322">Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.</span><span class="sxs-lookup"><span data-stu-id="35a12-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="35a12-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="35a12-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="35a12-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="35a12-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="35a12-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="35a12-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="35a12-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="35a12-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="35a12-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="35a12-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="35a12-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="35a12-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="35a12-329">Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="35a12-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-330">Az.Storage</span></span>
* <span data-ttu-id="35a12-331">Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="35a12-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="35a12-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="35a12-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="35a12-333">Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple</span><span class="sxs-lookup"><span data-stu-id="35a12-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="35a12-334">Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException</span><span class="sxs-lookup"><span data-stu-id="35a12-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="35a12-335">Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files</span><span class="sxs-lookup"><span data-stu-id="35a12-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="35a12-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="35a12-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="35a12-338">Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier</span><span class="sxs-lookup"><span data-stu-id="35a12-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="35a12-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35a12-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="35a12-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="35a12-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="35a12-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="35a12-341">Az.StorageSync</span></span>
* <span data-ttu-id="35a12-342">Ce module est désormais inclus dans le cadre du module `Az` de cumul</span><span class="sxs-lookup"><span data-stu-id="35a12-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="35a12-343">2.3.2 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-344">Az.Accounts</span></span>
* <span data-ttu-id="35a12-345">Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions</span><span class="sxs-lookup"><span data-stu-id="35a12-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="35a12-346">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="35a12-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="35a12-347">Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az</span><span class="sxs-lookup"><span data-stu-id="35a12-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="35a12-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="35a12-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="35a12-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="35a12-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-350">Az.Compute</span></span>
* <span data-ttu-id="35a12-351">Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».</span><span class="sxs-lookup"><span data-stu-id="35a12-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="35a12-352">Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »</span><span class="sxs-lookup"><span data-stu-id="35a12-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="35a12-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="35a12-353">Az.Dns</span></span>
* <span data-ttu-id="35a12-354">Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».</span><span class="sxs-lookup"><span data-stu-id="35a12-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35a12-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35a12-355">Az.EventGrid</span></span>
* <span data-ttu-id="35a12-356">Mis à jour effectuée pour utiliser la version d’API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="35a12-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="35a12-357">Nouvelles applets de commande :</span><span class="sxs-lookup"><span data-stu-id="35a12-357">New cmdlets:</span></span>
    - <span data-ttu-id="35a12-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="35a12-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="35a12-359">Crée un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="35a12-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="35a12-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="35a12-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="35a12-361">Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="35a12-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="35a12-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="35a12-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="35a12-363">Supprime un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="35a12-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="35a12-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="35a12-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="35a12-365">Regénère la clé d’accès partagé pour un domaine Azure Event Grid.</span><span class="sxs-lookup"><span data-stu-id="35a12-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="35a12-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="35a12-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="35a12-367">Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="35a12-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="35a12-368">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="35a12-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="35a12-369">Crée une rubrique de domaine Event Grid.</span><span class="sxs-lookup"><span data-stu-id="35a12-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="35a12-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="35a12-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="35a12-371">Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel.</span><span class="sxs-lookup"><span data-stu-id="35a12-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="35a12-372">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="35a12-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="35a12-373">Supprime une rubrique de domaine Azure Event Grid existante.</span><span class="sxs-lookup"><span data-stu-id="35a12-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="35a12-374">Cmdlets mises à jour :</span><span class="sxs-lookup"><span data-stu-id="35a12-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="35a12-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="35a12-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="35a12-376">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="35a12-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="35a12-377">Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="35a12-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="35a12-378">Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).</span><span class="sxs-lookup"><span data-stu-id="35a12-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="35a12-379">Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="35a12-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="35a12-380">Date d’expiration de l’abonnement aux événements</span><span class="sxs-lookup"><span data-stu-id="35a12-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="35a12-381">Paramètres de filtrage avancé</span><span class="sxs-lookup"><span data-stu-id="35a12-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="35a12-382">Ajout d’un nouvel enum pour servicebusqueue comme destination.</span><span class="sxs-lookup"><span data-stu-id="35a12-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="35a12-383">Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par</span><span class="sxs-lookup"><span data-stu-id="35a12-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="35a12-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :</span><span class="sxs-lookup"><span data-stu-id="35a12-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="35a12-385">Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.</span><span class="sxs-lookup"><span data-stu-id="35a12-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="35a12-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="35a12-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="35a12-387">Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="35a12-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="35a12-388">Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.</span><span class="sxs-lookup"><span data-stu-id="35a12-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35a12-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35a12-389">Az.FrontDoor</span></span>
* <span data-ttu-id="35a12-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="35a12-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="35a12-391">Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)</span><span class="sxs-lookup"><span data-stu-id="35a12-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="35a12-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="35a12-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="35a12-393">Ajout de nouvelles valeurs de saisie semi-automatique</span><span class="sxs-lookup"><span data-stu-id="35a12-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-394">Az.Network</span></span>
* <span data-ttu-id="35a12-395">Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="35a12-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="35a12-396">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-396">New cmdlets</span></span>
        - <span data-ttu-id="35a12-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="35a12-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="35a12-398">Ajout d’AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="35a12-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="35a12-399">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-399">New cmdlets</span></span> 
        - <span data-ttu-id="35a12-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="35a12-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="35a12-401">Ajout de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35a12-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="35a12-402">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-402">New cmdlets</span></span> 
        - <span data-ttu-id="35a12-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35a12-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="35a12-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35a12-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35a12-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="35a12-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="35a12-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="35a12-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="35a12-408">Ajout de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35a12-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="35a12-409">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-409">New cmdlets</span></span>
        - <span data-ttu-id="35a12-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35a12-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35a12-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35a12-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35a12-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="35a12-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="35a12-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="35a12-414">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection</span><span class="sxs-lookup"><span data-stu-id="35a12-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="35a12-415">Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="35a12-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="35a12-416">Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="35a12-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="35a12-417">Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="35a12-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="35a12-418">Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="35a12-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="35a12-419">Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="35a12-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="35a12-420">Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="35a12-421">Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.</span><span class="sxs-lookup"><span data-stu-id="35a12-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="35a12-422">Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="35a12-423">Correction des applets de commande Cortex Get pour lister toutes les parties</span><span class="sxs-lookup"><span data-stu-id="35a12-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="35a12-424">Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="35a12-425">Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="35a12-426">Ajout de l’applet de commande Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="35a12-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="35a12-427">Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="35a12-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="35a12-428">Mise à jour de l’applet de commande New-AzFirewall :</span><span class="sxs-lookup"><span data-stu-id="35a12-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="35a12-429">Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique</span><span class="sxs-lookup"><span data-stu-id="35a12-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="35a12-430">Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="35a12-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="35a12-431">Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)</span><span class="sxs-lookup"><span data-stu-id="35a12-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="35a12-432">Dépréciation des paramètres -PublicIpName et -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="35a12-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="35a12-433">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="35a12-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="35a12-434">Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="35a12-435">Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="35a12-436">Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="35a12-438">Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »</span><span class="sxs-lookup"><span data-stu-id="35a12-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-439">Az.Resources</span></span>
* <span data-ttu-id="35a12-440">Prise en charge d’autres options d’exportation de modèle</span><span class="sxs-lookup"><span data-stu-id="35a12-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="35a12-441">Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="35a12-442">Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="35a12-443">Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées</span><span class="sxs-lookup"><span data-stu-id="35a12-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35a12-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="35a12-445">Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-446">Az.Sql</span></span>
* <span data-ttu-id="35a12-447">Correction du suffixe du point de terminaison de stockage Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="35a12-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="35a12-448">Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="35a12-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="35a12-449">Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées</span><span class="sxs-lookup"><span data-stu-id="35a12-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="35a12-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="35a12-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="35a12-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="35a12-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="35a12-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="35a12-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="35a12-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="35a12-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="35a12-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="35a12-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-455">Az.Storage</span></span>
* <span data-ttu-id="35a12-456">Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="35a12-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="35a12-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="35a12-458">Clarification de la description de l’applet de commande d’immuabilité des objets blob</span><span class="sxs-lookup"><span data-stu-id="35a12-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="35a12-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-460">Az.Websites</span></span>
* <span data-ttu-id="35a12-461">Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client</span><span class="sxs-lookup"><span data-stu-id="35a12-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="35a12-462">Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="35a12-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="35a12-463">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="35a12-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35a12-464">Az.Cdn</span></span>
* <span data-ttu-id="35a12-465">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="35a12-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-466">Az.Compute</span></span>
* <span data-ttu-id="35a12-467">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="35a12-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="35a12-468">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="35a12-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35a12-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35a12-469">Az.EventHub</span></span>
* <span data-ttu-id="35a12-470">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="35a12-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="35a12-471">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a12-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-472">Az.Network</span></span>
* <span data-ttu-id="35a12-473">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="35a12-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="35a12-474">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="35a12-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35a12-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="35a12-476">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="35a12-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-478">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="35a12-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35a12-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35a12-479">Az.ServiceBus</span></span>
* <span data-ttu-id="35a12-480">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a12-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35a12-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="35a12-482">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="35a12-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="35a12-483">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="35a12-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-484">Az.Sql</span></span>
* <span data-ttu-id="35a12-485">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="35a12-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="35a12-486">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="35a12-487">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="35a12-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="35a12-488">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="35a12-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-489">Az.Websites</span></span>
* <span data-ttu-id="35a12-490">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="35a12-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="35a12-491">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="35a12-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35a12-492">Az.ApiManagement</span></span>
* <span data-ttu-id="35a12-493">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="35a12-494">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="35a12-495">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="35a12-496">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="35a12-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="35a12-497">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="35a12-498">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="35a12-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="35a12-499">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="35a12-500">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="35a12-501">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="35a12-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="35a12-502">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="35a12-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="35a12-503">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="35a12-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="35a12-504">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="35a12-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="35a12-505">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="35a12-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="35a12-506">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="35a12-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="35a12-507">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="35a12-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="35a12-508">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="35a12-509">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="35a12-510">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="35a12-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="35a12-511">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="35a12-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="35a12-512">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="35a12-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="35a12-513">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="35a12-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="35a12-514">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="35a12-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="35a12-515">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="35a12-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="35a12-516">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="35a12-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="35a12-517">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="35a12-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="35a12-518">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="35a12-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="35a12-519">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="35a12-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="35a12-520">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="35a12-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="35a12-521">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="35a12-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="35a12-522">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="35a12-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="35a12-523">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="35a12-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="35a12-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="35a12-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="35a12-525">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="35a12-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="35a12-526">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="35a12-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="35a12-527">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="35a12-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="35a12-528">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="35a12-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="35a12-529">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="35a12-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="35a12-530">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="35a12-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="35a12-531">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="35a12-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="35a12-532">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="35a12-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="35a12-533">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="35a12-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="35a12-534">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="35a12-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="35a12-535">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="35a12-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="35a12-536">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="35a12-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="35a12-537">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="35a12-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="35a12-538">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="35a12-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="35a12-539">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="35a12-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="35a12-540">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="35a12-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="35a12-541">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="35a12-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="35a12-542">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="35a12-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="35a12-543">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="35a12-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="35a12-544">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="35a12-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="35a12-545">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="35a12-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="35a12-546">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="35a12-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="35a12-547">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="35a12-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="35a12-548">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="35a12-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="35a12-549">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="35a12-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="35a12-550">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="35a12-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="35a12-551">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="35a12-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="35a12-552">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="35a12-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="35a12-553">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="35a12-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="35a12-554">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="35a12-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="35a12-555">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="35a12-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="35a12-556">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="35a12-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="35a12-557">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="35a12-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="35a12-558">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="35a12-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="35a12-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="35a12-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="35a12-560">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="35a12-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="35a12-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="35a12-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="35a12-562">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="35a12-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="35a12-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="35a12-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="35a12-564">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="35a12-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="35a12-565">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="35a12-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="35a12-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="35a12-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="35a12-567">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="35a12-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="35a12-568">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="35a12-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="35a12-569">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="35a12-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-570">Az.Automation</span></span>
* <span data-ttu-id="35a12-571">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="35a12-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="35a12-572">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="35a12-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="35a12-573">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="35a12-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="35a12-574">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="35a12-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="35a12-575">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="35a12-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="35a12-576">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="35a12-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="35a12-577">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="35a12-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-578">Az.Compute</span></span>
* <span data-ttu-id="35a12-579">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="35a12-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="35a12-580">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="35a12-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-582">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="35a12-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35a12-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35a12-583">Az.Monitor</span></span>
* <span data-ttu-id="35a12-584">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="35a12-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-585">Az.Network</span></span>
* <span data-ttu-id="35a12-586">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="35a12-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="35a12-587">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="35a12-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="35a12-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="35a12-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="35a12-589">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="35a12-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-590">Az.Resources</span></span>
* <span data-ttu-id="35a12-591">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="35a12-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-592">Az.Sql</span></span>
* <span data-ttu-id="35a12-593">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="35a12-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="35a12-594">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-595">Az.Accounts</span></span>
* <span data-ttu-id="35a12-596">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="35a12-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35a12-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35a12-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="35a12-598">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="35a12-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="35a12-599">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="35a12-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-600">Az.Compute</span></span>
* <span data-ttu-id="35a12-601">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="35a12-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="35a12-602">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="35a12-603">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="35a12-604">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="35a12-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="35a12-605">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="35a12-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="35a12-606">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35a12-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="35a12-607">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="35a12-607">Breaking changes</span></span>
    - <span data-ttu-id="35a12-608">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="35a12-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="35a12-609">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="35a12-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="35a12-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="35a12-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="35a12-611">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="35a12-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="35a12-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="35a12-612">Az.Dns</span></span>
* <span data-ttu-id="35a12-613">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="35a12-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="35a12-614">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="35a12-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="35a12-615">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="35a12-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="35a12-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35a12-616">Az.FrontDoor</span></span>
* <span data-ttu-id="35a12-617">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35a12-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="35a12-618">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="35a12-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="35a12-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35a12-619">Az.HDInsight</span></span>
* <span data-ttu-id="35a12-620">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="35a12-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="35a12-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35a12-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="35a12-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35a12-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="35a12-623">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="35a12-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="35a12-624">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="35a12-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="35a12-625">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="35a12-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="35a12-626">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="35a12-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35a12-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35a12-627">Az.Monitor</span></span>
* <span data-ttu-id="35a12-628">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="35a12-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="35a12-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="35a12-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="35a12-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="35a12-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="35a12-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="35a12-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="35a12-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="35a12-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="35a12-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="35a12-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="35a12-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="35a12-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35a12-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35a12-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35a12-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35a12-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35a12-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35a12-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35a12-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35a12-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="35a12-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="35a12-640">[Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="35a12-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="35a12-641">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="35a12-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-642">Az.Network</span></span>
* <span data-ttu-id="35a12-643">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="35a12-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="35a12-644">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-644">New cmdlets</span></span>
        - <span data-ttu-id="35a12-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="35a12-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="35a12-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="35a12-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="35a12-649">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="35a12-649">Updated cmdlets</span></span>
        - <span data-ttu-id="35a12-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="35a12-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="35a12-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="35a12-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="35a12-652">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="35a12-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="35a12-653">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="35a12-654">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="35a12-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35a12-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="35a12-656">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="35a12-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="35a12-657">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="35a12-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="35a12-658">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="35a12-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-660">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="35a12-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="35a12-661">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="35a12-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="35a12-662">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="35a12-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="35a12-663">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="35a12-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="35a12-664">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="35a12-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="35a12-665">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="35a12-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="35a12-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="35a12-666">Az.Relay</span></span>
* <span data-ttu-id="35a12-667">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="35a12-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35a12-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35a12-668">Az.ServiceBus</span></span>
* <span data-ttu-id="35a12-669">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="35a12-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-670">Az.Storage</span></span>
* <span data-ttu-id="35a12-671">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="35a12-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="35a12-672">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="35a12-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="35a12-673">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="35a12-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="35a12-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="35a12-675">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="35a12-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="35a12-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="35a12-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="35a12-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-679">Az.Websites</span></span>
* <span data-ttu-id="35a12-680">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="35a12-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="35a12-681">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="35a12-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="35a12-682">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35a12-683">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="35a12-683">Highlights since the last major release</span></span>
* <span data-ttu-id="35a12-684">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="35a12-684">General availability of `Az` module</span></span>
* <span data-ttu-id="35a12-685">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="35a12-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="35a12-686">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="35a12-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="35a12-687">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="35a12-688">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="35a12-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35a12-689">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="35a12-690">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="35a12-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35a12-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-691">Az.Accounts</span></span>
* <span data-ttu-id="35a12-692">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="35a12-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="35a12-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35a12-693">Az.Batch</span></span>
* <span data-ttu-id="35a12-694">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35a12-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35a12-695">Az.Cdn</span></span>
* <span data-ttu-id="35a12-696">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35a12-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35a12-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="35a12-698">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-699">Az.Compute</span></span>
* <span data-ttu-id="35a12-700">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="35a12-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="35a12-701">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35a12-702">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="35a12-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-703">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-704">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="35a12-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-706">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35a12-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35a12-707">Az.EventGrid</span></span>
* <span data-ttu-id="35a12-708">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="35a12-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35a12-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35a12-709">Az.EventHub</span></span>
* <span data-ttu-id="35a12-710">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="35a12-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="35a12-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="35a12-711">Az.HDInsight</span></span>
* <span data-ttu-id="35a12-712">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35a12-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35a12-713">Az.IotHub</span></span>
* <span data-ttu-id="35a12-714">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35a12-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-715">Az.KeyVault</span></span>
* <span data-ttu-id="35a12-716">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35a12-717">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="35a12-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="35a12-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="35a12-718">Az.MachineLearning</span></span>
* <span data-ttu-id="35a12-719">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="35a12-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="35a12-720">Az.Media</span></span>
* <span data-ttu-id="35a12-721">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35a12-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35a12-722">Az.Monitor</span></span>
  * <span data-ttu-id="35a12-723">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="35a12-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="35a12-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="35a12-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="35a12-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="35a12-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="35a12-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="35a12-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="35a12-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="35a12-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="35a12-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="35a12-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="35a12-729">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="35a12-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-730">Az.Network</span></span>
* <span data-ttu-id="35a12-731">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35a12-732">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="35a12-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="35a12-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="35a12-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="35a12-734">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="35a12-736">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="35a12-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="35a12-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="35a12-738">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-740">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35a12-741">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="35a12-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="35a12-742">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="35a12-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="35a12-743">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="35a12-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="35a12-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="35a12-744">Az.RedisCache</span></span>
* <span data-ttu-id="35a12-745">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-746">Az.Resources</span></span>
* <span data-ttu-id="35a12-747">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="35a12-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-748">Az.Sql</span></span>
* <span data-ttu-id="35a12-749">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="35a12-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="35a12-750">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35a12-751">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="35a12-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="35a12-752">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="35a12-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="35a12-753">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="35a12-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="35a12-754">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="35a12-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="35a12-755">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="35a12-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-756">Az.Websites</span></span>
* <span data-ttu-id="35a12-757">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="35a12-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="35a12-758">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="35a12-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="35a12-759">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="35a12-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="35a12-760">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="35a12-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="35a12-761">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35a12-762">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="35a12-762">Highlights since the last major release</span></span>
* <span data-ttu-id="35a12-763">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="35a12-763">General availability of `Az` module</span></span>
* <span data-ttu-id="35a12-764">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="35a12-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="35a12-765">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="35a12-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="35a12-766">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="35a12-767">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="35a12-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35a12-768">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="35a12-769">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="35a12-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="35a12-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-770">Az.Accounts</span></span>
* <span data-ttu-id="35a12-771">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="35a12-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="35a12-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35a12-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="35a12-773">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="35a12-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="35a12-774">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="35a12-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-775">Az.Automation</span></span>
* <span data-ttu-id="35a12-776">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="35a12-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="35a12-777">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="35a12-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="35a12-778">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="35a12-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-779">Az.Compute</span></span>
* <span data-ttu-id="35a12-780">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="35a12-781">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="35a12-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="35a12-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="35a12-783">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="35a12-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-784">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-785">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="35a12-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="35a12-786">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="35a12-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-787">Az.Resources</span></span>
* <span data-ttu-id="35a12-788">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="35a12-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="35a12-789">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="35a12-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="35a12-790">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="35a12-791">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="35a12-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="35a12-792">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="35a12-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="35a12-793">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="35a12-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-794">Az.Sql</span></span>
* <span data-ttu-id="35a12-795">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="35a12-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-796">Az.Storage</span></span>
* <span data-ttu-id="35a12-797">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="35a12-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="35a12-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="35a12-798">New-AzStorageContext</span></span>
* <span data-ttu-id="35a12-799">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="35a12-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="35a12-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="35a12-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="35a12-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="35a12-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="35a12-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="35a12-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="35a12-804">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="35a12-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="35a12-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35a12-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="35a12-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="35a12-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="35a12-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="35a12-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="35a12-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="35a12-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="35a12-809">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="35a12-810">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="35a12-810">Highlights since the last major release</span></span>
* <span data-ttu-id="35a12-811">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="35a12-811">General availability of `Az` module</span></span>
* <span data-ttu-id="35a12-812">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="35a12-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="35a12-813">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="35a12-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="35a12-814">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="35a12-815">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="35a12-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35a12-816">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="35a12-817">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="35a12-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-818">Az.Automation</span></span>
* <span data-ttu-id="35a12-819">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="35a12-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="35a12-820">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="35a12-820">Dynamic grouping</span></span>
    * <span data-ttu-id="35a12-821">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="35a12-821">Pre-Post script</span></span>
    * <span data-ttu-id="35a12-822">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="35a12-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-823">Az.Compute</span></span>
* <span data-ttu-id="35a12-824">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="35a12-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="35a12-825">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="35a12-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35a12-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-826">Az.KeyVault</span></span>
* <span data-ttu-id="35a12-827">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-828">Az.Network</span></span>
* <span data-ttu-id="35a12-829">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="35a12-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="35a12-830">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="35a12-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-832">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="35a12-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="35a12-833">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="35a12-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-834">Az.Resources</span></span>
* <span data-ttu-id="35a12-835">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="35a12-836">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="35a12-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-837">Az.Sql</span></span>
* <span data-ttu-id="35a12-838">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="35a12-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-839">Az.Storage</span></span>
* <span data-ttu-id="35a12-840">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="35a12-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="35a12-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="35a12-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="35a12-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="35a12-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="35a12-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="35a12-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="35a12-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="35a12-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="35a12-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-847">Az.Websites</span></span>
* <span data-ttu-id="35a12-848">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="35a12-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="35a12-849">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-850">Az.Accounts</span></span>
* <span data-ttu-id="35a12-851">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="35a12-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="35a12-852">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-853">Az.Automation</span></span>
* <span data-ttu-id="35a12-854">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="35a12-855">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="35a12-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="35a12-856">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="35a12-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35a12-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35a12-857">Az.Cdn</span></span>
* <span data-ttu-id="35a12-858">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="35a12-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-859">Az.Compute</span></span>
* <span data-ttu-id="35a12-860">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="35a12-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-861">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-862">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="35a12-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35a12-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35a12-863">Az.LogicApp</span></span>
* <span data-ttu-id="35a12-864">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="35a12-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-865">Az.Network</span></span>
* <span data-ttu-id="35a12-866">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="35a12-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-868">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="35a12-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="35a12-869">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="35a12-869">SDK Update</span></span>
* <span data-ttu-id="35a12-870">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="35a12-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="35a12-871">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="35a12-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-872">Az.Resources</span></span>
* <span data-ttu-id="35a12-873">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="35a12-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="35a12-874">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="35a12-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="35a12-875">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="35a12-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="35a12-876">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="35a12-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="35a12-877">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="35a12-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="35a12-878">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="35a12-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-879">Az.Sql</span></span>
* <span data-ttu-id="35a12-880">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="35a12-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="35a12-881">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="35a12-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-882">Az.Storage</span></span>
* <span data-ttu-id="35a12-883">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="35a12-884">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="35a12-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35a12-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="35a12-886">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="35a12-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-887">Az.Automation</span></span>
* <span data-ttu-id="35a12-888">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="35a12-889">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="35a12-890">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="35a12-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35a12-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="35a12-892">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="35a12-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-893">Az.Compute</span></span>
* <span data-ttu-id="35a12-894">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="35a12-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="35a12-895">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="35a12-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="35a12-896">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="35a12-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="35a12-897">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="35a12-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-899">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="35a12-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="35a12-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="35a12-900">Az.EventHub</span></span>
* <span data-ttu-id="35a12-901">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="35a12-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="35a12-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-902">Az.KeyVault</span></span>
* <span data-ttu-id="35a12-903">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35a12-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35a12-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35a12-904">Az.LogicApp</span></span>
* <span data-ttu-id="35a12-905">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="35a12-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="35a12-906">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="35a12-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="35a12-907">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="35a12-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="35a12-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35a12-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="35a12-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35a12-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="35a12-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35a12-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="35a12-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="35a12-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="35a12-912">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="35a12-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="35a12-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="35a12-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="35a12-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="35a12-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="35a12-917">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="35a12-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="35a12-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35a12-918">Az.Monitor</span></span>
* <span data-ttu-id="35a12-919">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="35a12-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-920">Az.Network</span></span>
* <span data-ttu-id="35a12-921">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="35a12-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="35a12-923">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="35a12-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="35a12-924">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="35a12-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="35a12-925">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="35a12-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="35a12-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-926">Az.Resources</span></span>
* <span data-ttu-id="35a12-927">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="35a12-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="35a12-928">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="35a12-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="35a12-929">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="35a12-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="35a12-930">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="35a12-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-931">Az.Sql</span></span>
* <span data-ttu-id="35a12-932">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="35a12-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="35a12-933">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="35a12-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-934">Az.Websites</span></span>
* <span data-ttu-id="35a12-935">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="35a12-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="35a12-936">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-937">Az.Accounts</span></span>
* <span data-ttu-id="35a12-938">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="35a12-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="35a12-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35a12-939">Az.AnalysisServices</span></span>
<span data-ttu-id="35a12-940">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="35a12-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-941">Az.Compute</span></span>
* <span data-ttu-id="35a12-942">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="35a12-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="35a12-943">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="35a12-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="35a12-944">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="35a12-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-945">Az.RecoveryServices</span></span>
<span data-ttu-id="35a12-946">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="35a12-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-947">Az.Resources</span></span>
* <span data-ttu-id="35a12-948">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="35a12-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="35a12-949">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="35a12-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="35a12-950">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="35a12-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="35a12-951">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="35a12-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-952">Az.Sql</span></span>
* <span data-ttu-id="35a12-953">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="35a12-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="35a12-954">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="35a12-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="35a12-955">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="35a12-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="35a12-956">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-957">Az.Accounts</span></span>
* <span data-ttu-id="35a12-958">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="35a12-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="35a12-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="35a12-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="35a12-960">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="35a12-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="35a12-962">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="35a12-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="35a12-963">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-964">Az.Accounts</span></span>
* <span data-ttu-id="35a12-965">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="35a12-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="35a12-966">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35a12-967">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="35a12-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="35a12-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="35a12-968">Az.Aks</span></span>
* <span data-ttu-id="35a12-969">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="35a12-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-970">Az.Automation</span></span>
* <span data-ttu-id="35a12-971">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="35a12-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="35a12-972">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="35a12-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="35a12-973">Az.Cdn</span></span>
* <span data-ttu-id="35a12-974">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-975">Az.Compute</span></span>
* <span data-ttu-id="35a12-976">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="35a12-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="35a12-977">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="35a12-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="35a12-978">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="35a12-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="35a12-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="35a12-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="35a12-980">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="35a12-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="35a12-981">Az.DataFactory</span></span>
* <span data-ttu-id="35a12-982">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="35a12-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-984">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="35a12-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="35a12-985">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="35a12-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="35a12-986">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35a12-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35a12-987">Az.IotHub</span></span>
* <span data-ttu-id="35a12-988">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="35a12-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="35a12-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-989">Az.KeyVault</span></span>
* <span data-ttu-id="35a12-990">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-991">Az.Network</span></span>
* <span data-ttu-id="35a12-992">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-993">Az.Resources</span></span>
* <span data-ttu-id="35a12-994">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="35a12-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="35a12-995">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="35a12-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="35a12-996">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35a12-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="35a12-997">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="35a12-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="35a12-998">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="35a12-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="35a12-999">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="35a12-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="35a12-1000">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="35a12-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35a12-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="35a12-1002">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="35a12-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="35a12-1003">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="35a12-1003">Fix some error messages.</span></span>
* <span data-ttu-id="35a12-1004">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="35a12-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="35a12-1005">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="35a12-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="35a12-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="35a12-1006">Az.SignalR</span></span>
* <span data-ttu-id="35a12-1007">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-1008">Az.Sql</span></span>
* <span data-ttu-id="35a12-1009">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35a12-1010">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="35a12-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="35a12-1011">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="35a12-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="35a12-1012">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="35a12-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-1013">Az.Storage</span></span>
* <span data-ttu-id="35a12-1014">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35a12-1015">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="35a12-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="35a12-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="35a12-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="35a12-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="35a12-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="35a12-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="35a12-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="35a12-1019">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-1020">Az.Websites</span></span>
* <span data-ttu-id="35a12-1021">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="35a12-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="35a12-1022">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="35a12-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="35a12-1023">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="35a12-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="35a12-1024">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="35a12-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="35a12-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-1025">Az.Accounts</span></span>
* <span data-ttu-id="35a12-1026">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="35a12-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-1027">Az.Compute</span></span>
* <span data-ttu-id="35a12-1028">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="35a12-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="35a12-1029">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="35a12-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="35a12-1030">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-1032">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="35a12-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="35a12-1033">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="35a12-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="35a12-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="35a12-1034">Az.EventGrid</span></span>
* <span data-ttu-id="35a12-1035">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="35a12-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="35a12-1036">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="35a12-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="35a12-1037">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="35a12-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="35a12-1038">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="35a12-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="35a12-1039">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="35a12-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="35a12-1040">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="35a12-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="35a12-1041">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="35a12-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="35a12-1042">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="35a12-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="35a12-1043">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="35a12-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="35a12-1044">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="35a12-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="35a12-1045">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="35a12-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="35a12-1046">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="35a12-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="35a12-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="35a12-1047">Az.IotHub</span></span>
* <span data-ttu-id="35a12-1048">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="35a12-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="35a12-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="35a12-1049">Az.LogicApp</span></span>
* <span data-ttu-id="35a12-1050">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="35a12-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1051">Az.Resources</span></span>
* <span data-ttu-id="35a12-1052">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="35a12-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="35a12-1053">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="35a12-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="35a12-1054">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35a12-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="35a12-1055">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="35a12-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="35a12-1056">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="35a12-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="35a12-1057">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="35a12-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="35a12-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="35a12-1058">Az.SignalR</span></span>
* <span data-ttu-id="35a12-1059">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-1060">Az.Sql</span></span>
* <span data-ttu-id="35a12-1061">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="35a12-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="35a12-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-1062">Az.Storage</span></span>
* <span data-ttu-id="35a12-1063">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="35a12-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="35a12-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="35a12-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="35a12-1065">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="35a12-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="35a12-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="35a12-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-1067">Az.Websites</span></span>
* <span data-ttu-id="35a12-1068">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="35a12-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="35a12-1069">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="35a12-1070">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="35a12-1071">Généralités</span><span class="sxs-lookup"><span data-stu-id="35a12-1071">General</span></span>

- <span data-ttu-id="35a12-1072">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="35a12-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="35a12-1073">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="35a12-1073">Online help for each module</span></span>
- <span data-ttu-id="35a12-1074">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="35a12-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="35a12-1075">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="35a12-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="35a12-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-1076">Az.Accounts</span></span>
- <span data-ttu-id="35a12-1077">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35a12-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="35a12-1078">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="35a12-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="35a12-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35a12-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="35a12-1080">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="35a12-1080">Fixes for #7002</span></span>
- <span data-ttu-id="35a12-1081">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="35a12-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="35a12-1082">Az.Batch</span></span>
- <span data-ttu-id="35a12-1083">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="35a12-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="35a12-1084">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="35a12-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="35a12-1085">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="35a12-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="35a12-1086">Az.Billing</span></span>
- <span data-ttu-id="35a12-1087">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="35a12-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="35a12-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="35a12-1089">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="35a12-1090">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="35a12-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="35a12-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="35a12-1092">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="35a12-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="35a12-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="35a12-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="35a12-1094">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="35a12-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="35a12-1096">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="35a12-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="35a12-1097">Az.Monitor</span></span>
- <span data-ttu-id="35a12-1098">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="35a12-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="35a12-1099">Az.KeyVault</span></span>
- <span data-ttu-id="35a12-1100">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="35a12-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="35a12-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="35a12-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="35a12-1102">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="35a12-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="35a12-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="35a12-1103">Az.Media</span></span>
- <span data-ttu-id="35a12-1104">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="35a12-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="35a12-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-1105">Az.Network</span></span>
<span data-ttu-id="35a12-1106">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="35a12-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="35a12-1107">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="35a12-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="35a12-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35a12-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35a12-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35a12-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35a12-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="35a12-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="35a12-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="35a12-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="35a12-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="35a12-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="35a12-1116">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="35a12-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="35a12-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35a12-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="35a12-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35a12-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="35a12-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="35a12-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="35a12-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="35a12-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="35a12-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="35a12-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="35a12-1123">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35a12-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="35a12-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="35a12-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="35a12-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="35a12-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="35a12-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="35a12-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="35a12-1127">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="35a12-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="35a12-1128">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="35a12-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="35a12-1130">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="35a12-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35a12-1131">Az.Profile</span></span>
- <span data-ttu-id="35a12-1132">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="35a12-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="35a12-1134">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="35a12-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1135">Az.Resources</span></span>
- <span data-ttu-id="35a12-1136">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="35a12-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="35a12-1138">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="35a12-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="35a12-1139">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="35a12-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="35a12-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="35a12-1141">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="35a12-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="35a12-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-1142">Az.Sql</span></span>
- <span data-ttu-id="35a12-1143">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="35a12-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="35a12-1144">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="35a12-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="35a12-1145">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="35a12-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-1146">Az.Storage</span></span>
- <span data-ttu-id="35a12-1147">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="35a12-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-1148">Az.Websites</span></span>
- <span data-ttu-id="35a12-1149">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="35a12-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="35a12-1150">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="35a12-1151">Généralités</span><span class="sxs-lookup"><span data-stu-id="35a12-1151">General</span></span>

* <span data-ttu-id="35a12-1152">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="35a12-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="35a12-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-1153">Az.Compute</span></span>

* <span data-ttu-id="35a12-1154">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="35a12-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="35a12-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="35a12-1156">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="35a12-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="35a12-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="35a12-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="35a12-1158">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="35a12-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="35a12-1159">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="35a12-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="35a12-1160">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="35a12-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="35a12-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="35a12-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="35a12-1162">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="35a12-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="35a12-1163">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="35a12-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="35a12-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1164">Az.Resources</span></span>

* <span data-ttu-id="35a12-1165">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="35a12-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="35a12-1166">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="35a12-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="35a12-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-1167">Az.Sql</span></span>

* <span data-ttu-id="35a12-1168">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="35a12-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="35a12-1169">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="35a12-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="35a12-1170">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="35a12-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="35a12-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-1171">Az.Storage</span></span>

* <span data-ttu-id="35a12-1172">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="35a12-1173">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="35a12-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="35a12-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="35a12-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="35a12-1175">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="35a12-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="35a12-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="35a12-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="35a12-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="35a12-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="35a12-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-1178">Az.Websites</span></span>

* <span data-ttu-id="35a12-1179">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="35a12-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="35a12-1180">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="35a12-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="35a12-1181">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="35a12-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="35a12-1182">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="35a12-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="35a12-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="35a12-1184">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="35a12-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="35a12-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="35a12-1185">Az.Automation</span></span>
* <span data-ttu-id="35a12-1186">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="35a12-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="35a12-1187">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="35a12-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="35a12-1188">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="35a12-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="35a12-1189">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="35a12-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="35a12-1190">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="35a12-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="35a12-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-1191">Az.Compute</span></span>
* <span data-ttu-id="35a12-1192">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="35a12-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="35a12-1193">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="35a12-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="35a12-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="35a12-1195">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="35a12-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="35a12-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="35a12-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="35a12-1197">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="35a12-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="35a12-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-1198">Az.Network</span></span>
* <span data-ttu-id="35a12-1199">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="35a12-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="35a12-1200">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="35a12-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="35a12-1201">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="35a12-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="35a12-1202">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="35a12-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="35a12-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="35a12-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="35a12-1204">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="35a12-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="35a12-1205">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="35a12-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="35a12-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="35a12-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="35a12-1207">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="35a12-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="35a12-1208">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="35a12-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="35a12-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="35a12-1209">Az.Relay</span></span>
* <span data-ttu-id="35a12-1210">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="35a12-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="35a12-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1211">Az.Resources</span></span>
* <span data-ttu-id="35a12-1212">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="35a12-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="35a12-1213">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="35a12-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="35a12-1214">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="35a12-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="35a12-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="35a12-1216">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="35a12-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="35a12-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-1217">Az.Sql</span></span>
* <span data-ttu-id="35a12-1218">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="35a12-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="35a12-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35a12-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35a12-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35a12-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="35a12-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="35a12-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35a12-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="35a12-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35a12-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="35a12-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35a12-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="35a12-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="35a12-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="35a12-1227">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="35a12-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="35a12-1228">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="35a12-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="35a12-1229">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="35a12-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="35a12-1230">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="35a12-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="35a12-1231">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="35a12-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="35a12-1232">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="35a12-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="35a12-1233">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="35a12-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="35a12-1234">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="35a12-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="35a12-1235">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="35a12-1236">Généralités</span><span class="sxs-lookup"><span data-stu-id="35a12-1236">General</span></span>
* <span data-ttu-id="35a12-1237">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="35a12-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="35a12-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35a12-1238">Az.Profile</span></span>
* <span data-ttu-id="35a12-1239">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="35a12-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="35a12-1240">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="35a12-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="35a12-1241">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="35a12-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="35a12-1242">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="35a12-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="35a12-1243">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="35a12-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="35a12-1244">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="35a12-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="35a12-1245">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="35a12-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="35a12-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35a12-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="35a12-1247">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="35a12-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-1248">Az.Compute</span></span>
* <span data-ttu-id="35a12-1249">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="35a12-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="35a12-1250">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="35a12-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="35a12-1251">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="35a12-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-1253">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="35a12-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="35a12-1254">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="35a12-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="35a12-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="35a12-1255">Az.Insights</span></span>
* <span data-ttu-id="35a12-1256">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="35a12-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="35a12-1257">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="35a12-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="35a12-1258">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="35a12-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="35a12-1259">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="35a12-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-1260">Az.Network</span></span>
* <span data-ttu-id="35a12-1261">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="35a12-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="35a12-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="35a12-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="35a12-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="35a12-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="35a12-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="35a12-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="35a12-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="35a12-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="35a12-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="35a12-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="35a12-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="35a12-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="35a12-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="35a12-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="35a12-1269">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="35a12-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1270">Az.Resources</span></span>
* <span data-ttu-id="35a12-1271">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="35a12-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="35a12-1272">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="35a12-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="35a12-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="35a12-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="35a12-1274">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="35a12-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="35a12-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="35a12-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="35a12-1276">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="35a12-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="35a12-1277">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="35a12-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="35a12-1278">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="35a12-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="35a12-1279">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="35a12-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="35a12-1280">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="35a12-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="35a12-1281">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="35a12-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="35a12-1282">Az.Profile</span></span>
* <span data-ttu-id="35a12-1283">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="35a12-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="35a12-1284">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="35a12-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-1285">Az.Compute</span></span>
* <span data-ttu-id="35a12-1286">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="35a12-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="35a12-1287">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="35a12-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="35a12-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="35a12-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="35a12-1289">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="35a12-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="35a12-1290">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="35a12-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="35a12-1291">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="35a12-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="35a12-1292">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="35a12-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="35a12-1293">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="35a12-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-1294">Az.Network</span></span>
* <span data-ttu-id="35a12-1295">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="35a12-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="35a12-1296">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="35a12-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1297">Az.Resources</span></span>
* <span data-ttu-id="35a12-1298">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="35a12-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="35a12-1299">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="35a12-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="35a12-1300">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="35a12-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="35a12-1301">Azure.Storage</span></span>
* <span data-ttu-id="35a12-1302">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="35a12-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="35a12-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="35a12-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="35a12-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="35a12-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="35a12-1305">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="35a12-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="35a12-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="35a12-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="35a12-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="35a12-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="35a12-1308">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="35a12-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="35a12-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="35a12-1309">Az.Compute</span></span>
* <span data-ttu-id="35a12-1310">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="35a12-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="35a12-1311">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="35a12-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="35a12-1312">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="35a12-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="35a12-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="35a12-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="35a12-1314">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="35a12-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="35a12-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="35a12-1315">Az.Network</span></span>
* <span data-ttu-id="35a12-1316">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="35a12-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="35a12-1317">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="35a12-1317">new cmdlets added</span></span>
    - <span data-ttu-id="35a12-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35a12-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="35a12-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35a12-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="35a12-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35a12-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="35a12-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="35a12-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="35a12-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="35a12-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="35a12-1324">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="35a12-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="35a12-1325">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="35a12-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="35a12-1326">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="35a12-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="35a12-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="35a12-1327">Az.RedisCache</span></span>
* <span data-ttu-id="35a12-1328">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="35a12-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="35a12-1329">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="35a12-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="35a12-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="35a12-1330">Az.Resources</span></span>
* <span data-ttu-id="35a12-1331">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="35a12-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="35a12-1332">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="35a12-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="35a12-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="35a12-1333">Az.Sql</span></span>
* <span data-ttu-id="35a12-1334">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="35a12-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="35a12-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="35a12-1335">Az.Websites</span></span>
* <span data-ttu-id="35a12-1336">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="35a12-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="35a12-1337">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="35a12-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="35a12-1338">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="35a12-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="35a12-1339">Version initiale</span><span class="sxs-lookup"><span data-stu-id="35a12-1339">Initial Release</span></span>