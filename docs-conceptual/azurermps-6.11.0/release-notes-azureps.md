---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738102"
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

---
## <a name="6110---october-2018"></a>6.11.0 - Octobre 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Problème résolu avec Get-AzureRmSubscription dans CloudShell
* Mise à jour du code commun pour utiliser la dernière version de ClientRuntime

#### <a name="azurermbackup"></a>AzureRM.Backup
* Applets de commande Sauvegarde Azure déconseillés.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ajout de nouvelles tailles à la liste blanche des tailles de machine virtuelle pour lesquelles une mise en réseau accélérée sera activée lors de l’utilisation de l’ensemble de paramètres simple pour « New-AzureRmVm »
* Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Ajout de la prise en charge des règles de réseau virtuel
    - Get-AzureRmDataLakeStoreVirtualNetworkRule : obtient ou liste la règle de réseau virtuel d’Azure Data Lake Store.
    - Add-AzureRmDataLakeStoreVirtualNetworkRule : ajoute une règle de réseau virtuel au compte Data Lake Store spécifié.
    - Set-AzureRmDataLakeStoreVirtualNetworkRule : modifie la règle de réseau virtuel spécifiée dans le compte Data Lake Store spécifié.
    - Remove-AzureRmDataLakeStoreVirtualNetworkRule : supprime une règle de réseau virtuel d’Azure Data Lake Store.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Mise à jour de l’applet de commande Test-AzureRmNetworkWatcherConnectivity, passage de la valeur du protocole au serveur principal.
* Ajout d’un complémenteur d’argument ResourceName pour tous les applets de commande.

#### <a name="azurermresources"></a>AzureRM.Resources
* Résout les problèmes où Get-AzureRMRoleDefinition lève une exception inintelligible (lorsque le profil par défaut ne contient aucun abonnement et qu’aucune portée n’est spécifiée) en ajoutant une exception explicite dans le scénario. Définit également le paramètre par défaut sur « RoleDefinitionNameParameterSet ».

## <a name="6100---october-2018"></a>6.10.0 - Octobre 2018
#### <a name="azurestorage"></a>Azure.Storage
* Correction d’un problème où le fichier/objet blob de copie ne copie pas les métadonnées lorsque la destination contient des problèmes de métadonnées
    - Start-AzureStorageBlobCopy
    - Start-AzureStorageFileCopy

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Prise en charge de Get-AzureRmCognitiveServicesAccountSkus sans compte existant.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Correction de Get-AzureRmVM -ResourceGroupName <rg> pour retourner plus de 50 résultats si besoin
* Ajout d’un exemple de la commande « SimpleParameterSet » à l’aide de cmdlet New-AzureRmVmss.
* Correction d’une faute de frappe dans le message de progression d’Azure Disk Encryption

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 2.3.0.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ajout de la fonctionnalité NetworkProfile. nouvelles cmdlets ajoutées
    - Get-AzureRMNetworkProfile
    - New-AzureRMNetworkProfile
    - Remove-AzureRMNetworkProfile
    - Set-AzureRMNetworkProfile
    - New-AzureRMContainerNicConfig
    - New-AzureRmContainerNicConfigIpConfig
* Ajout d’un lien d’association de service sur le modèle de sous-réseau
* Ajout des cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap
* Ajout des cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Autorisez toutes les chaînes en tant que Paramètre de taille à progresser. Ajout de P5 dans la fenêtre contextuelle PSArgumentCompleter

#### <a name="azurermresources"></a>AzureRM.Resources
* Ajout du paramètre manquant -Mode à Set-AzureRmPolicyDefinition
* Correction d’un bug de la cmdlet Get-AzureRmProviderOperation pour les opérations avec Origin comprenant un utilisateur

#### <a name="azurermsql"></a>AzureRM.Sql
* Correction d’un problème où certaines cmdlets ne reconnaissaient pas l’abonnement Azure actuel

#### <a name="azurermstorage"></a>AzureRM.Storage
* Prise en charge de l’obtention de l’utilisation d’une ressource de stockage d’un emplacement spécifique, et de l’ajout de message d'avertissement où l’obtention de l’utilisation d’une ressource de stockage globale est obsolète.
    - Get-AzureRmStorageUsage

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Nouvelle cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl : obtient l’URL du webhook de déploiement continu de conteneur
* Nouvelles cmdlets New-AzureRMWebAppContainerPSSession et Enter-WebAppContainerPSSession - démarrent une session PowerShell à distance dans une application de conteneur Windows

