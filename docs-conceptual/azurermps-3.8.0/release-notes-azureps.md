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
ms.date: 05/18/2017
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: b256bf48e15ee98865de0fae50e7b81878b03a54
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2017
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="version-380"></a>Version 3.8.0
* Calcul
  - Correction d’un bogue dans les applets de commande Get-* pour permettre la récupération de plusieurs pages de données (plus de 120 éléments)
* DataLakeAnalytics
  - Correction de l’aide de certaines commandes pour en améliorer la rédaction et les exemples.
* DataLakeStore
  - Ajout de la prise en charge du début et de la fin de l’applet de commande `Get-AzureRMDataLakeStoreItemContent`. Cela permet de retourner les N premières ou les N dernières nouvelles lignes à afficher.
* HDInsight
  - Ajout de la prise en charge du type de cluster RServer
    + La taille de machine virtuelle Edgenode peut être spécifiée pour le cluster RServer dans New-AzureRmHDInsightCluster ou New-AzureRmHDInsightClusterConfig
    + RServer est désormais une option de configuration dans Add-AzureRmHDInsightConfigValues. Cela permet à l’indicateur RStudio d’indiquer que l’installation de R Studio doit être effectuée.
* LogicApp
  - Corrections des applets de commande Set-AzureRmIntegrationAccountSchema et Set-AzureRmIntegrationAccountMap pour le problème lié à contentlink (content et contentlink étaient tous deux définis, ce qui entraînait un échec de la mise à jour).
* Réseau
  - Ajout de la prise en charge de nouvelles fonctionnalités de pare-feu d’applications web pour les passerelles d’application
    + Ajout de New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig
    + Ajout de Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias : List-AzureRmApplicationGatewayAvailableWafRuleSets)
    + Mise à jour de New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration : ajout des paramètres -RuleSetType -RuleSetVersion et -DisabledRuleGroups
    + Mise à jour de Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration : ajout des paramètres -RuleSetType -RuleSetVersion et -DisabledRuleGroups
  - Ajout de la prise en charge des stratégies IPSec pour les connexions de passerelle de réseau virtuel
  - Ajout de New-AzureRmIpsecPolicy
  - Mise à jour de New-AzureRmVirtualNetworkGatewayConnection : ajout des paramètres -IpsecPolicies et -UsePolicyBasedTrafficSelectors
* Profil
  - *Obsolète* : Save-AzureRmProfile est renommé Save-AzureRmContext. Il existe un alias pour l’ancien nom de l’applet de commande, il sera supprimé dans la prochaine version.
  - *Obsolète* : Select-AzureRmProfile est renommé Import-AzureRmContext. Il existe un alias pour l’ancien nom de l’applet de commande, il sera supprimé dans la prochaine version.
  - Les types de sortie PSAzureContext et PSAzureProfile des applets de commande de profil seront changés dans la prochaine version.
  - L’applet de commande Save-AzureRmContext n’aura aucun OutputType dans la prochaine version.
  - Correction d’un bogue dans le code commun d’applet de commande permettant d’utiliser un algorithme FIPS pour les hachages de données : https://github.com/Azure/azure-powershell/issues/3651
* SQL
  - Résolution des bogues sur les applets de commande de groupe de basculement Azure
  - Correction de l’interrogation d’opération
  - Correction de la valeur GracePeriodWithDataLossHour pendant la définition de FailoverPolicy sur Manuel
* TrafficManager
  - Prise en charge de la méthode de routage du trafic Géographique
    + Nouvelle valeur « Géographique » pour le paramètre TrafficRoutingMethod de New-AzureRmTrafficManagerProfile
    + Nouveau paramètre « GeoMapping » pour New-AzureRmTrafficManagerEndpoint et Add-AzureRmTrafficManagerEndpointConfig
    + Correction du piping pour l’applet de commande Get-AzureRmTrafficManagerProfile quand elle retourne une collection de profils
* ServiceManagement
  - Restart-AzureVM : Ajout du paramètre InitiateMaintenance pour effectuer la maintenance pendant le redémarrage de la machine virtuelle.
  - Get-AzureVM : Ajout du champ d’état de la maintenance.
  - Ajout de nouvelles applets de commande pour prendre en charge la mise à niveau du coffre Recovery Services
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
