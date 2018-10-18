---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 2a118e1aa8b6755ef5769f44429427d22532780d
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399669"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="8f5d9-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f5d9-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="8f5d9-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="8f5d9-105">La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="8f5d9-106">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="8f5d9-106">Sign in interactively</span></span>

<span data-ttu-id="8f5d9-107">Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="8f5d9-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="8f5d9-108">L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="8f5d9-109">Cette authentification est valable pour la session PowerShell en cours.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f5d9-110">À compter d’Azure PowerShell 6.3.0, vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté à Windows.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="8f5d9-111">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="8f5d9-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="8f5d9-112">Connexion avec un principal de service</span><span class="sxs-lookup"><span data-stu-id="8f5d9-112">Sign in with a service principal</span></span>

<span data-ttu-id="8f5d9-113">Les principaux de service sont des comptes Azure non interactifs.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="8f5d9-114">À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="8f5d9-115">En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="8f5d9-116">Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8f5d9-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="8f5d9-117">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="8f5d9-118">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="8f5d9-119">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="8f5d9-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="8f5d9-120">Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="8f5d9-121">Connexion à l’aide d’Azure Managed Service Identity</span><span class="sxs-lookup"><span data-stu-id="8f5d9-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="8f5d9-122">Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="8f5d9-123">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="8f5d9-124">Les identités managées sont disponibles uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="8f5d9-125">Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="8f5d9-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="8f5d9-126">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="8f5d9-126">Sign in to another Cloud</span></span>

<span data-ttu-id="8f5d9-127">Les services cloud Azure offrent des environnements conformes aux réglementations régionales en matière de gestion de données.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-127">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="8f5d9-128">Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="8f5d9-128">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="8f5d9-129">Par exemple, si votre compte se trouve dans le cloud situé en Chine :</span><span class="sxs-lookup"><span data-stu-id="8f5d9-129">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="8f5d9-130">Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8f5d9-130">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="8f5d9-131">En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure</span><span class="sxs-lookup"><span data-stu-id="8f5d9-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="8f5d9-132">Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="8f5d9-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="8f5d9-133">Applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="8f5d9-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="8f5d9-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8f5d9-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="8f5d9-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8f5d9-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="8f5d9-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8f5d9-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="8f5d9-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8f5d9-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="8f5d9-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8f5d9-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="8f5d9-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8f5d9-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="8f5d9-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8f5d9-140">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