## <a name="690---september-2018"></a>6.9.0 - septembre 2018
#### <a name="general"></a>Généralités
* AzureRM.SignalR a été ajouté au module Rollup AzureRM

#### <a name="azurermprofile"></a>AzureRM.Profile
* Modifications mineures du code commun de stockage
* Mise à jour des fichiers d’aide pour inclure des types de paramètre complet.
- Modification de -ServicePrincipal en non obligatoire dans l’ensemble de paramètres ServicePrincipalCertificateWithSubscriptionId 

#### <a name="azurestorage"></a>Azure.Storage
* Prise en charge du contexte de stockage avec OAuth. 
    - New-AzureStorageContext

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Ajout de Standard_Microsoft dans la référence SKU de tarification d’un CDN. 

#### <a name="azurermcompute"></a>AzureRM.Compute
* Déplacement des dépendances du coffre de clés et du stockage vers les dépendances communes
* Ajout de la prise en charge de plus de tailles de machine virtuelle aux cmdlets AEM
* Ajout du paramètre PublicIPPrefix à New-AzureRmVmssIpConfig
* Ajout du paramètre ResourceId à la cmdlet Invoke-AzureRmVMRunCommand
* Ajout de la cmdlet Invoke-AzureRmVmssVMRunCommand

#### <a name="azurermdns"></a>AzureRM.Dns
* Prise en charge de l’enregistrement d’alias pendant la création d’enregistrements DNS

#### <a name="azurerminsights"></a>AzureRM.Insights
* Résolution des problèmes #6833 et #7102 (zone Paramètres de diagnostic)
    - Problèmes avec un nom par défaut, par exemple « service », lors de la création et l’obtention/le référencement des paramètres de diagnostic
    - Problèmes créant des paramètres de diagnostic avec des catégories
* Ajout de message de désapprobation pour les paramètres de fragments de temps de métriques
    - Les paramètres Timegrains sont toujours acceptés (il s’agit d’une modification sans rupture,), mais ils sont ignorés dans le serveur principal dans la mesure où seul PT1M est valide

#### <a name="azurermnetwork"></a>AzureRM.Network
* Modifications apportées aux cmdlets LoadBalancer
  - LoadBalancerInboundNatPoolConfig : ajout des paramètres IdleTimeoutInMinutes, EnableFloatingIp et EnableTcpReset
  - LoadBalancerInboundNatRuleConfig : ajout du paramètre EnableTcpReset
  - LoadBalancerRuleConfig : ajout du paramètre EnableTcpReset
  - LoadBalancerProbeConfig : ajout d’une prise en charge de la valeur « Https » pour le paramètre Protocole
* Ajout de nouvelles commandes pour la sous-ressource OutboundRule du nouveau LoadBalancer
  - Add-AzureRmLoadBalancerOutboundRuleConfig
  - Get-AzureRmLoadBalancerOutboundRuleConfig
  - New-AzureRmLoadBalancerOutboundRuleConfig
  - Set-AzureRmLoadBalancerOutboundRuleConfig
  - Remove-AzureRmLoadBalancerOutboundRuleConfig
* Ajout d’une nouvelle propriété HostedWorkloads pour PSNetworkInterface
* Ajouté de nouvelles cmdlets pour la fonctionnalité : Pare-feu Azure via ARM
  - Ajout de Get-AzureRmFirewall
  - Ajout de Set-AzureRmFirewall
  - Ajout de New-AzureRmFirewall
  - Ajout de Remove-AzureRmFirewall
  - Ajout de New-AzureRmFirewallApplicationRuleCollection
  - Ajout de New-AzureRmFirewallApplicationRule
  - Ajout de New-AzureRmFirewallNatRuleCollection
  - Ajout de New-AzureRmFirewallNatRule
  - Ajout de New-AzureRmFirewallNetworkRuleCollection
  - Ajout de New-AzureRmFirewallNetworkRule
