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
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
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