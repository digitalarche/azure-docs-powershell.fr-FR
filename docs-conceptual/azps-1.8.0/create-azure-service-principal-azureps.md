---
title: Utiliser des principaux de service avec Azure PowerShell
description: Découvrez comment créer et utiliser des principaux de service avec Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 6d9df4a62238f1e3b9cc9a62864f5d4d9337d6a7
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807382"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="008d5-103">Créer un principal du service Azure avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="008d5-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="008d5-104">Les outils automatisés qui utilisent les services Azure doivent toujours avoir des autorisations restreintes.</span><span class="sxs-lookup"><span data-stu-id="008d5-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="008d5-105">Plutôt que de faire se connecter des applications en tant qu’utilisateur entièrement privilégié, Azure offre des principaux du service.</span><span class="sxs-lookup"><span data-stu-id="008d5-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="008d5-106">Un principal de service Azure est une identité créée pour une utilisation avec les applications, des services hébergés et des outils automatisés permettant d’accéder aux ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="008d5-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="008d5-107">Cet accès est limité par les rôles assignés au principal du service, ce qui vous permet de contrôler quelles ressources sont accessibles et à quel niveau.</span><span class="sxs-lookup"><span data-stu-id="008d5-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="008d5-108">Pour des raisons de sécurité, il est toujours recommandé d’utiliser les principaux du service avec des outils automatisés, plutôt que de leur permettre de se connecter avec une identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="008d5-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="008d5-109">Cet article vous explique les étapes à suivre pour créer un principal du service, obtenir des informations à son sujet et le réinitialiser avec Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="008d5-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="008d5-110">Créer un principal du service</span><span class="sxs-lookup"><span data-stu-id="008d5-110">Create a service principal</span></span>

