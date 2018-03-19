# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="91f22-101">Dernières modifications de Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="91f22-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="91f22-102">Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91f22-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="91f22-103">Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance.</span><span class="sxs-lookup"><span data-stu-id="91f22-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="91f22-104">Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.</span><span class="sxs-lookup"><span data-stu-id="91f22-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="91f22-105">Sommaire</span><span class="sxs-lookup"><span data-stu-id="91f22-105">Table of Contents</span></span>

- [<span data-ttu-id="91f22-106">Dernières modifications des applets de commande ApiManagement</span><span class="sxs-lookup"><span data-stu-id="91f22-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="91f22-107">Dernières modifications des applets de commande Batch</span><span class="sxs-lookup"><span data-stu-id="91f22-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="91f22-108">Dernières modifications des applets de commande Compute</span><span class="sxs-lookup"><span data-stu-id="91f22-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="91f22-109">Dernières modifications des applets de commande EventHub</span><span class="sxs-lookup"><span data-stu-id="91f22-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="91f22-110">Dernières modifications des applets de commande Insights</span><span class="sxs-lookup"><span data-stu-id="91f22-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="91f22-111">Dernières modifications des applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="91f22-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="91f22-112">Dernières modifications des applets de commande Resources</span><span class="sxs-lookup"><span data-stu-id="91f22-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="91f22-113">Dernières modifications des applets de commande ServiceBus</span><span class="sxs-lookup"><span data-stu-id="91f22-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="91f22-114">Dernières modifications des applets de commande ApiManagement</span><span class="sxs-lookup"><span data-stu-id="91f22-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="91f22-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="91f22-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="91f22-116">Les paramètres UserName et Password sont remplacés par une instance PSCredential.</span><span class="sxs-lookup"><span data-stu-id="91f22-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="91f22-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="91f22-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="91f22-118">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="91f22-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="91f22-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="91f22-120">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="91f22-121">Dernières modifications des applets de commande Batch</span><span class="sxs-lookup"><span data-stu-id="91f22-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="91f22-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="91f22-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="91f22-123">Le paramètre `Password` est remplacé par une chaîne sécurisée.</span><span class="sxs-lookup"><span data-stu-id="91f22-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="91f22-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="91f22-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="91f22-125">Le paramètre `Password` est remplacé par une chaîne sécurisée.</span><span class="sxs-lookup"><span data-stu-id="91f22-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="91f22-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="91f22-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="91f22-127">Le paramètre `Password` est remplacé par une chaîne sécurisée.</span><span class="sxs-lookup"><span data-stu-id="91f22-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="91f22-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="91f22-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="91f22-129">Le commutateur `RunElevated` a été remplacé par `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="91f22-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="91f22-130">Cela affecte par ailleurs la propriété `RunElevated` sur `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` et `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="91f22-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="91f22-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="91f22-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="91f22-132">Le constructeur `PSMultiInstanceSettings` ne prend plus de paramètre `numberOfInstances` requis, il prend plutôt un paramètre `coordinationCommandLine` requis.</span><span class="sxs-lookup"><span data-stu-id="91f22-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="91f22-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="91f22-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="91f22-134">La propriété `RunElevated` a été supprimée sur `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="91f22-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="91f22-135">La propriété `UserIdentity` a été ajoutée pour remplacer `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="91f22-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="91f22-136">Cela affecte par ailleurs la propriété `RunElevated` sur `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` et `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="91f22-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="91f22-137">**Plusieurs types**</span><span class="sxs-lookup"><span data-stu-id="91f22-137">**Multiple types**</span></span>

- <span data-ttu-id="91f22-138">La propriété `SchedulingError` a été renommée sur `PSExitConditions`, en `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="91f22-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="91f22-139">**Plusieurs types**</span><span class="sxs-lookup"><span data-stu-id="91f22-139">**Multiple types**</span></span>

- <span data-ttu-id="91f22-140">La propriété `SchedulingError` a été renommée sur `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` et `PSTaskExecutionInformation`, en `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="91f22-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="91f22-141">`FailureInformation` est renvoyé lors de chaque défaillance de tâche.</span><span class="sxs-lookup"><span data-stu-id="91f22-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="91f22-142">Sont concernés ici l’ensemble des erreurs de planification précédentes, les codes de sortie de tâche différents de 0 et les défaillances de chargement de fichiers de la nouvelle fonctionnalité de fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="91f22-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="91f22-143">La structure restant identique, aucune modification de code n’est nécessaire lors de l’utilisation de ce type.</span><span class="sxs-lookup"><span data-stu-id="91f22-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="91f22-144">Les instances suivantes sont également affectées : Get-AzureBatchPool, Get-AzureBatchSubtask et Get-AzureBatchJobPreparationAndReleaseTaskStatus.</span><span class="sxs-lookup"><span data-stu-id="91f22-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="91f22-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="91f22-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="91f22-146">L’instance `TargetDedicated` a été supprimée et remplacée par `TargetDedicatedComputeNodes` et `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="91f22-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="91f22-147">`TargetDedicatedComputeNodes` possède un alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="91f22-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="91f22-148">Cela affecte également l’instance suivante : Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="91f22-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="91f22-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="91f22-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="91f22-150">Les propriétés `TargetDedicated` et `CurrentDedicated` sur `PSCloudPool` ont été renommées en `TargetDedicatedComputeNodes` et `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="91f22-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="91f22-151">**Type PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="91f22-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="91f22-152">La propriété `ResizeError` a été renommée en `ResizeErrors` sur `PSCloudPool` ; il s’agit désormais d’une collection.</span><span class="sxs-lookup"><span data-stu-id="91f22-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="91f22-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="91f22-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="91f22-154">La propriété `TargetDedicated` sur `PSPoolSpecification` a été renommée en `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="91f22-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="91f22-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="91f22-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="91f22-156">La propriété `Name` a été supprimée et remplacée par `Path`.</span><span class="sxs-lookup"><span data-stu-id="91f22-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="91f22-157">`Path` possède un alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="91f22-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="91f22-158">Cela affecte aussi les instances suivantes : Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile.</span><span class="sxs-lookup"><span data-stu-id="91f22-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="91f22-159">Type **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="91f22-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="91f22-160">La propriété `Name` sur `PSNodeFile` a été renommée en `Path`.</span><span class="sxs-lookup"><span data-stu-id="91f22-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="91f22-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="91f22-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="91f22-162">Les propriétés `PreviousState` et `State` de `PSSubtaskInformation` ne sont plus de type `TaskState`, mais de type `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="91f22-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="91f22-163">Contrairement à `TaskState`, `SubtaskState` ne possède pas de valeur `Active`, dans la mesure où les sous-tâches ne peuvent pas présenter un état `Active`.</span><span class="sxs-lookup"><span data-stu-id="91f22-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="91f22-164">Dernières modifications des applets de commande Compute</span><span class="sxs-lookup"><span data-stu-id="91f22-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="91f22-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="91f22-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="91f22-166">Les paramètres UserName et Password sont remplacés par une instance PSCredential.</span><span class="sxs-lookup"><span data-stu-id="91f22-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="91f22-167">Dernières modifications des applets de commande EventHub</span><span class="sxs-lookup"><span data-stu-id="91f22-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="91f22-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-169">L’applet de commande New-AzureRmEventHubNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-170">Utilisez l’applet de commande New-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="91f22-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-172">L’applet de commande Get-AzureRmEventHubNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-173">Utilisez l’applet de commande Get-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="91f22-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-175">L’applet de commande Set-AzureRmEventHubNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-176">Utilisez l’applet de commande Set-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="91f22-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-178">L’applet de commande Remove-AzureRmEventHubNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-179">Utilisez l’applet de commande Remove-AzureRmEventHubAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="91f22-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="91f22-181">L’applet de commande New-AzureRmEventHubNamespaceKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-182">Utilisez l’applet de commande New-AzureRmEventHubKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="91f22-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="91f22-184">L’applet de commande Get-AzureRmEventHubNamespaceKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-185">Utilisez l’applet de commande Get-AzureRmEventHubKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="91f22-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="91f22-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="91f22-187">Les propriétés Status et Enabled de l’instance NamespceAttributes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="91f22-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="91f22-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="91f22-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="91f22-189">Les propriétés Status et Enabled de l’instance NamespceAttributes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="91f22-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="91f22-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="91f22-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="91f22-191">Les propriétés Status et Enabled de l’instance NamespceAttributes seront supprimées.</span><span class="sxs-lookup"><span data-stu-id="91f22-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="91f22-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="91f22-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="91f22-193">La propriété EventHubPath de l’instance ConsumerGroupAttributes sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="91f22-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="91f22-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="91f22-195">La propriété EventHubPath de l’instance ConsumerGroupAttributes sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="91f22-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="91f22-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="91f22-197">La propriété EventHubPath de l’instance ConsumerGroupAttributes sera supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="91f22-198">Dernières modifications des applets de commande Insights</span><span class="sxs-lookup"><span data-stu-id="91f22-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="91f22-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="91f22-200">L’applet de commande **Add-AzureRMLogAlertRule** a été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="91f22-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="91f22-201">À compter du 1er octobre, cette applet de commande n’aura plus aucun effet, dans la mesure où cette fonctionnalité est en cours de transition vers les alertes de journal d’activité.</span><span class="sxs-lookup"><span data-stu-id="91f22-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="91f22-202">Pour plus d’informations, consultez https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="91f22-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="91f22-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="91f22-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="91f22-204">L’applet de commande **Get-AzureRMUsage** a été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="91f22-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="91f22-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="91f22-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="91f22-206">Modification de sortie : le champ EventChannels de l’objet EventData (renvoyé par ces applets de commande) est déprécié, car il renvoie désormais une valeur constante (Admin, Operation).</span><span class="sxs-lookup"><span data-stu-id="91f22-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="91f22-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="91f22-208">Modification de sortie : la sortie de cette applet de commande sera tronquée, par l’élimination du champs des propriétés, ceci pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="91f22-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="91f22-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="91f22-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="91f22-210">Modification de sortie : le champ AutoscaleSettingResourceName sera déprécié, car il est toujours identique au champ Name.</span><span class="sxs-lookup"><span data-stu-id="91f22-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="91f22-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="91f22-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="91f22-212">Modification de sortie :le type de sortie sera modifié pour renvoyer un seul objet contenant l’ID de requête et le code d’état.</span><span class="sxs-lookup"><span data-stu-id="91f22-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="91f22-213">Dernières modifications des applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="91f22-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="91f22-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="91f22-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="91f22-215">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="91f22-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="91f22-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="91f22-217">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="91f22-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="91f22-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="91f22-219">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="91f22-220">Dernières modifications des applets de commande Resources</span><span class="sxs-lookup"><span data-stu-id="91f22-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="91f22-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="91f22-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="91f22-222">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="91f22-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="91f22-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="91f22-224">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="91f22-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="91f22-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="91f22-226">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="91f22-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="91f22-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="91f22-228">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="91f22-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="91f22-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="91f22-230">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="91f22-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="91f22-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="91f22-232">Le paramètre Password est remplacé par une instance SecureString.</span><span class="sxs-lookup"><span data-stu-id="91f22-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="91f22-233">Dernières modifications des applets de commande ServiceBus</span><span class="sxs-lookup"><span data-stu-id="91f22-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="91f22-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-235">L’applet de commande Get-AzureRmServiceBusTopicAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-236">Utilisez l’applet de commande Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="91f22-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="91f22-238">L’applet de commande Get-AzureRmServiceBusTopicKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-239">Utilisez l’applet de commande Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="91f22-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-241">L’applet de commande New-AzureRmServiceBusTopicAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-242">Utilisez l’applet de commande New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="91f22-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="91f22-244">L’applet de commande New-AzureRmServiceBusTopicKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-245">Utilisez l’applet de commande New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="91f22-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-247">L’applet de commande Remove-AzureRmServiceBusTopicAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-248">Utilisez l’applet de commande Remove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="91f22-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-250">L’applet de commande Set-AzureRmServiceBusTopicAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-251">Utilisez l’applet de commande Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="91f22-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="91f22-253">L’applet de commande New-AzureRmServiceBusNamespaceKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-254">Utilisez l’applet de commande New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="91f22-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-256">L’applet de commande Get-AzureRmServiceBusQueueAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-257">Utilisez l’applet de commande Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="91f22-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="91f22-259">L’applet de commande Get-AzureRmServiceBusQueueKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-260">Utilisez l’applet de commande Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="91f22-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-262">L’applet de commande New-AzureRmServiceBusQueueAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-263">Utilisez l’applet de commande New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="91f22-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="91f22-265">L’applet de commande New-AzureRmServiceBusQueueKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-266">Utilisez l’applet de commande New-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="91f22-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-268">L’applet de commande Remove-AzureRmServiceBusQueueAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-269">Utilisez l’applet de commande GRemove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="91f22-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-271">L’applet de commande Set-AzureRmServiceBusQueueAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-272">Utilisez l’applet de commande Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="91f22-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-274">L’applet de commande Get-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-275">Utilisez l’applet de commande Get-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="91f22-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="91f22-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="91f22-277">L’applet de commande Get-AzureRmServiceBusNamespaceKey a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-278">Utilisez l’applet de commande Get-AzureRmServiceBusKey.</span><span class="sxs-lookup"><span data-stu-id="91f22-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="91f22-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-280">L’applet de commande New-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-281">Utilisez l’applet de commande New-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="91f22-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-283">L’applet de commande Remove-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-284">Utilisez l’applet de commande Remove-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="91f22-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="91f22-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="91f22-286">L’applet de commande Set-AzureRmServiceBusNamespaceAuthorizationRule a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="91f22-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="91f22-287">Utilisez l’applet de commande Set-AzureRmServiceBusAuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91f22-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="91f22-288">**Type NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="91f22-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="91f22-289">Les propriétés suivantes ont été supprimées :</span><span class="sxs-lookup"><span data-stu-id="91f22-289">The following properties have been removed</span></span>
    - <span data-ttu-id="91f22-290">activé</span><span class="sxs-lookup"><span data-stu-id="91f22-290">Enabled</span></span>
    - <span data-ttu-id="91f22-291">Statut</span><span class="sxs-lookup"><span data-stu-id="91f22-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="91f22-292">**Type QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="91f22-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="91f22-293">Les propriétés suivantes sont marquées comme obsolètes :</span><span class="sxs-lookup"><span data-stu-id="91f22-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="91f22-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="91f22-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="91f22-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="91f22-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="91f22-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="91f22-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="91f22-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="91f22-297">SupportOrdering</span></span>

```powershell
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="91f22-298">**Type TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="91f22-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="91f22-299">Les propriétés suivantes sont marquées comme obsolètes :</span><span class="sxs-lookup"><span data-stu-id="91f22-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="91f22-300">Lieu</span><span class="sxs-lookup"><span data-stu-id="91f22-300">Location</span></span>
    - <span data-ttu-id="91f22-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="91f22-301">IsExpress</span></span>
    - <span data-ttu-id="91f22-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="91f22-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="91f22-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="91f22-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="91f22-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="91f22-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="91f22-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="91f22-305">EntityAvailabilityStatus</span></span>

```powershell
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="91f22-306">**Type SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="91f22-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="91f22-307">Les propriétés suivantes sont marquées comme obsolètes :</span><span class="sxs-lookup"><span data-stu-id="91f22-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="91f22-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="91f22-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="91f22-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="91f22-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="91f22-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="91f22-310">IsReadOnly</span></span>
    - <span data-ttu-id="91f22-311">Lieu</span><span class="sxs-lookup"><span data-stu-id="91f22-311">Location</span></span>
   
```powershell
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```