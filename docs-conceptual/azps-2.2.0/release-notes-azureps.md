---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498673"
---
## <a name="220---june-2019"></a><span data-ttu-id="6a0d5-101">2.2.0 - Juin 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6a0d5-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6a0d5-102">Az.Cdn</span></span>
* <span data-ttu-id="6a0d5-103">Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-104">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-105">Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6a0d5-106">Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6a0d5-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6a0d5-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-107">Az.EventHub</span></span>
* <span data-ttu-id="6a0d5-108">Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6a0d5-109">Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0d5-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-110">Az.Network</span></span>
* <span data-ttu-id="6a0d5-111">Mise à jour de ResourceId et de InputObject pour Nat Gateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6a0d5-112">Ajout d’un alias pour ResourceId et InputObject</span><span class="sxs-lookup"><span data-stu-id="6a0d5-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6a0d5-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="6a0d5-114">Correction du problème de la référence null dans Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6a0d5-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="6a0d5-116">Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7</span><span class="sxs-lookup"><span data-stu-id="6a0d5-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6a0d5-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6a0d5-117">Az.ServiceBus</span></span>
* <span data-ttu-id="6a0d5-118">Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a0d5-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6a0d5-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="6a0d5-120">Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6a0d5-121">Correction pour le caractère manquant dans les lignes de commande de Service Fabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-122">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-123">Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6a0d5-124">Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6a0d5-125">Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6a0d5-126">Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-127">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-128">Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6a0d5-129">2.1.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6a0d5-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-130">Az.ApiManagement</span></span>
* <span data-ttu-id="6a0d5-131">Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6a0d5-132">**Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6a0d5-133">**New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6a0d5-134">**New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps</span><span class="sxs-lookup"><span data-stu-id="6a0d5-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6a0d5-135">**New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6a0d5-136">**New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic</span><span class="sxs-lookup"><span data-stu-id="6a0d5-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6a0d5-137">**Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6a0d5-138">**Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6a0d5-139">Création d’applets de commande pour la gestion du cache dans le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6a0d5-140">**Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches</span><span class="sxs-lookup"><span data-stu-id="6a0d5-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6a0d5-141">**New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière</span><span class="sxs-lookup"><span data-stu-id="6a0d5-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6a0d5-142">**Remove-AzApiManagementCache** - Supprimer un cache</span><span class="sxs-lookup"><span data-stu-id="6a0d5-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6a0d5-143">**Update-AzApiManagementCache** - Mettre à jour un cache</span><span class="sxs-lookup"><span data-stu-id="6a0d5-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6a0d5-144">Création d’applets de commande pour la gestion du schéma des API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6a0d5-145">**New-AzApiManagementSchema** - Créer un schéma pour une API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6a0d5-146">**Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6a0d5-147">**Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6a0d5-148">**Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6a0d5-149">Création d’une applet de commande pour générer un jeton utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6a0d5-150">**New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./</span><span class="sxs-lookup"><span data-stu-id="6a0d5-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6a0d5-151">Création d’une applet de commande pour la récupération de l’état du réseau</span><span class="sxs-lookup"><span data-stu-id="6a0d5-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6a0d5-152">**Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6a0d5-153">Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6a0d5-154">Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API</span><span class="sxs-lookup"><span data-stu-id="6a0d5-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6a0d5-155">Ajout de la prise en charge de la nouvelle référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6a0d5-156">Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6a0d5-157">La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6a0d5-158">Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6a0d5-159">Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6a0d5-160">Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée</span><span class="sxs-lookup"><span data-stu-id="6a0d5-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6a0d5-161">Mise à jour de l’applet de commande pour afficher les messages d’erreur inline</span><span class="sxs-lookup"><span data-stu-id="6a0d5-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6a0d5-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6a0d5-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6a0d5-163">Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6a0d5-164">Mise à jour de l’applet de commande **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6a0d5-165">Pour importer des API depuis la spécification de document « OpenApi 3.0 »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6a0d5-166">Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).</span><span class="sxs-lookup"><span data-stu-id="6a0d5-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6a0d5-167">Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6a0d5-168">Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6a0d5-169">Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6a0d5-170">Mise à jour de l’applet de commande **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6a0d5-171">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6a0d5-172">Pour créer une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6a0d5-173">Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6a0d5-174">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6a0d5-175">Mise à jour de l’applet de commande **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6a0d5-176">Pour configurer une API avec le serveur d’autorisation « OpenId ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6a0d5-177">Pour mettre à jour une API dans un « ApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6a0d5-178">Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6a0d5-179">Mise à jour de l’applet de commande **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6a0d5-180">Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6a0d5-181">La nouvelle révision fait une supposition pour le « ApiId » du parent.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6a0d5-182">Pour fournir une « ApiRevisionDescription »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6a0d5-183">Pour remplacer le « ServiceUrl » lors du clonage d’une API.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6a0d5-184">Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6a0d5-185">Pour configurer « AAD » ou « AADB2C » avec une « Authority »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6a0d5-186">Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6a0d5-187">Mise à jour de l’applet de commande **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6a0d5-188">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6a0d5-189">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6a0d5-190">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6a0d5-191">Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6a0d5-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6a0d5-192">Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6a0d5-193">Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6a0d5-194">Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6a0d5-195">Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée</span><span class="sxs-lookup"><span data-stu-id="6a0d5-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6a0d5-196">« New-AzApiManagementContext »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6a0d5-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6a0d5-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6a0d5-198">« Get-AzApiManagementApiRelease »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6a0d5-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6a0d5-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6a0d5-200">« Get-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6a0d5-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6a0d5-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6a0d5-202">« Get-AzApiManagementAuthorizationServer »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6a0d5-203">« Get-AzApiManagementBackend »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6a0d5-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6a0d5-205">« Get-AzApiManagementCertificate »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6a0d5-206">« Remove-AzApiManagementApiVersionSet »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6a0d5-207">« Remove-AzApiManagementSubscription »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6a0d5-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-208">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-209">Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6a0d5-210">Corriger le problème https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="6a0d5-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6a0d5-211">Corriger le problème https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="6a0d5-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6a0d5-212">Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6a0d5-213">Corriger le problème https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="6a0d5-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6a0d5-214">Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6a0d5-215">Elle retourne désormais seulement le nœud correspondant.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-216">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-217">Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6a0d5-218">Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-220">Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6a0d5-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-221">Az.Monitor</span></span>
* <span data-ttu-id="6a0d5-222">Correction des noms de paramètres incorrects dans les exemples d’aide</span><span class="sxs-lookup"><span data-stu-id="6a0d5-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-223">Az.Network</span></span>
* <span data-ttu-id="6a0d5-224">Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives</span><span class="sxs-lookup"><span data-stu-id="6a0d5-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6a0d5-225">Mise à jour de l’applet de commande :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="6a0d5-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6a0d5-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6a0d5-227">Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6a0d5-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-228">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-229">Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus</span><span class="sxs-lookup"><span data-stu-id="6a0d5-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-230">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-231">Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="6a0d5-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6a0d5-232">2.0.0 - Mai 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-233">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-234">Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe</span><span class="sxs-lookup"><span data-stu-id="6a0d5-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6a0d5-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="6a0d5-236">Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6a0d5-237">Amélioration de l’erreur en cas d’échec de la création d’un compte.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-238">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-239">Fonctionnalité de groupe de placements de proximité.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6a0d5-240">Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6a0d5-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6a0d5-241">Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6a0d5-242">Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6a0d5-243">TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6a0d5-244">Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6a0d5-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6a0d5-245">Dernières modifications</span><span class="sxs-lookup"><span data-stu-id="6a0d5-245">Breaking changes</span></span>
    - <span data-ttu-id="6a0d5-246">Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6a0d5-247">Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6a0d5-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6a0d5-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="6a0d5-249">Première version en disponibilité générale des applets de commande Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="6a0d5-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6a0d5-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6a0d5-250">Az.Dns</span></span>
