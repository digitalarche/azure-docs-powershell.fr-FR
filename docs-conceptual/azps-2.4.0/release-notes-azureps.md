---
ms.openlocfilehash: ac8513b3eee4adfcaf0be8bf7b4e8d09190811df
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516638"
---
## <a name="240---july-2019"></a>2.4.0 - Juillet 2019
#### <a name="azaccounts"></a>Az.Accounts
* Ajout de la prise en charge des applets de commande de profil
* Ajout de la prise en charge des environnements et des plans de données dans les applets de commande générées
* Correction d’un bogue entraînant dans certains cas l’utilisation d’un point de terminaison incorrect pour les applets de commande de plan de données dans Windows PowerShell

#### <a name="azadvisor"></a>Az.Advisor
* Mise à la disposition générale de Az.Advisor
* Ce module est désormais inclus dans le cadre du module `Az` de cumul

#### <a name="azapimanagement"></a>Az.ApiManagement
* Corriger le problème https://github.com/Azure/azure-powershell/issues/8671
    - **Get-AzApiManagementSubscription**
        - Ajout de la prise en charge pour interroger les abonnements par utilisateur et par produit
        - Ajout de la prise en charge pour interroger en utilisant la portée « / », « /apis », « /apis/echo-api »
* Correction des problèmes https://github.com/Azure/azure-powershell/issues/9307 et https://github.com/Azure/azure-powershell/issues/8432
    - **Import-AzApiManagementApi**
        - Ajout de la prise en charge pour spécifier « ApiVersion » et « ApiVersionSetId » lors de l’importation d’API

#### <a name="azautomation"></a>Az.Automation
* Correction d’un bogue lié à la gestion des valeurs de chaîne par l’applet de commande Set-AzAutomationConnectionFieldValue.

#### <a name="azcompute"></a>Az.Compute
* Ajout du paramètre HyperVGeneration à New-AzImageConfig

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour de la sortie de plusieurs applets de commande ADF (obtention des exécutions d’activités, obtention des exécutions de pipeline et obtention des exécutions de déclencheur) pour prendre en charge le canal Select-Object.

#### <a name="azeventgrid"></a>Az.EventGrid
* Correction d’une faute de frappe dans la documentation sur « New-AzEventGridSubscription »

#### <a name="aziothub"></a>Az.IotHub
* Ajout de la prise en charge pour régénérer les clés de stratégie d’autorisation.

#### <a name="aznetwork"></a>Az.Network
* Ajout de « RoutingPreference » aux étiquettes d’adresses IP publiques
* Amélioration des exemples dans la documentation de référence sur « Get-AzNetworkServiceTag »

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Correction d’un problème de référence null dans Get-AzPolicyEvent
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9446

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Correction du modèle de source de données CustomLog retourné dans Get-AzOperationalInsightsDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Correction de la commande get-policy pour IaaSVMs

#### <a name="azresources"></a>Az.Resources
    - Correction du texte d’aide pour le paramètre -Top de Get-AzPolicyState
    - Ajout de la prise en charge de la pagination côté client pour Get-AzPolicyAlias
    - Ajout de nouveaux paramètres pour Set-AzPolicyAssignment, -PolicyParameters et -PolicyParametersObject
    - Mise à jour des documents et des exemples pour les applets de commande de stratégie

#### <a name="azservicebus"></a>Az.ServiceBus
* Correction du problème #4938 : New-AzureRmServiceBusQueue retourne BadRequest lors de la définition de MaxSizeInMegabytes

#### <a name="azsql"></a>Az.Sql
* Ajout d’applets de commande de groupe de basculement d’instances en préversion à la version publique
* Prise en charge de l’audit de serveurs/bases de données SQL Azure avec de nouvelles applets de commande.
    - Set-AzSqlServerAudit
    - Get-AzSqlServerAudit
    - Remove-AzSqlServerAudit
    - Set-AzSqlDatabaseAudit
    - Get-AzSqlDatabaseAudit
    - Remove-AzSqlDatabaseAudit
* Suppression des contraintes liées aux e-mails des paramètres d’évaluation des vulnérabilités

#### <a name="azstorage"></a>Az.Storage
* Les 2 paramètres obligatoires « -IndexDocument » et « -ErrorDocument404Path » sont désormais facultatifs dans l’applet de commande :
    -  Enable-AzStorageStaticWebsite
* Mise à jour de l’aide de Get-AzStorageBlobContent avec ajout d’un exemple
* Affichage d’informations supplémentaires sur l’erreur en cas d’échec de l’applet de commande avec StorageException
* Prise en charge de la création ou de la mise à jour du compte de stockage avec l’authentification AAD DS Azure Files
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Prise en charge de l’énumération ou de la fermeture des handles de fichier d’un partage de fichiers, d’un répertoire de fichiers ou d’un fichier
    - Get-AzStorageFileHandle
    - Close-AzStorageFileHandle

#### <a name="azstoragesync"></a>Az.StorageSync
* Ce module est désormais inclus dans le cadre du module `Az` de cumul

## <a name="232---june-2019"></a>2.3.2 - Juin 2019
#### <a name="azaccounts"></a>Az.Accounts
* Correction d’un bogue lié à l’utilisation, dans certains cas, d’une URL incorrecte pour les appels de fonctions
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8983
* Correction d’un problème lié aux alias d’AzureRM aux applets de commande Az
  - Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic
  - Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest

#### <a name="azcompute"></a>Az.Compute
* Les jeux de paramètres simples New-AzVm et New-AzVmss acceptent désormais le paramètre « ProximityPlacementGroup ».
* Correction d’une faute de frappe dans la documentation de référence de « New-AzVM »

#### <a name="azdns"></a>Az.Dns
* Correction d’une faute de frappe dans les exemples d’aide « Set-AzDnsZone ».

#### <a name="azeventgrid"></a>Az.EventGrid
* Mis à jour effectuée pour utiliser la version d’API 2019-06-01.
* Nouvelles applets de commande :
    - New-AzureRmEventGridDomain
        - Crée un domaine Azure Event Grid.
    - Get-AzureRmEventGridDomain
        - Obtient les détails d’un domaine Event Grid ou la liste de tous les domaines Event Grid dans l’abonnement Azure actuel.
    - Remove-AzureRmEventGridDomain
        - Supprime un domaine Azure Event Grid.
    - New-AzureRmEventGridDomainKey
        - Regénère la clé d’accès partagé pour un domaine Azure Event Grid.
    - Get-AzureRmEventGridDomainKey
        - Obtient les clés d’accès partagé utilisées pour publier des événements sur un domaine Event Grid.
    - New-AzureRmEventGridDomainTopic
        - Crée une rubrique de domaine Event Grid.
    - Get-AzureRmEventGridDomainTopic
        - Obtient les détails d’une rubrique de domaine Event Grid ou la liste de toutes les rubriques de domaine Event Grid sous un domaine Event Grid spécifique dans l’abonnement Azure actuel. 
    - Remove-AzureRmEventGridDomainTopic
        - Supprime une rubrique de domaine Azure Event Grid existante.
* Cmdlets mises à jour :
    - New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription
        - Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les nouveaux domaines Event Grid et les nouvelles rubriques de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.
        - Ajout de nouveaux paramètres obligatoires afin de spécifier les nouveaux noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la création d’un abonnement aux événements sous ces ressources.
        - Ajout de nouveaux jeux de paramètres pour les domaines et les rubriques de domaine afin de permettre la réutilisation de paramètres existants (par exemple, EndPointType, SubjectBeginsWith, etc.).
        - Ajoutez les nouveaux paramètres facultatifs pour spécifier :
            - Date d’expiration de l’abonnement aux événements
            - Paramètres de filtrage avancé
        - Ajout d’un nouvel enum pour servicebusqueue comme destination.
        - Interdiction de l’utilisation de « All » dans l’option -IncludedEventType et remplacement par 
    - Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription :
        - Ajout de nouveaux paramètres facultatifs (Top, ODataQuery et NextLink) pour prendre en charge le filtrage et la pagination des résultats.
    - Remove-AzureRmEventGridSubscription
        - Ajout de nouveaux paramètres obligatoires afin de prendre en charge l’utilisation du pipe avec les domaines Event Grid et les rubriques de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.
        - Ajout de nouveaux paramètres obligatoires afin de spécifier les noms de domaine Event Grid et/ou de rubrique de domaine Event Grid pour permettre la suppression d’un abonnement aux événements existant sous ces ressources.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* New-AzFrontDoorWafMatchConditionObject
    - Ajout de la prise en charge des transformations et d’une nouvelle valeur de saisie automatique d’opérateur (RegEx)
* New-AzFrontDoorWafManagedRuleObject
    - Ajout de nouvelles valeurs de saisie semi-automatique

#### <a name="aznetwork"></a>Az.Network
* Ajout de la prise en charge de la ressource de la passerelle de réseau virtuel
    - Nouvelles applets de commande
        - Get-AzVirtualNetworkGatewayVpnClientConnectionHealth
* Ajout d’AvailablePrivateEndpointType
    - Nouvelles applets de commande 
        - Get-AzAvailablePrivateEndpointType
* Ajout de PrivatePrivateLinkService
    - Nouvelles applets de commande 
        - Get-AzPrivateLinkService 
        - New-AzPrivateLinkService
        - Remove-AzPrivateLinkService
        - New-AzPrivateLinkServiceIpConfig
        - Set-AzPrivateEndpointConnection
