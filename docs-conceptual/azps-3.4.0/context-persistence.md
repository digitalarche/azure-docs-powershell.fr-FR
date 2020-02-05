---
title: Contextes et informations d’identification de connexion Azure
description: Apprenez à réutiliser les informations d’identification Azure (et autres informations) sur plusieurs sessions PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.openlocfilehash: f14583e7c24d0355d778607bab52c81ae22598b8
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2020
ms.locfileid: "77003130"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="8c490-103">Objets de contexte Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c490-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="8c490-104">Azure PowerShell utilise des _objets de contexte Azure PowerShell_ (contextes Azure) pour stocker les informations d’abonnement et d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8c490-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="8c490-105">Si vous avez plusieurs abonnements, les contextes Azure vous permettent de sélectionner l’abonnement sur lequel exécuter les applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c490-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="8c490-106">Les contextes Azure sont également utilisés pour stocker des informations de connexion entre plusieurs sessions PowerShell et exécuter des tâches en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8c490-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="8c490-107">Cet article traite de la gestion des contextes Azure, mais pas de la gestion des abonnements ou des comptes.</span><span class="sxs-lookup"><span data-stu-id="8c490-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="8c490-108">Si vous envisagez de gérer des utilisateurs, des abonnements, des locataires ou d’autres informations de compte, consultez la documentation [Azure Active Directory](/azure/active-directory).</span><span class="sxs-lookup"><span data-stu-id="8c490-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="8c490-109">Pour découvrir comment utiliser des contextes pour exécuter des tâches en arrière-plan ou des tâches parallèles, consultez [Utiliser des applets de commande Azure PowerShell dans les travaux PowerShell](using-psjobs.md) après vous être familiarisé avec les contextes Azure.</span><span class="sxs-lookup"><span data-stu-id="8c490-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="8c490-110">Vue d’ensemble des objets de contexte Azure</span><span class="sxs-lookup"><span data-stu-id="8c490-110">Overview of Azure context objects</span></span>

<span data-ttu-id="8c490-111">Les contextes Azure sont des objets PowerShell qui représentent votre abonnement actif sur lequel exécuter des commandes, et les informations d’authentification nécessaires pour se connecter à un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="8c490-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="8c490-112">Avec les contextes Azure, Azure PowerShell n’a pas besoin de réauthentifier votre compte chaque fois que vous changez d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c490-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="8c490-113">Un contexte Azure est constitué des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8c490-113">An Azure context consists of:</span></span>