* <span data-ttu-id="6a0d5-251">Délégation de serveur de noms DNS automatique</span><span class="sxs-lookup"><span data-stu-id="6a0d5-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6a0d5-252">L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6a0d5-253">Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6a0d5-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-254">Az.FrontDoor</span></span>
* <span data-ttu-id="6a0d5-255">Première version en disponibilité générale des applets de commande Azure FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6a0d5-256">Renommage des applets de commande WAF pour inclure « Waf »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6a0d5-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6a0d5-257">Az.HDInsight</span></span>
* <span data-ttu-id="6a0d5-258">Suppression de deux applets de commande :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6a0d5-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6a0d5-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6a0d5-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6a0d5-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6a0d5-261">Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6a0d5-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6a0d5-262">Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6a0d5-263">Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6a0d5-264">Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6a0d5-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-265">Az.Monitor</span></span>
* <span data-ttu-id="6a0d5-266">Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)</span><span class="sxs-lookup"><span data-stu-id="6a0d5-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6a0d5-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6a0d5-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6a0d5-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6a0d5-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6a0d5-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6a0d5-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6a0d5-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6a0d5-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6a0d5-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6a0d5-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6a0d5-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6a0d5-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6a0d5-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6a0d5-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6a0d5-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6a0d5-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6a0d5-278">[Plus d’informations](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) sur l’API SQR</span><span class="sxs-lookup"><span data-stu-id="6a0d5-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6a0d5-279">Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)</span><span class="sxs-lookup"><span data-stu-id="6a0d5-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-280">Az.Network</span></span>
* <span data-ttu-id="6a0d5-281">Ajout de la prise en charge de la ressource NAT Gateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6a0d5-282">Nouvelles applets de commande</span><span class="sxs-lookup"><span data-stu-id="6a0d5-282">New cmdlets</span></span>
        - <span data-ttu-id="6a0d5-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="6a0d5-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6a0d5-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6a0d5-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6a0d5-287">Applets de commande mises à jour</span><span class="sxs-lookup"><span data-stu-id="6a0d5-287">Updated cmdlets</span></span>
        - <span data-ttu-id="6a0d5-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6a0d5-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6a0d5-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6a0d5-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6a0d5-290">Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6a0d5-291">Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6a0d5-292">Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6a0d5-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="6a0d5-294">Prise en charge de l’interrogation des détails d’évaluation de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6a0d5-295">Ajout du paramètre « -Expand » à Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6a0d5-296">Prise en charge de « -Expand PolicyEvaluationDetails ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="6a0d5-298">Prise en charge de la récupération de site Azure vers Azure entre abonnements.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6a0d5-299">Marquage des changements cassants à venir pour Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6a0d5-300">Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6a0d5-301">Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6a0d5-302">Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6a0d5-303">Autres correctifs mineurs.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6a0d5-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6a0d5-304">Az.Relay</span></span>