* Ajout de PrivateEndpoint
    - Nouvelles applets de commande
        - Get-AzPrivateEndpoint
        - New-AzPrivateEndpoint
        - Remove-AzPrivateEndpoint
        - New-AzPrivateLinkServiceConnection
* Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur UseLocalAzureIpAddress sur VpnConnection
    - Mise à jour de New-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.
    - Mise à jour de Set-AzVpnConnection : Ajout du paramètre facultatif -UseLocalAzureIpAddress pour indiquer que l’adresse IP Azure locale doit être utilisée comme adresse source lors de l’établissement d’une connexion.
* Ajout du champ en lecture seule PeeredConnections dans le peering ExpressRoute.
* Ajout du champ en lecture seule GlobalReachEnabled dans ExpressRoute.
* Ajout d’un attribut de changement cassant pour indiquer la dépréciation du champ AllowGlobalReach dans le modèle ExpressRouteCircuit
* Correction de l’erreur 8756 liée à l’utilisation de TargetListenerID avec les applets de commande AzApplicationGatewayRedirectConfiguration
* Correction d’un bogue dans New-AzApplicationGatewayPathRuleConfig empêchant la définition de l’ensemble de règles de réécriture.
* Correction de l’affichage de VirtualNetworkTaps dans NetworkInterfaceIpConfiguration
* Correction des applets de commande Cortex Get pour lister toutes les parties
* Correction de la création de références VirtualHub pour ExpressRouteGateways, VpnGateway
* Ajout de la prise en charge des zones de disponibilité dans AzureFirewall et NatGateway
* Ajout de l’applet de commande Get-AzNetworkServiceTag
* Ajout de la prise en charge de plusieurs adresses IP publiques pour le Pare-feu Azure
    - Mise à jour de l’applet de commande New-AzFirewall :
        - Ajout du paramètre -PublicIpAddress qui accepte un ou plusieurs objets d’adresse IP publique
        - Ajout du paramètre -VirtualNetwork qui accepte un objet de réseau virtuel
        - Ajout des méthodes AddPublicIpAddress et RemovePublicIpAddress sur l’objet de pare-feu (ces méthodes acceptent un objet d’adresse IP publique comme entrée)
        - Dépréciation des paramètres -PublicIpName et -VirtualNetworkName 
* Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définition des options d’authentification AAD VpnClient sur la ressource de la passerelle de réseau virtuel. 
    - Mise à jour de New-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.
    - Mise à jour de Set-AzVirtualNetworkGateway : Ajout des paramètres facultatifs AadTenantUri, AadAudienceId et AadIssuerUri permettant de définir des options d’authentification AAD VpnClient sur la passerelle.
    - Mise à jour de Set-AzVirtualNetworkGateway : Ajout du paramètre booléen facultatif RemoveAadAuthentication pour supprimer les options d’authentification AAD VpnClient de la passerelle.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Activation du niveau tarifaire **pergb2018** dans la commande « New-AzureRmOperationalInsightsWorkspace »

#### <a name="azresources"></a>Az.Resources
* Prise en charge d’autres options d’exportation de modèle
    - Ajout du paramètre « -SkipResourceNameParameterization » à Export-AzResourceGroup
    - Ajout du paramètre « -SkipAllParameterization » à Export-AzResourceGroup
    - Ajout du paramètre «-Resource » à Export-AzResourceGroup pour le filtrage des ressources exportées

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correction d’un problème entraînant dans certains cas l’obtention d’une empreinte numérique incorrecte lors de l’ajout du certificat ByExistingKeyVault

#### <a name="azsql"></a>Az.Sql
* Correction du suffixe du point de terminaison de stockage Advanced Threat Protection
* Correction de la stratégie Advanced Threat Protection autorisant le remplacement des paramètres Advanced Data Security
* Ajout de nouvelles applets de commande à Management.Sql pour permettre aux clients d’ajouter des clés TDE et de définir le protecteur TDE pour les instances managées
   - Add-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceKeyVaultKey
   - Remove-AzSqlInstanceKeyVaultKey
   - Get-AzSqlInstanceTransparentDataEncryptionProtector
   - Set-AzSqlInstanceTransparentDataEncryptionProtector

#### <a name="azstorage"></a>Az.Storage
* Prise en charge des genres FileStorage et SkuName (Premium_ZRS) lors de la création d’un compte de stockage
    - New-AzStorageAccount
* Clarification de la description de l’applet de commande d’immuabilité des objets blob
    -  Remove-AzRmStorageContainerImmutabilityPolicy

#### <a name="azwebsites"></a>Az.Websites
* Optimisation de Get-AzWebAppCertificate pour filtrer par groupe de ressources sur le serveur au lieu du client
* Ajoute un paramètre booléen -UseDisasterRecovery à Get-AzWebAppSnapshot

## <a name="220---june-2019"></a>2.2.0 - Juin 2019
#### <a name="azcdn"></a>Az.Cdn
* Mise à jour des applets de commande pour prendre en charge la fonctionnalité rulesEngine basée sur la version de l’API du 15-04-2019.

#### <a name="azcompute"></a>Az.Compute
* Le paramètre `NoWait` a été ajouté : il démarre l’opération et retourne immédiatement, avant la fin de l’opération.
    - Cmdlets mises à jour :   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM

#### <a name="azeventhub"></a>Az.EventHub
* Correction pour #9231 - Get-AzEventHubNamespace ne retourne pas d’étiquettes
* Correction pour #9230 - Get-AzEventHubNamespace retourne ResourceGroup au lieu de ResourceGroupName

#### <a name="aznetwork"></a>Az.Network
* Mise à jour de ResourceId et de InputObject pour Nat Gateway
    - Ajout d’un alias pour ResourceId et InputObject

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Correction du problème de la référence null dans Get-AzPolicyEvent

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Conservation minimale de la stratégie IaaSVM en jours passée de 1 à 7

#### <a name="azservicebus"></a>Az.ServiceBus
* Correction pour #9182 - Get-AzServiceBusNamespace retourne ResourceGroup au lieu de ResourceGroupName

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correction de la faute de frappe dans le message d’erreur pour « Update-AzServiceFabricReliability »
* Correction pour le caractère manquant dans les lignes de commande de Service Fabric

#### <a name="azsql"></a>Az.Sql
* Ajout d’un paramètre DnsZonePartner pour l’applet de commande New-AzureSqlInstance pour prendre en charge AutoDr pour Managed Instance.
* Dépréciation de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy
* Renommage des applets de commande « Threat Detection » en « Advanced Threat Protection »
* Les paramètres New-AzSqlInstance -StorageSizeInGB et -LicenseType sont désormais facultatifs.

#### <a name="azwebsites"></a>Az.Websites
* Correction du problème où l’utilisation de Set-AzWebApp et de Set-AzWebAppSlot avec la propriété -WebApp supprimait les étiquettes

## <a name="210---may-2019"></a>2.1.0 - Mai 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Création d’applets de commande pour la gestion des diagnostics au niveau de l’étendue globale et de l’API
    - **Get-AzApiManagementDiagnostic** - Obtenir les diagnostics configurés au niveau de l’étendue globale ou de l’API
    - **New-AzApiManagementDiagnostic** - Créer des diagnostics au niveau de l’étendue globale ou de l’API
    - **New-AzApiManagementHttpMessageDiagnostic** - Créer un paramètre de diagnostic pour indiquer quelles en-têtes journaliser et la taille en octets du corps
    - **New-AzApiManagementPipelineDiagnosticSetting** - Créer des paramètres de diagnostic pour les messages HTTP entrants/sortants échangés avec la passerelle.
    - **New-AzApiManagementSamplingSetting** - Créer un paramètre d’échantillonnage pour les demandes/réponses d’un diagnostic
    - **Remove-AzApiManagementDiagnostic** - Supprimer une entité de diagnostic au niveau de l’étendue globale ou de l’API
    - **Set-AzApiManagementDiagnostic** - Mettre à jour une entité de diagnostic au niveau de l’étendue globale ou de l’API
* Création d’applets de commande pour la gestion du cache dans le service Gestion des API
    - **Get-AzApiManagementCache** - Obtenir les détails du cache spécifié par son identificateur ou de tous les caches
    - **New-AzApiManagementCache** - Créer un cache « par défaut » ou un cache dans une « région » Azure particulière
    - **Remove-AzApiManagementCache** - Supprimer un cache
    - **Update-AzApiManagementCache** - Mettre à jour un cache
* Création d’applets de commande pour la gestion du schéma des API
    - **New-AzApiManagementSchema** - Créer un schéma pour une API
    - **Get-AzApiManagementSchema** - Obtenir les schémas configurés dans l’API
    - **Remove-AzApiManagementSchema** - Supprimer le schéma configuré dans l’API
    - **Set-AzApiManagementSchema** - Mettre à jour le schéma configuré dans l’API
* Création d’une applet de commande pour générer un jeton utilisateur. 
    - **New-AzApiManagementUserToken** - Générer un nouveau jeton utilisateur valide pour 8 heures par défaut. Un jeton pour l’utilisateur « GIT » peut être généré avec cette applet de commande./
