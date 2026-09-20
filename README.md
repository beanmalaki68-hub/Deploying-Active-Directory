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

<img width="955" height="580" alt="image" src="https://github.com/user-attachments/assets/81a895f5-1fa0-417a-825f-10f4148b056e" />

- I logged into client-1 and joined it to the domian.
- Joining the client to the domain allows centralized authentication and management through Active Directory.

  <img width="933" height="659" alt="image" src="https://github.com/user-attachments/assets/50231aa3-ce13-421e-b09a-ef710793a498" />

- I then logged back into DC-1 and jane_admin to verify that client-1 was in active directory

# Part 2 of this lab

<img width="908" height="888" alt="image" src="https://github.com/user-attachments/assets/2961c5f9-afc5-4edb-9687-19d5a759b32d" />

- I first log into client-1 using the admin account Jane_admin
- Then once I have logged in I change the settings to allow all domain users the ability to remote into client-1
- Remote Desktop allows administrators and authorized users to remotely access Windows computers.
- The lab demonstrates how access can be granted to a domain group instead of manually configuring each individual user.

<img width="1696" height="866" alt="image" src="https://github.com/user-attachments/assets/4613cff2-2dc4-4ebe-8646-25efc8c1f76c" />


- I then logged one DC-1 and ran Powershell ISE with ADMIN privileges.
- I ran the provided PowerShell script to automatically create multiple Active Directory user accounts.
- Automation is an important system administration skill.
- PowerShell can significantly reduce the time required to perform repetitive tasks such as creating multiple user accounts.


<img width="922" height="632" alt="image" src="https://github.com/user-attachments/assets/824b40b6-e6be-4f68-af98-edcd091dddd7" />


- I then used Active Directory to verify that the script works and the accounts are being created by PowerShell
- Verification confirms that the automation successfully created the intended Active Directory objects.


<img width="1249" height="983" alt="image" src="https://github.com/user-attachments/assets/3581c1d0-fc07-48ff-8553-cb902d41a4ce" />

- I attempted to authenticate to Client-1 using one of the accounts created through PowerShell.
- This provides an end-to-end verification of the user creation process:

PowerShell Script
       ↓
Active Directory User
       ↓
Domain Authentication
       ↓
Client-1
       ↓
Successful Login


# Summary

This lab focused on deploying and configuring an Active Directory environment using Microsoft Azure. I installed Active Directory Domain Services on DC-1, promoted the server to a Domain Controller, and created the mydomain.com Active Directory forest. I then created Organizational Units for employees, administrators, and client computers, created a dedicated Domain Admin account, and joined Client-1 to the domain.

The lab also provided hands-on experience with Remote Desktop access for domain users and PowerShell automation. Multiple Active Directory accounts were created using a PowerShell script and verified through Active Directory Users and Computers. Finally, a newly created domain account was tested by logging into Client-1, demonstrating the complete process from account creation to domain authentication.