* <span data-ttu-id="6a0d5-305">Correction des fautes de frappe dans les messages destinés aux clients</span><span class="sxs-lookup"><span data-stu-id="6a0d5-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6a0d5-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6a0d5-306">Az.ServiceBus</span></span>
* <span data-ttu-id="6a0d5-307">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="6a0d5-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6a0d5-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-308">Az.Storage</span></span>
* <span data-ttu-id="6a0d5-309">Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)</span><span class="sxs-lookup"><span data-stu-id="6a0d5-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6a0d5-310">Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6a0d5-311">La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6a0d5-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="6a0d5-313">Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6a0d5-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6a0d5-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6a0d5-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-317">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-318">Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6a0d5-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6a0d5-319">Get-AzWebApp\*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés</span><span class="sxs-lookup"><span data-stu-id="6a0d5-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6a0d5-320">1.8.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6a0d5-321">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-321">Highlights since the last major release</span></span>
* <span data-ttu-id="6a0d5-322">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="6a0d5-322">General availability of `Az` module</span></span>
* <span data-ttu-id="6a0d5-323">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6a0d5-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6a0d5-324">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6a0d5-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6a0d5-325">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6a0d5-326">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6a0d5-327">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6a0d5-328">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-329">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-330">Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac</span><span class="sxs-lookup"><span data-stu-id="6a0d5-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6a0d5-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6a0d5-331">Az.Batch</span></span>
* <span data-ttu-id="6a0d5-332">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6a0d5-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6a0d5-333">Az.Cdn</span></span>
* <span data-ttu-id="6a0d5-334">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6a0d5-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="6a0d5-336">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-337">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-338">Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource</span><span class="sxs-lookup"><span data-stu-id="6a0d5-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6a0d5-339">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6a0d5-340">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="6a0d5-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6a0d5-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6a0d5-341">Az.DataFactory</span></span>
* <span data-ttu-id="6a0d5-342">Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-344">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6a0d5-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6a0d5-345">Az.EventGrid</span></span>
* <span data-ttu-id="6a0d5-346">Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6a0d5-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-347">Az.EventHub</span></span>
* <span data-ttu-id="6a0d5-348">Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace</span><span class="sxs-lookup"><span data-stu-id="6a0d5-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6a0d5-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6a0d5-349">Az.HDInsight</span></span>
* <span data-ttu-id="6a0d5-350">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6a0d5-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-351">Az.IotHub</span></span>
* <span data-ttu-id="6a0d5-352">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6a0d5-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a0d5-353">Az.KeyVault</span></span>
* <span data-ttu-id="6a0d5-354">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6a0d5-355">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="6a0d5-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6a0d5-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6a0d5-356">Az.MachineLearning</span></span>
* <span data-ttu-id="6a0d5-357">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6a0d5-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6a0d5-358">Az.Media</span></span>
* <span data-ttu-id="6a0d5-359">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6a0d5-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-360">Az.Monitor</span></span>
  * <span data-ttu-id="6a0d5-361">Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6a0d5-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6a0d5-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6a0d5-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6a0d5-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6a0d5-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6a0d5-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6a0d5-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6a0d5-367">Mise à jour du kit SDK Monitor avec la version 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="6a0d5-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-368">Az.Network</span></span>
* <span data-ttu-id="6a0d5-369">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6a0d5-370">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="6a0d5-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6a0d5-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6a0d5-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="6a0d5-372">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6a0d5-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="6a0d5-374">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6a0d5-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6a0d5-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6a0d5-376">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="6a0d5-378">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6a0d5-379">Mise à jour du format de table pour SQL dans azure VM</span><span class="sxs-lookup"><span data-stu-id="6a0d5-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6a0d5-380">Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="6a0d5-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6a0d5-381">Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="6a0d5-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6a0d5-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6a0d5-382">Az.RedisCache</span></span>
* <span data-ttu-id="6a0d5-383">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-384">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-385">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="6a0d5-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-386">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-387">Remplacement de la dépendance sur le kit SDK Monitor par du code courant</span><span class="sxs-lookup"><span data-stu-id="6a0d5-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6a0d5-388">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6a0d5-389">Amélioration du processus de classification de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6a0d5-390">Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6a0d5-391">Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6a0d5-392">Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6a0d5-393">Correction de la documentation des caractères génériques</span><span class="sxs-lookup"><span data-stu-id="6a0d5-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-394">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-395">Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="6a0d5-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6a0d5-396">Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6a0d5-397">Mise à jour du kit SDK WebSites.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6a0d5-398">Suppression de la propriété AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6a0d5-399">1.7.0 - Avril 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6a0d5-400">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-400">Highlights since the last major release</span></span>
* <span data-ttu-id="6a0d5-401">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="6a0d5-401">General availability of `Az` module</span></span>
* <span data-ttu-id="6a0d5-402">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6a0d5-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6a0d5-403">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6a0d5-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6a0d5-404">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6a0d5-405">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6a0d5-406">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6a0d5-407">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-408">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-409">Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="6a0d5-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6a0d5-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="6a0d5-411">Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine</span><span class="sxs-lookup"><span data-stu-id="6a0d5-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6a0d5-412">Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant</span><span class="sxs-lookup"><span data-stu-id="6a0d5-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6a0d5-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-413">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-414">Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6a0d5-415">Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6a0d5-416">Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-417">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-418">Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6a0d5-419">Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6a0d5-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="6a0d5-421">Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin</span><span class="sxs-lookup"><span data-stu-id="6a0d5-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6a0d5-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6a0d5-422">Az.DataFactory</span></span>
* <span data-ttu-id="6a0d5-423">Mise à jour du kit SDK .Net ADF avec la version 3.0.2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6a0d5-424">Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-425">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-426">Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis</span><span class="sxs-lookup"><span data-stu-id="6a0d5-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6a0d5-427">Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6a0d5-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6a0d5-428">Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande</span><span class="sxs-lookup"><span data-stu-id="6a0d5-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6a0d5-429">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6a0d5-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6a0d5-430">Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail</span><span class="sxs-lookup"><span data-stu-id="6a0d5-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6a0d5-431">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6a0d5-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-432">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-433">Prise en charge de la classification des données de base de données.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6a0d5-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-434">Az.Storage</span></span>
* <span data-ttu-id="6a0d5-435">Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion</span><span class="sxs-lookup"><span data-stu-id="6a0d5-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6a0d5-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a0d5-436">New-AzStorageContext</span></span>
* <span data-ttu-id="6a0d5-437">Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion</span><span class="sxs-lookup"><span data-stu-id="6a0d5-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6a0d5-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6a0d5-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6a0d5-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6a0d5-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6a0d5-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6a0d5-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6a0d5-442">Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob</span><span class="sxs-lookup"><span data-stu-id="6a0d5-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6a0d5-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6a0d5-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6a0d5-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6a0d5-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6a0d5-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6a0d5-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6a0d5-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6a0d5-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6a0d5-447">1.6.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6a0d5-448">Points importants depuis la dernière version majeure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-448">Highlights since the last major release</span></span>
* <span data-ttu-id="6a0d5-449">Disponibilité générale du module `Az`</span><span class="sxs-lookup"><span data-stu-id="6a0d5-449">General availability of `Az` module</span></span>
* <span data-ttu-id="6a0d5-450">Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6a0d5-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6a0d5-451">Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6a0d5-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6a0d5-452">Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6a0d5-453">Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6a0d5-454">Ajout de la prise en charge des runbooks Python 2 dans Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6a0d5-455">Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6a0d5-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-456">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-457">Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6a0d5-458">Regroupement dynamique</span><span class="sxs-lookup"><span data-stu-id="6a0d5-458">Dynamic grouping</span></span>
    * <span data-ttu-id="6a0d5-459">Pré-Post script</span><span class="sxs-lookup"><span data-stu-id="6a0d5-459">Pre-Post script</span></span>
    * <span data-ttu-id="6a0d5-460">Paramètre de redémarrage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-461">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-462">Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6a0d5-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6a0d5-463">Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6a0d5-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a0d5-464">Az.KeyVault</span></span>
