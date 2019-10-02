---
title: Notes de publication Azure PowerShell
description: Découvrez toutes les dernières mises à jour des modules Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: f0f09eee03ef9dd7fe07432252a3dc8ca93e3a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2019
ms.locfileid: "71319305"
---
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
### <a name="general"></a>Généralités

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

### <a name="general"></a>Généralités

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
#### <a name="general"></a>Généralités
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