<span data-ttu-id="008d5-111">Créez un principal de service avec l’applet de commande [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="008d5-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="008d5-112">Lorsque vous créez un principal de service, vous choisissez le type d’authentification de connexion qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="008d5-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="008d5-113">Si votre compte ne dispose pas d’autorisations pour créer un principal de service, `New-AzADServicePrincipal` vous retournera un message d’erreur contenant « Privilèges insuffisants pour effectuer l’opération ».</span><span class="sxs-lookup"><span data-stu-id="008d5-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="008d5-114">Contactez votre administrateur Azure Active Directory pour créer un principal de service.</span><span class="sxs-lookup"><span data-stu-id="008d5-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="008d5-115">Il existe deux types d’authentification disponibles pour les principaux de service : L’authentification basée sur un mot de passe et l’authentification basée sur un certificat.</span><span class="sxs-lookup"><span data-stu-id="008d5-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="008d5-116">L’authentification basée sur un mot de passe</span><span class="sxs-lookup"><span data-stu-id="008d5-116">Password-based authentication</span></span>

<span data-ttu-id="008d5-117">Sans autres paramètres d’authentification, l’authentification par mot de passe est utilisée et un mot de passe aléatoire est créé.</span><span class="sxs-lookup"><span data-stu-id="008d5-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="008d5-118">Si vous souhaitez une authentification basée sur un mot de passe, cette méthode est recommandée.</span><span class="sxs-lookup"><span data-stu-id="008d5-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="008d5-119">L’objet retourné contient le membre `Secret`, qui est un `SecureString` contenant le mot de passe généré.</span><span class="sxs-lookup"><span data-stu-id="008d5-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="008d5-120">Veillez à stocker cette valeur dans un endroit sécurisé pour vous authentifier auprès du principal de service.</span><span class="sxs-lookup"><span data-stu-id="008d5-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="008d5-121">Sa valeur __ne s’affichera pas__ dans la console.</span><span class="sxs-lookup"><span data-stu-id="008d5-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="008d5-122">Si vous perdez le mot de passe, effectuez une [réinitialisation des informations d’identification du principal de service](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="008d5-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span>

<span data-ttu-id="008d5-123">Le code suivant vous permet d’exporter le secret :</span><span class="sxs-lookup"><span data-stu-id="008d5-123">The following code will allow you to export the secret:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

<span data-ttu-id="008d5-124">Pour les mots de passe fournis par l’utilisateur, l’argument `-PasswordCredential` accepte les objets `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="008d5-124">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="008d5-125">Ces objets doivent avoir un `StartDate` et un `EndDate` valides, et accepter un `Password` en texte en clair.</span><span class="sxs-lookup"><span data-stu-id="008d5-125">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="008d5-126">Lorsque vous créez un mot de passe, assurez-vous de suivre les [règles et restrictions relatives aux mots de passe Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="008d5-126">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="008d5-127">N’utilisez pas de mot de passe faible. Ne réutilisez pas de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="008d5-127">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="008d5-128">L’objet retourné par `New-AzADServicePrincipal` contient les membres `Id` et `DisplayName`, qui peuvent être utilisés pour se connecter au principal de service.</span><span class="sxs-lookup"><span data-stu-id="008d5-128">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="008d5-129">La connexion au principal de service nécessite l’ID du locataire dans lequel le principal de service a été créé.</span><span class="sxs-lookup"><span data-stu-id="008d5-129">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="008d5-130">Pour obtenir le locataire qui était actif au moment de la création du principal de service, exécutez la commande suivante __immédiatement après__ avoir créé le principal de service :</span><span class="sxs-lookup"><span data-stu-id="008d5-130">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="008d5-131">Authentification par certificat</span><span class="sxs-lookup"><span data-stu-id="008d5-131">Certificate-based authentication</span></span>

<span data-ttu-id="008d5-132">Les principaux de service qui utilisent l’authentification par certificat sont créés avec le paramètre `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="008d5-132">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="008d5-133">Ce paramètre accepte la chaîne ASCII codée en base64 du certificat public.</span><span class="sxs-lookup"><span data-stu-id="008d5-133">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="008d5-134">Celui-ci est représenté par un fichier PEM, ou par un fichier CRT ou CER avec texte encodé.</span><span class="sxs-lookup"><span data-stu-id="008d5-134">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="008d5-135">Les encodages binaires du certificat public ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="008d5-135">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="008d5-136">Ces instructions supposent que vous disposez déjà d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="008d5-136">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="008d5-137">Vous pouvez également utiliser le paramètre `-KeyCredential`, qui accepte les objets `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="008d5-137">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="008d5-138">Ces objets doivent avoir un `StartDate` et un `EndDate` valides. De plus, leur membre `CertValue` doit être défini sur la chaîne ASCII codée en base64 du certificat public.</span><span class="sxs-lookup"><span data-stu-id="008d5-138">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="008d5-139">L’objet retourné par `New-AzADServicePrincipal` contient les membres `Id` et `DisplayName`, qui peuvent être utilisés pour se connecter au principal de service.</span><span class="sxs-lookup"><span data-stu-id="008d5-139">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="008d5-140">Les clients qui se connectent au principal de service ont également besoin d’accéder à la clé privée du certificat.</span><span class="sxs-lookup"><span data-stu-id="008d5-140">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="008d5-141">La connexion au principal de service nécessite l’ID du locataire dans lequel le principal de service a été créé.</span><span class="sxs-lookup"><span data-stu-id="008d5-141">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="008d5-142">Pour obtenir le locataire qui était actif au moment de la création du principal de service, exécutez la commande suivante __immédiatement après__ avoir créé le principal de service :</span><span class="sxs-lookup"><span data-stu-id="008d5-142">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="008d5-143">Obtenir un principal de service existant</span><span class="sxs-lookup"><span data-stu-id="008d5-143">Get an existing service principal</span></span>

<span data-ttu-id="008d5-144">Vous pouvez récupérer la liste des principaux de service du locataire actif à l’aide de [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="008d5-144">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="008d5-145">Par défaut, cette commande retourne __tous__ les principaux de service d’un locataire. Pour les grandes organisations, les résultats peuvent donc mettre du temps à s’afficher.</span><span class="sxs-lookup"><span data-stu-id="008d5-145">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="008d5-146">Pour cette raison, il est recommandé d’utiliser l’un des arguments de filtrage côté serveur facultatifs :</span><span class="sxs-lookup"><span data-stu-id="008d5-146">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="008d5-147">`-DisplayNameBeginsWith` demande les principaux de service ayant un _préfixe_ qui correspond à la valeur fournie.</span><span class="sxs-lookup"><span data-stu-id="008d5-147">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="008d5-148">Le nom d’affichage d’un principal de service correspond à la valeur définie avec `-DisplayName` lors de la création.</span><span class="sxs-lookup"><span data-stu-id="008d5-148">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="008d5-149">`-DisplayName` demande une _correspondance exacte_ du nom du principal de service.</span><span class="sxs-lookup"><span data-stu-id="008d5-149">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="008d5-150">Gérer les rôles du principal du service</span><span class="sxs-lookup"><span data-stu-id="008d5-150">Manage service principal roles</span></span>

<span data-ttu-id="008d5-151">Azure PowerShell fournit les applets de commande suivantes pour gérer les attributions de rôles :</span><span class="sxs-lookup"><span data-stu-id="008d5-151">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="008d5-152">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="008d5-152">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="008d5-153">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="008d5-153">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="008d5-154">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="008d5-154">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="008d5-155">Un principal du service a le rôle **Contributor** (Collaborateur) par défaut.</span><span class="sxs-lookup"><span data-stu-id="008d5-155">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="008d5-156">Ce rôle dispose des autorisations complètes de lecture et d’écriture dans un compte Azure.</span><span class="sxs-lookup"><span data-stu-id="008d5-156">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="008d5-157">Le rôle de **Lecteur** est plus restrictif avec un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="008d5-157">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="008d5-158">Pour plus d’informations sur les rôles et le contrôle d’accès en fonction du rôle, consultez [RBAC : rôles intégrés pour les ressources Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="008d5-158">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="008d5-159">Cet exemple ajoute le rôle de **Lecteur** et supprime le rôle de **Contributeur** :</span><span class="sxs-lookup"><span data-stu-id="008d5-159">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="008d5-160">Les applets de commande d’attribution de rôle n’acceptent pas l’ID d’objet du principal de service.</span><span class="sxs-lookup"><span data-stu-id="008d5-160">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="008d5-161">Elles acceptent l’ID d’application associé, qui est généré au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="008d5-161">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="008d5-162">Pour obtenir l’ID d’application d’un principal de service, utilisez `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="008d5-162">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="008d5-163">Si votre compte ne dispose pas d’autorisations pour assigner un rôle, un message d’erreur vous indiquera que votre compte « n’est pas autorisé à effectuer l’action ’Microsoft.Authorization/roleAssignments/write’ ». Contactez votre administrateur Azure Active Directory pour gérer les rôles.</span><span class="sxs-lookup"><span data-stu-id="008d5-163">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="008d5-164">L’ajout d’un rôle ne restreint _pas_ les autorisations précédemment assignées.</span><span class="sxs-lookup"><span data-stu-id="008d5-164">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="008d5-165">Lors de la restriction des autorisations du principal du service, le rôle de __Contributeur__ dot être supprimé.</span><span class="sxs-lookup"><span data-stu-id="008d5-165">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="008d5-166">Les modifications peuvent être vérifiées en répertoriant les rôles attribués :</span><span class="sxs-lookup"><span data-stu-id="008d5-166">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="008d5-167">Se connecter en tant que principal du service</span><span class="sxs-lookup"><span data-stu-id="008d5-167">Sign in using a service principal</span></span>

<span data-ttu-id="008d5-168">Testez les informations d’identification et les autorisations du nouveau principal du service en vous connectant.</span><span class="sxs-lookup"><span data-stu-id="008d5-168">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="008d5-169">Pour vous connecter à un principal de service, vous avez besoin de la valeur `applicationId` qui lui est associée, ainsi que du locataire dans lequel il a été créé.</span><span class="sxs-lookup"><span data-stu-id="008d5-169">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="008d5-170">Pour vous connecter avec un principal du service utilisant un mot de passe :</span><span class="sxs-lookup"><span data-stu-id="008d5-170">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="008d5-171">L’authentification par certificat nécessite qu’Azure PowerShell puisse récupérer des informations à partir d’un magasin de certificats local en se basant sur l’empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="008d5-171">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="008d5-172">Pour obtenir des instructions sur l’importation d’un certificat dans un magasin d’informations d’identification accessible par PowerShell, consultez [Se connecter avec Azure PowerShell](authenticate-azureps.md#sp-signin).</span><span class="sxs-lookup"><span data-stu-id="008d5-172">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="008d5-173">Réinitialiser les informations d’identification</span><span class="sxs-lookup"><span data-stu-id="008d5-173">Reset credentials</span></span>

<span data-ttu-id="008d5-174">Si vous avez oublié les informations d’identification d’un principal de service, utilisez [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) pour ajouter de nouvelles informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="008d5-174">If you forget the credentials for a service principal, use [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="008d5-175">Cette applet de commande accepte les mêmes arguments d’informations d’identification et les mêmes types que `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="008d5-175">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="008d5-176">En l’absence d’arguments d’informations d’identification, un nouveau `PasswordCredential` et un mot de passe aléatoire sont créés.</span><span class="sxs-lookup"><span data-stu-id="008d5-176">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="008d5-177">Avant d’attribuer de nouvelles informations d’identification, vous pouvez supprimer les informations d’identification existantes afin d’empêcher qu’elles soient utilisées pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="008d5-177">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="008d5-178">Pour ce faire, utilisez l’applet de commande [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) :</span><span class="sxs-lookup"><span data-stu-id="008d5-178">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
