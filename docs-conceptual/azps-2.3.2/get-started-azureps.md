---
title: Prise en main de Microsoft Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c60036ba8be6282007aa34a0bb9c0d9e33197072
ms.sourcegitcommit: fd62a6376eef9b6ca76df766de1edcd7938c7a30
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2019
ms.locfileid: "67388935"
---
# <a name="get-started-with-azure-powershell"></a>Prise en main de Microsoft Azure PowerShell

Azure PowerShell est conçu pour gérer et administrer des ressources Azure en ligne de commande. Utilisez Azure PowerShell lorsque vous voulez créer des outils automatisés qui utilisent le modèle Azure Resource Manager.
Essayez-le dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou installez-le sur votre ordinateur local.

Cet article vous aide à bien démarrer avec Azure PowerShell et explique les concepts de base.

## <a name="install-or-run-in-azure-cloud-shell"></a>Installer ou exécuter dans Azure Cloud Shell

La façon la plus simple de démarrer avec Azure PowerShell est de l’essayer dans un environnement Azure Cloud Shell.
Pour que Cloud Shell soit opérationnel, consultez le [guide de démarrage rapide de PowerShell dans Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
Les fonctionnalités spécifiques à Windows ne sont pas disponibles car Cloud Shell exécute PowerShell 6 sur un conteneur Linux.

Lorsque vous êtes prêt à installer Azure PowerShell sur votre ordinateur local, suivez les instructions dans [Installer le module Azure PowerShell](install-az-ps.md).

## <a name="sign-in-to-azure"></a>Connexion à Azure

Connexion interactive avec la cmdlet `Connect-AzAccount`. Ignorez cette étape si vous utilisez Cloud Shell : Votre session Azure Cloud Shell est déjà authentifiée pour l’environnement, l’abonnement et l’abonné qui a démarré la session Cloud Shell.

```azurepowershell-interactive
Connect-AzAccount
```

Si vous vous trouvez dans une région en dehors des États-Unis, utilisez le paramètre `-Environment` pour vous connecter. Obtenez le nom de l’environnement de votre région à l’aide de la cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment). Par exemple, pour se connecter dans la région Azure China 21Vianet :

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Vous obtenez un jeton à utiliser sur https://microsoft.com/devicelogin. Ouvrez cette page dans votre navigateur et entrez le jeton, puis connectez-vous avec les informations d’identification de votre compte Azure et autorisez Azure PowerShell. 

Une fois connecté, vous verrez des informations indiquant lequel de vos abonnements Azure est actif. Si vous avez plusieurs abonnements Azure dans votre compte et souhaitez en sélectionner un autre, affichez vos abonnements disponibles avec l’applet de commande [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), puis utilisez l’applet de commande [Set-AzContext](/powershell/module/az.accounts/set-azcontext) avec votre ID d’abonnement.
Pour plus d’informations sur la gestion de vos abonnements Azure dans Azure PowerShell, consultez [Utiliser plusieurs abonnements Azure](manage-subscriptions-azureps.md).

Une fois connecté à un compte Azure, utilisez les cmdlets Azure PowerShell pour gérer les ressources dans votre abonnement, et y accéder. Pour en savoir plus sur le processus de connexion et les méthodes d’authentification, consultez l’article sur la [connexion avec Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Trouver des commandes

Les cmdlets Azure PowerShell suivent une convention d’affectation de noms standard pour PowerShell, `VERB-NOUN`. Le verbe décrit l’action (par exemple, `New`, `Get`, `Set`, `Remove`) et le nom décrit le type de ressource (par exemple `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). Les noms dans Azure PowerShell commencent toujours par le préfixe `Az`. Pour obtenir une liste complète des verbes standard, consulte [Verbes approuvés pour les commandes PowerShell](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

Il est utile de connaître les noms, verbes et les modules Azure PowerShell disponibles pour trouver des commandes avec la cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Par exemple, pour trouver toutes les commandes relatives à une machine virtuelle qui utilisent le verbe `Get` :

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Pour vous aider à trouver des commandes courantes, ce tableau répertorie les types de ressources, correspondant au module Azure PowerShell et le préfixe du nom à utiliser avec `Get-Command` :

| Type de ressource | Module Azure PowerShell | Préfixe de nom |
|---------------|-------------------------|----------------|
| [Groupe de ressources](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [Machines virtuelles](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [Comptes de stockage](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [Key Vault](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [Applications web](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [Bases de données SQL](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

Pour obtenir une liste complète des modules dans Azure PowerShell, consultez la [Liste des modules Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) sur GitHub.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Apprendre les concepts de base Azure PowerShell à l’aide des démarrages rapides et des didacticiels

Pour prendre en main Azure PowerShell, essayez un tutoriel approfondi pour configurer des machines et apprendre à les interroger.

> [!div class="nextstepaction"]
> [Créer des machines virtuelles avec Azure PowerShell](azureps-vm-tutorial.yml)

Il existe aussi des guides de démarrage rapide Azure PowerShell pour d’autres services Azure populaires :

* [Créez un compte de stockage](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Transférer des objets vers/à partir de Stockage Blob Azure](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Créer et récupérer des données secrètes depuis Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Créer un pare-feu et une base de données Azure SQL](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Exécuter un conteneur dans Azure Container Instances](/azure/container-instances/container-instances-quickstart-powershell)
* [Créer un groupe de machines virtuelles identiques](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Créer un équilibreur de charge standard](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Étapes suivantes

* [Se connecter avec Azure PowerShell](authenticate-azureps.md)
* [Gérer les abonnements Azure avec Azure PowerShell](manage-subscriptions-azureps.md)
* [Créer des principaux du service avec Azure PowerShell](create-azure-service-principal-azureps.md)
* Obtenir de l’aide de la communauté :
  * [Forum Azure sur MSDN (en anglais)](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](http://go.microsoft.com/fwlink/?LinkId=320213)