* Création d’une applet de commande pour la récupération de l’état du réseau
    - **Get-AzApiManagementNetworkStatus** - Obtenir l’état de la connectivité réseau des ressources dont dépend le service Gestion des API. Ceci est utile lors du déploiement du service Gestion des API dans un réseau virtuel et pour vérifier si des dépendances sont rompues.
* Mise à jour de l’applet de commande **New-AzApiManagement** pour gérer le service Gestion des API 
    - Ajout de la prise en charge de la nouvelle référence SKU « Consommation »
    - Ajout de la prise en charge pour activer l’indicateur « EnableClientCertificate » pour la référence SKU « Consommation »
    - La nouvelle applet de commande **New-AzApiManagementSslSetting** permet de configurer le paramètre « TLS/SSL » sur le « Back-end » et sur le « Front-end ». Ceci peut également être utilisé pour configurer « Ciphers » (comme « 3DES ») et « ServerProtocols » (comme « Http2 ») sur le « Front-end » d’un service Gestion des API.
    - Ajout de la prise en charge de la configuration du nom d’hôte « DeveloperPortal » sur le service Gestion des API.
* Mise à jour des applets de commande **Get-AzApiManagementSsoToken** pour prendre un objet « PsApiManagement » comme entrée
* Mise à jour de l’applet de commande pour afficher les messages d’erreur inline 
     > PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Code d’erreur : Message d’erreur de ValidationError : Un ou plusieurs champs contiennent des valeurs incorrectes : Error Details:    [Code=ValidationError, Message=Erreur dans l’élément « log-to-eventhub » ligne 3, colonne 10 : Enregistreur d’événements introuvable, Cible=log-to-eventhub]
* Mise à jour de l’applet de commande **Export-AzApiManagementApi** pour exporter des API au format « OpenApi 3.0 »
* Mise à jour de l’applet de commande **Import-AzApiManagementApi**
    - Pour importer des API depuis la spécification de document « OpenApi 3.0 »
    - Pour remplacer la propriété « PsApiManagementSchema » spécifiée dans un document (« Swagger », « Wadl », « Wsdl », « OpenApi »).
    - Pour remplacer la propriété « ServiceUrl » spécifiée dans un document.
* Mise à jour de l’applet de commande **Get-AzApiManagementPolicy** pour retourner la stratégie au « format » avec échappement non-XML en utilisant « rawxml »
* Mise à jour de l’applet de commande **Set-AzApiManagementPolicy** pour accepter la stratégie au « format » avec échappement non-XML en utilisant « rawxml » et avec échappement XML en utilisant « xml »
* Mise à jour de l’applet de commande **New-AzApiManagementApi** 
    - Pour configurer une API avec le serveur d’autorisation « OpenId ».
    - Pour créer une API dans un « ApiVersionSet »
    - Pour cloner une API à l’aide de « SourceApiId » et « SourceApiRevision ».
    - Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API. 
* Mise à jour de l’applet de commande **Set-AzApiManagementApi**
    - Pour configurer une API avec le serveur d’autorisation « OpenId ».
    - Pour mettre à jour une API dans un « ApiVersionSet »    
    - Possibilité de configurer « SubscriptionRequired » au niveau de l’étendue de l’API. 
* Mise à jour de l’applet de commande **New-AzApiManagementRevision**
    - Pour cloner (copier les étiquettes, les produits, les opérations et les stratégies) une révision existante à l’aide de « SourceApiRevision ». La nouvelle révision fait une supposition pour le « ApiId » du parent.
    - Pour fournir une « ApiRevisionDescription »
    - Pour remplacer le « ServiceUrl » lors du clonage d’une API.
* Mise à jour de l’applet de commande **New-AzApiManagementIdentityProvider**
    - Pour configurer « AAD » ou « AADB2C » avec une « Authority »
    - Pour configurer « SignupPolicy », « SigninPolicy », « ProfileEditingPolicy » et « PasswordResetPolicy »
* Mise à jour de l’applet de commande **New-AzApiManagementSubscription**
    - Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »
    - Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »
    - Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.
* Mise à jour de l’applet de commande **Set-AzApiManagementSubscription**
    - Pour prendre en compte le nouveau modèle d’abonnement avec « Scope » et « UserId »
    - Pour prendre en compte l’ancien modèle d’abonnement avec « ProductId » et « UserId »
    - Ajout de la prise en charge de l’activation de « AllowTracing » au niveau de l’abonnement.
* Mise à jour des applets de commande suivantes pour accepter « ResourceId » comme entrée
    - « New-AzApiManagementContext »
        > New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso
    - « Get-AzApiManagementApiRelease »
        > Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId
    - « Get-AzApiManagementApiVersionSet »
        > Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset
    - « Get-AzApiManagementAuthorizationServer »
    - « Get-AzApiManagementBackend »
        > Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric
    - « Get-AzApiManagementCertificate » 
    - « Remove-AzApiManagementApiVersionSet »
    - « Remove-AzApiManagementSubscription »

#### <a name="azautomation"></a>Az.Automation
* Mise à jour de Get-AzAutomationJobOutputRecord pour gérer les valeurs des enregistrements JSON et Texte.
    - Corriger le problème https://github.com/Azure/azure-powershell/issues/7977
    - Corriger le problème https://github.com/Azure/azure-powershell/issues/8600
* Modification du comportement de Start-AzAutomationDscCompilationJob pour simplement démarrer le travail au lieu d’attendre son achèvement.
    * Corriger le problème https://github.com/Azure/azure-powershell/issues/8347
* Correction de Get-AzAutomationDscNode quand l’utilisation de -Name retourne tous les nœuds. Elle retourne désormais seulement le nœud correspondant.

#### <a name="azcompute"></a>Az.Compute
* Ajout des paramètres ProtectFromScaleIn et ProtectFromScaleSetAction à l’applet de commande Update-AzVmssVM.
* Le jeu de paramètres wimple de New-AzVM utilise désormais par défaut un emplacement disponible si « USA Est » n’est pas pris en charge.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Mise à jour du SDK ADLS pour utiliser httpclient, et pour intégrer le test du plan de données avec l’infrastructure Azure

#### <a name="azmonitor"></a>Az.Monitor
* Correction des noms de paramètres incorrects dans les exemples d’aide

#### <a name="aznetwork"></a>Az.Network
* Ajout d’un indicateur DisableBgpRoutePropagation à la sortie de la table des routes effectives
    - Mise à jour de l’applet de commande :
        - Get-AzEffectiveRouteTable
* Correction du tiret double dans la documentation de New-AzApplicationGatewayTrustedRootCertificate

#### <a name="azresources"></a>Az.Resources
* Ajout de la nouvelle applet de commande Get-AzureRmDenyAssignment pour la récupération des affectations de refus

#### <a name="azsql"></a>Az.Sql
* Renommage des applets de commande Advanced Threat Protection en Advanced Data Security, et activation par défaut de l’évaluation des vulnérabilités

## <a name="200---may-2019"></a>2.0.0 - Mai 2019
#### <a name="azaccounts"></a>Az.Accounts
* Mise à jour de la bibliothèque d’authentification pour résoudre les problèmes ADFS liés à l’authentification par nom d’utilisateur/mot de passe

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Clauses d’exclusion Bing uniquement affichées pour les services Recherche Bing.
* Amélioration de l’erreur en cas d’échec de la création d’un compte.

#### <a name="azcompute"></a>Az.Compute
* Fonctionnalité de groupe de placements de proximité.
    - Les nouvelles applets de commande suivantes sont ajoutées :   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup
    - Le nouveau paramètre, ProximityPlacementGroupId, est ajouté aux applets de commande suivantes :   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig
* Le paramètre StorageAccountType est ajouté à New-AzGalleryImageVersion.
* TargetRegion de New-AzGalleryImageVersion peut contenir StorageAccountType.
* Le paramètre de commutateur SkipShutdown est ajouté à Stop-AzVM et à Stop-AzVmss       
* Dernières modifications
    - Set-AzVMBootDiagnostics est remplacé par Set-AzVMBootDiagnostic.
    - Export-AzLogAnalyticThrottledRequests est remplacé par Export-AzLogAnalyticThrottledRequests.

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Première version en disponibilité générale des applets de commande Azure Deployment Manager

#### <a name="azdns"></a>Az.Dns
* Délégation de serveur de noms DNS automatique
    - L’applet de commande de création d’une zone DNS accepte un nom de zone parent en tant que paramètre facultatif supplémentaire.
    - Ajoute des enregistrements NS dans la zone parente pour la zone enfant nouvellement créée.

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Première version en disponibilité générale des applets de commande Azure FrontDoor
* Renommage des applets de commande WAF pour inclure « Waf »
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a>Az.HDInsight
* Suppression de deux applets de commande :
    - Grant-AzHDInsightHttpServicesAccess
    - Revoke-AzHDInsightHttpServicesAccess
* Ajout d’une nouvelle applet de commande Set-AzHDInsightGatewayCredential pour remplacer Grant-AzHDInsightHttpServicesAccess
* Mise à jour de l’applet de commande Get-AzHDInsightJobOutput pour faire la distinction entre le rôle de lecteur et le rôle d’opérateur hdinsight :
    - Les utilisateurs avec le rôle de lecteur doivent spécifier explicitement le paramètre « DefaultStorageAccountKey » ; sinon, une erreur se produit.
    - Les utilisateurs avec le rôle d’opérateur hdinsight ne sont pas affectés.

