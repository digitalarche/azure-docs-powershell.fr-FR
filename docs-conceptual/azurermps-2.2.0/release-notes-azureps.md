---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 6fe226a2525142f82b894318b0588681bff0e2ef
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="99330-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="99330-103">Release notes</span></span>

<span data-ttu-id="99330-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="99330-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="99330-105">Version 2.2.0</span><span class="sxs-lookup"><span data-stu-id="99330-105">Version 2.2.0</span></span>
* <span data-ttu-id="99330-106">Calcul</span><span class="sxs-lookup"><span data-stu-id="99330-106">Compute</span></span>
  - <span data-ttu-id="99330-107">Ajout de la prise en charge de l’interrogation de l’état de chiffrement par l’extension AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="99330-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="99330-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="99330-108">DataFactory</span></span>
  - <span data-ttu-id="99330-109">Ajout d’une nouvelle applet de commande pour répertorier les fenêtres d’activité</span><span class="sxs-lookup"><span data-stu-id="99330-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="99330-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="99330-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="99330-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="99330-111">DataLake</span></span>
  - <span data-ttu-id="99330-112">Changement du paramètre `Host` en `DatabaseHost` et ajout d’un alias à `Host`</span><span class="sxs-lookup"><span data-stu-id="99330-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="99330-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="99330-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="99330-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="99330-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="99330-115">Ajout de la prise en charge de la suppression de la liste de contrôle d’accès et de la liste de contrôle d’accès par défaut</span><span class="sxs-lookup"><span data-stu-id="99330-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="99330-116">Ajout de la prise en charge de l’obtention et de la définition d’autorisations sans nom sur des fichiers et des dossiers</span><span class="sxs-lookup"><span data-stu-id="99330-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="99330-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="99330-117">KeyVault</span></span>
  - <span data-ttu-id="99330-118">Ajout de la prise en charge des certificats</span><span class="sxs-lookup"><span data-stu-id="99330-118">Add support for certificates</span></span>
    + <span data-ttu-id="99330-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99330-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="99330-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99330-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="99330-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99330-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="99330-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99330-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="99330-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="99330-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="99330-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="99330-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="99330-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="99330-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="99330-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99330-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="99330-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="99330-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="99330-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="99330-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="99330-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="99330-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="99330-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="99330-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="99330-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99330-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="99330-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="99330-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="99330-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="99330-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="99330-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="99330-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="99330-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="99330-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="99330-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="99330-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="99330-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="99330-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="99330-138">Réseau</span><span class="sxs-lookup"><span data-stu-id="99330-138">Network</span></span>

  - <span data-ttu-id="99330-139">Ajout d’un nouveau paramètre de commutateur pour l’interface réseau afin d’activer/de désactiver la mise en réseau accélérée +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="99330-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="99330-140">Activation des applets de commande PowerShell de la fonctionnalité Active-Active gateway</span><span class="sxs-lookup"><span data-stu-id="99330-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="99330-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="99330-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="99330-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="99330-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="99330-143">Ajout d’une nouvelle applet de commande</span><span class="sxs-lookup"><span data-stu-id="99330-143">Added new cmdlet</span></span>
    + <span data-ttu-id="99330-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="99330-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="99330-145">Ressources</span><span class="sxs-lookup"><span data-stu-id="99330-145">Resources</span></span>
  - <span data-ttu-id="99330-146">Prise en charge des zones dans les applets de commande de fournisseur et de ressource</span><span class="sxs-lookup"><span data-stu-id="99330-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="99330-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="99330-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="99330-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="99330-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="99330-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="99330-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="99330-150">SQL</span><span class="sxs-lookup"><span data-stu-id="99330-150">Sql</span></span>
  - <span data-ttu-id="99330-151">Ajout de nouvelles applets de commande pour la gestion des stratégies de détection des menaces Azure SQL au niveau serveur</span><span class="sxs-lookup"><span data-stu-id="99330-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="99330-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="99330-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="99330-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="99330-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="99330-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="99330-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="99330-155">Ajout de nouvelles applets de commande pour prendre en charge l’activation/la désactivation de GeoBackupPolicy pour les entrepôts de données Azure SQL</span><span class="sxs-lookup"><span data-stu-id="99330-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="99330-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="99330-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="99330-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="99330-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="99330-158">Ajout de nouvelles applets de commande pour les conseillers Azure SQL et les API d’actions recommandées</span><span class="sxs-lookup"><span data-stu-id="99330-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="99330-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="99330-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="99330-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="99330-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="99330-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="99330-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="99330-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="99330-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="99330-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="99330-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="99330-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="99330-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="99330-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="99330-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="99330-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="99330-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="99330-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="99330-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="99330-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="99330-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="99330-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="99330-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="99330-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="99330-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
