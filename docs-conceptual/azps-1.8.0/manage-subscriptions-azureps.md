---
title: Gérer les abonnements Azure avec Azure PowerShell
description: Gérer les abonnements Azure avec Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807524"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="2c17c-103">Utilisez plusieurs abonnements Azure</span><span class="sxs-lookup"><span data-stu-id="2c17c-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="2c17c-104">La plupart des utilisateurs Azure ne possèdent qu’un seul abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c17c-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="2c17c-105">Toutefois, si vous faites partie de plus d’une organisation, ou si votre organisation a divisé l’accès à certaines ressources dans les regroupements, vous pouvez avoir plusieurs abonnements dans Azure.</span><span class="sxs-lookup"><span data-stu-id="2c17c-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="2c17c-106">L’interface CLI prend en charge la sélection d’un abonnement à la fois au niveau global et par commande.</span><span class="sxs-lookup"><span data-stu-id="2c17c-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="2c17c-107">Pour plus d’informations sur les abonnements, la facturation et la gestion des coûts, consultez la [documentation sur la facturation et la gestion des coûts](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="2c17c-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="2c17c-108">Locataires, utilisateurs et abonnements</span><span class="sxs-lookup"><span data-stu-id="2c17c-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="2c17c-109">La différence entre les locataires, les utilisateurs et les abonnements dans Azure peut prêter à confusion.</span><span class="sxs-lookup"><span data-stu-id="2c17c-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="2c17c-110">Un _locataire_ correspond à l’entité d’Azure Active Directory qui inclut une organisation complète.</span><span class="sxs-lookup"><span data-stu-id="2c17c-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="2c17c-111">Ce locataire possède au moins un _abonnement_ et _utilisateur_.</span><span class="sxs-lookup"><span data-stu-id="2c17c-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="2c17c-112">Un utilisateur est un individu qui n’est associé qu’à un seul locataire, c’est-à-dire à l’organisation auquel il appartient.</span><span class="sxs-lookup"><span data-stu-id="2c17c-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="2c17c-113">Les utilisateurs correspondent aux comptes qui se connectent à Azure afin de configurer, de gérer et d’utiliser des ressources.</span><span class="sxs-lookup"><span data-stu-id="2c17c-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="2c17c-114">Un utilisateur peut avoir accès à plusieurs _abonnements_, qui sont les contrats avec Microsoft pour utiliser les services de cloud, y compris Azure.</span><span class="sxs-lookup"><span data-stu-id="2c17c-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="2c17c-115">Chaque ressource est associée à un abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c17c-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="2c17c-116">Pour en savoir plus sur les différences entre les locataires, les utilisateurs et les abonnements, consultez le [Dictionnaire de terminologie cloud Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="2c17c-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="2c17c-117">Pour savoir comment ajouter un nouvel abonnement à votre locataire Azure Active Directory, consultez [Comment ajouter un abonnement Azure à Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="2c17c-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="2c17c-118">Pour savoir comment se connecter à un client en particulier, consultez la rubrique [Se connecter avec Azure PowerShell](/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="2c17c-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="2c17c-119">Modifier l’abonnement actif</span><span class="sxs-lookup"><span data-stu-id="2c17c-119">Change the active subscription</span></span>

<span data-ttu-id="2c17c-120">Dans Azure PowerShell, l’accès des ressources pour un abonnement requiert une modification de l’abonnement associé à votre session Azure.</span><span class="sxs-lookup"><span data-stu-id="2c17c-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="2c17c-121">Pour cela, vous devez modifier le contexte de la session active et les informations concernant les clients, les abonnements et les utilisateurs sur lesquelles sont exécutées les applets de commande.</span><span class="sxs-lookup"><span data-stu-id="2c17c-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="2c17c-122">Pour modifier des abonnements, un objet de contexte Azure PowerShell doit tout d’abord être récupéré avec [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) et ensuite le contexte actuel doit être modifié avec [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="2c17c-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="2c17c-123">L’exemple suivant montre comment obtenir un abonnement dans le client actuellement actif et définissez-le comme session active :</span><span class="sxs-lookup"><span data-stu-id="2c17c-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="2c17c-124">Pour en savoir plus sur les contextes Azure PowerShell, notamment comment les enregistrer et basculer rapidement entre eux pour travailler avec plusieurs abonnements facilement, consultez la section [Persistance des informations d’identification avec les contextes Azure PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="2c17c-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
