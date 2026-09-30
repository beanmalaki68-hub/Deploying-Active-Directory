<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Deploying Active Diretory</h1>



https://github.com/user-attachments/assets/afb81b6c-d9ef-417e-b089-e4b85c4b1edd



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
- Setting up an environment in Active Directory 

# Step 1 - Installing Active Directory and promoting it to a Domain Controller

I then logged into the Windows Server virtual machine that I created in Microsoft Azure and installed the Active Directory Domain Services (AD DS) role. After installing AD DS, I promoted the server to a Domain Controller (DC) and configured the Active Directory domain name as BeanInc.Local.


<h2>Video Walkthrough</h2>


https://youtu.be/0_h_OKCShdU


# Step 2 - Connecting the User VM to the BeanInc.Local Domain

Next, I logged onto the User VM and joined it to the BeanInc.Local domain that I had just created. After joining the domain, I went back to the Domain Controller and used Active Directory Users and Computers (ADUC) to confirm that the User VM had successfully joined the domain and appeared in Active Directory.


<h2>Video Walkthorugh</h2>


https://youtu.be/xMEWMextKz0


# Step 3 - Prepping our Active Directory environment

Lastly, I logged into our domain controller and set up our active directory environment for my next lab.

<h2>Video Walkthrough</h2>

https://youtu.be/glvUpmM2DJw

