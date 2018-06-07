---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819709"
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