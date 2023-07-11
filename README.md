<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

 **The following objectives were met in this post installation stage.**
- Configure Roles
- Configure Departments
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics.


<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/VgAOIig.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It is possible that the IP address would change if you've log out of your VM or lost connection in the installation stage, so login to Azure portal to copy a new VM IP address. Reconnect to VM as follows: Open RDP and past the VM IP address -> enter default username and password generated when creating VM -> ok to remotely gain access to VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/H1fisZm.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Remote access gained succefully.
</p>
<br />

<p>
<img src="https://i.imgur.com/D25cyWC.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Copy and paste admin URL on your VM browser -> login with admin user name and password created from the installation stage. osticket page will load as shown in the above image. 
  
 Admin URL- http://localhost/osTicket/scp/login.php
</p>
<br />

<p>
<img src="https://i.imgur.com/SJsQO93.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Possibly this page will come up if you click login. However, you can navigate between agent and admin panel at the tope right of the page as shown in image. Note that the above image is currently in agent panel then you can click admin panel to navigate from the current panel.
</p>
<br />

<p>
<img src="https://i.imgur.com/BEkZjQZ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Configure Roles: Roles are the permissions granted to Agents per Department that they have access to. Each Role has a set of permissions that can be checked/unchecked for agents given that Role in association with a Department they have access to. An unlimited number of roles can be created and assigned to Agents with access to various departments.

Admin Panel -> Agents -> Roles -> Add New Role -> Defination (Name it Supreme Admin) -> Permission -> Ticket -> Task -> Knowledged -> Add Role. Tick all boxes because we are given full permission to this supreme admin



</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
