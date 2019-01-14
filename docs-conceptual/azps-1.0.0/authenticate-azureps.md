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
ms.sourcegitcommit: b5635e291cdc324e66c936aa16c5772507fc78e8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/04/2019
ms.locfileid: "54055674"
---
# <a name="sign-in-with-azure-powershell"></a>Se connecter avec Azure PowerShell

Azure PowerShell prend en charge plusieurs méthodes d’authentification. Le moyen le plus simple pour commencer est d’utiliser [Azure Cloud Shell](/azure/cloud-shell/overview), qui vous connecte automatiquement. Avec une installation locale, vous pouvez vous connecter de manière interactive par le biais de votre navigateur. Lors de l’écriture de scripts pour l’automatisation, l’approche recommandée consiste à utiliser un [principal de service](create-azure-service-principal-azureps.md) avec les autorisations nécessaires. Lorsque vous limitez le plus possible les autorisations de connexion pour votre cas d’usage, vous assurez une meilleure protection de vos ressources Azure.

Une fois connecté, les commandes sont exécutées sur votre abonnement par défaut. Pour changer votre abonnement actif sur une session, utilisez l’applet de commande [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Pour changer l’abonnement par défaut utilisé lors de la connexion avec Azure PowerShell, utilisez [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).

> [!IMPORTANT]
>
> Vos informations d’identification sont partagées entre plusieurs sessions PowerShell tant que vous restez connecté.
> Pour plus d’informations, consultez l’article sur les [informations d’identification persistantes](context-persistence.md).

## <a name="sign-in-interactively"></a>Connexion interactive

Pour vous connecter de manière interactive, utilisez la cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Lorsque vous l’exécutez, cette cmdlet présente une chaîne de jeton. Pour vous connecter, copiez cette chaîne et collez-la dans https://microsoft.com/devicelogin dans un navigateur. Votre session PowerShell est ainsi authentifiée pour vous connecter à Azure.

## <a name="sign-in-with-credentials"></a>Se connecter avec des informations d’identification

Vous pouvez également vous connecter avec un objet `PSCredential` autorisé à se connecter à Azure.
Le moyen le plus simple d’obtenir un objet d’informations d’identification consiste à utiliser l’applet de commande [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential). Lorsqu’elle s’exécute, cette applet de commande vous demande une association nom d’utilisateur/mot de passe formant les informations d’identification.

> [!Note]
> Cette approche ne fonctionne pas avec les comptes Microsoft ou les comptes pour lesquels l’authentification à deux facteurs est activée.

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>Connexion avec un principal de service

Les principaux de service sont des comptes Azure non interactifs. À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory. En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.

Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).

Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzAccount`. Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service. Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Cette cmdlet présente une invite de commande pour l’ID d’utilisateur de principal du service et le mot de passe.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>Se connecter avec une identité managée 

Les identités managées sont une fonctionnalité d’Azure Active Directory. Les identités managées sont des principaux de service affectés aux ressources s’exécutant dans Azure. Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources. Les identités managées sont disponibles uniquement sur les ressources en cours d’exécution dans un cloud Azure.

Pour en savoir plus sur les identités managées des ressources Azure, consultez [Guide pratique pour utiliser des identités managées avec les ressources Azure sur une machine virtuelle Azure afin d’acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Se connecter avec un locataire non défini par défaut ou en tant que fournisseur de solutions cloud (CSP)

Si votre compte est associé à plusieurs locataires, l’utilisation du paramètre `-TenantId` est nécessaire au moment de la connexion. Ce paramètre fonctionne avec n’importe quelle autre méthode de connexion. Lors de la connexion, cette valeur de paramètre peut être l’ID d’objet Azure du locataire (ID de locataire) ou le nom de domaine complet du client.

Si vous êtes [fournisseur de solutions cloud (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), la valeur `-TenantId` **doit** être un ID de locataire.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Connexion à un autre cloud

Les services cloud Azure offrent des environnements conformes à la réglementation régionale sur la gestion des données.
Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.
Par exemple, si votre compte se trouve dans le cloud situé en Chine :

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```