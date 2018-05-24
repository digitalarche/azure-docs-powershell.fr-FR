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
ms.date: 05/18/2017
ms.openlocfilehash: 6fe226a2525142f82b894318b0588681bff0e2ef
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="version-220"></a>Version 2.2.0
* Calcul
  - Ajout de la prise en charge de l’interrogation de l’état de chiffrement par l’extension AzureDiskEncryptionForLinux
* DataFactory
  - Ajout d’une nouvelle applet de commande pour répertorier les fenêtres d’activité
    + Get-AzureRmDataFactoryActivityWindow
* DataLake
  - Changement du paramètre `Host` en `DatabaseHost` et ajout d’un alias à `Host`
    + New-AzureRmDataLakeAnalyticsCatalogSecret
    + Set-AzureRmDataLakeAnalyticsCatalogSecret
  - Ajout de la prise en charge de la suppression de la liste de contrôle d’accès et de la liste de contrôle d’accès par défaut
  - Ajout de la prise en charge de l’obtention et de la définition d’autorisations sans nom sur des fichiers et des dossiers
* KeyVault
  - Ajout de la prise en charge des certificats
    + Add-AzureKeyVaultCertificate
    + Add-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificate
    + Get-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificateIssuer
    + Get-AzureKeyVaultCertificateOperation
    + Get-AzureKeyVaultCertificatePolicy
    + Import-AzureKeyVaultCertificate
    + New-AzureKeyVaultCertificateAdministratorDetails
    + New-AzureKeyVaultCertificateOrganizationDetails
    + New-AzureKeyVaultCertificatePolicy
    + Remove-AzureKeyVaultCertificate
    + Remove-AzureKeyVaultCertificateContact
    + Remove-AzureKeyVaultCertificateIssuer
    + Remove-AzureKeyVaultCertificateOperation
    + Set-AzureKeyVaultCertificateAttribute
    + Set-AzureKeyVaultCertificateIssuer
    + Set-AzureKeyVaultCertificatePolicy
    + Stop-AzureKeyVaultCertificateOperation
* Réseau

  - Ajout d’un nouveau paramètre de commutateur pour l’interface réseau afin d’activer/de désactiver la mise en réseau accélérée +New-AzureRmNetworkInterface -EnableAcceleratedNetworking
  - Activation des applets de commande PowerShell de la fonctionnalité Active-Active gateway
    + Add-AzureRmVirtualNetworkGatewayIpConfig
    + Remove-AzureRmVirtualNetworkGatewayIpConfig
  - Ajout d’une nouvelle applet de commande
    + Test-AzureRmPrivateIpAddressAvailability
* Ressources
  - Prise en charge des zones dans les applets de commande de fournisseur et de ressource
    + Get-AzureRmProvider
    + New-AzureRmResource
    + Set-AzureRmResource
* SQL
  - Ajout de nouvelles applets de commande pour la gestion des stratégies de détection des menaces Azure SQL au niveau serveur
    + Get-AzureRmSqlServerThreatDetectionPolicy
    + Remove-AzureRmSqlServerThreatDetectionPolicy
    + Set-AzureRmSqlServerThreatDetectionPolicy
  - Ajout de nouvelles applets de commande pour prendre en charge l’activation/la désactivation de GeoBackupPolicy pour les entrepôts de données Azure SQL
    + Get-AzureRmSqlDatabaseGeoBackupPolicy
    + Set-AzureRmSqlDatabaseGeoBackupPolicy
  - Ajout de nouvelles applets de commande pour les conseillers Azure SQL et les API d’actions recommandées
    + Get-AzureRmSqlDatabaseAdvisor
    + Get-AzureRmSqlElasticPoolAdvisor
    + Get-AzureRmSqlServerAdvisor
    + Get-AzureRmSqlDatabaseRecommendedActions
    + Get-AzureRmSqlElasticPoolRecommendedActions
    + Get-AzureRmSqlServerRecommendedActions
    + Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus
    + Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus
    + Set-AzureRmSqlServerAdvisorAutoExecuteStatus
    + Set-AzureRmSqlDatabaseRecommendedActionState
    + Set-AzureRmSqlElasticPoolRecommendedActionState
    + Set-AzureRmSqlServerRecommendedActionState
