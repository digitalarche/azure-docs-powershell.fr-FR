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
ms.openlocfilehash: cf58789ba69fd2fc157e37d0b052827b361246e5
ms.sourcegitcommit: c42c7176276ec4e1cc3360a93e6b15d32083bf9f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2017
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="20171208-version-511"></a>08.12.2017 Version 5.1.1
* AnalysisServices
    - Modification de l’ensemble de l’emplacement valide de recherche dynamique afin que tous les clouds soient pris en charge.
* Automatisation
    - Mettre à jour vers Import-AzureRMAutomationRunbook
        - La prise en charge est désormais fournie pour les runbooks Python2
* Batch
    - Correction d’un bogue dans lequel les opérations de compte sans un groupe de ressources n’ont pas détecté automatiquement le groupe de ressources
* Calcul
    - Get-AzureRmComputeResourceSku affiche des informations de zone.
    - Mise à jour de Disable-AzureRmVmssDiskEncryption pour résoudre le problème https://github.com/Azure/azure-powershell/issues/5038
    - Ajout - Prise en charge AsJob pour les applets de commande de calcul longs. Permet aux applets de commande sélectionnées de s’exécuter en arrière-plan et de retourner une tâche pour suivre et contrôler la progression.
        - Les applets de commande affectées incluent : les applets de commande New-, Update-, Set-, Remove-, Start-, Restart-, Stop- pour les machines virtuelles et les groupes de machines virtuelles identiques
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
    - Ajout de deux nouvelles applets de commande : Update-AzureRmDataFactoryV2 et Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
    - Ajout d’un paramètre appelé ScriptParameter à Submit-AzureRmDataLakeAnalyticsJob
        - Des informations détaillées sur ScriptParameter sont accessibles en utilisant Get-Help sur Submit-AzureRmDataLakeAnalyticsJob
    - Pour New-AzureRmDataLakeAnalyticsAccount, modification du paramètre MaxDegreeOfParallelism en MaxAnalyticsUnits
        - Ajout d’un alias pour le paramètre MaxAnalyticsUnits : MaxDegreeOfParallelism
    - Pour New-AzureRmDataLakeAnalyticsComputePolicy, modification du paramètre MaxDegreeOfParallelismPerJob en MaxAnalyticsUnitsPerJob
        - Ajout d’un alias pour le paramètre MaxAnalyticsUnitsPerJob : MaxDegreeOfParallelismPerJob
    - Pour Set-AzureRmDataLakeAnalyticsAccount, modification du paramètre MaxDegreeOfParallelism en MaxAnalyticsUnits
        - Ajout d’un alias pour le paramètre MaxAnalyticsUnits : MaxDegreeOfParallelism
    - Pour Submit-AzureRmDataLakeAnalyticsJob, modification du paramètre DegreeOfParallelism en AnalyticsUnits
        - Ajout d’un alias pour le paramètre AnalyticsUnits : DegreeOfParallelism
    - Pour Update-AzureRmDataLakeAnalyticsComputePolicy, modification du paramètre MaxDegreeOfParallelismPerJob en MaxAnalyticsUnitsPerJob
        - Ajout d’un alias pour le paramètre MaxAnalyticsUnitsPerJob : MaxDegreeOfParallelismPerJob
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
    - Mise à jour USGovernmentActiveDirectoryEndpoint sur https://login.microsoftonline.us/
        - Pour plus d’informations sur les mappages de point de terminaison Azure Government, veuillez consulter la rubrique suivante : https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
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
    - Résolution du problème https://github.com/Azure/azure-powershell/issues/4974
        - Fourniture de la valeur AUDIT_CHANGED_GROUP non valide pour l’audit des applets de commande qui ne génère plus d’erreur et sera supprimée dans une prochaine version.
    - Résolution du problème https://github.com/Azure/azure-powershell/issues/5046
        - Le paramètre AuditAction dans l’audit des applets de commande n’est plus ignoré
    - Correction d’un problème dans les applets de commande de l’audit lorsque le StorageKeyType « secondaire » est fourni
        - Lors du paramétrage de l’audit blob, la clé de compte de stockage principal a été utilisée au lieu de la clé secondaire lors de la fourniture de valeur « secondaire » pour le paramètre StorageKeyType.
    - Modifier la formulation du message de confirmation pour Set-AzureRmSqlServerTransparentDataEncryptionProtector
* Azure (RDFE)
    - Supprimer toutes les applets de commande RemoteApp
* Azure.Storage
    - Mise à niveau vers Azure Storage Client Library 8.6.0 et Azure Storage DataMovement Library 0.6.5

Modifications de la dernière version : modifications depuis la dernière version :  https://github.com/azure/azure-powershell/compare/v5.0.1-November2017...v5.1.1-December2017

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