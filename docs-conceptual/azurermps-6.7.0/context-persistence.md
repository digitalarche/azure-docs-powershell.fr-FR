---
title: Conserver les informations d’identification d’utilisateur sur plusieurs sessions PowerShell
description: Apprenez à réutiliser les informations d’identification Azure (et autres informations) sur plusieurs sessions PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 76e08c462bb34bd2b16a11f70f14c4584b72795a
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43019055"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="f740c-103">Conservation des informations d’identification d’utilisateur sur plusieurs sessions PowerShell</span><span class="sxs-lookup"><span data-stu-id="f740c-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="f740c-104">Azure PowerShell offre une fonctionnalité appelée **Azure Context Autosave**, qui offre les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="f740c-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="f740c-105">La conservation d’informations de connexion pour une réutilisation au cours de nouvelles sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-105">Retention of sign in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="f740c-106">Une utilisation plus simple des tâches en arrière-plan pour exécuter des cmdlets à long terme.</span><span class="sxs-lookup"><span data-stu-id="f740c-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="f740c-107">Le basculement entre comptes, abonnements et environnement sans avoir recours à plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="f740c-107">Switch between accounts, subscriptions, and environments without a separate sign in.</span></span>
- <span data-ttu-id="f740c-108">L’exécution de tâches à l’aide d’informations d’identification et abonnements différents, en simultané et depuis la même session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="f740c-109">Contextes Azure définis</span><span class="sxs-lookup"><span data-stu-id="f740c-109">Azure contexts defined</span></span>

<span data-ttu-id="f740c-110">Un *contexte Azure* est un ensemble d’informations qui définit la cible des cmdlets Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="f740c-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f740c-111">Il est constitué de cinq éléments :</span><span class="sxs-lookup"><span data-stu-id="f740c-111">The context consists of five parts:</span></span>

