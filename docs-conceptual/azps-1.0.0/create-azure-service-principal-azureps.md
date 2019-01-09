---
title: Créer un principal du service Azure avec Azure PowerShell
description: Découvrez comment créer un principal du service pour votre application ou service avec Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594780"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="351fd-104">Créer un principal du service Azure avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="351fd-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="351fd-105">Si vous prévoyez de gérer votre application ou service avec Azure PowerShell, vous devez l’exécuter avec un principal du service Azure Active Directory (AAD) plutôt qu’avec vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="351fd-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="351fd-106">Cet article vous explique pas à pas comment créer un principal de sécurité avec Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="351fd-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="351fd-107">Qu’est-ce qu’un principal de service ?</span><span class="sxs-lookup"><span data-stu-id="351fd-107">What is a service principal?</span></span>

<span data-ttu-id="351fd-108">Un principal du service Azure est une identité de sécurité utilisée par les applications, les services et les outils d’automatisation créés par l’utilisateur pour accéder à des ressources Azure spécifiques.</span><span class="sxs-lookup"><span data-stu-id="351fd-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="351fd-109">Les principaux de service reçoivent des autorisations spécifiques liées à leurs tâches, ce qui vous donne un meilleur contrôle sur la sécurité.</span><span class="sxs-lookup"><span data-stu-id="351fd-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="351fd-110">Contrairement à une identité d’utilisateur, qui est généralement autorisée à apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="351fd-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="351fd-111">Vérifier votre propre niveau d’autorisation</span><span class="sxs-lookup"><span data-stu-id="351fd-111">Verify your own permission level</span></span>

<span data-ttu-id="351fd-112">Tout d’abord, vous devez avoir les autorisations suffisantes dans votre annuaire Azure Active Directory et votre abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="351fd-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="351fd-113">Vous devez être en mesure de créer une application dans Active Directory et d’affecter un rôle au principal du service.</span><span class="sxs-lookup"><span data-stu-id="351fd-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="351fd-114">Le moyen le plus simple de vous assurer que votre compte dispose des autorisations appropriées est d’utiliser le portail.</span><span class="sxs-lookup"><span data-stu-id="351fd-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="351fd-115">Consultez [Vérifier l’autorisation requise dans le portail](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="351fd-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="351fd-116">Créer un principal du service pour votre application</span><span class="sxs-lookup"><span data-stu-id="351fd-116">Create a service principal for your app</span></span>

<span data-ttu-id="351fd-117">Une fois que vous êtes connecté à votre compte Azure, vous pouvez créer le principal de service.</span><span class="sxs-lookup"><span data-stu-id="351fd-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="351fd-118">Vous devez identifier votre application déployée par l’une des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="351fd-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="351fd-119">Le nom unique de votre application déployée (par exemple, « MyDemoWebApp » dans les exemples suivants)</span><span class="sxs-lookup"><span data-stu-id="351fd-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="351fd-120">L’ID de l’application, le GUID unique associé à votre application, service ou objet déployé</span><span class="sxs-lookup"><span data-stu-id="351fd-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="351fd-121">Obtenir des informations sur votre application</span><span class="sxs-lookup"><span data-stu-id="351fd-121">Get information about your application</span></span>

<span data-ttu-id="351fd-122">Vous pouvez utiliser la cmdlet `Get-AzADApplication` pour obtenir des informations à propos de votre application.</span><span class="sxs-lookup"><span data-stu-id="351fd-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="351fd-123">Créer un principal du service pour votre application</span><span class="sxs-lookup"><span data-stu-id="351fd-123">Create a service principal for your application</span></span>

<span data-ttu-id="351fd-124">Utilisez l’applet de commande `New-AzADServicePrincipal` pour créer le principal du service.</span><span class="sxs-lookup"><span data-stu-id="351fd-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="351fd-125">À ce stade, vous pouvez directement utiliser la propriété `$servicePrincipal.Secret` en tant qu’argument pour `Connect-AzAccount` (voir « Connexion à l’aide du principal de service »), ou vous pouvez convertir `SecureString` en une chaîne de texte brut :</span><span class="sxs-lookup"><span data-stu-id="351fd-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="351fd-126">Se connecter en tant que principal du service</span><span class="sxs-lookup"><span data-stu-id="351fd-126">Sign in using the service principal</span></span>

