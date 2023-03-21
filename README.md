<p align="center">
<img src="https://i.imgur.com/j8EIglo.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Creating VMs in Azure and Observing Network Topology </h1>
This guide will teach you how to create Virtual Machines and a Virtual Network in Azure. A Virtual Machine is a virtual environment that functions as a virtual computer system with its own CPU, memory, network interface, and storage, created on a physical hardware system. A Virtual Network is a network that connects virtual machines and devices, no matter their location, using software. For our purposes, a Vnet is what facilitates data communication between 2 or more virtual machines. After the VMs and Vnet are set up in Azure, you will learn how to easily observe the Network Topology using Network Watcher. <br />

<h2>Prerequisites</h2>

- [Creating a Subscription and Resource Group in Azure](https://github.com/mikeguardiola/create-azure-sub-and-resource)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure

<h2>Operating Systems Used </h2>

- Windows 10 Pro (21H2)

<h2>High-Level Steps</h2>
 
- Create a Windows 10 Virtual Machine
- While creating the VM, allow it to create a new Virtual Network (Vnet) and Subnet
- Create a Linux (Ubuntu) Virtual Machine
- Observe your Virtual Network with Network Watcher

<h2>Step-By-Step Instructions:</h2>

<p>
  Step 1:
<img src="https://i.imgur.com/socu9go.png"/>
</p>
<p>
Within the Azure Portal, navigate to the search bar at the top. Within the search bar, type "Virtual machines" and select it.
</p>
<br />

<p>
  Step 2:
<img src="https://i.imgur.com/pr8xnDL.png"/>
</p>
<p>
After you click "Virtual machines", you will be taken to this screen. Once there, click on "Create" and select "Azure virtual machine".
</p>
<br />

<p>
  Step 3:
<img src="https://i.imgur.com/OEs2drO.png"/>
</p>
<p>
Once you are at this screen, you can begin configuring your virtual machine. Under "Project Details", make sure that you have the correct subscription and resource group selected from the drop down menus. Since you are building off the previous tutorial, you can go ahead and select "Azure subsciption 1" and "resource-group-lab-01". Under "Instance Details", you will need to give your virtual machine a name. I went with "VM1". Next, select the correct region that most closely matches where you live. Next, for "Image" you will want to select "Windows 10 Pro, version 21H2 - x64 Gen2 (free services eligible)".
</p>
<br />

<p>
  Step 4:
<img src="https://i.imgur.com/ZUBCPI5.png"/>
</p>
<p>
After that, you will need to scroll down until you see this portion of the screen. For the virtual machine size, select "Standard_E2s_v3-2 vcpus, 16 GiB memory" from the drop down menu. Under "Administrator account", create a username and password. Next, check the box under "Licensing". After that, go ahead and click on the "Next:Disks >" button.
</p>
<br />

<p>
  Step 5:
<img src="https://i.imgur.com/3umaVjc.png"/>
</p>
<p>
You do not need to change any of these settings, so just click on the "Next: Networking >" button.
</p>
<br />

<p>
  Step 6:
<img src="https://i.imgur.com/jMFjgEc.png"/>
</p>
<p>
Once you are at this screen, you do not need to change any settings. However, you will want to make some observations. Under " Network interface", you can see how Azure automatically creates a Virtual Network or Vnet whenever you are setting up a virtual machine. This Vnet is what will connect multiple virtual machines and allow you to facilitate data communication. When ready, go ahead and click on the "Review + create" button.
</p>
<br />

<p>
  Step 7:
<img src="https://i.imgur.com/jKQU4KZ.png"/>
</p>
<p>
Azure will now go through a quick validation process. Once the validation process is complete, click on the "Create" button.
</p>
<br />

<p>
  Step 8:
<img src="https://i.imgur.com/sTtHUUU.png"/>
</p>
<p>
Azure will go through its deployment process to create all of the resources connected to your virtual machine. Once deployment is complete, you will be able to see all the various resources that were created under "Deployment details". When ready, click on the "Create another VM" button.
</p>

<p>
  Step 9:
<img src="https://i.imgur.com/kEXy51l.png"/>
</p>
<p>
Once your container has been created, go ahead an click on it to enter your container's portal.
</p>
<br />

<p>
  Step 10:
<img src="https://i.imgur.com/A09i2FB.png"/>
</p>
<p>
Now you are going to want to upload a basic text file into your container.
</p>
<br />

<p>
  Step 11:
<img src="https://i.imgur.com/VjKDm35.png"/>
</p>
<p>
First, you will need to create a text document and save it to your desktop. For this tutorial, I will be using Notepad. You can access this program by pressing the Windows Key and typing "Notepad". Once you have it open, add some text to your file and save it to your desktop.
</p>
<br />

<p>
  Step 12:
<img src="https://i.imgur.com/J80CLl7.png"/>
</p>
<p>
Now, head back over to your container. Click on the "Upload" button. You can either drag and drop your file from your desktop, or you can upload from the file explorer. Click on the blue "Upload" button when ready.
</p>
<br />

<p>
  Step 13:
<img src="https://i.imgur.com/OwVZ16r.png"/>
</p>
<p>
Now that the text file has been uploaded, you can edit, download, delete or choose one of the other available options.
</p>
<br />
This will conclude your tutorial on how to create a storage account in Azure. Well done and thank you for following along!
