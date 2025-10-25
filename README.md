<p align="center">
  <img src="https://raw.githubusercontent.com/tylergehm/vm/main/Azure%20VM%20Logo.jpg" alt="Azure VM Logo" style="max-width:100%;height:auto;" />
</p>

<h1>Creating Windows and Linux Virtual Machines in Azure Portal</h1>
What are Virtual Machines? A virtual machine (VM) is like a computer running inside another computer or in the cloud. It acts like a real PC, letting you run Windows, Linux, or other operating systems without needing extra hardware. VMs are great for practicing IT skills, testing apps, or troubleshooting without risking your main system. In this guide, I will walk you through creating Windows and Linux VMs in the Microsoft Azure portal. <br> <br>
After the Virtual Machines are created, we will test their functionality utilizing Remote Desktop. Remote Desktop is a Windows feature that lets you connect to and control a computer from another device over the internet or a network, like accessing your work PC from home. It’s commonly used to manage virtual machines or troubleshoot systems remotely. For example, with Microsoft’s Remote Desktop Protocol (RDP), you can log into a Windows VM in Azure using its public IP and credentials.
</p>
<h2>Video Demonstration</h2>

- ### [YouTube: Creating Windows and Linux Virtual Machines in Azure Portal](https://www.youtube.com/watch?v=ISIau7bI14E)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Remote Desktop


<h2>Operating Systems Used </h2>

- Windows 11 Home (Host Machine)
- Ubuntu Linux (Azure VM)
- Windows 11 Pro (Azure VM)


<h2>Configuration Steps</h2>

- Step 1 - Create a Resource Group
- Step 2 - Create Windows 11 Pro VM within Resource Group
- Step 3 - Use Remote Desktop to test Windows VM functionality
- Step 4 - Create Ubuntu Linux VM within Resource Group


---
<h2><p align="center">Configuration Process</p></h2>
<h2>Step 1: Create a Resource Group</h2>
<img width="1912" height="844" alt="image" src="https://github.com/user-attachments/assets/e8e798af-0669-4a59-8dd8-04cfcdc54e4e" />

<p>
<br>
We begin the process by searching "Resource groups" in the Azure Portal search bar. Once "Resource groups" is entered into the text box, click on "Resource groups" under Services.

A Resource Group in Microsoft Azure is like a folder that organizes related cloud resources, such as virtual machines, storage, or networks, for easier management. It helps you keep track of costs, set permissions, and delete everything together when done. For this project, the Windows and Linux VMs will be grouped in a single Resource Group.
<br>
</p>
<img width="1913" height="844" alt="image" src="https://github.com/user-attachments/assets/080c5c81-424e-410b-aef5-99d6878a3cd7" />

<p>
  <br>
Once inside the Resource group portal, click "Create" to begin creating a new Resource group.
  <br>
</p>


</p>
<img width="1916" height="865" alt="image" src="https://github.com/user-attachments/assets/b3868c9d-3466-417a-8ab7-92065848ec05" />

</p>
Next, the information regarding the details of the Resource group are entered.
</p>
Subscription: This is the Azure account or billing plan you select to pay for and manage the resources in your Resource Group.
</p>
Resource Name: This is the unique name you give your Resource Group, such as "RG-Virtual-Machines" to identify and organize your resources.
</p>
Region: This is the geographic location, such as "(US) East US 2," where Azure hosts your resources. 
Once filled out, click "Review + Create"
<br>
</p>
<img width="591" height="807" alt="image" src="https://github.com/user-attachments/assets/5b37dbf5-49a4-499a-ab71-ac697a2f9f61" />
</p>
Next we review the summary of the Resource group to be created. Click "Create" to finish creating the Resource group.
</p>
<img width="1910" height="790" alt="image" src="https://github.com/user-attachments/assets/5da97361-cbf2-44ec-bfdd-048f36a8e078" />
</p>
The Resource group "RG-Virtual-Machines" has now been created and ready for use.
<br>
---

