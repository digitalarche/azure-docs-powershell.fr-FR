# <a name="breaking-changes-for-microsoft-azure-powershell-300"></a>Dernières modifications de Microsoft Azure PowerShell 3.0.0

Ce document fait office de notification des dernières modifications et de guide de migration pour les consommateurs des applets de commande Microsoft Azure PowerShell.  Chaque section décrit la dynamique sous-jacente aux dernières modifications et le chemin de migration à moindre résistance.  Pour bénéficier d’un contexte détaillé, référez-vous à la requête de tirage associée à chaque modification.

## <a name="table-of-contents"></a>Sommaire
1. [Dernières modifications des applets de commande Data Lake Store](#breaking-changes-to-data-lake-store-cmdlets)
2. [Dernières modifications des applets de commande ApiManagement](#breaking-changes-to-apimanagement-cmdlets)
3. [Dernières modifications des applets de commande Network](#breaking-changes-to-network-cmdlets)

## <a name="breaking-changes-to-data-lake-store-cmdlets"></a>Dernières modifications des applets de commande Data Lake Store

Les applets de commande suivantes affectaient cette version ([PR 2965](https://github.com/Azure/azure-powershell/pull/2965)) :

**Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)**
- Cette applet de commande a été supprimée et remplacée par ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.
- L’ancienne applet de commande a renvoyé un objet complexe représentant la liste de contrôle d’accès (ACL). La nouvelle applet de commande renvoie une liste simple d’entrées dans l’ACL du chemin d’accès choisi.

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)**
- Cette applet de commande remplace l’ancienne applet de commande ``Get-AzureRmDataLakeStoreItemAcl (Get-AdlStoreItemAcl)``.
- Cette nouvelle applet de commande renvoie une liste simple d’entrées dans l’ACL du chemin d’accès choisi, avec le type ``DataLakeStoreItemAce[]``.
- La sortie de cette applet de commande peut être passée au paramètre ``-Acl`` des applets de commande suivantes :
   - ``Remove-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAcl``
   - ``Set-AzureRmDataLakeStoreItemAclEntry``

```powershell
# Old
Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo

# New
Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
```

**Remove-AzureRmDataLakeStoreItemAcl (Remove-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAcl (Set-AdlStoreItemAcl)**, **Set-AzureRmDataLakeStoreItemAclEntry (Set-AdlStoreItemAclEntry)**
- Ces applets de commande acceptent désormais la valeur ``DataLakeStoreItemAce[]`` pour le paramètre ``-Acl``.
- ``DataLakeStoreItemAce[]`` est renvoyé par ``Get-AzureRmDataLakeStoreItemAclEntry (Get-AdlStoreItemAclEntry)``.

```powershell
# Old
$acl = Get-AdlStoreItemAcl -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $acl

# New
$aclEntries = Get-AdlStoreItemAclEntry -Account myadlsaccount -Path /foo
Set-AdlStoreItemAcl -Account myadlsaccount -Path /foo -Acl $aclEntries
```

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Dernières modifications des applets de commande ApiManagement

Les applets de commande suivantes affectaient cette version ([PR 2971](https://github.com/Azure/azure-powershell/pull/2971)) :

**New-AzureRmApiManagementVirtualNetwork**
- Les paramètres requis pour référencer un réseau virtuel modifié des demandes SubnetName et VnetId en SubnetResourceId au format ``/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ClassicNetwork/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}``.

```powershell
# Old
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetName <String> -VnetId <Guid>

# New
$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>

```

**Dépréciation de l’applet de commande Set-AzureRmApiManagementVirtualNetworks**
- L’applet de commande est dépréciée car il existait plus d’une manière de définir le réseau virtuel associé au déploiement ApiManagement.

```powershell
# Old
$networksList = @()
$networksList += New-AzureRmApiManagementVirtualNetwork -Location $vnetLocation -VnetId $vnetId -SubnetName $subnetName
Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $networksList

# New
$masterRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $masterRegionVirtualNetwork
```

## <a name="breaking-changes-to-network-cmdlets"></a>Dernières modifications des applets de commande Network

Les applets de commande suivantes affectaient cette version ([PR 2982](https://github.com/Azure/azure-powershell/pull/2982)) :

**New-AzureRmVirtualNetworkGateway**
- La description de la cause de modification de ``:- Bool parameter:-ActiveActive`` est supprimée, tandis que l’instance ``SwitchParameter:-EnableActiveActiveFeature`` est ajoutée pour l’activation de la fonction Active-Active sur la nouvelle création de passerelle de réseau virtuel.

```powershell
# Old 
# Sample of how the cmdlet was previously called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -ActiveActive $true

# New
# Sample of how the cmdlet should now be called
New-AzureRmVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -Location $location -IpConfigurations $vnetIpConfig1,$vnetIpConfig2 -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku HighPerformance -EnableActiveActiveFeature
```

Set-AzureRmVirtualNetworkGateway
- La description de la cause de modification de ``:- Bool parameter:-ActiveActive`` est supprimée, tandis que 2 instances ``SwitchParameters:-EnableActiveActiveFeature`` / ``DisableActiveActiveFeature`` sont ajoutées pour l’activation et la désactivation de la fonction Active-Active sur la passerelle de réseau virtuel.

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