<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Setting Up Active Directory in VMware Workstation Pro</h1>
This project outlines the installation of on-premises Active Directory within Vmware Workstation Pro 17.<br />


<h2>Environments and Technologies Used</h2>

- VMware Workstation Pro (Virtual Machines/Compute)
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022

<h2>High-Level Deployment and Configuration Steps</h2>

- Add Active Directory Domain Services to the Server
- Promote the server as the Domain Controller
- Create Organizational Units (OUs) for different departmenets
    - USA
    - Europe
    - Asia
- Create user accounts and groups within these OUs
- Add teh following groups: Users, Computers and Servers
- Add 3 Users for each Department
    - Users
        - IT
        - Accounting
        - HR
        - Sales
        - Management
    - Computers
        - IT
        - Accounting
        - HR
        - Sales
        - Management
    - Servers
        - IT
        - Accounting
        - HR
        - Sales
        - Management

<h2>Deployment and Configuration Steps</h2>

## Installing Active Directory
### Within Server Manager, go to Manage >> Add Roles and Features
<p>
<img src="https://github.com/user-attachments/assets/28842a3d-154e-43de-8485-3e4d7836935b" width="550" alt="Disk Sanitization Steps"/>
</p>

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/229024e4-d715-47fe-b00a-397feac98cac" width="550" alt="Disk Sanitization Steps"/>
</p

### Choose `Role-based or featured-based installation` then click Next
<p>
<img src="https://github.com/user-attachments/assets/ba425c71-0bc1-4645-b55c-3bad7ebe6023" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Choose `Select a Server from the server pool` then click Next
<p>
<img src="https://github.com/user-attachments/assets/1d508688-b8e0-43db-a52a-8e8acf41fca1" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Add the following Roles then click Next
<p>
<img src="https://github.com/user-attachments/assets/5e94bdbc-4f27-4062-a93e-64ca55c5f3b7" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Make sure that Group Policy Management is checked then click Next
<p>
<img src="https://github.com/user-attachments/assets/f307695c-87e9-4564-9ce1-3b1cb2590804" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/77959899-5038-4fa1-8016-40075507d483" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/04518211-0b0a-44f9-82c1-9745446b0fa6" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/79ff65e1-449a-4786-851b-acbb813cb05a" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Select the following Role services, then click Next
<p>
<img src="https://github.com/user-attachments/assets/e221127b-cde8-4160-97aa-eed641ccb889" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/076e5d5f-5a86-4ff1-99d7-4d11f068e8f1" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### By default the following services will be check, click Next
<p>
<img src="https://github.com/user-attachments/assets/4206d866-4581-478d-8497-2900766c3929" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Install after review all of the Roles and Features
<p>
<img src="https://github.com/user-attachments/assets/0f1faa61-9f8b-4054-a55b-89aa8d2472d8" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Promoting the server as a Domain Controller
### Once the installation for AD DS has been completed click on `Promote this server to a domain controller`
<p>
<img src="https://github.com/user-attachments/assets/f248377a-3ec0-4b51-80a3-e6bbc657cc39" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


### Under `Select the deployment operation` choose `Add a forest`
<p>
<img src="https://github.com/user-attachments/assets/8476ea97-8ec8-48ff-9bea-b7f090215362" width="550" alt="Disk Sanitization Steps" />
</p>
<br />


### Provide a domain name, in this case I will use `chaan.com` as the domain name, then click Next
<p>
<img src="https://github.com/user-attachments/assets/51e51975-7f49-4e2e-957e-620849c6b0b0" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Be sure to keep the `Forest Function Level` and `Domain Function Level` set to Windows Server 2016, and enter a secure password for the domain, then click Next
<p>
<img src="https://github.com/user-attachments/assets/76448cce-6dde-4b46-8512-4557912893b8" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/67fc6372-8d5d-4996-b6d9-60edaa365f82" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### The NetBIOS domain name will appear as the domain name without the `.com`, click Next
<p>
<img src="https://github.com/user-attachments/assets/b20f1ea0-1b84-4f67-8ea1-e83431ad1177" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Create the Client VM
<p>
<img src="https://github.com/user-attachments/assets/4464316f-abee-404d-ae8b-b2b088ea2692" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/164d5f17-eab8-4069-a19a-0290babcd27e" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/0d3405ee-d765-4377-b9b6-ca7e57dba340" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/aa6d7898-799f-4492-8837-8a8368a47cd8" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Be sure to check the Licensing to avoid any errors
<p>
<img src="https://github.com/user-attachments/assets/81729691-70c9-4e22-8252-53bbb41403a4" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Click on the Network section and assign the `windows-vnet` to the VM
<p>
<img src="https://github.com/user-attachments/assets/12f9bb63-b623-4c2f-a656-5e54882d75af" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/c10dbb36-1000-47dd-aee9-3aaf3213cbb0" width="550" alt="Disk Sanitization Steps" />
</p>
<br />

### Set `client-1` DNS settings to match `dc-1` Private IP address
<p>
<img src="https://github.com/user-attachments/assets/b0729472-1c35-4ec5-a92c-8658ba2af405" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/2a1f8bf2-a9f3-4fac-be5c-7ef9534cd4ce" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/2a1f8bf2-a9f3-4fac-be5c-7ef9534cd4ce" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/63ade75b-fedd-4798-86be-6cd3d7cf446a" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Get the private IP address from `dc-1`
<p>
<img src="https://github.com/user-attachments/assets/605cd1e8-ffcc-45a5-b817-61236d9aaecb" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Enter `dc-1` private IP address as the DNS server for `client-1`
<p>
<img src="https://github.com/user-attachments/assets/dc8b5e32-ecdb-4719-822b-dd472bf96306" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Restart `client-1` from the Azure Portal
<p>
<img src="https://github.com/user-attachments/assets/813ef37b-6794-458e-af21-759faa6c8719" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/813ef37b-6794-458e-af21-759faa6c8719" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Log into `client-1` and run the `ipconfig /all` command to view all internet protocal configurations
<p>
<img src="https://github.com/user-attachments/assets/f5ea1c2e-a2dd-4da7-b028-5870a012b1d4" width="550" alt="Disk Sanitization Steps"/>
</p>


---

<br />


# End of Project
