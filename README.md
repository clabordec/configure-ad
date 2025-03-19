<p align="center">
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

### Make sure that there are no errors present
<p>
<img src="https://github.com/user-attachments/assets/6a34590b-afc8-449f-a7c2-954a1afc41c8" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />



