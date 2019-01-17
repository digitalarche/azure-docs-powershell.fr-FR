---
title: Utilisation des modules Azure PowerShell expérimentaux
description: Comprenez l’utilisation et la philosophie des modules Azure PowerShell expérimentaux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ae2fecf73271a34a08ac66de03962a7a529e353b
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342030"
---
# <a name="use-experimental-azure-powershell-modules"></a>Utiliser des modules Azure PowerShell expérimentaux

En mettant l’accent sur les outils de développement dans Azure, l’équipe Azure PowerShell apporte de nombreuses améliorations à l’expérience d’utilisation d’Azure PowerShell. Cet article décrit comment participer à des expériences avec Azure PowerShell et envoyer des commentaires à l’équipe de développement.

## <a name="experimentation-methodology"></a>Méthodologie d’expérimentation

Pour faciliter l’expérimentation, nous créons des modules Azure PowerShell qui implémentent des fonctionnalités déjà existantes de Microsoft Azure SDK avec de nouvelles méthodes, plus simples d’utilisation. Dans la plupart des cas, les cmdlets reflètent exactement les cmdlets existantes. Toutefois, les cmdlets expérimentales fournissent une notation abrégée et des valeurs par défaut plus intelligentes, qui facilitent la création et la gestion des ressources Azure.

Ces modules peuvent être installés côte à côte avec des modules Azure PowerShell existants. Les noms de cmdlet ont été raccourcis, de manière à éviter les conflits de noms avec des cmdlets existantes, non expérimentales.

Les modules expérimentaux utilisent la convention d’affectation de noms suivante : `Az.*.Experiments`. Cette convention d’affectation de noms est similaire à la dénomination des modules de préversion : `Az.*.Preview`. Les modules de préversion diffèrent des modules expérimentaux. Ils implémentent de nouvelles fonctionnalités des services Azure qui sont uniquement disponibles en tant qu’offre de préversion. Les modules de préversion remplacent les modules Azure PowerShell existants et utilisent les mêmes noms de paramètre et de cmdlet.

## <a name="how-to-install-an-experimental-module"></a>Comment installer un module expérimental

Les modules expérimentaux sont publiés dans PowerShell Gallery, comme les modules Azure PowerShell existants. Pour consulter une liste de modules expérimentaux, exécutez la commande suivante :

```azurepowershell-interactive
Find-Module Az.*.Experiments
```

Pour installer un module expérimental, utilisez la cmdlet `Install-Module`.

### <a name="documentation-and-support"></a>Documentation et support

La documentation est incluse dans le package d’installation et est accessible à l’aide de la cmdlet `Get-Help`. Aucune documentation officielle n’est publiée pour les modules expérimentaux.

Nous vous encourageons à tester ces modules. Vos commentaires nous permettent d’améliorer la facilité d’utilisation et de répondre à vos besoins. Toutefois, comme il s’agit d’une fonctionnalité expérimentale, la prise en charge de ces modules est limitée. Vous pouvez poser vos questions ou signaler des problèmes en créant un [problème](https://github.com/Azure/azure-powershell/issues) dans le référentiel GitHub.

## <a name="experiments-and-areas-of-improvement"></a>Expérimentation et domaines à améliorer

Ces améliorations ont été sélectionnées en fonction des principaux atouts des produits concurrents. Par exemple, Azure CLI s’efforce de baser ses commandes sur des _scénarios_ plutôt que sur une _surface d’exposition des API_.
Azure CLI utilise différentes valeurs par défaut intelligentes, qui facilitent la compréhension des scénarios de démarrage par les utilisateurs.

### <a name="core-improvements"></a>Améliorations principales

Les améliorations principales sont considérées comme des optimisations de « bon sens », et l’implémentation de ces mises à jour requiert une expérimentation limitée.

- Cmdlets basées sur des scénarios : - **toutes* les cmdlets doivent être conçues sur la base de scénarios, et non du service REST Azure.

- Noms plus courts : cela inclut les noms des cmdlets et les noms des paramètres.
  Utilisez des alias pour assurer la compatibilité avec les « anciennes » cmdlets. Fournissez des ensembles de paramètres _à compatibilité descendante_.

- Valeurs par défaut intelligentes : créez des valeurs par défaut intelligentes pour indiquer les informations « requises ». Par exemple : 
  - Groupe de ressources
  - Lieu
  - Ressources dépendantes

### <a name="experimental-improvements"></a>Améliorations expérimentales

Les améliorations expérimentales présentent une modification importante que l’équipe souhaite valider à l’aide d’une expérimentation.

- Types simples : les scénarios de création doivent s’éloigner des types et des objets de configuration complexes. Simplifiez la configuration à un ou deux paramètres.

- « Création intelligente » : tous les scénarios de création qui implémentent la fonction de « création intelligente » ne disposent d’_aucun_ paramètre requis ; toutes les informations requises sont choisies par Azure PowerShell de manière répétée.

- Paramètres « gris » : dans de nombreux cas, certains paramètres peuvent être « gris », ou semi-facultatifs. Si le paramètre n’est pas spécifié, l’utilisateur est invité à indiquer s’il souhaite qu’il soit généré pour lui. Il est également judicieux pour les paramètres « gris » de déduire une valeur en fonction du contexte, avec le consentement de l’utilisateur.
  Par exemple, il peut être judicieux de faire en sorte que le paramètre « gris » suggère la valeur utilisée le plus récemment.

- Commutateur `-Auto` : le commutateur `-Auto` doit fournir une option d’abonnement pour permettre aux utilisateurs _de définir tous les éléments sur leur valeur par défaut_ tout en gérant l’intégrité des paramètres requis dans le chemin principal.

### <a name="feature-specific-switches"></a>Commutateurs spécifiques aux fonctionnalités

Par exemple, le scénario de « Création d’application web » peut avoir un commutateur `-Git` ou `-AddRemote` qui ajoutera automatiquement un élément « azure » distant à un référentiel git existant.

- Valeurs par défaut définissables : les utilisateurs doivent être en mesure de définir les valeurs par défaut pour les paramètres communs tels que `-ResourceGroupName` et `-Location`.

- Valeurs par défaut de la taille : les « tailles » des ressources peuvent être difficiles à comprendre pour les utilisateurs, car de nombreux fournisseurs de ressources utilisent des noms différents (par exemple, « Standard\_DS1\_v2 » ou « S1 »). Toutefois, la plupart des utilisateurs se préoccupent surtout des coûts. C’est pourquoi il est judicieux de définir des tailles « universelles » basées sur un programme de tarification. Les utilisateurs peuvent choisir une taille spécifique, ou laisser à Azure PowerShell le soin de choisir le _meilleure option_ en fonction de la ressource et du budget.

- Format de sortie : Azure PowerShell renvoie actuellement des éléments `PSObject` et la sortie de console est limitée. Azure PowerShell peut avoir besoin d’afficher certaines informations à l’utilisateur concernant les « valeurs par défaut intelligentes » utilisées.