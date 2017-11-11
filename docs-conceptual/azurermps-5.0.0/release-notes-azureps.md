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
ms.date: 07/26/2017
ms.openlocfilehash: d8a891673df343551cbd805016c2d25ee4e31c8c
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2017
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="20170925---version-440"></a>25 septembre 2017 - Version 4.4.0
* AnalysisServices
  * Ajout d’une nouvelle commandlet permettant la synchronisation des bases de données entre l’instance accessible en lecture/écriture et les instances accessibles en lecture seule
    - Fichier d’aide inclus pour la commandlet
    - Ajout des tests en mémoire et d’un scénario de test (uniquement en temps réel)
  * Correction des bogues dans la commandlet Add-AzureAsAccount
* Automatisation
  * Correction des documents d’aide pour les commandlets corrigés dans la version antérieure.
  * Ajout de 4 nouvelles commandlets pour prendre en charge le déploiement avec phases intermédiaire des configurations de nœud DSC.
    - Start-AzureRmAutomationDscNodeConfigurationDeployment
    - Stop-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeployment
    - Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule
* CognitiveServices
  * Intégration avec le Kit de développement logiciel (SDK) Cognitive Services Management version 2.0.0.
  * Maintenant, Get-AzureRmCognitiveServicesAccount peut correctement prendre en charge la pagination.
* Calcul
  * Exécutez la fonctionnalité de la commande :
    - Nouvelle cmdlet : Invoke-AzureRmVMRunCommand appelle une commande Exécuter sur une machine virtuelle
    - Nouvelle cmdlet : Get-AzureRmVMRunCommandDocument affiche les documents de commande Exécuter disponibles
  * Ajoutez le paramètre StorageAccountType à Set-AzureRmDataDisk
  * Prise en charge de la zone de disponibilité de la machine virtuelle, du groupe identique de machines virtuelles et du disque
    - Nouveau paramètre : l’élément Zone est ajouté à New-AzureRmVM, New-AzureRmVMConfig, New-AzureRmVmssConfig, New-AzureRmDiskConfig
  * Fonction de mise à niveau propagée du groupe identique de machines virtuelles :
    - Nouvelle cmdlet : Start-AzureRmVmssRollingOSUpgrade appelle la mise à niveau propagée du groupe identique de machines virtuelles
    - Nouvelle cmdlet : Set-AzureRmVmssRollingUpgradePolicy définit la stratégie de mise à niveau propagée du groupe identique de machines virtuelles.
    - Nouvelle cmdlet : Stop-AzureRmVmssRollingUpgrade annule la mise à niveau propagée du groupe identique de machines virtuelles
    - Nouvelle cmdlet : Get-AzureRmVmssRollingUpgrade affiche l’état de la mise à niveau propagé du groupe identique de machines virtuelles.
  * Le paramètre booléen AssignIdentity est introduit pour l’identité affectée par le système.
    - Nouveau paramètre : AssignIdentity est ajouté à New-AzureRmVMConfig, New-AzureRmVmssConfig et Update-AzureRmVM
  * Fonctionnalité de chiffrement de disque VMSS :
    - Nouvelle cmdlet : Set-AzureRmVmssDiskEncryptionExtension active le chiffrement de disque sur le groupe identique de machines virtuelles
    - Nouvelle cmdlet : Disable-AzureRmVmssDiskEncryption désactive le chiffrement de disque sur le groupe identique de machines virtuelles
    - Nouvelle cmdlet : Get-AzureRmVmssDiskEncryptionStatus affiche l’état du chiffrement de disque du groupe identique de machines virtuelles
    - Nouvelle cmdlet : Get-AzureRmVmssVMDiskEncryptionStatus affiche l’état du chiffrement de disque des machines virtuelles d’un groupe identique de machines virtuelles
* ContainerInstance
  * Ajout de cmdlets PowerShell pour Azure Container Instance
    - New-AzureRmContainerGroup
    - Get-AzureRmContainerGroup
    - Remove-AzureRmContainerGroup
    - Get-AzureRmContainerInstanceLog
* Insights
  * Nouvelle cmdlet Disable-AzureRmActivityLogAlert
    - Nouvelle cmdlet permettant de désactiver une alerte de journal d’activité existante.
    - Les balises peuvent être définies avec cette cmdlet (facultatif).
  * Nouvelle cmdlet Enable-AzureRmActivityLogAlert
    - Nouvelle cmdlet permettant d’activer une alerte de journal d’activité existante.
    - Les balises peuvent être définies avec cette cmdlet (facultatif).
  * Nouvelle cmdlet Get-AzureRmActivityLogAlert
    - Nouvelle cmdlet permettant de récupérer une ou plusieurs alertes de journal d’activité.
    - Les alertes peuvent être récupérées par nom, groupe de ressources ou abonnement.
  * Nouvelle cmdlet New-AzureRmActionGroup
    - Nouvelle cmdlet permettant de créer un objet ActionGroup dans la mémoire (sans requête).
  * Nouvelle cmdlet New-AzureRmActivityLogAlertCondition
    - Nouvelle cmdlet permettant de créer un objet de condition de nœud terminal d’une alerte de journal d’activité (sans requête).
  * Nouvelle cmdlet Set-AzureRmActivityLogAlert
    - Nouvelle cmdlet permettant de créer ou mettre à jour une alerte de journal d’activité.
  * Nouvelle cmdlet Remove-AzureRmActivityLogAlert
    - Nouvelle cmdlet permettant de supprimer une alerte de journal d’activité.
  * Nouvelle cmdlet Set-AzureRmActionGroup
    - Nouvelle cmdlet permettant de créer un groupe d’action et mettre à jour un groupe d’action existant.
  * Nouvelle cmdlet Get-AzureRmActionGroup
    - Nouvelle cmdlet permettant de récupérer un ou plusieurs groupes d’action.
    - Les groupes d’action peuvent être récupérés par nom, groupe de ressources ou abonnement.
  * Nouvelle cmdlet Remove-AzureRmActionGroup
    - Nouvelle cmdlet permettant de supprimer un groupe d’action.
  * Nouvelle cmdlet New-AzureRmActionGroupReceiver
    - Nouvelle cmdlet permettant de créer un récepteur de groupe d’action dans la mémoire.
* KeyVault
  * Cmdlets nouvelles ou mises à jour permettant de prendre en charge la suppression réversible des certificats KeyVault
    * Get-AzureKeyVaultCertificate
    * Remove-AzureKeyVaultCertificate
    * Undo-AzureKeyVaultCertificateRemoval