<span data-ttu-id="351fd-127">Vous pouvez maintenant vous connecter en tant que nouveau principal du service pour votre application en utilisant la valeur `appId` que vous avez fournie et `password` qui a été</span><span class="sxs-lookup"><span data-stu-id="351fd-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="351fd-128">généré.</span><span class="sxs-lookup"><span data-stu-id="351fd-128">generated.</span></span> <span data-ttu-id="351fd-129">Vous allez également avoir besoin de l’ID de locataire pour le principal de service.</span><span class="sxs-lookup"><span data-stu-id="351fd-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="351fd-130">Votre ID de locataire s’affiche lorsque vous vous connectez à Azure avec vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="351fd-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="351fd-131">Pour vous connecter avec un principal de service, utilisez les commandes :</span><span class="sxs-lookup"><span data-stu-id="351fd-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="351fd-132">Lorsque la connexion aboutit, la sortie est semblable à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="351fd-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="351fd-133">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="351fd-133">Congratulations!</span></span> <span data-ttu-id="351fd-134">Vous pouvez utiliser ces informations d’identification pour exécuter votre application.</span><span class="sxs-lookup"><span data-stu-id="351fd-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="351fd-135">Ensuite, modifiez les autorisations du principal du service.</span><span class="sxs-lookup"><span data-stu-id="351fd-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="351fd-136">Gestion des rôles</span><span class="sxs-lookup"><span data-stu-id="351fd-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="351fd-137">Le contrôle d’accès en fonction du rôle (RBAC) dans Azure est un modèle utilisé pour définir et gérer les rôles des principaux de l’utilisateur et du service.</span><span class="sxs-lookup"><span data-stu-id="351fd-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="351fd-138">Les rôles sont associés à des ensembles d’autorisations, qui déterminent les ressources qu’un principal peut lire, écrire ou gérer, ou auxquelles il peut accéder.</span><span class="sxs-lookup"><span data-stu-id="351fd-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="351fd-139">Pour plus d’informations sur le contrôle d’accès en fonction du rôle (RBAC) et sur les différents rôles, consultez [Rôles intégrés pour le contrôle d’accès en fonction du rôle Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="351fd-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="351fd-140">Azure PowerShell fournit les applets de commande suivantes pour gérer les attributions de rôle :</span><span class="sxs-lookup"><span data-stu-id="351fd-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="351fd-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="351fd-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="351fd-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="351fd-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="351fd-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="351fd-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="351fd-144">Un principal du service a le rôle **Contributor** (Collaborateur) par défaut.</span><span class="sxs-lookup"><span data-stu-id="351fd-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="351fd-145">En raison des autorisations générales qu’il inclut, ce rôle n’est pas forcément le meilleur choix en fonction de l’étendue des interactions de votre application avec les services Azure.</span><span class="sxs-lookup"><span data-stu-id="351fd-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="351fd-146">Le rôle **Reader** (Lecteur) étant plus restrictif, il peut être un bon choix pour les applications en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="351fd-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="351fd-147">Vous pouvez afficher les détails des autorisations propres à chaque rôle ou créer des autorisations personnalisées par le biais du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="351fd-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="351fd-148">Dans cet exemple, nous ajoutons le rôle **Reader** à notre exemple précédent, et nous supprimons le rôle **Contributor** :</span><span class="sxs-lookup"><span data-stu-id="351fd-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="351fd-149">Pour afficher les rôles actuellement attribués :</span><span class="sxs-lookup"><span data-stu-id="351fd-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="351fd-150">Autres applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="351fd-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="351fd-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="351fd-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="351fd-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="351fd-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="351fd-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="351fd-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="351fd-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="351fd-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="351fd-155">Changer les informations d’identification du principal de sécurité</span><span class="sxs-lookup"><span data-stu-id="351fd-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="351fd-156">Nous vous recommandons de vérifier les autorisations et de mettre à jour le mot de passe régulièrement.</span><span class="sxs-lookup"><span data-stu-id="351fd-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="351fd-157">Vous pouvez également gérer et modifier les informations d’identification de sécurité à mesure que votre application évolue.</span><span class="sxs-lookup"><span data-stu-id="351fd-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="351fd-158">Par exemple, changez le mot de passe du principal du service en remplaçant le mot de passe existant par un nouveau mot de passe de votre choix.</span><span class="sxs-lookup"><span data-stu-id="351fd-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="351fd-159">Ajouter un nouveau mot de passe pour le principal du service</span><span class="sxs-lookup"><span data-stu-id="351fd-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="351fd-160">Obtenir la liste des informations d’identification pour le principal du service</span><span class="sxs-lookup"><span data-stu-id="351fd-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="351fd-161">Supprimer l’ancien mot de passe du principal du service</span><span class="sxs-lookup"><span data-stu-id="351fd-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="351fd-162">Vérifier la liste des informations d’identification pour le principal du service</span><span class="sxs-lookup"><span data-stu-id="351fd-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="351fd-163">Obtenir des informations sur le principal du service</span><span class="sxs-lookup"><span data-stu-id="351fd-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
