<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

we need Azure Virtual Machine and Installation files which include:
- Heidi SQL
- MySQL 
- PHP manager for IIS(PHPManagerForIIS_V1.5.0.msi)
- php-7.3.8
- Rewrite Module(rewrite_amd64_en-US.msi)
- VC_redist.x86.exe
- osTicket-v1.15.8

<h2>Installation Steps</h2>
<P>To begin with, we need to create an Azure virtual machine. we have to create a resource group in my case it was "RS-A", the VM name titled "VM-osTickets" with 4 CPUs(but you can choose 2-4 CPUs). The reason why we're using a virtual machine is to protect our physical machine in case an incident happens plus VM provides several advantages over physical machines such as VMs can run multiple operating system environments on a single physical computer, saving physical space, time, and management costs. </P>
<p>
<img src="https://i.imgur.com/amCDMs3.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Moving Forward, connect to your newly created VM using RDP. In my case I was using MAC I had to download Microsoft RDP and to connect to it we use a public IPv4 address obtained after creating the VM then you double-click on it and provide the username and password of your VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/NRFUI3a.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the virtue of being connected to your VM, you will have to enable IIS. Simply access the control panel then select uninstall a program. Off to the left select "Turn Windows features on or off". A list will appear then you will enable Internet Information Services.


</p>
<br />

<p>
<img src="https://i.imgur.com/HhUTtWG.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To verify if you enabled Internet Information Services(IIS) successfully, you type "127.0.0.1" if your result looks like the picture below good job else you can always go back through the installation process and check what went wrong.
</p>

<p>
<img src="https://i.imgur.com/oh116PS.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we are going to install all other prerequisites which include:
PHP manager for IIS(PHPManagerForIIS_V1.5.0.msi),Mysql, PHP-7.3.8, Heidi SQL,Rewrite Module(rewrite_amd64_en-US.msi),VC_redist.x86.exe,osTicket-v1.15.8
you can use this link to access all of the material you need to download to get osTicket up and running: "https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"
</p>

<p>
<img src="https://i.imgur.com/jCiQ1Iw.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After downloading osTickets, Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterward, rename the folder to osTicket
</p>

<p>
<img src="https://i.imgur.com/Zj3eC7r.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS Manager and restart the server. Once inside the IIS manager go to Sites->Default->osTicket on the right, and click "Browse*.80" From there your default browser should open the osTicket webserver.
</p>

<p>
<img src="https://i.imgur.com/EnVoZdX.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into the IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket Then double click on PHP manager. Click on "Disable or enable an extension" Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and observe the changes "Intl Extension" should now be enabled.


</p>

<p>
<img src="https://i.imgur.com/dkeRuzE.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sample config.php and rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php Assign permissions to ost-config.php Disable inheritance->Removeall New Permissions->Everyone->all
</p>
<p>
<img src="https://i.imgur.com/RNJ994A.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, create a database using Heidi SQL 
</p>
<p>
<img src="https://i.imgur.com/0IXdH8z.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Afterward, continue setting up osTicket in the browser (click continue) then you will name the Helpdesk to your liking. Select a default email that will receive emails from customers who submit tickets, MySQL Database: osTicket, MySQL Username: root MySQL, Password: Password1. Click “Install Now!” Congratulations, hopefully, it is installed with no errors! 
</p>
<p>
<img src="https://i.imgur.com/8u1zqI7.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> Clean up Delete: C:\inetpub\wwwroot\osTicket\setup Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</p>






</p>

<br />
