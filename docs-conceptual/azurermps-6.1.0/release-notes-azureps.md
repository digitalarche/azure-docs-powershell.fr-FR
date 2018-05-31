---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461751"
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

---
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