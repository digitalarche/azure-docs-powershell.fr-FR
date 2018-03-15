---
title: "Connexions d’utilisateur persistant d’une session à l’autre PowerShell"
description: "Cet article détaille les nouvelles fonctionnalités d’Azure PowerShell qui vous permettent de réutiliser vos informations d’identification et d’autres informations utilisateur d’une session à l’autre PowerShell."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 8ef20796b64b16c78a653e293a57d5e752d89710
ms.sourcegitcommit: 20af779cd523c758d40e23d60eb989a4ef982d5c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="1a20e-103">Connexions d’utilisateur persistant d’une session à l’autre PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a20e-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="1a20e-104">Dans la version d’Azure PowerShell sortie en septembre 2017, les cmdlets d’Azure Resource Manager présentent une nouvelle fonctionnalité, **Azure Context Autosave**.</span><span class="sxs-lookup"><span data-stu-id="1a20e-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="1a20e-105">Elle permet plusieurs nouveaux scénarios utilisateur, comme par exemple :</span><span class="sxs-lookup"><span data-stu-id="1a20e-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="1a20e-106">La conservation d’informations de connexion pour une réutilisation au cours de nouvelles sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="1a20e-107">Une utilisation plus simple des tâches en arrière-plan pour exécuter des cmdlets à long terme.</span><span class="sxs-lookup"><span data-stu-id="1a20e-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="1a20e-108">Le basculement entre comptes, abonnements et environnement sans avoir recours à plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="1a20e-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="1a20e-109">L’exécution de tâches à l’aide d’informations d’identification et abonnements différents, en simultané et depuis la même session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="1a20e-110">Contextes Azure définis</span><span class="sxs-lookup"><span data-stu-id="1a20e-110">Azure contexts defined</span></span>

<span data-ttu-id="1a20e-111">Un *contexte Azure* est un ensemble d’informations qui définit la cible des cmdlets Azure Powershell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1a20e-112">Il est constitué de cinq éléments :</span><span class="sxs-lookup"><span data-stu-id="1a20e-112">The context consists of five parts:</span></span>

