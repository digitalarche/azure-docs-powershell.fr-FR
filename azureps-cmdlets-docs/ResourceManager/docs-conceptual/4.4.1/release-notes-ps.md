Programme d’installation d’Azure PowerShell 4.3.1 : [lien](https://github.com/Azure/azure-powershell/releases/download/v4.3.1-August2017/azure-powershell.4.3.1.msi)

Module de la galerie pour les applets de commande ARM : [lien](https://www.powershellgallery.com/packages/AzureRM/4.3.1)

Module de la galerie pour les applets de commande héritées pour la gestion du Service (RDFE) : [lien](https://www.powershellgallery.com/packages/Azure/4.3.1)

## <a name="changes-in-431"></a>Changements dans 4.3.1

- Problème résolu avec certains assemblys non signés qui entraînaient une erreur `could not load file or assembly` à l’importation des modules

## <a name="changes-in-430"></a>Changements dans 4.3.0

* AnalysisServices
    * Résolution du bogue dans Set-AzureRmAnalysisServciesServer
        - Lorsque l’administrateur n’est pas fourni, il est supprimé.
    * Ajout de BackupBlobContainerUri dans New-AzureRmAnalysisServicesServer et Set-AzureRmAnalysisServicesServer
        - Activer pour définir/désactiver le conteneur d’objets blob de sauvegarde pour la sauvegarde/restauration du serveur Azure Analysis Services
    * Mise à jour de la recherche de référence SKU dans New-AzureRmAnalysisServicesServer et Set-AzureRmAnalysisServicesServer
        - Remplacement de la recherche de référence SKU codée en dur par une recherche dynamique.
    * Add-AzureAnalysisServicesAccount pour prendre en charge la connexion avec le principal de service
* Automatisation
    * Modifications apportées aux applets de commande AutomationDSC * pour extraire plus de 100 enregistrements
    * Résolution du problème des flux de commentaires qui arrêtaient de fonctionner après l’appel de certaines applets de commande d’automatisation (par exemple, Get-AzureRmAutomationVariable, Get-AzureRmAutomationJob).
    * Ajout de la prise en charge de la gestion des versions de build NodeConfiguration dans StartAzureAutomationDscCompilationJob et ImportAzureAutomationDscNodeConfiguration.
    * Correctifs de bogues pour les problèmes existants - Résolution du problème d’alias n°3775 et de l’alias runOn, ainsi que de la prise en charge pour HybridWorkers.
* Calcul
    * Set-AzureRmVMAEMExtension : Ajout de la prise en charge des nouvelles tailles de disque Premium
    * Set-AzureRmVMAEMExtension : Ajout de la prise en charge de la série M
    * Ajout du paramètre ForceUpdateTag à Add-AzureRmVmssExtension
    * Ajout du paramètre Primary à New-AzureRmVmssIpConfig
    * Ajout du paramètre EnableAcceleratedNetworking à Add-AzureRmVmssNetworkInterfaceConfig
    * Ajout de InstanceId à Set-AzureRmVmss
    * Exposition de MaintenanceRedeployStatus à la sortie Get-AzureRmVM-Status
    * Exposition de Restriction et de Capability au format de tableau de Get-AzureRmComputeResourceSku
* DataLakeStore
    * Correctif du problème : https://github.com/Azure/azure-powershell/issues/4323
* Event Hub
    * Ajout de la propriété ResourceGroup à NamespaceAttributes
        - ResourceGroup - Obtient le nom du groupe de ressources dans lequel se trouve Namespace
    * Mise à jour des applets de commande avec le nouveau paramètre et l’alias de paramètre
        - Mise à jour des applets de commande ci-dessous avec les jeux de paramètres pour Namespace et EventHub dans l’opération d’AuthorizationRule
        - New-AzureRmEventHubAuthorizationRule
            + Ajoute une nouvelle règle AuthorizationRule au NameSpace ou EventHub existant.
        - Get-AzureRmEventHubAuthorizationRule
            + Obtient la règle AuthorizationRule / la liste des AuthorizationRules pour le NameSpace ou l’EventHub existant.
        - Set-AzureRmEventHubAuthorizationRule
            + Met à jour les propriétés de la règle AuthorizationRule existante de l’EventHub NameSpace.
        - Remove-AzureRmEventHubAuthorizationRule
            + Supprime la règle AuthorizationRule existante du NameSpace ou de l’EventHub existant.
        - New-AzureRmEventHubKey
            + Génère une nouvelle clé principale/secondaire pour la règle AuthorizationRule du NameSpace ou de l’EventHub existant.
        - Get-AzureRmEventHubKey
            + Obtient la clé principale/secondaire pour la règle AuthorizationRule du NameSpace ou de l’EventHub existant.
* Réseau
    * New-AzureRmExpressRouteCircuitPeeringConfig : ajout de la prise en charge d’IPv6. Nouveau paramètre facultatif ajouté
        - PeerAddressType
    * Set-AzureRmExpressRouteCircuitPeeringConfig : ajout de la prise en charge d’IPv6. Nouveau paramètre facultatif ajouté
        - PeerAddressType
    * Remove-AzureRmExpressRouteCircuitPeeringConfig : ajout de la prise en charge d’IPv6. Nouveau paramètre facultatif ajouté
        - PeerAddressType
    * Paramètre marqué - ProbeEnabled comme obsolète
        - Add-AzureRmApplicationGatewayBackendHttpSettings
        - New-AzureRmApplicationGatewayBackendHttpSettings
        - Set-AzureRmApplicationGatewayBackendHttpSettings
* Profil
    * La collecte de données a été activée par défaut. Les données d’utilisation sont collectées par Microsoft afin d’améliorer l’expérience utilisateur. Les données sont anonymes et n’incluent pas de valeurs d’argument de ligne de commande.
        - Utilisation de l’applet de commande Disable-AzureRmDataCollection pour désactiver la fonctionnalité
        - Utilisation de l’applet de commande Enable-AzureRmDataCollection pour activer la fonctionnalité
* Ressources
    * Ajout de la prise en charge de la validation des étendues des applets de commande roledefinition et roleassignment suivantes avant l’envoi de la requête à ARM
        - Get-AzureRMRoleAssignment
        - New-AzureRMRoleAssignment
        - Remove-AzureRMRoleAssignment
        - Get-AzureRMRoleDefinition
        - New-AzureRMRoleDefinition
        - Remove-AzureRMRoleDefinition
        - Set-AzureRMRoleDefinition
* ServiceBus
    * Ajout ci-dessous de nouvelles applets de commande pour AuthorizationRules pour NameSpace, Queue et Topic. En fonction du jeu de paramètres, les opérations de règle d’autorisation sont effectuées.
     - New-AzureRmServiceBusAuthorizationRule
       - Ajoute une nouvelle règle AuthorizationRule au NameSpace/Queue/Topic ServiceBus existant.
     - Get-AzureRmServiceBusAuthorizationRule
       - Obtient la règle AuthorizationRule / la liste des AuthorizationRules pour le NameSpace/Queue/Topic ServiceBus existant.
     - Set-AzureRmServiceBusAuthorizationRule
       - Met à jour les propriétés de la règle AuthorizationRule existante du NameSpace/Queue/Topic ServiceBus.
     - New-AzureRmServiceBusKey
       - Génère une nouvelle clé principale/secondaire pour la règle AuthorizationRule du NameSpace/Queue/Topic ServiceBus existant.
     - Get-AzureRmServiceBusKey
       - Obtient une nouvelle clé principale/secondaire pour la règle AuthorizationRule du NameSpace/Queue/Topic ServiceBus existant.
     - Remove-AzureRmServiceBusNamespaceAuthorizationRule
       - Supprime la règle AuthorizationRule existante du NameSpace/Queue/Topic ServiceBus.
    * Ajout de la propriété ResourceGroup à NamespaceAttributes
* SQL
    * Mise à jour de Set-AzureRmSqlServerTransparentDataEncryptionProtector pour afficher un avertissement et demander confirmation que le Type du protecteur de chiffrement est bien défini sur AzureKeyVault
    * Ajout de nouvelles applets de commande mises à jour pour les paramètres d’audit
        - Ajout de l’applet de commande Get-AzureRmSqlDatabaseAuditing qui obtient les paramètres d’audit d’une base de données SQL Azure.
        - Ajout de l’applet de commande Get-AzureRmSqlServerAuditing qui obtient les paramètres d’audit d’un serveur SQL Azure.
        - Ajout de l’applet de commande Set-AzureRmSqlDatabaseAuditing qui change les paramètres d’audit d’une base de données SQL Azure.
        - Ajout de l’applet de commande Set-AzureRmSqlServerAuditing qui change les paramètres d’audit d’un serveur SQL Azure.
    * Dépréciation des applets de commande de stratégie d’audit existantes
        - Dépréciation de Get-AzureRmSqlDatabaseAuditingPolicy
        - Dépréciation de Get-AzureRmSqlServerAuditingPolicy
        - Dépréciation de Set-AzureRmSqlDatabaseAuditingPolicy
        - Dépréciation de Set-AzureRmSqlServerAuditingPolicy
        - Dépréciation de Use-AzureRmSqlServerAuditingPolicy
        - Dépréciation de Remove-AzureRmSqlDatabaseAuditing
        - Dépréciation de Remove-AzureRmSqlServerAuditing
    * L’analyse du fichier de schéma pour Update-AzureRmSqlSyncGroup ne tient désormais plus compte de la casse.
* Storage
    * Ajout de la prise en charge de NeworkRule aux applets de commande de compte de stockage du mode de ressources
        - New-AzureRmStorageAccount
        - Set-AzureRmStorageAccount
        - Get-AzureRmStorageAccountNetworkRuleSet
        - Update-AzureRmStorageAccountNetworkRuleSet
        - Add-AzureRmStorageAccountNetworkRule
        - Remove-AzureRmStorageAccountNetworkRule

Voir [les modifications apportées depuis la dernière version](https://github.com/Azure/azure-powershell/compare/v4.2.1-July2017...v4.3.1-August2017)
