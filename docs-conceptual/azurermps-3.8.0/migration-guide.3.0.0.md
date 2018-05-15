# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a><span data-ttu-id="3a503-101">Dernières modifications de Microsoft Azure PowerShell 3.0.0</span><span class="sxs-lookup"><span data-stu-id="3a503-101">Breaking changes for Microsoft Azure PowerShell 3.0.0.</span></span>

<span data-ttu-id="3a503-102">Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3a503-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="3a503-103">Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance.</span><span class="sxs-lookup"><span data-stu-id="3a503-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span>  <span data-ttu-id="3a503-104">Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.</span><span class="sxs-lookup"><span data-stu-id="3a503-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="3a503-105">Sommaire</span><span class="sxs-lookup"><span data-stu-id="3a503-105">Table of Contents</span></span>
1. [<span data-ttu-id="3a503-106">Dernières modifications des applets de commande Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3a503-106">Breaking changes to Data Lake Store cmdlets</span></span>](#breaking-changes-to-data-lake-store-cmdlets)
2. [<span data-ttu-id="3a503-107">Dernières modifications des applets de commande ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a503-107">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
3. [<span data-ttu-id="3a503-108">Dernières modifications des applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="3a503-108">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a><span data-ttu-id="3a503-109">Dernières modifications des applets de commande Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3a503-109">Breaking changes to Data Lake Store cmdlets</span></span>

<span data-ttu-id="3a503-110">Les applets de commande suivantes affectaient cette version ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) :</span><span class="sxs-lookup"><span data-stu-id="3a503-110">The following cmdlets were affected this release ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)):</span></span>

<span data-ttu-id="3a503-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span><span class="sxs-lookup"><span data-stu-id="3a503-111">**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**</span></span>
- <span data-ttu-id="3a503-112">Cette applet de commande a été supprimée et remplacée par ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="3a503-112">This cmdlet was removed and replaced with ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>
- <span data-ttu-id="3a503-113">L’ancienne applet de commande a renvoyé un objet complexe représentant la liste de contrôle d’accès (ACL).</span><span class="sxs-lookup"><span data-stu-id="3a503-113">The old cmdlet returned a complex object representing the access control list (ACL).</span></span> <span data-ttu-id="3a503-114">La nouvelle applet de commande renvoie une liste simple d’entrées dans l’ACL du chemin d’accès choisi.</span><span class="sxs-lookup"><span data-stu-id="3a503-114">The new cmdlet returns a simple list of entries in the chosen path's ACL.</span></span>

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="3a503-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="3a503-115">**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="3a503-116">Cette applet de commande remplace l’ancienne applet de commande ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span><span class="sxs-lookup"><span data-stu-id="3a503-116">This cmdlet replaces the old cmdlet ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.</span></span>
- <span data-ttu-id="3a503-117">Cette nouvelle applet de commande renvoie une liste simple d’entrées dans l’ACL du chemin d’accès choisi, avec le type ``DataLakeStoreItemAce[]``.</span><span class="sxs-lookup"><span data-stu-id="3a503-117">This new cmdlet returns a simple list of entries in the chosen path's ACL, with type ``DataLakeStoreItemAce[]``.</span></span>
- <span data-ttu-id="3a503-118">La sortie de cette applet de commande peut être passée au paramètre ``-Acl`` des applets de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a503-118">The output of this cmdlet can be passed in to the ``-Acl`` parameter of the following cmdlets:</span></span>
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

<span data-ttu-id="3a503-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span><span class="sxs-lookup"><span data-stu-id="3a503-119">**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**</span></span>
- <span data-ttu-id="3a503-120">Ces applets de commande acceptent désormais la valeur ``DataLakeStoreItemAce[]`` pour le paramètre ``-Acl``.</span><span class="sxs-lookup"><span data-stu-id="3a503-120">These cmdlets now accept ``DataLakeStoreItemAce[]`` for the ``-Acl`` parameter.</span></span>
- <span data-ttu-id="3a503-121">``DataLakeStoreItemAce[]`` est renvoyé par ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span><span class="sxs-lookup"><span data-stu-id="3a503-121">``DataLakeStoreItemAce[]`` is returned by ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.</span></span>

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="3a503-122">Dernières modifications des applets de commande ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a503-122">Breaking changes to ApiManagement cmdlets</span></span>

<span data-ttu-id="3a503-123">Les applets de commande suivantes affectaient cette version ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) :</span><span class="sxs-lookup"><span data-stu-id="3a503-123">The following cmdlets were affected this release ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)):</span></span>

<span data-ttu-id="3a503-124">**New-AzureRmApiManagementVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="3a503-124">**New-AzureRmApiManagementVirtualNetwork**</span></span>
- <span data-ttu-id="3a503-125">Les paramètres requis pour référencer un réseau virtuel modifié des demandes SubnetName et VnetId en SubnetResourceId au format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``.</span><span class="sxs-lookup"><span data-stu-id="3a503-125">The required parameters to reference a virtual network changed from requiring SubnetName and VnetId to SubnetResourceId in format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``</span></span>

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

<span data-ttu-id="3a503-126">**Dépréciation de l’applet de commande Set-AzureRmApiManagementVirtualNetworks**</span><span class="sxs-lookup"><span data-stu-id="3a503-126">**Deprecating Cmdlet Set-AzureRmApiManagementVirtualNetworks**</span></span>
- <span data-ttu-id="3a503-127">L’applet de commande est dépréciée car il existait plus d’une manière de définir le réseau virtuel associé au déploiement ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3a503-127">The Cmdlet is getting deprecated as there was more than one way to Set Virtual Network associated to ApiManagement deployment.</span></span>

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="3a503-128">Dernières modifications des applets de commande Network</span><span class="sxs-lookup"><span data-stu-id="3a503-128">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="3a503-129">Les applets de commande suivantes affectaient cette version ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) :</span><span class="sxs-lookup"><span data-stu-id="3a503-129">The following cmdlets were affected this release ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)):</span></span>

<span data-ttu-id="3a503-130">**New-AzureRmVirtualNetworkGateway**</span><span class="sxs-lookup"><span data-stu-id="3a503-130">**New-AzureRmVirtualNetworkGateway**</span></span>
- <span data-ttu-id="3a503-131">La description de la cause de modification de ``:- Bool parameter:-ActiveActive`` est supprimée, tandis que l’instance ``SwitchParameter:-EnableActiveActiveFeature`` est ajoutée pour l’activation de la fonction Active-Active sur la nouvelle création de passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="3a503-131">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and ``SwitchParameter:-EnableActiveActiveFeature`` is added for enabling Active-Active feature on newly creating virtual network gateway.</span></span>

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

<span data-ttu-id="3a503-132">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3a503-132">Set-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="3a503-133">La description de la cause de modification de ``:- Bool parameter:-ActiveActive`` est supprimée, tandis que 2 instances ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` sont ajoutées pour l’activation et la désactivation de la fonction Active-Active sur la passerelle de réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="3a503-133">Description of what has changed ``:- Bool parameter:-ActiveActive`` is removed and 2 ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` are added for enabling and disabling Active-Active feature on virtual network gateway.</span></span>

```powershell
# Old
# Sample of how the cmdlet was previously called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $true
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -ActiveActive $false  

# New
# Sample of how the cmdlet should now be called
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -EnableActiveActiveFeature
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gw -DisableActiveActiveFeature
```