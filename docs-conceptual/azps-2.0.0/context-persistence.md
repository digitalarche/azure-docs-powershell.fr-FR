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
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048561"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="42140-103">Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell</span><span class="sxs-lookup"><span data-stu-id="42140-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="42140-104">Azure PowerShell offre une fonctionnalité appelée **Azure Context Autosave**, qui offre les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="42140-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="42140-105">La conservation des informations de connexion en vue d’une réutilisation lors de nouvelles sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="42140-106">Une utilisation plus simple des tâches en arrière-plan pour exécuter des cmdlets à long terme.</span><span class="sxs-lookup"><span data-stu-id="42140-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="42140-107">Le basculement entre des comptes, des abonnements et des environnements sans avoir recours à plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="42140-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="42140-108">L’exécution de tâches à l’aide d’informations d’identification et abonnements différents, en simultané et depuis la même session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="42140-109">Contextes Azure définis</span><span class="sxs-lookup"><span data-stu-id="42140-109">Azure contexts defined</span></span>

<span data-ttu-id="42140-110">Un *contexte Azure* est un ensemble d’informations qui définit la cible des cmdlets Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="42140-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="42140-111">Il est constitué de cinq éléments :</span><span class="sxs-lookup"><span data-stu-id="42140-111">The context consists of five parts:</span></span>

