---
title: Créer un principal du service Azure avec Azure PowerShell
description: Découvrez comment créer un principal du service pour votre application ou service avec Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 138047e510b7cb1f45abafe66c2b82ebc31c2cd9
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821579"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="9382f-104">Créer un principal du service Azure avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9382f-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="9382f-105">Si vous prévoyez de gérer votre application ou service avec Azure PowerShell, vous devez l’exécuter avec un principal du service Azure Active Directory (AAD) plutôt qu’avec vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="9382f-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="9382f-106">Cette rubrique vous explique pas à pas comment créer un principal de sécurité avec Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9382f-106">This topic steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="9382f-107">Vous pouvez également créer un principal du service par l’intermédiaire du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="9382f-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="9382f-108">Pour plus d’informations, consultez [Utiliser le portail pour créer une application et un principal du service Active Directory pouvant accéder aux ressources](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="9382f-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="9382f-109">Qu’est-ce qu’un « principal du service » ?</span><span class="sxs-lookup"><span data-stu-id="9382f-109">What is a 'service principal'?</span></span>

<span data-ttu-id="9382f-110">Un principal du service Azure est une identité de sécurité utilisée par les applications, les services et les outils d’automatisation créés par l’utilisateur pour accéder à des ressources Azure spécifiques.</span><span class="sxs-lookup"><span data-stu-id="9382f-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="9382f-111">Il équivaut un peu à une identité d’utilisateur (nom d’utilisateur et mot de passe ou certificat) avec un rôle spécifique et des autorisations étroitement contrôlées.</span><span class="sxs-lookup"><span data-stu-id="9382f-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="9382f-112">Il doit pouvoir effectuer uniquement des opérations spécifiques, contrairement à une identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9382f-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="9382f-113">Il améliore la sécurité si vous lui octroyez seulement le niveau d’autorisation minimal nécessaire pour effectuer ses tâches de gestion.</span><span class="sxs-lookup"><span data-stu-id="9382f-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="9382f-114">Vérifier votre propre niveau d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9382f-114">Verify your own permission level</span></span>

<span data-ttu-id="9382f-115">Tout d’abord, vous devez avoir les autorisations suffisantes dans votre annuaire Azure Active Directory et votre abonnement Azure.</span><span class="sxs-lookup"><span data-stu-id="9382f-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="9382f-116">Plus précisément, vous devez pouvoir créer une application dans l’annuaire Active Directory et affecter un rôle au principal du service.</span><span class="sxs-lookup"><span data-stu-id="9382f-116">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span>

<span data-ttu-id="9382f-117">Le moyen le plus simple pour vérifier que votre compte dispose des autorisations adéquates est d’utiliser le portail.</span><span class="sxs-lookup"><span data-stu-id="9382f-117">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="9382f-118">Consultez [Vérifier l’autorisation requise dans le portail](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="9382f-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="9382f-119">Créer un principal du service pour votre application</span><span class="sxs-lookup"><span data-stu-id="9382f-119">Create a service principal for your app</span></span>

<span data-ttu-id="9382f-120">Une fois que vous êtes connecté à votre compte Azure, vous pouvez créer le principal du service.</span><span class="sxs-lookup"><span data-stu-id="9382f-120">Once you are signed into your Azure account, you can create the service principal.</span></span> <span data-ttu-id="9382f-121">Vous devez identifier votre application déployée par l’une des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9382f-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="9382f-122">Le nom unique de votre application déployée (par exemple, « MyDemoWebApp » dans les exemples suivants)</span><span class="sxs-lookup"><span data-stu-id="9382f-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="9382f-123">L’ID de l’application, le GUID unique associé à votre application, service ou objet déployé</span><span class="sxs-lookup"><span data-stu-id="9382f-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="9382f-124">Obtenir des informations sur votre application</span><span class="sxs-lookup"><span data-stu-id="9382f-124">Get information about your application</span></span>

<span data-ttu-id="9382f-125">Vous pouvez utiliser l’applet de commande `Get-AzureRmADApplication` pour obtenir des informations sur votre application.</span><span class="sxs-lookup"><span data-stu-id="9382f-125">The `Get-AzureRmADApplication` cmdlet can be used to discover information about your application.</span></span>

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="9382f-126">Créer un principal du service pour votre application</span><span class="sxs-lookup"><span data-stu-id="9382f-126">Create a service principal for your application</span></span>

<span data-ttu-id="9382f-127">Utilisez l’applet de commande `New-AzureRmADServicePrincipal` pour créer le principal du service.</span><span class="sxs-lookup"><span data-stu-id="9382f-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="9382f-128">Obtenir des informations sur le principal du service</span><span class="sxs-lookup"><span data-stu-id="9382f-128">Get information about the service principal</span></span>

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="9382f-129">Se connecter en tant que principal du service</span><span class="sxs-lookup"><span data-stu-id="9382f-129">Sign in using the service principal</span></span>

<span data-ttu-id="9382f-130">Vous pouvez maintenant vous connecter en tant que nouveau principal du service pour votre application en utilisant les valeurs *appId* et *password* que vous avez fournies.</span><span class="sxs-lookup"><span data-stu-id="9382f-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="9382f-131">Vous devez fournir l’ID de locataire (TenantId) pour votre compte.</span><span class="sxs-lookup"><span data-stu-id="9382f-131">You need to supply the Tenant Id for your account.</span></span> <span data-ttu-id="9382f-132">Cet ID s’affiche quand vous vous connectez à Azure avec vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="9382f-132">Your Tenant Id is displayed when you sign into Azure with your personal credentials.</span></span>

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="9382f-133">Exécutez cette commande à partir d’une nouvelle session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9382f-133">Run this command from a new PowerShell session.</span></span> <span data-ttu-id="9382f-134">Une fois que vous êtes connecté, vous voyez un message similaire à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="9382f-134">After a successfully signing on you see output something like this:</span></span>

```
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="9382f-135">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="9382f-135">Congratulations!</span></span> <span data-ttu-id="9382f-136">Vous pouvez utiliser ces informations d’identification pour exécuter votre application.</span><span class="sxs-lookup"><span data-stu-id="9382f-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="9382f-137">Ensuite, modifiez les autorisations du principal du service.</span><span class="sxs-lookup"><span data-stu-id="9382f-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="9382f-138">Gestion des rôles</span><span class="sxs-lookup"><span data-stu-id="9382f-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="9382f-139">Le contrôle d’accès en fonction du rôle (RBAC) dans Azure est un modèle utilisé pour définir et gérer les rôles des principaux de l’utilisateur et du service.</span><span class="sxs-lookup"><span data-stu-id="9382f-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="9382f-140">Les rôles sont associés à des ensembles d’autorisations, qui déterminent les ressources qu’un principal peut lire, écrire ou gérer, ou auxquelles il peut accéder.</span><span class="sxs-lookup"><span data-stu-id="9382f-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="9382f-141">Pour plus d’informations sur le contrôle d’accès en fonction du rôle et sur les différents rôles, consultez [Rôles intégrés pour le contrôle d’accès en fonction du rôle Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="9382f-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="9382f-142">Azure PowerShell fournit les applets de commande suivantes pour gérer les attributions de rôle :</span><span class="sxs-lookup"><span data-stu-id="9382f-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="9382f-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9382f-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="9382f-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9382f-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="9382f-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9382f-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="9382f-146">Un principal du service a le rôle **Contributor** (Collaborateur) par défaut.</span><span class="sxs-lookup"><span data-stu-id="9382f-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="9382f-147">En raison des autorisations générales qu’il inclut, ce rôle n’est pas forcément le meilleur choix en fonction de l’étendue des interactions de votre application avec les services Azure.</span><span class="sxs-lookup"><span data-stu-id="9382f-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="9382f-148">Le rôle **Reader** (Lecteur) étant plus restrictif, il peut être un bon choix pour les applications en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9382f-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="9382f-149">Vous pouvez afficher les détails des autorisations propres à chaque rôle ou créer des autorisations personnalisées par le biais du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="9382f-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="9382f-150">Dans cet exemple, nous ajoutons le rôle **Reader** à notre exemple précédent, et nous supprimons le rôle **Contributor** :</span><span class="sxs-lookup"><span data-stu-id="9382f-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="9382f-151">Pour afficher les rôles actuellement attribués :</span><span class="sxs-lookup"><span data-stu-id="9382f-151">To view the current roles assigned:</span></span>

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="9382f-152">Autres applets de commande Azure PowerShell pour la gestion des rôles :</span><span class="sxs-lookup"><span data-stu-id="9382f-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="9382f-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9382f-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="9382f-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9382f-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="9382f-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9382f-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="9382f-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9382f-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="9382f-157">Changer les informations d’identification du principal de sécurité</span><span class="sxs-lookup"><span data-stu-id="9382f-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="9382f-158">Nous vous recommandons de vérifier les autorisations et de mettre à jour le mot de passe régulièrement.</span><span class="sxs-lookup"><span data-stu-id="9382f-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="9382f-159">Vous pouvez également gérer et modifier les informations d’identification de sécurité à mesure que votre application évolue.</span><span class="sxs-lookup"><span data-stu-id="9382f-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="9382f-160">Par exemple, changez le mot de passe du principal du service en remplaçant le mot de passe existant par un nouveau mot de passe de votre choix.</span><span class="sxs-lookup"><span data-stu-id="9382f-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="9382f-161">Ajouter un nouveau mot de passe pour le principal du service</span><span class="sxs-lookup"><span data-stu-id="9382f-161">Add a new password for the service principal</span></span>

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="9382f-162">Obtenir la liste des informations d’identification pour le principal du service</span><span class="sxs-lookup"><span data-stu-id="9382f-162">Get a list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="9382f-163">Supprimer l’ancien mot de passe du principal du service</span><span class="sxs-lookup"><span data-stu-id="9382f-163">Remove the old password from the service principal</span></span>

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="9382f-164">Vérifier la liste des informations d’identification pour le principal du service</span><span class="sxs-lookup"><span data-stu-id="9382f-164">Verify the list of credentials for the service principal</span></span>

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
