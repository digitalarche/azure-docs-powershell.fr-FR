---
title: Prise en main de Microsoft Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 0c3b749cb2ac7f11dacafca76b65944f523f727d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63068963"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="5d88a-102">Prise en main de Microsoft Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d88a-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="5d88a-103">Azure PowerShell est conçu pour gérer et administrer des ressources Azure en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="5d88a-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="5d88a-104">Utilisez Azure PowerShell lorsque vous voulez créer des outils automatisés qui utilisent le modèle Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5d88a-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="5d88a-105">Essayez-le dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou installez-le sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="5d88a-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="5d88a-106">Cet article vous aide à bien démarrer avec Azure PowerShell et explique les concepts de base.</span><span class="sxs-lookup"><span data-stu-id="5d88a-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="5d88a-107">Installer ou exécuter dans Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="5d88a-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="5d88a-108">La façon la plus simple de démarrer avec Azure PowerShell est de l’essayer dans un environnement Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="5d88a-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="5d88a-109">Pour que Cloud Shell soit opérationnel, consultez le [guide de démarrage rapide de PowerShell dans Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="5d88a-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="5d88a-110">Les fonctionnalités spécifiques à Windows ne sont pas disponibles car Cloud Shell exécute PowerShell 6 sur un conteneur Linux.</span><span class="sxs-lookup"><span data-stu-id="5d88a-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="5d88a-111">Lorsque vous êtes prêt à installer Azure PowerShell sur votre ordinateur local, suivez les instructions dans [Installer le module Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5d88a-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="5d88a-112">Connexion à Azure</span><span class="sxs-lookup"><span data-stu-id="5d88a-112">Sign in to Azure</span></span>

<span data-ttu-id="5d88a-113">Connexion interactive avec la cmdlet `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="5d88a-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="5d88a-114">Ignorez cette étape si vous utilisez Cloud Shell : Votre session Azure Cloud Shell est déjà authentifiée pour l’environnement, l’abonnement et l’abonné qui a démarré la session Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="5d88a-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="5d88a-115">Si vous vous trouvez dans une région en dehors des États-Unis, utilisez le paramètre `-Environment` pour vous connecter.</span><span class="sxs-lookup"><span data-stu-id="5d88a-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="5d88a-116">Obtenez le nom de l’environnement de votre région à l’aide de la cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="5d88a-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="5d88a-117">Par exemple, pour se connecter dans la région Azure China 21Vianet :</span><span class="sxs-lookup"><span data-stu-id="5d88a-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="5d88a-118">Vous obtenez un jeton à utiliser sur https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="5d88a-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="5d88a-119">Ouvrez cette page dans votre navigateur et entrez le jeton, puis connectez-vous avec les informations d’identification de votre compte Azure et autorisez Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d88a-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="5d88a-120">Une fois connecté, vous verrez des informations indiquant lequel de vos abonnements Azure est actif.</span><span class="sxs-lookup"><span data-stu-id="5d88a-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="5d88a-121">Si vous avez plusieurs abonnements Azure dans votre compte et souhaitez en sélectionner un autre, affichez vos abonnements disponibles avec l’applet de commande [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), puis utilisez l’applet de commande [Set-AzContext](/powershell/module/az.accounts/set-azcontext) avec votre ID d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d88a-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="5d88a-122">Pour plus d’informations sur la gestion de vos abonnements Azure dans Azure PowerShell, consultez [Utiliser plusieurs abonnements Azure](manage-subscriptions-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5d88a-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="5d88a-123">Une fois connecté à un compte Azure, utilisez les cmdlets Azure PowerShell pour gérer les ressources dans votre abonnement, et y accéder.</span><span class="sxs-lookup"><span data-stu-id="5d88a-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="5d88a-124">Pour en savoir plus sur le processus de connexion et les méthodes d’authentification, consultez l’article sur la [connexion avec Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5d88a-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="5d88a-125">Trouver des commandes</span><span class="sxs-lookup"><span data-stu-id="5d88a-125">Find commands</span></span>

<span data-ttu-id="5d88a-126">Les cmdlets Azure PowerShell suivent une convention d’affectation de noms standard pour PowerShell, `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="5d88a-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="5d88a-127">Le verbe décrit l’action (par exemple, `Create`, `Get`, `Set`, `Delete`) et le nom décrit le type de ressource (par exemple `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="5d88a-127">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="5d88a-128">Les noms dans Azure PowerShell commencent toujours par le préfixe `Az`.</span><span class="sxs-lookup"><span data-stu-id="5d88a-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="5d88a-129">Pour obtenir une liste complète des verbes standard, consulte [Verbes approuvés pour les commandes PowerShell](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span><span class="sxs-lookup"><span data-stu-id="5d88a-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="5d88a-130">Il est utile de connaître les noms, verbes et les modules Azure PowerShell disponibles pour trouver des commandes avec la cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="5d88a-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="5d88a-131">Par exemple, pour trouver toutes les commandes relatives à une machine virtuelle qui utilisent le verbe `Get` :</span><span class="sxs-lookup"><span data-stu-id="5d88a-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="5d88a-132">Pour vous aider à trouver des commandes courantes, ce tableau répertorie les types de ressources, correspondant au module Azure PowerShell et le préfixe du nom à utiliser avec `Get-Command` :</span><span class="sxs-lookup"><span data-stu-id="5d88a-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="5d88a-133">Type de ressource</span><span class="sxs-lookup"><span data-stu-id="5d88a-133">Resource type</span></span> | <span data-ttu-id="5d88a-134">Module Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d88a-134">Azure PowerShell module</span></span> | <span data-ttu-id="5d88a-135">Préfixe de nom</span><span class="sxs-lookup"><span data-stu-id="5d88a-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="5d88a-136">Groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="5d88a-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="5d88a-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5d88a-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="5d88a-138">Machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="5d88a-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="5d88a-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5d88a-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="5d88a-140">Comptes de stockage</span><span class="sxs-lookup"><span data-stu-id="5d88a-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="5d88a-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5d88a-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="5d88a-142">Key Vault</span><span class="sxs-lookup"><span data-stu-id="5d88a-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="5d88a-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5d88a-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="5d88a-144">Applications web</span><span class="sxs-lookup"><span data-stu-id="5d88a-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="5d88a-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5d88a-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="5d88a-146">Bases de données SQL</span><span class="sxs-lookup"><span data-stu-id="5d88a-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="5d88a-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5d88a-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="5d88a-148">Pour obtenir une liste complète des modules dans Azure PowerShell, consultez la [Liste des modules Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="5d88a-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="5d88a-149">Apprendre les concepts de base Azure PowerShell à l’aide des démarrages rapides et des didacticiels</span><span class="sxs-lookup"><span data-stu-id="5d88a-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="5d88a-150">Pour prendre en main Azure PowerShell, essayez un tutoriel approfondi pour configurer des machines et apprendre à les interroger.</span><span class="sxs-lookup"><span data-stu-id="5d88a-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="5d88a-151">Créer des machines virtuelles avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d88a-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="5d88a-152">Il existe aussi des guides de démarrage rapide Azure PowerShell pour d’autres services Azure populaires :</span><span class="sxs-lookup"><span data-stu-id="5d88a-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="5d88a-153">Créez un compte de stockage</span><span class="sxs-lookup"><span data-stu-id="5d88a-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="5d88a-154">Transférer des objets vers/à partir de Stockage Blob Azure</span><span class="sxs-lookup"><span data-stu-id="5d88a-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="5d88a-155">Créer et récupérer des données secrètes depuis Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="5d88a-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="5d88a-156">Créer un pare-feu et une base de données SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5d88a-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="5d88a-157">Exécuter un conteneur dans Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="5d88a-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="5d88a-158">Créer un groupe de machines virtuelles identiques</span><span class="sxs-lookup"><span data-stu-id="5d88a-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="5d88a-159">Créer un équilibreur de charge standard</span><span class="sxs-lookup"><span data-stu-id="5d88a-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="5d88a-160">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5d88a-160">Next steps</span></span>

* [<span data-ttu-id="5d88a-161">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d88a-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="5d88a-162">Gérer les abonnements Azure avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d88a-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="5d88a-163">Créer des principaux du service avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d88a-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="5d88a-164">Obtenir de l’aide de la communauté :</span><span class="sxs-lookup"><span data-stu-id="5d88a-164">Get help from the community:</span></span>
  * [<span data-ttu-id="5d88a-165">Forum Azure sur MSDN (en anglais)</span><span class="sxs-lookup"><span data-stu-id="5d88a-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="5d88a-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="5d88a-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
