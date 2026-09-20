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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
