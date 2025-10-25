<p align="center">
  <img src="https://raw.githubusercontent.com/tylergehm/vm/main/Azure%20VM%20Logo.jpg" alt="Azure VM Logo" style="max-width:100%;height:auto;" />
</p>

<h1>Creating Windows and Linux Virtual Machines in Azure Portal</h1>
What are Virtual Machines? A virtual machine (VM) is like a computer running inside another computer or in the cloud. It acts like a real PC, letting you run Windows, Linux, or other operating systems without needing extra hardware. VMs are great for practicing IT skills, testing apps, or troubleshooting without risking your main system. In this guide, I will walk you through creating Windows and Linux VMs in the Microsoft Azure portal.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Remote Desktop


<h2>Operating Systems Used </h2>

- Windows 11 Home (Host Machine)
- Ubuntu Linux (Azure VM)
- Windows 10 Pro (Azure VM)


<h2>Configuration Steps</h2>

- Step 1 - Create a Resource Group
- Step 2 - Create Windows 10 Pro VM within Resource Group
- Step 3 - Use Remote Desktop to test Windows VM functionality
- Step 4 - Create Ubunto Linux VM within Resource Group
- Step 5 - Use Remote Desktop to test Linux VM functionality
- Step 6 - Ping Linux VM to test connectivity



<h2>Configuration Process</h2>
<h2>Step 1: Create a Resource Group</h2>

<p>
The very first thing we have to do is sign-up for a free Microsoft Azure account. When your account is created you are awarded a $200 credit that expires in 30 days. 
After an account has been made we can began our project by creating a Resource Group. Resource Groups provide organization, security, cost management, and simplified operations for Azure VMs and other resources.
</p>
You can click on the Resource Group from the home screen or you can type Resource Group in the search bar at the top. Click on Create and let's get started.
</p>

<img width="785" height="413" alt="Resource Group SS1" src="https://github.com/user-attachments/assets/2d54b42e-bb27-4ae6-8d29-cfe8a714dbe3" />
<img width="809" height="395" alt="Resource Group SS2" src="https://github.com/user-attachments/assets/943c5f69-2c12-4331-af47-71643f92e697" />
</p>
<p>


</p>
Go ahead and give the subscription a name (I went with my first name "Aaron") or it will just generically show up as "Azure Subscription 1". Next we will assign a name for our Resource Group (for our example we chose "VM-Project"). The last thing left to do is click on Region and select one from the list of choices (ours is US East Region 2). At the bottom click 'Review + create' to move on, followed by clicking 'Create' at the bottom on the very next screen page.
</p>


</p>
<img width="573" height="400" alt="Resource Group SS3" src="https://github.com/user-attachments/assets/99e94d1e-42c0-48b7-96bb-2b53b2bfc5f5" />
</p>


The example below confirms our Resource Group was created. Next up: time to create our Virtual Machines!

<img width="784" height="389" alt="Resource Group SS4" src="https://github.com/user-attachments/assets/0090969c-a176-4a62-af06-4f5d08edbe53" />



</p>

<h2>Step 2 - Create Windows 10 Pro VM within Resource Group</h2>
<h2>Step 3 - Use Remote Desktop to test Windows VM functionality</h2>
<h2>Step 4 - Create Ubunto Linux VM within Resource Group</h2>
<h2>Step 5 - Use Remote Desktop to test Linux VM functionality</h2>
<h2>Step 6 - Ping Linux VM to test connectivity</h2>

<h2>Final Thoughts</h2>
</p>
Virtual machines are an incredible resource because they allow us to run multiple operating systems on the same physical hardware for testing or learning purposes.This project provided hands-on experience with virtualization and operating system installation, reinforcing key concepts in system administration and cross-platform compatibility. It lays a solid foundation for more advanced networking, cybersecurity, and DevOps projects.<br />