* Ajout de la prise en charge du certificat racine approuvé et de la configuration de mise à l’échelle automatique dans Application Gateway
  - Nouvelles cmdlets ajoutées :
      - Add-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayTrustedRootCertificate
      - New-AzureRmApplicationGatewayTrustedRootCertificate
      - Remove-AzureRmApplicationGatewayTrustedRootCertificate
      - Set-AzureRmApplicationGatewayTrustedRootCertificate
      - Get-AzureRmApplicationGatewayAutoscaleConfiguration
      - New-AzureRmApplicationGatewayAutoscaleConfiguration
      - Remove-AzureRmApplicationGatewayAutoscaleConfiguration
      - Set-AzureRmApplicationGatewayAutoscaleConfiguration
  - Cmdlets mises à jour avec le paramètre facultatif -TrustedRootCertificate
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
      - New-AzureRmApplicationGatewayBackendHttpSetting
      - Set-AzureRmApplicationGatewayBackendHttpSetting
  - Cmdlets mises à jour avec le paramètre facultatif -AutoscaleConfiguration
      - New-AzureRmApplicationGateway
      - Set-AzureRmApplicationGateway
* Ajout d’une cmdlet pour le point de terminaison d’interface Get-AzureInterfaceEndpoint
* Ajout de la prise en charge de plusieurs préfixes d’adresse dans un sous-réseau. Cmdlets mises à jour :
  - New-AzureRmVirtualNetworkSubnetConfig
  - Set-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmVirtualNetworkSubnetConfig
  - Get-AzureRmVirtualNetworkSubnetConfig
  - Add-AzureRmApplicationGatewayAuthenticationCertificate
  - Add-AzureRmApplicationGatewayFrontendIPConfig
  - New-AzureRmApplicationGatewayFrontendIPConfig
  - Set-AzureRmApplicationGatewayFrontendIPConfig
  - Add-AzureRmApplicationGatewayIPConfiguration
  - New-AzureRmApplicationGatewayIPConfiguration
  - Set-AzureRmApplicationGatewayIPConfiguration
  - Add-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmNetworkInterfaceIpConfig - Set-AzureRmNetworkInterfaceIpConfig
  - New-AzureRmVirtualNetworkGatewayIpConfig
  - Add-AzureRmVirtualNetworkGatewayIpConfig
  - Set-AzureRmLoadBalancerFrontendIpConfig
  - Add-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmLoadBalancerFrontendIpConfig
  - New-AzureRmNetworkInterface
* Ajout de cmdlets pour la délégation de sous-réseau.
  - New-AzureRmDelegation : crée une nouvelle délégation, celle-ci peut être ajoutée à un sous-réseau
  - Remove-AzureRmDelegation : accepte un sous-réseau et supprime le nom de délégation fourni de ce sous-réseau
  - Add-AzureRmDelegation : accepte un sous-réseau et ajoute le nom de service fourni en tant que délégation à ce sous-réseau
  - Get-AzureRmDelegation
  - Get-AzureRmAvailableServiceDelegations

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Prise en charge de la gestion de disque managé

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Mise à jour de la dépendance Insights.

#### <a name="azurermresources"></a>AzureRM.Resources
* Mise à jour de New-AzureRmResourceGroupDeployment avec le nouveau paramètre RollbackAction
    - Ajout de la prise en charge d’OnErrorDeployment avec le nouveau paramètre.
* Prise en charge des identités managées sur les affectations de stratégies.
* Des paramètres avec des valeurs par défaut ne sont plus requis lors de l’affectation d’une stratégie avec « New-AzureRmPolicyAssignment »
* Ajout de la nouvelle cmdlet Get-AzureRmPolicyAlias pour récupérer les alias de stratégie

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Résolution du problème #7161

#### <a name="azurermsignalr"></a>AzureRM.SignalR
* Mise à jour des noms de référence SKU en Free_F1 et Standard_S1
* Ajout d’un champ de version à l’objet PSSignalRResource et d’une chaîne de connexion à l’objet PSSignalRKeys.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Prise en charge de la stratégie d’immuabilité dans AzureRm.Storage 
    - Remove-AzureRmStorageAccountNetworkRule
    - Get-AzureRmStorageContainer
    - Update-AzureRmStorageContainer
    - New-AzureRmStorageContainer
    - Remove-AzureRmStorageContainer
    - Add-AzureRmStorageContainerLegalHold
    - Remove-AzureRmStorageContainerLegalHold
    - Set-AzureRmStorageContainerImmutabilityPolicy
    - Get-AzureRmStorageContainerImmutabilityPolicy
    - Remove-AzureRmStorageContainerImmutabilityPolicy
    - Lock-AzureRmStorageContainerImmutabilityPolicy

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Ajout de deux nouvelles cmdlets : Get-AzureRmDeletedWebApp et Restore-AzureRmDeletedWebApp
* New-AzureRmAppServicePlan : le commutateur HyperV est ajouté pour créer un plan App Service avec conteneur Windows
* New-AzureRmWebApp/New-AzureRmWebAppSlot/Set-AzureRmWebApp/Set-AzureRmWebAppSlot : les nouveaux paramètres (la chaîne -ContainerRegistryUser -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) ajoutés pour créer et gérer l’application de conteneur Windows

