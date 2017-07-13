---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: "Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-resource-manager
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 5c8fa2a5a8f94cd24b66f42c237749a7b89af3b3
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="version-400"></a>Version 4.0.0

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