* <span data-ttu-id="6a0d5-465">Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a0d5-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-466">Az.Network</span></span>
* <span data-ttu-id="6a0d5-467">Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6a0d5-468">Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées</span><span class="sxs-lookup"><span data-stu-id="6a0d5-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="6a0d5-470">Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés</span><span class="sxs-lookup"><span data-stu-id="6a0d5-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6a0d5-471">Ajout de la prise en charge de canal pour la désinscription de conteneur</span><span class="sxs-lookup"><span data-stu-id="6a0d5-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-472">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-473">Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a0d5-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6a0d5-474">Mise à jour des informations d’identification utilisées lors des appels génériques à ARM</span><span class="sxs-lookup"><span data-stu-id="6a0d5-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-475">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-476">Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6a0d5-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-477">Az.Storage</span></span>
* <span data-ttu-id="6a0d5-478">Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6a0d5-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6a0d5-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6a0d5-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6a0d5-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6a0d5-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6a0d5-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6a0d5-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6a0d5-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-485">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-486">Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots'</span><span class="sxs-lookup"><span data-stu-id="6a0d5-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6a0d5-487">1.5.0 - Mars 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-488">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-489">Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées</span><span class="sxs-lookup"><span data-stu-id="6a0d5-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6a0d5-490">Mise à jour des exemples pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6a0d5-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-491">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-492">Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6a0d5-493">Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6a0d5-494">Maintenant, elle retourne tous les nœuds</span><span class="sxs-lookup"><span data-stu-id="6a0d5-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6a0d5-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6a0d5-495">Az.Cdn</span></span>
* <span data-ttu-id="6a0d5-496">Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-497">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-498">Ajout de la prise en charge des caractères génériques pour les applets de commande Get</span><span class="sxs-lookup"><span data-stu-id="6a0d5-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6a0d5-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6a0d5-499">Az.DataFactory</span></span>
* <span data-ttu-id="6a0d5-500">Mise à jour du kit .Net SDK ADF avec la version 3.0.1</span><span class="sxs-lookup"><span data-stu-id="6a0d5-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6a0d5-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6a0d5-501">Az.LogicApp</span></span>
* <span data-ttu-id="6a0d5-502">Correction de ListWorkflows qui récupérait uniquement la première page de résultats</span><span class="sxs-lookup"><span data-stu-id="6a0d5-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-503">Az.Network</span></span>
* <span data-ttu-id="6a0d5-504">Ajout de la prise en charge des caractères génériques pour les applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="6a0d5-506">Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="6a0d5-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6a0d5-507">Mise à jour du kit SDK</span><span class="sxs-lookup"><span data-stu-id="6a0d5-507">SDK Update</span></span>
* <span data-ttu-id="6a0d5-508">Suppression de la vérification de VMappContainer dans Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6a0d5-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6a0d5-509">Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6a0d5-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-510">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-511">Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6a0d5-512">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6a0d5-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6a0d5-513">Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6a0d5-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6a0d5-514">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6a0d5-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6a0d5-515">Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="6a0d5-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6a0d5-516">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6a0d5-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-517">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-518">Mise à jour d’AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6a0d5-519">Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6a0d5-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-520">Az.Storage</span></span>
* <span data-ttu-id="6a0d5-521">Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6a0d5-522">1.4.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6a0d5-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="6a0d5-524">Applet de commande AddAzureASAccount dépréciée</span><span class="sxs-lookup"><span data-stu-id="6a0d5-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6a0d5-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-525">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-526">Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6a0d5-527">Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6a0d5-528">Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6a0d5-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="6a0d5-530">Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-531">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-532">Résolution d’un problème lié aux jeux de paramètres d’ID</span><span class="sxs-lookup"><span data-stu-id="6a0d5-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6a0d5-533">Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6a0d5-534">Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6a0d5-535">Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-537">Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL</span><span class="sxs-lookup"><span data-stu-id="6a0d5-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6a0d5-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-538">Az.EventHub</span></span>
* <span data-ttu-id="6a0d5-539">Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6a0d5-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a0d5-540">Az.KeyVault</span></span>
* <span data-ttu-id="6a0d5-541">Correction du balisage de Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a0d5-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6a0d5-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6a0d5-542">Az.LogicApp</span></span>
* <span data-ttu-id="6a0d5-543">Ajout des comptes d’intégration dans la référence SKU de base</span><span class="sxs-lookup"><span data-stu-id="6a0d5-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6a0d5-544">Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid</span><span class="sxs-lookup"><span data-stu-id="6a0d5-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6a0d5-545">Nouvelles applets de commande pour les assemblys de compte d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6a0d5-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6a0d5-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6a0d5-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6a0d5-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6a0d5-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6a0d5-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6a0d5-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6a0d5-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6a0d5-550">Nouvelles applets de commande pour la configuration par lots des comptes d’intégration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6a0d5-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6a0d5-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6a0d5-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6a0d5-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6a0d5-555">Mise à jour du SDK Logic App vers la version 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6a0d5-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6a0d5-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-556">Az.Monitor</span></span>
* <span data-ttu-id="6a0d5-557">Mise à jour de l’aide pour Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-558">Az.Network</span></span>
* <span data-ttu-id="6a0d5-559">Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="6a0d5-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6a0d5-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="6a0d5-561">Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6a0d5-562">Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6a0d5-563">Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6a0d5-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-564">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-565">Corriger le problème https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6a0d5-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6a0d5-566">Corriger le problème https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6a0d5-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6a0d5-567">Corriger le problème https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="6a0d5-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6a0d5-568">Correction du bogue empêchant de créer plusieurs fois des KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="6a0d5-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-569">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-570">Ajout de la prise en charge du niveau Hyperscale de la base de données SQL</span><span class="sxs-lookup"><span data-stu-id="6a0d5-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6a0d5-571">Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-572">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-573">Correction de l’exemple dans Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="6a0d5-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6a0d5-574">1.3.0 - Février 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-575">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-576">Mettre à jour vers la version la plus récente de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0d5-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6a0d5-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-577">Az.AnalysisServices</span></span>
<span data-ttu-id="6a0d5-578">Disponibilité générale pour le module Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-579">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-580">Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80</span><span class="sxs-lookup"><span data-stu-id="6a0d5-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6a0d5-581">Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6a0d5-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6a0d5-582">Mettre à jour la description de l’aide et l’exemple pour Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-583">Az.RecoveryServices</span></span>
<span data-ttu-id="6a0d5-584">Disponibilité générale pour le module Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-585">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-586">Corriger le balisage pour les groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6a0d5-587">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6a0d5-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6a0d5-588">Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction</span><span class="sxs-lookup"><span data-stu-id="6a0d5-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6a0d5-589">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6a0d5-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-590">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-591">Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6a0d5-592">Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande</span><span class="sxs-lookup"><span data-stu-id="6a0d5-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6a0d5-593">L’exception de référence null a été résolue dans Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="6a0d5-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6a0d5-594">1.2.1 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-595">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-596">Publication avec version correcte de l’authentification</span><span class="sxs-lookup"><span data-stu-id="6a0d5-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6a0d5-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="6a0d5-598">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="6a0d5-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="6a0d5-600">Publication avec dépendance d’authentification mise à jour</span><span class="sxs-lookup"><span data-stu-id="6a0d5-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6a0d5-601">1.2.0 - Janvier 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-602">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-603">Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6a0d5-604">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6a0d5-605">Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="6a0d5-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6a0d5-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6a0d5-606">Az.Aks</span></span>
* <span data-ttu-id="6a0d5-607">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6a0d5-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-608">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-609">Ajout de la prise en charge des runbooks Python 2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6a0d5-610">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6a0d5-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6a0d5-611">Az.Cdn</span></span>
* <span data-ttu-id="6a0d5-612">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-613">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-614">Ajouter l’applet de commande Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6a0d5-615">Ajouter le paramètre TempDisk à Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6a0d5-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6a0d5-616">Corriger le message d’avertissement de New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6a0d5-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6a0d5-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a0d5-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6a0d5-618">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6a0d5-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6a0d5-619">Az.DataFactory</span></span>
* <span data-ttu-id="6a0d5-620">Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0</span><span class="sxs-lookup"><span data-stu-id="6a0d5-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-622">Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="6a0d5-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6a0d5-623">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6a0d5-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6a0d5-624">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6a0d5-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-625">Az.IotHub</span></span>
* <span data-ttu-id="6a0d5-626">Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6a0d5-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a0d5-627">Az.KeyVault</span></span>
* <span data-ttu-id="6a0d5-628">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-629">Az.Network</span></span>
* <span data-ttu-id="6a0d5-630">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-631">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-632">Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6a0d5-633">Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6a0d5-634">Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a0d5-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6a0d5-635">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="6a0d5-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6a0d5-636">Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="6a0d5-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6a0d5-637">Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6a0d5-638">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6a0d5-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6a0d5-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="6a0d5-640">Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6a0d5-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6a0d5-641">Correction de certains messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-641">Fix some error messages.</span></span>
* <span data-ttu-id="6a0d5-642">Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6a0d5-643">Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6a0d5-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6a0d5-644">Az.SignalR</span></span>
* <span data-ttu-id="6a0d5-645">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-646">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-647">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6a0d5-648">Mise à jour de la description du paramètre LicenseType avec les valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="6a0d5-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6a0d5-649">Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour</span><span class="sxs-lookup"><span data-stu-id="6a0d5-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6a0d5-650">Prise en charge du classement personnalisé sur l’instance gérée</span><span class="sxs-lookup"><span data-stu-id="6a0d5-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6a0d5-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-651">Az.Storage</span></span>
* <span data-ttu-id="6a0d5-652">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6a0d5-653">Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6a0d5-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6a0d5-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6a0d5-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6a0d5-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6a0d5-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6a0d5-656">Az.TrafficManager</span></span>
* <span data-ttu-id="6a0d5-657">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-658">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-659">Mettre à jour des URL d’aide en ligne incorrectes</span><span class="sxs-lookup"><span data-stu-id="6a0d5-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6a0d5-660">« New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6a0d5-661">« New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application</span><span class="sxs-lookup"><span data-stu-id="6a0d5-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6a0d5-662">1.1.0 - janvier 2019</span><span class="sxs-lookup"><span data-stu-id="6a0d5-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6a0d5-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-663">Az.Accounts</span></span>
* <span data-ttu-id="6a0d5-664">Ajouter l’étendue « Local » à Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6a0d5-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-665">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-666">Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6a0d5-667">Mise à jour de la description d’ID dans les fichiers d’aide</span><span class="sxs-lookup"><span data-stu-id="6a0d5-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6a0d5-668">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-670">Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6a0d5-671">Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone</span><span class="sxs-lookup"><span data-stu-id="6a0d5-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6a0d5-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6a0d5-672">Az.EventGrid</span></span>
* <span data-ttu-id="6a0d5-673">Mis à jour pour utiliser la version d’API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6a0d5-674">Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6a0d5-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6a0d5-675">New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6a0d5-676">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="6a0d5-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6a0d5-677">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="6a0d5-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6a0d5-678">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6a0d5-679">Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6a0d5-680">la durée de vie de l’événement,</span><span class="sxs-lookup"><span data-stu-id="6a0d5-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6a0d5-681">le nombre max de tentatives de livraison pour les événements,</span><span class="sxs-lookup"><span data-stu-id="6a0d5-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6a0d5-682">le point de terminaison de lettres mortes.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="6a0d5-683">Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6a0d5-684">Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6a0d5-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-685">Az.IotHub</span></span>
* <span data-ttu-id="6a0d5-686">Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub</span><span class="sxs-lookup"><span data-stu-id="6a0d5-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6a0d5-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6a0d5-687">Az.LogicApp</span></span>
* <span data-ttu-id="6a0d5-688">Get-AzLogicApp répertorie tout cela sans nom spécifié</span><span class="sxs-lookup"><span data-stu-id="6a0d5-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-689">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-690">Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6a0d5-691">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6a0d5-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6a0d5-692">Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a0d5-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6a0d5-693">Correction des fautes dans la documentation New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6a0d5-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6a0d5-694">Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6a0d5-695">Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6a0d5-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6a0d5-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6a0d5-696">Az.SignalR</span></span>
* <span data-ttu-id="6a0d5-697">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-698">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-699">Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6a0d5-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-700">Az.Storage</span></span>
* <span data-ttu-id="6a0d5-701">Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme</span><span class="sxs-lookup"><span data-stu-id="6a0d5-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6a0d5-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6a0d5-702">New-AzStorageContext</span></span>
* <span data-ttu-id="6a0d5-703">Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané</span><span class="sxs-lookup"><span data-stu-id="6a0d5-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6a0d5-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6a0d5-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-705">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-706">Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6a0d5-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6a0d5-707">Correction du problème de compatibilité descendante avec le module Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6a0d5-708">1.0.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6a0d5-709">Généralités</span><span class="sxs-lookup"><span data-stu-id="6a0d5-709">General</span></span>

