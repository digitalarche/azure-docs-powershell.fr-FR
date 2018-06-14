---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854611"
---
# <a name="release-notes"></a><span data-ttu-id="abd1e-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="abd1e-103">Release notes</span></span>

<span data-ttu-id="abd1e-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="abd1e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="abd1e-105">Version 2.2.0</span><span class="sxs-lookup"><span data-stu-id="abd1e-105">Version 2.2.0</span></span>
* <span data-ttu-id="abd1e-106">Calcul</span><span class="sxs-lookup"><span data-stu-id="abd1e-106">Compute</span></span>
  - <span data-ttu-id="abd1e-107">Ajout de la prise en charge de l’interrogation de l’état de chiffrement par l’extension AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="abd1e-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="abd1e-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="abd1e-108">DataFactory</span></span>
  - <span data-ttu-id="abd1e-109">Ajout d’une nouvelle applet de commande pour répertorier les fenêtres d’activité</span><span class="sxs-lookup"><span data-stu-id="abd1e-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="abd1e-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="abd1e-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="abd1e-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="abd1e-111">DataLake</span></span>
  - <span data-ttu-id="abd1e-112">Changement du paramètre `Host` en `DatabaseHost` et ajout d’un alias à `Host`</span><span class="sxs-lookup"><span data-stu-id="abd1e-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="abd1e-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="abd1e-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="abd1e-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="abd1e-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="abd1e-115">Ajout de la prise en charge de la suppression de la liste de contrôle d’accès et de la liste de contrôle d’accès par défaut</span><span class="sxs-lookup"><span data-stu-id="abd1e-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="abd1e-116">Ajout de la prise en charge de l’obtention et de la définition d’autorisations sans nom sur des fichiers et des dossiers</span><span class="sxs-lookup"><span data-stu-id="abd1e-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="abd1e-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="abd1e-117">KeyVault</span></span>
  - <span data-ttu-id="abd1e-118">Ajout de la prise en charge des certificats</span><span class="sxs-lookup"><span data-stu-id="abd1e-118">Add support for certificates</span></span>
    + <span data-ttu-id="abd1e-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="abd1e-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="abd1e-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="abd1e-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="abd1e-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="abd1e-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="abd1e-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="abd1e-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="abd1e-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="abd1e-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="abd1e-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="abd1e-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="abd1e-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="abd1e-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="abd1e-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="abd1e-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="abd1e-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="abd1e-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="abd1e-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="abd1e-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="abd1e-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="abd1e-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="abd1e-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="abd1e-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="abd1e-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="abd1e-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="abd1e-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="abd1e-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="abd1e-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="abd1e-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="abd1e-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="abd1e-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="abd1e-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="abd1e-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="abd1e-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="abd1e-138">Réseau</span><span class="sxs-lookup"><span data-stu-id="abd1e-138">Network</span></span>

  - <span data-ttu-id="abd1e-139">Ajout d’un nouveau paramètre de commutateur pour l’interface réseau afin d’activer/de désactiver la mise en réseau accélérée +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="abd1e-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="abd1e-140">Activation des applets de commande PowerShell de la fonctionnalité Active-Active gateway</span><span class="sxs-lookup"><span data-stu-id="abd1e-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="abd1e-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="abd1e-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="abd1e-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="abd1e-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="abd1e-143">Ajout d’une nouvelle applet de commande</span><span class="sxs-lookup"><span data-stu-id="abd1e-143">Added new cmdlet</span></span>
    + <span data-ttu-id="abd1e-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="abd1e-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="abd1e-145">Ressources</span><span class="sxs-lookup"><span data-stu-id="abd1e-145">Resources</span></span>
  - <span data-ttu-id="abd1e-146">Prise en charge des zones dans les applets de commande de fournisseur et de ressource</span><span class="sxs-lookup"><span data-stu-id="abd1e-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="abd1e-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="abd1e-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="abd1e-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="abd1e-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="abd1e-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="abd1e-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="abd1e-150">SQL</span><span class="sxs-lookup"><span data-stu-id="abd1e-150">Sql</span></span>
  - <span data-ttu-id="abd1e-151">Ajout de nouvelles applets de commande pour la gestion des stratégies de détection des menaces Azure SQL au niveau serveur</span><span class="sxs-lookup"><span data-stu-id="abd1e-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="abd1e-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="abd1e-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="abd1e-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="abd1e-155">Ajout de nouvelles applets de commande pour prendre en charge l’activation/la désactivation de GeoBackupPolicy pour les entrepôts de données Azure SQL</span><span class="sxs-lookup"><span data-stu-id="abd1e-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="abd1e-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="abd1e-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="abd1e-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="abd1e-158">Ajout de nouvelles applets de commande pour les conseillers Azure SQL et les API d’actions recommandées</span><span class="sxs-lookup"><span data-stu-id="abd1e-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="abd1e-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="abd1e-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="abd1e-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="abd1e-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="abd1e-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="abd1e-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="abd1e-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="abd1e-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="abd1e-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="abd1e-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="abd1e-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="abd1e-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="abd1e-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="abd1e-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="abd1e-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="abd1e-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="abd1e-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="abd1e-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="abd1e-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="abd1e-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="abd1e-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="abd1e-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="abd1e-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="abd1e-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
