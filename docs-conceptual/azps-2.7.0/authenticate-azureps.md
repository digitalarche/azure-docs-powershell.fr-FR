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
ms.sourcegitcommit: 92722d603b60dc769660e7517da60110133d9959
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71226352"
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

> [!IMPORTANT]
>
> Les autorisations obtenues à l’aide des informations d’identification Nom d’utilisateur/Mot de passe ont été supprimées d’Azure PowerShell en raison des modifications apportées à l’implémentation des autorisations Active Directory ainsi qu’à l’évolution des problèmes de sécurité.
> Si vous utilisez ce type d’autorisations à des fins d’automatisation, [créez un principal de service](create-azure-service-principal-azureps.md).

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a>Se connecter à un principal de service <a name="sp-signin"/>

Les principaux de service sont des comptes Azure non interactifs. À l’instar des autres comptes d’utilisateur, leurs autorisations sont gérées avec Azure Active Directory. En accordant uniquement les autorisations nécessaires à un principal de service, vous vous assurez que vos scripts d’automatisation restent sécurisés.

Pour savoir comment créer un principal de service à utiliser avec Azure PowerShell, voir [Créer un principal du service Azure avec Azure PowerShell](create-azure-service-principal-azureps.md).

Pour se connecter avec un principal de service, utilisez l’argument `-ServicePrincipal` avec l’applet de commande `Connect-AzAccount`. Vous aurez également besoin de l’ID d’application du principal de service, des informations d’identification de connexion ainsi que de l’ID du locataire associé au principal du service. La façon dont vous vous connectez à un principal du service varie selon que celui-ci a été configuré pour l’authentification par mot de passe ou pour l’authentification par certificat.

### <a name="password-based-authentication"></a>L’authentification basée sur un mot de passe

Pour obtenir les informations d’identification du principal de service en tant qu’objet approprié, utilisez la cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Cette applet de commande affichera une invite pour entrer un nom d’utilisateur et un mot de passe. Pour le nom d’utilisateur, utilisez l’ID du principal de service.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Pour les scénarios d’automatisation, vous devez créer des informations d’identification à partir d’un nom d’utilisateur et d’une chaîne sécurisée :

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Lorsque vous automatisez les connexions au principal de service, utilisez les bonnes pratiques relatives au stockage des mots de passe.

### <a name="certificate-based-authentication"></a>Authentification par certificat

L’authentification par certificat nécessite qu’Azure PowerShell puisse récupérer des informations à partir d’un magasin de certificats local en se basant sur l’empreinte numérique du certificat.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Quand vous utilisez un principal de service au lieu d’une application inscrite, ajoutez l’argument `-ServicePrincipal` et fournissez l’ID du principal de service comme valeur du paramètre `-ApplicationId`.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

Dans PowerShell 5.1, le magasin de certificats peut être géré et inspecté avec le module [PKI](/powershell/module/pkiclient). Pour PowerShell Core 6.x et ultérieur, le processus est plus complexe. Les scripts suivants montrent comment importer un certificat existant dans le magasin de certificats qui est accessible via PowerShell.

#### <a name="import-a-certificate-in-powershell-51"></a>Importer un certificat dans PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Importer un certificat dans PowerShell Core 6.x et ultérieur

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

## <a name="sign-in-using-a-managed-identity"></a>Se connecter avec une identité managée

Les identités managées sont une fonctionnalité d’Azure Active Directory. Les identités managées sont des principaux de service affectés aux ressources s’exécutant dans Azure. Vous pouvez utiliser un principal de service d’identité managée pour vous connecter et obtenir un jeton d’accès réservé à l’application afin d’accéder à d’autres ressources. Les identités managées sont disponibles uniquement sur les ressources en cours d’exécution dans un cloud Azure.

Pour en savoir plus sur les identités managées des ressources Azure, consultez [Guide pratique pour utiliser des identités managées avec les ressources Azure sur une machine virtuelle Azure afin d’acquérir un jeton d’accès](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Se connecter avec un locataire non défini par défaut ou en tant que fournisseur de solutions cloud (CSP)

Si votre compte est associé à plusieurs locataires, l’utilisation du paramètre `-Tenant` est nécessaire au moment de la connexion. Ce paramètre fonctionne avec n’importe quelle méthode de connexion. Lors de la connexion, cette valeur de paramètre peut être l’ID d’objet Azure du locataire (ID de locataire) ou le nom de domaine complet du client.

Si vous êtes [fournisseur de solutions cloud (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), la valeur `-Tenant` **doit** être un ID de locataire.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Connexion à un autre cloud

Les services cloud Azure offrent des environnements conformes à la réglementation régionale sur la gestion des données.
Pour les comptes situés dans un cloud régional, définissez l’environnement lorsque vous vous connectez avec l’argument `-Environment`.
Ce paramètre fonctionne avec n’importe quelle méthode de connexion. Par exemple, si votre compte se trouve dans le cloud situé en Chine :

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Pour obtenir une liste des environnements disponibles, utilisez la commande suivante :

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
