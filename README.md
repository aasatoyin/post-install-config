<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Configure osTicket, post-installation](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Create an Azure Virtual Machine Windows 10, 4 vCPUs
- Install / Enable IIS in Windows WITH CGI and Common HTTP Features
- Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Download and install the Rewrite Module (rewrite_amd64_en-US.msi)
- Create the directory C:\PHP
- Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- Download and install VC_redist.x86.exe
- Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- Open IIS as an Admin
- Register PHP from within IIS
- Reload IIS (Open IIS, Stop and Start the server)
- Install osTicket v1.15.8
- Reload IIS (Open IIS, Stop and Start the server)
- Go to sites -> Default -> osTicket
- Note that some extensions are not enabled
- Rename: ost-config.php
- Assign Permissions: ost-config.php
- Continue Setting up osTicket in the browser (click Continue)
- Download and install HeidiSQL
- Continue Setting up osticket in the browser
- Clean up

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/VgAOIig.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
IP address is copied from VM created on Azure, default username and password generated when creating our VM were used to gain access and VM was remote login into successfully.
</p>
<br />

<p>
<img src="https://i.imgur.com/H1fisZm.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The image above showed how remote access was gained into our VM (check the IP address against the Remote Desktope Connection image 2)
</p>
<br />

<p>
<img src="https://i.imgur.com/DLuLShI.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
  
</p>
<p>
  We install / enable IIS in Windows WITH CGI and Common HTTP Features as followed: 
CGI and Common HTTP Features
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
AND IIS Management Console
Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console.   Pictuure shown above for ease of navigation

</p>
<br />

<p>
<img src="https://i.imgur.com/1hFt9KB.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
IIS is a Web server that OSticket runs on, therefore, we checked if the webserver is up and running by typing. 127.0.0.1 into web browser to load default IIS server shown the image above. 127.0.0.1 is a local host of the loopback trying to load a webpage that is running off myself, then.
</p>
<br />

<p>
<img src="https://i.imgur.com/IcNzhjF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/N68MeBh.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install the Rewrite Module (rewrite_amd64_en-US. (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/tttJZU3.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create the directory C:\PHP
</p>
<br />

<p>
<img src="https://i.imgur.com/hHc5Wt6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP as follows:  goto download>right click to Extract>browse>This PC>PHP>Extract. (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/f4TtSvF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download and install VC_redist.x86.exe (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/PSj1sZm.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) as follows: Agree>Next>Select Tropical>Install>Finish>Next>Tick Standard configuration>Next>Enter password>Next>Execute>Finish. (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/x86p96x.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Open IIS as an Admin (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/RlaH9lb.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Register PHP from within IIS as foolows: double click PHP Manager>register new PHP version>browser>This PC>window (c:)\PHP folder>php.cgi>open>okay (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/IcNzhjF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/IcNzhjF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) (image shown above)
</p>
<br />

<p>
<img src="https://i.imgur.com/IcNzhjF.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) (image shown above)
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
