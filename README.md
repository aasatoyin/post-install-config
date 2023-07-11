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
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics.


<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/VgAOIig.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It is possible that the IP address would change if you've log out of your VM or lost connection in the installation stage, so login to Azure portal to copy a new VM IP address. Reconnect to VM as follows: Open RDP and paste the VM IP address -> enter default username and password generated when creating VM -> ok to remotely gain access to VM.
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

Admin Panel -> Agents -> Roles -> Add New Role -> Defination (Name it Supreme Admin) -> Permission -> Ticket -> Task -> Knowledged -> Add Role. Tick all boxes because we are given full permission to this supreme admin. 

For the purpose of this project we have created a role that can do everything in the organization. Note that you can assign permission based on role.
</p>
<br />

<p>
<img src="https://i.imgur.com/bIA2mCS.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure Departments: Since tickets are routed through Departments in the help desk, there are many settings that can be set for each Department.

Admin Panel -> Agents -> Department -> Add Department -> Settings (Name it System Administrator) -> Access. Note: there are whole lot of what we can do when creating department but we just limit it to typing the name of the department and click on 'create dept' to make sure the project is not too long.

Department created successuly as 'System Administrator' form the image shown above.
</p>
<br />

<p>
<img src="https://i.imgur.com/tZJRAqG.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure Teams: Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter. Having Agents from different Departments assigned to a Team will supersede the parameters of the Agents’ Department rules. For example, you can create a Help Topic associated with a particular product you produce, and assign it to a Team of specialist Agents from different Departments. A Team can have an appointed leader who can receive Alerts & Notices separate from other team members. In order to set a Team Leader you can choose an Agent from the Team Lead dropdown when creating a Team or Editing an existing Team.

To create a Team in your Admin Panel, locate the Agents tab, and click on Teams. Then click Add New Team on the right, and fill out the appropriate information. Then you will be able to add Agents to the team by clicking on their name from your list of Agents and checking the corresponding box next to the Team name you wish to add them at the bottom of the page.

</p>
<br />

<p>
<img src="https://i.imgur.com/x6lOInK.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure Agents: Agents are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department. Agents can be given Extended Access to additional departments of the help desk as well as assigned different Roles to those departments; this can be configured in the Access tab of the Agent’s Profile.

Admin Panel -> Agents -> Add New Agent -> and fill out the appropriate information. Note: We can configure a whole lot of thing here such as assign permission, Set or reset agent password, assign agent to Team, assign department, assign team, assign extended access and so on. Note: We can add as many agents as possible y repeating this process.
</p>
<br />

<p>
<img src="https://i.imgur.com/3Xnj3of.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure Users: Users can now create an account and log-in to create a ticket or check a ticket’s status. As always with osTicket, users or ticket creators are associated with their email address as the unique identifier of each user. The User Directory, located on the Agent Panel, allows agents to search tickets by user as well as create Organizations to associate the user to. Agents can be configured as internal Account Managers for tickets created by users of an Organization.

What is a User?
Users are the ticket owners of the tickets in the help desk. When a ticket is created in the help desk, the user is associated with their email address in the User Directory of the help desk. Users can be added or deleted from the User Directory of the help desk at any time. Please note, if the user is deleted the tickets of the user must also be deleted.

A user is created in the Agent Panel, so we will switch to agent panel at the top right of the page : Agent panel -> USer > Add User > and fill out the appropriate information. Note: We can add as many user as possible by repeating this process.
</p>
<br />


<p>
<img src="https://i.imgur.com/nsKqjM7.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure SLA: SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.

SLA Plans can be created by going to the Admin Panel > Manage > SLA Plans. Click on the top right of the table to “Add New SLA Plan.” Note: SLA plan is configured based on the organization SOP and SLA schedule.
</p>
<br />

<p>
<img src="https://i.imgur.com/af59u8H.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure Help Topics: Help Topic is like a quick guide that helps user to choose the right Topic for their ticket. For instance, Business Critical Outage, Personal Computer Issues, Equipment Request, Password Reset and so on.

Help Topics can be created by going to the Admin Panel -> Manage -> Help Topics


</p>
<br />
