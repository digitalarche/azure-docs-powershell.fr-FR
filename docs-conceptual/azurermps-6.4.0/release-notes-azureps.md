---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406292"
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

---
## <a name="640---july-2018"></a>6.4.0 - Juillet 2018
#### <a name="general"></a>Généralités
* Correction de mise en forme de OutputType dans les fichiers d’aide pour la plupart des modules

#### <a name="azurermprofile"></a>AzureRM.Profile
* Ajout de l’attribut Ps1Xml aux types de sortie de base

#### <a name="azurermcompute"></a>AzureRM.Compute
* Fonctionnalité IP Tag pour VMSS
    - La cmdlet New-AzureRmVmssIpTagConfig est ajoutée
    - Ajout du paramètre IpTag à New-AzureRmVmssIpConfig
* Fonctionnalité de restauration du système d’exploitation automatique pour VMSS
    - Les paramètres DisableAutoRollback sont ajoutés à New-AzureRmVmssConfig et Update-AzureRmVmss
* Fonctionnalité OS Upgrade History pour Vmss
    - Le paramètre de commutateur OSUpgradeHistory est ajouté à Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Ajout de la prise en charge des listes de contrôle d’accès de catalogue avec les commandes suivantes :
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Ajout de la prise en charge de l’annulation et du suivi de la progression pour Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Ajout de la prise en charge de l’annulation pour Export-AzureRmDataLakeStoreChildItemProperties
* Correction du vidage des messages de débogage pour les cmdlets qui effectuent des opérations récursives
* Correction de l’emplacement du test des applets de commande DataLake

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Ajout du paramètre MaxCount facultatif à la cmdlet Répertorier les opérations Get-AzureRmEventHub et Get-AzureRmEventHubConsumerGroup
* Résolution du problème dans la cmdlet New-AzureRmEventHub où au moins un paramètre est nécessaire lors de la création du nouveau EventHub. Jeu de paramètres par défaut fourni.
* Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmEventHubKey, qui permet à l’utilisateur de fournir KeyValue.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Résolution d’un problème où toutes les ressources sont renvoyées par Get-AzureRmKeyVault -Tag

#### <a name="azurermnetwork"></a>AzureRM.Network
* Exposer les nouvelles références SKU pour Zone-Redundant VirtualNetworkGateways
* Ajout de nouvelles commandes pour la fonctionnalité : API de partenaire ExpressRoute via ARM
    - Ajout de Get-AzureRmExpressRouteCrossConnection
    - Ajout de Set-AzureRmExpressRouteCrossConnection
    - Ajout de Add-AzureRmExpressRouteCrossConnectionPeering
    - Ajout de Get-AzureRmExpressRouteCrossConnectionPeering
    - Ajout de Remove-AzureRmExpressRouteCrossConnectionPeering
    - Ajout de Get-AzureRMExpressRouteCrossConnectionArpTable
    - Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTable
    - Ajout de Get-AzureRMExpressRouteCrossConnectionRouteTableSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Ajout de la cmdlet Get-AzureRmRecoveryServicesBackupStatus. Cette cmdlet prend un ID de machine virtuelle et vérifie si la machine virtuelle est protégée par un coffre dans l’abonnement. Si un tel coffre existe, la cmdlet sort les informations du coffre.

#### <a name="azurermresources"></a>AzureRM.Resources
* Mettre à jour les cmdlets Get-AzureRmPolicyAssignment :
    - Ajouter la prise de l’énumération des valeurs -Scope values au niveau du groupe de gestion
    - Ajouter la prise en charge de la récupération des affectations individuelles avec les valeurs -Scope au niveau du groupe de gestion
    - Ajouter les commutateurs -Effective et -All au paramètre de contrôle
* Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition
    - Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné
    - Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné
* Mettre à jour les cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition
    - Ajouter le paramètre - ManagementGroupName pour appliquer des opérations à un groupe de gestion donné
    - Ajouter le paramètre -SubscriptionId pour appliquer des opérations à un abonnement donné
