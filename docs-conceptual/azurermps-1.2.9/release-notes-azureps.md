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
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853013"
---
# <a name="release-notes"></a>Notes de publication

Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.

## <a name="version-129"></a>Version 1.2.9

Modifications apportées à cette version

* Module AzureRm.AzureStackAdmin
    + Modifications de l’applet de commande Add-AzureRmResourceProviderRegistration pour la prise en charge de la séparation entre l’administrateur et le locataire Azure Resource Manager. Ajout d’un nouveau paramètre -ResourceManagerType.
    + Suppression des paramètres -AdminUri, -ApiVersion, -SubscriptionId et -Token dans chaque applet de commande. Nous avions publié des avertissements indiquant que ces paramètres allaient être déconseillés, ils sont désormais supprimés.
* Module AzureStackStorage
    + Ajout de nouvelles applets de commande pour prendre en charge les scénarios de migration de conteneur.
    + Suppression des applets de commande faisant référence aux composants internes et aux fonctionnalités sous-jacentes.
* AzureRM.BootStrapper
    + Création d’un module pour gérer les versions des applets de commande Azure PowerShell par le biais de l’utilisation des profils de version