* Réseau
  * Ajout de la prise en charge des services de point de terminaison dans les sous-réseaux de réseau virtuel
    - Mise à jour du paramètre Add-AzureRmVirtualSubnetConfig : ajout du paramètre optionnel -ServiceEndpoint
    - Mise à jour du paramètre New-AzureRmVirtualSubnetConfig : ajout du paramètre optionnel -ServiceEndpoint
    - Mise à jour du paramètre Set-AzureRmVirtualSubnetConfig : ajout du paramètre optionnel -ServiceEndpoint
  * Ajout d’une cmdlet pour répertorier les services de point de terminaison disponibles à l’emplacement
    - Get-AzureRmVirtualNetworkAvailableEndpointService
  * Ajout de la possibilité de configurer une authentification P2S basée sur un serveur RADIUS externe pour les commandlets suivantes
    - New-AzureVirtualNetworkGateway
    - Set-AzureVirtualNetworkGateway
    - Set-AzureRmVirtualNetworkGatewayVpnClientConfig
  * Ajout d’une cmdlet pour permettre la génération de profils VPN pour une authentification P2S basée sur un serveur RADIUS externe
    - New-AzureRmVpnClientConfiguration
    - Get-AzureRmVpnClientConfiguration
  * Ajout de la prise en charge de paramètre SKU pour les adresses IP publiques et les équilibreurs de charge
    - Mise à jour du paramètre New-AzureRMLoadBalancer : ajout du paramètre optionnel -Sku
    - Mise à jour du paramètre New-AzureRMPublicIpAddress : ajout du paramètre optionnel - Sku
  * Ajout de la prise en charge du paramètre DisableOutboundSNAT pour les règles d’équilibrage de charge
    - Mise à jour du paramètre New-AzureRMLoadBalancerRuleConfig : ajout du paramètre optionnel DisableOutboundSNAT
    - Mise à jour du paramètre Add-AzureRMLoadBalancerRuleConfig : ajout du paramètre optionnel DisableOutboundSNAT
    - Mise à jour du paramètre Set-AzureRMLoadBalancerRuleConfig : ajout du paramètre optionnel DisableOutboundSNAT
  * Ajout de la prise en charge de IkeV2 P2S
    - Mise à jour du paramètre New-AzureRmVirtualNetworkGateway : ajout du paramètre optionnel -VpnClientProtocol, valeur par défaut [ « SSTP », « IkeV2 » ]
    - Mise à jour du paramètre Set-AzureRmVirtualNetworkGateway : ajout du paramètre optionnel -VpnClientProtocol
  * Ajout de la prise en charge de règles MultiValued dans les règles de sécurité réseau et les règles de sécurité réseau efficaces
    - Mise à jour du paramètre Add-AzureRmNetworkSecurityRuleConfig : mise à jour des paramètres SourcePortRange, DestinationPortRange et SourceAddressPrefix pour accepter une liste de chaînes
    - Mise à jour du paramètre New-AzureRmNetworkSecurityRuleConfig : mise à jour des paramètres SourcePortRange, DestinationPortRange et SourceAddressPrefix pour accepter une liste de chaînes
    - Mise à jour du paramètre Set-AzureRmNetworkSecurityRuleConfig : mise à jour des paramètres SourcePortRange, DestinationPortRange et SourceAddressPrefix pour accepter une liste de chaînes
    - Mise à jour du paramètre Add-AzureRmNetworkSecurityRuleConfig : mise à jour des paramètres SourcePortRange, DestinationPortRange et SourceAddressPrefix pour accepter une liste de chaînes
    - Mise à jour du paramètre New-AzureRmNetworkSecurityGroup : mise à jour du paramètre SecurityRules pour accepter les paramètres SourcePortRange, DestinationPortRange et SourceAddressPrefix, qui sont des listes de chaînes dans l’objet PSSecurityRule
    - Mise à jour du paramètre Get-AzureRmEffectiveNetworkSecurityGroup : ajout du paramètre TagMap
    - Mise à jour du paramètre Get-AzureRmEffectiveNetworkSecurityGroup : mise à jour de l’objet PSEffectiveSecurityRule retourné avec les paramètres SourcePortRange, DestinationPortRange et SourceAddressPrefix, qui sont des listes de chaînes.
  * Ajout de la prise en charge de la protection DDOS pour les réseaux virtuels
    - Mise à jour du paramètre New-AzureRmVirtualNetwork : ajout des paramètres booléens EnableDDoSProtection et EnableVmProtection
    - Ajout des propriétés EnableDDoSProtection et EnableVmProtection dans l’objet PSVirtualNetwork
  * Ajout de la prise en charge de l’équilibreur de charge interne à haute disponibilité
    - Mise à jour du paramètre Add-AzureRmLoadBalancerRuleConfig : ajout de l’élément All comme valeur acceptable pour le paramètre Protocol
    - Mise à jour du paramètre New-AzureRmLoadBalancerRuleConfig : ajout de l’élément All comme valeur acceptable pour le paramètre Protocol
    - Mise à jour du paramètre Set-AzureRmLoadBalancerRuleConfig : ajout de l’élément All comme valeur acceptable pour le paramètre Protocol
  * Ajout de la prise en charge de groupes de sécurité d’application
    - Ajout du paramètre New-AzureRmApplicationSecurityGroup
    - Ajout du paramètre Get-AzureRmApplicationSecurityGroup
    - Ajout du paramètre Remove-AzureRmApplicationSecurityGroup
    - Mise à jour du paramètre New-AzureRmNetworkInterface : ajout des paramètres optionnels ApplicationSecurityGroup et ApplicationSecurityGroupId
    - Mise à jour du paramètre New-AzureRmNetworkInterfaceIpConfig : ajout des paramètres optionnels ApplicationSecurityGroup et ApplicationSecurityGroupId
    - Mise à jour du paramètre Add-AzureRmNetworkInterfaceIpConfig : ajout des paramètres optionnels ApplicationSecurityGroup et ApplicationSecurityGroupId
    - Mise à jour du paramètre Set-AzureRmNetworkInterfaceIpConfig : ajout des paramètres optionnels ApplicationSecurityGroup et ApplicationSecurityGroupId
    - Mise à jour du paramètre New-AzureRmNetworkSecurityRuleConfig : ajout des paramètres optionnels SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup et DestinationApplicationSecurityGroupId
    - Mise à jour du paramètre Add-AzureRmNetworkSecurityRuleConfig : ajout des paramètres optionnels SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup et DestinationApplicationSecurityGroupId
    - Mise à jour du paramètre Set-AzureRmNetworkSecurityRuleConfig : ajout des paramètres optionnels SourceApplicationSecurityGroup, SourceApplicationSecurityGroupId, DestinationApplicationSecurityGroup et DestinationApplicationSecurityGroupId
  * Ajout de nouvelles commandes pour les scripts VpnDeviceConfiguration
    - Get-AzureRmVirtualNetworkGatewaySupportedVpnDevices
    - Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript
* Profil
  * Prise en charge de Start-Job pour les cmdlets AzureRM.
    * Toutes les cmdlets AzureRM ajoutent le paramètre -AzureRmContext, qui peut accepter un contexte (sortie d’une cmdlet de contexte).
      - Modèle commun pour les tâches avec la conservation de contexte DÉSACTIVÉE : `Start-Job {param ($context) New-AzureRmVM -AzureRmContext $context [... other parameters]} -ArgumentList (Get-AzureRmContext)`
      - Modèle commun pour les tâches avec la conservation de contexte ACTIVÉE : `Start-Job {New-AzureRmVM [... other parameters]}`
  * Conservation des informations de connexion d’une session à l’autre, nouvelles cmdlets :
    - Enable-AzureRmContextAutosave : active la conservation de connexion d’une session à l’autre.
    - Disable-AzureRmContextAutosave : désactive la conservation de connexion d’une session à l’autre.
  * Gestion des informations de contexte, nouvelles cmdlets
    - Select-AzureRmContext : sélectionne le contexte nommé actif.
    - Rename-AzureRmContext : renomme un contexte existant pour le retrouver facilement.
    - Remove-AzureRmContext : supprime un contexte existant.
    - Remove-AzureRmAccount : supprime toutes les informations d’identification, abonnements et clients associés à un compte.
  * Gestion d’informations de contexte, modifications apportées aux cmdlets :
    - Ajout du paramètre Scope = (Process | CurrentUser) à toutes les cmdlets qui modifient les informations d’identification
    - Get-AzureRmContext : ajout du paramètre ListAvailable pour répertorier tous les contextes sauvegardés
