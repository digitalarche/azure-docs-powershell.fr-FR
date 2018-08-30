---
title: Prise en main de Microsoft Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 5354a75e969e084d6457d0566a516705f365476f
ms.sourcegitcommit: 9cb98f055a0525c2061f65149965d5e7c3e03ddc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43117119"
---
# <a name="get-started-with-azure-powershell"></a>Prise en main de Microsoft Azure PowerShell

Azure PowerShell est conçu pour la gestion et l’administration des ressources Azure à partir de la ligne de commande, et pour la création de scripts d’automatisation utilisables avec Azure Resource Manager. Vous pouvez l’utiliser dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou l’installer sur votre ordinateur local. Cet article vous aide à bien démarrer avec Azure PowerShell et explique les concepts de base.

## <a name="install-azure-powershell"></a>Installation d’Azure PowerShell

La première étape est de vérifier que la dernière version d’Azure PowerShell est installée. Pour plus d’informations sur la version la plus récente, consultez les [notes de publication](./release-notes-azureps.md).

1. [Installez Azure PowerShell](install-azurerm-ps.md).

2. Pour vérifier que l’installation a réussi, exécutez `Get-Module AzureRM -ListAvailable` à partir de la ligne de commande.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

La façon la plus simple de commencer est de [lancer Cloud Shell](/azure/cloud-shell/quickstart).

1. Lancez Cloud Shell dans le volet de navigation supérieur du Portail Azure.

   ![Icône Shell](~/media/get-started-azureps/shell-icon.png)

2. Sélectionnez l’abonnement que vous souhaitez utiliser, et créez un compte de stockage.

   ![Créez un compte de stockage.](~/media/get-started-azureps/storage-prompt.png)

Une fois que votre espace de stockage est créé, Azure Cloud Shell ouvre une session PowerShell dans le navigateur.

