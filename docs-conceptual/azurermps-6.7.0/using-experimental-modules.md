---
title: Utilisation des modules Azure PowerShell expérimentaux
description: Comprenez l’utilisation et la philosophie des modules Azure PowerShell expérimentaux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: ac571363d79c83b268b5c25f65b14f16d4b86e71
ms.sourcegitcommit: 7df99dc139e93a8a4e6d5b1a27968857588d75dd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/16/2018
ms.locfileid: "40106486"
---
# <a name="using-experimental-azure-powershell-modules"></a>Utilisation des modules Azure PowerShell expérimentaux

En mettant l’accent sur les outils de développement (surtout les CLI) dans Azure, l’équipe Azure PowerShell peut apporter de nombreuses améliorations de l’expérience d’utilisation d’Azure PowerShell.

## <a name="experimentation-methodology"></a>Méthodologie d’expérimentation

Pour faciliter l’expérimentation, nous créons des modules Azure PowerShell qui implémentent les fonctionnalités existantes de Microsoft Azure SDK grâce à de nouvelles méthodes, plus simples. Dans la plupart des cas, les cmdlets reflètent exactement les cmdlets existantes. Toutefois, les cmdlets expérimentales fournissent une notation abrégée et des valeurs par défaut plus intelligentes, qui facilitent la création et la gestion des ressources Azure.

Ces modules peuvent être installés en parallèle avec des modules Azure PowerShell existants. Les noms de cmdlet ont été raccourcis, de manière à éviter les conflits de noms avec des cmdlets existantes, non expérimentales.

Les modules expérimentaux utilisent la convention d’affectation de noms suivante : `AzureRM.*.Experiments`. Cette convention d’affectation de noms est similaire à la dénomination des modules de préversion : `AzureRM.*.Preview`. Les modules de préversion diffèrent des modules expérimentaux. Ils implémentent de nouvelles fonctionnalités des services Azure qui sont uniquement disponibles en tant qu’offre de préversion. Les modules de préversion remplacent les modules Azure PowerShell existants et utilisent les mêmes noms de paramètre et de cmdlet.

## <a name="how-to-install-an-experimental-module"></a>Comment installer un module expérimental

Les modules expérimentaux sont publiés dans PowerShell Gallery, comme les modules Azure PowerShell existants. Pour consulter une liste de modules expérimentaux, exécutez la commande suivante :

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

Pour installer le module expérimental, utilisez les commandes suivantes à partir d’une session PowerShell avec élévation de privilèges :

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>Documentation et support

La documentation est incluse dans le package d’installation et est accessible à l’aide de la cmdlet `Get-Help`. Aucune documentation officielle n’est publiée pour les modules expérimentaux.

Nous vous encourageons à tester ces modules. Vos commentaires nous permettent d’améliorer la facilité d’utilisation et de répondre à vos besoins. Toutefois, comme il s’agit d’une fonctionnalité expérimentale, la prise en charge de ces modules est limitée. Vous pouvez poser vos questions ou signaler des problèmes en créant un [problème](https://github.com/Azure/azure-powershell/issues) dans le référentiel GitHub.

## <a name="experiments-and-areas-of-improvement"></a>Expérimentation et domaines à améliorer

Ces améliorations ont été sélectionnées en fonction des principaux atouts des produits concurrents. Par exemple, Azure CLI 2.0 s’efforce de baser ses commandes sur des _scénarios_ plutôt que sur _une surface d’exposition des API_.
Azure CLI 2.0 utilise différentes valeurs par défaut intelligentes, qui facilitent la compréhension des scénarios de démarrage par les utilisateurs.

### <a name="core-improvements"></a>Améliorations principales

Les améliorations principales sont considérées comme des optimisations de « bon sens », et l’implémentation de ces mises à jour requiert une expérimentation limitée.

- Cmdlets basées sur des scénarios : - **toutes* les cmdlets doivent être conçues sur la base de scénarios, et non du service REST Azure.

- Noms plus courts : cela inclut les noms des cmdlets (par exemple, `New-AzureRmVM` => `New-AzVm`) et les noms des paramètres (par exemple, `-ResourceGroupName` => `-Rg`). Utilisez des alias pour assurer la compatibilité avec les « anciennes » cmdlets. Fournissez des ensembles de paramètres _à compatibilité descendante_.

- Valeurs par défaut intelligentes : créez des valeurs par défaut intelligentes pour indiquer les informations « requises ». Par exemple : 
  - Groupe de ressources
  - Lieu
  - Ressources dépendantes

### <a name="experimental-improvements"></a>Améliorations expérimentales

Les améliorations expérimentales présentent une modification importante que l’équipe souhaite valider à l’aide d’une expérimentation.

- Types simples : les scénarios de création doivent s’éloigner des types et des objets de configuration complexes. Simplifiez la configuration à un ou deux paramètres.

- « Création intelligente » : tous les scénarios de création qui implémentent la fonction de « création intelligente » ne disposent d’_aucun_ paramètre requis ; toutes les informations requises sont choisies par Azure PowerShell de manière répétée.

- Paramètres « gris » : dans de nombreux cas, certains paramètres peuvent être « gris », ou semi-facultatifs. Si le paramètre n’est pas spécifié, l’utilisateur est invité à indiquer s’il veut qu’il soit généré pour lui. Il est également judicieux pour les paramètres « gris » de déduire une valeur en fonction du contexte, avec le consentement de l’utilisateur.
  Par exemple, il peut être judicieux de faire en sorte que le paramètre « gris » suggère la valeur utilisée le plus récemment.

- Commutateur `-Auto` : le commutateur `-Auto` doit fournir une option d’abonnement pour permettre aux utilisateurs _de définir tous les éléments sur leur valeur par défaut_ tout en gérant l’intégrité des paramètres requis dans le chemin principal.

### <a name="feature-specific-switches"></a>Commutateurs spécifiques aux fonctionnalités

Par exemple, le scénario de « Création d’application web » peut avoir un commutateur `-Git` ou `-AddRemote` qui ajoutera automatiquement un élément « azure » distant à un référentiel git existant.

- Valeurs par défaut définissables : les utilisateurs doivent être à même de définir certains paramètres omniprésents sur la valeur par défaut, tels que `-ResourceGroupName` et `-Location`.

- Valeurs par défaut de la taille : les « tailles » des ressources peuvent être difficiles à comprendre pour les utilisateurs, car de nombreux fournisseurs de ressources utilisent des noms différents (par exemple, « Standard\_DS1\_v2 » ou « S1 »). Toutefois, la plupart des utilisateurs se préoccupent surtout des coûts. Pour cette raison, il est judicieux de définir des tailles « universelles » selon un calendrier de tarification. Les utilisateurs peuvent choisir une taille spécifique, ou laisser à Azure PowerShell le soin de choisir le _meilleure option_ en fonction de la ressource et du budget.

- Format de sortie : actuellement, Azure PowerShell renvoie des éléments `PSObject` et la sortie de console est limitée. Azure PowerShell peut avoir besoin d’afficher certaines informations à l’utilisateur concernant les « valeurs par défaut intelligentes » utilisées.