<h2>Step 2 - Create Windows 11 Pro VM within Resource Group</h2>
<img width="1885" height="683" alt="image" src="https://github.com/user-attachments/assets/5cff2984-f0fc-41af-9934-6e62eaa87354" />
</p>
Next, we utilize the search bar to look up "Virtual Machines" and click on "Virtual machines" under the Services section.
</p>
<img width="1860" height="709" alt="image" src="https://github.com/user-attachments/assets/581be47d-5362-45a3-94e9-8b72ed51306b" />
</p>
Once inside the Virtual machines portal, we select "Create" to begin setting up the virtual machines.
</p>
<img width="1434" height="615" alt="image" src="https://github.com/user-attachments/assets/31ee6600-94b4-4ec5-9b8f-f5c9b3d4e76f" />
</p>
The first step of VM creation is to select the Resource group that was previously created for this project, "RG-Virtual-Machines". This is important to select the correct Resource group so that the VMs can be placed in the same group.
</p>
<img width="1081" height="572" alt="image" src="https://github.com/user-attachments/assets/69a3ebde-0ab4-489d-be21-ebb14504e7a8" />
Next we will provide the Virtual machine with a name and indicate the region that the VM will be created in. 

Creating virtual machines in the same region in Azure ensures faster performance and lower latency since the resources are hosted close together in the same data center. It also simplifies management and reduces potential costs or issues related to cross-region data transfers.
</p>
<img width="1071" height="507" alt="image" src="https://github.com/user-attachments/assets/463cc129-5276-4787-a7b3-f68cc36e3c16" />
Next, select the Image drop down box and find Windows 11 Pro.
An image in Azure is a pre-configured template that defines the operating system and software for a virtual machine, in this case, it is Windows 11 Pro.

</p>
<img width="1424" height="978" alt="image" src="https://github.com/user-attachments/assets/2bcb6495-02d0-4184-81e3-ad0862d0fe5a" />
Once the image is selected, scroll down to fill out the user name and password for the VM. 
</p>
Make sure that the inbound ports have RDP (3389) selected, as this is what will allow us to remotely access the VM.
</p>
If you don't select the option confirming an eligible Windows 10/11 license with multi-tenant hosting rights, Azure blocks the VM creation because it requires proof you have a valid license to run Windows in a shared cloud environment. Select the checkbox and click "Next: Disks"
</p>
<img width="990" height="318" alt="image" src="https://github.com/user-attachments/assets/cf844068-6500-49c7-9cbc-edf88de3131c" />
Click "Next: Networking" to move into the Networking section of the VM creation.
</p>
<img width="1319" height="559" alt="image" src="https://github.com/user-attachments/assets/ceb0aa1a-b08e-446c-918e-3af3b16ef3e6" />
Under "Virtual Network" click "Edit virtual network" to rename the virtual network. 
</p>
Having VMs on the same virtual network in Azure allows them to communicate quickly and securely with low latency, as they’re in the same isolated network environment. It simplifies setup for tasks like testing or sharing data between VMs without needing complex routing or public internet access.
</p>
<img width="1059" height="807" alt="image" src="https://github.com/user-attachments/assets/f68c0cb2-c168-49e0-99f1-1f6e963a7865" />
</p>
Here is where the virtual network will be renamed and then click save when finished.
</p>
A virtual network in Azure is a private, isolated network in the cloud that lets your virtual machines and other resources communicate securely with each other, like a digital version of a local office network. It controls traffic flow, security rules, and connections, keeping your VMs organized and protected.
</p>
<img width="1013" height="807" alt="image" src="https://github.com/user-attachments/assets/e28a5787-ca18-432d-81db-8349fd0038a8" />
</p>
Next, click on "Review + Create" to be taken to the VM summary page.
</p>
<img width="1461" height="807" alt="image" src="https://github.com/user-attachments/assets/07d93cc9-0af4-4a3a-ac14-c743b13091f5" />
</p>
Validation in Azure, when reviewing and creating a virtual machine, is the process where Azure checks your configuration settings to ensure they meet requirements, like valid licensing, resource availability, and correct network settings. It confirms everything is set up properly before deployment to avoid errors.
</p>
Once the validation has been passed, click "Create" to finish the VM creation.
</p>
<img width="1442" height="571" alt="image" src="https://github.com/user-attachments/assets/3f5198da-459a-46cb-a656-70430c827395" />
</p>
Once the Windows 11 Pro VM has been created or "deployed"; click "Go to resource" to find the public IP address for the VM. This will be used to test the VM with Remote Desktop Connection.
</p>

<img width="1847" height="559" alt="image" src="https://github.com/user-attachments/assets/853c0dc0-2c92-4683-8c05-b9c29543c23b" />

</p>
In the Windows VM portal, scroll down to the "Networking" section. Here is where the information for the Public IP address and Virtual network is shown.

---

