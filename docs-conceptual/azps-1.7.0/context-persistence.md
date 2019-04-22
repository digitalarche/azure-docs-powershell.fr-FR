---
title: Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell
description: Apprenez à réutiliser les informations d’identification Azure (et autres informations) sur plusieurs sessions PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59363728"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell

Azure PowerShell offre une fonctionnalité appelée **Azure Context Autosave**, qui offre les fonctions suivantes :

- La conservation des informations de connexion en vue d’une réutilisation lors de nouvelles sessions PowerShell.
- Une utilisation plus simple des tâches en arrière-plan pour exécuter des cmdlets à long terme.
- Le basculement entre des comptes, des abonnements et des environnements sans avoir recours à plusieurs connexions.
- L’exécution de tâches à l’aide d’informations d’identification et abonnements différents, en simultané et depuis la même session PowerShell.

## <a name="azure-contexts-defined"></a>Contextes Azure définis

Un *contexte Azure* est un ensemble d’informations qui définit la cible des cmdlets Azure Powershell. Il est constitué de cinq éléments :

- Un *compte* : nom d’utilisateur ou le principal du service utilisé pour authentifier les communications avec Azure
- Un *abonnement* : l’abonnement Azure contenant les ressources sur lesquelles vous agissez.
- Un *client* : le client Azure Active Directory qui contient votre abonnement. Les clients sont plus importants pour l’authentification du principal du service.
- Un *environnement* : le cloud Azure ciblé, en général le cloud Azure global.
  Toutefois, la configuration de l’environnement vous permet aussi de cibler les clouds nationaux, gouvernementaux et locaux (Azure Stack).
- *Informations d’identification* : les informations dont Azure se sert pour vérifier votre identité et pour confirmer votre autorisation d’accès à des ressources dans Azure.

Depuis la dernière version d’Azure PowerShell, les contextes Azure peuvent être automatiquement enregistrés à chaque ouverture d’une nouvelle session PowerShell.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>Sauvegarde automatique du contexte pour la connexion suivante

Azure PowerShell conserve vos informations de contexte automatiquement entre les sessions. Pour configurer PowerShell de sorte qu’il oublie votre contexte et les informations d’identification, utilisez `Disable-AzContextAutoSave`. Si l’enregistrement du contexte est désactivé, vous devez vous connecter à Azure chaque fois que vous ouvrez une session PowerShell.

Pour permettre à Azure PowerShell de se rappeler de votre contexte après la fermeture d’une session, utilisez `Enable-AzContextAutosave`. Le contexte et les informations d’identification sont enregistrés automatiquement dans un dossier spécial caché dans votre répertoire utilisateur (`$env:USERPROFILE\.Azure` sous Windows et `$HOME/.Azure` sous les autres plateformes). Chaque nouvelle session PowerShell cible le contexte utilisé lors de la dernière session.