* Ressources
  * Ajout des cmdlets PolicySetDefinition
    - New-AzureRmPolicySetDefinition : cmdlet pour créer une définition d’ensemble de stratégies
    - Get-AzureRmPolicySetDefinition : cmdlet pour répertorier toutes les définitions d’ensemble de stratégies ou pour obtenir une définition d’ensemble de stratégies spécifique
    - Remove-AzureRmPolicySetDefinition : cmdlet pour supprimer une définition d’ensemble de stratégies
    - Set-AzureRmPolicySetDefinition : cmdlet pour mettre à jour une définition d’ensemble de stratégies existant
  * Ajout des paramètres -PolicySetDefinition, -Sku et -NotScope aux cmdlets New-AzureRmPolicyAssignment et Set-AzureRmPolicyAssignment
  * Ajout de la prise en charge de transmission d’URL de stratégie aux cmdlets New-AzureRmPolicyDefinition et Set-AzureRmPolicyDefinition
  * Ajout du paramètre -Mode à la cmdlet New-AzureRmPolicyDefinition
  * Ajout de la prise en charge de la suppression d’affectation de rôle à l’aide de l’objet PSRoleAssignment
    - Les utilisateurs peuvent désormais utiliser l’objet d’entrée PSRoleassignment avec la commandlet Remove-AzureRMRoleAssignment pour supprimer l’affectation de rôle.
  * Ajouter des cmdlets ManagedApplication
    - New-AzureRmManagedApplication : cmdlet pour créer une application gérée
    - Get-AzureRmManagedApplication : cmdlet pour répertorier toutes les applications gérées d’un abonnement ou pour obtenir une application gérée spécifique
    - Remove-AzureRmManagedApplication : cmdlet pour supprimer une application gérée
    - Set-AzureRmManagedApplication : cmdlet pour mettre à jour une application gérée existante
  * Ajout des cmdlets ManagedApplicationDefinition
    - New-AzureRmManagedApplicationDefinition : cmdlet pour créer une définition d’application gérée à l’aide d’une URI de fichier zip ou des fichiers JSON mainTemplate et createUiDefinition
    - Get-AzureRmManagedApplicationDefinition : cmdlet pour répertorier toutes les définitions d’application gérée d’un groupe de ressources ou pour obtenir une définition d’application gérée spécifique
    - Remove-AzureRmManagedApplicationDefinition : cmdlet pour supprimer une définition d’application gérée
    - Set-AzureRmManagedApplicationDefinition : cmdlet pour mettre à jour une définition d’application gérée existante
* SQL
  * Ajout de la prise en charge des règles de réseau virtuel
    - Ajout de la cmdlet Get-AzureRmSqlServerVirtualNetworkRule qui obtient les règles de réseau virtuel par un nom de règle spécifique ou une liste de règles de réseau virtuel dans un serveur Azure SQL.
    - Ajout de la cmdlet Set-AzureRmSqlServerVirtualNetworkRule qui modifie le réseau virtuel visé par la règle.
    - Ajout de la cmdlet Remove-AzureRmSqlServerVirtualNetworkRule qui supprime une règle de réseau virtuel d’un serveur Azure SQL.
    - Ajout de la cmdlet New-AzureRmSqlServerVirtualNetworkRule qui crée une règle de réseau virtuel pour un serveur Azure SQL.
* Sites web
  * Ajout du niveau PremiumV2 pour les plans App Service
* Azure.Storage
  * Mise à niveau vers Azure Storage Client Library 8.4.0 et Azure Storage Data Movement Library 0.6.1
  * Ajout de la prise en charge de PremiumPageBlobTier dans l’API de chargement et de copie d’objet blob
    - Set-AzureStorageBlobContent
    - Start-AzureStorageBlobCopy
  * Définition plus fine du format de sortie de la console d’AzureStorageContainer, AzureStorageBlob, AzureStorageQueue et AzureStorageTable
    - Get-AzureStorageContainer
    - Get-AzureStorageBlob
    - Get-AzureStorageQueue
    - Get-AzureStorageTable

## <a name="20170810---version-431"></a>10.08.2017 - Version 4.3.1
  * Mise à jour pour résoudre le problème de signature d’assembly

## <a name="20170807---version-430"></a>07/08/2017 - Version 4.3.0
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
  * Ajout de la prise en charge de la gestion des versions de build NodeConfiguration dans StartAzureAutomationDscCompilationJob et ImportAzureAutomationDscNodeConfiguration
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
  * Mise à jour des applets de commande avec les jeux de paramètres pour Namespace et EventHub dans l’opération d’AuthorizationRule
    - New-AzureRmEventHubAuthorizationRule - Ajoute une nouvelle règle AuthorizationRule au NameSpace ou EventHub existant.
    - Get-AzureRmEventHubAuthorizationRule - Obtient la règle AuthorizationRule / la liste des AuthorizationRules pour le NameSpace ou l’EventHub existant.
    - Set-AzureRmEventHubAuthorizationRule - Met à jour les propriétés de la règle AuthorizationRule existante de l’EventHub NameSpace.
    - Remove-AzureRmEventHubAuthorizationRule - Supprime la règle AuthorizationRule existante du NameSpace ou de l’EventHub existant.
    - New-AzureRmEventHubKey - Génère une nouvelle clé principale/secondaire pour la règle AuthorizationRule du NameSpace ou de l’EventHub existant.
    - Get-AzureRmEventHubKey - Obtient la clé principale/secondaire pour la règle AuthorizationRule du NameSpace ou de l’EventHub existant.
* Réseau
    * Ajout de la prise en charge d’IPv6 et du nouveau paramètre facultatif - PeerAddressType
      * New-AzureRmExpressRouteCircuitPeeringConfig :
      * Set-AzureRmExpressRouteCircuitPeeringConfig : ajout de la prise en charge d’IPv6. Nouveau paramètre facultatif ajouté
      * Remove-AzureRmExpressRouteCircuitPeeringConfig : ajout de la prise en charge d’IPv6. Nouveau paramètre facultatif ajouté
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
     - New-AzureRmServiceBusAuthorizationRule - Ajoute une nouvelle règle AuthorizationRule au NameSpace/Queue/Topic ServiceBus existant.
     - Get-AzureRmServiceBusAuthorizationRule - Obtient une règle AuthorizationRule / la liste des AuthorizationRules pour le NameSpace/Queue/Topic ServiceBus existant.
     - Set-AzureRmServiceBusAuthorizationRule - Met à jour les propriétés de la règle AuthorizationRule existante du NameSpace/Queue/Topic ServiceBus.
     - New-AzureRmServiceBusKey - Génère une nouvelle clé principale/secondaire pour la règle AuthorizationRule du NameSpace/Queue/Topic ServiceBus existant.
     - Get-AzureRmServiceBusKey - Obtient une clé principale/secondaire pour la règle AuthorizationRule du NameSpace/Queue/Topic ServiceBus existant.
     - Remove-AzureRmServiceBusNameSpaceAuthorizationRule - Supprime la règle AuthorizationRule existante du NameSpace/Queue/Topic ServiceBus existant.
    * Ajout de la propriété ResourceGroup à NamespaceAttributes
