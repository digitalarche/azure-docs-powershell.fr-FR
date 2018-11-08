---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 9a93145f2abeea466a739775ca8ae7e337e78166
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212112"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="06b37-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06b37-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="06b37-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="06b37-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="06b37-105">La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="06b37-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="06b37-106">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="06b37-106">Sign in interactively</span></span>

<span data-ttu-id="06b37-107">Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="06b37-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="06b37-108">L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure.</span><span class="sxs-lookup"><span data-stu-id="06b37-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="06b37-109">Lorsque vous vous authentifiez, ces informations sont enregistrées pour la session PowerShell actuelle, la boîte de dialogue est fermée, et vous avez accès à toutes les applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06b37-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06b37-110">Cette procédure de connexion est valable pour la session PowerShell _uniquement_.</span><span class="sxs-lookup"><span data-stu-id="06b37-110">This sign in is for the current PowerShell session _only_.</span></span> <span data-ttu-id="06b37-111">Pour conserver l’authentification sur plusieurs sessions, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="06b37-111">To persist authentication across multiple sessions, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="06b37-112">Connexion avec un principal de service</span><span class="sxs-lookup"><span data-stu-id="06b37-112">Sign in with a service principal</span></span>

<span data-ttu-id="06b37-113">Les principaux du service offrent un moyen de créer des comptes non interactifs que vous pouvez ensuite utiliser pour manipuler les ressources.</span><span class="sxs-lookup"><span data-stu-id="06b37-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="06b37-114">Les principaux du service sont comme des comptes d’utilisateur auxquels vous pouvez appliquer des règles à l’aide d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="06b37-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="06b37-115">En accordant les autorisations minimales nécessaires à un principal du service, vous sécurisez encore davantage vos scripts d’automatisation.</span><span class="sxs-lookup"><span data-stu-id="06b37-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="06b37-116">Si vous avez besoin de créer un principal de service à utiliser avec Azure PowerShell, consultez [Créer un principal de service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="06b37-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="06b37-117">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="06b37-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="06b37-118">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion et de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="06b37-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="06b37-119">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez l’applet de commande [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="06b37-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="06b37-120">Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.</span><span class="sxs-lookup"><span data-stu-id="06b37-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="06b37-121">Se connecter en utilisant des identités managées pour les ressources Azure</span><span class="sxs-lookup"><span data-stu-id="06b37-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="06b37-122">Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="06b37-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="06b37-123">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="06b37-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="06b37-124">Les identités managées sont disponibles uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="06b37-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="06b37-125">Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="06b37-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="06b37-126">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="06b37-126">Sign in to another Cloud</span></span>

<span data-ttu-id="06b37-127">Les services de cloud Azure offrent différents environnements conformes aux règles de traitement des données de nombreuses régions.</span><span class="sxs-lookup"><span data-stu-id="06b37-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="06b37-128">Si votre compte Azure se trouve dans un cloud associé à une de ces régions, vous devez spécifier cet environnement lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="06b37-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="06b37-129">Par exemple, si votre compte se trouve dans le cloud de la Chine, connectez-vous à l’aide la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="06b37-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="06b37-130">Pour obtenir la liste d’environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="06b37-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="06b37-131">En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure</span><span class="sxs-lookup"><span data-stu-id="06b37-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="06b37-132">Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="06b37-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="06b37-133">Applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="06b37-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="06b37-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06b37-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="06b37-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06b37-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="06b37-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06b37-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="06b37-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06b37-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="06b37-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="06b37-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="06b37-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06b37-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="06b37-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="06b37-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
