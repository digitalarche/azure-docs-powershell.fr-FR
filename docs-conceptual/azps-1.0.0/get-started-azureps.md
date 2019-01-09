---
title: Prise en main de Microsoft Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 10/30/2018
ms.openlocfilehash: 7367648a0a84cd5be5c7501ef4bf743a4290ce0f
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982907"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="a5cd6-102">Prise en main de Microsoft Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5cd6-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="a5cd6-103">Azure PowerShell est conçu pour la gestion et l’administration des ressources Azure à partir de la ligne de commande, et pour la création de scripts d’automatisation utilisables avec Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="a5cd6-104">Vous pouvez l’utiliser dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou l’installer sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="a5cd6-105">Cet article vous aide à bien démarrer avec Azure PowerShell et explique les concepts de base.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="a5cd6-106">Installation d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5cd6-106">Install Azure PowerShell</span></span>

<span data-ttu-id="a5cd6-107">La première étape est de vérifier que la dernière version d’Azure PowerShell est installée.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="a5cd6-108">Pour plus d’informations sur la version la plus récente, consultez les [Notes de publication](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a5cd6-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="a5cd6-109">[Installez Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="a5cd6-109">[Install Azure PowerShell](install-az-ps.md).</span></span>

2. <span data-ttu-id="a5cd6-110">Pour vérifier que l’installation a réussi, exécutez `Get-InstalledModule Az -AllVersions` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-110">To verify the installation was successful, run `Get-InstalledModule Az -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="a5cd6-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="a5cd6-111">Azure Cloud Shell</span></span>

<span data-ttu-id="a5cd6-112">La façon la plus simple de commencer est de [lancer Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="a5cd6-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="a5cd6-113">Lancez Cloud Shell dans le volet de navigation supérieur du Portail Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Icône Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="a5cd6-115">Sélectionnez l’abonnement que vous souhaitez utiliser, et créez un compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Créez un compte de stockage.](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="a5cd6-117">Une fois que votre espace de stockage est créé, Azure Cloud Shell ouvre une session PowerShell dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Azure Cloud Shell pour PowerShell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a><span data-ttu-id="a5cd6-119">Connexion à Azure</span><span class="sxs-lookup"><span data-stu-id="a5cd6-119">Sign in to Azure</span></span>

<span data-ttu-id="a5cd6-120">Connectez-vous de manière interactive :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-120">Sign on interactively:</span></span>

1. <span data-ttu-id="a5cd6-121">Saisissez `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-121">Type `Connect-AzAccount`.</span></span> <span data-ttu-id="a5cd6-122">L’argument `-Environment` permet de vous authentifier pour une autre région ou un autre cloud.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-122">The `-Environment` argument lets you authenticate for a different region or cloud.</span></span> <span data-ttu-id="a5cd6-123">Par exemple, pour vous connecter à Azure Chine :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-123">For example, to connect to Azure China:</span></span>

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. <span data-ttu-id="a5cd6-124">Vous obtenez un jeton à utiliser sur https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-124">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="a5cd6-125">Ouvrez cette page dans votre navigateur et entrez le jeton pour vous connecter avec vos informations d’identification Azure et autoriser Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-125">Open this page in your browser and enter the token to sign in with your Azure credentials, and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="a5cd6-126">Une fois que vous êtes connecté à un compte Azure, vous pouvez utiliser les cmdlets Azure PowerShell pour gérer les ressources dans votre abonnement, et y accéder.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-126">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span> <span data-ttu-id="a5cd6-127">Pour en savoir plus sur le processus de connexion et les méthodes d’authentification disponibles, consultez l’article sur la [connexion avec Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a5cd6-127">To learn more about the sign in process and available authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="a5cd6-128">Créer une machine virtuelle Windows avec des valeurs par défaut simples</span><span class="sxs-lookup"><span data-stu-id="a5cd6-128">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="a5cd6-129">L’applet de commande `New-AzVM` propose une syntaxe simplifiée qui facilite la création d’une nouvelle machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-129">The `New-AzVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="a5cd6-130">Seules deux valeurs de paramètre sont à fournir : le nom de la machine virtuelle et un ensemble d’informations d’identification pour le compte d’administrateur local sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-130">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="a5cd6-131">Commencez par créer l’objet d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-131">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="a5cd6-132">Ensuite, créez la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-132">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzVM -Name SampleVM -Credential $cred
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

<span data-ttu-id="a5cd6-133">Il se peut que vous vous demandiez quels autres éléments ont été créés et comment la machine virtuelle est configurée.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-133">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="a5cd6-134">Commençons par examiner nos groupes de ressources.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-134">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="a5cd6-135">Le groupe de ressources **cloud-shell-storage-westus** est créé lors de la première utilisation de Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-135">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="a5cd6-136">Le groupe de ressources **SampleVM** a été créé par l’applet de commande `New-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-136">The **SampleVM** resource group was created by the `New-AzVM` cmdlet.</span></span>

<span data-ttu-id="a5cd6-137">Quelles sont les autres ressources créées dans ce nouveau groupe de ressources ?</span><span class="sxs-lookup"><span data-stu-id="a5cd6-137">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzResource |
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

<span data-ttu-id="a5cd6-138">Il s’agit d’obtenir de plus amples informations sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-138">Let's get some more details about the VM.</span></span> <span data-ttu-id="a5cd6-139">Cet exemple indique comment récupérer les informations relatives à l’image du système d’exploitation utilisée pour créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-139">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzVM -Name SampleVM -ResourceGroupName SampleVM |
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

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="a5cd6-140">Créer une machine virtuelle Linux entièrement configurée</span><span class="sxs-lookup"><span data-stu-id="a5cd6-140">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="a5cd6-141">Des valeurs de paramètre par défaut et une syntaxe simplifiée ont été utilisées dans l’exemple précédent pour créer une machine virtuelle Windows.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-141">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="a5cd6-142">Dans cet exemple, nous fournissons des valeurs pour toutes les options de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-142">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="a5cd6-143">Créer un groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="a5cd6-143">Create a resource group</span></span>

<span data-ttu-id="a5cd6-144">Dans cet exemple, nous souhaitons créer un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-144">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="a5cd6-145">Les groupes de ressources dans Azure permettent de gérer plusieurs ressources à regrouper logiquement.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-145">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="a5cd6-146">Par exemple, vous pouvez créer un groupe de ressources pour une application ou un projet, et y ajouter une machine virtuelle, une base de données et un service CDN.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-146">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="a5cd6-147">Nous allons créer un groupe de ressources nommé « MyResourceGroup » dans la région uswest2 d’Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-147">Let's create a resource group named "MyResourceGroup" in the uswest2 region of Azure.</span></span> <span data-ttu-id="a5cd6-148">Pour ce faire, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-148">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name 'myResourceGroup' -Location 'westus2'
```

```output
ResourceGroupName : myResourceGroup
Location          : westus2
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="a5cd6-149">Ce nouveau groupe de ressources sera utilisé pour contenir toutes les ressources nécessaires à la nouvelle machine virtuelle en cours de création.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-149">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="a5cd6-150">Pour créer une machine virtuelle Linux, nous devons d’abord créer les autres ressources nécessaires, puis les affecter à une configuration.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-150">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="a5cd6-151">Ensuite, nous utiliserons cette configuration pour créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-151">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="a5cd6-152">En outre, vous devez disposer d’une clé publique SSH nommée `id_rsa.pub` dans le répertoire `.ssh` de votre profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-152">Also, you will need to have an SSH public key named `id_rsa.pub` in the `.ssh` directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="a5cd6-153">Créer les ressources réseau nécessaires</span><span class="sxs-lookup"><span data-stu-id="a5cd6-153">Create the required network resources</span></span>

<span data-ttu-id="a5cd6-154">Nous devons tout d’abord créer la configuration de sous-réseau à utiliser pour le processus de création du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-154">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="a5cd6-155">Nous créons également une adresse IP publique pour pouvoir nous connecter à cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-155">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="a5cd6-156">Nous créons un groupe de sécurité réseau pour sécuriser l’accès à l’adresse publique.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-156">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="a5cd6-157">Enfin, nous créons la carte réseau virtuelle à l’aide de toutes les ressources créées.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-157">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westus2"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="a5cd6-158">Créer la configuration de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="a5cd6-158">Create the VM configuration</span></span>

<span data-ttu-id="a5cd6-159">Maintenant que nous avons les ressources nécessaires, nous pouvons créer l’objet de configuration de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-159">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B1s |
  Set-AzVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="a5cd6-160">Créer la machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="a5cd6-160">Create the virtual machine</span></span>

<span data-ttu-id="a5cd6-161">Nous pouvons maintenant créer la machine virtuelle à l’aide de l’objet de configuration de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-161">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="a5cd6-162">Maintenant que la machine virtuelle est créée, vous pouvez vous connecter à votre nouvelle machine virtuelle Linux à l’aide de SSH, avec l’adresse IP publique de la machine virtuelle que vous venez de créer :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-162">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```powershell-interactive
ssh azureuser@$($publicIp.IpAddress)
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="a5cd6-163">Création d’autres ressources dans Azure</span><span class="sxs-lookup"><span data-stu-id="a5cd6-163">Creating other resources in Azure</span></span>

<span data-ttu-id="a5cd6-164">Nous avons vu comment créer un groupe de ressources, une machine virtuelle Linux et une machine virtuelle Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-164">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="a5cd6-165">Nous pouvons aussi créer de nombreux autres types de ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-165">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="a5cd6-166">Par exemple, nous pouvons créer un équilibrage de la charge réseau Azure, pour l’associer ensuite à nos nouvelles machines virtuelles, en utilisant la commande create suivante :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-166">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

<span data-ttu-id="a5cd6-167">Nous pouvons aussi créer un réseau privé virtuel (communément appelé « VNet » dans Azure) pour notre infrastructure à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-167">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="a5cd6-168">Ce qui rend Azure et Azure PowerShell si puissants, c’est que nous pouvons les utiliser non seulement pour mettre en place une infrastructure cloud, mais également pour créer des services de plateforme gérés.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-168">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="a5cd6-169">Ces services peuvent ensuite être combinés avec l’infrastructure pour obtenir des solutions encore plus puissantes.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-169">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="a5cd6-170">Par exemple, utilisez Azure PowerShell pour créer un service Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-170">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="a5cd6-171">Azure App Service est un service de plateforme géré qui offre un excellent moyen d’héberger des applications web sans avoir à se soucier de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-171">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="a5cd6-172">Après avoir créé le service App Service, vous pouvez y créer deux applications Azure Web Apps à l’aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-172">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="a5cd6-173">Affichage des ressources déployées</span><span class="sxs-lookup"><span data-stu-id="a5cd6-173">Listing deployed resources</span></span>

<span data-ttu-id="a5cd6-174">Vous pouvez utiliser l’applet de commande `Get-AzResource` pour répertorier les ressources actuellement exécutées dans Azure.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-174">You can use the `Get-AzResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="a5cd6-175">L’exemple suivant affiche les ressources que nous avons créées dans le nouveau groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-175">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westus2 Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westus2 Microsoft.Compute/disks
myLinuxVM                                             westus2 Microsoft.Compute/virtualMachines
myWindowsVM                                           westus2 Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westus2 Microsoft.Compute/virtualMachines/extensions
myNic1                                                westus2 Microsoft.Network/networkInterfaces
myNic2                                                westus2 Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westus2 Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westus2 Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westus2 Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westus2 Microsoft.Network/publicIPAddresses
MYvNET1                                               westus2 Microsoft.Network/virtualNetworks
MYvNET2                                               westus2 Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westus2 Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="a5cd6-176">Suppression de ressources</span><span class="sxs-lookup"><span data-stu-id="a5cd6-176">Deleting resources</span></span>

<span data-ttu-id="a5cd6-177">Pour nettoyer votre compte Azure, vous souhaitez supprimer les ressources que nous avons créées dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-177">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="a5cd6-178">Utilisez les applets de commande `Remove-Az*` pour supprimer les ressources dont vous n’avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-178">You can use the `Remove-Az*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="a5cd6-179">Pour supprimer la machine virtuelle Windows que nous avons créée, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-179">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="a5cd6-180">Un message va s’afficher pour vous demander de confirmer la suppression de la ressource.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-180">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a5cd6-181">Vous pouvez également supprimer plusieurs ressources simultanément.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-181">You can also delete many resources at once.</span></span> <span data-ttu-id="a5cd6-182">Par exemple, la commande suivante supprime le groupe de ressources « MyResourceGroup » que nous avons jusqu’alors utilisé pour l’ensemble des exemples.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-182">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="a5cd6-183">Toutes les ressources du groupe sont également supprimées.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-183">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a5cd6-184">La réalisation de la tâche peut prendre plusieurs minutes, en fonction du nombre et du type de ressources.</span><span class="sxs-lookup"><span data-stu-id="a5cd6-184">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="a5cd6-185">Obtenir les exemples</span><span class="sxs-lookup"><span data-stu-id="a5cd6-185">Get samples</span></span>

<span data-ttu-id="a5cd6-186">Pour plus d’informations sur les différentes utilisations d’Azure PowerShell, découvrez nos scripts les plus courants pour les [machines virtuelles Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), les [machines virtuelles Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), les [applications Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) et les [bases de données SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="a5cd6-186">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a5cd6-187">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a5cd6-187">Next steps</span></span>

* [<span data-ttu-id="a5cd6-188">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5cd6-188">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="a5cd6-189">Gérer les abonnements Azure avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5cd6-189">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="a5cd6-190">Créer des principaux du service dans Azure à l’aide d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a5cd6-190">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="a5cd6-191">Obtenir de l’aide de la communauté :</span><span class="sxs-lookup"><span data-stu-id="a5cd6-191">Get help from the community:</span></span>
  * [<span data-ttu-id="a5cd6-192">Forum Azure sur MSDN (en anglais)</span><span class="sxs-lookup"><span data-stu-id="a5cd6-192">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="a5cd6-193">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="a5cd6-193">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
