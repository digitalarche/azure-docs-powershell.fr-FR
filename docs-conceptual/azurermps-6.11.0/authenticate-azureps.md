---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: c19d9ade0f69f4af9f14c68ad22b327c27c8ccfd
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738204"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ad783-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad783-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="ad783-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="ad783-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="ad783-105">La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ad783-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ad783-106">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="ad783-106">Sign in interactively</span></span>

<span data-ttu-id="ad783-107">Pour se connecter de manière interactive, utilisez l’applet de commande [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="ad783-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="ad783-108">L’exécution de cette applet de commande permet d’afficher une boîte de dialogue vous invitant à entrer votre adresse de messagerie et le mot de passe associé à votre compte Azure.</span><span class="sxs-lookup"><span data-stu-id="ad783-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="ad783-109">Cette authentification est valable pour la session PowerShell en cours.</span><span class="sxs-lookup"><span data-stu-id="ad783-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad783-110">À compter d’Azure PowerShell 6.3.0, vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté à Windows.</span><span class="sxs-lookup"><span data-stu-id="ad783-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="ad783-111">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ad783-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="ad783-112">Connexion avec un principal de service</span><span class="sxs-lookup"><span data-stu-id="ad783-112">Sign in with a service principal</span></span>

<span data-ttu-id="ad783-113">Les principaux de service sont des comptes Azure non interactifs.</span><span class="sxs-lookup"><span data-stu-id="ad783-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="ad783-114">À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad783-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="ad783-115">En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.</span><span class="sxs-lookup"><span data-stu-id="ad783-115">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="ad783-116">Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ad783-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ad783-117">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="ad783-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="ad783-118">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="ad783-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="ad783-119">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="ad783-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ad783-120">Cette applet de commande affiche une boîte de dialogue permettant d’entrer l’ID utilisateur du principal de service et le mot de passe associé.</span><span class="sxs-lookup"><span data-stu-id="ad783-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="ad783-121">Connexion à l’aide d’Azure Managed Service Identity</span><span class="sxs-lookup"><span data-stu-id="ad783-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="ad783-122">Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad783-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="ad783-123">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="ad783-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ad783-124">Les identités managées sont disponibles uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="ad783-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="ad783-125">Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="ad783-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="ad783-126">Se connecter en tant que fournisseur de solutions cloud (CSP)</span><span class="sxs-lookup"><span data-stu-id="ad783-126">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="ad783-127">Une connexion en tant que [fournisseur de solutions Cloud (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) nécessite l’utilisation de `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="ad783-127">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="ad783-128">Normalement, ce paramètre peut être spécifié comme un ID de locataire ou un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="ad783-128">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="ad783-129">Toutefois, pour les connexions en tant que CSP, un **ID de locataire** doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="ad783-129">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ad783-130">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="ad783-130">Sign in to another Cloud</span></span>

<span data-ttu-id="ad783-131">Les services cloud Azure offrent des environnements conformes aux réglementations régionales en matière de gestion de données.</span><span class="sxs-lookup"><span data-stu-id="ad783-131">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="ad783-132">Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="ad783-132">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="ad783-133">Par exemple, si votre compte se trouve dans le cloud situé en Chine :</span><span class="sxs-lookup"><span data-stu-id="ad783-133">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ad783-134">Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ad783-134">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="ad783-135">En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure</span><span class="sxs-lookup"><span data-stu-id="ad783-135">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="ad783-136">Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="ad783-136">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="ad783-137">Applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="ad783-137">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="ad783-138">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad783-138">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="ad783-139">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ad783-139">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="ad783-140">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad783-140">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="ad783-141">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ad783-141">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="ad783-142">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad783-142">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="ad783-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ad783-143">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="ad783-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ad783-144">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