* SQL
    * Mise à jour de Set-AzureRmSqlServerTransparentDataEncryptionProtector pour afficher un avertissement et demander confirmation que le Type du protecteur de chiffrement est bien défini sur AzureKeyVault
    * Ajout de nouvelles applets de commande mises à jour pour les paramètres d’audit
      - L’applet de commande Get-AzureRmSqlDatabaseAuditing qui obtient les paramètres d’audit d’une base de données SQL Azure.
      - L’applet de commande Get-AzureRmSqlServerAuditing qui obtient les paramètres d’audit d’un serveur SQL Azure.
      - L’applet de commande Set-AzureRmSqlDatabaseAuditing qui modifie les paramètres d’audit pour une base de données SQL Azure.
      - L’applet de commande Set-AzureRmSqlServerAuditing qui modifie les paramètres d’audit d’un serveur SQL Azure.
    * Dépréciation des applets de commande de stratégie d’audit existantes
      - Get-AzureRmSqlDatabaseAuditingPolicy
      - Get-AzureRmSqlServerAuditingPolicy
      - Set-AzureRmSqlDatabaseAuditingPolicy
      - Set-AzureRmSqlServerAuditingPolicy
      - Use-AzureRmSqlServerAuditingPolicy
      - Remove-AzureRmSqlDatabaseAuditing
      - Remove-AzureRmSqlServerAuditing
    * L’analyse du fichier de schéma pour Update-AzureRmSqlSyncGroup ne tient désormais plus compte de la casse.
* Storage
    * Ajout de la prise en charge de NeworkRule aux applets de commande de compte de stockage du mode de ressources
      - New-AzureRmStorageAccount
      - Set-AzureRmStorageAccount
      - Get-AzureRmStorageAccountNetworkRuleSet
      - Update-AzureRmStorageAccountNetworkRuleSet
      - Add-AzureRmStorageAccountNetworkRule
      - Remove-AzureRmStorageAccountNetworkRule

