---
title: Se connecter avec Azure PowerShell
description: Procédure de connexion avec Azure PowerShell en tant qu’utilisateur, en tant que principal de service, ou avec des identités managées pour les ressources Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 1e25d4650cc20d7b6613e0efb12ec60d424608c4
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68658094"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="0305e-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0305e-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="0305e-104">Azure PowerShell prend en charge plusieurs méthodes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="0305e-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="0305e-105">Le moyen le plus simple pour commencer est d’utiliser [Azure Cloud Shell](/azure/cloud-shell/overview), qui vous connecte automatiquement.</span><span class="sxs-lookup"><span data-stu-id="0305e-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="0305e-106">Avec une installation locale, vous pouvez vous connecter de manière interactive par le biais de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="0305e-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="0305e-107">Lors de l’écriture de scripts pour l’automatisation, l’approche recommandée consiste à utiliser un [principal de service](create-azure-service-principal-azureps.md) avec les autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0305e-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="0305e-108">Lorsque vous limitez le plus possible les autorisations de connexion pour votre cas d’usage, vous assurez une meilleure protection de vos ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="0305e-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="0305e-109">Une fois connecté, les commandes sont exécutées sur votre abonnement par défaut.</span><span class="sxs-lookup"><span data-stu-id="0305e-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="0305e-110">Pour changer votre abonnement actif sur une session, utilisez l’applet de commande [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="0305e-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="0305e-111">Pour changer l’abonnement par défaut utilisé lors de la connexion avec Azure PowerShell, utilisez [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="0305e-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="0305e-112">Vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté.</span><span class="sxs-lookup"><span data-stu-id="0305e-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="0305e-113">Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0305e-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="0305e-114">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="0305e-114">Sign in interactively</span></span>

<span data-ttu-id="0305e-115">Pour vous connecter de manière interactive, utilisez la cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="0305e-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="0305e-116">Lorsque vous l’exécutez, cette cmdlet présente une chaîne de jeton.</span><span class="sxs-lookup"><span data-stu-id="0305e-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="0305e-117">Pour vous connecter, copiez cette chaîne et collez-la dans https://microsoft.com/devicelogin dans un navigateur.</span><span class="sxs-lookup"><span data-stu-id="0305e-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="0305e-118">Votre session PowerShell est ainsi authentifiée pour vous connecter à Azure.</span><span class="sxs-lookup"><span data-stu-id="0305e-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="0305e-119">Les autorisations obtenues à l’aide des informations d’identification Nom d’utilisateur/Mot de passe ont été supprimées d’Azure PowerShell en raison des modifications apportées à l’implémentation des autorisations Active Directory ainsi qu’à l’évolution des problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0305e-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="0305e-120">Si vous utilisez ce type d’autorisations à des fins d’automatisation, [créez un principal de service](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0305e-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="0305e-121">Se connecter à un principal de service <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="0305e-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="0305e-122">Les principaux de service sont des comptes Azure non interactifs.</span><span class="sxs-lookup"><span data-stu-id="0305e-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="0305e-123">À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0305e-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="0305e-124">En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.</span><span class="sxs-lookup"><span data-stu-id="0305e-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="0305e-125">Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="0305e-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="0305e-126">Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="0305e-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="0305e-127">Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service.</span><span class="sxs-lookup"><span data-stu-id="0305e-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="0305e-128">La façon dont vous vous connectez à un principal du service varie selon que celui-ci a été configuré pour l’authentification par mot de passe ou pour l’authentification par certificat.</span><span class="sxs-lookup"><span data-stu-id="0305e-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="0305e-129">L’authentification basée sur un mot de passe</span><span class="sxs-lookup"><span data-stu-id="0305e-129">Password-based authentication</span></span>

<span data-ttu-id="0305e-130">Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="0305e-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="0305e-131">Cette applet de commande affichera une invite pour entrer un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0305e-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="0305e-132">Pour le nom d’utilisateur, utilisez l’ID du principal de service.</span><span class="sxs-lookup"><span data-stu-id="0305e-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="0305e-133">Pour les scénarios d’automatisation, vous devez créer des informations d’identification à partir d’un nom d’utilisateur et d’une chaîne sécurisée :</span><span class="sxs-lookup"><span data-stu-id="0305e-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="0305e-134">Lorsque vous automatisez les connexions au principal de service, utilisez les bonnes pratiques relatives au stockage des mots de passe.</span><span class="sxs-lookup"><span data-stu-id="0305e-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="0305e-135">Authentification par certificat</span><span class="sxs-lookup"><span data-stu-id="0305e-135">Certificate-based authentication</span></span>

<span data-ttu-id="0305e-136">L’authentification par certificat nécessite qu’Azure PowerShell puisse récupérer des informations à partir d’un magasin de certificats local en se basant sur l’empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="0305e-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="0305e-137">Dans PowerShell 5.1, le magasin de certificats peut être géré et inspecté avec le module [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="0305e-137">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="0305e-138">Pour PowerShell Core 6.x et ultérieur, le processus est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="0305e-138">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="0305e-139">Les scripts suivants montrent comment importer un certificat existant dans le magasin de certificats qui est accessible via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0305e-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="0305e-140">Importer un certificat dans PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0305e-140">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="0305e-141">Importer un certificat dans PowerShell Core 6.x et ultérieur</span><span class="sxs-lookup"><span data-stu-id="0305e-141">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="0305e-142">Se connecter avec une identité managée</span><span class="sxs-lookup"><span data-stu-id="0305e-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="0305e-143">Les identités managées sont une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0305e-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="0305e-144">Les identités managées sont des principaux de service affectés aux ressources s’exécutant dans Azure.</span><span class="sxs-lookup"><span data-stu-id="0305e-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="0305e-145">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="0305e-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="0305e-146">Les identités managées sont disponibles uniquement sur les ressources en cours d’exécution dans un cloud Azure.</span><span class="sxs-lookup"><span data-stu-id="0305e-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="0305e-147">Pour en savoir plus sur les identités managées des ressources Azure, consultez [Guide pratique pour utiliser des identités managées avec les ressources Azure sur une machine virtuelle Azure afin d’acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="0305e-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="0305e-148">Se connecter avec un locataire non défini par défaut ou en tant que fournisseur de solutions cloud (CSP)</span><span class="sxs-lookup"><span data-stu-id="0305e-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="0305e-149">Si votre compte est associé à plusieurs locataires, l’utilisation du paramètre `-TenantId` est nécessaire au moment de la connexion.</span><span class="sxs-lookup"><span data-stu-id="0305e-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="0305e-150">Ce paramètre fonctionne avec n’importe quelle autre méthode de connexion.</span><span class="sxs-lookup"><span data-stu-id="0305e-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="0305e-151">Lors de la connexion, cette valeur de paramètre peut être l’ID d’objet Azure du locataire (ID de locataire) ou le nom de domaine complet du client.</span><span class="sxs-lookup"><span data-stu-id="0305e-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="0305e-152">Si vous êtes [fournisseur de solutions cloud (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), la valeur `-TenantId` **doit** être un ID de locataire.</span><span class="sxs-lookup"><span data-stu-id="0305e-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="0305e-153">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="0305e-153">Sign in to another Cloud</span></span>

<span data-ttu-id="0305e-154">Les services cloud Azure offrent des environnements conformes à la réglementation régionale sur la gestion des données.</span><span class="sxs-lookup"><span data-stu-id="0305e-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="0305e-155">Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="0305e-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="0305e-156">Par exemple, si votre compte se trouve dans le cloud situé en Chine :</span><span class="sxs-lookup"><span data-stu-id="0305e-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="0305e-157">Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0305e-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