#### <a name="azmonitor"></a>Az.Monitor
* Nouvelles applets de commande pour l’API SQR (Scheduled Query Rule)  
    - New-AzScheduledQueryRuleAlertingAction
    - New-AzScheduledQueryRuleAznsActionGroup
    - New-AzScheduledQueryRuleLogMetricTrigger
    - New-AzScheduledQueryRuleSchedule
    - New-AzScheduledQueryRuleSource
    - New-AzScheduledQueryRuleTriggerCondition
    - New-AzScheduledQueryRule
    - Get-AzScheduledQueryRule
    - Set-AzScheduledQueryRule
    - Update-AzScheduledQueryRule
    - Remove-AzScheduledQueryRule
    - [Plus d’informations](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) sur l’API SQR
    - Mise à jour d’Az.Monitor.md de manière à inclure des applets de commande pour la règle d’alerte basée sur des métriques GenV2 (non classique)

#### <a name="aznetwork"></a>Az.Network
* Ajout de la prise en charge de la ressource NAT Gateway
    - Nouvelles applets de commande
        - New-AzNatGateway
        - Get-AzNatGateway
        - Set-AzNatGateway
        - Remove-AzNatGateway
   - Applets de commande mises à jour
        - New-AzureVirtualNetworkSubnetConfigCommand
        - Add-AzureVirtualNetworkSubnetConfigCommand
* Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Définir/supprimer des routes personnalisées sur la passerelle Brooklyn.
    - Mise à jour de New-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.
    - Mise à jour de Set-AzVirtualNetworkGateway : ajout du paramètre facultatif -CustomRoute pour définir les préfixes d’adresse en tant que routes personnalisées sur la passerelle.

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Prise en charge de l’interrogation des détails d’évaluation de la stratégie.
    - Ajout du paramètre « -Expand » à Get-AzPolicyState. Prise en charge de « -Expand PolicyEvaluationDetails ».

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Prise en charge de la récupération de site Azure vers Azure entre abonnements.
* Marquage des changements cassants à venir pour Azure Site Recovery.
* Correction du plan d’action de fin pour un plan de récupération Azure Site Recovery.
* Correction de la mise à jour du mappage réseau Azure vers Azure dans Azure Site Recovery.
* Correction de la mise à jour de la direction de la protection Azure vers Azure dans Azure Site Recovery pour un disque managé.
* Autres correctifs mineurs.

#### <a name="azrelay"></a>Az.Relay
* Correction des fautes de frappe dans les messages destinés aux clients

#### <a name="azservicebus"></a>Az.ServiceBus
* Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace

#### <a name="azstorage"></a>Az.Storage
* Mise à niveau de la bibliothèque de client de stockage 10.0.1 (l’espace de noms de tous les objets de ce SDK passe de « Microsoft.WindowsAzure.Storage.  *» à « Microsoft.Azure.Storage.*  »)
* Mise à niveau vers Microsoft.Azure.Management.Storage 11.0.0 pour prendre en charge la nouvelle version d’API 2019-04-01.
* La propriété Kind du compte de stockage par défaut dans Créer un compte de stockage passe de « Storage » à « StorageV2 »
    - New-AzStorageAccount
* Changement apporté au Sku.Name en sortie de l’applet de commande du compte de stockage pour l’aligner sur le SkuName en entrée avec « - ». Par exemple : « StandardLRS » remplacé par « Standard_LRS »
    - New-AzStorageAccount
    - Get-AzStorageAccount
    - Set-AzStorageAccount

#### <a name="azwebsites"></a>Az.Websites
* Propriété « Kind » désormais définie pour les objets PSSite retournés par Get-AzWebApp
* Get-AzWebApp*Metrics et Get-AzAppServicePlanMetrics marqués comme dépréciés

## <a name="180---april-2019"></a>1.8.0 - Avril 2019
### <a name="highlights-since-the-last-major-release"></a>Points importants depuis la dernière version majeure
* Disponibilité générale du module `Az`
* Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce
* Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
* Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network
* Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement
* Ajout de la prise en charge des runbooks Python 2 dans Az.Automation
* Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration

#### <a name="azaccounts"></a>Az.Accounts
* Mise à jour de Uninstall-AzureRm pour supprimer correctement les modules dans Mac

#### <a name="azbatch"></a>Az.Batch
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azcdn"></a>Az.Cdn
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azcompute"></a>Az.Compute
* Résolution du problème d’installation d’AEM si les ID de ressource des disques avaient des groupes de ressources en minuscules dans l’ID de ressource
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.
* Correction de la documentation des caractères génériques

#### <a name="azdatafactory"></a>Az.DataFactory
* Ajout de SsisProperties si NodeCount n’est pas null pour le runtime d’intégration managé.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azeventgrid"></a>Az.EventGrid
* Mise à jour du texte d’aide du point de terminaison pour indiquer que les ressources doivent être créées avant d’utiliser les applets de commande de création/mise à jour d’abonnements à des événements.

#### <a name="azeventhub"></a>Az.EventHub
* Ajout de nouvelles applets de commande pour le NetworkRuleSet de Namespace 

#### <a name="azhdinsight"></a>Az.HDInsight
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="aziothub"></a>Az.IotHub
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azkeyvault"></a>Az.KeyVault
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.
* Correction de la documentation des caractères génériques

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azmedia"></a>Az.Media
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azmonitor"></a>Az.Monitor
  * Nouvelles applets de commande pour la règle d’alerte basée sur des métriques (non classique) GenV2
      - New-AzMetricAlertRuleV2DimensionSelection
      - New-AzMetricAlertRuleV2Criteria
      - Remove-AzMetricAlertRuleV2
      - Get-AzMetricAlertRuleV2
      - Add-AzMetricAlertRuleV2
  * Mise à jour du kit SDK Monitor avec la version 0.22.0-preview

#### <a name="aznetwork"></a>Az.Network
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.
* Correction de la documentation des caractères génériques

#### <a name="aznotificationhubs"></a>Az.NotificationHubs
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azpowerbiembedded"></a>Az.PowerBIEmbedded
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.
* Mise à jour du format de table pour SQL dans azure VM
* Ajout d’une autre méthode pour récupérer l’emplacement dans AzureFileShare
* Mise à jour de ScheduleRunDays dans l’objet SchedulePolicy en fonction du fuseau horaire

#### <a name="azrediscache"></a>Az.RedisCache
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.

#### <a name="azresources"></a>Az.Resources
* Correction de la documentation des caractères génériques

#### <a name="azsql"></a>Az.Sql
* Remplacement de la dépendance sur le kit SDK Monitor par du code courant
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.
* Amélioration du processus de classification de plusieurs colonnes.
* Ajout de propriétés de référence SKU (nom, famille et capacité de la référence sku) en réponse à Get-AzSqlServerServiceObjective et mise au format table par défaut.
* Possibilité d’utiliser Get-AzSqlServerServiceObjective par emplacement sans avoir besoin d’un serveur préexistant dans la région.
* Prise en charge du paramètre de fuseau horaire dans la création d’instances managées.
* Correction de la documentation des caractères génériques

#### <a name="azwebsites"></a>Az.Websites
* Correction de Set-AzWebApp et Set-AzWebAppSlot pour ne plus supprimer les balises lors de l’exécution
* Mise à jour des applets de commande au pluriel avec des noms au singulier et dépréciation des noms au pluriel.
* Mise à jour du kit SDK WebSites.
* Suppression de la propriété AdminSiteName de PSAppServicePlan.

## <a name="170---april-2019"></a>1.7.0 - Avril 2019
### <a name="highlights-since-the-last-major-release"></a>Points importants depuis la dernière version majeure
* Disponibilité générale du module `Az`
* Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce
* Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
* Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network
* Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement
* Ajout de la prise en charge des runbooks Python 2 dans Az.Automation
* Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration

#### <a name="azaccounts"></a>Az.Accounts
* Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter le paramètre AzureAnalysisServicesEndpointResourceId

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Utilisation de ServiceClient dans les applets de commande dataplane et suppression de la logique d’authentification d’origine
* Faire de Add-AzureASAccount un wrapper de Connect-AzAccount pour éviter un changement cassant

#### <a name="azautomation"></a>Az.Automation
* Correction du bogue de l’applet de commande New-AzAutomationSoftwareUpdateConfiguration pour les inclusions. Les paramètres IncludedKbNumber et IncludedPackageNameMask devraient maintenant fonctionner.
* Correctif de bogue pour le groupe dynamique de gestion de mises à jour d’automatisation Azure

#### <a name="azcompute"></a>Az.Compute
* Ajout du paramètre HyperVGeneration à New-AzDiskConfig et New-AzSnapshotConfig
* Autorisation de créer des machines virtuelles avec l’image de galerie d’autres locataires. 

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Problème résolu dans le paramètre -Command de New-AzContainerGroup qui ajoutait un argument vide de fin

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour du kit SDK .Net ADF avec la version 3.0.2
* Mise à jour de l’applet de commande Set-AzDataFactoryV2 avec des paramètres supplémentaires pour les paramètres connexes RepoConfiguration.

