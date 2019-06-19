---
title: Gérer les abonnements Azure avec Azure PowerShell
description: Gérer les abonnements Azure avec Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: 0356a4694f77eda40eec8c3759b9bb7f28979eb6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2019
ms.locfileid: "67193139"
---
# <a name="use-multiple-azure-subscriptions"></a>Utilisez plusieurs abonnements Azure

La plupart des utilisateurs Azure ne possèdent qu’un seul abonnement. Toutefois, si vous faites partie de plus d’une organisation, ou si votre organisation a divisé l’accès à certaines ressources dans les regroupements, vous pouvez avoir plusieurs abonnements dans Azure. L’interface CLI prend en charge la sélection d’un abonnement à la fois au niveau global et par commande.

Pour plus d’informations sur les abonnements, la facturation et la gestion des coûts, consultez la [documentation sur la facturation et la gestion des coûts](/azure/billing/).

## <a name="tenants-users-and-subscriptions"></a>Locataires, utilisateurs et abonnements

La différence entre les locataires, les utilisateurs et les abonnements dans Azure peut prêter à confusion. Un _locataire_ correspond à l’entité d’Azure Active Directory qui inclut une organisation complète. Ce locataire possède au moins un _abonnement_ et _utilisateur_. Un utilisateur est un individu qui n’est associé qu’à un seul locataire, c’est-à-dire à l’organisation auquel il appartient. Les utilisateurs correspondent aux comptes qui se connectent à Azure afin de configurer, de gérer et d’utiliser des ressources.
Un utilisateur peut avoir accès à plusieurs _abonnements_, qui sont les contrats avec Microsoft pour utiliser les services de cloud, y compris Azure. Chaque ressource est associée à un abonnement.

Pour en savoir plus sur les différences entre les locataires, les utilisateurs et les abonnements, consultez le [Dictionnaire de terminologie cloud Azure](/azure/azure-glossary-cloud-terminology).  Pour savoir comment ajouter un nouvel abonnement à votre locataire Azure Active Directory, consultez [Comment ajouter un abonnement Azure à Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Pour savoir comment se connecter à un client en particulier, consultez la rubrique [Se connecter avec Azure PowerShell](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Modifier l’abonnement actif

Dans Azure PowerShell, l’accès des ressources pour un abonnement requiert une modification de l’abonnement associé à votre session Azure.
Pour cela, vous devez modifier le contexte de la session active et les informations concernant les clients, les abonnements et les utilisateurs sur lesquelles sont exécutées les applets de commande.
Pour modifier des abonnements, un objet de contexte Azure PowerShell doit tout d’abord être récupéré avec [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) et ensuite le contexte actuel doit être modifié avec [Set-AzContext](/powershell/module/az.accounts/set-azcontext).

L’exemple suivant montre comment obtenir un abonnement dans le client actuellement actif et définissez-le comme session active :

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Pour en savoir plus sur les contextes Azure PowerShell, notamment comment les enregistrer et basculer rapidement entre eux pour travailler avec plusieurs abonnements facilement, consultez la section [Persistance des informations d’identification avec les contextes Azure PowerShell](context-persistence.md).