* <span data-ttu-id="8c490-114">Le _compte_ qui a été utilisé pour se connecter à Azure avec [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="8c490-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="8c490-115">Les contextes Azure traitent les utilisateurs, les ID d’application et les principaux de service de la même façon du point de vue d’un compte.</span><span class="sxs-lookup"><span data-stu-id="8c490-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="8c490-116">L’_abonnement_ actif, un contrat de service avec Microsoft pour créer et exécuter des ressources Azure, qui sont associées à un _locataire_.</span><span class="sxs-lookup"><span data-stu-id="8c490-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="8c490-117">Les locataires sont souvent appelés _organisations_ dans la documentation ou lors de l’utilisation d’Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8c490-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="8c490-118">Une référence à un _cache de jeton_, un jeton d’authentification stocké pour accéder à un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="8c490-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="8c490-119">L’endroit où ce jeton est stocké et sa durée de conservation sont déterminés par les [paramètres d’enregistrement automatique du contexte](#save-azure-contexts-across-powershell-sessions).</span><span class="sxs-lookup"><span data-stu-id="8c490-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="8c490-120">Pour plus d’informations sur ces termes, consultez [Terminologie d’Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="8c490-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="8c490-121">Les jetons d’authentification utilisés par les contextes Azure sont identiques aux autres jetons stockés qui font partie d’une session persistante.</span><span class="sxs-lookup"><span data-stu-id="8c490-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="8c490-122">Quand vous vous connectez avec `Connect-AzAccount`, au moins un contexte Azure est créé pour votre abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c490-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="8c490-123">L’objet retourné par `Connect-AzAccount` est le contexte Azure par défaut utilisé pour le reste de la session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c490-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="8c490-124">Obtenir les contextes Azure</span><span class="sxs-lookup"><span data-stu-id="8c490-124">Get Azure contexts</span></span>

<span data-ttu-id="8c490-125">Les contextes Azure disponibles sont récupérés avec l’applet de commande [Get-AzContext](/powershell/module/az.accounts/get-azcontext).</span><span class="sxs-lookup"><span data-stu-id="8c490-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="8c490-126">Listez tous les contextes disponibles avec `-ListAvailable` :</span><span class="sxs-lookup"><span data-stu-id="8c490-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="8c490-127">Vous pouvez aussi obtenir un contexte en utilisant son nom :</span><span class="sxs-lookup"><span data-stu-id="8c490-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="8c490-128">Les noms de contexte peuvent être différents du nom de l’abonnement associé.</span><span class="sxs-lookup"><span data-stu-id="8c490-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c490-129">Les contextes Azure disponibles __ne sont pas__ toujours vos abonnements disponibles.</span><span class="sxs-lookup"><span data-stu-id="8c490-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="8c490-130">Les contextes Azure représentent seulement des informations stockées localement.</span><span class="sxs-lookup"><span data-stu-id="8c490-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="8c490-131">Vous pouvez obtenir vos abonnements avec l’applet de commande [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).</span><span class="sxs-lookup"><span data-stu-id="8c490-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="8c490-132">Créer un contexte Azure à partir des informations d’un abonnement</span><span class="sxs-lookup"><span data-stu-id="8c490-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="8c490-133">L’applet de commande [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) est utilisée à la fois pour créer des contextes Azure et pour les définir comme contexte actif.</span><span class="sxs-lookup"><span data-stu-id="8c490-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="8c490-134">La façon la plus simple de créer un contexte Azure est d’utiliser les informations d’un abonnement existant.</span><span class="sxs-lookup"><span data-stu-id="8c490-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="8c490-135">L’applet de commande est conçue pour prendre l’objet de sortie de `Get-AzSubscription` comme valeur redirigée et pour configurer un nouveau contexte Azure :</span><span class="sxs-lookup"><span data-stu-id="8c490-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="8c490-136">Vous pouvez aussi donner le nom ou l’ID de l’abonnement, et l’ID du locataire, si nécessaire :</span><span class="sxs-lookup"><span data-stu-id="8c490-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="8c490-137">Si l’argument `-Name` est omis, le nom et l’ID de l’abonnement sont utilisés comme nom du contexte, selon le format `Subscription Name (subscription-id)`.</span><span class="sxs-lookup"><span data-stu-id="8c490-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="8c490-138">Changer le contexte Azure actif</span><span class="sxs-lookup"><span data-stu-id="8c490-138">Change the active Azure context</span></span>

<span data-ttu-id="8c490-139">`Set-AzContext` et [Select-AzContext](/powershell/module/az.accounts/set-azcontext) peuvent toutes deux être utilisées pour changer le contexte Azure actif.</span><span class="sxs-lookup"><span data-stu-id="8c490-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="8c490-140">Comme décrit dans [Créer un contexte Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` crée un contexte Azure pour un abonnement s’il n’en existe pas, puis utilise ce contexte comme contexte actif.</span><span class="sxs-lookup"><span data-stu-id="8c490-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="8c490-141">`Select-AzContext` est destinée à être utilisée seulement avec des contextes Azure existants ; elle fonctionne de façon similaire à `Set-AzContext -Context`, mais elle est conçue pour être utilisée avec la redirection :</span><span class="sxs-lookup"><span data-stu-id="8c490-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="8c490-142">Comme de nombreuses autres commandes de gestion de compte et de contexte dans Azure PowerShell, `Set-AzContext` et `Select-AzContext` prennent en charge l’argument `-Scope`, qui vous permet de contrôler le temps pendant lequel le contexte est actif.</span><span class="sxs-lookup"><span data-stu-id="8c490-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="8c490-143">`-Scope` vous permet de changer le contexte actif d’une seule session sans changer le contexte par défaut :</span><span class="sxs-lookup"><span data-stu-id="8c490-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="8c490-144">Pour éviter de basculer entre les contextes pendant toute une session PowerShell, toutes les commandes Azure PowerShell peuvent être exécutées sur un contexte donné avec l’argument `-AzContext` :</span><span class="sxs-lookup"><span data-stu-id="8c490-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="8c490-145">L’autre utilisation principale des contextes avec les applets de commande Azure PowerShell est d’exécuter des commandes en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8c490-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="8c490-146">Pour plus d’informations sur l’exécution de travaux PowerShell avec Azure PowerShell, consultez [Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="8c490-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="8c490-147">Enregistrer des contextes Azure entre des sessions PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c490-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="8c490-148">Par défaut, les contextes Azure sont enregistrés pour une utilisation entre des sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c490-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="8c490-149">Vous pouvez changer ce comportement de l’une des façons suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c490-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="8c490-150">Connectez-vous en utilisant `-Scope Process` avec `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="8c490-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="8c490-151">Le contexte Azure retourné dans le cadre de cette connexion est valide _seulement_ pour la session active et n’est pas enregistré automatiquement, quel que soit le paramètre d’enregistrement automatique du contexte d’Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c490-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="8c490-152">Désactivez l’enregistrement automatique du contexte d’Azure PowerShell avec l’applet de commande [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="8c490-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="8c490-153">La désactivation de l’enregistrement automatique du contexte __n’efface pas__ les jetons stockés.</span><span class="sxs-lookup"><span data-stu-id="8c490-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="8c490-154">Pour découvrir comment effacer les informations de contexte Azure stockées, consultez [Supprimer les contextes et les informations d’identification Azure](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="8c490-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="8c490-155">Vous pouvez activer explicitement l’enregistrement automatique du contexte Azure avec l’applet de commande [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="8c490-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="8c490-156">Quand l’enregistrement automatique est activé, tous les contextes d’un utilisateur sont stockés localement pour les sessions PowerShell ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c490-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="8c490-157">Enregistrez manuellement les contextes avec [Save-AzContext](/powershell/module/az.accounts/save-azcontext) pour les utiliser dans des sessions PowerShell futures, où elles peuvent être chargées avec [Import-AzContext](/powershell/module/az.accounts/import-azcontext) :</span><span class="sxs-lookup"><span data-stu-id="8c490-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="8c490-158">La désactivation de l’enregistrement automatique du contexte __n’efface pas__ les informations de contexte stockées qui ont été enregistrées.</span><span class="sxs-lookup"><span data-stu-id="8c490-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="8c490-159">Pour supprimer les informations stockées, utilisez l’applet de commande [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="8c490-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="8c490-160">Pour plus d’informations sur la suppression des contextes enregistrés, consultez [Supprimer les contextes et les informations d’identification](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="8c490-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="8c490-161">Chacune de ces commandes prend en charge le paramètre `-Scope`, qui peut prendre la valeur `Process` pour s’appliquer seulement au processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8c490-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="8c490-162">Par exemple, pour faire en sorte que les contextes nouvellement créés ne soient pas enregistrés après que l’utilisateur quitte une session PowerShell :</span><span class="sxs-lookup"><span data-stu-id="8c490-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="8c490-163">Les informations de contexte et les jetons sont stockés dans le répertoire `$env:USERPROFILE\.Azure` sur Windows, et dans `$HOME/.Azure` sur les autres plateformes.</span><span class="sxs-lookup"><span data-stu-id="8c490-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="8c490-164">Des informations sensibles comme les ID d’abonnement et les ID de locataire peuvent néanmoins toujours être exposées dans des informations stockées, via des journaux ou des contextes enregistrés.</span><span class="sxs-lookup"><span data-stu-id="8c490-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="8c490-165">Pour découvrir comment effacer les informations stockées, consultez la section [Supprimer les contextes et les informations d’identification Azure](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="8c490-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="8c490-166">Supprimer les contextes et les informations d’identification stockées Azure</span><span class="sxs-lookup"><span data-stu-id="8c490-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="8c490-167">Pour effacer les contextes et les informations d’identification Azure :</span><span class="sxs-lookup"><span data-stu-id="8c490-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="8c490-168">Déconnectez-vous d’un compte avec [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="8c490-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="8c490-169">Vous pouvez vous déconnecter de n’importe quel compte en utilisant le compte ou le contexte :</span><span class="sxs-lookup"><span data-stu-id="8c490-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="8c490-170">La déconnexion supprime toujours les jetons d’authentification stockés et efface les contextes enregistrés associés à l’utilisateur ou au contexte déconnecté.</span><span class="sxs-lookup"><span data-stu-id="8c490-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="8c490-171">Utilisez [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="8c490-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="8c490-172">Cette applet de commande supprime toujours les contextes et les jetons d’authentification stockés, et elle vous déconnecte.</span><span class="sxs-lookup"><span data-stu-id="8c490-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="8c490-173">Supprimez un contexte avec [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext) :</span><span class="sxs-lookup"><span data-stu-id="8c490-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="8c490-174">Si vous supprimez le contexte actif, vous êtes déconnecté d’Azure et vous devez vous réauthentifier avec `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="8c490-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c490-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c490-175">See also</span></span>

* [<span data-ttu-id="8c490-176">Exécuter des applets de commande Azure PowerShell dans des travaux PowerShell</span><span class="sxs-lookup"><span data-stu-id="8c490-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="8c490-177">Terminologie d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8c490-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="8c490-178">Informations de référence sur Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="8c490-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