## <a name="681---august-2018"></a>6.8.1 - Août 2018
#### <a name="general"></a>Généralités
* Résolution du problème relatif aux groupes de ressources par défaut non définis.
* Mise à jour des assemblys de runtime courants

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Résolution du problème relatif aux groupes de ressources par défaut non définis.
* Problème résolu https://github.com/Azure/azure-powershell/issues/6603
    - Les cmdlets Import-AzureRmApiManagementApi et *-AzureRmApiManagementCertificate peuvent maintenant gérer les chemins d’accès relatifs
* Problème résolu https://github.com/Azure/azure-powershell/issues/6879
    - CertificateInformation est une propriété définissable permettant à la cmdlet Set-AzureRmApiManagement de fonctionner correctement. Résolu en passant au nuget 4.0.4-preview
* Problème résolu https://github.com/Azure/azure-powershell/issues/6853
    - Recherche par nom sur produit du filtre Odata résolue
* Problème résolu https://github.com/Azure/azure-powershell/issues/6814
    - Recherche par nom sur Api du filtre Odata résolue
* Ajout de la prise en charge de l’enregistreur d'événements AzureMonitor


#### <a name="azurermcompute"></a>AzureRM.Compute
* Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.
* Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé
* Résolution du problème relatif aux groupes de ressources par défaut non définis.
* Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine

#### <a name="azurermnetwork"></a>AzureRM.Network
* Modification de la présentation d’une sortie de cmdlet par défaut en affichage sous forme de table

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause


#### <a name="azurermresources"></a>AzureRM.Resources
* Résolution du problème de création d’applications managées depuis le Marketplace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Problèmes résolus
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Ajout de la prise en charge de la méthode de routage MultiValue
    - Nouveau paramètre « MaxReturn » pour le routage MultiValue
* Ajout de la prise en charge de la méthode de routage Subnet
    - Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison
* Ajout de la prise en charge des en-têtes personnalisés dans les profils
* Ajout de la prise en charge des plages de codes avec l’état Attendu dans les profils
* Ajout de la prise en charge des en-têtes personnalisés dans les points de terminaison

## <a name="680---august-2018"></a>6.8.0 - Août 2018
#### <a name="general"></a>Généralités
* Résolution du problème relatif aux groupes de ressources par défaut non définis.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Ajout d’une propriété d’expiration aux jetons renvoyés lors de la phase Connect-AzureRmAccount.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Résolution du problème signalant que la cible est manquante dans la sortie d’erreur.
* Résolution du problème relatif au type de compte de stockage pour les machines virtuelles dotées d’un disque managé
* Correction des applets de commande AEM Extension pour d’autres environnements, par exemple Azure Chine

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Correction des exemples pour New-AzureRmIotHubExportDevices et New-AzureRmIotHubImportDevices

#### <a name="azurermnetwork"></a>AzureRM.Network
* Modification de la représentation sous forme de modèles par défaut en affichage sous forme de table

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Correction de l’erreur dans Update-AzureRmPowerBIEmbeddedCapacity lors d’une tentative de redimensionnement de la capacité mise en pause

#### <a name="azurermresources"></a>AzureRM.Resources
* Résolution du problème de création d’application managée depuis le Marketplace.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Résolution des problèmes
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Prise en charge de la méthode de routage MultiValue
    - Nouveau paramètre « MaxReturn » pour le routage MultiValue
* Prise en charge de la méthode de routage Subnet
    - Prise en charge des plages d’adresses IP (sous-réseaux) dans les points de terminaison
