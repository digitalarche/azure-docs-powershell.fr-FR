---
title: Notes de publication Azure PowerShell
description: Découvrez toutes les dernières mises à jour des modules Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002671"
---
# <a name="azure-powershell-release-notes"></a>Notes de publication Azure PowerShell

## <a name="340---february-2020"></a>3.4.0 - Février 2020
### <a name="highlights-since-the-last-major-release"></a>Points importants depuis la dernière version majeure
* Publication de la première version 0.1.0 d’Az.CosmosDB
* Ajout de la prise en charge d’Az.Network ConnectionMonitor V2

#### <a name="azaccounts"></a>Az.Accounts
* Désactivation de l’enregistrement automatique du contexte quand AzureRmContext.json n’est pas disponible
* Mise à jour de la référence à Azure PowerShell Common vers 1.3.5-preview

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Get-AzApiManagementApiSchema** Correction de l’obtention du schéma Open-Api associé à une API   https://github.com/Azure/azure-powershell/issues/10626
* **New-AzApiManagementProduct*** et **Set-AzApiManagementProduct**
  - Correction de la documentation pour https://github.com/Azure/azure-powershell/issues/10472
* **Set-AzApiManagementApi** Ajout d’un exemple pour montrer comment mettre à jour ServiceUrl avec l’applet de commande

#### <a name="azcompute"></a>Az.Compute
* Limitation du nombre d’états de machine virtuelle à 100 pour éviter un étranglement quand Get-AzVM-Status est exécuté sans nom de machine virtuelle.
* Ajout de l’applet de commande Update-AzDiskEncryptionSet
* Ajout des paramètres EncryptionType et DiskEncryptionSetId dans les applets de commande suivantes :
    - New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig
* Ajout du paramètre ColocationStatus à l’applet de commande Get-AzProximityPlacementGroup.

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour de la version du SDK .NET ADF vers 4.7.0

#### <a name="azdeploymentmanager"></a>Az.DeploymentManager
* Ajout des opérations LIST pour les ressources
* Ajout d’une fonctionnalité permettant d’effectuer des opérations sur les étapes de contrôle d’intégrité

#### <a name="azhdinsight"></a>Az.HDInsight
* Correction d’une erreur de documentation de New-AzHDInsightCluster.

#### <a name="azkeyvault"></a>Az.KeyVault
* Ajout d’un alias de nom à l’attribut VaultName pour que Remove-AzureKeyVault soit cohérent avec New-AzureKeyVault.

#### <a name="aznetwork"></a>Az.Network
* Ajout d’un nouvel exemple à Set-AzNetworkWatcherConfigFlowLog.md pour illustrer le scénario de désactivation de Traffic Analytics.
* Ajout de la prise en charge de l’affectation de la configuration IP de gestion au Pare-feu Azure - un sous-réseau dédié et une adresse IP publique que le pare-feu utilisera pour son trafic de gestion
    - Mise à jour de l’applet de commande New-AzFirewall :
        - Ajout du paramètre -ManagementPublicIpAddress (non obligatoire) qui accepte un objet d’adresse IP publique
        - Ajout de la méthode SetManagementIpConfiguration sur l’objet de pare-feu - nécessite un sous-réseau et une adresse IP publique comme entrée - le nom de sous-réseau doit être 'AzureFirewallManagementSubnet'
* Correction des exemples Get-AzNetworkSecurityGroup pour montrer des exemples de cartes réseau au lieu d’interfaces réseau.
* Correction d’une faute de frappe dans la commande New-AzVpnSite qui empêchait l’ID de ressource de réaliser un paramètre.
* Ajout de la prise en charge de la configuration d’URL dans un jeu d’actions de règles de réécriture dans Application Gateway
    - Ajout de nouvelles applets de commande :
        - New-AzApplicationGatewayRewriteRuleUrlConfiguration
    - Mise à jour des applets de commande avec le paramètre facultatif - UrlConfiguration
        - New-AzApplicationGatewayRewriteRuleActionSet
* Ajout de la prise en charge des ressources pour NetworkWatcher ConnectionMonitor version 2

#### <a name="azpolicyinsights"></a>Az.PolicyInsights
* Prise en charge de l’évaluation de la conformité avant de déterminer la ressource à corriger
    - Ajout du paramètre '-ResourceDiscoverMode' à Start-AzPolicyRemediation
* Ajout de l’applet de commande Get-AzPolicyMetadata pour obtenir les ressources de métadonnées de stratégie
* Mise à jour de Get-AzPolicyState et de Get-AzPolicyStateSummary pour la version d’API 2019-10-01

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Prise en charge d’Azure Site Recovery pour supprimer un disque répliqué.
* Ajout de la prise en charge de l’ajout d’étiquettes dans Sauvegarde Azure lors de la création d’un coffre Recovery Services.

#### <a name="azresources"></a>Az.Resources
* -Scope devenu facultatif dans les applets de commande *-AzPolicyAssignment avec la valeur par défaut pour le contexte d’abonnement
* Ajout d’exemples de création d’ADServicePrincipal avec des informations d’identification de clé et un mot de passe

#### <a name="azsql"></a>Az.Sql
Correction de l’applet de commande New-AzSqlDatabaseSecondary pour vérifier l’existence de PartnerDatabaseName au lieu de l’existence de DatabaseName.

#### <a name="azstorage"></a>Az.Storage
* Prise en charge de la définition du type de clés de chiffrement de table/file d’attente dans Créer un compte de stockage
    - New-AzStorageAccount
* Affichage de RequestId quand StorageException n’a pas ExtendedErrorInformation
* Correction de l’exemple 6 de l’applet de commande Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Set-AzWebapp et Set-AzWebappSlot prennent en charge les propriétés AlwaysOn, MinTls et FtpsState
* Résolution d’un problème où la définition de HttpsOnly en même temps que le changement de AppservicePlan avec la commande Set-AzWebApp consistait à redéfinir HttpsOnly avec la valeur par défaut

## <a name="330---january-2020"></a>3.3.0 - Janvier 2020
#### <a name="azaccounts"></a>Az.Accounts
* Mise à jour de Add-AzEnvironment et Set-AzEnvironment pour accepter les paramètres AzureAttestationServiceEndpointResourceId et AzureAttestationServiceEndpointSuffix

#### <a name="azcdn"></a>Az.Cdn
* Affichage du détail de la réponse à l’erreur dans l’applet de commande New-AzCdnEndpoint

#### <a name="azcompute"></a>Az.Compute
* Correction de l’applet de commande Set-AzVMCustomScriptExtension pour une machine virtuelle avec le disque OD managé qui n’a pas de profil de système d’exploitation.

#### <a name="azcontainerinstance"></a>Az.ContainerInstance
* Correction des noms de paramètres utilisés par l’exemple de New-AzContainerGroup

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Ajout de l’applet de commande 'Get-AzDataBoxEdgeStorageContainer'
  - Obtention du conteneur de stockage Edge
* Ajout de l’applet de commande 'New-AzDataBoxEdgeStorageContainer'
  - Création d’un conteneur de stockage Edge
* Ajout de l’applet de commande 'Remove-AzDataBoxEdgeStorageContainer'
  - Suppression du conteneur de stockage Edge
* Ajout de l’applet de commande 'Invoke-AzDataBoxEdgeStorageContainer'
  - Appel à l’action pour actualiser les données dans le conteneur de stockage Edge
* Ajout de l’applet de commande 'Get-AzDataBoxEdgeStorageAccount'
  - Obtention du compte de stockage Edge
* Ajout de l’applet de commande 'New-AzDataBoxEdgeStorageAccount'
  - Création du compte de stockage Edge
* Ajout de l’applet de commande 'Remove-AzDataBoxEdgeStorageAccount'
  - Suppression du compte de stockage Edge
* Appel de l’applet de commande 'Invoke-AzDataBoxEdgeShare'
  - Appel à l’action pour actualiser les données sur le partage
* Ajout de l’applet de commande 'Set-AzDataBoxEdgeStorageAccountCredential'
  - Définition des informations d’identification du compte de stockage az databoxedge

#### <a name="azdatafactory"></a>Az.DataFactory
* Ajout des propriétés AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId et VersionStatus pour la commande Get-AzDataFactoryV2IntegrationRuntime
* Mise à jour de la version du SDK .NET ADF vers 4.6.0
* Ajout du paramètre 'PublicIPs' pour la commande 'Set-AzureRmDataFactoryV2IntegrationRuntime' afin d’activer la création de runtimes intégrés Azure-SSIS avec des adresses IP publiques statiques.

#### <a name="azdevtestlabs"></a>Az.DevTestLabs
* Suppression du lien rompu dans Get-AzDtlAllowedVMSizesPolicy.md

