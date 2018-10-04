---
title: Se connecter avec Azure PowerShell
description: Se connecter avec Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 71a2554052f5a25ea86fe44b6dcf5d9343c81f3e
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "47424681"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="8d081-103">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d081-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="8d081-104">Azure PowerShell prend en charge plusieurs méthodes de connexion.</span><span class="sxs-lookup"><span data-stu-id="8d081-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="8d081-105">La méthode la plus simple est de vous connecter de manière interactive à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8d081-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="8d081-106">Connexion interactive</span><span class="sxs-lookup"><span data-stu-id="8d081-106">Interactive log in</span></span>

1. <span data-ttu-id="8d081-107">Saisissez `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="8d081-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="8d081-108">Une boîte de dialogue s’affiche pour vous demander vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="8d081-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="8d081-109">Entrez l’adresse de messagerie et le mot de passe associés à votre compte.</span><span class="sxs-lookup"><span data-stu-id="8d081-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="8d081-110">Azure authentifie et enregistre les informations d’identification, puis ferme la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8d081-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="8d081-111">Connexion avec un principal du service</span><span class="sxs-lookup"><span data-stu-id="8d081-111">Log in with a service principal</span></span>

<span data-ttu-id="8d081-112">Les principaux du service offrent un moyen de créer des comptes non interactifs que vous pouvez ensuite utiliser pour manipuler les ressources.</span><span class="sxs-lookup"><span data-stu-id="8d081-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="8d081-113">Les principaux du service sont comme des comptes d’utilisateur auxquels vous pouvez appliquer des règles à l’aide d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d081-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="8d081-114">En accordant les autorisations minimales nécessaires à un principal du service, vous sécurisez encore davantage vos scripts d’automatisation.</span><span class="sxs-lookup"><span data-stu-id="8d081-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="8d081-115">Si vous n’avez pas encore de principal du service, [créez-en un](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8d081-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="8d081-116">Connectez-vous avec le principal du service.</span><span class="sxs-lookup"><span data-stu-id="8d081-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="8d081-117">Pour obtenir votre ID de locataire (TenantId), connectez-vous de manière interactive, puis recherchez la valeur TenantId dans votre abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d081-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="8d081-118">Connectez-vous en utilisant des identités managées pour les ressources Azure</span><span class="sxs-lookup"><span data-stu-id="8d081-118">Log in using managed identities for Azure resources</span></span>

<span data-ttu-id="8d081-119">Identités managées pour ressources Azure est une fonctionnalité d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d081-119">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="8d081-120">Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="8d081-120">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="8d081-121">Pour plus d’informations concernant les identités managées pour les ressources Azure, voir [Guide pratique d’utilisation d’identités managées pour ressources Azure sur une machine virtuelle Azure pour acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="8d081-121">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="8d081-122">Connexion à un autre cloud</span><span class="sxs-lookup"><span data-stu-id="8d081-122">Log in to another Cloud</span></span>

<span data-ttu-id="8d081-123">Les services de cloud computing d’Azure offrent différents environnements conformes aux règles de traitement des données de nombreux gouvernements.</span><span class="sxs-lookup"><span data-stu-id="8d081-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="8d081-124">Si votre compte Azure se trouve dans un des clouds gouvernementaux, vous devez spécifier cet environnement lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="8d081-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="8d081-125">Par exemple, si votre compte se trouve dans le cloud de la Chine, connectez-vous à l’aide la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8d081-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="8d081-126">Pour obtenir la liste d’environnements disponibles, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="8d081-126">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="8d081-127">En savoir plus sur la gestion de l’accès en fonction du rôle dans Azure</span><span class="sxs-lookup"><span data-stu-id="8d081-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="8d081-128">Pour plus d’informations sur la gestion de l’authentification et de l’abonnement dans Azure, consultez la page [Gérer des comptes, des abonnements et des rôles d’administrateur](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="8d081-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="8d081-129">Applets de commande Azure PowerShell pour la gestion des rôles</span><span class="sxs-lookup"><span data-stu-id="8d081-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="8d081-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8d081-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="8d081-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8d081-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="8d081-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8d081-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="8d081-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8d081-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="8d081-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8d081-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="8d081-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8d081-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="8d081-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="8d081-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