* Ajouter la prise en charge des références secrètes des coffres de clés dans les paramètres lors de l’utilisation de TemplateParameterObject dans New-AzureRmResourceGroupDeployment
* Correction du problème où le paramètre EndDatea été ignoré pour New-AzureRmADAppCredential
    - https://github.com/Azure/azure-powershell/issues/6505
* Correction du problème où Add-AzureRmADGroupMember a utilisé une URL pour effectuer la demande
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Ajout du Parameter -KeyValue facultatif à la cmdlet New-AzureRmServiceBusKey, qui permet à l’utilisateur de fournir KeyValue.

#### <a name="azurermsql"></a>AzureRM.Sql
* Clarification des points de restauration définis par l’utilisateur pour SQLDW dans l’aide de New-AzureRmSqlDatabaseRestorePoint
* Mise à jour de la documentation du paramètre - ComputeGeneration dans plusieurs cmdlets

## <a name="630---june-2018"></a>6.3.0 - juin 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Mise à jour des messages d’erreur pour la commande Enable-AzureRmContextAutoSave
* Création d’un contexte pour chaque abonnement lors de l’exécution de la commande Connect-AzureRmAccount sans contexte précédent

#### <a name="azurestorage"></a>Azure.Storage
* Ajout d’informations supplémentaires sur le paramètre -Permissions dans les fichiers d’aide.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Get-AzureRmVmDiskEncryptionStatus résout un problème rencontré sur les machines virtuelles sans disques de données 
* Mise à jour de la version de la bibliothèque de client Compute pour résoudre les cmdlets suivantes
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Problème relatif aux cmdlets suivantes résolu afin d’afficher « ID d’opération » et « État d’opération » correctement :
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Suppression des conditions de validation de ValidateNotNullOrEmpty pour SubjectBeginsWith/SubjectEndsWith dans la cmdlet Update-AzureRmEventGridSubscription afin de changer ces paramètres pour vider la chaîne, si nécessaire.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Résolution d’un problème où les balises sont retournées lorsque la commande Get-AzureRmKeyVault est exécutée

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Version publique des cmdlets Policy Insights
    - Utiliser l’API de version du 04/04/2018
    - Ajout de PolicyDefinitionReferenceId aux résultats de la commande Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Ajout du paramètre -Vault aux cmdlets RecoveryServices.Backup. Une fois envoyé, il écrasera la cmdlet Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Mise à jour d’un exemple dans le fichier d’aide de la commande Get-AzureRmSqlDatabaseExpanded

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Mise à jour du fichier d’aide de la commande Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Mise à jour de la commande Set-AzureRMWebApp afin qu’elle n’écrase pas le paramètre AppSettings lors de l’exécution de -AssignIdentity
* Mise à jour de la commande New-AzureRMWebAppSlot pour rendre optionnel le paramètre AppServicePlan

## <a name="621---june-2018"></a>6.2.1 - juin 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Mise à jour du modèle PSWorkspace pour permettre à Network d’utiliser le type en paramètre

## <a name="620---june-2018"></a>6.2.0 - Juin 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Correction d’un problème où la version 10.0.3 de Newtonsoft.Json n’était pas chargée lors de l’importation du module

#### <a name="azurermcompute"></a>AzureRM.Compute
* Fonctionnalité de mise à jour de machine virtuelle de groupe de machines virtuelles identiques (VMSS)
    - Ajout des cmdlet « Update-AzureRmVmssVM » et « New-AzureRmVMDataDisk »
    - Ajout du paramètre VirtualMachineScaleSetVM à la cmdlet « Add-AzureRmVMDataDisk » pour prendre en charge l’ajout d’un disque de données à un groupe de machines virtuelles identiques (VMSS).

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.8.0 - préversion , qui contient les modifications suivantes :
    - Ajout de l’opération de référentiel de configuration de fabrique
    - Mise à jour des QuickBooks LinkedService pour exposer les propriétés consumerKey et consumerSecret
    - Mise à jour de plusieurs types de modèle de SecretBase à l’objet
    - Ajout d’un déclencheur d’événements d’objet Blob

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Mise à jour de la documentation avec l’exemple de sortie

### <a name="azurermnetwork"></a>AzureRM.Network
* Activation des paramètres Traffic Analytics sur les cmdlet Network Watcher

