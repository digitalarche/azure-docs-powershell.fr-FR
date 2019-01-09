---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786677"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="9bfbd-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9bfbd-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="9bfbd-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="9bfbd-105">La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="9bfbd-106">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="9bfbd-106">Sign in interactively</span></span>

<span data-ttu-id="9bfbd-107">Pour vous connecter de manière interactive, utilisez la cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="9bfbd-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="9bfbd-108">Lorsque vous l’exécutez, cette cmdlet présente une chaîne de jeton.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="9bfbd-109">Pour vous connecter, copiez cette chaîne et collez-la dans https://microsoft.com/devicelogin dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="9bfbd-110">Votre session PowerShell sera ensuite authentifiée pour vous connecter à Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="9bfbd-111">Cette authentification est valable pour la session PowerShell en cours.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9bfbd-112">Vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="9bfbd-113">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9bfbd-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="9bfbd-114">Connexion avec un principal de service</span><span class="sxs-lookup"><span data-stu-id="9bfbd-114">Sign in with a service principal</span></span>

<span data-ttu-id="9bfbd-115">Les principaux de service sont des comptes Azure non interactifs.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="9bfbd-116">À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="9bfbd-117">En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="9bfbd-118">Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9bfbd-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="9bfbd-119">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="9bfbd-120">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="9bfbd-121">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="9bfbd-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="9bfbd-122">Cette cmdlet présente une invite de commande pour l’ID d’utilisateur de principal du service et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="9bfbd-123">Connexion à l’aide d’Azure Managed Service Identity</span><span class="sxs-lookup"><span data-stu-id="9bfbd-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="9bfbd-124">Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="9bfbd-125">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="9bfbd-126">Les identités managées sont disponibles uniquement sur les machines virtuelles en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="9bfbd-127">Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="9bfbd-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="9bfbd-128">Se connecter en tant que fournisseur de solutions cloud (CSP)</span><span class="sxs-lookup"><span data-stu-id="9bfbd-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="9bfbd-129">Une connexion en tant que [fournisseur de solutions Cloud (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) nécessite l’utilisation de `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="9bfbd-130">Normalement, ce paramètre peut être spécifié comme un ID de locataire ou un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="9bfbd-131">Toutefois, pour les connexions en tant que CSP, un **ID de locataire** doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="9bfbd-132">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="9bfbd-132">Sign in to another Cloud</span></span>

<span data-ttu-id="9bfbd-133">Les services cloud Azure offrent des environnements conformes aux réglementations régionales en matière de gestion de données.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="9bfbd-134">Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="9bfbd-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="9bfbd-135">Par exemple, si votre compte se trouve dans le cloud situé en Chine :</span><span class="sxs-lookup"><span data-stu-id="9bfbd-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="9bfbd-136">Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="9bfbd-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="9bfbd-137">En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure</span><span class="sxs-lookup"><span data-stu-id="9bfbd-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="9bfbd-138">Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="9bfbd-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="9bfbd-139">Applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="9bfbd-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="9bfbd-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9bfbd-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="9bfbd-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9bfbd-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="9bfbd-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9bfbd-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="9bfbd-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9bfbd-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="9bfbd-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9bfbd-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="9bfbd-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9bfbd-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="9bfbd-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9bfbd-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
