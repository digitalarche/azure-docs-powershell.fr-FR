---
title: Contextes et informations d’identification de connexion Azure
description: Apprenez à réutiliser les informations d’identification Azure (et autres informations) sur plusieurs sessions PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: 72d1b07bb2c66f80ea6f5d37ef7012d0d0a5bbbc
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182449"
---
# <a name="azure-powershell-context-objects"></a>Objets de contexte Azure PowerShell

Azure PowerShell utilise des _objets de contexte Azure PowerShell_ (contextes Azure) pour stocker les informations d’abonnement et d’authentification. Si vous avez plusieurs abonnements, les contextes Azure vous permettent de sélectionner l’abonnement sur lequel exécuter les applets de commande Azure PowerShell. Les contextes Azure sont également utilisés pour stocker des informations de connexion entre plusieurs sessions PowerShell et exécuter des tâches en arrière-plan.

Cet article traite de la gestion des contextes Azure, mais pas de la gestion des abonnements ou des comptes. Si vous envisagez de gérer des utilisateurs, des abonnements, des locataires ou d’autres informations de compte, consultez la documentation [Azure Active Directory](/azure/active-directory). Pour découvrir comment utiliser des contextes pour exécuter des tâches en arrière-plan ou des tâches parallèles, consultez [Utiliser des applets de commande Azure PowerShell dans les travaux PowerShell](using-psjobs.md) après vous être familiarisé avec les contextes Azure.

## <a name="overview-of-azure-context-objects"></a>Vue d’ensemble des objets de contexte Azure

Les contextes Azure sont des objets PowerShell qui représentent votre abonnement actif sur lequel exécuter des commandes, et les informations d’authentification nécessaires pour se connecter à un cloud Azure. Avec les contextes Azure, Azure PowerShell n’a pas besoin de réauthentifier votre compte chaque fois que vous changez d’abonnement. Un contexte Azure est constitué des éléments suivants :