<h2>Step 3 - Use Remote Desktop to test Windows VM functionality</h2>
<img width="454" height="271" alt="image" src="https://github.com/user-attachments/assets/5f9b4599-a663-48a3-9e04-2085c5e12c08" />
</p>
To open Windows Remote Desktop Connection, press Windows key + R, type "mstsc", and press Enter. MSTSC stands for Microsoft Terminal Services Client. Alternatively, search for "Remote Desktop Connection" in the Start menu and click the app to launch it.
<img width="529" height="300" alt="image" src="https://github.com/user-attachments/assets/1b977a8b-fd9c-40f9-bd1f-408522d3b17c" />
</p>
Next, enter the Public IP address of the Windows 11 VM, then press Enter. In this case, it is 172.206.16.70. 
<img width="553" height="522" alt="image" src="https://github.com/user-attachments/assets/45786818-4985-490f-9f0d-0a1cde417b0d" />
</p>
Windows Security will then prompt for login credentials for the VM. Enter the user name and password that was chosen during the VM creation and press "Okay".
</p>
<img width="517" height="520" alt="image" src="https://github.com/user-attachments/assets/0ff4e06f-e172-4bcb-9315-13d3482f6164" />
Verify that the name in the certificate is the name of the intended VM to connect into. Once verified, click "Yes" to launch the VM.

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/630261ba-6448-4718-b973-5f1e73ea53bc" />
</p>
The Windows 11 Pro VM functionality has been verified.

---

<h2>Step 4 - Create Ubuntu Linux VM within Resource Group</h2>
<img width="1866" height="445" alt="image" src="https://github.com/user-attachments/assets/ca671c31-7fff-496c-83ca-7b3c85ec6ea9" />
Returning to the Virtual machines portal, we can see the previous VM created is listed as a Running virtual machine; which indicates that the machine is on and ready for use. 
</p>

To create the Ubuntu Linux VM, click "Create".
<img width="442" height="328" alt="image" src="https://github.com/user-attachments/assets/6670edb7-6ef6-46c2-8f3c-41ebbc97c365" />
</p>
In the drop down box, select "Azure Virtual Machine"

<img width="959" height="214" alt="image" src="https://github.com/user-attachments/assets/f150ef2c-0332-4dc1-aa04-6b4febc3ce29" />
</p>
In the Resource group section, select "RG-Virtual-Machines" to make sure the Ubuntu Linux VM is placed in the same Resource group as the Windows 11 VM.
</p>
<img width="992" height="167" alt="image" src="https://github.com/user-attachments/assets/20793a07-7e6d-47d8-b322-ef7fed8ff1e0" />
</p>
In this section, the VM will be named "Linux-VM" and the Region will be "(US) East US 2", which is the same region where the Windows 11 VM was created.
</p>
<img width="948" height="390" alt="image" src="https://github.com/user-attachments/assets/f9aa8237-5ece-4779-b72c-5585de1ffe1e" />
</p>
In the Image drop down box; select Ubuntu Pro 24.04 LTS. 
</p>
<img width="980" height="277" alt="image" src="https://github.com/user-attachments/assets/1fdbf025-164f-4516-8db9-41f4021f0fc7" />
</p>
In the Administrator account section, select the Password button and fill out the Username and password sections. This is the credentials that will be used for logging into the Ubuntu VM. Then click "Next" twice to enter into the Networking section of the VM creation.
</p>
<img width="1074" height="443" alt="image" src="https://github.com/user-attachments/assets/a1f4cc8f-79f1-49e0-8e1f-c086046c07e9" />
</p>
In the drop down box, select "Virtual-Machines-Vnet"; as this is the virtual network that the Windows 11 VM was created on. Then click "Review + Create".
</p>
<img width="1185" height="764" alt="image" src="https://github.com/user-attachments/assets/0bfe2a21-472f-4e59-9ee3-cef817987003" />
</p>

After the VM creation validation has passed, click "Create" to deploy the Ubuntu Linux VM.

<img width="1917" height="521" alt="image" src="https://github.com/user-attachments/assets/f146e75d-3bc3-49c9-a405-f11c6a5d9603" />
</p>
Returning the Virtual machines portal, there are now 2 VMs available: The Windows 11 VM and the Ubuntu Linux VM. In this view, the Public IP address information for both VMs is available.
</p>
<h2>Conclusion</h2>
This project demonstrates the power and flexibility of Microsoft Azure for creating and managing virtual machines, enabling hands-on experience with both Windows and Linux environments in a cloud setting. By utilizing Azure’s Resource Groups and virtual networks, users develop essential skills in configuring and connecting VMs, fostering a deeper understanding of virtualization and network management. This practical experience lays a strong foundation for mastering virtual machine deployment and virtual network setups in cloud environments.
