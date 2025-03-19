![image](https://github.com/user-attachments/assets/93459f11-facf-4ad2-81ab-04982c05ace7)<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This project outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [Project Walkthrough](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Install Active Directory
- Create a Domain Admin user within the domain
- Join Client-1 to your domain `mydomain.com`
- Setup Remote Desktop for non-administrative users on Client-1
- Create 1000 additional users and attempt to log into client-1 with one or more of the users

<h1>Deployment and Configuration Steps</h1>

## Install Active Directory(AD)
### Login to DC-1 and install Active Directory Domain Services
<p>
<img src="https://github.com/user-attachments/assets/630f3853-34d0-40fc-96c8-0c514537dad7" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/790dd745-b585-4cf4-9bfd-200020deb681" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/5e19dc10-d17b-4a83-ac17-9ecf653a782a" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/c9fb39c4-cf59-430e-a1fb-1fc7c914ca7e" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/336f25e5-841d-4462-a5da-753ea893b6b8" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/e80a8758-9993-4788-9033-2467b5a8d63c" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/1a2a70d9-5942-48c0-b6bc-6f1c2d9c07b4" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/9144eff9-ac29-4639-945c-32e0e4586898" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/888fd07a-a669-4674-87c4-407f3f41d4da" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/758c1c28-d17e-4fdc-a07f-eea284c7fea1" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/0936fd50-21b2-4472-8295-b8b1c1b86255" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Promote the VM as the DC(Domain Controller)
### Click on the notification icon, then click "Promote this server to a domain controller"
<br />

### Create the domain by choosing the "Add a forest" option
</p>
<p>
<img src="https://github.com/user-attachments/assets/d8414873-daa3-4daf-a50b-c156b02fc409" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Set the password for the DC(password: AdminSecurePassword123!!!)
<p>
<img src="https://github.com/user-attachments/assets/8a411fdf-c4b1-4525-8bfb-7f56d416723a" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Uncheck the "Create DNS delegation" checkbox
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

### Make sure that the NetBIOS name is correct
<p>
<img src="https://github.com/user-attachments/assets/d44bed71-d8d1-40fa-83d2-43edd785ec0b" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Continue with setup
<p>
<img src="https://github.com/user-attachments/assets/24182c93-14be-4867-80b9-57d06263c24c" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/4ca8dd8b-b2fc-4fae-81f1-8bfd76b7c981" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Make sure that there are no errors present, once installed, the server will automatically log out
<p>
<img src="https://github.com/user-attachments/assets/6a34590b-afc8-449f-a7c2-954a1afc41c8" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Log back into the domain with the following credentials
<p>
<img src="https://github.com/user-attachments/assets/c42e96ed-800f-4c24-8d0c-b7d598a5979a" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Creating a Domain User
### In Server Manager, navigate tools ---> Active Directory Users and Computers
<p>
<img src="https://github.com/user-attachments/assets/5213ecae-9f6c-49a5-b7b6-bb994d02fef6" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### In Active Directory Users and Computers, under `mydomain.com`, create two new OUs(Organizational Units) called `_EMPLOYEES` and `_ADMINS`
<p>
<img src="https://github.com/user-attachments/assets/12e581c3-3024-4c9e-a801-90c175ebb62d" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/403713bd-d7a5-4e00-9ae0-257d29ff679b" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### In `_ADMIN` OU, create a user named `Jane Doe` with the username and password of "jane_admin / Cyberlab123!"
<p>
<img src="https://github.com/user-attachments/assets/a228d65c-caba-423a-980d-b08f1d6d30a6" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/d619aa7a-0645-4f4e-b0bd-9e52170e30d6" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/2dda4a34-b488-4e53-98d6-01dd0007c6bb" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/3f603215-4e41-4740-9ea1-62b4805ca2aa" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Add `jane_admin` to the Domain Admin Security Group
<p>
<img src="https://github.com/user-attachments/assets/1c76b3f5-0182-444d-b837-fc29569a7430" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Log out then log back in as `jane_admin`
<p>
<img src="https://github.com/user-attachments/assets/5bb9857c-071b-47b6-94ab-2bb4992228e4" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/7fa4bfca-3f79-42fd-a8f9-a4314573dd1a" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Joining `client-1` to the domain
### Right click on the Windows icon, and choose system, within the system settings go to the "Rename this PC (advanced)"
<p>
<img src="https://github.com/user-attachments/assets/0fcffcb7-48e2-47b2-8dd6-f4e49425f3ff" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Change the PC name to the domain
<p>
<img src="https://github.com/user-attachments/assets/dc0a80be-64d2-4f6c-8a8f-8c21160fbc6f" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/b98c4ce3-69be-44e2-a59b-4a01f5e22302" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Enter the domain admin's credentials
<p>
<img src="https://github.com/user-attachments/assets/2e7d6fc3-ae8f-4f0f-9aa9-e144920f4284" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/f82f2d3f-6c8b-4bb2-b4a2-b19d0399f0af" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/1192901d-675f-41e9-9779-db071b73febf" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/9b311aa2-741a-4f79-93d0-df6aa03fe689" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Log into `dc-1` and confirm that `client-1` has been added to the domain
<p>
<img src="https://github.com/user-attachments/assets/ccef2412-ac90-452e-8e82-53cd66784939" width="550" alt="Disk Sanitization Steps" />
</p>
<br />


## Setup Remote Desktop for non-administrative users on Client-1
### Allow domain users to remote into other machines within the domain
<p>
<img src="https://github.com/user-attachments/assets/75ca36c0-e4d9-4da5-9391-8729010a99a2" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/35256afb-40c3-447d-a63f-d8704a272106" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Enter the crenditals of the admin
<p>
<img src="https://github.com/user-attachments/assets/57965c41-9de2-4e55-a7fb-dc62c3709421" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/eb978960-9a83-4401-9ea2-778e9badf981" width="550" alt="Disk Sanitization Steps" />
</p>
<br />


## Creating additional users
### Within powershell ISE run the following script to create 1000 users
[create_users](https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1)
<p>
<img src="https://github.com/user-attachments/assets/eb978960-9a83-4401-9ea2-778e9badf981" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/3c378a64-598f-4a47-955a-460e9ea670dd" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Log in as one of the users
<p>
<img src="https://github.com/user-attachments/assets/5eefda18-69a1-4331-a75a-8c34ba75f248" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/2ad8949b-53e6-4f56-aef6-8e54a92b07ef" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/baa7feff-0498-4ca2-a20f-f45349d15e5d" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

# End of Project