![Azure Cloud Shell pour PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Vous pouvez également installer Azure PowerShell et l’utiliser en local dans une session PowerShell.

## <a name="sign-in-to-azure"></a>Connexion à Azure

Connectez-vous de manière interactive :

1. Saisissez `Connect-AzureRmAccount`. Une boîte de dialogue s’affiche pour vous demander vos informations d’identification Azure. L’option « -Environment » peut vous permettre de vous authentifier pour Azure - Chine ou Azure - Allemagne.

   Par exemple, Connect-AzureRmAccount -Environment AzureChinaCloud

2. Entrez l’adresse de messagerie et le mot de passe associés à votre compte. Azure authentifie et enregistre les informations d’identification, puis ferme la fenêtre.

Une fois que vous êtes connecté à un compte Azure, vous pouvez utiliser les cmdlets Azure PowerShell pour gérer les ressources dans votre abonnement, et y accéder.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Créer une machine virtuelle Windows avec des valeurs par défaut simples

L’applet de commande `New-AzureRmVM` propose une syntaxe simplifiée qui facilite la création d’une nouvelle machine virtuelle. Seules deux valeurs de paramètre sont à fournir : le nom de la machine virtuelle et un ensemble d’informations d’identification pour le compte d’administrateur local sur la machine virtuelle.

Commencez par créer l’objet d’informations d’identification.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Ensuite, créez la machine virtuelle.

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

Il s’agit de la partie facile. Toutefois, il se peut que vous vous demandiez quels autres éléments ont été créés et comment la machine virtuelle est configurée. Commençons par examiner nos groupes de ressources.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

Le groupe de ressources **cloud-shell-storage-westus** est créé lors de la première utilisation de Cloud Shell. Le groupe de ressources **SampleVM** a été créé par l’applet de commande `New-AzureRmVM`.

Quelles sont les autres ressources créées dans ce nouveau groupe de ressources ?

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

Il s’agit d’obtenir de plus amples informations sur la machine virtuelle. Cet exemple montre comment récupérer des informations sur l’image de système d’exploitation utilisée pour créer la machine virtuelle.

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Créer une machine virtuelle Linux entièrement configurée

Des valeurs de paramètre par défaut et une syntaxe simplifiée ont été utilisées dans l’exemple précédent pour créer une machine virtuelle Windows. Dans cet exemple, nous fournissons des valeurs pour toutes les options de la machine virtuelle.

### <a name="create-a-resource-group"></a>Créer un groupe de ressources

Pour cet exemple, nous souhaitons créer un groupe de ressources. Les groupes de ressources dans Azure permettent de gérer plusieurs ressources à regrouper logiquement. Par exemple, vous pouvez créer un groupe de ressources pour une application ou un projet, et y ajouter une machine virtuelle, une base de données et un service CDN.

Nous allons créer un groupe de ressources nommé « MyResourceGroup » dans la région westeurope d’Azure. Pour ce faire, tapez la commande suivante :

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

Ce nouveau groupe de ressources sera utilisé pour contenir toutes les ressources nécessaires à la nouvelle machine virtuelle en cours de création. Pour créer une machine virtuelle Linux, nous devons d’abord créer les autres ressources nécessaires et les affecter à une configuration. Ensuite, nous utiliserons cette configuration pour créer la machine virtuelle. En outre, vous devez disposer d’une clé publique SSH nommée `id_rsa.pub` dans le répertoire .ssh de votre profil utilisateur.

#### <a name="create-the-required-network-resources"></a>Créer les ressources réseau nécessaires

Nous devons tout d’abord créer la configuration de sous-réseau à utiliser pour le processus de création du réseau virtuel. Nous créons également une adresse IP publique pour pouvoir nous connecter à cette machine virtuelle. Nous créons un groupe de sécurité réseau pour sécuriser l’accès à l’adresse publique. Enfin, nous créons la carte réseau virtuelle à l’aide de toutes les ressources créées.

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a>Créer la configuration de machine virtuelle

Maintenant que nous avons les ressources nécessaires, nous pouvons créer l’objet de configuration de la machine virtuelle.

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a>Créer la machine virtuelle

Nous pouvons maintenant créer la machine virtuelle à l’aide de l’objet de configuration de la machine virtuelle.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Vous pouvez maintenant vous connecter à votre nouvelle machine virtuelle Linux en utilisant SSH avec l’adresse IP publique de la machine virtuelle que vous avez créée :

```bash
ssh xx.xxx.xxx.xxx
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a>Création d’autres ressources dans Azure

Nous avons vu comment créer un groupe de ressources, une machine virtuelle Linux et une machine virtuelle Windows Server. Nous pouvons aussi créer de nombreux autres types de ressources Azure.

Par exemple, nous pouvons créer un équilibrage de la charge réseau Azure, pour l’associer ensuite à nos nouvelles machines virtuelles, en utilisant la commande create suivante :

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Nous pouvons aussi créer un réseau privé virtuel (communément appelé « VNet » dans Azure) pour notre infrastructure à l’aide de la commande suivante :

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Ce qui rend Azure et Azure PowerShell si puissants, c’est que nous pouvons les utiliser non seulement pour mettre en place une infrastructure cloud, mais également pour créer des services de plateforme gérés. Ces services peuvent ensuite être combinés avec l’infrastructure pour obtenir des solutions encore plus puissantes.

Par exemple, utilisez Azure PowerShell pour créer un service Azure App Service. Azure App Service est un service de plateforme géré qui offre un excellent moyen d’héberger des applications web sans avoir à se soucier de l’infrastructure. Après avoir créé le service App Service, vous pouvez y créer deux applications Azure Web Apps à l’aide des commandes suivantes :

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Affichage des ressources déployées

Vous pouvez utiliser l’applet de commande `Get-AzureRmResource` pour répertorier les ressources actuellement exécutées dans Azure. L’exemple ci-dessous affiche les ressources que nous venons de créer dans le nouveau groupe de ressources.

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a>Suppression de ressources

Pour nettoyer votre compte Azure, vous souhaitez supprimer les ressources que nous avons créées dans cet exemple. Utilisez les applets de commande `Remove-AzureRm*` pour supprimer les ressources dont vous n’avez plus besoin. Pour supprimer la machine virtuelle Windows que nous avons créée, exécutez la commande suivante :

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Un message s’affiche pour vous demander de confirmer la suppression de la ressource.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Vous pouvez aussi supprimer de nombreuses ressources à la fois. Par exemple, la commande suivante supprime tout le groupe de ressources « MyResourceGroup » que nous avons utilisé dans l’ensemble des exemples de ce didacticiel. Cette commande supprime le groupe de ressources et toutes les ressources qu’il contient.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

L’exécution de cette commande peut prendre plusieurs minutes.

## <a name="get-samples"></a>Obtenir des exemples

Pour plus d’informations sur les différentes utilisations d’Azure PowerShell, découvrez nos scripts les plus courants pour les [machines virtuelles Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), les [machines virtuelles Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), les [applications Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) et les [bases de données SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Étapes suivantes

* [Se connecter avec Azure PowerShell](authenticate-azureps.md)
* [Gérer les abonnements Azure avec Azure PowerShell](manage-subscriptions-azureps.md)
* [Créer des principaux du service dans Azure à l’aide d’Azure PowerShell](create-azure-service-principal-azureps.md)
* Lisez les notes de publication sur la migration à partir d’une version antérieure : [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Obtenir de l’aide de la communauté :
  * [Forum Azure sur MSDN (en anglais)](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