- <span data-ttu-id="42140-112">Un *compte* : nom d’utilisateur ou le principal du service utilisé pour authentifier les communications avec Azure</span><span class="sxs-lookup"><span data-stu-id="42140-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="42140-113">Un *abonnement* : l’abonnement Azure contenant les ressources sur lesquelles vous agissez.</span><span class="sxs-lookup"><span data-stu-id="42140-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="42140-114">Un *client* : le client Azure Active Directory qui contient votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="42140-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="42140-115">Les clients sont plus importants pour l’authentification du principal du service.</span><span class="sxs-lookup"><span data-stu-id="42140-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="42140-116">Un *environnement* : le cloud Azure ciblé, en général le cloud Azure global.</span><span class="sxs-lookup"><span data-stu-id="42140-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="42140-117">Toutefois, la configuration de l’environnement vous permet aussi de cibler les clouds nationaux, gouvernementaux et locaux (Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="42140-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="42140-118">*Informations d’identification* : les informations dont Azure se sert pour vérifier votre identité et pour confirmer votre autorisation d’accès à des ressources dans Azure.</span><span class="sxs-lookup"><span data-stu-id="42140-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="42140-119">Depuis la dernière version d’Azure PowerShell, les contextes Azure peuvent être automatiquement enregistrés à chaque ouverture d’une nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="42140-120">Sauvegarde automatique du contexte pour la connexion suivante</span><span class="sxs-lookup"><span data-stu-id="42140-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="42140-121">Azure PowerShell conserve vos informations de contexte automatiquement entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="42140-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="42140-122">Pour configurer PowerShell de sorte qu’il oublie votre contexte et les informations d’identification, utilisez `Disable-AzContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="42140-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="42140-123">Si l’enregistrement du contexte est désactivé, vous devez vous connecter à Azure chaque fois que vous ouvrez une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="42140-124">Pour permettre à Azure PowerShell de se rappeler de votre contexte après la fermeture d’une session, utilisez `Enable-AzContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="42140-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="42140-125">Le contexte et les informations d’identification sont enregistrés automatiquement dans un dossier spécial caché dans votre répertoire utilisateur (`$env:USERPROFILE\.Azure` sous Windows et `$HOME/.Azure` sous les autres plateformes).</span><span class="sxs-lookup"><span data-stu-id="42140-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="42140-126">Chaque nouvelle session PowerShell cible le contexte utilisé lors de la dernière session.</span><span class="sxs-lookup"><span data-stu-id="42140-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="42140-127">Les cmdlets qui vous permettent de gérer des contextes Azure vous offrent aussi un contrôle affiné.</span><span class="sxs-lookup"><span data-stu-id="42140-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="42140-128">Si vous souhaitez que les modifications ne s’appliquent qu’à la session PowerShell actuelle (étendue `Process`) ou à chaque session PowerShell (étendue `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="42140-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="42140-129">Ces options sont abordées en détail dans [Utilisation des étendues de contexte](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="42140-129">These options are discussed in more detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="42140-130">Exécution de cmdlets Azure PowerShell en tant que tâche en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="42140-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="42140-131">La fonctionnalité **Azure Context Autosave** vous permet aussi de partager votre contexte avec des tâches en arrière-plan PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="42140-132">PowerShell vous permet de démarrer et de surveiller des tâches dont l’exécution est longue en tant que tâches en arrière-plan, sans avoir à attendre qu’elles ne soient terminées.</span><span class="sxs-lookup"><span data-stu-id="42140-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="42140-133">Vous pouvez partager les informations d’identification avec les tâches en arrière-plan de deux façons :</span><span class="sxs-lookup"><span data-stu-id="42140-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="42140-134">En transmettant le contexte en tant qu’argument</span><span class="sxs-lookup"><span data-stu-id="42140-134">Passing the context as an argument</span></span>

  <span data-ttu-id="42140-135">La plupart des cmdlets AzureRM vous permettent de transmettre le contexte en tant que paramètre à la cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42140-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="42140-136">Vous pouvez transmettre un contexte à une tâche en arrière-plan, comme montré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="42140-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="42140-137">En utilisant le contexte par défaut avec la sauvegarde automatique activée</span><span class="sxs-lookup"><span data-stu-id="42140-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="42140-138">Si vous avez activé la fonctionnalité **Context Autosave**, les tâches en arrière-plan utiliseront automatiquement le contexte par défaut sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="42140-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="42140-139">Lorsque vous avez besoin de connaître le résultat de la tâche en arrière-plan, utilisez `Get-Job` pour vérifier son état et `Wait-Job` pour attendre qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="42140-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="42140-140">Utilisez `Receive-Job` pour capturer ou afficher la sortie de la tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="42140-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="42140-141">Pour plus d’informations, consultez [à propos des_tâches](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="42140-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="42140-142">Création, sélection, changement de nom et suppression de contextes</span><span class="sxs-lookup"><span data-stu-id="42140-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="42140-143">Pour créer un contexte, vous devez être connecté à Azure.</span><span class="sxs-lookup"><span data-stu-id="42140-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="42140-144">La cmdlet `Connect-AzAccount` (ou son alias, `Login-AzAccount`) définit le contexte par défaut utilisé par les cmdlets Azure PowerShell, et vous permet d’accéder à n’importe quel locataire ou abonnement autorisé par vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="42140-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="42140-145">Pour ajouter un nouveau contexte après la connexion, utilisez `Set-AzContext` (ou son alias, `Select-AzSubscription`).</span><span class="sxs-lookup"><span data-stu-id="42140-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="42140-146">L’exemple précédent ajoute un nouveau contexte qui cible « Contoso Subscription 1 » en utilisant vos informations d’identification actuelles.</span><span class="sxs-lookup"><span data-stu-id="42140-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="42140-147">Le nouveau contexte est nommé « Contoso1 ».</span><span class="sxs-lookup"><span data-stu-id="42140-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="42140-148">Si vous ne fournissez aucun nom pour le contexte, un nom par défaut est utilisé, constitué de l’ID du compte et de l’ID de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="42140-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="42140-149">Pour renommer un contexte existant, utilisez la cmdlet `Rename-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="42140-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="42140-150">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="42140-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="42140-151">Cet exemple change le nom `[user1@contoso.org; 123456-7890-1234-564321]` automatiquement attribué au contexte par le nom « Contoso2 ».</span><span class="sxs-lookup"><span data-stu-id="42140-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="42140-152">Les cmdlets qui gèrent les contextes utilisent aussi la saisie automatique via la touche Tab, ce qui vous permet de sélectionner rapidement le contexte.</span><span class="sxs-lookup"><span data-stu-id="42140-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="42140-153">Enfin, pour supprimer un contexte, utilisez la cmdlet `Remove-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="42140-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="42140-154">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="42140-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="42140-155">Oublie le contexte nommé « Contoso2 ».</span><span class="sxs-lookup"><span data-stu-id="42140-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="42140-156">Vous pouvez recréer ce contexte à l’aide de `Set-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="42140-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="42140-157">Suppression des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="42140-157">Removing credentials</span></span>

<span data-ttu-id="42140-158">Vous pouvez supprimer toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service à l’aide de `Disconnect-AzAccount` (aussi appelé `Logout-AzAccount`).</span><span class="sxs-lookup"><span data-stu-id="42140-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="42140-159">Si vous l’exécutez sans paramètres, la cmdlet `Disconnect-AzAccount` supprime toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="42140-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="42140-160">Vous pouvez, si vous le souhaitez, transmettre un nom d’utilisateur, un nom de principal du service ou un contexte pour cibler un principal spécifique.</span><span class="sxs-lookup"><span data-stu-id="42140-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="42140-161">Utilisation des étendues de contexte</span><span class="sxs-lookup"><span data-stu-id="42140-161">Using context scopes</span></span>

<span data-ttu-id="42140-162">Vous pouvez de temps en temps sélectionner, modifier ou supprimer un contexte d’une session PowerShell sans impacter d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="42140-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="42140-163">Pour modifier le comportement par défaut des cmdlets de contexte, utilisez le paramètre `Scope`.</span><span class="sxs-lookup"><span data-stu-id="42140-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="42140-164">L’étendue `Process` remplace le comportement par défaut en l’appliquant uniquement à la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="42140-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="42140-165">À l’inverse, l’étendue `CurrentUser` modifie le contexte dans toutes les sessions, et non uniquement dans la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="42140-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="42140-166">Par exemple, pour modifier le contexte par défaut de la session PowerShell actuelle sans impacter d’autres fenêtres ni le contexte utilisé lors de la prochaine ouverture de session, utilisez :</span><span class="sxs-lookup"><span data-stu-id="42140-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="42140-167">Mémorisation du paramètre de sauvegarde automatique du contexte</span><span class="sxs-lookup"><span data-stu-id="42140-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="42140-168">Le paramètre de sauvegarde automatique du contexte est enregistré dans le répertoire Azure PowerShell de l’utilisateur (`$env:USERPROFILE\.Azure` sous Windows et `$HOME/.Azure` sous les autres plateformes).</span><span class="sxs-lookup"><span data-stu-id="42140-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="42140-169">Certains types de comptes d’ordinateur peuvent ne pas être capables d’accéder à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="42140-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="42140-170">Dans ce cas, vous pouvez utiliser la variable d’environnement</span><span class="sxs-lookup"><span data-stu-id="42140-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="42140-171">Si la valeur est définie sur « True », le contexte est automatiquement sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="42140-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="42140-172">Si la valeur est définie sur « False », le contexte n’est pas sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="42140-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="42140-173">Cmdlets de gestion de contexte</span><span class="sxs-lookup"><span data-stu-id="42140-173">Context management cmdlets</span></span>

- <span data-ttu-id="42140-174">[Enable-AzContextAutosave][enable] : permet la sauvegarde de contexte entre les sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="42140-175">Toutes modifications altèrent le contexte global.</span><span class="sxs-lookup"><span data-stu-id="42140-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="42140-176">[Disable-AzContextAutosave][disable] : désactive la sauvegarde automatique du contexte.</span><span class="sxs-lookup"><span data-stu-id="42140-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="42140-177">Vous devez vous connecter à chaque nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42140-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="42140-178">[Select-AzContext][select] : sélectionne un contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="42140-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="42140-179">Toutes les cmdlets utilisent les informations d’identification de ce contexte pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="42140-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="42140-180">[Disconnect-AzAccount][remove-cred] : supprime toutes les informations d’identification et les contextes associés à un compte.</span><span class="sxs-lookup"><span data-stu-id="42140-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="42140-181">[Remove-AzContext][remove-context] : supprime un contexte nommé.</span><span class="sxs-lookup"><span data-stu-id="42140-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="42140-182">[Rename-AzContext][rename] : renomme un contexte existant.</span><span class="sxs-lookup"><span data-stu-id="42140-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="42140-183">[Add-AzAccount][login] : permet d’étendre la portée de la connexion au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="42140-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="42140-184">Permet de renommer le contexte par défaut après authentification.</span><span class="sxs-lookup"><span data-stu-id="42140-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="42140-185">[Import-AzContext][import] : permet d’étendre la portée de la connexion au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="42140-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="42140-186">[Set-AzContext][set-context] : permet la sélection de contextes nommés existants, et d’étendre les modifications au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="42140-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

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
