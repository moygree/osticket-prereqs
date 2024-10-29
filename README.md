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

![image](https://github.com/user-attachments/assets/6b3ead02-8e77-448e-8454-f3a1b6869eaf)

<p>
</p>
<p>
Before we install osTicket, we will need a virtual machine. In this case, we will use the Microsoft Azure portal to create one. We are using a virtual machine so we don't make any permanent changes to our own computer, and we can easily delete everything once we are finished. In the Azure portal, we will create a resource group. Inside your resource group, create a virtual machine preferably with 2-4 CPUs.
</p>
<br />

<p>
<img src="https://i.imgur.com/f7mrpwV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you've created your virtual machine, connect to it using the Remote Desktop Connection App. Enter the Public IP Address of the virtual machine, which can be found on the virtual machine's overview section inside the Microsoft Azure portal. 
</p>
<br />

<p>
<img src="https://i.imgur.com/qtEnuWu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After connecting to our virtual machine, we are going to enable Internet Information Services, or IIS for short. Inside the control panel we are going to select uninstall a program. After you have selected uninstall a program, you will select Turn Windows Features On or Off. Then from there, enable Internet Information Services.
</p>
<br />

<p>
<img src="https://i.imgur.com/AxHCfQ6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Excellent. Now that you have enabled IIS we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 That link will provide you with all of the material you need to download to get osTicket up and running. Simply click the link and install the Web Platform Installer
</p>
<br />

<p>
<img src="https://i.imgur.com/JJ8bZeJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you have installed Web Installer Platform open it. From inside the application you are going to install MySQL 5.5 Afterwards install x86 version of PHP up until 7.3. Some files will inevitably fail such as C++ redistributable package and the PHP manager for IIS. You can access those files in the install link. On the off chance that PHP 7.3.8 failed to be installed it can also be accessed within the install link.
</p>
<br />

<p>
<img src="https://i.imgur.com/TUGiSKi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
</p>
<br />

<p>
<img src="https://i.imgur.com/4AkTkV0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
</p>
<br />

<p>
<img src="https://i.imgur.com/nezgcWd.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket Then double click on PHP manager. Click on "Disable or enable an extension" Make sure "php_imap.dll" is enabled. Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and observe the changes "Intl Extension" should now be enabled.
</p>
<br />

<p>
<img src="https://i.imgur.com/1nYaYGe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php Assign permissions to ost-config.php Disable inheritance->Removeall New Permissions->Everyone->all
</p>
<br />

<p>
<img src="https://i.imgur.com/RmVk3q5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Afterwards continue setting up osTicket in the browser (click continue) then you will name the Helpdesk to your liking. Select a default email that will receive emails from customers who submit tickets.
</p>
<br />

<p>
<p>Continue Setting up osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1 Click “Install Now!”
Congratulations, hopefully it is installed with no errors!
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