* Prise en charge des en-têtes personnalisés dans les profils
* Prise en charge des plages de codes avec l’état Attendu dans les profils
* Prise en charge des en-têtes personnalisés dans les points de terminaison

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Résolution du problème relatif aux groupes de ressources par défaut mal définis.

## <a name="670---august-2018"></a>6.7.0 : août 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Mise à jour vers la dernière version d’Azure ClientRuntime.
* Ajout d’un identifiant utilisateur au nom de contexte par défaut afin d’éviter un conflit de contextes.
    - https://github.com/Azure/azure-powershell/issues/6489
* Résolution des problèmes liés à Clear-AzureRmContext avec la sélection d’un contexte 6398.
* Possibilité de transmettre le domaine du locataire au paramètre « -TenantId » pour la cmdlet Connect-AzureRmAccount.
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a>Azure.Storage
* Suppression de la limite de 5 To pour le quota de partage de fichiers Azure.
- Set-AzureStorageShareQuota

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azureanalysisservices"></a>Azure.AnalysisServices
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermbackup"></a>AzureRM.Backup
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermbatch"></a>AzureRM.Batch
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermbilling"></a>AzureRM.Billing
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Mise à jour vers la dernière version d’Azure ClientRuntime.
* Ajout du paramètre EvictionPolicy à la cmdlet New-AzureRmVmssConfig.
* Utilisation de l’emplacement par défaut dans le paramètre DiskFileParameterSet de la cmdlet New-AzureRmVm si aucun emplacement n’est spécifié.
* Correction de la description de paramètre dans la cmdlet Save-AzureRmVMImage.
* Correction de la cmdlet Get-AzureRmVMDiskEncryptionStatus pour certains scénarios liés à un passage unique.

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Correction du débogage lorsque le paramètre DebugPreference est défini à partir de la ligne de commande PowerShell.
* Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAcl.
* Mise à jour vers la dernière version d’Azure ClientRuntime.
* Mise à jour de l’exemple pour la cmdlet Set-AzureRmDataLakeStoreItemAclEntry.

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermdns"></a>AzureRM.Dns
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurerminsights"></a>AzureRM.Insights
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermmarketplaceordering"></a>AzureRM.MarketplaceOrdering
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermmedia"></a>AzureRM.Media
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ajout d’un exemple pour la cmdlet Set-AzureRmLocalNetworkGateway.
* Ajout d’exemples et de descriptions pour les cmdlets Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey et New-AzureRmVirtualNetworkGatewayConnection.
* Ajout d’exemples pour les cmdlets Remove-AzureRmVirtualNetworkGatewayIpConfig et Reset-AzureRmVirtualNetworkGateway.
* Ajout d’un exemple pour la cmdlet Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.
* Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.
* Ajout d’un exemple pour la cmdlet Set-AzureRmVirtualNetworkGatewayConnection.
* Régénération des cmdlets pour ApplicationSecurityGroup, RouteTable et Usage à l’aide du tout dernier générateur de code.
* Clarification du message d’erreur pour la cmdlet Get-AzureRmVirtualNetworkSubnetConfig lors de la tentative d’obtention d’un sous-réseau qui n’existe pas.

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Ajout d’un filtre de stratégie pour la cmdlet Get-AzureRmRecoveryServicesBackItem. La commande retourne la liste des éléments de sauvegarde protégés par l’ID de stratégie donnée.
* Mise à jour de Microsoft.Azure.Management.RecoveryServices.Backup vers la préversion 3.0.0.
* Mise à jour vers la dernière version d’Azure ClientRuntime.
* Ajout du paramètre TargetResourceGroupName à la cmdlet Restore-AzureRmRecoveryServicesBackupItem. Groupe de ressources vers lequel les disques managés sont restaurés. S’applique à la sauvegarde des machines virtuelles avec disques managés.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermresources"></a>AzureRM.Resources
* Prise en charge du déploiement de modèle à l’étendue de l’abonnement. Ajout de nouvelles cmdlets :
    - New-AzureRmDeployment
    - Get-AzureRmDeployment
    - Test-AzureRmDeployment
    - Remove-AzureRmDeployment
    - Stop-AzureRmDeployment
    - Save-AzureRmDeploymentTemplate
    - Get-AzureRmDeploymentOperation
* Résolution du problème entraînant une erreur lors de la transmission d’un contexte à la cmdlet Set-AzureRmResource.
    - https://github.com/Azure/azure-powershell/issues/5705