#### <a name="azresources"></a>Az.Resources
* Amélioration de la gestion des fournisseurs pour 'Get-AzResource' quand les paramètres '-ResourceId' ou '-ResourceGroupName', '-Name' et '-ResourceType' sont fournis
* Amélioration de la gestion des erreurs pour 'Test-AzDeployment' et 'Test-AzResourceGroupDeployment'
    - Gestion des erreurs levées en dehors de la validation du déploiement en les ajoutant plutôt dans la sortie de commande
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856
* Ajout du paramètre de commutateur '-IgnoreDynamicParameters' à l’ensemble des applets de commande de déploiement pour ignorer l’invite dans les scénarios de script et de travail
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/6856

#### <a name="azsql"></a>Az.Sql
* Prise en charge de la classification des données de base de données.

#### <a name="azstorage"></a>Az.Storage
* Signalement détaillé d’une erreur lors de la création du contexte de stockage avec le paramètre -UseConnectedAccount, mais sans compte Azure de connexion
    - New-AzStorageContext
* Prise en charge de la gestion des propriétés du service Blob d’un compte de stockage spécifié avec l’API de plan de gestion
    - Update-AzStorageBlobServiceProperty
    - Get-AzStorageBlobServiceProperty
    - Enable-AzStorageBlobDeleteRetentionPolicy
    - Disable-AzStorageBlobDeleteRetentionPolicy
* Prise en charge de -AsJob pour les applets de commande de chargement et de téléchargement de fichiers et d’objets blob
    - Get-AzStorageBlobContent
    - Set-AzStorageBlobContent
    - Get-AzStorageFileContent
    - Set-AzStorageFileContent

## <a name="160---march-2019"></a>1.6.0 - Mars 2019
### <a name="highlights-since-the-last-major-release"></a>Points importants depuis la dernière version majeure
* Disponibilité générale du module `Az`
* Pour plus d’informations sur le module `Az`, consultez https://aka.ms/azps-announce
* Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/
* Ajout de la prise en charge des caractères génériques dans les applets de commande Get pour Az.Compute et Az.Network
* Ajout de l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement
* Ajout de la prise en charge des runbooks Python 2 dans Az.Automation
* Az.LogicApp : Nouvelles applets de commande pour la configuration par lots et des assemblys des comptes d’intégration

#### <a name="azautomation"></a>Az.Automation
* Modification dans la gestion des mise à jour Azure Automation pour prendre en charge les nouvelles fonctionnalités suivantes :
    * Regroupement dynamique
    * Pré-Post script
    * Paramètre de redémarrage

#### <a name="azcompute"></a>Az.Compute
* Correction d’un problème de résolution de chemin dans Get-AzVmBootDiagnosticsData
* Mise à jour de la bibliothèque cliente Compute vers la version 25.0.0.

#### <a name="azkeyvault"></a>Az.KeyVault
* Ajout de la prise en charge des caractères génériques pour les applets de commande KeyVault

#### <a name="aznetwork"></a>Az.Network
* Ajout de la prise en charge Threat Intelligence pour le Pare-feu Azure
* Ajout de la ressource de niveau supérieur de la stratégie de pare-feu Application Gateway et des règles personnalisées

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Ajout de SnapshotRetentionInDays dans la stratégie Azure VM pour prendre en charge les RP instantanés
* Ajout de la prise en charge de canal pour la désinscription de conteneur

#### <a name="azresources"></a>Az.Resources
* Mise à jour de la prise en charge des caractères génériques pour Get-AzResource et Get-AzResourceGroup
* Mise à jour des informations d’identification utilisées lors des appels génériques à ARM

#### <a name="azsql"></a>Az.Sql
* Modification du paramètre des applets de commande de Threat Detection (ExcludeDetectionType) où DetectionType est remplacé par string[] pour en faire une future preuve quand de nouveaux DetectionTypes sont ajoutés et pour prendre également en charge l’autocomplétion.

#### <a name="azstorage"></a>Az.Storage
* Prise en charge de Get/Set/Remove Management Policy sur un compte de stockage
    - Set-AzStorageAccountManagementPolicy
    - Get-AzStorageAccountManagementPolicy
    - Remove-AzStorageAccountManagementPolicy
    - Add-AzStorageAccountManagementPolicyAction
    - New-AzStorageAccountManagementPolicyFilter
    - New-AzStorageAccountManagementPolicyRule

#### <a name="azwebsites"></a>Az.Websites
* Correction du bogue du modèle ARM qui cassait le clonage de tous les emplacements avec 'New-AzWebApp -IncludeSourceWebAppSlots' 

## <a name="150---march-2019"></a>1.5.0 - Mars 2019
#### <a name="azaccounts"></a>Az.Accounts
* Ajout de la commande « Register-AzModule » pour prendre en charge les applets de commande AutoRest générées
* Mise à jour des exemples pour Connect-AzAccount

#### <a name="azautomation"></a>Az.Automation
* Résolution du problème de récupération de certaines planifications mensuelles dans plusieurs applets de commande Azure Automation
* Correction de Get-AzAutomationDscNode qui retournait juste les 20 premiers nœuds. Maintenant, elle retourne tous les nœuds

#### <a name="azcdn"></a>Az.Cdn
* Ajout de nouvelles applets de commande Powershell pour activer/désactiver les URL HTTPS de domaine personnalisé, et dépréciation des anciennes

#### <a name="azcompute"></a>Az.Compute
* Ajout de la prise en charge des caractères génériques pour les applets de commande Get

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour du kit .Net SDK ADF avec la version 3.0.1

#### <a name="azlogicapp"></a>Az.LogicApp
* Correction de ListWorkflows qui récupérait uniquement la première page de résultats

#### <a name="aznetwork"></a>Az.Network
* Ajout de la prise en charge des caractères génériques pour les applets de commande Network

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Ajout de la prise en charge de SQL Server dans les machines virtuelles Azure
* Mise à jour du kit SDK
* Suppression de la vérification de VMappContainer dans Get-ProtectableItem
* Ajout de Name et ServerName comme paramètres pour Get-ProtectableItem

#### <a name="azresources"></a>Az.Resources
* Ajout du paramètre `-TemplateObject` aux applets de commande de déploiement
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2933
* Résolution du problème d’envoi du résultat de `Get-AzResource` à `Set-AzResource`
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8240
* Résolution du problème de changement de type de données JSON lors de l’exécution de `Set-AzResource`
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7930

#### <a name="azsql"></a>Az.Sql
* Mise à jour d’AuditingEndpointsCommunicator.
    - Correction du comportement d’un cas limite lors de la création de nouveaux paramètres de diagnostic.

#### <a name="azstorage"></a>Az.Storage
* Prise en charge de Kind BlockBlobStorage lors de la création du compte de stockage      - New-AzStorageAccount

## <a name="140---february-2019"></a>1.4.0 - Février 2019
#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Applet de commande AddAzureASAccount dépréciée

#### <a name="azautomation"></a>Az.Automation
* Mise à jour de l’aide pour Import-AzAutomationDscNodeConfiguration
* Ajout de la validation des noms de configuration pour l’applet de commande Import-AzAutomationDscConfiguration
* Amélioration de la gestion des erreurs pour l’applet de commande Import-AzAutomationDscConfiguration

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Ajout de CustomSubdomainName en tant que nouveau paramètre facultatif de New-AzCognitiveServicesAccount, qui est utilisé pour spécifier le sous-domaine de la ressource.

#### <a name="azcompute"></a>Az.Compute
* Résolution d’un problème lié aux jeux de paramètres d’ID
* Mise à jour de Get-AzVMExtension pour lister toutes les extensions installées si le paramètre Name n’est pas fourni.
* Ajout des paramètres Tag et ResourceId pour l’applet de commande Update-AzImage
* Get-AzVmssVM sans ID d’instance et avec InstanceView peut lister les machines virtuelles VMSS avec une vue d’instance.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Ajout d’applets de commande pour l’énumération et la restauration des éléments supprimés dans ADL

#### <a name="azeventhub"></a>Az.EventHub
* Ajout de la nouvelle propriété booléenne SkipEmptyArchives pour ignorer les archives vides dans la classe CaptureDescription de Eventhub 

#### <a name="azkeyvault"></a>Az.KeyVault
* Correction du balisage de Set-AzKeyVaultSecret

#### <a name="azlogicapp"></a>Az.LogicApp
* Ajout des comptes d’intégration dans la référence SKU de base
* Ajout dans XSLT 2.0, XSLT 3.0 et dans les types de mappages Liquid
* Nouvelles applets de commande pour les assemblys de compte d’intégration
    - Get-AzIntegrationAccountAssembly
    - New-AzIntegrationAccountAssembly
    - Remove-AzIntegrationAccountAssembly
    - Set-AzIntegrationAccountAssembly
* Nouvelles applets de commande pour la configuration par lots des comptes d’intégration
    - Get-AzIntegrationAccountBatchConfiguration
    - New-AzIntegrationAccountBatchConfiguration
    - Remove-AzIntegrationAccountBatchConfiguration
    - Set-AzIntegrationAccountBatchConfiguration
* Mise à jour du SDK Logic App vers la version 4.1.0

#### <a name="azmonitor"></a>Az.Monitor
* Mise à jour de l’aide pour Get-AzMetric

