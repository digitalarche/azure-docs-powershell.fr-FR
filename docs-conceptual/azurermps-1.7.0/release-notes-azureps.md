---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 9a40eae86b60afb5e04dd6a6074b60e82731578f
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854628"
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="version-170"></a>Version 1.7.0

* **Modification du comportement des paramètres -Force, –Confirm et $ConfirmPreference pour toutes les applets de commande. Nous modifions cette implémentation conformément aux directives PowerShell. Pour la plupart des applets de commande, cela implique de supprimer le paramètre Force et d’ignorer l’invite ShouldProcess, les utilisateurs doivent inclure le paramètre : « -Confirm:$false » dans leurs scripts PowerShell.** Ces changements corrigent les problèmes suivants :
  - Implémentation correcte de la fonctionnalité –WhatIf, qui permet à un utilisateur de déterminer les effets d’une applet de commande ou d’un script sans apporter de modification réelle
  - Contrôle des invites à l’aide du paramètre $ConfirmPreference à l’échelle de la session. De cette façon, l’utilisateur est invité à confirmer l’action en fonction de l’impact d’une modification potentielle (comme indiqué dans le paramètre ConfirmImpact de l’applet de commande)
  - Contrôle des invites de confirmation propres à une applet de commande à l’aide du paramètre –Confirm
  - Utilisation cohérente de ShouldContinue et du paramètre –Force dans les applets de commande, uniquement pour les actions nécessitant la confirmation de l’utilisateur en raison de la nature particulière des modifications (par exemple, la suppression de fichiers cachés)
  - Cohérence avec les autres applets de commande PowerShell, pour que la connaissance des scripts PowerShell soit immédiatement applicable aux applets de commande Azure PowerShell.

**Notez que dorénavant pour *ignorer automatiquement toutes les invites dans toutes les circonstances*, les applets de commande Azure PowerShell nécessitent que l’utilisateur fournisse deux paramètres :**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Calcul Azure
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Paramètre -Redeploy pour Restart-AzureVM
  - Paramètre -Validate pour Move-AzureService, Move-AzureStorageAccount et Move-AzureVirtualNetwork
  - Les paramètres de nom et de version pour les applets de commande d’extension sont facultatifs comme auparavant.
  - New-AzureVM peut obtenir le type de licence d’un objet de machine virtuelle.
* Stockage Azure
  - Changement du paramètre Tags en Tag et ajout de l’alias de paramètre Tags
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Réseau Azure
  - Ajout d’une nouvelle applet de commande pour l’appairage de réseaux virtuels
* Cache Redis Azure
  - Ajout d’une nouvelle applet de commande pour Reset-AzureRmRedisCache
  - Ajout d’une nouvelle applet de commande pour Export-AzureRmRedisCache
  - Ajout d’une nouvelle applet de commande pour Import-AzureRmRedisCache
  - Modification de l’applet de commande New-AzureRmRedisCache pour inclure le changement de paramètre de réseau virtuel
* Sauvegarde/restauration d’Azure SQL Database
  - Applets de commande pour la fonctionnalité de sauvegarde avec rétention à long terme
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase prend désormais en charge la limite de restauration dans le temps d’une base de données supprimée
  - Restore-AzureRmSqlDatabase prend désormais en charge la restauration à partir d’une sauvegarde avec rétention à long terme
* Azure LogicApp
  - Ajout des applets de commande des comptes d’intégration LogicApp.
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - Amélioration drastique des performances de téléchargement et de chargement de fichiers et de dossiers.
  - Cela inclut une légère modification des noms de paramètre pour le téléchargement ainsi que l’inclusion de deux nouveaux paramètres pour le chargement :
    + NumThreads -> PerFileThreadCount, utilisé pour indiquer le nombre de threads à utiliser dans un seul fichier
    + ConcurrentFileCount, utilisé pour indiquer le nombre de fichiers à charger/télécharger en parallèle pour le chargement/téléchargement de dossiers.
  - Les valeurs de thread par défaut sont maintenant conçues afin d’apporter un meilleur débit général pour la plupart des tailles de fichier. Si les performances ne correspondent pas à ce que vous attendez, les valeurs ci-dessus peuvent être modifiées pour répondre aux exigences.
* Service Analytique Azure Data Lake
  - L’applet de commande Get-AzureRMDataLakeAnalyticsDataSource retourne à présent toutes les sources de données quand elle est appelée sans argument.
  - Cette modification supprime également le paramètre de type de source de données de l’applet de commande.
  - Elle entraîne le retour d’un nouvel objet pour l’opération de liste avec les propriétés suivantes :
    + Type (type de source de données)
    + Nom (nom de la source de données)
    + IsDefault, défini sur true s’il s’agit de la source de données par défaut pour le compte
  - Correction de Get-AzureRMDataLakeAnalyticsJob pour la liste de certaines valeurs de décalage de date et d’heure pendant le filtrage sur submittedBefore et submittedAfter.
* Web Apps
  - Ajout de l’applet de commande Swap-AzureRmWebAppSlot pour l’échange normal et l’échange avec aperçu
  - Extension de l’applet de commande Set-AzureRmWebAppSlot pour prendre en charge l’échange automatique
* Gestion des API Azure
  - Correction des applets de commande de déploiement de gestion des API Azure pour AzureChinaCloud.
  - Suppression de l’applet de commande Set-AzureRmApiManagementTenantGitAccess, car l’accès Git est activé par défaut.
* Sauvegarde Azure Recovery Services
  - Ajout de la prise en charge de la charge de travail Azure SQL
  - Ajout de la prise en charge de la sauvegarde et de la restauration de machines virtuelles Azure chiffrées
  - Backup-AzureRmRecoveryServicesBackupItem - Ajout de la fonctionnalité facultative de durée de rétention pour les points de récupération
  - Résolution de bogues mineurs liés aux filtres dans les applets de commande Get-AzureRmRecoveryServicesBackupContainer et Get-AzureRmRecoveryServicesBackupItem
* Azure Automation
  - Ajout de Get-AzureRmAutomationHybridWorkerGroup