* Correction de l’exemple indiqué pour la cmdlet New-AzureRmResourceGroupDeployment.
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermsql"></a>AzureRM.Sql
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermstorage"></a>AzureRM.Storage
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermtags"></a>AzureRM.Tags
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Mise à jour vers la dernière version d’Azure ClientRuntime.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Mise à jour vers la dernière version d’Azure ClientRuntime.

## <a name="660---july-2018"></a>6.6.0 - juillet 2018
#### <a name="general"></a>Généralités
* Mise à jour de tous les fichiers d’aide pour inclure les types de paramètre complet et les types d’entrée/sortie corrects.

#### <a name="azurermprofile"></a>AzureRM.Profile
* Mise à jour de la bibliothèque Common.Strategy pour être en mesure de valider que la configuration actuelle pour une ressource est compatible avec la ressource cible.
* Ajout des types ps1xml à Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Ajout de la prise en charge de l’obtention du contexte de stockage à partir de DefaultProfile.
* Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Problème résolu https://github.com/Azure/azure-powershell/issues/6370
    - Correction du bogue dans Automapper pour traduire PsApiManagementApi à ApiContract
* Problème résolu https://github.com/Azure/azure-powershell/issues/6515
    - Correction du bogue dans File.Save pour ne pas surcharger avec le Type d’encodage
* Problème résolu https://github.com/Azure/azure-powershell/issues/6560
    - Mise à jour vers la version 4.0.3 de Nuget qui corrige l’exception du modèle sur apiId

#### <a name="azurermcompute"></a>AzureRM.Compute
* Correction du problème d’échec de création d’une machine virtuelle à l’aide de DiskFileParameterSet dans New-AzureRmVm en raison du changement de nom du type de compte de stockage PremiumLRS.
* Correction de la cmdlet Invoke-AzureRmVMRunCommand
* Mise à jour de Get-AzureRmAvailabilitySet pour activer la liste de tous les groupes à haute disponibilité dans un abonnement.  (La paramètre ResouceGroupName est désormais facultatif.)
* Mise à jour de SimpleParameterSet pour « New-AzureRmVm » pour activer le réseau accéléré sur les machines virtuelles admissibles.
* Mise à jour du jeu de paramètres simple de New-AzureRmVmss qui échoue à créer les groupes de machines virtuelles identiques lorsqu’un équilibreur de charge spécifié par un utilisateur existe déjà.
* Mise à jour de l’exemple pour New-AzureRmDisk
* Ajout d’un exemple pour « New-AzureRmVM »
* Mise à jour de la description pour Set-AzureRmVMOSDisk
* Mise à jour de l’exemple 1 pour Set-AzureRmVMBginfoExtension pour corriger l’orthographe et le préfixe. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Mise à jour de la version du Kit de développement logiciel (SDK) ADF .Net vers la version 1.1.0.
* Prise en charge du runtime d’intégration auto-hébergé en partageant entre les fabriques de données.
     - Ajout d’un nouveau paramètre -SharedIntegrationRuntimeResourceId à la cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Ajout d’un nouveau paramètre facultatif -LinkedDataFactoryName à la cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Mise à jour de la version du Kit de développement logiciel (SDK) DataPlane (Microsoft.Azure.DataLake.Store) vers la version 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression

#### <a name="azurerminsights"></a>AzureRM.Insights
* Correction de mise en forme de OutputType dans les fichiers d’aide
* À l’aide de la préversion 0.19.1 du Kit de développement logiciel Microsoft.Azure.Management.Monitor

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correction des problèmes de redirection dans Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Ajout d’exemples pour les cmdlets LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Correction du problème lorsque vous fournissez le nom de la balise et la valeur pour « Get-AzureRmResource »
    - https://github.com/Azure/azure-powershell/issues/6765
* Correction du scénario de redirection avec « Set-AzureRmResource »

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Mise à jour de la redirection pour InputObject et ResourceId dans les cmdlets de suppression
* quelques problèmes résolus
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Ajout d’un support de serveur de protection avancée contre les menaces avec les cmdlets suivantes :
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Ajout d’un support d’évaluation des vulnérabilités avec les cmdlets suivantes :
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Correction de l’exemple dans Remove-AzureRmSqlServerFirewallRule
* Correction de la manipulation incorrecte de la DateHeure pour les cultures non-américaines dans Get-AzureSqlSyncGroupLog

