---
title: Guide de migration pour Az 2.0.0
description: Ce guide de migration contient une liste des changements cassants apportés à Azure PowerShell dans la version Az 2.0.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.openlocfilehash: 133769c09f74e1d0d90eff0c6c4bdbb90d1ebe24
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "75721936"
---
# <a name="migration-guide-for-az-200"></a>Guide de migration pour Az 2.0.0

Ce document décrit les modifications apportées entre les versions 1.0.0 et 2.0.0 d’Az. 

## <a name="table-of-contents"></a>Sommaire
- [Changements cassants de module](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Changements cassants de module

### <a name="azcompute"></a>Az.Compute

- Paramètre `Managed` supprimé des applets de commande `New-AzAvailabilitySet` et `Update-AzAvailabilitySet`, au profit de ```Sku = Aligned```

  #### <a name="before"></a>Avant

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- Pour des raisons de cohérence, le paramètre `Image` a été supprimé des jeux de paramètres « ByName » et « ByResourceId » dans `Update-AzImage` 
  
  #### <a name="before"></a>Avant

  Notez que le code ci-dessous est fonctionnel, mais que le paramètre ImageName passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>After

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Restart-AzVM`
  
  #### <a name="before"></a>Avant

  Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Start-AzVM`
  
  #### <a name="before"></a>Avant

  Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Stop-AzVM`
  
  #### <a name="before"></a>Avant

  Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>After

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Remove-AzVM`
  
  #### <a name="before"></a>Avant

  Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>After

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Set-AzVM`
  
  #### <a name="before"></a>Avant

  Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- Pour des raisons de cohérence, le paramètre `Name` a été supprimé des jeux de paramètres « ByObject » et « ByResourceId » dans `Save-AzVMImage` 
  
  #### <a name="before"></a>Avant
  Notez que le code ci-dessous est fonctionnel, mais que le paramètre Name passé n’est pas utilisé : la suppression de ce paramètre n’a donc pas d’impact fonctionnel.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>After
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- La propriété ProtectionPolicy a été ajoutée pour encapsuler la propriété `ProtectFromScaleIn` dans `PSVirtualMachineScaleSetVM`

  #### <a name="before"></a>Avant

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- La propriété ```EncryptionSettingsCollection``` a été ajoutée pour inclure la propriété `EncryptionSettings` dans `PSDisk`

  #### <a name="before"></a>Avant

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- La propriété ```EncryptionSettingsCollection``` a été ajoutée pour inclure la propriété `EncryptionSettings` dans `PSSnapshot`

  #### <a name="before"></a>Avant

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a>After

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- La propriété `VirtualMachineProfile` a été supprimée de `PSVirtualMachineScaleSet`

  #### <a name="before"></a>Avant

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>After

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- L’alias de l’applet de commande `Set-AzVMBootDiagnostic` vers `Set-AzVMBootDiagnostics` a été supprimé

  #### <a name="before"></a>Avant

  Utilisation de l’alias déprécié

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- L’alias de l’applet de commande `Export-AzLogAnalyticThrottledRequest` vers `Export-AzLogAnalyticThrottledRequests` a été supprimé

  #### <a name="before"></a>Avant

  Utilisation de l’alias déprécié

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>After

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- Les applets de commande `Grant-AzHDInsightHttpServicesAccess` et `Revoke-AzHDInsightHttpServicesAccess` ont été supprimées. Elles ne sont plus nécessaires, car l’accès HTTP est toujours activé sur tous les clusters HDInsight.
- L’applet de commande `Set-AzHDInsightGatewayCredential` a été ajoutée. Utilisez cette applet de commande pour changer le nom d’utilisateur et le mot de passe HTTP de la passerelle (elle remplace `Grant-AzHDInsightHttpServicesAccess`).
- L’applet de commande `Get-AzHDInsightJobOutput` a été mise à jour de façon à prendre en charge la précision de l’accès en fonction du rôle à la clé de stockage.
    - Les utilisateurs avec les rôles Opérateur, Contributeur et Propriétaire de cluster HDInsight ne seront pas affectés.
    - Les utilisateurs qui ont seulement le rôle Lecteur doivent spécifier explicitement le paramètre `DefaultStorageAccountKey`.

Pour plus d’informations sur ces modifications de l’accès en fonction du rôle, consultez [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)

  #### <a name="before"></a>Avant

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>After

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Utilisateurs avec seulement le rôle Lecteur pour l’applet de commande Get-AzHDInsightJobOutput

  ####  <a name="before"></a>Avant

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>After

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Les espaces de noms pour les types retournés depuis les applets de commande pour les objets Blob, File d’attente et Fichier ont été changés de `Microsoft.WindowsAzure.Storage` en `Microsoft.Azure.Storage`.  Bien que ceci ne représente pas un changement cassant sur le plan technique du point de vue de la stratégie des changements cassants, il peut nécessiter certaines modifications dans le code qui utilise les méthodes du SDK Stockage .NET pour interagir avec les objets retournés par ces applets de commande.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Exemple 1 :  Ajouter un message à une file d’attente (changement de l’espace de noms de l’objet CloudQueueMessage)

  Avant : 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Après :

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Exemple 2 :  Extraire les attributs d’un objet Blob/Fichier avec AccessCondition (changement de l’espace de noms de l’objet AccessCondition)

  Avant : 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Après :

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Il ne s’agit pas techniquement d’un changement cassant, mais vous constaterez des différences de sortie dans la propriété Sku.Name des comptes de stockage retournés depuis `New/Get/Set-AzStorageAccount`. Les changements sont les suivants. (Après la modification, le SkuName en entrée et en sortie sont alignés.)
  - « StandardLRS » -> « Standard_LRS » ;
  - « StandardGRS » -> « Standard_GRS » ;
  - « StandardRAGRS » -> « Standard_RAGRS » ;
  - « StandardZRS » -> « Standard_ZRS » ;
  - « PremiumLRS » -> « Premium_LRS » ;

- Le comportement par défaut du service quand vous créez un compte de stockage sans spécifier un type (Kind) a changé.  Dans les versions précédentes, quand un compte de stockage était créé sans spécification de `Kind`, le type de compte de stockage `Storage` était utilisé ; dans la nouvelle version, `StorageV2` est la valeur par défaut de `Kind`. Si vous devez créer un compte de stockage V1 avec le type « Stockage », ajoutez le paramètre « -Kind Storage »

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Exemple : Créer un stockage de compte (changement du type par défaut)  

  Avant :

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Après :

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
