---
title: <span data-ttu-id="0b249-101">Installer et configurer le module Azure PowerShell Service Management | Microsoft Docs</span><span class="sxs-lookup"><span data-stu-id="0b249-101">Install and configure the Azure PowerShell Service Management module | Microsoft Docs</span></span>
description: "<span data-ttu-id=\"0b249-102\">Comment installer et configurer Azure PowerShell pour la première utilisation.</span><span class=\"sxs-lookup\"><span data-stu-id=\"0b249-102\">How to install and configure Azure PowerShell for first time use.</span></span>"
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: c51c727c1cb022eca59f819c7f24d8e058c677da
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="0b249-103">Installer le module Azure PowerShell Service Management</span><span class="sxs-lookup"><span data-stu-id="0b249-103">Installing the Azure PowerShell Service Management module</span></span>
<a id="installing-the-azure-powershell-service-management-module" class="xliff"></a>

<span data-ttu-id="0b249-104">La méthode recommandée est d’installer Azure PowerShell à partir de [PowerShell Gallery](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="0b249-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <span data-ttu-id="0b249-105">Étape 1 : Installer PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="0b249-105">Step 1: Install PowerShellGet</span></span>
<a id="step-1-install-powershellget" class="xliff"></a>

<span data-ttu-id="0b249-106">Pour installer des éléments à partir de PowerShell Gallery, vous avez besoin du module PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0b249-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="0b249-107">Vérifiez que votre système a la version appropriée de PowerShellGet et qu’il présente toute la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="0b249-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="0b249-108">Exécutez la commande suivante pour vérifier que PowerShellGet est installé sur votre système.</span><span class="sxs-lookup"><span data-stu-id="0b249-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="0b249-109">Vous obtenez normalement un résultat similaire à la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="0b249-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="0b249-110">Si PowerShellGet n’est pas installé, consultez [Comment obtenir PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="0b249-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).</span></span>

## <span data-ttu-id="0b249-111">Étape 2 : Installer Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0b249-111">Step 2: Install Azure PowerShell</span></span>
<a id="step-2-install-azure-powershell" class="xliff"></a>

<span data-ttu-id="0b249-112">Exécutez la commande suivante à partir de la console Windows PowerShell en tant qu’administrateur :</span><span class="sxs-lookup"><span data-stu-id="0b249-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="0b249-113">Le module Azure est un module cumulatif pour les applets de commande Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="0b249-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="0b249-114">Quand vous installez ce module, les autres modules Azure qui n’ont pas encore été installés sont téléchargés et installés à partir de PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="0b249-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="0b249-115">Le module Azure Service Management partage des dépendances avec les modules Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="0b249-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="0b249-116">Si vous avez installé ces modules, vous devez ajouter le paramètre `-AllowClobber` à la commande install.</span><span class="sxs-lookup"><span data-stu-id="0b249-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="0b249-117">Cela garantit la mise à jour des dépendances partagées existantes.</span><span class="sxs-lookup"><span data-stu-id="0b249-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="0b249-118">Sans ce paramètre, l’installation du module échoue.</span><span class="sxs-lookup"><span data-stu-id="0b249-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="0b249-119">Après avoir installé ce module, vous pouvez l’importer en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0b249-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <span data-ttu-id="0b249-120">Pour utiliser les applets de commande</span><span class="sxs-lookup"><span data-stu-id="0b249-120">To use the cmdlets</span></span>
<a id="to-use-the-cmdlets" class="xliff"></a>

<span data-ttu-id="0b249-121">Avant de commencer à utiliser les applets de commande Azure Service Management, connectez-vous à votre compte Azure.</span><span class="sxs-lookup"><span data-stu-id="0b249-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="0b249-122">Pour vous connecter à votre compte, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0b249-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="0b249-123">Une fois que vous êtes connecté à Azure, Azure PowerShell crée un contexte pour la session.</span><span class="sxs-lookup"><span data-stu-id="0b249-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="0b249-124">Ce contexte contient l’environnement, le compte, le locataire et l’abonnement Azure PowerShell qui seront utilisés pour toutes les applets de commande dans cette session.</span><span class="sxs-lookup"><span data-stu-id="0b249-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="0b249-125">Vous êtes maintenant prêt à utiliser les modules ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0b249-125">Now you are ready to use the modules below.</span></span>

## <span data-ttu-id="0b249-126">Applets de commande Azure Service Management</span><span class="sxs-lookup"><span data-stu-id="0b249-126">Azure Service Management cmdlets</span></span>
<a id="azure-service-management-cmdlets" class="xliff"></a>

<span data-ttu-id="0b249-127">Les modules Azure PowerShell sont fréquemment mis à jour.</span><span class="sxs-lookup"><span data-stu-id="0b249-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="0b249-128">Si vous remarquez que l’aide en ligne des applets de commande comporte des applets de commande ou des paramètres qui ne sont pas dans votre module, téléchargez et installez la toute dernière version du module.</span><span class="sxs-lookup"><span data-stu-id="0b249-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="0b249-129">Pour déterminer la version du module que vous utilisez, tapez `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="0b249-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="0b249-130">Pour obtenir des exemples de scripts qui peuvent vous aider à automatiser certaines tâches courantes dans Azure, consultez le [Centre de scripts Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="0b249-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="0b249-131">Pour obtenir des informations générales sur l’installation, l’apprentissage, l’utilisation et la personnalisation de Windows PowerShell, consultez [Écriture de scripts avec Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="0b249-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>
