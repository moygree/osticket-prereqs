<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machine/Computer)
- Remote Desktop Connection
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Virtual Machine 
- Heidi SQL
- osTicket 
- Internet Information Services (IIS) 
- Remote Desktop Connection

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Before we install osTicket, we will need a virtual machine. In this case, we will use the Microsoft Azure portal to create one. We are using a virtual machine so we don't make any permanent changes to our own computer, and we can easily delete everything once we are finished. In the Azure portal, we will create a resource group. Inside your resource group, create a virtual machine preferably with 2-4 CPUs.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you've created your virtual machine, connect to it using the Remote Desktop Connection App. Enter the Public IP Address of the virtual machine, which can be found on the virtual machine's overview section inside the Microsoft Azure portal. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After connecting to our virtual machine, we are going to enable Internet Information Services, or IIS for short. Inside the control panel we are going to select uninstall a program. After you have selected uninstall a program, you will select Turn Windows Features On or Off. Then from there, enable Internet Information Services.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Excellent. Now that you have enabled IIS we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 That link will provide you with all of the material you need to download to get osTicket up and running. Simply click the link and install the Web Platform Installer
</p>
<br />
