---
title: Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell
description: Découvrez comment exécuter des applets de commande Azure PowerShell en parallèle ou en tant que tâches en arrière-plan, en utilisant -AsJob et Start-Job.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: d74d3681794398534fe2c75a0c8fc314767ffa85
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002705"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell

Azure PowerShell dépend de la connexion à un cloud Azure et de l’attente des réponses : la plupart de ces applets de commande bloquent donc votre session PowerShell jusqu’à ce qu’elles reçoivent une réponse du cloud.
Les travaux PowerShell vous permettent d’exécuter des applets de commande en arrière-plan ou d’effectuer plusieurs tâches en même temps sur Azure, à partir d’une seule session PowerShell.

Cet article est une brève vue d’ensemble de la façon d’exécuter des applets de commande Azure PowerShell en tant que travaux PowerShell et de vérifier leur achèvement. L’exécution de commandes dans Azure PowerShell nécessite l’utilisation de contextes Azure PowerShell, qui sont abordés en détail dans [Contextes et informations d’identification de connexion Azure](context-persistence.md).
Pour plus d’informations sur les travaux PowerShell, consultez [À propos des travaux PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Contextes Azure avec des travaux PowerShell

Les travaux PowerShell sont exécutés en tant que processus distincts sans session PowerShell attachée : vos informations d’identification Azure doivent donc être partagées avec ces travaux. Les informations d’identification sont passées en tant qu’objets de contexte Azure, selon une des méthodes suivantes :

* Persistance de contexte automatique La persistance de contexte est activée par défaut et elle conserve vos informations de connexion entre plusieurs sessions. Si la persistance du contexte est activée, le contexte Azure actuel est passé au nouveau processus :

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Utilisez le paramètre `-AzContext` avec les applets de commande Azure PowerShell pour fournir un objet de contexte Azure :

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Si la persistance de contexte est désactivée, l’argument `-AzContext` est obligatoire.

* Utilisez le commutateur `-AsJob` fourni par certaines applets de commande Azure PowerShell. Ce commutateur démarre automatiquement l’applet de commande en tant que travail PowerShell, en utilisant le contexte Azure actuellement actif :

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Pour voir si une applet de commande prend en charge `-AsJob`, consultez sa documentation de référence. Le commutateur `-AsJob` ne nécessite pas que l’enregistrement automatique du contexte soit activé.

Vous pouvez vérifier l’état d’un travail en cours d’exécution avec l’applet de commande [Get-Job](/powershell/module/microsoft.powershell.core/get-job). Pour obtenir le résultat d’un travail à un moment donné, utilisez l’applet de commande [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Pour vérifier la progression d’une opération à distance sur Azure, utilisez les applets de commande `Get-` associées au type de ressource modifié par le travail :

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Voir aussi

* [Contextes Azure PowerShell](context-persistence.md)
* [À propos des travaux PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Informations de référence sur Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Informations de référence sur Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