- <span data-ttu-id="6a0d5-710">Disponibilité générale du module Az</span><span class="sxs-lookup"><span data-stu-id="6a0d5-710">General Availability of Az Module</span></span>
- <span data-ttu-id="6a0d5-711">Aide en ligne pour chaque module</span><span class="sxs-lookup"><span data-stu-id="6a0d5-711">Online help for each module</span></span>
- <span data-ttu-id="6a0d5-712">Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="6a0d5-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6a0d5-713">Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM</span><span class="sxs-lookup"><span data-stu-id="6a0d5-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6a0d5-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-714">Az.Accounts</span></span>
- <span data-ttu-id="6a0d5-715">Remplace Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="6a0d5-716">Formats de tableau fixe pour les types de profil et de contexte</span><span class="sxs-lookup"><span data-stu-id="6a0d5-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6a0d5-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-717">Az.ApiManagement</span></span>
- <span data-ttu-id="6a0d5-718">Correctifs pour #7002</span><span class="sxs-lookup"><span data-stu-id="6a0d5-718">Fixes for #7002</span></span>
- <span data-ttu-id="6a0d5-719">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6a0d5-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6a0d5-720">Az.Batch</span></span>
- <span data-ttu-id="6a0d5-721">Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6a0d5-722">La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6a0d5-723">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6a0d5-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6a0d5-724">Az.Billing</span></span>
- <span data-ttu-id="6a0d5-725">Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6a0d5-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-726">Az.CognitivServices</span></span>
- <span data-ttu-id="6a0d5-727">Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6a0d5-728">Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="6a0d5-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6a0d5-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="6a0d5-730">Ajout de la prise en charge de ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="6a0d5-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6a0d5-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6a0d5-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6a0d5-732">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="6a0d5-734">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6a0d5-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-735">Az.Monitor</span></span>
- <span data-ttu-id="6a0d5-736">Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6a0d5-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6a0d5-737">Az.KeyVault</span></span>
- <span data-ttu-id="6a0d5-738">Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie</span><span class="sxs-lookup"><span data-stu-id="6a0d5-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6a0d5-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6a0d5-739">Az.MachineLearning</span></span>
- <span data-ttu-id="6a0d5-740">Inclusion des cmdlets du module Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6a0d5-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6a0d5-741">Az.Media</span></span>
- <span data-ttu-id="6a0d5-742">Suppression des alias -Tags déconseillés de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="6a0d5-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6a0d5-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-743">Az.Network</span></span>
<span data-ttu-id="6a0d5-744">Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6a0d5-745">Ajout de nouvelles cmdlets :</span><span class="sxs-lookup"><span data-stu-id="6a0d5-745">New cmdlets added:</span></span>
        - <span data-ttu-id="6a0d5-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6a0d5-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6a0d5-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6a0d5-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6a0d5-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6a0d5-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6a0d5-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6a0d5-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a0d5-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6a0d5-754">Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6a0d5-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a0d5-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6a0d5-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6a0d5-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6a0d5-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6a0d5-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6a0d5-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6a0d5-760">New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6a0d5-761">Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6a0d5-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6a0d5-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6a0d5-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6a0d5-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6a0d5-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6a0d5-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6a0d5-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6a0d5-765">Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="6a0d5-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6a0d5-766">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6a0d5-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="6a0d5-768">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6a0d5-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-769">Az.Profile</span></span>
