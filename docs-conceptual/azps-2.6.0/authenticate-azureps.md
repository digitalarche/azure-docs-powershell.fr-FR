---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.openlocfilehash: 44f5d5b44788a52db297a0d73697161eec2eedc2
ms.sourcegitcommit: e5b029312d17e12257b2b5351b808fdab0b4634c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2019
ms.locfileid: "70386759"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="99d7d-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="99d7d-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="99d7d-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="99d7d-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="99d7d-105">Le moyen le plus simple pour commencer est d’utiliser [Azure Cloud Shell](/azure/cloud-shell/overview), qui vous connecte automatiquement.</span><span class="sxs-lookup"><span data-stu-id="99d7d-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="99d7d-106">Avec une installation locale, vous pouvez vous connecter de manière interactive par le biais de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="99d7d-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="99d7d-107">Lors de l’écriture de scripts pour l’automatisation, l’approche recommandée consiste à utiliser un [principal de service](create-azure-service-principal-azureps.md) avec les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="99d7d-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="99d7d-108">Lorsque vous limitez le plus possible les autorisations de connexion pour votre cas d’usage, vous assurez une meilleure protection de vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="99d7d-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="99d7d-109">Une fois connecté, les commandes sont exécutées sur votre abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="99d7d-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="99d7d-110">Pour changer votre abonnement actif sur une session, utilisez l’applet de commande [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="99d7d-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="99d7d-111">Pour changer l’abonnement par défaut utilisé lors de la connexion avec Azure PowerShell, utilisez [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="99d7d-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="99d7d-112">Vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté.</span><span class="sxs-lookup"><span data-stu-id="99d7d-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="99d7d-113">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="99d7d-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="99d7d-114">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="99d7d-114">Sign in interactively</span></span>

<span data-ttu-id="99d7d-115">Pour vous connecter de manière interactive, utilisez la cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="99d7d-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="99d7d-116">Lorsque vous l’exécutez, cette cmdlet présente une chaîne de jeton.</span><span class="sxs-lookup"><span data-stu-id="99d7d-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="99d7d-117">Pour vous connecter, copiez cette chaîne et collez-la dans https://microsoft.com/devicelogin dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="99d7d-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="99d7d-118">Votre session PowerShell est ainsi authentifiée pour vous connecter à Azure.</span><span class="sxs-lookup"><span data-stu-id="99d7d-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="99d7d-119">Les autorisations obtenues à l’aide des informations d’identification Nom d’utilisateur/Mot de passe ont été supprimées d’Azure PowerShell en raison des modifications apportées à l’implémentation des autorisations Active Directory ainsi qu’à l’évolution des problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="99d7d-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="99d7d-120">Si vous utilisez ce type d’autorisations à des fins d’automatisation, [créez un principal de service](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="99d7d-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="99d7d-121">Se connecter à un principal de service <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="99d7d-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="99d7d-122">Les principaux de service sont des comptes Azure non interactifs.</span><span class="sxs-lookup"><span data-stu-id="99d7d-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="99d7d-123">À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="99d7d-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="99d7d-124">En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.</span><span class="sxs-lookup"><span data-stu-id="99d7d-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="99d7d-125">Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="99d7d-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="99d7d-126">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="99d7d-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="99d7d-127">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="99d7d-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="99d7d-128">La façon dont vous vous connectez à un principal du service varie selon que celui-ci a été configuré pour l’authentification par mot de passe ou pour l’authentification par certificat.</span><span class="sxs-lookup"><span data-stu-id="99d7d-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="99d7d-129">L’authentification basée sur un mot de passe</span><span class="sxs-lookup"><span data-stu-id="99d7d-129">Password-based authentication</span></span>

<span data-ttu-id="99d7d-130">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="99d7d-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="99d7d-131">Cette applet de commande affichera une invite pour entrer un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="99d7d-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="99d7d-132">Pour le nom d’utilisateur, utilisez l’ID du principal de service.</span><span class="sxs-lookup"><span data-stu-id="99d7d-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="99d7d-133">Pour les scénarios d’automatisation, vous devez créer des informations d’identification à partir d’un nom d’utilisateur et d’une chaîne sécurisée :</span><span class="sxs-lookup"><span data-stu-id="99d7d-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="99d7d-134">Lorsque vous automatisez les connexions au principal de service, utilisez les bonnes pratiques relatives au stockage des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="99d7d-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="99d7d-135">Authentification par certificat</span><span class="sxs-lookup"><span data-stu-id="99d7d-135">Certificate-based authentication</span></span>

<span data-ttu-id="99d7d-136">L’authentification par certificat nécessite qu’Azure PowerShell puisse récupérer des informations à partir d’un magasin de certificats local en se basant sur l’empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="99d7d-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="99d7d-137">Quand vous utilisez un principal de service au lieu d’une application inscrite, ajoutez l’argument `-ServicePrincipal` et fournissez l’ID du principal de service comme valeur du paramètre `-ApplicationId`.</span><span class="sxs-lookup"><span data-stu-id="99d7d-137">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="99d7d-138">Dans PowerShell 5.1, le magasin de certificats peut être géré et inspecté avec le module [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="99d7d-138">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="99d7d-139">Pour PowerShell Core 6.x et ultérieur, le processus est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="99d7d-139">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="99d7d-140">Les scripts suivants montrent comment importer un certificat existant dans le magasin de certificats qui est accessible via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99d7d-140">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="99d7d-141">Importer un certificat dans PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="99d7d-141">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="99d7d-142">Importer un certificat dans PowerShell Core 6.x et ultérieur</span><span class="sxs-lookup"><span data-stu-id="99d7d-142">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="99d7d-143">Se connecter avec une identité managée</span><span class="sxs-lookup"><span data-stu-id="99d7d-143">Sign in using a managed identity</span></span>

<span data-ttu-id="99d7d-144">Les identités managées sont une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="99d7d-144">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="99d7d-145">Les identités managées sont des principaux de service affectés aux ressources s’exécutant dans Azure.</span><span class="sxs-lookup"><span data-stu-id="99d7d-145">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="99d7d-146">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="99d7d-146">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="99d7d-147">Les identités managées sont disponibles uniquement sur les ressources en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="99d7d-147">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="99d7d-148">Pour en savoir plus sur les identités managées des ressources Azure, consultez [Guide pratique pour utiliser des identités managées avec les ressources Azure sur une machine virtuelle Azure afin d’acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="99d7d-148">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="99d7d-149">Se connecter avec un locataire non défini par défaut ou en tant que fournisseur de solutions cloud (CSP)</span><span class="sxs-lookup"><span data-stu-id="99d7d-149">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="99d7d-150">Si votre compte est associé à plusieurs locataires, l’utilisation du paramètre `-Tenant` est nécessaire au moment de la connexion.</span><span class="sxs-lookup"><span data-stu-id="99d7d-150">If your account is associated with more than one tenant, sign-in requires the use of the `-Tenant` parameter when connecting.</span></span> <span data-ttu-id="99d7d-151">Ce paramètre fonctionne avec n’importe quelle méthode de connexion.</span><span class="sxs-lookup"><span data-stu-id="99d7d-151">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="99d7d-152">Lors de la connexion, cette valeur de paramètre peut être l’ID d’objet Azure du locataire (ID de locataire) ou le nom de domaine complet du client.</span><span class="sxs-lookup"><span data-stu-id="99d7d-152">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="99d7d-153">Si vous êtes [fournisseur de solutions cloud (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), la valeur `-Tenant` **doit** être un ID de locataire.</span><span class="sxs-lookup"><span data-stu-id="99d7d-153">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="99d7d-154">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="99d7d-154">Sign in to another Cloud</span></span>

<span data-ttu-id="99d7d-155">Les services cloud Azure offrent des environnements conformes à la réglementation régionale sur la gestion des données.</span><span class="sxs-lookup"><span data-stu-id="99d7d-155">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="99d7d-156">Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="99d7d-156">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="99d7d-157">Ce paramètre fonctionne avec n’importe quelle méthode de connexion.</span><span class="sxs-lookup"><span data-stu-id="99d7d-157">This parameter will work with any sign-in method.</span></span> <span data-ttu-id="99d7d-158">Par exemple, si votre compte se trouve dans le cloud situé en Chine :</span><span class="sxs-lookup"><span data-stu-id="99d7d-158">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="99d7d-159">Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="99d7d-159">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
