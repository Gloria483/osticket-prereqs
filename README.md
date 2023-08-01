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
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/HhUTtWG.png://" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
