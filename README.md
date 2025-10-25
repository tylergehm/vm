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

<h2>Steps Included</h2>

- STEP 1 - Create a Resource Group
- STEP 2 - Create a virtual machine for Windows
- STEP 3 - Deploy the Windows VM
- STEP 4 - Verify the Windows VM is running
- STEP 5 - Create a virtual machine for Linux
- STEP 6 - Deploy the Linux VM
- STEP 7 - Verify the Linux VM is running
- STEP 8 - Verify both our VMs are running



<h2>Installation Steps</h2>

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



</p>
<h2>Step-by-Step Windows VM setup</h2>
</p>
Click on the Home tab to return to the main page. Type virtual machines in the search bar at the top then underneath 'Services' select virtual machines. When the Virtual Machines page comes up we are going to select Create then click on Virtual Machines.
</p>

<img width="860" height="374" alt="WVM 1" src="https://github.com/user-attachments/assets/77b72606-9cdf-4d64-899d-309e2b174516" />


</p>


The Subscription name is already be pre-selected for us. Next we want to ensure the Resource Group is the same previously created "VM-Project". Give the Virtual Machine a name (in the example we went with "WindowsVM"). Make sure that the same Region is picked - (US) East 2 as when the Resource Group was intially created. For Availiabilty Zone uncheck Zone 1 then check the Zone 3 box. 
<br />
</p>
<img width="1184" height="695" alt="WVM 2" src="https://github.com/user-attachments/assets/1fd133e3-e378-44ce-8a00-c432514122ab" />


</p>
For the Image scroll down and select Windows 11 Pro version 24H2 or whichever version you are using. For the Size pick something with at least 2VPUs and don't worry because we are going to delete everything once our project has concluded. For the Username & Password decide on your own set credentials, but do not forget to write them down if it's not easy to remember. Check the box under 'Licensing' at the bottom and click Next to skip over 'Disk' section so you can get to 'Networking'.
<br />
</p>
<img width="1289" height="694" alt="WVM 3" src="https://github.com/user-attachments/assets/5c2c3c52-afb3-455a-bf73-558db5c14aab" />

<img width="478" height="390" alt="WVM 4" src="https://github.com/user-attachments/assets/058d77ef-b7a7-4248-b3bf-ecbbaa570441" />


</p>
On the Networking page we see the Virtual network and Subnet have already been pre-selected. Be certain all the other inputs are correctly checked/selected as in the example. We are now ready to click 'Review + create' towards the bottom of the page.
<br />
</p>
<img width="1088" height="692" alt="WVM 5" src="https://github.com/user-attachments/assets/a166e8f7-35a4-4a97-9050-19667b6b260f" />

<img width="467" height="390" alt="WVM 6" src="https://github.com/user-attachments/assets/3f993681-7f02-48f3-9b8f-925b3cb4ad8b" />



</p>
If all went well "Validation passed" should show up on the next page. Once you see that go ahead and click on 'Create' at the bottom.
<br />
</p>
<img width="514" height="387" alt="WVM 7" src="https://github.com/user-attachments/assets/2aa3eb56-7123-4fe3-b3aa-1eb359d01ad2" />


</p>
Once Create is clicked, our Virtual Machine will began loading and as it's buffering we get a "Deployment is in progress" notification on the screen. When the deployment is done a notification that says "Your deployment is complete" will appear on screen. With that being said, we just set up our first virtual machine! One down, one to go!
<br />
</p>
<img width="1453" height="532" alt="WVM 8" src="https://github.com/user-attachments/assets/499f5cfa-924b-489b-9f23-1ba329b92c65" />


</p>
If we want to double check that our Windows virtual machine has been created, we can click on the Home button to be taken back to the main page. On the main page click the Virtual Machines icon or type it in the search bar. We are taken to the Virtual Machines page & can see our Virtual Machine does indeed exist so now we can move on to creating our next one.
<br />
</p>
<img <img width="930" height="329" alt="WVM 9" src="https://github.com/user-attachments/assets/1c63add5-3411-4e61-a6ec-9b4e5ac01ba4" />





<br />
<h2>Step-by-Step Linux VM setup</h2>
<p>

To began the process click Create and click on Virtual Machine. You will be taken to the 'Create a virtue machine page'.

<img width="804" height="383" alt="LVM 1" src="https://github.com/user-attachments/assets/2894baf2-7491-4f12-a0d5-c9ba8f66f086" />


</p>
The Subscription name is already be pre-selected for us. Next we want to ensure the Resource Group is the same previously created "VM-Project". Give the Virtual Machine a name (in the example we went with "LinuxVM"). Make sure that the same Region is picked - (US) East 2 as when the Resource Group was intially created. For Availiabilty Zone uncheck Zone 1 then check the Zone 3 box.  

<img width="1416" height="699" alt="LVM2" src="https://github.com/user-attachments/assets/5cbf4a3a-586e-445f-bbf5-ba43c66bb6ba" />


</p>
For the Image pick Ubuntu Server 24.04 LTS. For the Size pick something with at least 2VPUs and don't worry because we are going to delete everything once our project has concluded. For the Username & Password decide on your own set credentials, but do not forget to write them down somewhere if it's not easy to remember. At the bottom click Next to skip over 'Disk' section so you can get to 'Networking'.

<img width="424" height="386" alt="LVM 3" src="https://github.com/user-attachments/assets/cb095440-edb5-46c3-bdd3-3933450eb38d" />


</p>
On the Networking page we see the Virtual network and Subnet have already been pre-selected. Be certain all the other inputs are correctly marked/checked as in the example. We are now ready to click 'Review + create' towards the bottom of the page.
<br />
</p>
<img width="1172" height="684" alt="LVM 4" src="https://github.com/user-attachments/assets/1b46c76f-7aa0-464e-ba51-e56c98e9bedc" />

<img width="545" height="387" alt="LVM 5" src="https://github.com/user-attachments/assets/5008812a-dbcf-41b1-9d71-de6e0d8da0bd" />


</p>
If all went well "Validation passed" should show up on the next page. Once you see that go ahead and click on 'Create' at the bottom.
<br />
<p>
<img width="695" height="379" alt="LVM 6" src="https://github.com/user-attachments/assets/d737905f-8d73-491e-9657-503a7d254304" />


</p>
Once Create is clicked, our Virtual Machine will began loading and as it's buffering we get a "Deployment is in progress" notification on the screen. When the deployment is done a notification that says "Your deployment is complete" will appear on screen. With that being said, we just set up our second virtual machine!
<br />
</p>
<img width="1480" height="548" alt="LVM 7" src="https://github.com/user-attachments/assets/1d8b76ea-9f2b-4e3f-b5aa-ad702e2c84a1" />



</p>
Let's double check to see if our Linux virtual machine was created. Click the Home button to return to the main page. On the main page click the Virtual Machines icon or type it in the search bar. From there we are taken to the Virtual Machines page & can see our Linux VM does exist along with the Windows VM we previously created. Congrats! You have now completed this project by setting up two virtual machines!
<br />
<p>
<img width="958" height="316" alt="LVM 8" src="https://github.com/user-attachments/assets/32b98098-d244-45f8-8917-3678d22bc898" />


</p>
<p>


<h2>Final Thoughts</h2>
</p>
Virtual machines are an incredible resource because they allow us to run multiple operating systems on the same physical hardware for testing or learning purposes.This project provided hands-on experience with virtualization and operating system installation, reinforcing key concepts in system administration and cross-platform compatibility. It lays a solid foundation for more advanced networking, cybersecurity, and DevOps projects.<br />