#### <a name="azurermresources"></a>AzureRM.Resources
* Résolution d’un problème où la propriété « Properties » des objets « PSResource » était retournée à partir de « Get-AzureRmResource »

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Correction d’un problème de mise à jour où ServiceBusQueueJob ne définissait pas de nouvelles valeurs d’authentification

### <a name="azurermsql"></a>AzureRM.Sql
* Mise à jour des cmdlet suivantes avec le paramètre facultatif LicenseType
    - New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* « New-AzureRMWebApp » est mis à jour pour utiliser des algorithmes communs à partir de la bibliothèque de stratégies.

## <a name="610---may-2018"></a>6.1.0 - Mai 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Correction d’un problème où un contexte vide avec le nom du contexte par défaut précédent était conservé lors de l’exécution de « Clear-AzureRmContext », ce qui empêchait l’utilisateur de créer un nouveau contexte avec l’ancien nom

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Activation des opérations d’association/dissociation de passerelle sur les systèmes autonomes

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Ajout de la prise en charge des éléments ApiVersions, ApiReleases et ApiRevisions
* Ajout de la prise en charge du principal ServiceFabric
* Ajout de la prise en charge de l’enregistreur d’événements Application Insights
* Ajout de la reconnaissance de la référence « De base » comme une référence valide du service Gestion des Api
* Ajout de la prise en charge de l’installation des certificats émis par une autorité de certification privée en tant que certificats racine ou d’autorité de certification
* Ajout de la prise en charge des certificats SSL personnalisés via KeyVault et de plusieurs noms d’hôte de proxy
* Ajout de la prise en charge de l’identité MSI
* Ajout de la prise en charge des stratégies via une URL. REMARQUE : les cmdlet suivantes seront déconseillées dans une version ultérieure :
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Ajout de la nouvelle cmdlet Get-AzureBatchPoolNodeCounts
* Ajout de la nouvelle cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Ajout des nouveaux paramètres Expand, ResourceGroup, InstanceName, InstanceId, Tags et Top pour la cmdlet Get-AzureRmConsumptionUsageDetail

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Correction de l’exemple pour Export-AzureRmDataLakeStoreChildItemProperties
* Correction de l’exception de paramètre Null pour le cas Recurse dans Set-AzureRmDataLakeStoreItemAclEntry 
* Correction des fichiers d’aide pour Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl et Remove-AzureRmDataLakeStoreItemAclEntry 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Passage de la version du Kit de développement logiciel (SDK) Network de 18.0.0-preview à 19.0.0-preview
* Ajout d’une cmdlet pour créer une configuration de protocole :
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Ajout d’une cmdlet pour ajouter une nouvelle connexion de circuit à un circuit ExpressRoute existant :
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Ajout d’une cmdlet pour supprimer une connexion de circuit d’un circuit ExpressRoute existant :
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Ajout d’une cmdlet pour récupérer une connexion de circuit :
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Correction de l’utilisation de l’authentification serveur avec les certificats générés (problème nº 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* Mise à jour des cmdlets d’audit pour permettre la suppression des éléments AuditAction ou AuditActionGroup
* Correction d’un problème concernant Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy lors de la définition d’une nouvelle stratégie de rétention flexible, où la commande échouait avec le message d’erreur « Configure long term retention policy with azure recovery service vault and policy is no longer supported. Please submit request with the new flexible retention policy » (La configuration d’une stratégie de rétention à long terme avec un coffre et une stratégie Azure Recovery Services n’est plus prise en charge. Veuillez soumettre une demande avec la nouvelle stratégie de rétention flexible.).
* Mise à jour de toutes les cmdlets liées à la création/mise à jour de bases de données/pools élastiques Azure SQL pour utiliser la nouvelle API Base de données, qui prend en charge la propriété Sku pour les propriétés liées à la mise à l’échelle et au niveau.
* Les cmdlets mises à jour incluent : 
    - New-AzureRmSqlDatabase ; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool ; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Mise à jour des paramètres pour « Get-AzureRmTrafficManagerProfile » afin que le paramètre -ResourceGroupName soit requis lors de l’utilisation du paramètre -name