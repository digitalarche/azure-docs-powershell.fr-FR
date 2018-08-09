---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, principal de service ou avec MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653863"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="1df31-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1df31-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="1df31-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="1df31-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="1df31-105">La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="1df31-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="1df31-106">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="1df31-106">Sign in interactively</span></span>

<span data-ttu-id="1df31-107">Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="1df31-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="1df31-108">L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure.</span><span class="sxs-lookup"><span data-stu-id="1df31-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="1df31-109">Lorsque vous vous authentifiez, ces informations sont enregistrées pour la session PowerShell actuelle, la boîte de dialogue est fermée, et vous avez accès à toutes les applets de commande Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1df31-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1df31-110">À compter d’Azure PowerShell 6.3.0, vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté à Windows.</span><span class="sxs-lookup"><span data-stu-id="1df31-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="1df31-111">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1df31-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="1df31-112">Connexion avec un principal de service</span><span class="sxs-lookup"><span data-stu-id="1df31-112">Sign in with a service principal</span></span>

<span data-ttu-id="1df31-113">Les principaux du service offrent un moyen de créer des comptes non interactifs que vous pouvez ensuite utiliser pour manipuler les ressources.</span><span class="sxs-lookup"><span data-stu-id="1df31-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="1df31-114">Les principaux du service sont comme des comptes d’utilisateur auxquels vous pouvez appliquer des règles à l’aide d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1df31-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="1df31-115">En accordant les autorisations minimales nécessaires à un principal du service, vous sécurisez encore davantage vos scripts d’automatisation.</span><span class="sxs-lookup"><span data-stu-id="1df31-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="1df31-116">Si vous avez besoin de créer un principal de service à utiliser avec Azure PowerShell, consultez [Créer un principal de service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1df31-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="1df31-117">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="1df31-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="1df31-118">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion et de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="1df31-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="1df31-119">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez l’applet de commande [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="1df31-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="1df31-120">Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.</span><span class="sxs-lookup"><span data-stu-id="1df31-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="1df31-121">Connexion à l’aide d’une identité de service administrée de machine virtuelle Azure</span><span class="sxs-lookup"><span data-stu-id="1df31-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="1df31-122">L’identité du service administré (MSI) est une fonctionnalité en version préliminaire d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1df31-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="1df31-123">Vous pouvez utiliser un principal du service MSI pour vous connecter et obtenir un jeton d’accès d’application uniquement pour accéder aux autres ressources.</span><span class="sxs-lookup"><span data-stu-id="1df31-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="1df31-124">MSI est disponible uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="1df31-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="1df31-125">Pour en savoir plus sur MSI, consultez [Utilisation d’une identité de service administré (MSI) de machine virtuelle Azure pour se connecter et obtenir des jetons](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="1df31-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="1df31-126">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="1df31-126">Sign in to another Cloud</span></span>

<span data-ttu-id="1df31-127">Les services de cloud Azure offrent différents environnements conformes aux règles de traitement des données de nombreuses régions.</span><span class="sxs-lookup"><span data-stu-id="1df31-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="1df31-128">Si votre compte Azure se trouve dans un cloud associé à une de ces régions, vous devez spécifier cet environnement lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="1df31-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="1df31-129">Par exemple, si votre compte se trouve dans le cloud de la Chine, connectez-vous à l’aide la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1df31-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="1df31-130">Pour obtenir la liste d’environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1df31-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="1df31-131">En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure</span><span class="sxs-lookup"><span data-stu-id="1df31-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="1df31-132">Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="1df31-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="1df31-133">Applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="1df31-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="1df31-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1df31-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="1df31-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1df31-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="1df31-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1df31-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="1df31-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1df31-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="1df31-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="1df31-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="1df31-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1df31-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="1df31-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1df31-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