- <span data-ttu-id="6a0d5-770">Nom du module remplacé par Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6a0d5-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="6a0d5-772">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6a0d5-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-773">Az.Resources</span></span>
- <span data-ttu-id="6a0d5-774">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6a0d5-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="6a0d5-776">Prise en charge des certificats spécifiés par nom commun et empreinte</span><span class="sxs-lookup"><span data-stu-id="6a0d5-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6a0d5-777">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6a0d5-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6a0d5-778">Az.SIgnalR</span></span>
- <span data-ttu-id="6a0d5-779">Disponibilité générale des cmdlets PowerShell pour SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6a0d5-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6a0d5-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-780">Az.Sql</span></span>
- <span data-ttu-id="6a0d5-781">Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces</span><span class="sxs-lookup"><span data-stu-id="6a0d5-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6a0d5-782">Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL</span><span class="sxs-lookup"><span data-stu-id="6a0d5-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6a0d5-783">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6a0d5-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-784">Az.Storage</span></span>
- <span data-ttu-id="6a0d5-785">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6a0d5-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-786">Az.Websites</span></span>
- <span data-ttu-id="6a0d5-787">Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6a0d5-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6a0d5-788">0.7.0 - Décembre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6a0d5-789">Généralités</span><span class="sxs-lookup"><span data-stu-id="6a0d5-789">General</span></span>