#### <a name="azeventhub"></a>Az.EventHub
* Résolution du problème 10634 : Correction de la référence d’objet null pour remove eventhubnamespace

#### <a name="azhdinsight"></a>Az.HDInsight
* Correction de l’erreur Invoke-AzHDInsightHiveJob.md.

#### <a name="azmachinelearning"></a>Az.MachineLearning
* Suppression des applets de commande ci-dessous parce que MachineLearningCompute n’est plus disponible
  - Get-AzMlOpCluster
  - Get-AzMlOpClusterKey
  - New-AzMlOpCluster
  - Remove-AzMlOpCluster
  - Set-AzMlOpCluster
  - Test-AzMlOpClusterSystemServicesUpdateAvailability
  - Update-AzMlOpClusterSystemService

#### <a name="aznetwork"></a>Az.Network
* Mise à niveau de la dépendance de Microsoft.Azure.Management.Sql de 1.36-preview vers 1.37-preview

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Changement de la prise en charge d’Azure Site Recovery pour les machines virtuelles de disque managé chiffrées au repos avec des clés gérées par le client pour Azure dans le fournisseur Azure.
* Prise en charge d’Azure Site Recovery pour entrer l’ID de jeu de chiffrement de disque comme entrée facultative afin d’activer la protection pour VMware sur Azure.
* Prise en charge d’Azure Site Recovery pour entrer l’ID de jeu de chiffrement de disque comme entrée facultative au niveau du disque afin d’activer la protection pour VMware sur Azure.
* Prise en charge d’Azure Site Recovery pour mettre à jour l’élément protégé de réplication avec mappage de jeu de chiffrement de disque pour HyperV vers Azure

#### <a name="azresources"></a>Az.Resources
* Correction d’une erreur dans le document d’aide de 'Remove-AzTag'.

#### <a name="azsql"></a>Az.Sql
* Correction de la fonctionnalité des applets de commande de base définies avec l’évaluation des vulnérabilités pour qu’elles fonctionnent sur la base de données master de la base de données Azure et limitation de cette même fonctionnalité sur les bases de données système Managed Instance.
* Correction d’une erreur lors de la création du groupe de basculement d’instance SQL

#### <a name="azsqlvirtualmachine"></a>Az.SqlVirtualMachine
* Ajout de la reprise d’activité après sinistre comme nouveau type de licence valide

#### <a name="azstorage"></a>Az.Storage
* Ajout d’un message d’avertissement de changement cassant pour la modification de la valeur DefaultAction dans une version ultérieure
    - Update-AzStorageAccountNetworkRuleSet
* Prise en charge de l’obtention de l’heure de la dernière synchronisation du compte de stockage en exécutant get-AzureRMStorageAccount avec le paramètre -IncludeGeoReplicationStats 
    - Get-AzureRMStorageAccount

## <a name="320---december-2019"></a>3.2.0 - Décembre 2019

### <a name="general"></a>Général
* Mise à jour des références dans. psd1 pour utiliser le chemin relatif pour tous les modules

#### <a name="azaccounts"></a>Az.Accounts
* Définition du UserAgent approprié pour la télémétrie côté client pour la préversion Az 4.0
* Affichage d’un message d’erreur convivial quand le contexte est null dans la préversion Az 4.0

