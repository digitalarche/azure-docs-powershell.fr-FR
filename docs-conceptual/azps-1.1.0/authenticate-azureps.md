---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342064"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="1605d-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1605d-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="1605d-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="1605d-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="1605d-105">Le moyen le plus simple pour commencer est d’utiliser [Azure Cloud Shell](/azure/cloud-shell/overview), qui vous connecte automatiquement.</span><span class="sxs-lookup"><span data-stu-id="1605d-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="1605d-106">Avec une installation locale, vous pouvez vous connecter de manière interactive par le biais de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="1605d-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="1605d-107">Lors de l’écriture de scripts pour l’automatisation, l’approche recommandée consiste à utiliser un [principal de service](create-azure-service-principal-azureps.md) avec les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="1605d-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="1605d-108">Lorsque vous limitez le plus possible les autorisations de connexion pour votre cas d’usage, vous assurez une meilleure protection de vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="1605d-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="1605d-109">Une fois connecté, les commandes sont exécutées sur votre abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="1605d-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="1605d-110">Pour changer votre abonnement actif sur une session, utilisez l’applet de commande [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="1605d-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="1605d-111">Pour changer l’abonnement par défaut utilisé lors de la connexion avec Azure PowerShell, utilisez [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="1605d-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1605d-112">Vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté.</span><span class="sxs-lookup"><span data-stu-id="1605d-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="1605d-113">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1605d-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="1605d-114">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="1605d-114">Sign in interactively</span></span>

<span data-ttu-id="1605d-115">Pour vous connecter de manière interactive, utilisez la cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="1605d-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="1605d-116">Lorsque vous l’exécutez, cette cmdlet présente une chaîne de jeton.</span><span class="sxs-lookup"><span data-stu-id="1605d-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="1605d-117">Pour vous connecter, copiez cette chaîne et collez-la dans https://microsoft.com/devicelogin dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="1605d-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="1605d-118">Votre session PowerShell est ainsi authentifiée pour vous connecter à Azure.</span><span class="sxs-lookup"><span data-stu-id="1605d-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="1605d-119">Se connecter avec des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="1605d-119">Sign in with credentials</span></span>

<span data-ttu-id="1605d-120">Vous pouvez également vous connecter avec un objet `PSCredential` autorisé à se connecter à Azure.</span><span class="sxs-lookup"><span data-stu-id="1605d-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="1605d-121">Le moyen le plus simple d’obtenir un objet d’informations d’identification consiste à utiliser l’applet de commande [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential).</span><span class="sxs-lookup"><span data-stu-id="1605d-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="1605d-122">Lorsqu’elle s’exécute, cette applet de commande vous demande une association nom d’utilisateur/mot de passe formant les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1605d-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="1605d-123">Cette approche ne fonctionne pas avec les comptes Microsoft ou les comptes pour lesquels l’authentification à deux facteurs est activée.</span><span class="sxs-lookup"><span data-stu-id="1605d-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="1605d-124">Connexion avec un principal de service</span><span class="sxs-lookup"><span data-stu-id="1605d-124">Sign in with a service principal</span></span>

<span data-ttu-id="1605d-125">Les principaux de service sont des comptes Azure non interactifs.</span><span class="sxs-lookup"><span data-stu-id="1605d-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="1605d-126">À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1605d-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="1605d-127">En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.</span><span class="sxs-lookup"><span data-stu-id="1605d-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="1605d-128">Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1605d-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="1605d-129">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="1605d-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="1605d-130">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="1605d-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="1605d-131">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="1605d-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="1605d-132">Cette cmdlet présente une invite de commande pour l’ID d’utilisateur de principal du service et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="1605d-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="1605d-133">Se connecter avec une identité managée</span><span class="sxs-lookup"><span data-stu-id="1605d-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="1605d-134">Les identités managées sont une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1605d-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="1605d-135">Les identités managées sont des principaux de service affectés aux ressources s’exécutant dans Azure.</span><span class="sxs-lookup"><span data-stu-id="1605d-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="1605d-136">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="1605d-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="1605d-137">Les identités managées sont disponibles uniquement sur les ressources en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="1605d-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="1605d-138">Pour en savoir plus sur les identités managées des ressources Azure, consultez [Guide pratique pour utiliser des identités managées avec les ressources Azure sur une machine virtuelle Azure afin d’acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="1605d-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="1605d-139">Se connecter avec un locataire non défini par défaut ou en tant que fournisseur de solutions cloud (CSP)</span><span class="sxs-lookup"><span data-stu-id="1605d-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="1605d-140">Si votre compte est associé à plusieurs locataires, l’utilisation du paramètre `-TenantId` est nécessaire au moment de la connexion.</span><span class="sxs-lookup"><span data-stu-id="1605d-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="1605d-141">Ce paramètre fonctionne avec n’importe quelle autre méthode de connexion.</span><span class="sxs-lookup"><span data-stu-id="1605d-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="1605d-142">Lors de la connexion, cette valeur de paramètre peut être l’ID d’objet Azure du locataire (ID de locataire) ou le nom de domaine complet du client.</span><span class="sxs-lookup"><span data-stu-id="1605d-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="1605d-143">Si vous êtes [fournisseur de solutions cloud (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), la valeur `-TenantId` **doit** être un ID de locataire.</span><span class="sxs-lookup"><span data-stu-id="1605d-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="1605d-144">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="1605d-144">Sign in to another Cloud</span></span>

<span data-ttu-id="1605d-145">Les services cloud Azure offrent des environnements conformes à la réglementation régionale sur la gestion des données.</span><span class="sxs-lookup"><span data-stu-id="1605d-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="1605d-146">Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="1605d-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="1605d-147">Par exemple, si votre compte se trouve dans le cloud situé en Chine :</span><span class="sxs-lookup"><span data-stu-id="1605d-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="1605d-148">Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="1605d-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```