#### <a name="aznetwork"></a>Az.Network
* Mise à jour des exemples de l’aide pour Add-AzApplicationGatewayCustomError

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Prise en charge supplémentaire des opérations New et Get pour les sources de données ApplicationInsights.
    - Ajout du nouveau type « ApplicationInsights » permettant de prendre en charge les opérations Get Specific et Get All pour les sources de données ApplicationInsights d’un espace de travail donné. 
    - Ajout de l’applet de commande New-AzOperationalInsightsApplicationInsightsDataSource pour la création de sources de données à l’aide de paramètres de ressource Application Insights donnés : subscription Id, resourceGroupName et name. 

#### <a name="azresources"></a>Az.Resources
* Corriger le problème https://github.com/Azure/azure-powershell/issues/8166
* Corriger le problème https://github.com/Azure/azure-powershell/issues/8235
* Corriger le problème https://github.com/Azure/azure-powershell/issues/6219
* Correction du bogue empêchant de créer plusieurs fois des KeyCredentials

#### <a name="azsql"></a>Az.Sql
* Ajout de la prise en charge du niveau Hyperscale de la base de données SQL
* Correction du bogue lors duquel la restauration pouvait échouer à cause de la définition de propriétés non nécessaires dans la requête de restauration

#### <a name="azwebsites"></a>Az.Websites
* Correction de l’exemple dans Get-AzWebAppSlotMetrics

## <a name="130---february-2019"></a>1.3.0 - Février 2019
#### <a name="azaccounts"></a>Az.Accounts
* Mettre à jour vers la version la plus récente de ClientRuntime

#### <a name="azanalysisservices"></a>Az.AnalysisServices
Disponibilité générale pour le module Az.AnalysisServices.

#### <a name="azcompute"></a>Az.Compute
* Extension AEM : Ajouter la prise en charge des disques UltraSSD et P60, P70 et P80
* Mettre à jour la description de l’aide pour Set-AzVMBootDiagnostics
* Mettre à jour la description de l’aide et l’exemple pour Update-AzImage

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
Disponibilité générale pour le module Az.RecoveryServices.

#### <a name="azresources"></a>Az.Resources
* Corriger le balisage pour les groupes de ressources 
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8166
* Corriger le problème de `Get-AzureRmRoleAssignment` ne respectant pas - ErrorAction 
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8235

#### <a name="azsql"></a>Az.Sql
* Ajouter Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy
* Résoudre le problème d’absence de connexion à un compte Azure se manifestant par une exception nullref lors de l’exécution d’applets de commande
* L’exception de référence null a été résolue dans Get-AzSqlCapability

## <a name="121---january-2019"></a>1.2.1 - Janvier 2019
#### <a name="azaccounts"></a>Az.Accounts
* Publication avec version correcte de l’authentification

#### <a name="azanalysisservices"></a>Az.AnalysisServices
* Publication avec dépendance d’authentification mise à jour

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Publication avec dépendance d’authentification mise à jour

## <a name="120---january-2019"></a>1.2.0 - Janvier 2019
#### <a name="azaccounts"></a>Az.Accounts
* Ajouter l’authentification interactive et par nom d’utilisateur/mot de passe pour Windows PowerShell 5.1 uniquement
* Mettre à jour des URL d’aide en ligne incorrectes
* Ajouter le message d’avertissement dans PS Core pour Uninstall-AzureRm

#### <a name="azaks"></a>Az.Aks
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azautomation"></a>Az.Automation
* Ajout de la prise en charge des runbooks Python 2
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azcdn"></a>Az.Cdn
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azcompute"></a>Az.Compute
* Ajouter l’applet de commande Invoke-AzVMReimage
* Ajouter le paramètre TempDisk à Set-AzVmss
* Corriger le message d’avertissement de New-AzVM

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azdatafactory"></a>Az.DataFactory
* Kit de développement logiciel .Net ADK mis à jour vers la version 3.0.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Résoudre un problème lié au point de terminaison ADLS lors de l’utilisation de MSI
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7462
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="aziothub"></a>Az.IotHub
* Ajouter le format d’encodage à l’applet de commande Add-IotHubRoutingEndpoint.

#### <a name="azkeyvault"></a>Az.KeyVault
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="aznetwork"></a>Az.Network
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azresources"></a>Az.Resources
* Corriger des exemples incorrects dans « New-AzADAppCredential » et la documentation de référence « New-AzADSpCredential »
* Corriger le problème d’absence de résolution du paramètre « -TemplateFile » avant l’exécution des applets de déploiement du groupe de ressources
* Az.Resources : Corriger la documentation pour la valeur par défaut du mode New-AzureRmPolicyDefinition
* Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/7522
* Az.Resources : Corriger le problème https://github.com/Azure/azure-powershell/issues/5747
* Résoudre un problème de mise en forme avec l’objet « PSResourceGroupDeployment »
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/2123

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Restauration quand un certificat est ajouté au modèle VMSS, mais qu’une exception est levée. Le bogue suivant a été corrigé : https://github.com/Azure/service-fabric-issues/issues/932
* Correction de certains messages d’erreur.
* Correction de la création de cluster avec modèle ARM par défaut pour New-AzServiceFabriCluster qui ne fonctionnait pas avec la migration vers Az.
* Correction de l’ajout du certificat du cluster/de l’application pour ajouter uniquement une instance VM Scale Sets correspondant au cluster en vérifiant l’ID du cluster dans l’extension.

#### <a name="azsignalr"></a>Az.SignalR
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azsql"></a>Az.Sql
* Mettre à jour des URL d’aide en ligne incorrectes
* Mise à jour de la description du paramètre LicenseType avec les valeurs possibles
* Correctif pour la mise à jour de l’identité de l’instance gérée qui ne fonctionnait pas lorsqu’il s’agissait de la seule propriété mise à jour
* Prise en charge du classement personnalisé sur l’instance gérée

#### <a name="azstorage"></a>Az.Storage
* Mettre à jour des URL d’aide en ligne incorrectes
* Message d’erreur détaillé lors de l’obtention/la définition de la journalisation/des métriques classique sur le compte de stockage Premium, étant donné que le compte de stockage Premium ne prend pas en charge la journalisation/les métriques classiques.
    - Get/Set-AzStorageServiceLoggingProperty
    - Get/Set-AzStorageServiceMetricsProperty

#### <a name="aztrafficmanager"></a>Az.TrafficManager
* Mettre à jour des URL d’aide en ligne incorrectes

#### <a name="azwebsites"></a>Az.Websites
* Mettre à jour des URL d’aide en ligne incorrectes
* « New-AzWebAppSSLBinding » a été corrigé pour télécharger le certificat vers le groupe de ressources+emplacement corrects si l’application est hébergée sur un ASE.
* « New-AzWebAppSSLBinding » a été corrigé pour éviter le remplacement des balises sur la liaison d’un certificat SSL à une application

## <a name="110---january-2019"></a>1.1.0 - janvier 2019
#### <a name="azaccounts"></a>Az.Accounts
* Ajouter l’étendue « Local » à Enable-AzureRmAlias

#### <a name="azcompute"></a>Az.Compute
* Le nom est désormais optionnel dans l’ensemble de paramètre d’ID pour Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage
* Mise à jour de la description d’ID dans les fichiers d’aide
* Correction du problème de compatibilité descendante avec le module Az.Accounts

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Mettez à jour la version du kit de développement logiciel (SDK) de dataplane vers 1.1.1.14 pour appliquer les correctifs.
    - Correction de la gestion des propriétés accesstime et modificationtime négatives pour getfilestatus et liststatus. Correction du jeton d’annulation asynchrone

#### <a name="azeventgrid"></a>Az.EventGrid
* Mis à jour pour utiliser la version d’API 2019-01-01.
* Mettre à jour les cmdlets suivantes pour prendre en charge un nouveau scénario dans la version d’API 2019-01-01
    - New-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :
        - la durée de vie de l’événement,
        - le nombre max de tentatives de livraison pour les événements,
        - le point de terminaison de lettres mortes.
    - Update-AzureRmEventGridSubscription : Ajoutez les nouveaux paramètres facultatifs pour spécifier :
        - la durée de vie de l’événement,
        - le nombre max de tentatives de livraison pour les événements,
        - le point de terminaison de lettres mortes.
* Ajoutez les nouvelles valeurs enum (à savoir storageQueue et hybridConnection) pour l’option EndpointType dans les cmdlets New-AzureRmEventGridSubscription et Update-AzureRmEventGridSubscription.
* Affichez le message d’avertissement si la création ou la mise à jour de l’abonnement à l’événement risque d’empêcher une action manuelle de la part de l’utilisateur.

#### <a name="aziothub"></a>Az.IotHub
* Mise à jour vers la dernière version du kit de développement logiciel (SDK) IotHub

#### <a name="azlogicapp"></a>Az.LogicApp
* Get-AzLogicApp répertorie tout cela sans nom spécifié

#### <a name="azresources"></a>Az.Resources
* Résolution du problème relatif à l’ensemble de paramètres lorsque les paramètres « -ODataQuery » et « ResourceId » sont renseignés pour « Get-AzResource »
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/7875
* Correction de la gestion du paramètre -Custom dans New/Set-AzPolicyDefinition
* Correction des fautes dans la documentation New-AzDeployment
* Paramètre « -MailNickname » maintenant obligatoire pour « New-AzADUser »
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/8220

#### <a name="azsignalr"></a>Az.SignalR
* Correction du problème de compatibilité descendante avec le module Az.Accounts

#### <a name="azsql"></a>Az.Sql
* Conversion de la dépendance du client de gestion de stockage en implémentation du kit de développement logiciel (SDK) commun.

