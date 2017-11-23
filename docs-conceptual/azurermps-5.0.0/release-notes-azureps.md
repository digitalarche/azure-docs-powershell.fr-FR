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
ms.date: 11/14/2017
ms.openlocfilehash: ab35cbc4ec1a0bd4e7ee40e1864bd7941f5bca87
ms.sourcegitcommit: 79dd3700b5cb4cb90b268778b482082052160093
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2017
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

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
* Remarque : Il s’agit d’une modification critique. Veuillez consulter le guide de migration (https://aka.ms/azps-migration-guide) pour une liste complète des modifications critiques introduites.
* Toutes les cmdlets contenus dans AzureRM prennent désormais en charge l’aide en ligne
    - Exécutez Get-Help avec le paramètre -Online pour ouvrir l’aide en ligne dans votre navigateur Internet par défaut
* AnalysisServices
    * Correction de la commande Synchronize-AzureAsInstance pour utiliser la nouvelle API REST AsAzure pour la synchronisation
* ApiManagement
    * Veuillez consulter le guide de migration pour les modifications critiques apportées à cette version pour ApiManagement
    * Mise à jour de la cmdlet Get-AzureRmApiManagementUser pour résoudre le problème https://github.com/Azure/azure-powershell/issues/4510
    * Mise à jour de la cmdlet New-AzureRmApiManagementApi pour créer une API avec un chemin vide https://github.com/Azure/azure-powershell/issues/4069
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
        - `PoolAllocationMode` : Le mode d’allocation à utiliser pour créer des pools dans le compte Batch. Pour créer un compte Batch qui alloue des nœuds de pool dans l’abonnement de l’utilisateur, configurez sur `UserSubscription`.
        - `KeyVaultId` : L’ID de ressource du coffre Azure Key Vault associé au compte Batch.
        - `KeyVaultUrl` : L’URL du coffre Azure Key Vault associé au compte Batch.
    * Mise à jour des paramètres de `New-AzureBatchTask`.
        - Suppression du commutateur `RunElevated`. Le paramètre `UserIdentity` a été ajouté pour remplacer `RunElevated`, et un comportement équivalent peut être obtenu en construisant un `PSUserIdentity` comme indiqué ci-dessous :
            - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
            - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
        - Ajout du paramètre `AuthenticationTokenSettings`. Ce paramètre vous permet de demander au service Batch de vous fournir un jeton d’authentification pour la tâche lorsqu’elle s’exécute. Cela évite d’avoir à transmettre les clés de compte Batch à la tâche pour qu’elle émette des requêtes au service Batch.
        - Ajout du paramètre `ContainerSettings`.
            - Ce paramètre vous permet de demander au service Batch d’exécuter la tâche à l’intérieur d’un conteneur.
        - Ajout du paramètre `OutputFiles`.
            - Ce paramètre vous permet de configurer la tâche pour télécharger les fichiers dans le stockage Azure après avoir terminé.
    * Mise à jour des paramètres à `New-AzureBatchPool`.
        - Ajout du paramètre `UserAccounts`.
            - Ce paramètre définit les comptes d’utilisateur créés sur chaque nœud dans le pool.
        - Ajout de `TargetLowPriorityComputeNodes` et `TargetDedicated` renommé `TargetDedicatedComputeNodes`.
            - Un alias `TargetDedicated` a été créé pour le paramètre `TargetDedicatedComputeNodes`.
        - Ajout du paramètre `NetworkConfiguration`.
            - Ce paramètre vous permet de configurer les paramètres réseau des pools.
    * Mise à jour des paramètres à `New-AzureBatchCertificate`.
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
    * Corrections https://github.com/Azure/azure-powershell/issues/3164
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