Les cmdlets qui vous permettent de gérer des contextes Azure vous offrent aussi un contrôle affiné. Si vous souhaitez que les modifications ne s’appliquent qu’à la session PowerShell actuelle (étendue `Process`) ou à chaque session PowerShell (étendue `CurrentUser`). Ces options sont abordées en détail dans [Utilisation des étendues de contexte](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Exécution de cmdlets Azure PowerShell en tant que tâche en arrière-plan

La fonctionnalité **Azure Context Autosave** vous permet aussi de partager votre contexte avec des tâches en arrière-plan PowerShell. PowerShell vous permet de démarrer et de surveiller des tâches dont l’exécution est longue en tant que tâches en arrière-plan, sans avoir à attendre qu’elles ne soient terminées. Vous pouvez partager les informations d’identification avec les tâches en arrière-plan de deux façons :

- En transmettant le contexte en tant qu’argument

  La plupart des cmdlets AzureRM vous permettent de transmettre le contexte en tant que paramètre à la cmdlet. Vous pouvez transmettre un contexte à une tâche en arrière-plan, comme montré dans l’exemple suivant :

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- En utilisant le contexte par défaut avec la sauvegarde automatique activée

  Si vous avez activé la fonctionnalité **Context Autosave**, les tâches en arrière-plan utiliseront automatiquement le contexte par défaut sauvegardé.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

Lorsque vous avez besoin de connaître le résultat de la tâche en arrière-plan, utilisez `Get-Job` pour vérifier son état et `Wait-Job` pour attendre qu’elle soit terminée. Utilisez `Receive-Job` pour capturer ou afficher la sortie de la tâche en arrière-plan. Pour plus d’informations, consultez [à propos des_tâches](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Création, sélection, changement de nom et suppression de contextes

Pour créer un contexte, vous devez être connecté à Azure. La cmdlet `Connect-AzAccount` (ou son alias, `Login-AzAccount`) définit le contexte par défaut utilisé par les cmdlets Azure PowerShell, et vous permet d’accéder à n’importe quel locataire ou abonnement autorisé par vos informations d’identification.

Pour ajouter un nouveau contexte après la connexion, utilisez `Set-AzContext` (ou son alias, `Select-AzSubscription`).

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

L’exemple précédent ajoute un nouveau contexte qui cible « Contoso Subscription 1 » en utilisant vos informations d’identification actuelles. Le nouveau contexte est nommé « Contoso1 ». Si vous ne fournissez aucun nom pour le contexte, un nom par défaut est utilisé, constitué de l’ID du compte et de l’ID de l’abonnement.

Pour renommer un contexte existant, utilisez la cmdlet `Rename-AzContext`. Par exemple : 

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Cet exemple change le nom `[user1@contoso.org; 123456-7890-1234-564321]` automatiquement attribué au contexte par le nom « Contoso2 ». Les cmdlets qui gèrent les contextes utilisent aussi la saisie automatique via la touche Tab, ce qui vous permet de sélectionner rapidement le contexte.

Enfin, pour supprimer un contexte, utilisez la cmdlet `Remove-AzContext`.  Par exemple : 

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

Oublie le contexte nommé « Contoso2 ». Vous pouvez recréer ce contexte à l’aide de `Set-AzContext`.

## <a name="removing-credentials"></a>Suppression des informations d’identification

Vous pouvez supprimer toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service à l’aide de `Disconnect-AzAccount` (aussi appelé `Logout-AzAccount`). Si vous l’exécutez sans paramètres, la cmdlet `Disconnect-AzAccount` supprime toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service dans le contexte actuel. Vous pouvez, si vous le souhaitez, transmettre un nom d’utilisateur, un nom de principal du service ou un contexte pour cibler un principal spécifique.

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Utilisation des étendues de contexte

Vous pouvez de temps en temps sélectionner, modifier ou supprimer un contexte d’une session PowerShell sans impacter d’autres sessions. Pour modifier le comportement par défaut des cmdlets de contexte, utilisez le paramètre `Scope`. L’étendue `Process` remplace le comportement par défaut en l’appliquant uniquement à la session actuelle. À l’inverse, l’étendue `CurrentUser` modifie le contexte dans toutes les sessions, et non uniquement dans la session actuelle.

Par exemple, pour modifier le contexte par défaut de la session PowerShell actuelle sans impacter d’autres fenêtres ni le contexte utilisé lors de la prochaine ouverture de session, utilisez :

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Mémorisation du paramètre de sauvegarde automatique du contexte

Le paramètre de sauvegarde automatique du contexte est enregistré dans le répertoire Azure PowerShell de l’utilisateur (`$env:USERPROFILE\.Azure` sous Windows et `$HOME/.Azure` sous les autres plateformes). Certains types de comptes d’ordinateur peuvent ne pas être capables d’accéder à ce répertoire. Dans ce cas, vous pouvez utiliser la variable d’environnement

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Si la valeur est définie sur « True », le contexte est automatiquement sauvegardé. Si la valeur est définie sur « False », le contexte n’est pas sauvegardé.

## <a name="context-management-cmdlets"></a>Cmdlets de gestion de contexte

- [Enable-AzContextAutosave][enable] : permet la sauvegarde de contexte entre les sessions PowerShell.
  Toutes modifications altèrent le contexte global.
- [Disable-AzContextAutosave][disable] : désactive la sauvegarde automatique du contexte. Vous devez vous connecter à chaque nouvelle session PowerShell.
- [Select-AzContext][select] : sélectionne un contexte par défaut. Toutes les cmdlets utilisent les informations d’identification de ce contexte pour l’authentification.
- [Disconnect-AzAccount][remove-cred] : supprime toutes les informations d’identification et les contextes associés à un compte.
- [Remove-AzContext][remove-context] : supprime un contexte nommé.
- [Rename-AzContext][rename] : renomme un contexte existant.
- [Add-AzAccount][login] : permet d’étendre la portée de la connexion au processus ou à l’utilisateur actuel.
  Permet de renommer le contexte par défaut après authentification.
- [Import-AzContext][import] : permet d’étendre la portée de la connexion au processus ou à l’utilisateur actuel.
- [Set-AzContext][set-context] : permet la sélection de contextes nommés existants, et d’étendre les modifications au processus ou à l’utilisateur actuel.

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