#### <a name="azurermstorage"></a>AzureRM.Storage
* Ajout de Ps1XmlAttribute aux propriétés de types de sortie des cmdlets
* Affichage de la sortie de la cmdlet StorageAccount dans l’affichage du tableau
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Suppression de l’instruction incorrecte de l’aide de la cmdlet Tag
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - Juillet 2018
#### <a name="azurermprofile"></a>AzureRM.Profile
* Mise à jour de l’aide pour « Get-AzureRmContextAutosaveSetting »

#### <a name="azurestorage"></a>Azure.Storage
* Prise en charge du chargement de l’objet blob ou du fichier avec un jeton SAS en écriture seule
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Ajout de la propriété ResourceGroupName requise au système autonome.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Mise à jour de l’aide et ajout d’un exemple pour « New-AzureRMAutomationSchedule »

#### <a name="azurermcompute"></a>AzureRM.Compute
* Ajout du paramètre de balise à Update/New-AzureRmAvailabilitySet
* Ajout d’un exemple pour « Add-AzureRmVmssExtension »
* Ajout d’exemples pour « Remove-AzureRmVmssExtension »
* Mise à jour de l’aide pour « Set-AzureRmVMAccessExtension »
* Mettez à jour SimpleParameterSet pour New-AzureRmVmss pour définir SinglePlacementGroup sur false par défaut, et ajoutez le paramètre de commutateur « SinglePlacementGroup » qui permet à l’utilisateur de créer le groupe de machines virtuelles identiques dans un seul groupe de placement.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSEventHubDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Mise à jour du message d’erreur pour Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Correction de l’erreur « impossible de résoudre le jeu de paramètres » dans New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Activer l’homologation entre des réseaux virtuels dans plusieurs locataires pour Set/Add-AzureRmVirtualNetworkPeering
* Mise à jour des applets de commande ci-dessous pour Application Gateway
    - New-AzureRmApplicationGateway : ajout de la prise en charge des zones et de l’indicateur EnableFIPS
    - New-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2
    - Set-AzureRmApplicationGatewaySku : ajout des nouvelles références (SKU) Standard_v2 et WAF_v2
* Régénération des applets de commande RouteTable avec la dernière version du Générateur

#### <a name="azurermrelay"></a>AzureRM.Relay
* Mise à jour des fichiers Markdown, correction du problème relatif au nom du paramètre dans l’exemple

#### <a name="azurermresources"></a>AzureRM.Resources
* Mise à jour des applets de commande Roleassignment et Roledefinition :
    - Supprimez les appels Roledefinition supplémentaires dans le cadre de la pagination.
* Correction de l’applet de commande Get-AzureRmRoleAssignment
    - Correction de la fonctionnalité du paramètre de commande -ExpandPrincipalGroups
* Résolution du problème avec « Get-AzureRmResource » où le paramètre « -ResourceType » était sensible à la casse

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Ajout des paramètres Top et Skip à la liste des applets de commande
* Ajout des applets de commande de migration de l’espace de noms Standard vers l’espace de noms Premium :
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* Ajout d’une propriété en lecture seule « PendingReplicationOperationsCount » à la classe PSServiceBusDRConfigurationAttributes, ce qui donne le nombre d’opérations de réplication en attente pendant l’exécution de la réplication

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Mise à jour de l’exemple pour « New-AzureRmServiceFabricCluster »

#### <a name="azurermsql"></a>AzureRM.Sql
* Ajout de nouvelles applets de commande pour Management.Sql pour permettre aux clients d’ajouter le certificat TDE à l’instance SQL Server ou à une instance gérée
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Lorsque `Set-AzureRmWebApp -AssignIdentity` et `Set-AzureRmWebAppSlot -AssignIdentity` sont définis sur false, cela supprime également la propriété d’identité de la balise d’aperçu du site object.Removing.
* Exemples `Get-AzureRmWebAppMetrics` et `Get-AzureRmAppServicePlanMetrics` mis à jour
* `Set-AzureRmWebApp -PhpVersion` prend en charge hors connexion en tant que version PHP valide

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
* Exposer les nouvelles références SKU pour les passerelles de réseau virtuel redondantes interzone
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
