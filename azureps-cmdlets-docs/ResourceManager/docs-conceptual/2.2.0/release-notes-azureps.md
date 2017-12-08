---
title: Journal de modifications Azure PowerShell | Microsoft Docs
description: "Il s’agit d’un historique des modifications apportées à Azure PowerShell dans la dernière version."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="59234-103">Notes de publication</span><span class="sxs-lookup"><span data-stu-id="59234-103">Release notes</span></span>

<span data-ttu-id="59234-104">Il s’agit de la liste des modifications apportées à Azure PowerShell dans cette version.</span><span class="sxs-lookup"><span data-stu-id="59234-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="59234-105">Version 2.2.0</span><span class="sxs-lookup"><span data-stu-id="59234-105">Version 2.2.0</span></span>
* <span data-ttu-id="59234-106">Calcul</span><span class="sxs-lookup"><span data-stu-id="59234-106">Compute</span></span>
  - <span data-ttu-id="59234-107">Ajout de la prise en charge de l’interrogation de l’état de chiffrement par l’extension AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="59234-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="59234-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="59234-108">DataFactory</span></span>
  - <span data-ttu-id="59234-109">Ajout d’une nouvelle applet de commande pour répertorier les fenêtres d’activité</span><span class="sxs-lookup"><span data-stu-id="59234-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="59234-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="59234-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="59234-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="59234-111">DataLake</span></span>
  - <span data-ttu-id="59234-112">Changement du paramètre `Host` en `DatabaseHost` et ajout d’un alias à `Host`</span><span class="sxs-lookup"><span data-stu-id="59234-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="59234-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="59234-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="59234-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="59234-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="59234-115">Ajout de la prise en charge de la suppression de la liste de contrôle d’accès et de la liste de contrôle d’accès par défaut</span><span class="sxs-lookup"><span data-stu-id="59234-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="59234-116">Ajout de la prise en charge de l’obtention et de la définition d’autorisations sans nom sur des fichiers et des dossiers</span><span class="sxs-lookup"><span data-stu-id="59234-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="59234-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="59234-117">KeyVault</span></span>
  - <span data-ttu-id="59234-118">Ajout de la prise en charge des certificats</span><span class="sxs-lookup"><span data-stu-id="59234-118">Add support for certificates</span></span>
    + <span data-ttu-id="59234-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59234-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="59234-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59234-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="59234-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59234-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="59234-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59234-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="59234-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="59234-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="59234-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="59234-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="59234-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59234-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="59234-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59234-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="59234-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="59234-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="59234-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="59234-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="59234-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59234-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="59234-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="59234-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="59234-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="59234-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="59234-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="59234-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="59234-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="59234-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="59234-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="59234-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="59234-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="59234-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="59234-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="59234-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="59234-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="59234-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="59234-138">Réseau</span><span class="sxs-lookup"><span data-stu-id="59234-138">Network</span></span>

  - <span data-ttu-id="59234-139">Ajout d’un nouveau paramètre de commutateur pour l’interface réseau afin d’activer/de désactiver la mise en réseau accélérée +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="59234-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="59234-140">Activation des applets de commande PowerShell de la fonctionnalité Active-Active gateway</span><span class="sxs-lookup"><span data-stu-id="59234-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="59234-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="59234-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="59234-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="59234-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="59234-143">Ajout d’une nouvelle applet de commande</span><span class="sxs-lookup"><span data-stu-id="59234-143">Added new cmdlet</span></span>
    + <span data-ttu-id="59234-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="59234-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="59234-145">Ressources</span><span class="sxs-lookup"><span data-stu-id="59234-145">Resources</span></span>
  - <span data-ttu-id="59234-146">Prise en charge des zones dans les applets de commande de fournisseur et de ressource</span><span class="sxs-lookup"><span data-stu-id="59234-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="59234-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="59234-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="59234-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="59234-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="59234-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="59234-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="59234-150">SQL</span><span class="sxs-lookup"><span data-stu-id="59234-150">Sql</span></span>
  - <span data-ttu-id="59234-151">Ajout de nouvelles applets de commande pour la gestion des stratégies de détection des menaces Azure SQL au niveau serveur</span><span class="sxs-lookup"><span data-stu-id="59234-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="59234-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59234-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="59234-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59234-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="59234-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59234-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="59234-155">Ajout de nouvelles applets de commande pour prendre en charge l’activation/la désactivation de GeoBackupPolicy pour les entrepôts de données Azure SQL</span><span class="sxs-lookup"><span data-stu-id="59234-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="59234-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="59234-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="59234-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="59234-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="59234-158">Ajout de nouvelles applets de commande pour les conseillers Azure SQL et les API d’actions recommandées</span><span class="sxs-lookup"><span data-stu-id="59234-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="59234-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="59234-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="59234-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="59234-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="59234-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="59234-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="59234-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="59234-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="59234-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="59234-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="59234-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="59234-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="59234-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="59234-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="59234-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="59234-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="59234-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="59234-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="59234-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="59234-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="59234-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="59234-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="59234-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="59234-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