* Le _compte_ qui a été utilisé pour se connecter à Azure avec [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Les contextes Azure traitent les utilisateurs, les ID d’application et les principaux de service de la même façon du point de vue d’un compte.
* L’_abonnement_ actif, un contrat de service avec Microsoft pour créer et exécuter des ressources Azure, qui sont associées à un _locataire_. Les locataires sont souvent appelés _organisations_ dans la documentation ou lors de l’utilisation d’Active Directory.
* Une référence à un _cache de jeton_, un jeton d’authentification stocké pour accéder à un cloud Azure. L’endroit où ce jeton est stocké et sa durée de conservation sont déterminés par les [paramètres d’enregistrement automatique du contexte](#save-azure-contexts-across-powershell-sessions).

Pour plus d’informations sur ces termes, consultez [Terminologie d’Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Les jetons d’authentification utilisés par les contextes Azure sont identiques aux autres jetons stockés qui font partie d’une session persistante. 

Quand vous vous connectez avec `Connect-AzAccount`, au moins un contexte Azure est créé pour votre abonnement par défaut. L’objet retourné par `Connect-AzAccount` est le contexte Azure par défaut utilisé pour le reste de la session PowerShell.

## <a name="get-azure-contexts"></a>Obtenir les contextes Azure

Les contextes Azure disponibles sont récupérés avec l’applet de commande [Get-AzContext](/powershell/module/az.accounts/get-azcontext). Listez tous les contextes disponibles avec `-ListAvailable` :

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Vous pouvez aussi obtenir un contexte en utilisant son nom :

```azurepowershell-interactive
$context = Get-Context -Name "mycontext"
```

Les noms de contexte peuvent être différents du nom de l’abonnement associé.

> [!IMPORTANT]
> Les contextes Azure disponibles __ne sont pas__ toujours vos abonnements disponibles. Les contextes Azure représentent seulement des informations stockées localement. Vous pouvez obtenir vos abonnements avec l’applet de commande [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).

## <a name="create-a-new-azure-context-from-subscription-information"></a>Créer un contexte Azure à partir des informations d’un abonnement

L’applet de commande [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) est utilisée à la fois pour créer des contextes Azure et pour les définir comme contexte actif.
La façon la plus simple de créer un contexte Azure est d’utiliser les informations d’un abonnement existant. L’applet de commande est conçue pour prendre l’objet de sortie de `Get-AzSubscription` comme valeur redirigée et pour configurer un nouveau contexte Azure :

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Vous pouvez aussi donner le nom ou l’ID de l’abonnement, et l’ID du locataire, si nécessaire :

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Si l’argument `-Name` est omis, le nom et l’ID de l’abonnement sont utilisés comme nom du contexte, selon le format `Subscription Name (subscription-id)`.

## <a name="change-the-active-azure-context"></a>Changer le contexte Azure actif

`Set-AzContext` et [Select-AzContext](/powershell/module/az.accounts/set-azcontext) peuvent toutes deux être utilisées pour changer le contexte Azure actif. Comme décrit dans [Créer un contexte Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` crée un contexte Azure pour un abonnement s’il n’en existe pas, puis utilise ce contexte comme contexte actif.

`Select-AzContext` est destinée à être utilisée seulement avec des contextes Azure existants ; elle fonctionne de façon similaire à `Set-AzContext -Context`, mais elle est conçue pour être utilisée avec la redirection :

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Comme de nombreuses autres commandes de gestion de compte et de contexte dans Azure PowerShell, `Set-AzContext` et `Select-AzContext` prennent en charge l’argument `-Scope`, qui vous permet de contrôler le temps pendant lequel le contexte est actif. `-Scope` vous permet de changer le contexte actif d’une seule session sans changer le contexte par défaut :

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Pour éviter de basculer entre les contextes pendant toute une session PowerShell, toutes les commandes Azure PowerShell peuvent être exécutées sur un contexte donné avec l’argument `-AzContext` :

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

L’autre utilisation principale des contextes avec les applets de commande Azure PowerShell est d’exécuter des commandes en arrière-plan. Pour plus d’informations sur l’exécution de travaux PowerShell avec Azure PowerShell, consultez [Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Enregistrer des contextes Azure entre des sessions PowerShell

Par défaut, les contextes Azure sont enregistrés pour une utilisation entre des sessions PowerShell. Vous pouvez changer ce comportement de l’une des façons suivantes :

* Connectez-vous en utilisant `-Scope Process` avec `Connect-AzAccount`.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Le contexte Azure retourné dans le cadre de cette connexion est valide _seulement_ pour la session active et n’est pas enregistré automatiquement, quel que soit le paramètre d’enregistrement automatique du contexte d’Azure PowerShell.
* Désactivez l’enregistrement automatique du contexte d’Azure PowerShell avec l’applet de commande [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).
  La désactivation de l’enregistrement automatique du contexte __n’efface pas__ les jetons stockés. Pour découvrir comment effacer les informations de contexte Azure stockées, consultez [Supprimer les contextes et les informations d’identification Azure](#remove-azure-contexts-and-stored-credentials).
* Vous pouvez activer explicitement l’enregistrement automatique du contexte Azure avec l’applet de commande [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave). Quand l’enregistrement automatique est activé, tous les contextes d’un utilisateur sont stockés localement pour les sessions PowerShell ultérieures.
* Enregistrez manuellement les contextes avec [Save-AzContext](/powershell/module/az.accounts/save-azcontext) pour les utiliser dans des sessions PowerShell futures, où elles peuvent être chargées avec [Import-AzContext](/powershell/module/az.accounts/import-azcontext) :

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> La désactivation de l’enregistrement automatique du contexte __n’efface pas__ les informations de contexte stockées qui ont été enregistrées. Pour supprimer les informations stockées, utilisez l’applet de commande [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Pour plus d’informations sur la suppression des contextes enregistrés, consultez [Supprimer les contextes et les informations d’identification](#remove-azure-contexts-and-stored-credentials).

Chacune de ces commandes prend en charge le paramètre `-Scope`, qui peut prendre la valeur `Process` pour s’appliquer seulement au processus en cours d’exécution. Par exemple, pour faire en sorte que les contextes nouvellement créés ne soient pas enregistrés après que l’utilisateur quitte une session PowerShell :

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Les informations de contexte et les jetons sont stockés dans le répertoire `$env:USERPROFILE\.Azure` sur Windows, et dans `$HOME/.Azure` sur les autres plateformes. Des informations sensibles comme les ID d’abonnement et les ID de locataire peuvent néanmoins toujours être exposées dans des informations stockées, via des journaux ou des contextes enregistrés. Pour découvrir comment effacer les informations stockées, consultez la section [Supprimer les contextes et les informations d’identification Azure](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Supprimer les contextes et les informations d’identification stockées Azure

Pour effacer les contextes et les informations d’identification Azure :

* Déconnectez-vous d’un compte avec [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).
  Vous pouvez vous déconnecter de n’importe quel compte en utilisant le compte ou le contexte :

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  La déconnexion supprime toujours les jetons d’authentification stockés et efface les contextes enregistrés associés à l’utilisateur ou au contexte déconnecté.
* Utilisez [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Cette applet de commande supprime toujours les contextes et les jetons d’authentification stockés, et elle vous déconnecte.
* Supprimez un contexte avec [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) :
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Si vous supprimez le contexte actif, vous êtes déconnecté d’Azure et vous devez vous réauthentifier avec `Connect-AzAccount`.

## <a name="see-also"></a>Voir aussi

* [Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell](using-psjobs.md)
* [Terminologie d’Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Informations de référence sur Az.Accounts](/powershell/module/az.accounts)