* <span data-ttu-id="6a0d5-790">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="6a0d5-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6a0d5-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-791">Az.Compute</span></span>

* <span data-ttu-id="6a0d5-792">Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="6a0d5-794">Correction de la barre oblique de fin dans le domaine du compte ADLS</span><span class="sxs-lookup"><span data-stu-id="6a0d5-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6a0d5-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6a0d5-795">Az.FrontDoor</span></span>

* <span data-ttu-id="6a0d5-796">Correction de certains liens rompus</span><span class="sxs-lookup"><span data-stu-id="6a0d5-796">Fixed some broken links</span></span>
    - <span data-ttu-id="6a0d5-797">Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6a0d5-798">Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6a0d5-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="6a0d5-800">Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6a0d5-801">Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6a0d5-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-802">Az.Resources</span></span>

* <span data-ttu-id="6a0d5-803">Correctif pour https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6a0d5-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6a0d5-804">Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6a0d5-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-805">Az.Sql</span></span>

* <span data-ttu-id="6a0d5-806">Changements mineurs pour la future transition d’AzureRM vers Az</span><span class="sxs-lookup"><span data-stu-id="6a0d5-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6a0d5-807">Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet</span><span class="sxs-lookup"><span data-stu-id="6a0d5-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6a0d5-808">Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6a0d5-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-809">Az.Storage</span></span>

* <span data-ttu-id="6a0d5-810">Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6a0d5-811">Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext</span><span class="sxs-lookup"><span data-stu-id="6a0d5-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6a0d5-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6a0d5-813">Prise en charge de la configuration du site Web statique</span><span class="sxs-lookup"><span data-stu-id="6a0d5-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="6a0d5-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6a0d5-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6a0d5-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6a0d5-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6a0d5-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-816">Az.Websites</span></span>