- <span data-ttu-id="1a20e-113">Un *compte* : nom d’utilisateur ou le principal du service utilisé pour authentifier les communications avec Azure</span><span class="sxs-lookup"><span data-stu-id="1a20e-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="1a20e-114">Un *abonnement* : l’abonnement Azure qui contient les ressources sur lesquelles vous agissez.</span><span class="sxs-lookup"><span data-stu-id="1a20e-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="1a20e-115">Un *client* : le client Azure Active Directory qui contient votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a20e-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="1a20e-116">Les clients sont plus importants pour l’authentification du principal du service.</span><span class="sxs-lookup"><span data-stu-id="1a20e-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="1a20e-117">Un *environnement* : le cloud Azure ciblé, en général le cloud Azure global.</span><span class="sxs-lookup"><span data-stu-id="1a20e-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="1a20e-118">Toutefois, la configuration de l’environnement vous permet aussi de cibler les clouds nationaux, gouvernementaux et locaux (Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="1a20e-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="1a20e-119">Des *informations d’identification* : les informations dont Azure se sert pour vérifier votre identité et assurer votre autorisation d’accès à des ressources dans Azure</span><span class="sxs-lookup"><span data-stu-id="1a20e-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="1a20e-120">Dans les versions précédentes, vous deviez créer un contexte Azure à chaque ouverture d’une nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="1a20e-121">Avec Azure PowerShell v4.4.0, vous pouvez activer la sauvegarde automatique de contextes Azure et leur réutilisation à chaque ouverture d’une nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="1a20e-122">Sauvegarde automatique d’un contexte pour la future connexion</span><span class="sxs-lookup"><span data-stu-id="1a20e-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="1a20e-123">Par défaut, Azure PowerShell oublie les informations de votre contexte à chaque fermeture d’une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="1a20e-124">Pour permettre à Azure PowerShell de se rappeler de votre contexte après la fermeture d’une session, utilisez `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="1a20e-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="1a20e-125">Le contexte et les informations d’identification sont sauvegardés automatiquement dans un dossier spécial caché dans votre répertoire utilisateur (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="1a20e-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="1a20e-126">Chaque nouvelle session PowerShell cible alors le contexte utilisé lors de la dernière session.</span><span class="sxs-lookup"><span data-stu-id="1a20e-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="1a20e-127">Pour configurer PowerShell de sorte qu’il oublie votre contexte et les informations d’identification, utilisez `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="1a20e-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="1a20e-128">Vous devez vous connecter à Azure à chaque fois que vous ouvrez une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="1a20e-129">Les cmdlets qui vous permettent de gérer des contextes Azure vous offrent aussi un contrôle affiné.</span><span class="sxs-lookup"><span data-stu-id="1a20e-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="1a20e-130">Si vous souhaitez que les modifications ne s’appliquent qu’à la session PowerShell actuelle (étendue `Process`) ou à chaque session PowerShell (étendue `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="1a20e-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="1a20e-131">Ces options sont détaillées dans les détails du mode dans [Utilisation des étendues de contexte](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="1a20e-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="1a20e-132">Exécution de cmdlets Azure PowerShell en tant que tâche en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="1a20e-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="1a20e-133">La fonctionnalité **Azure Context Autosave** vous permet aussi de partager votre contexte avec des tâches en arrière-plan PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="1a20e-134">PowerShell vous permet de démarrer et de surveiller des tâches dont l’exécution est longue en tant que tâches en arrière-plan, sans avoir à attendre qu’elles ne soient terminées.</span><span class="sxs-lookup"><span data-stu-id="1a20e-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="1a20e-135">Vous pouvez partager les informations d’identification avec les tâches en arrière-plan de deux façons :</span><span class="sxs-lookup"><span data-stu-id="1a20e-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="1a20e-136">En transmettant le contexte en tant qu’argument</span><span class="sxs-lookup"><span data-stu-id="1a20e-136">Passing the context as an argument</span></span>

  <span data-ttu-id="1a20e-137">La plupart des cmdlets AzureRM vous permettent de transmettre le contexte en tant que paramètre à la cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a20e-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="1a20e-138">Vous pouvez transmettre un contexte à une tâche en arrière-plan, comme montré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="1a20e-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="1a20e-139">En utilisant le contexte par défaut avec la sauvegarde automatique activée</span><span class="sxs-lookup"><span data-stu-id="1a20e-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="1a20e-140">Si vous avez activé la fonctionnalité **Context Autosave**, les tâches en arrière-plan utiliseront automatiquement le contexte par défaut sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="1a20e-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="1a20e-141">Lorsque vous avez besoin de connaître le résultat de la tâche en arrière-plan, utilisez `Get-Job` pour vérifier son état et `Wait-Job` pour attendre qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="1a20e-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="1a20e-142">Utilisez `Receive-Job` pour capturer ou afficher la sortie de la tâche en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="1a20e-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="1a20e-143">Pour plus d’informations, consultez [à propos des_tâches](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="1a20e-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="1a20e-144">Création, sélection, changement de nom et suppression de contextes</span><span class="sxs-lookup"><span data-stu-id="1a20e-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="1a20e-145">Pour créer un contexte, vous devez être connecté à Azure.</span><span class="sxs-lookup"><span data-stu-id="1a20e-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="1a20e-146">La cmdlet `Add-AzureRmAccount` (ou son alias, `Login-AzureRmAccount`) définit le contexte par défaut utilisé par les cmdlets Azure PowerShell suivantes, et vous permet d’accéder à n’importe quel client ou abonnement autorisé par vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1a20e-146">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="1a20e-147">Pour ajouter un nouveau contexte après la connexion,utilisez `Set-AzureRmContext` (ou son alias, `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="1a20e-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="1a20e-148">L’exemple précédent ajoute un nouveau contexte qui cible « Contoso Subscription 1 » en utilisant vos informations d’identification actuelles.</span><span class="sxs-lookup"><span data-stu-id="1a20e-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="1a20e-149">Le nouveau contexte est nommé « Contoso1 ».</span><span class="sxs-lookup"><span data-stu-id="1a20e-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="1a20e-150">Si vous ne fournissez aucun nom au contexte, un nom par défaut sera utilisé, constitué de l’ID du compte et de l’ID de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a20e-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="1a20e-151">Pour renommer un contexte existant, utilisez la cmdlet `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="1a20e-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="1a20e-152">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="1a20e-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="1a20e-153">Cet exemple change le nom `[user1@contoso.org; 123456-7890-1234-564321]` automatiquement attribué au contexte par le nom « Contoso2 ».</span><span class="sxs-lookup"><span data-stu-id="1a20e-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="1a20e-154">Les cmdlets qui gèrent les contextes utilisent aussi la saisie automatique via la touche Tab, ce qui vous permet de sélectionner rapidement le contexte.</span><span class="sxs-lookup"><span data-stu-id="1a20e-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="1a20e-155">Enfin, pour supprimer un contexte, utilisez la cmdlet `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="1a20e-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="1a20e-156">Par exemple : </span><span class="sxs-lookup"><span data-stu-id="1a20e-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="1a20e-157">Oublie le contexte nommé « Contoso2 ».</span><span class="sxs-lookup"><span data-stu-id="1a20e-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="1a20e-158">Vous pouvez recréer ce contexte par la suite à l’aide de `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="1a20e-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="1a20e-159">Suppression des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="1a20e-159">Removing credentials</span></span>

<span data-ttu-id="1a20e-160">Vous pouvez supprimer toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service à l’aide de `Remove-AzureRmAccount` (aussi appelé `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="1a20e-160">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="1a20e-161">Si vous l’exécutez sans paramètres, la cmdlet `Remove-AzureRmAccount` supprime toutes les informations d’identification et les contextes associés à un utilisateur ou un principal du service dans le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="1a20e-161">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="1a20e-162">Vous pouvez, si vous le souhaitez, transmettre un nom d’utilisateur, un nom de principal du service ou un contexte pour cibler un principal spécifique.</span><span class="sxs-lookup"><span data-stu-id="1a20e-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="1a20e-163">Utilisation des étendues de contexte</span><span class="sxs-lookup"><span data-stu-id="1a20e-163">Using context scopes</span></span>

<span data-ttu-id="1a20e-164">Vous pouvez de temps en temps sélectionner, modifier ou supprimer un contexte d’une session PowerShell sans impacter d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="1a20e-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="1a20e-165">Pour modifier le comportement par défaut des cmdlets de contexte, utilisez le paramètre `Scope`.</span><span class="sxs-lookup"><span data-stu-id="1a20e-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="1a20e-166">L’étendue `Process` remplace le comportement par défaut en l’appliquant uniquement à la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="1a20e-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="1a20e-167">À l’inverse, l’étendue `CurrentUser` modifie le contexte dans toutes les sessions, et non uniquement dans la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="1a20e-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="1a20e-168">Par exemple, pour modifier le contexte par défaut de la session PowerShell actuelle sans impacter d’autres fenêtres ni le contexte utilisé lors de la prochaine ouverture de session, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1a20e-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="1a20e-169">Mémorisation du paramètre de sauvegarde automatique du contexte</span><span class="sxs-lookup"><span data-stu-id="1a20e-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="1a20e-170">Le paramètre de sauvegarde automatique du contexte est sauvegardé dans le répertoire Azure PowerShell de l’utilisateur (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="1a20e-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="1a20e-171">Certains types de comptes d’ordinateur peuvent ne pas être capables d’accéder à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="1a20e-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="1a20e-172">Dans ce cas, vous pouvez utiliser la variable d’environnement</span><span class="sxs-lookup"><span data-stu-id="1a20e-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="1a20e-173">Si la valeur est «True», alors le contexte est sauvegardé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1a20e-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="1a20e-174">Si la valeur est «False», alors le contexte n’est pas sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="1a20e-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="1a20e-175">Modifications apportées au module AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1a20e-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="1a20e-176">Nouvelles cmdlets pour la gestion de contexte</span><span class="sxs-lookup"><span data-stu-id="1a20e-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="1a20e-177">[Enable-AzureRmContextAutosave][enable] : permet la sauvegarde de contexte entre les sessions PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="1a20e-178">Toutes modifications altèrent le contexte global.</span><span class="sxs-lookup"><span data-stu-id="1a20e-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="1a20e-179">[Disable-AzureRmContextAutosave][disable] : désactive la sauvegarde automatique du contexte.</span><span class="sxs-lookup"><span data-stu-id="1a20e-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="1a20e-180">Vous devez vous connecter à chaque nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a20e-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="1a20e-181">[Select-AzureRmContext][select] : sélectionne un contexte par défaut.</span><span class="sxs-lookup"><span data-stu-id="1a20e-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="1a20e-182">Toutes les cmdlets suivantes utilisent les informations d’identification de ce contexte pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="1a20e-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="1a20e-183">[Remove-AzureRmAccount][remove-cred] : supprime toutes les informations d’identification et les contextes associés à un compte.</span><span class="sxs-lookup"><span data-stu-id="1a20e-183">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="1a20e-184">[Remove-AzureRmContext][remove-context] : supprime un contexte nommé.</span><span class="sxs-lookup"><span data-stu-id="1a20e-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="1a20e-185">[Remove-AzureRmContext][rename] : renomme un contexte existant.</span><span class="sxs-lookup"><span data-stu-id="1a20e-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="1a20e-186">Modifications apportées à des cmdlets de profil existantes</span><span class="sxs-lookup"><span data-stu-id="1a20e-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="1a20e-187">[Add-AzureRmAccount][login] : permet d’étendre la connexion au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1a20e-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="1a20e-188">Permet de renommer le contexte par défaut après connexion.</span><span class="sxs-lookup"><span data-stu-id="1a20e-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="1a20e-189">[Import-AzureRmContext][import] : permet d’étendre la connexion au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1a20e-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="1a20e-190">[Set-AzureRmContext][set-context] : permet la sélection de contextes nommés existants, et d’étendre les modifications au processus ou à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1a20e-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