## <a name="20170717---version-421"></a>17/07/2017 - Version 4.2.1
* Calcul
    - Correction d’un problème avec le disque de machine virtuelle et les applets de commande create et update de capture instantanée de disque de machine virtuelle, (lien) [https://github.com/azure/azure-powershell/issues/4309]
      - New-AzureRmDisk
      - New-AzureRmSnapshot
      - Update-AzureRmDisk
      - Update-AzureRmSnapshot
* Profil
    - Correction d’un problème avec l’authentification des utilisateurs non interactifs dans RDFE (lien) [https://github.com/Azure/azure-powershell/issues/4299]
* ServiceManagement
    - Correction d’un problème avec l’authentification des utilisateurs non interactifs (lien) [https://github.com/Azure/azure-powershell/issues/4299]

## <a name="2017711---version-420"></a>11/07/2017 - Version 4.2.0
* AnalysisServices
    * Ajout d’une nouvelle API dataplane
        - Introduction de l’API pour récupérer le journal du serveur Analysis Services, Export-AzureAnalysisServicesInstanceLog
* Automatisation
    * Paramétrage correct de la valeur TimeZone pour les planifications hebdomadaires et mensuelles pour New-AzureRmAutomationSchedule
        - Des informations supplémentaires sont disponibles pour le problème : https://github.com/Azure/azure-powershell/issues/3043
* AzureBatch
    - Ajout d’une nouvelle applet de commande Get-AzureBatchJobPreparationAndReleaseTaskStatus.
    - Ajout du début et de la fin de la plage d’octets aux paramètres Get-AzureBatchNodeFileContent.
* CognitiveServices
    * Intégration avec le kit SDK de gestion Cognitive Services version 1.0.0.
    * Correction d’un bogue de vérification de la longueur du nom de compte.
* Calcul
    * Prise en charge du type de compte de stockage pour le disque de l’image :
        - Ajout du paramètre « StorageAccountType » à Set-AzureRmImageOsDisk et Add-AzureRmImageDataDisk
    * Fonctionnalité PrivateIP et PublicIP dans la configuration IP de VMSS :
        - Ajout des noms « PrivateIPAddressVersion », « PublicIPAddressConfigurationName », « PublicIPAddressConfigurationIdleTimeoutInMinutes », « DnsSetting » à New-AzureRmVmssIpConfig
        - Ajout du paramètre « PrivateIPAddressVersion » pour la spécification IPv4 ou IPv6 à New-AzureRmVmssIpConfig
    * Fonctionnalité de maintenance des performances :
        - Ajout du paramètre de commutateur « PerformMaintenance » à Restart-AzureRmVM.
        - Get-AzureRmVM -Status affiche les informations de maintenance des performances de la machine virtuelle donnée
    * Fonctionnalité d’identité de la machine virtuelle :
        - Ajout du paramètre « IdentityType » à New-AzureRmVMConfig et UpdateAzureRmVM
        - Get-AzureRmVM affiche les informations de l’identité de la machine virtuelle donnée
    * Fonctionnalité d’identité VMSS :
        - Le paramètre « IdentityType » a été ajouté à New-AzureRmVmssConfig
        - Get-AzureRmVmss affiche les informations de l’identité de la machine virtuelle VMSS donnée
    * Fonctionnalité de diagnostic de démarrage VMSS :
        - Nouvelle applet de commande pour la définition des diagnostics de démarrage de l’objet VMSS : Set-AzureRmVmssBootDiagnostics
        - Ajout du paramètre « BootDiagnostic » à New-AzureRmVmssConfig
    * Fonctionnalité LicenseType VMSS :
        - Ajout du paramètre « LicenseType » à New-AzureRmVmssConfig
    * Prise en charge de RecoveryPolicyMode :
        - Ajout du paramètre « RecoveryPolicyMode » à New-AzureRmVmssConfig
    * Fonctionnalité SKU de ressources de calcul :
        - La nouvelle applet de commande « Get-AzureRmComputeResourceSku » répertorie toutes les références (SKU) des ressources de calcul
* DataFactories
    * New-AzureRmDataFactoryGatewayKey est déconseillé
    * Introduction de la fonctionnalité de clé d’authentification de passerelle via l’ajout de New-AzureRmDataFactoryGatewayAuthKey et de Get-AzureRmDataFactoryGatewayAuthKey
* DataLakeAnalytics
    * Ajout de la prise en charge des opérations CRUD de stratégie de calcul avec les commandes suivantes :
        - New-AzureRMDataLakeAnalyticsComputePolicy
        - Get-AzureRMDataLakeAnalyticsComputePolicy
        - Remove-AzureRMDataLakeAnalyticsComputePolicy
        - Update-AzureRMDataLakeAnalyticsComputePolicy
    * Ajout de la prise en charge des métadonnées de relation de travail pour fournir de l’aide avec les tâches récurrentes et les pipelines de travail. Les commandes suivantes ont été mises à jour ou ajoutées :
        - Submit-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJob
        - Get-AzureRMDataLakeAnalyticsJobRecurrence
        - Get-AzureRMDataLakeAnalyticsJobPipeline
    * L’audience du jeton a été mise à jour pour les API de catalogue et de travaux afin d’utiliser l’audience spécifique Data Lake correcte à la place de l’audience des ressources Azure.
* DataLakeStore
    * La prise en charge des rotations de clés KeyVault gérées par l’utilisateur a été ajoutée dans l’applet de commande Set-AzureRMDataLakeStoreAccount
    * Une mise à jour de la qualité de vie a été ajoutée pour déclencher automatiquement un appel `enableKeyVault` quand un coffre de clés géré par l’utilisateur est ajouté ou qu’une clé est tournée.
    * L’audience du jeton a été mise à jour pour les API de catalogue et de travaux afin d’utiliser l’audience spécifique Data Lake correcte à la place de l’audience des ressources Azure.
    * Correction d’un bogue limitant la taille des fichiers créés/ajoutés à l’aide des applets de commande suivantes :
        - New-AzureRmDataLakeStoreItem
        - Add-AzureRmDataLakeStoreItemContent
* DNS
    * Correction d’un bogue dans le scénario de redirection pour Get-AzureRmDnsZone
        - Des informations supplémentaires sont disponibles ici : https://github.com/Azure/azure-powershell/issues/4203
* HDInsight
    * Ajout de la prise en charge pour activer/désactiver Operations Management Suite(OMS)
    * Nouvelles applets de commande
        - Enable-AzureRmHDInsightOperationsManagementSuite
        - Disable-AzureRmHDInsightOperationsManagementSuite
        - Get-AzureRmHDInsightOperationsManagementSuite
    * Ajout de nouveaux paramètres pour définir des configurations personnalisées Spark à Add-AzureRmHDInsightConfigValues
        - Paramètres SparkDefaults et SparkThriftConf pour Spark 1.6
        - Paramètres Spark2Defaults et Spark2ThriftConf pour Spark 2.0
* Insights
    * Problème #4215 (demande de modification) : suppression de la limite de 15 jours dans la fenêtre de temps pour l’applet de commande Get-AzureRmLog. Modifications mineures des noms de tests unitaires.
    * Correction du problème #3957 pour Get-AzureRmLog
        - Problème #1 : Le serveur back-end renvoie les enregistrements dans des pages de 200 enregistrements chacune, liées par le jeton de continuation à la page suivante. Les clients voyaient l’applet de commande renvoyer uniquement 200 enregistrements alors qu’ils savaient qu’il en existait plus. Cela se produisait quelle que soit la valeur qu’ils définissaient pour MaxEvents, sauf si cette valeur était inférieure à 200.
        - Problème #2 : La documentation contenait des données erronées sur cette applet de commande, par exemple : la fenêtre de temps par défaut était de 1 heure.
        - Correctif #1 : L’applet de commande suit désormais le jeton de continuation retourné par le serveur back-end jusqu’à ce qu’il atteigne MaxEvents ou la fin de l’ensemble.<br>La valeur par défaut pour MaxEvents est comprise entre 1000 et sa valeur maximale, 100 000. Toute valeur de MaxEvents inférieure à 1 est ignorée et la valeur par défaut est utilisée à la place. Ces valeurs et ce comportement n’ont pas changé. Ils sont correctement documentés maintenant.<br>Un alias de MaxEvents a été ajouté (MaxRecords), étant donné que le nom de l’applet de commande ne mentionne plus les événements, mais seulement les journaux.
        - Correctif #2 : La documentation contient des informations correctes et plus détaillées : un nouvel alias, une fenêtre horaire correcte, des valeurs par défaut, minimales et maximales correctes.
* KeyVault
    * Suppression de l’adresse e-mail à partir de la requête d’annuaire quand -UserPrincipalName est spécifié pour les applets de commande Set-AzureRMKeyVaultAccessPolicy et Remove-AzureRMKeyVaultAccessPolicy.
      - Les deux applets de commande ont maintenant un paramètre -EmailAddress qui peut être utilisé à la place du paramètre -UserPrincipalName lorsqu’il est approprié d’exécuter une requête pour obtenir l’adresse e-mail.  S’il existe plusieurs adresses e-mail correspondantes dans l’annuaire, l’applet de commande échoue.
* Réseau
    * New-AzureRmIpsecPolicy : SALifeTimeSeconds et SADataSizeKilobytes ne sont plus des paramètres obligatoires
        - Par défaut, SALifeTimeSeconds a pour valeur 27 000 secondes
        - Par défaut, SADataSizeKilobytes a pour valeur 102 400 000 Ko
    * Ajout de la prise en charge de la configuration de suite de chiffrement personnalisée à l’aide de la stratégie ssl et de l’API répertoriant toutes les options ssl dans Application Gateway
        - Ajout du paramètre facultatif -PolicyType, -PolicyName, -MinProtocolVersion, -Ciphersuite
            - Add-AzureRmApplicationGatewaySslPolicy
            - New-AzureRmApplicationGatewaySslPolicy
            - Set-AzureRmApplicationGatewaySslPolicy
        - Ajout de Get-AzureRmApplicationGatewayAvailableSslOptions (Alias : List-AzureRmApplicationGatewayAvailableSslOptions)
        - Ajout de Get-AzureRmApplicationGatewaySslPredefinedPolicy (Alias : List-AzureRmApplicationGatewaySslPredefinedPolicy)
    * Ajout de la prise en charge de la redirection dans Application Gateway
        - Ajout de Add-AzureRmApplicationGatewayRedirectConfiguration
        - Ajout de Get-AzureRmApplicationGatewayRedirectConfiguration
        - Ajout de New-AzureRmApplicationGatewayRedirectConfiguration
        - Ajout de Remove-AzureRmApplicationGatewayRedirectConfiguration
        - Ajout de Set-AzureRmApplicationGatewayRedirectConfiguration
        - Ajout du paramètre facultatif -RedirectConfiguration
            - Add-AzureRmApplicationGatewayRequestRoutingRule
            - New-AzureRmApplicationGatewayRequestRoutingRule
            - Set-AzureRmApplicationGatewayRequestRoutingRule
        - Ajout du paramètre facultatif -DefaultRedirectConfiguration
            - Add-AzureRmApplicationGatewayUrlPathMapConfig
            - New-AzureRmApplicationGatewayUrlPathMapConfig
            - Set-AzureRmApplicationGatewayUrlPathMapConfig
        - Ajout du paramètre facultatif -RedirectConfiguration
            - Add-AzureRmApplicationGatewayPathRuleConfig
            - New-AzureRmApplicationGatewayPathRuleConfig
            - Set-AzureRmApplicationGatewayPathRuleConfig
        - Ajout du paramètre facultatif -RedirectConfigurations
            - New-AzureRmApplicationGateway
            - Set-AzureRmApplicationGateway
    * Ajout de la prise en charge des sites web Azure dans Application Gateway
        - Ajout de New-AzureRmApplicationGatewayProbeHealthResponseMatch
        - Ajout des paramètres facultatifs -PickHostNameFromBackendHttpSettings, -MinServers, -Match
            - Add-AzureRmApplicationGatewayProbeConfig
            - New-AzureRmApplicationGatewayProbeConfig
            - Set-AzureRmApplicationGatewayProbeConfig
        - Ajout des paramètres facultatifs -PickHostNameFromBackendAddress, -AffinityCookieName, -ProbeEnabled, -Path
            - Add-AzureRmApplicationGatewayBackendHttpSettings
            - New-AzureRmApplicationGatewayBackendHttpSettings
            - Set-AzureRmApplicationGatewayBackendHttpSettings
    * Mise à jour de Get-AzureRmPublicIPaddress pour récupérer les ressources publicipaddress créées via le groupe de machines virtuelles identiques
    * Ajout d’une applet de commande pour obtenir l’utilisation actuelle du réseau virtuel
        - Get-AzureRmVirtualNetworkUsageList
* Profil
    * Correction de l’erreur lors de l’utilisation d’Import-AzureRmContext ou de Save-AzureRmContext
        - Des informations supplémentaires sont disponibles pour le problème : https://github.com/Azure/azure-powershell/issues/3954
* RecoveryServices.SiteRecovery
    * Introduction d’un nouveau module pour les opérations Azure Site Recovery.
        - Toutes les applets de commande commencent par AzureRmRecoveryServicesAsr*
* SQL
    * Ajout d’applets de commande PowerShell de synchronisation des données à AzureRM.Sql
    * Mise à jour des applets de commande AzureRmSqlServer pour utiliser une nouvelle version de l’API REST qui permet d’éviter l’expiration des délais d’attente lors de la création d’un serveur.
    * Les applets de commande de mise à niveau de serveur sont déconseillées car l’ancienne version du serveur (2.0) n’existe plus.
    * Ajout d’un nouveau paramètre de commutateur facultatif « AssignIdentity » aux applets de commande New-AzureRmSqlServer et Set-AzureRmSqlServer pour prendre en charge l’approvisionnement d’une identité de ressource pour la ressource SQL Server
    * Le paramètre ResourceGroupName est désormais facultatif pour Get-AzureRmSqlServer
        - Des informations supplémentaires sont disponibles pour le problème suivant : https://github.com/Azure/azure-powershell/issues/635
* ServiceManagement pour ExpressRoute :
    * L’applet de commande New-AzureBgpPeering a été mise à jour pour ajouter les nouvelles options suivantes :
        - PeerAddressType : la valeur « IPv4 » ou « IPv6 » peut être spécifiée pour créer une homologation BGP du type de famille d’adresses correspondant
    * L’applet de commande Set-AzureBgpPeering a été mise à jour pour ajouter les nouvelles options suivantes :
        - PeerAddressType : la valeur « IPv4 » ou « IPv6 » peut être spécifiée pour mettre à jour l’homologation BGP du type de famille d’adresses correspondant
    * L’applet de commande Remove-AzureBgpPeering a été mise à jour pour ajouter les nouvelles options suivantes :
        - PeerAddressType : la valeur « IPv4 », « IPv6 » ou All peut être spécifiée pour supprimer l’homologation BGP du type de famille d’adresses correspondant ou de tous les types de famille d’adresses

## <a name="20170607---version-410"></a>07/06/2017 - Version 4.1.0
* AnalysisServices
    * Ajout des nouvelles références SKU : B1, B2, S0
    * Ajout de la prise en charge de la montée/descente en puissance
* CognitiveServices
    * Mise à jour de l’affichage détaillé des contrats de licence lors de la création de ressources Cognitive Services
* Calcul
    * Correction de Test-AzureRmVMAEMExtension pour les machines virtuelles avec plusieurs disques gérés
    * Mise à jour de Set-AzureRmVMAEMExtension : ajout d’informations de mise en cache pour les disques gérés Premium
    * Add-AzureRmVhd : la limite de taille sur le disque dur virtuel a été augmentée à 4 To.
    * Stop-AzureRmVM : clarifier la documentation pour le paramètre STayProvisioned
    * New-AzureRmDiskUpdateConfig
      * Paramètres déconseillés : CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmDiskUpdateImageReference : applet de commande déconseillée
    * New-AzureRmSnapshotUpdateConfig
      * Paramètres déconseillés : CreateOption, StorageAccountId, ImageReference, SourceUri, SourceResourceId
    * Set-AzureRmSnapshotUpdateImageReference : applet de commande déconseillée
* DataLakeStore
    * Enable-AzureRmDataLakeStoreKeyVault (Enable-AdlStoreKeyVault)
      * Activation du chiffrement géré de KeyVault pour un magasin DataLake
* DevTestLabs
    * Mise à jour des applets de commande pour fonctionner avec les versions de l’API DevTest Labs actuelle et mise à jour.
* IotHub
    * Ajout de la prise en charge du routage pour les applets de commande IoTHub
* KeyVault
  * Nouvelles applets de commande pour prendre en charge les clés de compte de stockage géré KeyVault
    * Get-AzureKeyVaultManagedStorageAccount
    * Add-AzureKeyVaultManagedStorageAccount
    * Remove-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccount
    * Update-AzureKeyVaultManagedStorageAccountKey
    * Get-AzureKeyVaultManagedStorageSasDefinition
    * Set-AzureKeyVaultManagedStorageSasDefinition
    * Remove-AzureKeyVaultManagedStorageSasDefinition
* Réseau
    * Get-AzureRmNetworkUsage : nouvelle applet de commande pour afficher les détails de capacité et d’utilisation du réseau
    * Ajout de nouvelles options GatewaySku pour VirtualNetworkGateways
        * VpnGw1, VpnGw2, VpnGw3 sont les nouvelles références SKU ajoutées pour les passerelles VPN
    * Set-AzureRmNetworkWatcherConfigFlowLog
      * Exemples d’aide corrigés
* NotificationHubs
    * Mise à jour transparente des applets de commande NotificationHubs pour la nouvelle API
* Profil
    * Resolve-AzureRmError
      * Nouvelle applet de commande pour afficher les détails des erreurs et des exceptions levées par les applets de commande, y compris les données de demande/réponse du serveur
    * Send-Feedback
      * Activation de l’envoi de commentaires sans ouvrir de session
    * Get-AzureRmSubscription
      * Correction d’un bogue lors de la récupération des abonnements CSP
* Ressources
    * Correction d’un problème dans le cadre duquel Get-AzureRMRoleAssignment générait une requête incorrecte si le nombre d’attributions de rôles était supérieur à 1 000
        * Les utilisateurs peuvent désormais utiliser Get-AzureRMRoleAssignment même si le nombre d’attributions de rôles à retourner est supérieur à 1 000
* SQL
    * Restore-AzureRmSqlDatabase : exemple de documentation de mise à jour
* Storage
    * Ajout de la prise en charge du paramètre AssignIdentity aux applets de commande de compte de stockage du mode de ressources
        * New-AzureRmStorageAccount
        * Set-AzureRmStorageAccount
    * Ajout de la prise en charge de la clé du client aux applets de commande de compte de stockage du mode de ressources
        * Set-AzureRmStorageAccount
        * New-AzureRmStorageAccountEncryptionKeySource
* TrafficManager

    * Nouveaux paramètres de moniteur « MonitorIntervalInSeconds », « MonitorTimeoutInSeconds », « MonitorToleratedNumberOfFailures »
    * Nouveau protocole de moniteur « TCP »
* ServiceManagement
    * Add-AzureVhd : la limite de taille sur le disque dur virtuel a été augmentée à 4 To.
    * New-AzureBGPPeering : prise en charge de LegacyMode
* Azure.Storage
    * Mise à jour de l’aide pour les paramètres qui acceptent des caractères génériques et mise à jour du type StorageContext

## <a name="20170523---version-402"></a>23/05/2017 - Version 4.0.2
* Profil
    * Add-AzureRmAccount
      * Ajout de l’alias de paramètre `-EnvironmentName` pour la compatibilité descendante avec les versions 2.x d’AzureRM.profile

## <a name="20170512---version-401"></a>12/05/2017 - Version 4.0.1
 * Correction d’un problème avec New-AzureStorageContext dans les scénarios hors connexion : https://github.com/Azure/azure-powershell/issues/3939

## <a name="20170510---version-400"></a>10/05/2017 - Version 4.0.0


* Cette version contient des modifications conséquentes. Consultez [le guide de migration](https://aka.ms/azps-migration-guide) pour connaître les détails des changements et leur impact sur les scripts existants.
* ApiManagement
  - Prise en charge ajoutée pour la configuration de groupes externes dans New-AzureRmApiManagementGroup.
* Facturation
  - Nouvelle applet de commande Get-AzureRmBillingPeriod
    + applet de commande pour récupérer les périodes de facturation Azure de l’abonnement.
  - Mise à jour de l’applet de commande Get-AzureRmBillingInvoice
  - nouvelle propriété BillingPeriodNames
  - sortie dans affichage de liste
* Calcul
  - Mise à jour des applets de commande Set-AzureRmVMAEMExtension et Test-AzureRmVMAEMExtension pour prendre en charge les disques gérés Premium
  - Paramètres de chiffrement de sauvegarde pour les machines virtuelles IaaS et restauration en cas d’échec
  - L’option ChefServiceInterval est renommée en ChefDaemonInterval maintenant. L’ancien continuera à fonctionner, cependant.
  - Suppression des propriétés DataDiskNames et NetworkInterfaceIDs en double de l’objet de machine virtuelle PS.
  - Paramètres DataDiskNames et NetworkInterfaceIDs rendus facultatifs dans Remove-AzureRmVMDataDisk et Remove-AzureRmVMNetworkInterface, respectivement.
  - Corrigez le problème de combinaison d’applets de commande Get quand les applets de commande Get retournent un objet de liste.
  - Les applets de commande qui sont en conflit avec les applets de commande RDFE ont été renommées. Consultez la page du problème https://github.com/Azure/azure-powershell/issues/2917 pour plus de détails
    + `New-AzureVMSqlServerAutoBackupConfig` a été renommé en `New-AzureRmVMSqlServerAutoBackupConfig`
    + `New-AzureVMSqlServerAutoPatchingConfig` a été renommé en `New-AzureRmVMSqlServerAutoPatchingConfig`
    + `New-AzureVMSqlServerKeyVaultCredentialConfig` a été renommé en `New-AzureRmVMSqlServerKeyVaultCredentialConfig`
* Consommation
  - Nouvelle applet de commande Get-AzureRmConsumptionUsageDetail
    + applet de commande pour récupérer les détails de l’utilisation de l’abonnement.
* ContainerRegistry
  - Ajout d’applets de commande PowerShell pour Azure Container Registry
    + New-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistry
    + Update-AzureRmContainerRegistry
    + Remove-AzureRmContainerRegistry
    + Get-AzureRmContainerRegistryCredential
    + Update-AzureRmContainerRegistryCredential
    + Test-AzureRmContainerRegistryNameAvailability
* DataLakeAnalytics
  - Ajout de la prise en charge des fonctions d’obtention et de récupération d’affichage de liste packages de catalogues
  - Ajoutez la prise en charge de l’affichage de liste des éléments de catalogue suivants d’ancêtres plus en profondeur :
    + Table
    + TVF
    + Affichage
    + Statistiques
* DataLakeStore
  - Pour `Import-AzureRMDataLakeStoreItem` et `Export-AzureRMDataLakeStoreItem`, la journalisation du suivi a été désactivée par défaut pour améliorer les performances. Si la journalisation du suivi est souhaitée, veuillez utiliser les paramètres `-DiagnosticLogLevel` et `-DiagnosticLogPath`
  - Correction d’un bogue qui provoquait parfois le plantage de PowerShell lors du téléchargement d’un grand nombre de petits fichiers vers ADLS.
* Event Hub
  - Résolution de bogue :
    + Correction de l’erreur de l’applet de commande Set-AzureRmEventHubNamespace « Tier » ne peut pas avoir la valeur Null. Il doit être défini sur « SkuName »
    + Set-AzureRmEventHub - Correction de l’erreur « La référence d'objet n'est pas définie à une instance d'un objet » lors de la mise à jour d’EventHub
* Insights
  - Add-AzureRm*AlertRule
    + Renvoie un objet unique : newResource, statusCode, requestId
  - Get-AzureRmAlertRule
    + La sortie est désormais énumérée au lieu d’être considérée comme un seul objet. Son type n’a pas changé, il s’agit toujours d’une liste.
  - Remove-AzureRmAlertRule
    + La valeur de statusCode suit le code d’état renvoyé par la requête (elle renvoyait toujours OK avant).
  - Add-AzureRmAutoscaleSetting
    + Renvoie désormais un statusCode contenant un objet unique (pas une liste comme avant), un requestId et la ressource nouvellement créée ou mise à jour.
    + La valeur de statusCode suit l’état renvoyé par la requête (elle renvoyait toujours OK avant).
  - New-AzureRmAutoscaleRule
    + Le paramètre ScaleActionType a été étendu, il reçoit désormais les valeurs suivantes : ChangeCount, PercentChangeCount, ExactCount.
  - Remove-AzureRmAutoscaleSetting
    + La valeur de statusCode dans la sortie suit le statusCode renvoyé par la demande. Avant, la valeur était toujours OK.
  - Get-AzureRMLogProfile
    + La sortie est maintenant énumérée. Avant, elle était considérée comme un seul objet. Le type de la sortie reste une liste, comme avant.
  - Remove-AzureRmLogProfile
    + Le paramètre PassThru a été implémenté.
  - API de métriques
    + Le kit de développement logiciel récupère maintenant les métriques depuis MDM.
  - Get-AzureRmMetricDefinition
    + La sortie est toujours une liste, mais la structure de la liste est modifiée.
  - Get-AzureRmMetric
    + L’appel a été modifié. Voici la nouvelle syntaxe : Get-AzureRmMetric ResourceId [MetricNames [TimeGrain] [AggregationType] [StartTime] [EndTime]] [DetailedOutput]
    + La sortie est une liste, et la structure de ses éléments a changé.
* KeyVault
  - Ajout de prise en charge de la sauvegarde/restauration des secrets KeyVault
    + Les secrets peuvent être sauvegardés et restaurés, comme pour la fonctionnalité actuellement prise en charge pour les clés

  - Les applets de commande de sauvegarde pour les clés et secrets acceptent désormais un objet correspondant en tant que paramètre d’entrée
    + L’appelant peut utiliser les opérations de sauvegarde et de récupération de chaîne : Get-AzureKeyVaultKey -VaultName myVault -Name myKey | Backup-AzureKeyVaultKey

  - Les applets de commande de sauvegarde prennent désormais en charge une option -Force pour remplacer un fichier existant
    + Notez que la tentative de remplacer un fichier existant ne lèvera plus d’erreur, et que l’utilisateur se verra demander comment poursuivre à la place.
* LogicApp
  - Nouveaux paramètres pour les applets de commande de récupération d’urgence de numéro de contrôle d’échange :
    + Paramètre -AgreementType facultatif (« X12 », ou « Edifact ») pour spécifier les numéros de contrôle pertinents
* MachineLearning
  - Utiliser la nouvelle version du SDK Azure Machine Learning .NET et ajouter une nouvelle applet de commande
    + Add-AzureRmMlWebServiceRegionalProperty
  - Corrections de texte mineures dans l’aide.
* Réseau
  - Applet de commande Test-AzureRmNetworkWatcherConnectivity ajoutée
    + Renvoie les informations de connexion pour une machine virtuelle source et une destination spécifiées
    + Si la connectivité entre la source et la destination ne peut pas être établie, l’applet de commande renvoie les détails relatifs au problème
* Profil
  - Ajout de l’applet de commande ’Send-Feedback’ : permet à un utilisateur de lancer un ensemble d’invites pour l’envoi de commentaires à l’équipe Azure PowerShell.
  - Les alias suivants ont été supprimés, car ils étaient en conflit avec des noms d’applet de commande existants dans le module Azure :
    + `Enable-AzureDataCollection` (pris en charge par `Enable-AzureRmDataCollection`)
    + `Disable-AzureDataCollection` (pris en charge par `Disable-AzureRmDataCollection`)
* Relais
  - Ajout à Azure Relay d’applets de commande qui permettent aux utilisateurs de créer et de gérer toutes les ressources Azure Relay.
    + `New-AzureRmRelayNamespace`
    + `Get-AzureRmRelayNamespace`
    + `Set-AzureRmRelayNamespace`
    + `Remove-AzureRmRelayNamespace`
    + `New-AzureRmWcfRelay`
    + `Get-AzureRmWcfRelay`
    + `Set-AzureRmWcfRelay`
    + `Remove-AzureRmWcfRelay`
    + `New-AzureRmRelayHybridConnection`
    + `Get-AzureRmRelayHybridConnection`
    + `Set-AzureRmRelayHybridConnection`
    + `Remove-AzureRmRelayHybridConnection`
    + `Test-AzureRmRelayName`
    + `Get-AzureRmRelayOperation`
    + `New-AzureRmRelayKey`
    + `Get-AzureRmRelayKey`
    + `New-AzureRmRelayAuthorizationRule`
    + `Get-AzureRmRelayAuthorizationRule`
    + `Set-AzureRmRelayAuthorizationRule`
    + `Remove-AzureRmRelayAuthorizationRule`
* Ressources
  - Prise en charge des déploiements sur plusieurs groupes de ressources pour New-AzureRmResourceGroupDeployment
    + Les utilisateurs peuvent désormais utiliser des déploiements imbriqués pour déployer sur différents groupes de ressources.
* ServiceBus

  - Correctif de bogue : les valeurs de propriété de file d’attente de ServiceBus étaient définies sur null, l’objet est utilisé en tant que paramètre d’entrée dans l’applet de commande Set-AzureRmServiceBusQueue pour mettre à jour la file d’attente.
   - Les propriétés affectées sont LockDuration, EntityAvailabilityStatus, DuplicateDetectionHistoryTimeWindow, MaxDeliveryCount et MessageCount
* ServiceFabric

  - Applets de commande ajoutées pour Service Fabric
    + Add-AzureRmServiceFabricApplicationCertificate       Ajout d’un certificat qui sera utilisé comme certificat d’application
    + Add-AzureRmServiceFabricClientCertificate       Ajout d’un nom ou d’une empreinte en commun pour les paramètres de cluster pour l’authentification client
    + Add-AzureRmServiceFabricClusterCertificate       Ajout d’un certificat de cluster secondaire au cluster pour régénérer le certificat existant
    + Add-AzureRmServiceFabricNodes       Ajout de nœuds/machines virtuelles d’un type de nœud spécifique à un cluster
    + Add-AzureRmServiceFabricNodeType       Ajout d’un type de nœud/de machines virtuelles à un cluster existant
    + Get-AzureRmServiceFabricCluster       Récupération des détails de la ressource de cluster
    + New-AzureRmServiceFabricCluster Création d’un nouveau cluster ServiceFabric. Cette commande a de nombreuses surcharges pour couvrir différents scénarios
    + Remove-AzureRmServiceFabricClientCertificate       Empêche un certificat client d’être utilisé pour accéder à un cluster
    + Remove-AzureRmServiceFabricClusterCertificate       Empêche un certificat de cluster d’être utilisé pour la sécurité du cluster
    + Remove-AzureRmServiceFabricNodes       Suppression de nœuds appartenant à un type spécifique d’un cluster
    + Remove-AzureRmServiceFabricNodeType       Suppression d’un type de nœud d’un cluster
    + Remove-AzureRmServiceFabricSettings       Suppression d’un ou plusieurs paramètres ServiceFabric d’un cluster
    + Set-AzureRmServiceFabricSettings       Ajout ou mise à jour d’un ou plusieurs paramètres ServiceFabric d’un cluster
    + Set-AzureRmServiceFabricUpgradeType       Modification du type de mise à niveau de ServiceFabric d’un cluster
    + Update-AzureRmServiceFabricDurability       Modification du niveau de durabilité d’un cluster
    + Update-AzureRmServiceFabricReliability       Modification du niveau de fiabilité d’un cluster
* SQL
  - Ajout du paramètre -SampleName à New-AzureRmSqlDatabase
  - Mises à jour des applets de commande de groupe de basculement
  - Suppression des paramètres ’Tag’
  - Suppression des paramètres 'PartnerResourceGroupName' et 'PartnerServerName' de l’applet de commande Remove-AzureRmSqlDatabaseFailoverGroup
  - Ajout d’un paramètre 'GracePeriodWithDataLossHours' aux applets de commande New- et Set-, qui finiront par remplacer « GracePeriodWithDataLossHour »
  - La documentation a été étoffée et mise à jour
  - Modification du format des objets retournés et correction des bogues à cause desquels les champs n’étaient pas toujours remplis
  - Ajout des propriétés 'DatabaseNames' et 'PartnerLocation' à l’objet groupe de basculement
  - Correction du bogue qui faisait que l’applet de commande Switch- se terminait immédiatement au lieu d’attendre la fin de l’opération
  - Correction du bogue de dépassement de capacité d’entier lorsque des valeurs de délai élevées étaient utilisées
  - Ajustement de la période de grâce à un minimum de 1 heure si une priorité plus faible est fournie
  - Suppression de « Usage_Anomaly » des valeurs acceptées pour le paramètre « ExcludedDetectionType » des applets de commande Set-AzureRmSqlDatabaseThreatDetectionPolicy et Set-AzureRmSqlServerThreatDetectionPolicy.
* Storage
  - Mise à niveau du SDK SRP vers la version 6.3.0
  - New/Set-AzureRmStorageAccount : ajout d’un paramètre pour prendre en charge EnableHttpsTrafficOnly
  - New/Set/Get-AzureRmStorageAccount : le compte de stockage renvoyé contient un nouvel attribut, EnableHttpsTrafficOnly
* Azure.Storage
  - Mise à niveau vers Azure Storage Client Library 8.1.1 et Azure Storage DataMovement Library 0.5.1
  - Ajout d’une nouvelle applet de commande pour prendre en charge la fonctionnalité de copie incrémentielle d’objet blob
