---
title: Bien démarrer avec Azure PowerShell | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 3114f9e9b36dc374f9fb2d402c448cff7fef0aa3
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/22/2018
ms.locfileid: "52258653"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="5adf1-102">Bien démarrer avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5adf1-102">Getting started with Azure PowerShell</span></span>

<span data-ttu-id="5adf1-103">Azure PowerShell est conçu pour la gestion et l’administration des ressources Azure à partir de la ligne de commande, et pour la création de scripts d’automatisation utilisables avec Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5adf1-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="5adf1-104">Vous pouvez l’ouvrir dans le navigateur avec [Azure Cloud Shell](/azure/cloud-shell/overview), ou vous pouvez l’installer sur votre ordinateur local et l’utiliser dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5adf1-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="5adf1-105">Cet article vous aide à bien démarrer et explique les concepts de base.</span><span class="sxs-lookup"><span data-stu-id="5adf1-105">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="5adf1-106">Connecter</span><span class="sxs-lookup"><span data-stu-id="5adf1-106">Connect</span></span>

<span data-ttu-id="5adf1-107">La façon la plus simple de commencer est de [lancer Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="5adf1-107">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="5adf1-108">Lancez Cloud Shell dans le volet de navigation supérieur du Portail Azure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-108">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Icône Shell](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="5adf1-110">Sélectionnez l’abonnement que vous souhaitez utiliser, et créez un compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="5adf1-110">Choose the subscription you want to use and create a storage account.</span></span>

   ![Créez un compte de stockage.](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="5adf1-112">Une fois que votre espace de stockage est créé, Azure Cloud Shell ouvre une session PowerShell dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="5adf1-112">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Azure Cloud Shell pour PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="5adf1-114">Vous pouvez également installer Azure PowerShell et l’utiliser en local dans une session PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5adf1-114">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="5adf1-115">Installation d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5adf1-115">Install Azure PowerShell</span></span>

<span data-ttu-id="5adf1-116">La première étape est de vérifier que la dernière version d’Azure PowerShell est installée.</span><span class="sxs-lookup"><span data-stu-id="5adf1-116">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="5adf1-117">Pour plus d’informations sur la version la plus récente, consultez les [Notes de publication](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5adf1-117">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="5adf1-118">[Installez Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="5adf1-118">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="5adf1-119">Pour vérifier que l’installation a réussi, exécutez `Get-Module AzureRM -ListAvailable` à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="5adf1-119">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="log-in-to-azure"></a><span data-ttu-id="5adf1-120">Connexion à Azure</span><span class="sxs-lookup"><span data-stu-id="5adf1-120">Log in to Azure</span></span>

<span data-ttu-id="5adf1-121">Connectez-vous de manière interactive :</span><span class="sxs-lookup"><span data-stu-id="5adf1-121">Sign on interactively:</span></span>

1. <span data-ttu-id="5adf1-122">Saisissez `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="5adf1-122">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="5adf1-123">Une boîte de dialogue s’affiche pour vous demander vos informations d’identification Azure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="5adf1-124">L’option '-EnvironmentName' peut vous permettre de vous connecter à Azure Chine ou Azure Allemagne.</span><span class="sxs-lookup"><span data-stu-id="5adf1-124">Option '-EnvironmentName' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="5adf1-125">Par exemple, Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="5adf1-125">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="5adf1-126">Entrez l’adresse de messagerie et le mot de passe associés à votre compte.</span><span class="sxs-lookup"><span data-stu-id="5adf1-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="5adf1-127">Azure authentifie et enregistre les informations d’identification, puis ferme la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5adf1-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="5adf1-128">Une fois que vous êtes connecté à un compte Azure, vous pouvez utiliser les applets de commande Azure PowerShell pour gérer les ressources dans votre abonnement, et y accéder.</span><span class="sxs-lookup"><span data-stu-id="5adf1-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="5adf1-129">Créer un groupe de ressources</span><span class="sxs-lookup"><span data-stu-id="5adf1-129">Create a resource group</span></span>

<span data-ttu-id="5adf1-130">Nous avons terminé l’installation. Nous allons maintenant utiliser Azure PowerShell pour créer des ressources dans Azure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-130">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="5adf1-131">Nous devons d’abord créer un groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="5adf1-131">First, create a Resource Group.</span></span> <span data-ttu-id="5adf1-132">Les groupes de ressources dans Azure permettent de gérer plusieurs ressources à regrouper logiquement.</span><span class="sxs-lookup"><span data-stu-id="5adf1-132">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="5adf1-133">Par exemple, vous pouvez créer un groupe de ressources pour une application ou un projet, et y ajouter une machine virtuelle, une base de données et un service CDN.</span><span class="sxs-lookup"><span data-stu-id="5adf1-133">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="5adf1-134">Nous allons créer un groupe de ressources nommé « MyResourceGroup » dans la région westeurope d’Azure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-134">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="5adf1-135">Pour ce faire, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5adf1-135">To do so type the following command:</span></span>

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="5adf1-136">Créer une machine virtuelle Windows</span><span class="sxs-lookup"><span data-stu-id="5adf1-136">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="5adf1-137">Maintenant que nous avons notre groupe de ressources, nous allons y créer une machine virtuelle Windows.</span><span class="sxs-lookup"><span data-stu-id="5adf1-137">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="5adf1-138">Pour créer une machine virtuelle, nous devons d’abord créer les autres ressources nécessaires et les affecter à une configuration.</span><span class="sxs-lookup"><span data-stu-id="5adf1-138">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="5adf1-139">Ensuite, nous utiliserons cette configuration pour créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-139">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="5adf1-140">Créer les ressources réseau nécessaires</span><span class="sxs-lookup"><span data-stu-id="5adf1-140">Create the required network resources</span></span>

<span data-ttu-id="5adf1-141">Nous devons tout d’abord créer la configuration de sous-réseau à utiliser pour le processus de création du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="5adf1-141">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="5adf1-142">Nous créons également une adresse IP publique pour pouvoir nous connecter à cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-142">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="5adf1-143">Nous créons un groupe de sécurité réseau pour sécuriser l’accès à l’adresse publique.</span><span class="sxs-lookup"><span data-stu-id="5adf1-143">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="5adf1-144">Enfin, nous créons la carte réseau virtuelle à l’aide de toutes les ressources créées.</span><span class="sxs-lookup"><span data-stu-id="5adf1-144">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="5adf1-145">Créer la machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="5adf1-145">Create the virtual machine</span></span>

<span data-ttu-id="5adf1-146">Tout d’abord, obtenons des informations d’identification pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5adf1-146">First we need a set of credentials for the OS.</span></span>

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="5adf1-147">Maintenant que nous avons les ressources nécessaires, nous pouvons créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-147">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="5adf1-148">Pour cette étape, nous créons un objet de configuration de machine virtuelle, puis nous utilisons la configuration pour créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-148">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="5adf1-149">La commande `New-AzureRmVM` retourne un résultat une fois que la machine virtuelle a été créée et qu’elle est prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="5adf1-149">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="5adf1-150">Connectez-vous maintenant à la nouvelle machine virtuelle Windows Server à l’aide du Bureau à distance et de l’adresse IP publique de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-150">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="5adf1-151">La commande suivante affiche l’adresse IP publique ayant été créée dans le script précédent.</span><span class="sxs-lookup"><span data-stu-id="5adf1-151">The following command displays the public IP address created in the previous script.</span></span>

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="5adf1-152">Sur un système Windows, vous pouvez vous connecter en exécutant la commande mstsc à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="5adf1-152">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="5adf1-153">Fournissez les mêmes informations de connexion nom d’utilisateur/mot de passe que celles que vous avez utilisées lors de la création de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-153">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="5adf1-154">Créer une machine virtuelle Linux</span><span class="sxs-lookup"><span data-stu-id="5adf1-154">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="5adf1-155">Pour créer une machine virtuelle Linux, nous devons d’abord créer les autres ressources nécessaires et les affecter à une configuration.</span><span class="sxs-lookup"><span data-stu-id="5adf1-155">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="5adf1-156">Ensuite, nous utiliserons cette configuration pour créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-156">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="5adf1-157">Cela suppose que vous avez déjà créé le groupe de ressources, comme expliqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="5adf1-157">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="5adf1-158">En outre, vous devez disposer d’une clé publique SSH nommée `id_rsa.pub` dans le répertoire .ssh de votre profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5adf1-158">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="5adf1-159">Créer les ressources réseau nécessaires</span><span class="sxs-lookup"><span data-stu-id="5adf1-159">Create the required network resources</span></span>

<span data-ttu-id="5adf1-160">Nous devons tout d’abord créer la configuration de sous-réseau à utiliser pour le processus de création du réseau virtuel.</span><span class="sxs-lookup"><span data-stu-id="5adf1-160">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="5adf1-161">Nous créons également une adresse IP publique pour pouvoir nous connecter à cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-161">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="5adf1-162">Nous créons un groupe de sécurité réseau pour sécuriser l’accès à l’adresse publique.</span><span class="sxs-lookup"><span data-stu-id="5adf1-162">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="5adf1-163">Enfin, nous créons la carte réseau virtuelle à l’aide de toutes les ressources créées.</span><span class="sxs-lookup"><span data-stu-id="5adf1-163">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="5adf1-164">Créer la machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="5adf1-164">Create the virtual machine</span></span>

<span data-ttu-id="5adf1-165">Maintenant que nous avons les ressources nécessaires, nous pouvons créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-165">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="5adf1-166">Pour cette étape, nous créons un objet de configuration de machine virtuelle, puis nous utilisons la configuration pour créer la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5adf1-166">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="5adf1-167">Vous pouvez maintenant vous connecter à votre nouvelle machine virtuelle Linux en utilisant SSH avec l’adresse IP publique de la machine virtuelle que vous avez créée :</span><span class="sxs-lookup"><span data-stu-id="5adf1-167">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="5adf1-168">Création d’autres ressources dans Azure</span><span class="sxs-lookup"><span data-stu-id="5adf1-168">Creating other resources in Azure</span></span>

<span data-ttu-id="5adf1-169">Nous avons vu comment créer un groupe de ressources, une machine virtuelle Linux et une machine virtuelle Windows Server.</span><span class="sxs-lookup"><span data-stu-id="5adf1-169">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="5adf1-170">Nous pouvons aussi créer de nombreux autres types de ressources Azure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-170">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="5adf1-171">Par exemple, nous pouvons créer un équilibrage de la charge réseau Azure, pour l’associer ensuite à nos nouvelles machines virtuelles, en utilisant la commande create suivante :</span><span class="sxs-lookup"><span data-stu-id="5adf1-171">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="5adf1-172">Nous pouvons aussi créer un réseau privé virtuel (communément appelé « VNet » dans Azure) pour notre infrastructure à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5adf1-172">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="5adf1-173">Ce qui rend Azure et Azure PowerShell si puissants, c’est que nous pouvons les utiliser non seulement pour mettre en place une infrastructure cloud, mais également pour créer des services de plateforme gérés.</span><span class="sxs-lookup"><span data-stu-id="5adf1-173">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="5adf1-174">Ces services peuvent ensuite être combinés avec l’infrastructure pour obtenir des solutions encore plus puissantes.</span><span class="sxs-lookup"><span data-stu-id="5adf1-174">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="5adf1-175">Par exemple, utilisez Azure PowerShell pour créer un service Azure App Service.</span><span class="sxs-lookup"><span data-stu-id="5adf1-175">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="5adf1-176">Azure App Service est un service de plateforme géré qui offre un excellent moyen d’héberger des applications web sans avoir à se soucier de l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-176">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="5adf1-177">Après avoir créé le service App Service, vous pouvez y créer deux applications Azure Web Apps à l’aide des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5adf1-177">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="5adf1-178">Affichage des ressources déployées</span><span class="sxs-lookup"><span data-stu-id="5adf1-178">Listing deployed resources</span></span>

<span data-ttu-id="5adf1-179">Vous pouvez utiliser l’applet de commande `Get-AzureRmResource` pour répertorier les ressources actuellement exécutées dans Azure.</span><span class="sxs-lookup"><span data-stu-id="5adf1-179">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="5adf1-180">L’exemple ci-dessous affiche les ressources que nous venons de créer dans le nouveau groupe de ressources.</span><span class="sxs-lookup"><span data-stu-id="5adf1-180">The following example shows the resources we just created in the new resource group.</span></span>

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
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

## <a name="deleting-resources"></a><span data-ttu-id="5adf1-181">Suppression de ressources</span><span class="sxs-lookup"><span data-stu-id="5adf1-181">Deleting resources</span></span>

<span data-ttu-id="5adf1-182">Pour nettoyer votre compte Azure, vous souhaitez supprimer les ressources que nous avons créées dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="5adf1-182">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="5adf1-183">Utilisez les applets de commande `Remove-AzureRm*` pour supprimer les ressources dont vous n’avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="5adf1-183">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="5adf1-184">Pour supprimer la machine virtuelle Windows que nous avons créée, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="5adf1-184">To remove the Windows VM we created, using the following command:</span></span>

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="5adf1-185">Un message s’affiche pour vous demander de confirmer la suppression de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5adf1-185">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5adf1-186">Vous pouvez aussi supprimer de nombreuses ressources à la fois.</span><span class="sxs-lookup"><span data-stu-id="5adf1-186">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="5adf1-187">Par exemple, la commande suivante supprime tout le groupe de ressources « MyResourceGroup » que nous avons utilisé dans l’ensemble des exemples de ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="5adf1-187">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="5adf1-188">Cette commande supprime le groupe de ressources et toutes les ressources qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="5adf1-188">This removes the resource group and all of the resources in it.</span></span>

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="5adf1-189">L’exécution de cette commande peut prendre plusieurs minutes.</span><span class="sxs-lookup"><span data-stu-id="5adf1-189">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="5adf1-190">Obtenir des exemples</span><span class="sxs-lookup"><span data-stu-id="5adf1-190">Get samples</span></span>

<span data-ttu-id="5adf1-191">Pour plus d’informations sur les différentes utilisations d’Azure PowerShell, découvrez nos scripts les plus courants pour les [machines virtuelles Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), les [machines virtuelles Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), les [applications Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) et les [bases de données SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="5adf1-191">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="5adf1-192">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5adf1-192">Next steps</span></span>

* [<span data-ttu-id="5adf1-193">Se connecter avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5adf1-193">Login with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="5adf1-194">Gérer les abonnements Azure avec Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5adf1-194">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="5adf1-195">Créer des principaux du service dans Azure à l’aide d’Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5adf1-195">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="5adf1-196">Lisez les notes de publication sur la migration à partir d’une version antérieure : [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="5adf1-196">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="5adf1-197">Obtenir de l’aide de la communauté :</span><span class="sxs-lookup"><span data-stu-id="5adf1-197">Get help from the community:</span></span>
  * [<span data-ttu-id="5adf1-198">Forum Azure sur MSDN (en anglais)</span><span class="sxs-lookup"><span data-stu-id="5adf1-198">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="5adf1-199">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="5adf1-199">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