* <span data-ttu-id="6a0d5-817">Set-AzureRmWebApp et Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6a0d5-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6a0d5-818">Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6a0d5-819">Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6a0d5-820">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6a0d5-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-821">Az.ApiManagement</span></span>
* <span data-ttu-id="6a0d5-822">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="6a0d5-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6a0d5-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6a0d5-823">Az.Automation</span></span>
* <span data-ttu-id="6a0d5-824">Cmdlets Azure Automation basées sur Swagger</span><span class="sxs-lookup"><span data-stu-id="6a0d5-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6a0d5-825">Ajout des cmdlets Update Management</span><span class="sxs-lookup"><span data-stu-id="6a0d5-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6a0d5-826">Ajout des cmdlets de contrôle de code source</span><span class="sxs-lookup"><span data-stu-id="6a0d5-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6a0d5-827">Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="6a0d5-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6a0d5-828">Correction de la commande de nœud d’inscription DSC</span><span class="sxs-lookup"><span data-stu-id="6a0d5-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6a0d5-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-829">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-830">Résolution du problème d’identité pour l’identité SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="6a0d5-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6a0d5-831">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="6a0d5-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6a0d5-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="6a0d5-833">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="6a0d5-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6a0d5-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6a0d5-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6a0d5-835">Mise à jour de la description d’exemples pour les cmdlets marketplace</span><span class="sxs-lookup"><span data-stu-id="6a0d5-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6a0d5-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-836">Az.Network</span></span>
* <span data-ttu-id="6a0d5-837">Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6a0d5-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6a0d5-838">Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0d5-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6a0d5-839">Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6a0d5-840">Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6a0d5-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6a0d5-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6a0d5-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6a0d5-842">Correction de la stratégie de modification pour un partage de fichiers protégé.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6a0d5-843">Conversion du fuseau horaire de stratégie en majuscules.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6a0d5-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6a0d5-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6a0d5-845">Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="6a0d5-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6a0d5-846">Mise à jour des dépendances pour le problème de mappage de types</span><span class="sxs-lookup"><span data-stu-id="6a0d5-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6a0d5-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6a0d5-847">Az.Relay</span></span>
* <span data-ttu-id="6a0d5-848">Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6a0d5-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-849">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-850">Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="6a0d5-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6a0d5-851">Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata</span><span class="sxs-lookup"><span data-stu-id="6a0d5-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6a0d5-852">Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6a0d5-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6a0d5-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="6a0d5-854">Ajout de messages d’obsolescence pour les changements cassants à venir</span><span class="sxs-lookup"><span data-stu-id="6a0d5-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6a0d5-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-855">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-856">Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database</span><span class="sxs-lookup"><span data-stu-id="6a0d5-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6a0d5-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6a0d5-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6a0d5-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6a0d5-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6a0d5-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6a0d5-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a0d5-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6a0d5-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a0d5-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6a0d5-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a0d5-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6a0d5-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6a0d5-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6a0d5-865">Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6a0d5-866">Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6a0d5-867">Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6a0d5-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6a0d5-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6a0d5-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6a0d5-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6a0d5-872">Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6a0d5-873">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6a0d5-874">Généralités</span><span class="sxs-lookup"><span data-stu-id="6a0d5-874">General</span></span>
* <span data-ttu-id="6a0d5-875">Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive</span><span class="sxs-lookup"><span data-stu-id="6a0d5-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6a0d5-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-876">Az.Profile</span></span>
* <span data-ttu-id="6a0d5-877">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0d5-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6a0d5-878">Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId</span><span class="sxs-lookup"><span data-stu-id="6a0d5-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6a0d5-879">Mise à jour de la description TenantId pour Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="6a0d5-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6a0d5-880">Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni</span><span class="sxs-lookup"><span data-stu-id="6a0d5-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6a0d5-881">Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement</span><span class="sxs-lookup"><span data-stu-id="6a0d5-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6a0d5-882">Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI</span><span class="sxs-lookup"><span data-stu-id="6a0d5-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6a0d5-883">Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion</span><span class="sxs-lookup"><span data-stu-id="6a0d5-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6a0d5-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="6a0d5-885">Ajout de l’opération Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-886">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-887">Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6a0d5-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6a0d5-888">Get-AzVMImage affiche AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6a0d5-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6a0d5-889">Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-891">Mise à jour du package DataLake vers la version 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6a0d5-892">Ajout de la valeur de concurrence par défaut aux opérations multithread.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6a0d5-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-893">Az.Insights</span></span>
* <span data-ttu-id="6a0d5-894">Correction du problème #7267 (zone de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="6a0d5-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6a0d5-895">Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).</span><span class="sxs-lookup"><span data-stu-id="6a0d5-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6a0d5-896">Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres</span><span class="sxs-lookup"><span data-stu-id="6a0d5-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6a0d5-897">À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté</span><span class="sxs-lookup"><span data-stu-id="6a0d5-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-898">Az.Network</span></span>
* <span data-ttu-id="6a0d5-899">Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -</span><span class="sxs-lookup"><span data-stu-id="6a0d5-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6a0d5-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6a0d5-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6a0d5-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6a0d5-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6a0d5-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6a0d5-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6a0d5-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6a0d5-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6a0d5-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6a0d5-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6a0d5-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6a0d5-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6a0d5-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6a0d5-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="6a0d5-907">Ajout des cmdlets de correction des stratégies</span><span class="sxs-lookup"><span data-stu-id="6a0d5-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-908">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-909">Correctif pour https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6a0d5-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6a0d5-910">Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6a0d5-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6a0d5-911">Az.ServiceBus</span></span>
* <span data-ttu-id="6a0d5-912">Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6a0d5-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a0d5-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="6a0d5-914">Correction de l’ajout de certificat au VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6a0d5-915">Correction de « Add-AzServiceFabricClusterCertificate »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6a0d5-916">Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="6a0d5-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6a0d5-917">Affichage correct des exceptions (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="6a0d5-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6a0d5-918">Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6a0d5-919">0.4.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6a0d5-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-920">Az.Profile</span></span>
* <span data-ttu-id="6a0d5-921">Problème résolu avec Get-AzSubscription dans CloudShell</span><span class="sxs-lookup"><span data-stu-id="6a0d5-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6a0d5-922">Mise à jour du code commun pour utiliser la dernière version de ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6a0d5-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-923">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-924">Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »</span><span class="sxs-lookup"><span data-stu-id="6a0d5-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6a0d5-925">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6a0d5-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a0d5-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="6a0d5-927">Ajout de la prise en charge des règles de réseau virtuel</span><span class="sxs-lookup"><span data-stu-id="6a0d5-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6a0d5-928">Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6a0d5-929">Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6a0d5-930">Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6a0d5-931">Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-932">Az.Network</span></span>
* <span data-ttu-id="6a0d5-933">Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6a0d5-934">Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-935">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-936">Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6a0d5-937">Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».</span><span class="sxs-lookup"><span data-stu-id="6a0d5-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6a0d5-938">0.3.0 - Octobre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6a0d5-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-939">Azure.Storage</span></span>
* <span data-ttu-id="6a0d5-940">Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="6a0d5-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6a0d5-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6a0d5-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6a0d5-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6a0d5-943">Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6a0d5-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6a0d5-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6a0d5-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6a0d5-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="6a0d5-946">Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6a0d5-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6a0d5-947">Az.Compute</span></span>
* <span data-ttu-id="6a0d5-948">Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin</span><span class="sxs-lookup"><span data-stu-id="6a0d5-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6a0d5-949">Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6a0d5-950">Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="6a0d5-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6a0d5-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6a0d5-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6a0d5-952">Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6a0d5-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6a0d5-953">Az.Network</span></span>
* <span data-ttu-id="6a0d5-954">Ajout de la fonctionnalité NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6a0d5-955">nouvelles cmdlets ajoutées</span><span class="sxs-lookup"><span data-stu-id="6a0d5-955">new cmdlets added</span></span>
    - <span data-ttu-id="6a0d5-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6a0d5-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6a0d5-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6a0d5-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6a0d5-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6a0d5-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6a0d5-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6a0d5-962">Ajout d’un lien d’association de service sur le modèle de sous-réseau</span><span class="sxs-lookup"><span data-stu-id="6a0d5-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6a0d5-963">Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="6a0d5-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6a0d5-964">Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="6a0d5-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6a0d5-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6a0d5-965">Az.RedisCache</span></span>
* <span data-ttu-id="6a0d5-966">Autorisez toutes les chaînes en tant que Paramètre de taille à progresser.</span><span class="sxs-lookup"><span data-stu-id="6a0d5-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6a0d5-967">Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="6a0d5-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6a0d5-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6a0d5-968">Az.Resources</span></span>
* <span data-ttu-id="6a0d5-969">Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6a0d5-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6a0d5-970">Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur</span><span class="sxs-lookup"><span data-stu-id="6a0d5-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6a0d5-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6a0d5-971">Az.Sql</span></span>
* <span data-ttu-id="6a0d5-972">Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel</span><span class="sxs-lookup"><span data-stu-id="6a0d5-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6a0d5-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6a0d5-973">Az.Websites</span></span>
* <span data-ttu-id="6a0d5-974">Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur</span><span class="sxs-lookup"><span data-stu-id="6a0d5-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6a0d5-975">Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows</span><span class="sxs-lookup"><span data-stu-id="6a0d5-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6a0d5-976">0.2.0 - Septembre 2018</span><span class="sxs-lookup"><span data-stu-id="6a0d5-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6a0d5-977">Version initiale</span><span class="sxs-lookup"><span data-stu-id="6a0d5-977">Initial Release</span></span>