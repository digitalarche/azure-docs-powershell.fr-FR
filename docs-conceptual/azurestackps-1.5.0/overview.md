---
title: Vue d’ensemble d’Azure Stack PowerShell administrateur | Microsoft Docs
description: Une vue d’ensemble d’Azure Stack PowerShell administrateur avec des instructions sur les procédures d’installation et de configuration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153397"
---
# <a name="azure-stack-module-150"></a>Module Azure Stack 1.5.0

## <a name="requirements"></a>Requirements:
La version minimale d’Azure Stack prise en charge est la version 1808.

Remarque : Si vous utilisez une version antérieure, installez la version 1.4.0.

## <a name="known-issues"></a>Problèmes connus :

- La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public. La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.
- Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.

## <a name="install"></a>Installer
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>Notes de publication
* Tous les modules Azure Stack administrateurs sont mis à jour pour une dépendance supérieure ou égale sur le module AzureRm.Profile
* Prise en charge de la gestion des noms de ressource imbriquée dans tous les modules
* Correction de bogue dans tous les modules où l’état de ErrorActionPreference est remplacé par Arrêter
* Module Azs.Compute.Admin
    * De nouvelles propriétés de quota ont été ajoutées pour la prise en charge des disques managés
    * Ajout de cmdlets associées à la migration de disque
    * Propriétés supplémentaires dans les images de plateforme et les objets d’extension de machine virtuelle
* Azs.Fabric.Admin 
    * Nouvelle cmdlet pour l’ajout de nœud d’unité d’échelle
* Azs.Backup.Admin
    * Set-AzsBackupShare est à présent un alias pour la cmdlet Set-AzsBackupConfiguration
    * Get-AzsBackupShare est à présent un alias pour la cmdlet Get-AzsBackupConfiguration
    * Set-AzsBackupConfiguration, le paramètre BackupShare est à présent un alias pour le chemin d’accès de paramètre
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer, le paramètre OfferName est à présent un alias pour Offer
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer, le paramètre OfferName est à présent un alias pour Offer

## <a name="content"></a>Contenu :
### <a name="azure-bridge"></a>Azure Bridge
Préversion du module administrateur AzureBridge d’Azure Stack, qui permet de syndiquer des images à partir d’Azure.

### <a name="backup"></a>Sauvegarde
Préversion du module administrateur Sauvegarde, à l’aide duquel les administrateurs peuvent :
- Configurer l’emplacement de stockage des sauvegardes
- Effectuer des sauvegardes
- Répertorier et restaurer les sauvegardes terminées

### <a name="commerce"></a>Commerce
Préversion du module administrateur Commerce d’Azure Stack, qui permet d’afficher l’utilisation de données agrégées pour l’ensemble du système Azure Stack.

### <a name="compute"></a>Calcul
Préversion du module administrateur de calcul Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme, les disques managés et les extensions de machine virtuelle de calcul.

### <a name="fabric"></a>Structure
Préversion du module administrateur Structure d’Azure Stack, qui permet aux administrateurs d’afficher et de gérer les composants d’infrastructure :
- Démarrage, arrêt et fermeture des nœuds d’unités d’échelle
- Vidage et reprise des nœuds d’unités d’échelle pour les activités liées à des FRU
- Réparation des nœuds d’unités d’échelle
- Redémarrage du rôle d’infrastructure
- Démarrage, arrêt et fermeture des instances de rôle d’infrastructure
- Création de nouveaux pools d’adresses IP


### <a name="gallery"></a>Galerie
Préversion du module administrateur Galerie d’Azure Stack, qui fournit des fonctionnalités pour gérer les éléments de la galerie dans la place de marché Azure Stack.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Préversion du module administrateur Infrastructure Insights, à l’aide duquel les administrateurs peuvent :
- Afficher l’intégrité de leurs ressources de piles Azure Stack
- Afficher et gérer les alertes

### <a name="keyvault"></a>KeyVault
Préversion du module administrateur KeyVault d’Azure Stack, qui permet aux administrateurs d’afficher les quotas de coffres de clés.

### <a name="network"></a>Réseau
Préversion du module administrateur Réseau, à l’aide duquel les administrateurs peuvent :
- Gérer les quotas réseau
- Afficher les ressources réseau allouées, telles que les adresses IP publiques, les réseaux virtuels et les équilibreurs de charge
- Exploiter une cmdlet qui affiche une vue d’ensemble pour l’administration

### <a name="storage"></a>Stockage
Préversion du module administrateur Stockage d’Azure Stack,  qui fournit des fonctionnalités pour :
- Gérer les quotas de stockage
- Nettoyer de la mémoire les ressources de stockage supprimées
- Restaurer les comptes de stockage supprimés
- Migrer des conteneurs d’un partage vers un autre
- Afficher des informations sur les composants de stockage individuels
- Afficher des informations sur l’utilisation et les performances

### <a name="subscription-admin"></a>Administration des abonnements
Préversion du module Administration des abonnements d’Azure Stack.  Ce module fournit aux administrateurs des fonctionnalités pour :
- Gérer les plans et les offres
- Afficher des informations sur l’utilisation et les performances
- Gérer RBAC

### <a name="subscription"></a>Abonnement
Préversion du module Abonnement d’Azure Stack.  Ce module fournit aux utilisateurs des fonctionnalités pour :
- Créer, supprimer et mettre à jour des abonnements

### <a name="update"></a>Mettre à jour
Préversion du module administrateur Mise à jour d’Azure Stack.  À l’aide de ce module, les administrateurs peuvent :
- Répertorier et installer les mises à jour disponibles
- Reprendre les mises à jour interrompues
- Afficher les mises à jour installées
