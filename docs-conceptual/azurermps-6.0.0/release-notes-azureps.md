---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

---

## <a name="600---may-2018"></a>6.0.0 - Mai 2018

### <a name="general"></a>Généralités
* Configurer la dépendance minimale des modules sur PowerShell 5.0

### <a name="azurestorage"></a>Azure.Storage
* Support comme nom du conteneur d’objets blob du stockage Azure
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Corrige le fait qu’une sortie d’échec d’applets de commande de stockage ne contient pas les informations détaillées de l’échec

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Introduit plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermautomation"></a>AzureRM.Automation
* Retrait des alias des « balises » déconseillées des applets de commande
    - 'Set-AzureRmAutomationRunbook'

### <a name="azurermbatch"></a>AzureRM.Batch
* Mise à jour de la documentation sur New-AzureBatchPool pour supprimer l’exemple déconseillé

### <a name="azurermcdn"></a>AzureRM.Cdn
* Introduit plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermcompute"></a>AzureRM.Compute
* « New-AzureRmVm » et « New-AzureRmVmss » prennent en charge la sortie détaillée des paramètres
* « New-AzureRmVm » et « New-AzureRmVmss » (ensemble de paramètres simples) prennent en charge l’attribution d’identités définies par le système et/ou d’identités définies par l’utilisateur pour les machines virtuelles.
* Fonction Redeploy et PerformMaintenance de VMSS
    -  Ajoute un nouveau paramètre de commutateur-Redeploy et -PerformMaintenance à « Set-AzureRmVmss » et « Set-AzureRmVmssVM »
* Ajoute un paramètre de commutateur DisableVMAgent à l’applet de commande « Set-AzureRmVMOperatingSystem »
* « New-AzureRmVm » et « New-AzureRmVmss » (ensemble de paramètres simples) prennent en charge une image « Win10 ».
* L’applet de commande « Repair-AzureRmVmssServiceFabricUpdateDomain » est ajouté.
* Introduit plusieurs changements cassants
    - Pour plus de détails, reportez-vous au guide de migration
* « Set-AzureRmVmDiskEncryptionExtension » rend les paramètres AAD facultatifs

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Retrait des alias des « balises » déconseillées des applets de commande
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* La mise à jour du Kit de développement logiciel (SDK) .Net ADF vers la version 0.7.0 - préversion , qui contient les modifications suivantes :
    - Ajout des paramètres d’exécution et de la propriété des gestionnaires de connexion sur l’activité ExecuteSSISPackage
    - Mise à jour du service lié PostgreSql et MySql pour utiliser une chaîne de connexion complète au lieu d’un serveur, d’une base de données, d’un schéma, d’un nom d’utilisateur et d’un mot de passe
    - Retrait du schéma du service lié D2B
    - Retrait de la propriété du schéma du service lié Teradata
    - Ajout de service lié, jeu de données, copie source pour Responsys

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Retrait des alias des « balises » déconseillées des applets de commande
    - «New-AzureRmDataLakeAnalyticsAccount»
    - «Set-AzureRmDataLakeAnalyticsAccount»

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Ajout d’une nouvelle fonctionnalité de changements ACL récursifs à Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Ajout d’un nouvel applet de commande pour la récupération du résumé du contenu dans un répertoire
* Ajout d’un nouvel applet de commande pour récupérer le vidage des ACL et l’utilisation du disque
* Type de retour correct de Set-AzureRmDataLakeStoreItemAcl bool sur IEnumerable<DataLakeStoreItemAce>
* Type de retour correct de Set-AzureRmDataLakeStoreItemAclEntry bool sur IEnumerable<DataLakeStoreItemAce>
* Changements cassant dans Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem

### <a name="azurermdns"></a>AzureRM.Dns
* Introduit plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermeventhub"></a>AzureRM.EventHub
* Mise à jour de l’aide pour les applets de commande ayant des exemples manquants

### <a name="azurerminsights"></a>AzureRM.Insights
* Introduction de plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermiothub"></a>AzureRM.IotHub
* Activation des balises et de la référence SKU de base sur IotHub

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Changements cassants pour la prise en charge des scénarios de redirection
* Ajout de nouveaux applets de commande : Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, et Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Retrait des alias des « balises » déconseillées des applets de commande
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Retrait des alias des « balises » déconseillées des applets de commande
    - «Set-AzureRmMediaService»

### <a name="azurermnetwork"></a>AzureRM.Network
* Ajout de la prise en charge de la ressource de plan de protection DDoS
* Introduction de plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Introduit plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Introduit plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermprofile"></a>AzureRM.Profile
* Activation par défaut de l’enregistrement automatique du contexte
* Ajout des propriétés Add USGovernmentOperationalInsightsEndpoint et USGovernmentOperationalInsightsEndpointResourceId à l’environnement Azure pour le gouvernement des États-Unis.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* En-tête d’authentification corrigé dans les scénarios SiteRecovery

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Introduction de plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermresources"></a>AzureRM.Resources
* Suppression d’un paramètre obsolète -AtScopeAndBelow à partir de l’appel Get-AzureRmRoledefinition
* Affectations incluses aux utilisateurs/groupes/principaux de service supprimés dans les résultats de Get-AzureRmRoleAssignment
* Ajout des compléments d’onglet pour Scope et ResourceType
* Ajout d’un applet de commande de commodité pour la création des principaux de service
* Fusion des fonctionnalités Get - et Find- dans Get-AzureRmResource
* Ajout des applets de commande AD :
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Mise à jour de la référence SKU par défaut de la version de l’image Linux
  - NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update

### <a name="azurermstorage"></a>AzureRM.Storage
* Introduction de plusieurs changements cassants
    - Pour plus d’informations, reportez-vous au guide de migration

### <a name="azurermwebsites"></a>AzureRM.Websites
* Mise à jour vers la dernière version du Kit de développement logiciel des sites web
* Ajout des propriétés -AssignIdentity et -Httpsonly pour Set-AzureRmWebApp et Set-AzureRmWebAppSlot
* Ajout de deux nouveaux applets de commande : Get-AzureRmWebAppSnapshots et Restore-AzureRmWebAppSnapshot
