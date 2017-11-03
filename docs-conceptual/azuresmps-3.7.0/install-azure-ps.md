---
title: Installer et configurer le module Azure PowerShell Service Management | Microsoft Docs
description: "Comment installer et configurer Azure PowerShell pour la première utilisation."
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 164af369d49e3044e5409c28d8b6145ebc067313
ms.sourcegitcommit: 020066d68d4ab68da162a4ae0cb4e239241f950f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2017
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Installer le module Azure PowerShell Service Management

La méthode recommandée est d’installer Azure PowerShell à partir de [PowerShell Gallery](https://www.powershellgallery.com/).

## <a name="step-1-install-powershellget"></a>Étape 1 : Installer PowerShellGet

Pour installer des éléments à partir de PowerShell Gallery, vous avez besoin du module PowerShellGet. Vérifiez que votre système a la version appropriée de PowerShellGet et qu’il présente toute la configuration requise. Exécutez la commande suivante pour vérifier que PowerShellGet est installé sur votre système.

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

Vous obtenez normalement un résultat similaire à la sortie suivante :

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Si PowerShellGet n’est pas installé, consultez [Comment obtenir PowerShellGet](#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>Étape 2 : Installer Azure PowerShell

Exécutez la commande suivante à partir de la console Windows PowerShell en tant qu’administrateur :

```powershell
Install-Module Azure
```

Le module Azure est un module cumulatif pour les applets de commande Azure Resource Manager. Quand vous installez ce module, les autres modules Azure qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.

Le module Azure Service Management partage des dépendances avec les modules Azure PowerShell Resource Manager. Si vous avez installé ces modules, vous devez ajouter le paramètre `-AllowClobber` à la commande install. Cela garantit la mise à jour des dépendances partagées existantes. Sans ce paramètre, l’installation du module échoue.

```powershell
Install-Module Azure -AllowClobber
```

Après avoir installé ce module, vous pouvez l’importer en exécutant la commande suivante :

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Pour utiliser les applets de commande

Avant de commencer à utiliser les applets de commande Azure Service Management, connectez-vous à votre compte Azure. Pour vous connecter à votre compte, exécutez la commande suivante :

```powershell
Add-AzureAccount
```

Une fois que vous êtes connecté à Azure, Azure PowerShell crée un contexte pour la session. Ce contexte contient l’environnement, le compte, le locataire et l’abonnement Azure PowerShell qui seront utilisés pour toutes les applets de commande dans cette session. Vous êtes maintenant prêt à utiliser les modules ci-dessous.

## <a name="azure-service-management-cmdlets"></a>Applets de commande Azure Service Management

Les modules Azure PowerShell sont fréquemment mis à jour. Si vous remarquez que l’aide en ligne des applets de commande comporte des applets de commande ou des paramètres qui ne sont pas dans votre module, téléchargez et installez la toute dernière version du module. Pour déterminer la version du module que vous utilisez, tapez `(Get-Module Azure).Version`.

Pour obtenir des exemples de scripts qui peuvent vous aider à automatiser certaines tâches courantes dans Azure, consultez le [Centre de scripts Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).

Pour obtenir des informations générales sur l’installation, l’apprentissage, l’utilisation et la personnalisation de Windows PowerShell, consultez [Écriture de scripts avec Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).

### <a name="how-to-get-powershellget"></a>Comment obtenir PowerShellGet

|Version du SE|Instructions d’installation|
|---|---|
|J’ai Windows 10 ou Windows Server 2016|Intégré à Windows Management Framework (WMF) 5.0 inclus dans le système d’exploitation|
|Je veux effectuer la mise à niveau vers PowerShell 5|[Installer la dernière version de WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Mon ordinateur exécute une version de Windows avec PowerShell 3 ou 4|[Obtenir les modules PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Vérification de la version d’Azure PowerShell

Bien que nous vous encouragions à effectuer la mise à niveau vers la version la plus récente dès que possible, plusieurs versions d’Azure PowerShell sont prises en charge. Pour déterminer la version d’Azure PowerShell installée, exécutez `Get-Module AzureRM` à partir de la ligne de commande.

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
