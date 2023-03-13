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
<img src="https://i.imgur.com/iptUhEI.png"/>
</p>
<p>
Within the Azure Portal, navigate to the search bar at the top. Within the search bar, type "Storage accounts" and select it.
</p>
<br />

<p>
  Step 2:
<img src="https://i.imgur.com/hYekkug.png"/>
</p>
<p>
After you click "Storage accounts", you will be taken to this screen. Once there, click on "Create".
</p>
<br />

<p>
  Step 3:
<img src="https://i.imgur.com/jux9fkp.png"/>
</p>
<p>
Once you are at this screen, you can begin configuring your storage account. Under "Project Details", make sure that you have the correct subscription and resource group selected from the drop down menus. Since you are building off the previous tutorial, you can go ahead and select "Azure subsciption 1" and "resource-group-lab-01". Under "Instance Details", you will need to create a globally unique storage account name. I went with "mikecoursecareerslab01", but you can choose something that is unique to you. Next, select the correct region that most closely matches where you live. After that, you can click the "Review" button at the bottom of the screen.
</p>
<br />

<p>
  Step 4:
<img src="https://i.imgur.com/FgrJl29.png"/>
</p>
<p>
Azure will now run through a quick validation process. Once that is complete, you can click on the "Create" button at the bottom left of the screen.
</p>
<br />

<p>
  Step 5:
<img src="https://i.imgur.com/U3TxVhV.png"/>
</p>
<p>
Your storage account will now go through a deployment process which may take about 30 seconds to a minute. Once completed, you will see a green check mark next to "Your deploymeny is complete" and you can now click on the "Go to resource" button.
</p>
<br />

<p>
  Step 6:
<img src="https://i.imgur.com/QXIHGL2.png"/>
</p>
<p>
You will be taken to the portal for your storage account. We are now ready to upload a basic text file. To do so, you will want to create a folder within your storage account, also known as a container. On the left of your screen, click on "Containers".
</p>
<br />

<p>
  Step 7:
<img src="https://i.imgur.com/2UeninD.png"/>
</p>
<p>
Once you are at this screen, click on "+ Container".
</p>
<br />

<p>
  Step 8:
<img src="https://i.imgur.com/6gYK0gP.png"/>
</p>
<p>
A new window will open up on the right side of your screen to edit your container. Give your container a unique name. You can leave the "Public access level" to the default setting of "Private". When you are finished, click on the "Create" button.
</p>

<p>
  Step 9:
<img src="https://i.imgur.com/aoajfg1.png"/>
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
Congratulations! This concludes this tutorial on how to create a storage account in Azure. Thank you for following along!
