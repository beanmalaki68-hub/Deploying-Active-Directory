<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Deploying Active Diretory</h1>
This lab focuses on deploying and configuring Active Directory (AD) in the Azure environment created in the previous lab. The existing Domain Controller (DC-1) and Client-1 virtual machines are started and configured to establish a functional Active Directory domain. The lab includes installing Active Directory Domain Services (AD DS) on DC-1, creating a new Active Directory forest, creating administrative users and Organizational Units (OUs), joining Client-1 to the domain, and verifying the computer account in Active Directory Users and Computers (ADUC).

The second part of the lab expands the environment by allowing non-administrative domain users to connect to Client-1 through Remote Desktop and using PowerShell to create multiple additional domain accounts.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2025
- Windows 11 Pro (25H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Deploy Active Directory Domian Services
- Build the Active Directory Organizational Structure 
- Join Client-1 to the Domain
- Configure Domian User REmote Access
- Automate User Creation and Verify

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1827" height="977" alt="image" src="https://github.com/user-attachments/assets/b4cf5dba-0f46-4128-b03b-00bb787b27fc" />

</p>

- I first wanted to log back into the DC-1 & client-1 from the first lab.
- DC-1 and Client-1 were created in the previous Azure infrastructure lab. This lab builds on that existing environment rather than creating new virtual machines.
<br />

<p>
<img width="970" height="690" alt="image" src="https://github.com/user-attachments/assets/bf023c35-1b55-4556-9a62-9c1fd51b1e55" />

</p>

- The first major configuration step is installing Active Directory Domain Services (AD DS).
- Active Directory Domain Services provides the centralized identity and directory infrastructure used to manage users, computers, groups, authentication, and other domain resources.
  
<br />

<p>
<img width="948" height="698" alt="image" src="https://github.com/user-attachments/assets/167025f3-b56f-4009-b016-e0524eb96bb1" />

</p>

- After installing AD DS I promoted DC-1 to a Domain Controller.
- I promoted DC-1 to a Domain Controller and created a new Active Directory forest using mydomain.com.
- Creating the forest establishes the Active Directory domain environment that will be used to centrally manage users and computers.


<br />

<img width="925" height="636" alt="image" src="https://github.com/user-attachments/assets/efc016d9-3115-453a-900b-fad949dea241" />

- I then created two Organizational Units(OU), called _EMPLOYEES & _ADMINS
- Organizational Units help organize Active Directory objects.
- These will be important later when creating and managing new users


<img width="1028" height="669" alt="image" src="https://github.com/user-attachments/assets/cca00454-068f-451a-a0c8-2ddfd6208975" />


- I then created and new user in _ADMINS called Jane_admins and added that user to the domain's admins security group.
- Instead of continuing to use the original administrative account for all tasks, this lab creates a dedicated administrative account.
- Security groups allow permissions to be assigned to groups of users instead of configuring permissions individually.