#### <a name="azstorage"></a>Az.Storage
* Définition de la propriété StorageAccountName du contexte de stockage comme nom réel du compte de stockage, lorsque créé avec un jeton Sas, OAuth ou Anonyme
    - New-AzStorageContext
* Création du jeton Sas de l’objet d’instantané blob avec le paramètre -FullUri, correction de l’Uri retournée pour correspondre à l’Uri de l’instantané
    - New-AzStorageBlobSASToken

#### <a name="azwebsites"></a>Az.Websites
* Correction d’un bogue d’analyse de date dans Get-AzDeletedWebApp
* Correction du problème de compatibilité descendante avec le module Az.Accounts

## <a name="100---december-2018"></a>1.0.0 - Décembre 2018
### <a name="general"></a>Généralités

- Disponibilité générale du module Az
- Aide en ligne pour chaque module
- Pour obtenir plus d’informations et une feuille de route, voir la [page d’annonce d’Az](https://aka.ms/azps-announce)
- Voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations sur la migration à partir d’AzureRM

### <a name="azaccounts"></a>Az.Accounts
- Remplace Az.Profile
- Formats de tableau fixe pour les types de profil et de contexte

### <a name="azapimanagement"></a>Az.ApiManagement
- Correctifs pour #7002
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azbatch"></a>Az.Batch
- Possibilité pour voir quelle version de l’agent de nœud Azure Batch s’exécute sur chacune des machines virtuelles dans un pool, via la nouvelle propriété `NodeAgentInformation` sur `PSComputeNode`.
- La valeur par défaut `Caching` pour `PSDataDisk` est désormais `ReadWrite` au lieu de `None`.
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azbilling"></a>Az.Billing
- Combine les cmdlets Billing, Consumption et UsageAggregates, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azcognitivservices"></a>Az.CognitivServices
- Possibilité d’ajouter des compléments pour SkuName et Typem sur l’opération New-AzureRmCognitiveServicesAccount
- Suppression du jeu de paramètres GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus

### <a name="azcontainerinstance"></a>Az.ContainerInstance
- Ajout de la prise en charge de ManagedIdentity

### <a name="azdatalakeanalytics"></a>Az.DataLakeAnalytics
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azdatalakestore"></a>Az.DataLakeStore
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azmonitor"></a>Az.Monitor
- Remplacement du nom Az.Insights par Az.Monitor et autres changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azkeyvault"></a>Az.KeyVault
- Suppression de la propriété déconseillée ’PurgeDisabled’ dans les types de sortie

### <a name="azmachinelearning"></a>Az.MachineLearning
- Inclusion des cmdlets du module Az.MachineLearningCompute

### <a name="azmedia"></a>Az.Media
- Suppression des alias -Tags déconseillés de New-AzMediaService

### <a name="aznetwork"></a>Az.Network
Ajout de la prise en charge de la configuration de RewriteRuleSets dans Application Gateway
    - Ajout de nouvelles cmdlets :
        - Add-AzureRmApplicationGatewayRewriteRuleSet
        - Get-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRuleSet
        - Remove-AzureRmApplicationGatewayRewriteRuleSet
        - Set-AzureRmApplicationGatewayRewriteRuleSet
        - New-AzureRmApplicationGatewayRewriteRule
        - New-AzureRmApplicationGatewayRewriteRuleActionSet
        - New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration
    - Cmdlets mises à jour avec le paramètre facultatif -RewriteRuleSet
        - New-AzureRmApplicationGateway
        - New-AzureRmApplicationGatewayRequestRoutingRule
        - Add-AzureRmApplicationGatewayRequestRoutingRule
        - New-AzureRmApplicationGatewayPathRuleConfig
        - Add-AzureRmApplicationGatewayUrlPathMapConfig
        - New-AzureRmApplicationGatewayUrlPathMapConfig Ajout de la prise en charge de KeyVault pour Application Gateway avec l’identité.
    - Mise à jour des cmdlets avec le paramètre facultatif -KeyVaultSecretId, -KeyVaultSecret
        - Add-AzApplicationGatewaySslCertificate
        - New-AzApplicationGatewaySslCertificate
        - Set-AzApplicationGatewaySslCertificate
    - Cmdlet New-AzApplicationGateway mise à jour avec le paramètre facultatif -UserAssignedIdentity
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azoperationalinsights"></a>Az.OperationalInsights
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azprofile"></a>Az.Profile
- Nom du module remplacé par Az.Accounts

### <a name="azrecoveryservices"></a>Az.RecoveryServices
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azresources"></a>Az.Resources
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azservicefabric"></a>Az.ServiceFabric
- Prise en charge des certificats spécifiés par nom commun et empreinte
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azsignalr"></a>Az.SIgnalR
- Disponibilité générale des cmdlets PowerShell pour SIgnalR

### <a name="azsql"></a>Az.Sql
- Ajout des nouveaux types de détection Data_Exfiltration et Unsafe_Action aux cmdlets de détection des menaces
- Mise à jour des exemples de la documentation pour les cmdlets d’audit SQL
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azstorage"></a>Az.Storage
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

### <a name="azwebsites"></a>Az.Websites
- Changements cassants mineurs, voir le [guide de migration](https://aka.ms/azps-migration-guide) pour plus d’informations

## <a name="070---december-2018"></a>0.7.0 - Décembre 2018

### <a name="general"></a>Généralités

* Changements mineurs pour la future transition d’AzureRM vers Az

### <a name="azcompute"></a>Az.Compute

* Ajout de la prise en charge d’UltraSSD et des images de la galerie dans les jeux de paramètres simples pour les cmdlets `New-AzVm(ss)`.

### <a name="azdatalakestore"></a>Az.DataLakeStore

* Correction de la barre oblique de fin dans le domaine du compte ADLS

### <a name="azfrontdoor"></a>Az.FrontDoor

* Correction de certains liens rompus
    - Dans les articles New-AzureRmFrontDoor et Set-AzureRmFrontDoor, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.
    - Dans l’article New-AzureRmFrontDoorManagedRuleObject, correction du lien vers l’article sur la cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.

### <a name="azrecoveryservices"></a>Az.RecoveryServices

* Ajout de validations du côté client pour les opérations de restauration sur un partage de fichiers Azure.
* Caractère facultatif de storageAccountName et storageAccountResourceGroupName pour la restauration AFS.

### <a name="azresources"></a>Az.Resources

* Correctif pour https://github.com/Azure/azure-powershell/issues/7679
    - Mise à jour de Get-AzureRmRoleAssignment pour utiliser l’étendue de l’abonnement si elle est fournie lors de la demande des administrateurs classiques.

### <a name="azsql"></a>Az.Sql

* Changements mineurs pour la future transition d’AzureRM vers Az
* Correction d’un problème lors de l’utilisation de Get-AzureRmSqlDatabaseVulnerabilityAssessment avec le principal DotNet
* Modification de la documentation sur les messages d’aide relatifs aux cmdlets d’audit SQL.

### <a name="azstorage"></a>Az.Storage

* Ajout de -EnableHierarchicalNamespace à New-AzureRmStorageAccount
* Correction d’un problème où la cmdlet de copie de fichier ne peut pas réutiliser le contexte source dans la destination sans entrée -DestContext
    - Start-AzureStorageFileCopy
* Prise en charge de la configuration du site Web statique
    - Enable-AzureStorageStaticWebsite
    - Disable-AzureStorageStaticWebsite

### <a name="azwebsites"></a>Az.Websites

* Set-AzureRmWebApp et Set-AzureRmWebAppSlot 
    - Nouveau paramètre (-AzureStoragePath) ajouté pour spécifier que des chemins d’accès au stockage Azure doivent être montés dans les applications de conteneurs Windows et Linux. Utilisation de la sortie de la nouvelle cmdlet New-AzureRmWebAppAzureStoragePath en tant que paramètre pour définir les chemins d’accès au stockage Azure.

## <a name="061---november-2018"></a>0.6.1 - Novembre 2018

### <a name="azapimanagement"></a>Az.ApiManagement
* Mise à jour des dépendances pour le problème de mappage de types

### <a name="azautomation"></a>Az.Automation
* Cmdlets Azure Automation basées sur Swagger
* Ajout des cmdlets Update Management
* Ajout des cmdlets de contrôle de code source
* Ajout de la cmdlet Remove-AzureRmAutomationHybridWorkerGroup
* Correction de la commande de nœud d’inscription DSC

### <a name="azcompute"></a>Az.Compute
* Résolution du problème d’identité pour l’identité SystemAssigned
* Mise à jour des dépendances pour le problème de mappage de types

### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Mise à jour des dépendances pour le problème de mappage de types

### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Mise à jour de la description d’exemples pour les cmdlets marketplace

### <a name="aznetwork"></a>Az.Network
* Ajout des cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError
* Nouvel ajout d’ICMP aux protocoles réseau AzureFirewall pris en charge
* Mise à jour de la cmdlet Test-AzureRmNetworkWatcherConnectivity, ajout de validation sur l’ID de destination, l’adresse et le port. 
* Résolution des problèmes avec l’utilisation de la mémoire dans la carte VirtualNetwork

### <a name="azrecoveryservicesbackup"></a>Az.RecoveryServices.Backup
* Correction de la stratégie de modification pour un partage de fichiers protégé.
* Conversion du fuseau horaire de stratégie en majuscules.

### <a name="azrecoveryservicessiterecovery"></a>Az.RecoveryServices.SiteRecovery
* Correction de l’exemple dans New-AzureRmRecoveryServicesAsrProtectableItem
* Mise à jour des dépendances pour le problème de mappage de types

### <a name="azrelay"></a>Az.Relay
* Ajout du Parameter -KeyValue à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.

### <a name="azresources"></a>Az.Resources
* Mise à jour de la documentation d’aide pour des paramètres relatifs à l’identité de ressource dans `New-AzureRmPolicyAssignment` et `Set-AzureRmPolicyAssignment`
* Ajout d’un exemple pour New-AzureRmPolicyDefinition qui utilise -Metadata
* Correction pour permettre la conservation de la casse dans les clés Tag dans NetStandard: #7678 #7703

### <a name="azservicefabric"></a>Az.ServiceFabric
* Ajout de messages d’obsolescence pour les changements cassants à venir

### <a name="azsql"></a>Az.Sql
* Ajout de nouvelles applets de commande pour les opérations CRUD sur Azure Sql Database Managed Instance et Azure Sql Managed Database
    - Get-AzureRmSqlInstance
    - New-AzureRmSqlInstance
    - Set-AzureRmSqlInstance
    - Remove-AzureRmSqlInstance
    - Get-AzureRmSqlInstanceDatabase
    - New-AzureRmSqlInstanceDatabase
    - Restore-AzureRmSqlInstanceDatabase
    - Remove-AzureRmSqlInstanceDatabase
* Activation de la gestion de stratégie d’audit étendue sur un serveur ou une base de données.
    - Un nouveau paramètre (PredicateExpression) a été ajouté pour activer le filtrage des journaux d’audit.
    - Des cmdlets ont été modifiées pour utiliser des clients SQL plutôt que des clients hérités.
    - Set-AzureRmSqlServerAuditing.
    - Get-AzureRmSqlServerAuditing.
    - Set-AzureRmSqlDatabaseAuditing.
    - Get-AzureRmSqlDatabaseAuditing.
* Correction du problème relatif à l’utilisation de Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings avec un ensemble de paramètres de nom de compte de stockage

## <a name="050---november-2018"></a>0.5.0 - Novembre 2018
#### <a name="general"></a>Généralités
* Ajout de compléments de ressources à de nombreuses cmdlets principales, ce qui permet de parcourir les noms des ressources existantes ave la touche Tabulation lors de l’appel des cmdlets de manière interactive

#### <a name="azprofile"></a>Az.Profile
* Mise à jour du code commun pour utiliser la dernière version de ClientRuntime
* Changement de nom du paramètre TenantId dans la cmdlet Connect-AzAccount en Tenant et ajout d’un alias pour TenantId
* Mise à jour de la description TenantId pour Connect-AzAccount
* Correction du message d’erreur en cas d’échec de connexion lorsqu’un domaine de locataire est fourni
    - https://github.com/Azure/azure-powershell/issues/6936
* Résolution du conflit avec le nom de contexte pour les comptes dont le locataire ne dispose d’aucun abonnement
    - https://github.com/Azure/azure-powershell/issues/7453
* Correction du problème avec les points de terminaison DataLake lors de l’utilisation de MSI
    - https://github.com/Azure/azure-powershell/issues/7462
* Correction du problème de levée de « Disconnect-Connect-AzAccount » lorsqu’il n’y a pas de connexion
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Ajout de l’opération Get-AzCognitiveServicesAccountSkus.

#### <a name="azcompute"></a>Az.Compute
* Ajout des cmdlets Add-AzVmssVMDataDisk et Remove-AzVmssVMDataDisk
* Get-AzVMImage affiche AutomaticOSUpgradeProperties
* Correction des valeurs des options -BootstrapOptions et -JsonAttribute de SetAzVMChefExtension qui ne sont pas définies au format JSON.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Mise à jour du package DataLake vers la version 1.1.10.
* Ajout de la valeur de concurrence par défaut aux opérations multithread.

#### <a name="azinsights"></a>Az.Insights
* Correction du problème #7267 (zone de mise à l’échelle)
    - Problèmes lorsqu’une nouvelle règle de mise à l’échelle est créée sans avoir défini correctement les paramètres énumérés (toujours définir leurs valeurs par défaut).
* Correction du problème #7513 [Insights], les catégories de Set-AzDiagnosticSetting doivent être spécifiées explicitement lors de la création des paramètres
    - À présent, l’activation des catégories de la cmdlet ne doit plus être indiquée explicitement lors de la création. Par exemple, cela fonctionne comme documenté

#### <a name="aznetwork"></a>Az.Network
* Modification du type d’homologation en paramètre obligatoire pour les cmdlets suivantes : -
    - Get-AzExpressRouteCircuitRouteTable
    - Get-AzExpressRouteCircuitARPTable
    - Get-AzExpressRouteCircuitRouteTableSummary
    - Get-AzExpressRouteCrossConnectionArpTable
    - Get-AzExpressRouteCrossConnectionRouteTable
    - Get-AzExpressRouteCrossConnectionRouteTableSummary

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Ajout des cmdlets de correction des stratégies

#### <a name="azresources"></a>Az.Resources
* Correctif pour https://github.com/Azure/azure-powershell/issues/7402
    - Autorisation de l’énumération des ressources à l’aide du paramètre « ResourceId » pour « Get-AzResource »

#### <a name="azservicebus"></a>Az.ServiceBus
* Ajout de la propriété en lecture seule MigrationState à PSServiceBusMigrationConfigurationAttributes afin d’aider à connaître l’état de la migration.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correction de l’ajout de certificat au VMSS Linux.
* Correction de « Add-AzServiceFabricClusterCertificate »
    - Utilisation de la bonne empreinte numérique d’un nouveau certificat (Azure/service-fabric-issues#932).
    - Affichage correct des exceptions (Azure/service-fabric-issues#1054).
* Correction de « Update-AzServiceFabricDurability » afin de mettre à jour la configuration des clusters avant de démarrer l’opération VMSS CreateOrUpdate.

## <a name="040---october-2018"></a>0.4.0 - Octobre 2018
#### <a name="azprofile"></a>Az.Profile
* Problème résolu avec Get-AzSubscription dans CloudShell
* Mise à jour du code commun pour utiliser la dernière version de ClientRuntime

#### <a name="azcompute"></a>Az.Compute
* Ajout de nouvelles tailles à la liste verte des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation du jeu de paramètres simple pour « New-AzVm »
* Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Ajout de la prise en charge des règles de réseau virtuel
    - Get-AzDataLakeStoreVirtualNetworkRule : Obtient ou liste la règle de réseau virtuel Azure Data Lake Store.
    - Add-AzDataLakeStoreVirtualNetworkRule : Ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.
    - Set-AzDataLakeStoreVirtualNetworkRule : Modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.
    - Remove-AzDataLakeStoreVirtualNetworkRule : Supprime une règle de réseau virtuel Azure Data Lake Store.

#### <a name="aznetwork"></a>Az.Network
* Mise à jour de la cmdlet Test-AzNetworkWatcherConnectivity, transmission de la valeur du protocole au serveur principal.
* Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.

#### <a name="azresources"></a>Az.Resources
* Résolution des problèmes où Get-AzRoleDefinition cause une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario. Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».

## <a name="030---october-2018"></a>0.3.0 - Octobre 2018
#### <a name="azurestorage"></a>Azure.Storage
* Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy
* Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.
    - Get-AzStorageUsage
    
#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Prise en charge de Get-AzCognitiveServicesAccountSkus sans compte existant.

#### <a name="azcompute"></a>Az.Compute
* Correction de Get-AzVM -ResourceGroupName <rg> pour renvoyer plus de 50 résultats si besoin
* Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de la cmdlet New-AzVmss.
* Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption

#### <a name="azdatafactoryv2"></a>Az.DataFactoryV2
* Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.

#### <a name="aznetwork"></a>Az.Network
* Ajout de la fonctionnalité NetworkProfile. nouvelles cmdlets ajoutées
    - Get-AzNetworkProfile
    - New-AzNetworkProfile
    - Remove-AzNetworkProfile
    - Set-AzNetworkProfile
    - New-AzContainerNicConfig
    - New-AzContainerNicConfigIpConfig
* Ajout d’un lien d’association de service sur le modèle de sous-réseau
* Ajout des cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap
* Ajout des cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig

#### <a name="azrediscache"></a>Az.RedisCache
* Autorisez toutes les chaînes en tant que Paramètre de taille à progresser. Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter

#### <a name="azresources"></a>Az.Resources
* Ajout du paramètre manquant -Mode à Set-AzPolicyDefinition
* Correction d’un bogue de la cmdlet Get-AzProviderOperation pour les opérations avec Origin comprenant un utilisateur

#### <a name="azsql"></a>Az.Sql
* Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel

#### <a name="azwebsites"></a>Az.Websites
* Nouvelle cmdlet Get-AzWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur
* Nouvelles cmdlets New-AzWebAppContainerPSSession et Enter-WebAppContainerPSSession : démarrent une session PowerShell à distance dans une application de conteneur Windows

## <a name="020---september-2018"></a>0.2.0 - Septembre 2018
 Version initiale