- <span data-ttu-id="f740c-112">Un *compte* : nom d’utilisateur ou le principal du service utilisé pour authentifier les communications avec Azure</span><span class="sxs-lookup"><span data-stu-id="f740c-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="f740c-113">Un *abonnement* : l’abonnement Azure qui contient les ressources sur lesquelles vous agissez.</span><span class="sxs-lookup"><span data-stu-id="f740c-113">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="f740c-114">Un *client* : le client Azure Active Directory qui contient votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="f740c-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="f740c-115">Les clients sont plus importants pour l’authentification du principal du service.</span><span class="sxs-lookup"><span data-stu-id="f740c-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="f740c-116">Un *environnement* : le cloud Azure ciblé, en général le cloud Azure global.</span><span class="sxs-lookup"><span data-stu-id="f740c-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="f740c-117">Toutefois, la configuration de l’environnement vous permet aussi de cibler les clouds nationaux, gouvernementaux et locaux (Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="f740c-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="f740c-118">Des *informations d’identification* : les informations dont Azure se sert pour vérifier votre identité et assurer votre autorisation d’accès à des ressources dans Azure</span><span class="sxs-lookup"><span data-stu-id="f740c-118">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="f740c-119">Dans les versions précédentes, vous deviez créer un contexte Azure à chaque ouverture d’une nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-119">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="f740c-120">Avec Azure PowerShell v4.4.0, vous pouvez activer la sauvegarde automatique de contextes Azure et leur réutilisation à chaque ouverture d’une nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-120">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a><span data-ttu-id="f740c-121">Sauvegarde automatique d’un contexte pour la future connexion</span><span class="sxs-lookup"><span data-stu-id="f740c-121">Automatically saving the context for the next sign in</span></span>

<span data-ttu-id="f740c-122">Depuis la version 6.3.0, Azure PowerShell conserve vos informations de contexte automatiquement entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="f740c-122">As of version 6.3.0, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="f740c-123">Pour configurer PowerShell de sorte qu’il oublie votre contexte et les informations d’identification, utilisez `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="f740c-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="f740c-124">Vous devez vous connecter à Azure à chaque fois que vous ouvrez une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-124">You will need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="f740c-125">Pour permettre à Azure PowerShell de se rappeler de votre contexte après la fermeture d’une session, utilisez `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="f740c-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="f740c-126">Le contexte et les informations d’identification sont sauvegardés automatiquement dans un dossier spécial caché dans votre répertoire utilisateur (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="f740c-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="f740c-127">Chaque nouvelle session PowerShell cible alors le contexte utilisé lors de la dernière session.</span><span class="sxs-lookup"><span data-stu-id="f740c-127">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="f740c-128">Les cmdlets qui vous permettent de gérer des contextes Azure vous offrent aussi un contrôle affiné.</span><span class="sxs-lookup"><span data-stu-id="f740c-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="f740c-129">Si vous souhaitez que les modifications ne s’appliquent qu’à la session PowerShell actuelle (étendue `Process`) ou à chaque session PowerShell (étendue `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="f740c-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="f740c-130">Ces options sont détaillées dans les détails du mode dans [Utilisation des étendues de contexte](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="f740c-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="f740c-131">Exécution de cmdlets Azure PowerShell en tant que tâche en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="f740c-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="f740c-132">La fonctionnalité **Azure Context Autosave** vous permet aussi de partager votre contexte avec des tâches en arrière-plan PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="f740c-133">PowerShell vous permet de démarrer et de surveiller des tâches dont l’exécution est longue en tant que tâches en arrière-plan, sans avoir à attendre qu’elles ne soient terminées.</span><span class="sxs-lookup"><span data-stu-id="f740c-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="f740c-134">Vous pouvez partager les informations d’identification avec les tâches en arrière-plan de deux façons :</span><span class="sxs-lookup"><span data-stu-id="f740c-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="f740c-135">En transmettant le contexte en tant qu’argument</span><span class="sxs-lookup"><span data-stu-id="f740c-135">Passing the context as an argument</span></span>

  <span data-ttu-id="f740c-136">La plupart des cmdlets AzureRM vous permettent de transmettre le contexte en tant que paramètre à la cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f740c-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="f740c-137">Vous pouvez transmettre un contexte à une tâche en arrière-plan, comme montré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="f740c-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="f740c-138">En utilisant le contexte par défaut avec la sauvegarde automatique activée</span><span class="sxs-lookup"><span data-stu-id="f740c-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="f740c-139">Si vous avez activé la fonctionnalité **Context Autosave**, les tâches en arrière-plan utiliseront automatiquement le contexte par défaut sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="f740c-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="f740c-140">Lorsque vous avez besoin de connaître le résultat de la tâche en arrière-plan, utilisez `Get-Job` pour vérifier son état et `Wait-Job` pour attendre qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="f740c-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="f740c-141">Utilisez `Receive-Job` pour capturer ou afficher la sortie de la tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f740c-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="f740c-142">Pour plus d’informations, consultez [à propos des_tâches](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="f740c-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="f740c-143">Création, sélection, changement de nom et suppression de contextes</span><span class="sxs-lookup"><span data-stu-id="f740c-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="f740c-144">Pour créer un contexte, vous devez être connecté à Azure.</span><span class="sxs-lookup"><span data-stu-id="f740c-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="f740c-145">La cmdlet `Connect-AzureRmAccount` (ou son alias, `Login-AzureRmAccount`) définit le contexte par défaut utilisé par les cmdlets Azure PowerShell suivantes, et vous permet d’accéder à n’importe quel client ou abonnement autorisé par vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="f740c-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="f740c-146">Pour ajouter un nouveau contexte après la connexion,utilisez `Set-AzureRmContext` (ou son alias, `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="f740c-146">To add a new context after sign in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="f740c-147">L’exemple précédent ajoute un nouveau contexte qui cible « Contoso Subscription 1 » en utilisant vos informations d’identification actuelles.</span><span class="sxs-lookup"><span data-stu-id="f740c-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="f740c-148">Le nouveau contexte est nommé « Contoso1 ».</span><span class="sxs-lookup"><span data-stu-id="f740c-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="f740c-149">Si vous ne fournissez aucun nom au contexte, un nom par défaut sera utilisé, constitué de l’ID du compte et de l’ID de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="f740c-149">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="f740c-150">Pour renommer un contexte existant, utilisez la cmdlet `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="f740c-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="f740c-151">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="f740c-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="f740c-152">Cet exemple change le nom `[user1@contoso.org; 123456-7890-1234-564321]` automatiquement attribué au contexte par le nom « Contoso2 ».</span><span class="sxs-lookup"><span data-stu-id="f740c-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="f740c-153">Les cmdlets qui gèrent les contextes utilisent aussi la saisie automatique via la touche Tab, ce qui vous permet de sélectionner rapidement le contexte.</span><span class="sxs-lookup"><span data-stu-id="f740c-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="f740c-154">Enfin, pour supprimer un contexte, utilisez la cmdlet `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="f740c-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="f740c-155">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="f740c-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="f740c-156">Oublie le contexte nommé « Contoso2 ».</span><span class="sxs-lookup"><span data-stu-id="f740c-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="f740c-157">Vous pouvez recréer ce contexte par la suite à l’aide de `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="f740c-157">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="f740c-158">Suppression des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="f740c-158">Removing credentials</span></span>

<span data-ttu-id="f740c-159">Vous pouvez supprimer toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service à l’aide de `Disconnect-AzureRmAccount` (aussi appelé `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="f740c-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="f740c-160">Si vous l’exécutez sans paramètres, la cmdlet `Disconnect-AzureRmAccount` supprime toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="f740c-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="f740c-161">Vous pouvez, si vous le souhaitez, transmettre un nom d’utilisateur, un nom de principal du service ou un contexte pour cibler un principal spécifique.</span><span class="sxs-lookup"><span data-stu-id="f740c-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="f740c-162">Utilisation des étendues de contexte</span><span class="sxs-lookup"><span data-stu-id="f740c-162">Using context scopes</span></span>

<span data-ttu-id="f740c-163">Vous pouvez de temps en temps sélectionner, modifier ou supprimer un contexte d’une session PowerShell sans impacter d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="f740c-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="f740c-164">Pour modifier le comportement par défaut des cmdlets de contexte, utilisez le paramètre `Scope`.</span><span class="sxs-lookup"><span data-stu-id="f740c-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="f740c-165">L’étendue `Process` remplace le comportement par défaut en l’appliquant uniquement à la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="f740c-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="f740c-166">À l’inverse, l’étendue `CurrentUser` modifie le contexte dans toutes les sessions, et non uniquement dans la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="f740c-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="f740c-167">Par exemple, pour modifier le contexte par défaut de la session PowerShell actuelle sans impacter d’autres fenêtres ni le contexte utilisé lors de la prochaine ouverture de session, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f740c-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="f740c-168">Mémorisation du paramètre de sauvegarde automatique du contexte</span><span class="sxs-lookup"><span data-stu-id="f740c-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="f740c-169">Le paramètre de sauvegarde automatique du contexte est sauvegardé dans le répertoire Azure PowerShell de l’utilisateur (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="f740c-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="f740c-170">Certains types de comptes d’ordinateur peuvent ne pas être capables d’accéder à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="f740c-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="f740c-171">Dans ce cas, vous pouvez utiliser la variable d’environnement</span><span class="sxs-lookup"><span data-stu-id="f740c-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="f740c-172">Si la valeur est «True», alors le contexte est sauvegardé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f740c-172">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="f740c-173">Si la valeur est «False», alors le contexte n’est pas sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="f740c-173">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="f740c-174">Modifications apportées au module AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f740c-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="f740c-175">Nouvelles cmdlets pour la gestion de contexte</span><span class="sxs-lookup"><span data-stu-id="f740c-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="f740c-176">[Enable-AzureRmContextAutosave][enable] : permet la sauvegarde de contexte entre les sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="f740c-177">Toutes modifications altèrent le contexte global.</span><span class="sxs-lookup"><span data-stu-id="f740c-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="f740c-178">[Disable-AzureRmContextAutosave][disable] : désactive la sauvegarde automatique du contexte.</span><span class="sxs-lookup"><span data-stu-id="f740c-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="f740c-179">Vous devez vous connecter à chaque nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f740c-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="f740c-180">[Select-AzureRmContext][select] : sélectionne un contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="f740c-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="f740c-181">Toutes les cmdlets suivantes utilisent les informations d’identification de ce contexte pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="f740c-181">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="f740c-182">[Disconnect-AzureRmAccount][remove-cred] : supprime toutes les informations d’identification et les contextes associés à un compte.</span><span class="sxs-lookup"><span data-stu-id="f740c-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="f740c-183">[Remove-AzureRmContext][remove-context] : supprime un contexte nommé.</span><span class="sxs-lookup"><span data-stu-id="f740c-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="f740c-184">[Remove-AzureRmContext][rename] : renomme un contexte existant.</span><span class="sxs-lookup"><span data-stu-id="f740c-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="f740c-185">Modifications apportées à des cmdlets de profil existantes</span><span class="sxs-lookup"><span data-stu-id="f740c-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="f740c-186">[Add-AzureRmAccount][login] : permet d’étendre la connexion au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f740c-186">[Add-AzureRmAccount][login] - Allow scoping of the sign in to the process or the current user.</span></span>
  <span data-ttu-id="f740c-187">Permet de renommer le contexte par défaut après authentification.</span><span class="sxs-lookup"><span data-stu-id="f740c-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="f740c-188">[Import-AzureRmContext][import] : permet d’étendre la connexion au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f740c-188">[Import-AzureRmContext][import] - Allow scoping of the sign in to the process or the current user.</span></span>
- <span data-ttu-id="f740c-189">[Set-AzureRmContext][set-context] : permet la sélection de contextes nommés existants, et d’étendre les modifications au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="f740c-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