#### <a name="azbatch"></a>Az.Batch
* Correction du problème [#10602](https://github.com/Azure/azure-powershell/issues/10602), où **New-AzBatchPool** n’envoyait pas correctement 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' au serveur.

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour de la version du SDK .NET ADF vers 4.5.0

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Ajout de la prise en charge de l’exclusion des règles managées WAF
* Ajout de SocketAddr dans l’autocomplétion

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Gestion des exceptions

#### <a name="azkeyvault"></a>Az.KeyVault
* Correction de l’erreur d’accès à une valeur potentiellement non définie
* Gestion des certificats de chiffrement à courbe elliptique
    - Possibilité de spécifier la courbe pour les stratégies de certificat

#### <a name="azmonitor"></a>Az.Monitor
* Ajout d’un argument facultatif à la commande Ajouter des paramètres de diagnostic. Argument de commutateur qui, s’il est présent, indique que l’exportation vers Log Analytics doit être dans un schéma fixe (également appelé type de données dédié)

#### <a name="aznetwork"></a>Az.Network
* Prise en charge de IpGroups dans l’application AzureFirewall, règles NAT et réseau.

#### <a name="azresources"></a>Az.Resources
* Correction d’un problème où le déploiement de modèle ne parvenait pas à lire un paramètre de modèle si son nom était en conflit avec un nom de paramètre intégré.
* Mise à jour des applets de commande de stratégie pour utiliser la nouvelle version d’API 2019-09-01 qui introduit la prise en charge de regroupement dans les définitions d’ensemble de stratégies.

#### <a name="azsql"></a>Az.Sql
* Mise à niveau de la création de stockage avec l’activation automatique de StorageV2 dans Évaluation des vulnérabilités

#### <a name="azstorage"></a>Az.Storage
* Prise en charge de la génération d’un jeton SAS basé sur l’identité d’un objet blob/conteneur avec un contexte de stockage basé sur l’authentification Oauth
    - New-AzStorageContainerSASToken
    - New-AzStorageBlobSASToken
* Prise en charge de la révocation des clés de délégation d’utilisateur de compte de stockage pour pouvoir révoquer tous les jetons SAS d’identité
    - Revoke-AzStorageAccountUserDelegationKeys
* Mise à niveau vers Microsoft.Azure.Management.Storage 14.2.0 pour prendre en charge la nouvelle version d’API 2019-06-01.
* Prise en charge de QuotaGiB (quota de partage dans Gibibye) pour les valeurs supérieures à 5120 dans le plan de gestion des applets de commande de partage de fichiers et ajout de l’alias de paramètre « quota » au paramètre « QuotaGiB ». 
    - New-AzRmStorageShare
    - Update-AzRmStorageShare
* Ajout de l’alias de paramètre « QuotaGiB » au paramètre « Quota »
    - Set-AzStorageShareQuota
* Résolution du problème où Set-AzStorageContainerAcl pouvait nettoyer la stratégie d’accès stockée
    - Set-AzStorageContainerAcl

## <a name="310---november-2019"></a>3.1.0 - Novembre 2019
### <a name="highlights-since-the-last-major-release"></a>Points importants depuis la dernière version majeure
* Publication d’Az.DataBoxEdge 1.0.0
* Publication d’Az.SqlVirtualMachine 1.0.0

#### <a name="azcompute"></a>Az.Compute
* Fonctionnalité VM Reapply
    - Ajout du paramètre Reapply à l’applet de commande Set-AzVM
* Fonctionnalité VM Scale Set AutomaticRepairs :
    - Ajout des paramètres EnableAutomaticRepair, AutomaticRepairGracePeriod et AutomaticRepairMaxInstanceRepairsPercent aux applets de commande suivantes :   New-AzVmssConfig   Update-AzVmss
* Prise en charge interlocataire des images de galerie pour New-AzVM
* Ajout de « Spot » à l’argument completer du paramètre Priority dans les applets de commande New-AzVM, New-AzVMConfig et New-AzVmss
* Ajout des paramètres DiskIOPSReadWrite et DiskMBpsReadWrite à l’applet de commande Add-AzVmssDataDisk
* Définition du paramètre SourceImageId de l’applet de commande New-AzGalleryImageVersion sur facultatif
* Ajout des paramètres OSDiskImage et DataDiskImage à l’applet de commande New-AzGalleryImageVersion
* Ajout du paramètre HyperVGeneration à l’applet de commande New-AzGalleryImageDefinition
* Ajout des paramètres SkipExtensionsOnOverprovisionedVMs aux applets de commande New-AzVmss, New-AzVmssConfig et Update-AzVmss

#### <a name="azdataboxedge"></a>Az.DataBoxEdge
* Ajout de l’applet de commande `Get-AzDataBoxEdgeOrder`
    - Obtenir la commande
* Ajout de l’applet de commande `New-AzDataBoxEdgeOrder`
    - Créer une règle
* Ajout de l’applet de commande `Remove-AzDataBoxEdgeOrder`
    - Supprimer la commande
* Changement dans l’applet de commande `New-AzDataBoxEdgeShare`
    - Crée maintenant un partage local
* Ajout de l’applet de commande `Set-AzDataBoxEdgeRole`
    - Désormais, IotRole peut être mappé au partage
* Ajout de l’applet de commande `Invoke-AzDataBoxEdgeDevice`
    - Appeler l’analyse de la mise à jour, le téléchargement de la mise à jour, l’installation des mises à jour sur l’appareil
* Ajout de l’applet de commande `Get-AzDataBoxEdgeTrigger`
    - Obtient des informations sur les déclencheurs
* Ajout de l’applet de commande `New-AzDataBoxEdgeTrigger`
    - Créer des déclencheurs
* Ajout de l’applet de commande `Remove-AzDataBoxEdgeTrigger`
    - Supprimer les déclencheurs

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour de la version du SDK .NET ADF vers 4.4.0
* Ajout du paramètre « ExpressCustomSetup » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin d’activer les configurations d’installation et les composants tiers sans script d’installation personnalisé.

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Mise à jour de la documentation de Get-AzDataLakeStoreDeletedItem et de Restore-AzDataLakeStoreDeletedItem

#### <a name="azeventhub"></a>Az.EventHub
* Résolution du problème 10301 : Correction du format de date du jeton SAS

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Ajout du paramètre MinimumTlsVersion à Enable-AzFrontDoorCustomDomainHttps et New-AzFrontDoorFrontendEndpointObject
* Ajout des paramètres HealthProbeMethod et EnabledState à New-AzFrontDoorHealthProbeSettingObject
* Ajout d’une nouvelle applet de commande pour créer un objet BackendPoolsSettings à transmettre à la création/mise à jour de la porte d’entrée
    - New-AzFrontDoorBackendPoolsSettingObject

#### <a name="aznetwork"></a>Az.Network
* Changement des exemples d’options FilterData « Start-AzVirtualNetworkGatewayConnectionPacketCapture.md » et « Start-AzVirtualnetworkGatewayPacketCapture.md ».

#### <a name="azprivatedns"></a>Az.PrivateDns
* Mise à jour du SDK .NET PrivateDns vers la version 1.0.0

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Prise en charge Azure Site Recovery pour sélectionner le type de disque à l’activation de la protection.
* Correction de bogue Azure Site Recovery pour modifier l’action du plan de récupération.
* Prise en charge de la restauration SQL de sauvegarde Azure pour accepter les bases de données filestream.

#### <a name="azrediscache"></a>Az.RedisCache
* Ajout du paramètre « MinimumTlsVersion » dans les applets de commande « New-AzRedisCache » et « Set-AzRedisCache ». Par ailleurs, ajout de « MinimumTlsVersion » dans la sortie de l’applet de commande « Get-AzRedisCache ».
* Ajout de la validation sur le paramètre « -size » pour les applets de commande « Set-AzRedisCache » et « New-AzRedisCache »

#### <a name="azresources"></a>Az.Resources
- Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-06-01 incluant la nouvelle propriété EnforcementMode dans l’attribution de stratégie.
- Mise à jour de l’exemple d’aide pour créer une définition de stratégie
- Correction de bogue pour Remove-AZADServicePrincipal-ServicePrincipalName qui générait une référence Null quand le nom de principal de service était introuvable.
- Correction de bogue pour New-AZADServicePrincipal, qui générait une référence Null quand le locataire n’avait pas d’abonnement.
- Changement de New-AzAdServicePrincipal pour ajouter des informations d’identification uniquement à l’application associée.

#### <a name="azsql"></a>Az.Sql
* Ajout de la prise en charge de la base de données ReadReplicaCount.
* Correction de Set-AzSqlDatabase quand la redondance de zone n’est pas définie

## <a name="300---november-2019"></a>3.0.0 - Novembre 2019
### <a name="general"></a>Général
* Publication d’Az.PrivateDns 1.0.0

#### <a name="azaccounts"></a>Az.Accounts
* Ajout d’un message de dépréciation pour l’alias « Resolve-Error ».

#### <a name="azadvisor"></a>Az.Advisor
* Ajout d’une nouvelle catégorie « Excellence opérationnelle » à l’applet de commande Get-AzAdvisorRecommendation.

#### <a name="azbatch"></a>Az.Batch
* Renommage de `CoreQuota` sur `BatchAccountContext` en `DedicatedCoreQuota`. Il existe également un nouveau `LowPriorityCoreQuota`.
  - Cela a un impact sur **Get-AzBatchAccount**.
* Le paramètre `-ResourceFile` **New-AzBatchTask** prend à présent une collection d’objets `PSResourceFile`, qui peuvent être construits à l’aide de la nouvelle applet de commande **New-AzBatchResourceFile**.
* Nouvelle applet de commande **New-AzBatchResourceFile** pour aider à créer des objets `PSResourceFile`. Ceux-ci peuvent être fournis à **New-AzBatchTask** sur le paramètre `-ResourceFile`.
  - Cela prend en charge deux nouveaux types de fichiers de ressources, en plus de la procédure `HttpUrl` existante :
    - Les fichiers de ressources basés sur `AutoStorageContainerName` téléchargent l’intégralité d’un conteneur de stockage automatique dans le nœud Batch.
    - Les fichiers de ressources basés sur `StorageContainerUrl` téléchargent le conteneur spécifié dans l’URL dans le nœud Batch.
* Suppression de la propriété `ApplicationPackages` de `PSApplication` retournée par **Get-AzBatchApplication**.
  - Les packages spécifiques à l’intérieur d’une application peuvent maintenant être récupérés à l’aide de **Get-AzBatchApplicationPackage**. Par exemple : `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.
* Renommage de `ApplicationId` en `ApplicationName` sur **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** et **Set-AzBatchApplication**.
  - `ApplicationId` est maintenant un alias de `ApplicationName`.
* Ajout de la nouvelle propriété `PSWindowsUserConfiguration` à `PSUserAccount`.
* Renommage de `Version` en `Name` sur `PSApplicationPackage`.
* Renommage de `BlobSource` en `HttpUrl` sur `PSResourceFile`.
* Suppression de la propriété `OSDisk` de `PSVirtualMachineConfiguration`.
* Suppression de **Set-AzBatchPoolOSVersion**. Cette opération n’est plus prise en charge.
* Suppression de `TargetOSVersion` de `PSCloudServiceConfiguration`.
* Renommage de `CurrentOSVersion` en `OSVersion` sur `PSCloudServiceConfiguration`.
* Suppression de `DataEgressGiB` et `DataIngressGiB` de `PSPoolUsageMetrics`.
* Suppression de **Get-AzBatchNodeAgentSku** et remplacement par **Get-AzBatchSupportedImage**. 
  - **Get-AzBatchSupportedImage** retourne les mêmes données que **Get-AzBatchNodeAgentSku**, mais sous un format plus convivial.
  - Les nouvelles images non vérifiées sont désormais également retournées. Vous trouverez également des informations supplémentaires sur `Capabilities` et `BatchSupportEndOfLife` pour chaque image.
* Ajout de la possibilité de monter des systèmes de fichiers distants sur chaque nœud d’un pool via le nouveau paramètre `MountConfiguration` de **New-AzBatchPool**.
* Prise en charge désormais des règles de sécurité bloquant l’accès réseau à un pool basé sur le port source du trafic. Cette opération s’effectue via la propriété `SourcePortRanges` sur `PSNetworkSecurityGroupRule`.
* Lors de l’exécution d’un conteneur, Batch prend désormais en charge l’exécution de la tâche dans le répertoire de travail du conteneur ou dans le répertoire de travail de la tâche Batch. Cela est contrôlé par la propriété `WorkingDirectory` sur `PSTaskContainerSettings`.
* Ajout de la possibilité de spécifier une collection d’adresses IP publiques sur `PSNetworkConfiguration` via la nouvelle propriété `PublicIPs`. Cela garantit que les nœuds du pool obtiendront une adresse IP de la liste des adresses IP fournies par l’utilisateur.
* Lorsqu’elle n’est pas spécifiée, la valeur par défaut de `WaitForSuccess` sur `PSSTartTask` est désormais `$True` (était `$False`).
* Lorsqu’elle n’est pas spécifiée, la valeur par défaut de `Scope` sur `PSAutoUserSpecification` est désormais `Pool` (était `Task` sur Windows et `Pool` sur Linux).

#### <a name="azcdn"></a>Az.Cdn
* Introduction d’UrlRewriteAction et de CacheKeyQueryStringAction pour RulesEngine.
* Correction de plusieurs bogues comme une entrée « Selector » manquante dans l’applet de commande New-AzDeliveryRuleCondition.

#### <a name="azcompute"></a>Az.Compute
* Fonctionnalité Ensemble de chiffrements de disque
    - Nouvelles applets de commande :   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet
    - Le paramètre DiskEncryptionSetId est ajouté aux applets de commande suivantes : Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile        
        Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk
    - Les paramètres DiskEncryptionSetId et EncryptionType sont ajoutés aux applets de commande suivantes :   New-AzDiskConfig   New-AzSnapshotConfig
* Ajout du paramètre PublicIPAddressVersion à New-AzVmssIPConfig
* Déplacement de fileUris de l’extension de script personnalisé du paramètre public au paramètre protégé
* Ajout de ScaleInPolicy aux applets de commande New-AzVmss, New-AzVmssConfig et Update-AzVmss
* Changements cassants
    - Le paramètre UploadSizeInBytes est utilisé à la place de DiskSizeGB pour New-AzDiskConfig lorsque CreateOption est Upload
    - PublishingProfile.Source.ManagedImage.Id est remplacé par StorageProfile.Source.Id dans l’objet GalleryImageVersion

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour de la version du SDK .NET ADF vers la version 4.3.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* La mise à jour de la version du SDK ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) apporte les correctifs suivants
* Levée d’une exception évitée alors qu’il n’est pas possible de désérialiser la valeur creationtime de l’entrée de répertoire ou de la corbeille.
* Exposition du paramètre par délai d’expiration de demande dans adlsclient
* Correction du passage du syncflag d’origine pour la récupération badoffset
* Correction d’EnumerateDirectory pour récupérer le jeton de continuation une fois la réponse vérifiée
* Correction du bogue de concaténation

#### <a name="azfrontdoor"></a>Az.FrontDoor
* Correction de diverses fautes de frappe dans le module

#### <a name="azhdinsight"></a>Az.HDInsight
* Correction du bogue à cause duquel le client reçoit l’erreur indiquant que l’entrée n’est pas une chaîne en base 64 valide lors de l’utilisation de Get-AzHDInsightCluster pour obtenir le cluster avec le stockage ADLSGen1.
* Ajout d’un paramètre nommé « ApplicationId » à trois applets de commande Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig et New-AzHDInsightCluster afin que le client puisse fournir l’ID d’application du principal de service pour l’accès à Azure Data Lake.
* Remplacement de 2.1.0 par 5.1.0 pour Microsoft.Azure.Management.HDInsight
* Suppression de cinq applets de commande :
    - Get-AzHDInsightOMS
    - Enable-AzHDInsightOMS
    - Disable-AzHDInsightOMS
    - Grant-AzHDInsightRdpServicesAccess
    - Revoke-AzHDInsightRdpServicesAccess
* Ajout de trois applets de commande :
    - Get-AzHDInsightMonitoring pour remplacer Get-AzHDInsightOMS.
    - Enable-AzHDInsightMonitoring pour remplacer Enable-AzHDInsightOMS.
    - Disable-AzHDInsightMonitoring pour remplacer Disable-AzHDInsightOMS.
* Correction de l’applet de commande Get-AzHDInsightProperties pour prendre en charge l’obtention d’informations sur les fonctionnalités à partir d’un emplacement spécifique.
* Suppression des jeux de paramètres (« Spark1 », « Spark2 ») d’Add-AzHDInsightConfigValue.
* Ajout d’exemples aux documents d’aide de l’applet de commande Add-AzHDInsightSecurityProfile.
* Changement du type de sortie des applets de commande suivantes :
*  - Remplacement du type de sortie CapabilitiesResponse de Get-AzHDInsightProperties par AzureHDInsightCapabilities.
*  - Remplacement du type de sortie ClusterGetResponse de Remove-AzHDInsightCluster par une valeur booléenne.
*  - Remplacement du type de sortie HttpConnectivitySettings de Set-AzHDInsightGatewaySettings par GatewaySettings.
* Ajout de cas de test de scénario.
* Suppression d’alias : « Add-AzHDInsightConfigValues », « Get-AzHDInsightProperties ».

#### <a name="aziothub"></a>Az.IotHub
* Changements cassants :
    - L’applet de commande « Add-AzIotHubEventHubConsumerGroup » ne prend plus en charge le paramètre « EventHubEndpointName » et aucun alias n’a été trouvé pour le nom de paramètre d’origine.
    - Le jeu de paramètres « __AllParameterSets » pour l’applet de commande « Add-AzIotHubEventHubConsumerGroup » a été supprimé.
    - L’applet de commande « Get-AzIotHubEventHubConsumerGroup » ne prend plus en charge le paramètre « EventHubEndpointName » et aucun alias n’a été trouvé pour le nom de paramètre d’origine.
    - Le jeu de paramètres « __AllParameterSets » pour l’applet de commande « Get-AzIotHubEventHubConsumerGroup » a été supprimé.
    - La propriété « OperationsMonitoringProperties » de type « Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties » a été supprimée.
    - La propriété « OperationsMonitoringProperties » de type « Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties » a été supprimée.
    - L’applet de commande « New-AzIotHubExportDevice » ne prend plus en charge l’alias « New-AzIotHubExportDevices ».
    - L’applet de commande « New-AzIotHubImportDevice » ne prend plus en charge l’alias « New-AzIotHubImportDevices ».
    - L’applet de commande « Remove-AzIotHubEventHubConsumerGroup » ne prend plus en charge le paramètre « EventHubEndpointName » et aucun alias n’a été trouvé pour le nom de paramètre d’origine.
    - Le jeu de paramètres « __AllParameterSets » pour l’applet de commande « Remove-AzIotHubEventHubConsumerGroup » a été supprimé.
    - L’applet de commande « Set-AzIotHub » ne prend plus en charge le paramètre « OperationsMonitoringProperties » et aucun alias n’a été trouvé pour le nom de paramètre d’origine.
    - Le jeu de paramètres « UpdateOperationsMonitoringProperties » pour l’applet de commande « Set-AzIotHub » a été supprimé.

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Prise en charge Azure Site Recovery de la configuration des ressources de mise en réseau telles que le groupe de sécurité réseau, l’adresse IP publique et les équilibreurs de charge internes pour Azure vers Azure.
* Prise en charge Azure Site Recovery de l’écriture sur un disque managé pour vMWare vers Azure.
* Prise en charge Azure Site Recovery de la réduction de carte réseau pour vMWare vers Azure.
* Prise en charge Azure Site Recovery de la mise en réseau accélérée pour Azure vers Azure.
* Prise en charge Azure Site Recovery de la mise à jour automatique de l’agent pour Azure vers Azure.
* Prise en charge Azure Site Recovery de SSD Standard pour Azure vers Azure.
* Prise en charge Azure Site Recovery de deux passes Azure Disk Encryption pour Azure vers Azure.
* Prise en charge Azure Site Recovery de la protection du disque récemment ajouté pour Azure vers Azure.
* Ajout de la fonctionnalité SoftDelete pour les machines virtuelles et de tests pour softdelete

#### <a name="azresources"></a>Az.Resources
* Mise à jour de l’assembly de dépendance Microsoft.Extensions.Caching.Memory de 1.1.1 à 2.2

#### <a name="aznetwork"></a>Az.Network
* Modification de toutes les applets de commande de PrivateEndpointConnection pour prendre en charge le fournisseur de services générique.
    - Mise à jour de l’applet de commande :
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Set-AzPrivateEndpointConnection
* Ajout d’une nouvelle applet de commande pour PrivateLinkResource avec prise en charge du fournisseur de services générique.
    - Nouvelle applet de commande :
        - Get-AzPrivateLinkResource
* Ajout de nouveaux champs et paramètres pour la fonctionnalité de protocole proxy V2.
    - Ajout de la propriété EnableProxyProtocol dans PrivateLinkService
    - Ajout de la propriété LinkIdentifier dans PrivateEndpointConnection
    - Mise à jour de New-AzPrivateLinkService pour ajouter un nouveau paramètre facultatif EnableProxyProtocol.
* Correction de la description des paramètres incorrects dans la documentation de référence « New-AzApplicationGatewaySku »
* Nouvelles applets de commande pour prendre en charge la stratégie de pare-feu Azure
* Ajout de la prise en charge de la ressource enfant RouteTables de VirtualHub
    - Ajout de nouvelles cmdlets :
        - Add-AzVirtualHubRoute
        - Add-AzVirtualHubRouteTable
        - Get-AzVirtualHubRouteTable
        - Remove-AzVirtualHubRouteTable
        - Set-AzVirtualHub
* Ajout de la prise en charge des nouvelles propriétés SKU de VirtualHub et VirtualWANType de VirtualWan
    - Mise à jour d’applets de commande avec des paramètres facultatifs :
        - New-AzVirtualHub : ajout du paramètre SKU
        - Update-AzVirtualHub : ajout du paramètre SKU
        - New-AzVirtualWan : ajout du paramètre VirtualWANType
        - Update-AzVirtualWan : ajout du paramètre VirtualWANType
* Ajout de la prise en charge de la propriété EnableInternetSecurity pour HubVnetConnection, VpnConnection et ExpressRouteConnection
    - Ajout de nouvelles cmdlets :
        - Update-AzureRmVirtualHubVnetConnection
    - Mise à jour d’applets de commande avec des paramètres facultatifs :
        - New-AzureRmVirtualHubVnetConnection : ajout du paramètre EnableInternetSecurity
        - New-AzureRmVpnConnection : ajout du paramètre EnableInternetSecurity
        - Update-AzureRmVpnConnection : ajout du paramètre EnableInternetSecurity
        - New-AzureRmExpressRouteConnection : ajout du paramètre EnableInternetSecurity
        - Set-AzureRmExpressRouteConnection : ajout du paramètre EnableInternetSecurity
* Ajout de la prise en charge de la configuration de la stratégie WebApplicationFirewall de niveau supérieur
    - Ajout de nouvelles cmdlets :
        - New-AzApplicationGatewayFirewallPolicySetting
        - New-AzApplicationGatewayFirewallPolicyExclusion
        - New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRuleOverride
        - New-AzApplicationGatewayFirewallPolicyManagedRule
        - New-AzApplicationGatewayFirewallPolicyManagedRuleSet
    - Mise à jour d’applets de commande avec des paramètres facultatifs :
        - New-AzApplicationGatewayFirewallPolicy : ajout du paramètre PolicySetting, ManagedRule
* Ajout de la prise en charge de l’opérateur de géocorrespondance sur CustomRule
    - Ajout de GeoMatch à l’opérateur sur FirewallCondition
* Ajout de la prise en charge des stratégies de pare-feu perListener et perSite
    - Mise à jour d’applets de commande avec des paramètres facultatifs :
        - New-AzApplicationGatewayHttpListener : ajout du paramètre FirewallPolicy, FirewallPolicyId
        - New-AzApplicationGatewayPathRuleConfig : ajout du paramètre FirewallPolicy, FirewallPolicyId
* La correction du sous-réseau requis avec le nom AzureBastionSubnet dans « PSBastion » peut ne pas respecter la casse
* Prise en charge des noms de domaine complets de destination dans les règles réseau et du nom de domaine complet traduit dans les règles NAT du pare-feu Azure
* Ajout de la prise en charge de la ressource de niveau supérieur RouteTables d’IpGroup
    - Ajout de nouvelles cmdlets :
        - New-AzIpGroup
        - Remove-AzIpGroup
        - Get-AzIpGroup
        - Set-AzIpGroup

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Suppression de l’applet de commande Add-AzServiceFabricApplicationCertificate, car ce scénario est couvert par Add-AzVmssSecret.

#### <a name="azsql"></a>Az.Sql
* Ajout de la prise en charge de la restauration des bases de données supprimées sur les instances managées.
* Dépréciation dans le code des anciennes applets de commande d’audit.
* Suppression des alias dépréciés :
* Get-AzSqlDatabaseIndexRecommendations (utiliser Get-AzSqlDatabaseIndexRecommendation à la place)
* Get-AzSqlDatabaseRestorePoints (utiliser Get-AzSqlDatabaseRestorePoint à la place)
* Suppression de l’applet de commande Get-AzSqlDatabaseSecureConnectionPolicy
* Suppression des alias des applets de commande de paramètres d’évaluation des vulnérabilités dépréciées
* Dépréciation des applets de commande de paramètres de détection avancée des menaces 
* Ajout d’applets de commande pour désactiver et activer les recommandations de sensibilité sur les colonnes d’une base de données.

#### <a name="azstorage"></a>Az.Storage
* Prise en charge de l’activation du partage de fichiers volumineux lors de la création ou de la mise à jour d’un compte de stockage
    -  New-AzStorageAccount
    -  Set-AzStorageAccount
* Lors de la fermeture/l’obtention du descripteur de fichier, ne pas vérifier si le chemin d’entrée est Répertoire de fichier ou Fichier, afin d’éviter un échec avec l’objet dans l’état DeletePending
    -  Get-AzStorageFileHandle
    -  Close-AzStorageFileHandle
    
## <a name="280---october-2019"></a>2.8.0 - octobre 2019
### <a name="general"></a>Général
* Az.HealthcareApis 1.0.0 release

#### <a name="azaccounts"></a>Az.Accounts
* Mise à jour de la télémétrie et réécriture des URL pour les modules générés, correction des tests unitaires Windows.

#### <a name="azapimanagement"></a>Az.ApiManagement
* **Set-AzApiManagementApi** - Ajout de la prise en charge de la mise à jour d’Api dans ApiVersionSet
    - Corriger le problème https://github.com/Azure/azure-powershell/issues/10068

#### <a name="azautomation"></a>Az.Automation
* Correction de l’applet de commande New-AzureAutomationSoftwareUpdateConfiguration pour le paramètre de définition de redémarrage Linux. 

#### <a name="azbatch"></a>Az.Batch
* **Get-AzBatchNodeAgentSku** est déprécié et va être remplacé par **Get-AzBatchSupportImage** dans la version 2.0.0.

#### <a name="azcompute"></a>Az.Compute
* Ajout des paramètres Priority, EvictionPolicy et MaxPrice aux applets de commande New-AzVM et New-AzVmss
* Correction du message d’avertissement et du document d’aide pour les applets de commande Add-AzVMAdditionalUnattendContent et Add-AzVMSshPublicKey
* Correction de l’exception Fix-skipVmBackup pour les machines virtuelles Linux avec des disques managés pour Set-AzVMDiskEncryptionExtension. 
* Correction du bogue dans les paramètres de chiffrement de mise à jour dans Set-AzVMDiskEncryptionExtension, deux scénarios de réussite.

#### <a name="azdatafactory"></a>Az.DataFactory
* Ajout des commandes CRUD pour le flux de données ADF V2 : Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow et Get-AzDataFactoryV2DataFlow.
* Ajout de commandes d’action pour la session de débogage de flux de données ADF V2 : Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand et Stop-AzDataFactoryV2DataFlowDebugSession.
* Mise à jour de la version du SDK .NET ADF vers la version 4.2.0

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Correction de la validation de compte afin que les comptes avec '-' puissent être passés sans domaine

#### <a name="azhealthcareapis"></a>Az.HealthcareApis
* Mise à jour de la version PowerShell vers 1.0.0
* Mise à jour de la version du SDK vers 1.0.2
* Mise à jour dans les tests pour faire référence à la nouvelle version du SDK
* Mise à jour de la structure de sortie qui passe d’un état imbriqué à un état aplati.

#### <a name="aziothub"></a>Az.IotHub
* Ajout d’une nouvelle source de routage : DigitalTwinChangeEvents
* Correctif de bogues mineurs : Get-AzIothub ne retourne pas subscriptionId 

#### <a name="azmonitor"></a>Az.Monitor
* Nouveaux récepteurs de groupe d’actions ajoutés pour le groupe d’actions   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver
* Utiliser le schéma d’alerte commun activé pour les récepteurs. Cela ne s’applique pas aux SMS, au push Azure App, à ITSM et aux systèmes vocaux
* Les webhooks prennent maintenant en charge l’authentification Azure Active Directory.

#### <a name="aznetwork"></a>Az.Network
* Ajout de la nouvelle applet de commande Get-AzAvailableServiceAlias qui peut être appelée pour obtenir des alias pouvant être utilisés pour les stratégies de point de terminaison de service.
* Ajout de la prise en charge des sélecteurs de trafic pour les connexions de passerelle de réseau virtuel
    - Ajout de nouvelles cmdlets :
        - New-AzureRmTrafficSelectorPolicy
    - Applets de commande mises à jour avec un paramètre facultatif -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection
* Ajout de la prise en charge des protocoles ESP et AH dans les configurations de règles de sécurité réseau
    - Cmdlets mises à jour :
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Amélioration de la gestion des exceptions dans les applets de commande cortex
* Nouvelles générations et références SKU pour VirtualNetworkGateways
  - Introduction de nouvelles générations pour VirtualNetworkGateways.
  - Introduction de nouvelles références SKU haut débit pour VirtualNetworkGateways.

#### <a name="azrediscache"></a>Az.RedisCache
* Mise à jour de la documentation de référence 'Set-AzRedisCache' afin d’inclure les valeurs manquantes pour le paramètre '-Size'

#### <a name="azsql"></a>Az.Sql
* Ajout de la prise en charge de la définition de l’administrateur Active Directory sur Managed Instance

#### <a name="azstorage"></a>Az.Storage
* Mise à niveau de la bibliothèque de client de stockage vers la version 11.1.0
* Listing des conteneurs avec l’API de plan de gestion, sera listé avec NextPageLink
    -  Get-AzRmStorageContainer
* Listing des comptes de stockage de l’abonnement, sera listé avec NextPageLink
    -  Get-AzStorageAccount

#### <a name="azstoragesync"></a>Az.StorageSync
* Correction du problème 9810 dans Reset-AzStorageSyncServerCertificate.

#### <a name="azwebsites"></a>Az.Websites
* Échec de la mise à jour Set-AzWebApp avec l’ASP d’une application

## <a name="270---september-2019"></a>2.7.0 - septembre 2019
#### <a name="azapimanagement"></a>Az.ApiManagement
* Mise à jour de la description du paramètre « -Format » dans la documentation de référence de « Set-AzApiManagementPolicy »
* Suppression des références de la cmdlet dépréciée « Update-AzApiManagementDeployment » dans la documentation de référence. Utilisation de « Set-AzApiManagement » à la place.

#### <a name="azautomation"></a>Az.Automation
* Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Register-AzAutomationDscNode »
* Ajout d’une précision sur la restriction de système d’exploitation à Register-AzAutomationDSCNode
* Correction de l’exception de référence Null de la comdlet Start-AzAutomationRunbook pour l’option -Wait.

#### <a name="azcompute"></a>Az.Compute
* Ajout du paramètre UploadSizeInBytes à New-AzDiskConfig
* Ajout du paramètre Incremental à New-AzSnapshotConfig
* Ajouter d’une fonctionnalité de machine virtuelle basse priorité :
    - Les paramètres MaxPrice, EvictionPolicy et Priority sont ajoutés à New-AzVMConfig.
    - Le paramètre MaxPrice est ajouté aux cmdlets New-AzVmssConfig, Update-AzVM et Update-AzVmss.
* Correction du problème de référence de machine virtuelle pour la cmdlet AzAvailabilitySet quand elle liste tous les groupes à haute disponibilité inclus dans l’abonnement.
* Correction de l’exception Null pour Get-AzRemoteDesktopFile.
* Correction de la méthode de recherche de disque dur virtuel pour la position relative de fin.
* Correction du problème UltraSSD pour New-AzVM et Update-AzVM.

#### <a name="azdatafactory"></a>Az.DataFactory
* Ajout de 3 nouvelles commandes pour ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription et Get-AzDataFactoryV2TriggerSubscriptionStatus
* Mise à jour de la version du SDK .NET ADF vers la version 4.1.3

#### <a name="azhdinsight"></a>Az.HDInsight
* Explication des changements cassants

#### <a name="aziothub"></a>Az.IotHub
* Ajout de la prise en charge pour appeler le basculement d’un IotHub vers la région de reprise d’activité géocouplée.
* Ajout de la prise en charge pour gérer l’enrichissement de message pour un IotHub. Les nouvelles cmdlets sont :
    - Add-AzIotHubMessageEnrichment
    - Get-AzIotHubMessageEnrichment
    - Remove-AzIotHubMessageEnrichment
    - Set-AzIotHubMessageEnrichment

#### <a name="azmonitor"></a>Az.Monitor
* Pointage vers le dernier SDK Monitor, par exemple, 0.24.1-preview
   - Ajout de changements non cassants aux cmdlets Metrics, c.-à-d. que l’énumération Unit prend en charge plusieurs nouvelles valeurs. Il s’agit de cmdlets en lecture seule, donc aucune modification n’est apportée à leur entrée.
   - La version d’API des demandes **ActionGroups** est désormais **2019-06-01**, auparavant il s’agissait de la version **2018-03-01**. Les tests de scénario ont été mis à jour pour tenir compte de cette modification.
   - Les constructeurs des classes **EmailReceiver** et **WebhookReceiver** ont un nouvel argument obligatoire, à savoir une valeur booléenne appelée **useCommonAlertSchema**. Actuellement, la valeur est définie sur **false** pour masquer ce changement cassant par rapport aux cmdlets. **REMARQUE** : Il s’agit d’une modification temporaire qui doit être validée par l’équipe des alertes.
   - L’ordre des arguments pour le constructeur de la classe **Source** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent. Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.
   - L’ordre des arguments pour le constructeur de la classe **AlertingAction** (liée à la classe **ScheduledQueryRuleSource**) a été modifié par rapport au SDK précédent. Cette modification exigeait la correction de deux tests unitaires : ils se compilaient, mais ne parvenaient pas à passer les tests.
* Prise en charge des critères de seuil dynamique pour l’alerte de métrique V2
    - New-AzMetricAlertRuleV2Criteria : création de critères de seuil dynamique également
    - Add-AzMetricAlertRuleV2 : acceptation de critères de seuil dynamique également
* Améliorations apportées aux cmdlets de règle de requête planifiée
 - Les cmdlets acceptent le paramètre « location » dans les deux formats, à savoir l’emplacement (par exemple, usa-est) ou le nom d’affichage de l’emplacement (par exemple, USA Est)
 - Illustration correcte du paramètre « Enabled » dans les fichiers d’aide
 - Ajout d’exemples pour le paramètre facultatif « ActionGroup »
 - Amélioration globale des fichiers d’aide
* Correction du bogue lié à la détermination du type d’étendue pour « Set-AzActionRule »

#### <a name="aznetwork"></a>Az.Network
* Correction de l’exemple incorrect dans la documentation de référence de « New-AzApplicationGateway » 
* Ajout d’une remarque à la documentation de référence de « Get-AzNetworkWatcherPacketCapturee » à propos de la récupération de toutes les propriétés d’une capture de paquets
* Correction de l’exemple dans la documentation de référence de « Test-AzNetworkWatcherIPFlow » pour énumérer correctement les cartes réseau
* Amélioration de l’analyse des exceptions cloud pour afficher des détails supplémentaires s’ils existent
* Amélioration de l’analyse des exceptions cloud pour gérer un type supplémentaire d’exception de SDK
* Correction du mappage incorrect des modèles de règle de sécurité
* Ajout de propriétés à une interface réseau pour la fonctionnalité d’adresse IP privée
    - Ajout de la propriété « PrivateEndpoint » comme type de PSResourceId à PSNetworkInterface
    - Ajout de la propriété « PrivateLinkConnectionProperties » comme type de PSIpConfigurationConnectivityInformation à PSNetworkInterfaceIPConfiguration
    - Ajout d’une nouvelle classe de modèle PSIpConfigurationConnectivityInformation
* Ajout de « MSSQL » ApplicationRuleProtocolType pour la ressource du Pare-feu Azure
* Prise en charge de liaisons multiples dans Azure Virtual WAN
    - Nouvelles applets de commande
        - New-AzVpnSiteLink
        - New-AzVpnSiteLinkConnection
    - Mise à jour de l’applet de commande :
        - New-VpnSite
        - Update-VpnSite
        - New-VpnConnection
        - Update-VpnConnection
* Correction des documents de certains exemples PowerShell pour utiliser des cmdlets Az à la place de cmdlets AzureRM

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Mise à jour de l’objet AzureVMpolicy avec l’attribut ProtectedItemsCount
* Ajout de tests pour la stratégie de machine virtuelle et la restauration du compte de stockage d’origine

#### <a name="azresources"></a>Az.Resources
* Correction du bogue qui empêchait l’appel de New-AzRoleAssignment sans paramètre d’étendue.

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correction de la faute de frappe dans l’exemple de la documentation de référence pour « Update-AzServiceFabricReliability »
* Ajout de nouvelles cmdlets pour gérer les applications et les services :
    - New-AzServiceFabricApplication
    - New-AzServiceFabricApplicationType
    - New-AzServiceFabricApplicationTypeVersion
    - New-AzServiceFabricService
    - Update-AzServiceFabricApplication
    - Get-AzServiceFabricApplication
    - Get-AzServiceFabricApplicationType
    - Get-AzServiceFabricApplicationTypeVersion
    - Get-AzServiceFabricService
    - Remove-AzServiceFabricApplication
    - Remove-AzServiceFabricApplicationType
    - Remove-AzServiceFabricApplicationTypeVersion
    - Remove-AzServiceFabricServic
* Mise à niveau du SDK Service Fabric vers la version 1.2.0 qui utilise la version d’API du fournisseur de ressources Service Fabric 2019-03-01.

#### <a name="azsignalr"></a>Az.SignalR
* Ajout de cmdlets Update, Restart, CheckNameAvailability, GetUsage

#### <a name="azsql"></a>Az.Sql
* Mise à jour de l’exemple dans la documentation de référence pour « Get-AzSqlElasticPool »
* Ajout d’un exemple vCore à la création d’un pool élastique (New-AzSqlElasticPool).
* Suppression de la validation de EmailAddresses et de la vérification que EmailAdmins n’a pas la valeur false quand EmailAddresses est vide dans Set-AzSqlServerAdvancedThreatProtectionPolicy et Set-AzSqlDatabaseAdvancedThreatProtectionPolicy
* Activation de la suppression des paramètres d’audit du serveur/de la base de données quand il existe plusieurs paramètres de diagnostic qui activent la catégorie d’audit.
* Correction de la validation des adresses e-mail dans plusieurs cmdlets d’évaluation des vulnérabilités SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting et Update-AzSqlInstanceVulnerabilityAssessmentSetting).

#### <a name="azstorage"></a>Az.Storage
* Mise à jour de l’exemple dans la documentation de référence pour « Get-AzStorageAccountKey »
* Lors d’un chargement/téléchargement de fichier Azure, prise en charge de la conservation des propriétés SMB des fichiers sources (attributs du fichier, heure de création du fichier, heure de la dernière écriture du fichier) dans le fichier de destination
    -  Set-AzStorageFileContent
    -  Get-AzStorageFileContent
* Correction de l’échec de chargement de l’objet blob de blocs avec des propriétés/métadonnées sur ImmutabilityPolicy avec conteneur activé.
    -  Set-AzStorageBlobContent
* Prise en charge de la gestion des partages de fichiers Azure avec l’API de plan de gestion
    -  New-AzRmStorageShare
    -  Get-AzRmStorageShare
    -  Update-AzRmStorageShare
    -  Remove-AzRmStorageShare

#### <a name="azwebsites"></a>Az.Websites
* Résolution du problème de suppression des balises d’application web lors de la migration de l’application vers un nouvel ASP
* Correction de Publish-AzureWebapp pour un fonctionnement sur Linux et Windows
* Mise à jour de l’exemple dans la documentation de référence pour « Get-AzWebAppPublishingProfile »

## <a name="260---august-2019"></a>2.6.0 - Août 2019
#### <a name="general"></a>Général
* Correction des fautes de frappe diverses dans de nombreux modules

#### <a name="azaccounts"></a>Az.Accounts
* Prise en charge de l’identité MSI affectée à l’utilisateur dans l’authentification Azure Functions (n° 9479)

#### <a name="azaks"></a>Az.Aks
* Résolution du problème relatif à la sortie de « Get-AzAks »
    * Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9847

#### <a name="azapimanagement"></a>Az.ApiManagement
* Corriger le problème https://github.com/Azure/azure-powershell/issues/9351
    - Mise à jour de la version de .Net NuGet, qui n’applique pas de restrictions sur productId, apiId, groupId et userId
* **Get-AzApiManagementProduct** : ajout de la prise en charge de l’interrogation de produits à l’aide d’une API.
  https://github.com/Azure/azure-powershell/issues/9482
* **New-AzApiManagementApiRevision** : résolution du problème où ApiRevisionDescription n’était pas défini lors de la création d’une révision d’API https://github.com/Azure/azure-powershell/issues/9752
* Correction d’une faute de frappe dans le modèle « PsApiManagementOAuth2AuthrozationServer » remplacé par « PsApiManagementOAuth2AuthorizationServer »

#### <a name="azbatch"></a>Az.Batch
* Correction d’une faute de frappe dans un message d’aide et la documentation pour mettre Windows en majuscules

#### <a name="azcdn"></a>Az.Cdn
* Correction d’une faute de frappe dans l’application d’assistance du module CDN

#### <a name="azcompute"></a>Az.Compute
* Ajout de VmssId à l’applet de commande New-AzVMConfig
* Ajout des paramètres TerminateScheduledEvents et TerminateScheduledEventNotBeforeTimeoutInMinutes à New-AzVmssConfig et Update-AzVmss
* Ajout de la propriété HyperVGeneration à l’objet image de machine virtuelle
* Ajout des fonctionnalités Host et HostGroup
    - Nouvelles applets de commande :   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost
    - Le paramètre HostId est ajouté à New-AzVMConfig et New-AzVM
* Mise à jour de l’exemple dans la documentation « Invoke-AzVMRunCommand » de manière utiliser le nom de paramètre approprié
* Mise à jour de la description « -VolumeType » dans la documentation de référence de « Set-AzVMDiskEncryptionExtension » et de « Set-AzVmssDiskEncryptionExtension »

#### <a name="azdatafactory"></a>Az.DataFactory
* Correction de la faute de frappe pour mettre « Windows » en majuscules dans la documentation de « New-AzDataFactoryEncryptValue »
* Mise à jour de la version du SDK .NET ADF vers la version 4.1.2
* Ajout des paramètres « DataProxyIntegrationRuntimeName », « DataProxyStagingLinkedServiceName » et « DataProxyStagingPath » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » afin de permettre la configuration du runtime d’intégration auto-hébergé comme proxy pour SSIS Integration Runtime
* Mise à jour de PSTriggerRun pour afficher les pipelines déclenchés, le message et les propriétés, et de PSActivityRun pour afficher le type d’activité

#### <a name="azdatalakestore"></a>Az.DataLakeStore
* Correction de la suspension de Get-DataLakeStoreDeletedItem pour toutes les erreurs ou exceptions à distance.

#### <a name="azeventhub"></a>Az.EventHub
* Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNteworkRule dans Set-AzEventHubNetworkRuleSet
* Résolution du problème n° 9558 : Set-AzEventHubNamespace utilise PATCH au lieu de PUT
* Ajout du paramètre EnableKafka à l’applet de commande Set-AzEventHubNamespace
* Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement

#### <a name="azmarketplaceordering"></a>Az.MarketplaceOrdering
* Résolution de la faute de frappe où « Azure » était tout en minuscules dans la documentation

#### <a name="azmonitor"></a>Az.Monitor
* Correction du nom de paramètre incorrect dans la documentation

#### <a name="aznetwork"></a>Az.Network
* Mise à jour dans New-AzPrivateLinkServiceIpConfig
    - Dépréciation du paramètre « PublicIpAddress », car il n’est jamais utilisé côté serveur.
    - Ajout d’un paramètre facultatif « Primary » qui indique si la configuration IP actuelle est primaire ou non.
* Amélioration de la gestion de l’exception d’erreur de demande à partir du SDK : résolution du problème où les exceptions du SDK n’étaient précédemment pas gérées correctement, ce qui empêchait l’affichage des détails des erreurs de clé
* Ajustement de la logique de validation pour le préfixe IP IPv6 afin de rechercher la longueur de préfixe IPv6 appropriée. 
* Mise à jour de Get-AzVirtualNetworkSubnetConfig : Ajout d’un paramètre défini pour obtenir l’ID de ressource de sous-réseau.
* Mise à jour de la description du paramètre Location pour AzNetworkServiceTag

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Mise à jour de la documentation pour « New-AzOperationalInsightsLinuxSyslogDataSource »
    - Ajout d’un exemple
    - Mise à jour de la description du paramètre « -Name »
* Ajout d’un exemple pour New-AzOperationalInsightsWindowsEventDataSource
* Changement de la description du paramètre -Name pour New-AzOperationalInsightsWindowsEventDataSource

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Mise à jour de « Get-AzRecoveryServicesBackupJobDetail.md »

#### <a name="azresources"></a>Az.Resources
* Ajout de la prise en charge de la nouvelle API version 2019-05-10 pour Microsoft.Resource
    - Ajout de la prise en charge de « copy.count = 0 » pour les variables, les ressources et les propriétés
    - Les ressources avec « condition = false » ou « copy.count = 0 » seront supprimées en mode Complet
* Ajout d’un exemple d’affectation de stratégie au niveau de l’abonnement à la documentation d’aide

#### <a name="azservicebus"></a>Az.ServiceBus
* Résolution du problème n° 9658 : Faute de frappe sur le paramètre VirtualNetworkRule dans Set-AzServiceBusNetworkRuleSet
* Résolution du problème n° 9786 : Impossible de créer une règle avec des droits Écouter uniquement
* Ajout de la nouvelle commande « Test-AzServiceBusNameAvailability » afin de vérifier la disponibilité du nom pour la file d’attente et la rubrique 

#### <a name="azservicefabric"></a>Az.ServiceFabric
* Correction des bogues relatifs à l’applet de commande add node type :
    - bogue NullReferenceException quand un groupe de ressources avait d’autres groupes de machines virtuelles identiques non liés au cluster Service Fabric. Résolution du problème : https://github.com/Azure/azure-powershell/issues/8681
    - Correction du bogue où l’applet de commande échouait si virtualNetwork se trouvait dans un groupe de ressources différent de celui du cluster. Résolution du problème : https://github.com/Azure/azure-powershell/issues/8407
    - Dépréciation de l’applet de commande Add-AzServiceFabricApplicationCertificate

#### <a name="azsql"></a>Az.Sql
* Mise à jour de la documentation des anciennes applets de commande d’audit.

#### <a name="azstorage"></a>Az.Storage
* Mise à jour de l’aide pour Get/Close-AzStorageFileHandle, en ajoutant d’autres scénarios aux exemples d’applets de commande et mise à jour des descriptions des paramètres
* Prise en charge de StandardBlobTier dans le chargement d’objet blob et la copie d’objet blob
    -  Set-AzStorageBlobContent
    -  Start-AzStorageBlobCopy
* Prise en charge de la priorité de réalimentation dans la copie d’objet blob
    -  Start-AzStorageBlobCopy

#### <a name="azwebsites"></a>Az.Websites
* Ajout d’une clarification concernant le paramètre -AppSettings dans Set-AzWebApp et Set-AzWebAppSlot

## <a name="250---july-2019"></a>2.5.0 - Juillet 2019
#### <a name="azaccounts"></a>Az.Accounts
* Mise à jour du code commun pour utiliser la dernière version de ClientRuntime

#### <a name="azapplicationinsights"></a>Az.ApplicationInsights
* Correction d’une faute de frappe dans un exemple de la documentation sur « Remove-AzApplicationInsightsApiKey » 

#### <a name="azautomation"></a>Az.Automation
* Correction d’une faute de frappe dans la chaîne de ressource 

#### <a name="azcognitiveservices"></a>Az.CognitiveServices
* Prise en charge de NetworkRuleSet.

#### <a name="azcompute"></a>Az.Compute
* Ajout des propriétés manquantes (ComputerName, OsName, OsVersion et HyperVGeneration) de l’objet de vue d’instance de machine virtuelle.

#### <a name="azcontainerregistry"></a>Az.ContainerRegistry
* Correction d’une faute de frappe dans Remove-AzContainerRegistryReplication pour le paramètre Replication
    - Plus d’informations ici : https://github.com/Azure/azure-powershell/issues/9633

#### <a name="azdatafactory"></a>Az.DataFactory
* Mise à jour du SDK .NET ADF avec la version 4.1.0
* Correction d’une faute de frappe dans la documentation sur « Get-AzDataFactoryV2PipelineRun »

#### <a name="azeventhub"></a>Az.EventHub
* Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzEventHubAuthorizationRuleSASToken
* Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté

#### <a name="azkeyvault"></a>Az.KeyVault
* Possibilité de spécifier KeySize pour les stratégies de certificat

#### <a name="azlogicapp"></a>Az.LogicApp
* Correction de Get-AzIntegrationAccountMap pour lister tous les types de cartes
    - Ajout d’un nouveau paramètre MapType pour le filtrage

#### <a name="azmanagedservices"></a>Az.ManagedServices
* Ajout de la prise en charge de l’API version 2019-06-01 (GA)

#### <a name="aznetwork"></a>Az.Network
* Prise en charge d’un point de terminaison privé et du service de liaison privée
    - Nouvelles applets de commande
        - Set-AzPrivateEndpoint
        - Set-AzPrivateLinkService
        - Approve-AzPrivateEndpointConnection
        - Deny-AzPrivateEndpointConnection
        - Get-AzPrivateEndpointConnection
        - Remove-AzPrivateEndpointConnection
        - Test-AzPrivateLinkServiceVisibility
        - Get-AzAutoApprovedPrivateLinkService
* Les commandes ci-dessous ont été mises à jour pour la fonctionnalité : Indicateur PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies sur le sous-réseau dans VirtualNetwork
    - Mise à jour de New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig
        - Ajout du paramètre facultatif -PrivateEndpointNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un point de terminaison privé dans ce sous-réseau.
        - Ajout du paramètre facultatif -PrivateLinkServiceNetworkPoliciesFlag qui configure l’application de stratégies réseau sur un service de liaison privé dans ce sous-réseau.
* Le paramètre d’applet de commande « ServiceName » d’AzPrivateLinkService a été renommé « Name » avec un alias « ServiceName » à des fins de compatibilité descendante
* Activation du protocole ICMP pour les configurations des règles de sécurité réseau
    - Applets de commande mises à jour
        - Add-AzNetworkSecurityRuleConfig
        - New-AzNetworkSecurityRuleConfig
        - Set-AzNetworkSecurityRuleConfig
* Ajout de ConnectionProtocolType (Ikev1/Ikev2) comme paramètre configurable pour New-AzVirtualNetworkGatewayConnection
* Ajout de PrivateIpAddressVersion dans LoadBalancerFrontendIpConfiguration
    - Mise à jour de l’applet de commande :
        - New-AzLoadBalancerFrontendIpConfig
        - Add-AzLoadBalancerFrontendIpConfig
        - Set-AzLoadBalancerFrontendIpConfig
* Mise à jour de la commande Application Gateway New-AzApplicationGatewayProbeConfig pour prendre en charge un port personnalisé dans la sonde
    - Mise à jour de New-AzApplicationGatewayProbeConfig : Ajout d’un paramètre facultatif Port permettant de détecter un serveur back-end. Ce paramètre s’applique aux références SKU Standard_V2 et WAF_V2.

#### <a name="azoperationalinsights"></a>Az.OperationalInsights
* Affectation de la valeur 1 à la version par défaut pour les recherches enregistrées. 
* Correction de la gestion des expressions régulières null des journaux personnalisés

#### <a name="azrecoveryservices"></a>Az.RecoveryServices
* Mise à jour de « Get-AzRecoveryServicesBackupJob.md »
* Mise à jour de « Get-AzRecoveryServicesBackupContainer.md »
* Mise à jour de « Get-AzRecoveryServicesVault.md »
* Mise à jour de « Wait-AzRecoveryServicesBackupJob.md »
* Mise à jour de « Set-AzRecoveryServicesVaultContext.md »
* Mise à jour de « Get-AzRecoveryServicesVault.md »
* Mise à jour de « Get-AzRecoveryServicesBackupRecoveryPoint.md »
* Mise à jour de « Restore-AzRecoveryServicesBackupItem.md »
* Mise à jour de l’appel de service pour annuler l’inscription du conteneur pour le partage de fichiers Azure
* Mise à jour de « Set-AzRecoveryServicesAsrAlertSetting.md »

#### <a name="azresources"></a>Az.Resources
- Suppression de l’applet de commande manquante référencée dans la documentation sur « New-AzResourceGroupDeployment »
- Mise à jour des applets de commande de stratégie pour utiliser la nouvelle API version 2019-01-01

#### <a name="azservicebus"></a>Az.ServiceBus
* Ajout d’une nouvelle applet de commande pour la génération d’un jeton SAS : New-AzServiceBusAuthorizationRuleSASToken
* Ajout d’un message de vérification et d’erreur pour les droits authorizationrules si seul « Manage » est affecté

#### <a name="azsql"></a>Az.Sql
* Correction des exemples absents de l’applet de commande Set-AzSqlDatabaseSecondary
* Correction des analyses récurrentes d’évaluation des vulnérabilités sans fournir d’adresse e-mail
* Correction d’une faute de frappe dans un message d’avertissement.

#### <a name="azstorage"></a>Az.Storage
* Mise à jour de l’exemple dans la documentation de référence de manière à ce que « Get-AzStorageAccount » utilise le nom de paramètre approprié

#### <a name="azstoragesync"></a>Az.StorageSync
* Ajout de l’applet de commande Invoke-AzStorageSyncChangeDetection.
* Résolution du problème 9551 pour honorer TierFilesOlderThanDays

#### <a name="azwebsites"></a>Az.Websites
* Correction d’un bogue empêchant AzWebApp et Set-AzWebApp de retourner de certaines propriétés SiteConfig
* Ajoute un nouveau paramètre d’emplacement à AzDeletedWebApp et Restore-AzDeletedWebApp
* Correction d’un bogue lié au clonage d’emplacements d’application web à l’aide de New-AzWebApp -IncludeSourceWebAppSlots

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
* Changements cassants
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
    - [Plus d’informations](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) sur l’API SQR
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
* Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/
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
* Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/
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
* Ajouts des compléments Location, ResourceGroup et ResourceName : https://azure.microsoft.com/blog/completers-in-azure-powershell/
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
### <a name="general"></a>Général

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

### <a name="general"></a>Général

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
#### <a name="general"></a>Général
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
* Modification du type de peering en paramètre obligatoire pour les cmdlets suivantes : -
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
