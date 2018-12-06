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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826645"
---
# <a name="azure-stack-module-140"></a>Module Azure Stack 1.4.0

## <a name="requirements"></a>Requirements:
La version minimale d’Azure Stack prise en charge est la version 1804.

Remarque : si vous utilisez une version antérieure, installez la version 1.2.11.

## <a name="known-issues"></a>Problèmes connus :

- L’option Fermer l’alerte nécessite la version 1803 d’Azure Stack.
- La cmdlet New-AzsOffer ne permet pas de créer une offre avec l’état Public. La cmdlet Set-AzsOffer doit être appelée après pour modifier l’état.
- Un pool d’adresses IP ne peut pas être supprimé sans redéploiement.

## <a name="breaking-changes"></a>Dernières modifications
Il n’existe pas de changement cassant par rapport à la version 1.3.0. Tous les changements cassants liés à la migration à partir de la version 1.2.11 sont décrits ici : https://aka.ms/azspowershellmigration.

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
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a>Notes de publication
    * La version 1.4.0 de Azurestack ne présente aucun changement cassant par rapport à la version 1.3.0 précédente
    * Azs.AzureBridge.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Backup.Admin
        - Ajout de nouveaux paramètres BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays dans la cmdlet Set-AzsBackupShare
        - Ajout d’une cmdlet New-EncyptionKeyBase64 pour faciliter la création de clé de chiffrement
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Commerce.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Fabric.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
        - Ajout d’une cmdlet Add-AzsScaleUnitNode pour permettre à l’administrateur d’ajouter de nouveaux nœuds d’unité d’échelle au tampon azurestack
        - Ajout de cmdlet et de New-AzsScaleUnitNodeObject pour faciliter les objets de paramètre de création d’unité d'échelle
    * Azs.Gallery.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.InfrastructureInsights.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Network.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Update.Admin
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Subscriptions
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés
    * Azs.Subscriptions.Admin
        - Ajout d’une cmdlet Move-AzsSubscription pour déplacer des abonnements entre les offres de fournisseur délégué
        - Ajout d’une cmdlet Test-AzsMoveSubscription pour valider que les abonnements d’utilisateur peuvent être déplacés entre les offres de fournisseur délégué
        - Correction du bogue qui n’a renvoyé qu’une seule page dans les résultats paginés

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
Préversion du module administrateur Calcul d’Azure Stack, qui fournit des fonctionnalités pour gérer les quotas, les images de plateforme et les extensions de machine virtuelle de calcul.

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
