---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.openlocfilehash: 61ab0f91c3d6fffdbffd336fa0d6ed9b0ab8f6ec
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68863295"
---
# <a name="release-notes"></a>Notes de publication

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

---

# <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Programme d’installation d’Azure PowerShell 5.7.0 : [lien](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

Module de la galerie pour les applets de commande ARM : [lien](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

Pour installer `AzureRM` à partir de PowerShell Gallery, exécutez la commande suivante :

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

Pour mettre à jour à partir d’une version antérieure de `AzureRM`, exécutez la commande suivante :

```powershell-interactive
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a>Modifications apportées depuis la dernière version

#### <a name="general"></a>Généralités
* Mise à jour vers la dernière version d’Azure ClientRuntime

#### <a name="azurestorage"></a>Azure.Storage
* Correction du problème d’échec de la cmdlet de chargement d’objet Blob et de chargement de fichier sur les machines où la stratégie FIPS est activée
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* Nouvelle cmdlet Get-AzureRmEnrollmentAccount
  - cmdlet pour récupérer les comptes d’inscription

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Intégration avec le Kit de développement logiciel (SDK) Cognitive Services Management version 4.0.0.
* Ajout de l’opération AzureRmCognitiveServicesAccountUsage.

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus` prend en charge l’état du chiffrement au niveau du disque de données
* `Get-AzureRmVmssVmDiskEncryptionStatus` prend en charge l’état du chiffrement au niveau du disque de données
* Mise à jour de la résilience dans la zone
* « New-AzureRmVm » et « New-AzureRmVmss » (ensemble de paramètres simples) prennent en charge les zones de disponibilité.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Découplez la dépendance envers Commands.Resources.Rest et les Kits de développement logiciel (SDK) ARM/Stockage.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Ajout de fonctionnalités de débogage
* Mise à jour de la version des Kits de développement logiciel (SDK) du plan de données ADLS vers 1.1.2
* Export-AzureRmDataLakeStoreItem : les paramètres PerFileThreadCount, ConcurrentFileCount sont déconseillés et le paramètre Concurrency a été introduit
* Import-AzureRMDataLakeStoreItem : les paramètres PerFileThreadCount, ConcurrentFileCount sont déconseillés et le paramètre Concurrency a été introduit
* Get-AzureRMDataLakeStoreItemContent : résolution du comportement de fin pour les contenus supérieurs à 4 Mo
* Set-AzureRMDataLakeStoreItemExpiry : introduction du nouvel ensemble de paramètres SetRelativeExpiry pour définir le délai d’expiration relatif
* Remove-AzureRmDataLakeStoreItem : le paramètre Clean est déconseillé.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Correction de AlternameName dans New-AzureRmEventHubGeoDRConfiguration

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Mise à jour des cmdlet pour inclure des scénarios de redirection
* Ajout de messages d’obsolescence pour les changements cassants à venir

#### <a name="azurermnetwork"></a>AzureRM.Network
* Correction du message d’erreur avec les cmdlet réseau

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Ajout de « propriétés » dans le filtre de corrélations des règles pour prendre en charge les propriétés personnalisées
* Mise à jour de l’aide New-AzureRmServiceBusGeoDRConfigurationet et correction de la sortie de la cmdlet Règles
* Correction des propriétés de transfert automatique dans les cmdlet New-AzureRmServiceBusQueue et New-AzureRmServiceBusSubscription

#### <a name="azurermsql"></a>AzureRM.Sql
* Ajout de la nouvelle cmdlet « Stop-AzureRmSqlElasticPoolActivity » pour prendre en charge l’annulation des opérations asynchrones sur le pool élastique
* Mise à jour de la réponse pour les cmdlet Get-AzureRmSqlDatabaseActivity et Get-AzureRmSqlElasticPoolActivity afin de refléter plus d’informations dans la réponse

Modifications apportées depuis la dernière version : https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 - Mars 2018

#### <a name="general"></a>Généralités
* Résolution d’un problème avec le groupe de ressources par défaut dans CloudShell
* Résolution d’un problème qui causait l’exécution de scripts de démarrage incorrects lors de l’importation du module

#### <a name="azurermprofile"></a>AzureRM.Profile
* Activation de l’authentification MSI dans les scénarios non pris en charge
* Ajout de la prise en charge pour Managed Service Identity défini par l’utilisateur

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Résolution d’un problème lié au nettoyage des scripts dans la build

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Résolution d’un problème lié au nettoyage des scripts dans la build

#### <a name="azurermcompute"></a>AzureRM.Compute
* « New-AzureRmVM » et « New-AzureRmVMSS » prennent en charge les disques de données.
* « New-AzureRmVM » et « New-AzureRmVMSS » prennent en charge les images personnalisées par nom ou par ID.
* Fonctionnalité Log Analytics
    - Ajout de la cmdlet « Export-AzureRmLogAnalyticRequestRateByInterval »
    - Ajout de la cmdlet « Export-AzureRmLogAnalyticThrottledRequests »

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Résolution du problème de jeux de paramètre du montage de volume de fichiers azure et du registre de conteneur

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Mise à jour du Kit de développement logiciel (SDK) ADF .Net vers la version 0.6.0 - préversion, qui contient les modifications suivantes :
    - Ajout de nouveaux services liés Azure Databricks et activités Databricks Notebook
    - Ajout de propriétés headNodeSize et dataNodeSize dans le service lié HDInsightOnDemand
    - Ajout de service lié, jeu de données, copie source pour SalesforceMarketingCloud
    - Prise en charge supplémentaire pour SecureOutput sur toutes les activités
    - Ajout d’une nouvelle propriété BatchCount sur l’activité ForEach qui contrôle le nombre d’activités simultanées à exécuter
    - Ajout de nouvelles activités de filtre
    - Ajout de la prise en charge des paramètres de service lié

#### <a name="azurermdns"></a>AzureRM.Dns
* Prise en charge des Zones DNS privées (Préversion publique)
    - Ajoute la possibilité de créer des zones DNS qui sont visibles uniquement pour les réseaux virtuels associés

#### <a name="azurermnetwork"></a>AzureRM.Network
* Mise à jour des types de modèles pour assurer la compatibilité avec les cmdlet DNS.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Modifications pour ASR Azure vers Azure Site Recovery (les cmdlets prennent actuellement en charge des opérations pour Enterprise vers Enterprise, Enterprise vers Azure, HyperV vers Azure, VMware vers Azure)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Les paramètres suivants sont obsolètes dans les applets de commande de compte de stockage New et Set : EnableEncryptionService et DisableEncryptionService, puisque le chiffrement au repos est activé par défaut et ne peut pas être désactivé.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Résolution de l’aide pour Remove-AzureRmWebAppSlot

## <a name="550---march-2018"></a>5.5.0 - Mars 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Résolution du problème avec l’importation d’alias
* Charger la version 10.0.3 de Newtonsoft.Json parallèlement à la version 6.0.8

#### <a name="azurestorage"></a>Azure.Storage
* Prise en charge de la fonctionnalité de suppression réversible
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Résolution du problème avec l’importation d’alias
* Ajouter la prise en charge du pare-feu et de la fonctionnalité de montée en puissance parallèle de requête, ainsi que la prise en charge de la version de l’API 2017-08-01.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Résolution du problème avec l’importation d’alias

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Résolution du problème avec l’importation d’alias

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Mettre à jour notice.txt et le message de notification.

#### <a name="azurermcompute"></a>AzureRM.Compute
* ’New-AzureRmVMSS’ imprime les chaînes de connexion en mode détaillé.
* ’New-AzureRmVmss’ prend en charge l’adresse IP publique, les règles d’équilibrage de charge, et les règles NAT de trafic entrant.
* Fonctionnalité WriteAccelerator
    - Paramètre de commutateur WriteAccelerator ajouté aux applets de commande suivantes : Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - Paramètre de commutateur OsDiskWriteAccelerator ajouté à l’applet de commande suivante :     Set-AzureRmVmssStorageProfile.
    - Paramètre booléen OsDiskWriteAccelerator ajouté aux applets de commande suivantes :     Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Résoudre le problème de chiffrement des informations d’identification qui n’est à l’origine d’aucune erreur explicite pour certaines opérations de chiffrement
* Activer le partage du runtime d’intégration dans la fabrique de données

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Ajouter les paramètres « SetupScriptContainerSasUri » et « Edition » à la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » pour activer les fonctionnalités d’installation personnalisée et de sélection d’édition
* Résoudre le problème de chiffrement des informations d’identification qui n’est à l’origine d’aucune erreur explicite pour certaines opérations de chiffrement.
* Activer le partage du runtime d’intégration dans la fabrique de données

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Résolution du problème avec l’importation d’alias

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Résolution de l’exemple pour Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Résolution du problème avec l’importation d’alias

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Résolution du problème avec l’importation d’alias

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Résolution du problème avec l’importation d’alias

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Résolution du problème avec l’importation d’alias

#### <a name="azurermresources"></a>AzureRM.Resources
* Résolution du problème avec l’importation d’alias

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Ajout de la propriété EnableBatchedOperations à la file d’attente
* Ajout de la propriété DeadLetteringOnFilterEvaluationExceptions aux abonnements

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Actualisation de l’applet de commande Service Fabric
  - Mise à jour des modèles ARM
  - Les opérations ayant échoué ne se restaurent plus
  - Add-AzureRmServiceFabricNodeType
    - Les machines virtuelles correspondent par défaut à des disques managés
    - Sous-réseau VMSS existant utilisé
    - Toutes les opérations sont idempotentes
  - Remove-AzureRmServiceFabricNodeType nettoie les VMSS partiellement créés et/ou les types de nœuds de cluster
  - Résolution de la sortie de l’objet PSCluster pour les types de propriétés complexes

#### <a name="azurermsql"></a>AzureRM.Sql
* Résolution du problème avec l’importation d’alias
* Les réponses Get-AzureRmSqlServer, New-AzureRmSqlServer, et Remove-AzureRmSqlServer comprennent désormais la propriété FullyQualifiedDomainName.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Résolution du problème avec l’importation d’alias
* New-AzureRMWebApp - ajout du jeu de paramètre pour la création simplifiée de la WebApp, avec prise en charge du référentiel Git local.

## <a name="540---february-2018"></a>5.4.0 : février 2018
#### <a name="azurermautomation"></a>AzureRM.Automation
* Ajout d’un alias depuis New-AzureRmAutomationModule vers Import-AzureRmAutomationModule

#### <a name="azurermcompute"></a>AzureRM.Compute
* Correction du problème lié à ErrorAction pour certaines cmdlets Get.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Application d’Azure Container Instances SDK, 2018-02-01
    - Prise en charge de l’étiquette du nom DNS

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Correction de l’ensemble des cmdlets GET qui ne fonctionnaient pas auparavant.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Correction d’un problème dans l’aide de Get-AzureRmEventHubGeoDRConfiguration

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ajout d’une cmdlet pour créer un moniteur de connexion
    - New-AzureRmNetworkWatcherConnectionMonitor
* Ajout d’une cmdlet pour mettre à jour un moniteur de connexion
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Ajout d’une cmdlet pour obtenir un moniteur de connexion ou une liste de moniteurs de connexion
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Ajout d’une cmdlet pour interroger un moniteur de connexion
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Ajout d’une cmdlet pour démarrer un moniteur de connexion
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Ajout d’une cmdlet pour arrêter un moniteur de connexion
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Ajout d’une cmdlet pour supprimer un moniteur de connexion
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Mise à jour de la documentation relative à Set-AzureRmApplicationGatewayBackendAddressPool pour supprimer un exemple déconseillé
* Ajout de l’indicateur EnableHttp2 à Application Gateway
    - Mise à jour de New-AzureRmApplicationGateway : Ajout du paramètre facultatif -EnableHttp2
* Ajouter un élément IpTags à PublicIpAddress
    - Mise à jour de New-AzureRmPublicIpAddress : Ajout d’IpTags
    - New-AzureRmPublicIpTag pour ajouter un paramètre Iptag
* Ajoutez une propriété DisableBgpRoutePropagation dans les éléments RouteTable et effectiveRoute.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature : Ajout d’un exemple manquant dans la documentation
* Register-AzureRmResourceProvider : Ajout d’un exemple manquant dans la documentation

#### <a name="azurermstorage"></a>AzureRM.Storage
* Les paramètres suivants sont obsolètes dans les applets de commande de compte de stockage New et Set : EnableEncryptionService et DisableEncryptionService, puisque le chiffrement au repos est activé par défaut et ne peut pas être désactivé.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 - Février 2018
### <a name="azurermprofile"></a>AzureRM.Profile
* Ajout d’un avertissement de désapprobation à PowerShell 3 et 4
* `Add-AzureRmAccount` a été renommé en tant que `Connect-AzureRmAccount` ; un alias a été ajouté pour l’ancien nom de l’applet de commande et les autres alias (`Login-AzAccount` et `Login-AzureRmAccount`) ont été redirigés vers le nouveau nom de l’applet de commande.
* `Remove-AzureRmAccount` a été renommé en tant que `Disconnect-AzureRmAccount` ; un alias a été ajouté pour l’ancien nom de l’applet de commande et les autres alias (`Logout-AzAccount` et `Logout-AzureRmAccount`) ont été redirigés vers le nouveau nom de l’applet de commande.
* Correction des chaînes de ressources pour utiliser `Connect-AzureRmAccount` au lieu de `Login-AzureRmAccount`
* `Add-AzureRmEnvironment` et `Set-AzureRmEnvironment`
  - Ajout de `-AzureOperationalInsightsEndpoint` et `-AzureOperationalInsightsEndpointResourceId` en tant que paramètres pour une utilisation avec le fournisseur de plans de données OperationalInsights.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`

### <a name="azurermcompute"></a>AzureRM.Compute
* Ajout du paramètre `-AvailabilitySetName` au parameterset simplifié de `New-AzureRmVM`.
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`
* Prise en charge d’une identité affectée par l’utilisateur pour les machines virtuelles et les groupes de machines virtuelles identiques
    - Les paramètres `-IdentityType` et `-IdentityId` sont ajoutés à `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` et `Update-AzureRmVmss`
* Ajout du paramètre `-EnableIPForwarding` pour `Add-AzureRmVmssNetworkInterfaceConfig`
* Ajout du paramètre `-Priority` pour `New-AzureRmVmssConfig`

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`
* Correction du message d’erreur de `Test-AzureRmDataLakeStoreAccount` lors de l’exécution de cette applet de commande sans se connecter à l’aide de `Login-AzureRmAccount`

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Mis à jour pour utiliser la version d’API 2018-01-01.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* Ajout de nouvelles commandes ci-dessous pour les opérations de géorécupération d’urgence.
  - Création d’un nouvel alias (configuration de la récupération d’urgence) :
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Récupération de l’alias (configuration de la récupération d’urgence) :
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Désactivation de la récupération d’urgence et arrêt de la réplication des changements de l’espace de noms principal sur l’espace de noms secondaire
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Appel d’un basculement de récupération d’urgence et reconfiguration de l’alias pour qu’il pointe vers l’espace de noms secondaire
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Suppression d’un alias (configuration de la récupération d’urgence)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* Ajout de nouvelles commandes ci-dessous pour la vérification du nom de l’espace de noms et du nom de la configuration GeoDr - Disponibilité de l’alias.
  - Vérification de la disponibilité du nom de l’espace de noms ou du nom d’alias (configuration de la récupération d’urgence) :
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`

### <a name="azurermnetwork"></a>AzureRM.Network
* Corriger le message de remplacement « Voulez-vous vraiment remplacer la ressource »

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Ajout de la prise en charge pour les requêtes d’API V2 via `Invoke-AzureRmOperationalInsightsQuery`. Consultez [https://dev.loganalytics.io/](https://dev.loganalytics.io/) pour plus d’informations sur la nouvelle API.

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: `-ServicePrincipalName` supprimé du jeu de paramètres vide par défaut car il était redondant avec le jeu de paramètres SPN

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* Ajout de la correction de fonctionnalités pour `Remove-AzureRmServiceBusRule` et `Get-AzureRmServiceBusKey`
* Ajout de nouvelles applets de commande ci-dessous pour les opérations de géorécupération d’urgence.
  - Création d’un nouvel alias (configuration de la récupération d’urgence) :
    - `New-AzureRmServiceBusDRConfigurations`
  - Récupération de l’alias (configuration de la récupération d’urgence) :
    - `Get-AzureRmServiceBusDRConfigurations`
  - Désactivation de la récupération d’urgence et arrêt de la réplication des changements de l’espace de noms principal sur l’espace de noms secondaire
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Appel d’un basculement de récupération d’urgence et reconfiguration de l’alias pour qu’il pointe vers l’espace de noms secondaire
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Suppression d’un alias (configuration de la récupération d’urgence)
    - `Remove-AzureRmServiceBusDRConfigurations`
* Mise à jour des applets de commande `Test-AzureRmServiceBusName` pour prendre en charge la géorécupération d’urgence - Opérations de vérification de la disponibilité du nom d’alias.
  - Vérification de la disponibilité du nom de l’espace de noms ou du nom d’alias (configuration de la récupération d’urgence) :
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Correction de l’utilisation de `Login-AzureRmAccount` pour utiliser `Connect-AzureRmAccount`

## <a name="520---january-2018"></a>5.2.0 - Janvier 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Add-AzureRmAccount
  * Ajout du nom de connexion -MSI pour l’authentification à l’aide des informations d’identification du Managed Service Identity du service/de la machine virtuelle actuelle
  * Résolution du problème d’authentification du coffre de clés lors de la connexion avec les jetons d’accès fourni par l’utilisateur

#### <a name="azurestorage"></a>Azure.Storage
* Ajout d’applets de commande pour obtenir et définir les propriétés de service de stockage
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty, et New-AzureRmApiManagement

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermautomation"></a>AzureRM.Automation
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour Set-AzureRmAutomationRunbook

#### <a name="azurermbackup"></a>AzureRM.Backup
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermbatch"></a>AzureRM.Batch
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmCdnEndpoint et New-AzureRmCdnProfile

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Intégration avec le Kit de développement logiciel (SDK) Cognitive Services Management version 3.0.0.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ajout du jeu de paramètre simplifié à New-AzureRmVmss, ce qui crée un groupe de machines virtuelles identiques et toutes les ressources nécessaires utilisant des valeurs par défaut intelligentes
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmVm et Update-AzureRmVm
* Correction de l’applet de commande Get-AzureRmComputeResourceSku lors de l’inclusion de la zone dans la restriction.
* Mise à jour du schéma de configuration de Diagnostics Agent pour la prise en charge du récepteur Azure Monitor.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Activation de la prise en charge d’Azure Key Vault pour tous les services associés du magasin de données
* Ajout de la propriété du type de licence pour le runtime d’intégration Azure SSIS
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmDataFactory

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Activation de la prise en charge d’Azure Key Vault pour tous les services associés du magasin de données
* Ajout de la propriété du type de licence pour le runtime d’intégration Azure SSIS
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout du paramètre « LicenseType » pour la commande « Set-AzureRmDataFactoryV2IntegrationRuntime » pour activer la fonctionnalité AHUB

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour AzureRmDataLakeAnalyticsAccount et Set-AzureRmDataLakeAnalyticsAccount

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmDataLakeStoreAccount et Set-AzureRmDataLakeStoreAccount

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermdns"></a>AzureRM.Dns
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Ajouter de la nouvelle applet de commande suivante :
  - Update-AzureRmEventGridSubscription
    - Mise à jour des propriétés d’un abonnement aux événements Event Grid.
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurerminsights"></a>AzureRM.Insights
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Ajout de la prise en charge des certificats pour les applets de commande IoTHub
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout de la prise en charge d’-AsJob pour les applets de commande de coffre de clés longues. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
  * L’applet de commande concernée est : Remove-AzureRmKeyVault
* Correction du bogue dans Set-AzureRmKeyVaultAccessPolicy dans lequel le filtre AAD définissait le SPN sur le nom d’utilisateur principal fourni, plutôt que de définir le nom d’utilisateur principal
  - Pour plus d’informations, consultez le problème suivant : https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour Update-AzureRmMlCommitmentPlan

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Ajout du paramètre IncludeAllResources à l’applet de commande Remove-AzureRmMlOpCluster
  - L’utilisation de ce paramètre de commutateur supprimera toutes les ressources qui ont été créés à l’origine avec le cluster
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermmedia"></a>AzureRM.Media
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour Set-AzureRmMediaService and New-AzureRmMediaService

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ajout de la prise en charge d’-AsJob pour les applets de commande de réseau longues. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmNotificationHubsNamespace et Set-AzureRmNotificationHubsNamespace

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace, et Set-AzureRmOperationalInsightsWorkspace

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout de l’option - UseOriginalStorageAccount à l’applet de commande Restore-AzureRmRecoveryServicesBackupItem.
  - L’activation de cet indicateur entraîne la restauration des disques sur leurs comptes de stockage d’origine, ce qui permet aux utilisateurs de maintenir la configuration de la machine virtuelle restaurée aussi proche que possible de celle des machines virtuelles d’origine.
  - Cela permet également d’améliorer les performances de l’opération de restauration.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout de 3 nouvelles applets de commande pour les règles de pare-feu
* Ajout de 3 nouvelles applets de commande pour la géo-réplication
* Ajout de la prise en charge des zones et des balises
* Rendre ResourceGroup facultatif chaque fois que cela est possible.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermresources"></a>AzureRM.Resources
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout de la prise en charge d’-AsJob pour les applets de commande de ressources longues. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
* Ajout de l’alias à partir de Get-AzureRmProviderOperation à Get-AzureRmResourceProviderAction pour respecter les conventions d’affectation de noms

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* -Tags obsolète et remplacé par -Tag pour New-AzureRmServerManagementNode et New-AzureRmServerManagementGateway

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermsql"></a>AzureRM.Sql
* Mise à jour de la description des paramètres de commande de l’audit
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout du paramètre - AsJob aux applets de commande longues
* Paramètre - DatabaseName obsolète de Get-AzureRmSqlServiceObjective

#### <a name="azurermstorage"></a>AzureRM.Storage
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Résolution d’un problème de référence null de l’applet de commande d’exécution New-AzureRMStorageAccount avec le paramètre - EnableEncryptionService None
* Ajout de la prise en charge d’-AsJob pour les applets de commande de stockage longues. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
    - Les applets de commande affectées sont New-, Remove-, Add-, et Update- pour le compte de stockage et sa règle de réseau.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Ajout de Location Completer aux paramètres -Location pour permettre la saisie semi-automatique via la touche Tab dans les emplacements valides
* Ajout de ResourceGroup Completer aux paramètres -ResourceGroup pour permettre la saisie semi-automatique via la touche Tab dans les groupes de ressources de l’abonnement actuel
* Ajout de la prise en charge d’-AsJob pour les applets de commande de sites web longues. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
     - Les applets de commande affectées sont New-, Remove-, Add-, et Set- pour WebApps, AppServicePlan et Slots

## <a name="2017128-version-511"></a>8\.12.2017 Version 5.1.1
* AnalysisServices
  - Modification de l’ensemble de l’emplacement valide de recherche dynamique afin que tous les clouds soient pris en charge.
* Automatisation
  - Mettre à jour vers Import-AzureRMAutomationRunbook
    - La prise en charge est désormais fournie pour les runbooks Python2
* Batch
  - Correction d’un bogue dans lequel les opérations de compte sans un groupe de ressources n’ont pas détecté automatiquement le groupe de ressources
* Calcul
  - Get-AzureRmComputeResourceSku affiche des informations de zone.
  - Mettre à jour Disable-AzureRmVmssDiskEncryption pour résoudre le problème https://github.com/Azure/azure-powershell/issues/5038
  - Ajout - Prise en charge AsJob pour les applets de commande de calcul longs. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
    - Les applets de commande concernées sont : les applets de commande New-, Update-, Set-, Remove-, Start-, Restart-, Stop- pour les machines virtuelles et les groupes de machines virtuelles identiques
    - Ajout du jeu de paramètre simplifié à New-AzureRmVM, ce qui crée une machine virtuelle et toutes les ressources nécessaires utilisant des valeurs par défaut intelligentes
* ContainerInstance
  - Appliquer Azure Container Instances SDK 2017-10-01
    - Prise en charge du conteneur run-to-completion
    - Prise en charge du montage du volume de fichiers Azure
    - Prise en charge de l’ouverture de plusieurs ports pour l’adresse IP publique
* ContainerRegistry
  - Nouvelles applets de commande pour la géo-réplication et les Webhooks
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - La fonctionnalité de chiffrement des informations d’identification fonctionne désormais avec « Accès à distance » activé (sur le réseau) et « Accès à distance » désactivé (ordinateur local).
* DataFactoryV2
  - Ajout de deux nouvelles applets de commande : Update-AzureRmDataFactoryV2 et Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - Ajout d’un paramètre appelé ScriptParameter à Submit-AzureRmDataLakeAnalyticsJob
    - Des informations détaillées sur ScriptParameter sont accessibles en utilisant Get-Help sur Submit-AzureRmDataLakeAnalyticsJob
  - Pour New-AzureRmDataLakeAnalyticsAccount, modification du paramètre MaxDegreeOfParallelism en MaxAnalyticsUnits
    - Ajout d’un alias pour le paramètre MaxAnalyticsUnits : MaxDegreeOfParallelism
  - Pour New-AzureRmDataLakeAnalyticsComputePolicy, modification du paramètre MaxDegreeOfParallelismPerJob en MaxAnalyticsUnitsPerJob
    - Ajout d’un alias pour le paramètre MaxAnalyticsUnitsPerJob : MaxDegreeOfParallelismPerJob
  - Pour Set-AzureRmDataLakeAnalyticsAccount, modification du paramètre MaxDegreeOfParallelism en MaxAnalyticsUnits
    - Ajout d’un alias pour le paramètre MaxAnalyticsUnits : MaxDegreeOfParallelism
  - Pour Submit-AzureRmDataLakeAnalyticsJob, modification du paramètre DegreeOfParallelism en AnalyticsUnits
    - Ajout d’un alias pour le paramètre AnalyticsUnits : DegreeOfParallelism
  - Pour Update-AzureRmDataLakeAnalyticsComputePolicy, modification du paramètre MaxDegreeOfParallelismPerJob en MaxAnalyticsUnitsPerJob
    - Ajout d’un alias pour le paramètre MaxAnalyticsUnitsPerJob : MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - Ajouter Set-AzureRmMlOpCluster
    - Mettre à jour le nombre d’agents ou la configuration SSL d’un cluster
  - Les propriétés de l’orchestrateur sont facultatives
    - Le service crée un principal de service s’il n’est pas fourni, les propriétés d’orchestrateur sont donc désormais facultatives
* PowerBIEmbedded
  - Ajout de la prise en charge pour les applets de commande de capacité Power BI Embedded
  - Nouvelle applet de commande Get-AzureRmPowerBIEmbeddedCapacity - Obtient les détails d’une capacité Power BI Embedded.
  - Nouvelle applet de commande New-AzureRmPowerBIEmbeddedCapacity - Crée une nouvelle capacité Power BI Embedded
  - Nouvelle applet de commande Remove-AzureRmPowerBIEmbeddedCapacity - Supprime une instance de capacité Power BI Embedded
  - Nouvelle applet de commande Resume-AzureRmPowerBIEmbeddedCapacity - Reprend une instance de capacité Power BI Embedded
  - Nouvelle applet de commande Suspend-AzureRmPowerBIEmbeddedCapacity - Suspend une instance de capacité Power BI Embedded
  - Nouvelle applet de commande Test-AzureRmPowerBIEmbeddedCapacity - Teste l’existence d’une instance de capacité Power BI Embedded
  - Nouvelle applet de commande Update-AzureRmPowerBIEmbeddedCapacity - Modifie une instance de capacité Power BI Embedded
* Profil
  - Mise à jour de USGovernmentActiveDirectoryEndpoint pour https://login.microsoftonline.us/
    - Pour plus d’informations sur les mappages de point de terminaison Azure Government, consultez la rubrique suivante : https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - Ajout - Prise en charge AsJob pour les applets de commande, permettant aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression
    - Ajout - Paramètre AsJob à l’applet de commande Get-AzureRmSubscription
* RecoveryServices.Backup
  - Correction d’un bogue - Get-AzureRmRecoveryServicesBackupItem doit réaliser une comparaison insensible à la casse pour le filtre de nom de conteneur.
  - Correction de bogue - AzureVmItem possède maintenant une propriété qui indique la dernière fois qu’une opération de sauvegarde a été réalisée - LastBackupTime.
* Ressources
  - Résolution du problème où Get-AzureRMRoleAssignment entraînait une affectation sans nom de roledefiniton pour des rôles personnalisés
    - Les utilisateurs peuvent désormais utiliser Get-AzureRMRoleAssignment avec des affectations possédant des noms de roledefinition quel que soit le type de rôle
  - Résolution du problème où Set-AzureRMRoleRoleDefinition générait des erreurs introuvables de bureau à distance lorsqu’il y avait une nouvelle étendue dans assignablescopes
    - Les utilisateurs peuvent désormais utiliser Set-AzureRMRoleRoleDefinition avec des étendues assignables, y compris les nouvelles étendues, quelle que soit la position de l’étendue
  - Autoriser les étendues à se terminer par « / »
    - Les utilisateurs peuvent désormais utiliser les applets de commande RoleDefinition et RoleAssignment avec des étendues se terminant par « / », cohérentes avec les API et CLI
  - Autoriser les utilisateurs à créer RoleAssignment en utilisant l’indicateur de délégation
    - Les utilisateurs peuvent désormais utiliser New-AzureRMRoleAssignment avec une option d’ajout de l’indicateur de délégation
  - Corriger RoleAssignment afin de respecter le paramètre d’étendue
  - Ajouter un alias pour ServicePrincipalName dans l’applet de commande New-AzureRmRoleAssignment
    - Les utilisateurs peuvent désormais utiliser ApplicationId au lieu de ServicePrincipalName lors de l’utilisation de l’applet de commande New-AzureRmRoleAssignment
* SiteRecovery
  - Ajouter des avertissements de désapprobation pour toutes les applets de commande dans ce module en vue de la prochaine version de modification avec rupture.
    - Veuillez consulter le guide de modifications avec rupture à venir pour plus d’informations sur la migration de vos applets de commande à partir de AzureRM.
* SQL
  - Ajout de la possibilité de renommer la base de données à l’aide de Set-AzureRmSqlDatabase
  - Problème résolu https://github.com/Azure/azure-powershell/issues/4974
    - Fourniture de la valeur AUDIT_CHANGED_GROUP non valide pour l’audit des applets de commande qui ne génère plus d’erreur et sera supprimée dans une prochaine version.
  - Problème résolu https://github.com/Azure/azure-powershell/issues/5046
    - Le paramètre AuditAction dans l’audit des applets de commande n’est plus ignoré
  - Correction d’un problème dans les applets de commande de l’audit lorsque le StorageKeyType « secondaire » est fourni
    - Lors du paramétrage de l’audit blob, la clé de compte de stockage principal a été utilisée au lieu de la clé secondaire lors de la fourniture de valeur « secondaire » pour le paramètre StorageKeyType.
  - Modifier la formulation du message de confirmation pour Set-AzureRmSqlServerTransparentDataEncryptionProtector
* Azure (RDFE)
    - Supprimer toutes les applets de commande RemoteApp
* Azure.Storage
    - Mise à niveau vers Azure Storage Client Library 8.6.0 et Azure Storage DataMovement Library 0.6.5

## <a name="20171110-version-501"></a>10/11/2017 - Version 5.0.1
* Résolution du problème de chargement d’assembly qui a provoqué l’échec des applets de commande lors de l’exécution dans les modules suivants :
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>8/11/2017 - Version 5.0.0
* REMARQUE :  Il s’agit d’une modification critique. Veuillez consulter le guide de migration (https://aka.ms/azps-migration-guide) pour une liste complète des modifications critiques introduites.
* Toutes les cmdlets contenus dans AzureRM prennent désormais en charge l’aide en ligne
  - Exécutez Get-Help avec le paramètre -Online pour ouvrir l’aide en ligne dans votre navigateur Internet par défaut
* AnalysisServices
  * Correction de la commande Synchronize-AzureAsInstance pour utiliser la nouvelle API REST AsAzure pour la synchronisation
* ApiManagement
  * Veuillez consulter le guide de migration pour les modifications critiques apportées à cette version pour ApiManagement
  * Mise à jour de l’applet de commande Get-AzureRmApiManagementUser pour résoudre le problème https://github.com/Azure/azure-powershell/issues/4510
  * Mise à jour de l’applet de commande New-AzureRmApiManagementApi pour créer une API avec un chemin vide https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
  * Ajout des commandes pour obtenir/créer/supprimer une ressource Application Insights
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Ajout des commandes pour obtenir/mettre à jour la tarification/limite quotidienne de la ressource Application Insights
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Ajout des commandes pour obtenir/créer/mettre à jour/supprimer l’exportation continue d’une ressource Application Insights
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Ajout des commandes pour obtenir/créer/supprimer les clés API d’une ressource Application Insights
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * Ajout de nouveaux paramètres à `New-AzureRmBatchAccount`.
    - `PoolAllocationMode`: Mode d’allocation à utiliser pour créer des pools dans le compte Batch. Pour créer un compte Batch qui alloue des nœuds de pool dans l’abonnement de l’utilisateur, configurez sur `UserSubscription`.
    - `KeyVaultId`: ID de ressource du coffre de clés Azure associé au compte Batch.
    - `KeyVaultUrl`: URL du coffre de clés Azure associé au compte Batch.
  * Mise à jour des paramètres de `New-AzureBatchTask`.
    - Suppression du commutateur `RunElevated`. Le paramètre `UserIdentity` a été ajouté pour remplacer `RunElevated`, et un comportement équivalent peut être obtenu en construisant un `PSUserIdentity` comme indiqué ci-dessous :
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - Ajout du paramètre `AuthenticationTokenSettings`. Ce paramètre vous permet de demander au service Batch de vous fournir un jeton d’authentification pour la tâche lorsqu’elle s’exécute. Cela évite d’avoir à transmettre les clés de compte Batch à la tâche pour qu’elle émette des requêtes au service Batch.
    - Ajout du paramètre `ContainerSettings`.
      - Ce paramètre vous permet de demander au service Batch d’exécuter la tâche à l’intérieur d’un conteneur.
    - Ajout du paramètre `OutputFiles`.
      - Ce paramètre vous permet de configurer la tâche pour télécharger les fichiers dans le stockage Azure après avoir terminé.
  * Mise à jour des paramètres de `New-AzureBatchPool`.
    - Ajout du paramètre `UserAccounts`.
      - Ce paramètre définit les comptes d’utilisateur créés sur chaque nœud dans le pool.
    - Ajout de `TargetLowPriorityComputeNodes` et `TargetDedicated` renommé `TargetDedicatedComputeNodes`.
      - Un alias `TargetDedicated` a été créé pour le paramètre `TargetDedicatedComputeNodes`.
    - Ajout du paramètre `NetworkConfiguration`.
      - Ce paramètre vous permet de configurer les paramètres réseau des pools.
  * Mise à jour des paramètres de `New-AzureBatchCertificate`.
    - Le paramètre `Password` est maintenant `SecureString`.
  * Mise à jour des paramètres à `New-AzureBatchComputeNodeUser`.
    - Le paramètre `Password` est maintenant `SecureString`.
  * Mise à jour des paramètres à `Set-AzureBatchComputeNodeUser`.
    - Le paramètre `Password` est maintenant `SecureString`.
  * Paramètre `Name` renommé `Path` sur `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, et `Remove-AzureBatchNodeFile`.
    - Un alias `Name` a été créé pour le paramètre `Path`.
  * Modifications apportées aux objets
    - Veuillez consulter le journal des modifications Batch pour obtenir la liste complète
  * Ajout de la prise en charge pour l’authentification basée sur Azure Active Directory.
    - Pour utiliser l’authentification Azure Active Directory, vous devez récupérer un objet `BatchAccountContext` à l’aide de la cmdlet `Get-AzureRmBatchAccount`, et fournir l’élément `BatchAccountContext` au paramètre `-BatchContext` d’une cmdlet de service Batch. L’authentification Azure Active Directory est obligatoire pour les comptes avec `PoolAllocationMode = UserSubscription`.
    - Pour les comptes existants ou pour les nouveaux comptes créés avec `PoolAllocationMode = BatchService`, vous pouvez continuer à utiliser l’authentification par clé partagée en récupérant un objet `BatchAccountContext` à l’aide de la cmdlet `Get-AzureRmBatchAccoutKeys`.
* Calcul
  * Commandes d’extension Azure Disk Encryption
    - Nouveau paramètre 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' pour chiffrer les formats des disques de données
    - Les nouveaux paramètres 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' et '-ExtensionType ' permettent de basculer vers d’autres versions de l’extension
    - Les nouveaux paramètres 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' et '-ExtensionType ' permettent de basculer vers d’autres versions de l’extension
    - Les nouveaux paramètres 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' et '-ExtensionType ' permettent de basculer vers d’autres versions de l’extension
* DataLakeAnalytics
  * Veuillez consulter le guide de migration pour les modifications critiques apportées à cette version pour DataLakeAnalytics
  * Modification d’un des deux types de sortie OutputTypes de Get-AzureRmDataLakeAnalyticsAccount
    - List\<DataLakeAnalyticsAccount> en List\<PSDataLakeAnalyticsAccountBasic>
    - Les propriétés de PSDataLakeAnalyticsAccountBasic sont un sous-ensemble strict des propriétés de DataLakeAnalyticsAccount
    - Les propriétés supplémentaires comprises dans DataLakeAnalyticsAccount ne sont pas retournées par le service.  Par conséquent, cette modification doit le refléter correctement. Ces propriétés supplémentaires sont toujours comprises dans PSDataLakeAnalyticsAccountBasic, mais elles sont marquées comme obsolètes.
  * Modification d’un des deux types de sortie OutputTypes de Get-AzureRmDataLakeAnalyticsJob
    - List\<JobInformation> en List\<PSJobInformationBasic>
    - Les propriétés de PSJobInformationBasic sont un sous-ensemble strict des propriétés de JobInformation
    - Les propriétés supplémentaires comprises dans JobInformation ne sont pas retournées par le service.  Par conséquent, cette modification doit le refléter correctement. Ces propriétés supplémentaires sont toujours comprises dans PSJobInformationBasic, mais elles sont marquées comme obsolètes.
* DataLakeStore
  * Veuillez consulter le guide de migration pour les modifications critiques apportées à cette version pour DataLakeStore
  * Modification d’un des deux types de sortie OutputTypes de Get-AzureRmDataLakeStoreAccount
    - List\<PSDataLakeStoreAccount> en List\<PSDataLakeStoreAccountBasic>
    - Les propriétés de PSDataLakeStoreAccountBasic sont un sous-ensemble strict des propriétés de PSDataLakeStoreAccount
    - Les propriétés supplémentaires comprises dans PSDataLakeStoreAccount ne sont pas retournées par le service.  Par conséquent, cette modification doit le refléter correctement. Ces propriétés supplémentaires sont toujours comprises dans PSDataLakeStoreAccountBasic, mais elles sont marquées comme obsolètes.
* DNS
  * Prise en charge des types d’enregistrement CAA dans le DNS Azure
    - Prend en charge toutes les opérations sur le type d’enregistrement CAA
* Event Hub
  * Veuillez consulter le guide de migration pour les modifications de rupture apportées à cette version pour EventHub
* Insights
  * Veuillez consulter le guide de migration pour les modifications de rupture apportées à cette version pour Insights
* Réseau
  * Veuillez consulter le guide de migration pour les modifications de rupture apportées à cette version pour Network
  * Ajout d’une applet de commande pour lister les fournisseurs de services internet disponibles pour une région Azure spécifique
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Ajout d’une cmdlet pour obtenir le score de la latence relatif pour les fournisseurs de services Internet à partir d’un emplacement spécifié pour les régions Azure
    - Get-AzureRmNetworkWatcherReachabilityReport
* Profil
  - Set-AzureRmDefault
    - Utilisez cette cmdlet pour définir un groupe de ressources par défaut.  Cela rendra le paramètre -ResourceGroup optionnel pour certaines cmdlets, et utilisera le groupe par défaut quand un groupe de ressources n’est pas spécifié
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Si le groupe de ressources spécifié est compris dans l’abonnement, ce groupe de ressources sera défini par défaut.  Sinon, le groupe de ressources sera créé et puis défini par défaut.
  - Get-AzureRmDefault
    - Utilisez cette cmdlet pour obtenir le groupe de ressources par défaut actif (et les autres valeurs par défaut dans le futur).
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Utilisez cette cmdlet pour supprimer le groupe de ressources par défaut actif
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment et Set-AzureRmEnvironment
    - Ajoutez le paramètre BatchAudience, qui vous permet de spécifier l’audience d’Azure Batch Active Directory à utiliser lors de l’acquisition de jetons d’authentification pour le service Batch.
* RecoveryServices.Backup
  * Ajout de cmdlets pour effectuer une récupération de fichier instantanée.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * Mise à jour du kit de développement logiciel (SDK) RecoveryServices.Backup à la version la plus récente
  * Mise à jour des tests pour la charge de travail de la machine virtuelle Azure, afin que toutes les configurations requises pour les séries de tests soient effectuées par les tests eux-mêmes.
  * Correctifs https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
  * Modifications pour ASR VMware vers Azure Site Recovery (les cmdlets prennent actuellement en charge des opérations pour Enterprise vers Enterprise, Enterprise vers Azure, HyperV vers Azure)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * Ajout de la prise en charge pour le coffre AAD
  * Ajout de cmdlets pour gérer les ressources de VCenter
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Ajout d’autres cmdlets
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - Veuillez consulter le guide de migration pour les modifications critiques apportées à cette version pour ServiceBus
* SQL
  * Ajout de prise en charge pour lister et annuler l’opération asynchrone updateslo sur la base de données
    - Mise à jour de la cmdlet existante Get-AzureRmSqlDatabaseActivity pour retourner le statut d’opération updateslo de la base de données.
    - Ajout d’une nouvelle cmdled Stop-AzureRmSqlDatabaseActivity pour annuler l’opération asynchrone updateslo sur la base de données.
  * Ajout de la prise en charge de la redondance de zone pour les bases de données et les pools élastiques
    - Ajout du paramètre de commutateur ZoneRedundant à New-AzureRmSqlDatabase
    - Ajout du paramètre de commutateur ZoneRedundant à Set-AzureRmSqlDatabase
    - Ajout du paramètre de commutateur ZoneRedundant à New-AzureRmSqlElasticPool
    - Ajout du paramètre de commutateur ZoneRedundant à Set-AzureRmSqlElasticPool
  * Ajout de la prise en charge pour les alias du serveur DNS
    - Ajout d’une cmdlet Get-AzureRmSqlServerDnsAlias qui obtient des alias de serveur DNS par le serveur et d’un nom d’alias ou une liste d’alias de serveur DNS pour un serveur Azure SQL.
    - Ajout d’une cmdlet New-AzureRmSqlServerDnsAlia qui crée un nouvel alias de serveur DNS pour un serveur Azure SQL donné
    - Ajout d’une cmdlet AzurermSqlServerDnsAlias qui permet la mise à jour d’un serveur Azure SQL vers lequel pointe un alias de serveur DNS
    - Ajout d’une cmdlet Remove-AzureRmSqlServerDnsAlias qui supprime un alias de serveur DNS pour un serveur Azure SQL
* Azure.Storage
  * Mise à niveau vers Azure Storage Client Library 8.5.0 et Azure Storage DataMovement Library 0.6.3
  * Ajout de la fonctionnalité de prise en charge du partage de fichiers instantanés
    - Ajout d’un paramètre 'SnapshotTime' à Get-AzureStorageShare
    - Ajout d’un paramètre 'IncludeAllSnapshot' à Remove-AzureStorageShare
