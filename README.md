<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Installing and setting up Windows Server 2022 in VMware Workstation Pro</h1>
This project outlines the installation of on-premises Active Directory within Vmware Workstation Pro 17.<br />


<h2>Environments and Technologies Used</h2>

- VMware Workstation Pro (Virtual Machines/Compute)
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022

<h2>High-Level Deployment and Configuration Steps</h2>

- Install and set up Windows Server 2022 onto the VM
- Add Active Directory Domain Services to the Server
- Promote the server as the Domain Controller
- Create Organizational Units (OUs) for different departmenets
    - USA
    - Europe
    - Asia
- Create user accounts and groups within these OUs
- Add the following groups: Users, Computers and Servers
- Add the following departments
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

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/bbe830c7-bc35-40ea-9299-2687120c77ba" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/1a773e7e-90d4-4455-af36-9b8ef2dc2019" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Click Install
<p>
<img src="https://github.com/user-attachments/assets/23f51a4c-d07d-46a4-af6a-f7801a605595" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Once the installation is complete, you will be prompted with the following message, the VM will automatically sign out in 5-10 seconds depending in Internet speed
<p>
<img src="https://github.com/user-attachments/assets/376f6be1-e617-4c12-97de-2bc27d839d24" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Enter in the password that was created for the domain
<p>
<img src="https://github.com/user-attachments/assets/59b1c7bc-eb2c-4323-9b33-1e12f18c5d3f" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Go to Server Manager, then click on Tools, you will see all of the features for Active Directory, along with others that was installed
<p>
<img src="https://github.com/user-attachments/assets/fed75294-b6e8-4c8c-b997-9e6c71d95a49" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Create Organizational Units (OUs) for different departmenets
### Go to Server Manager >> Tools >> Active Directory Users and Computers
<p>
<img src="https://github.com/user-attachments/assets/bb40457e-2cc0-4f6e-8c24-89df2705f615" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/261fc132-3ab6-4c34-bebf-8a2af3031e5e" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Right click on the domain name >> New >> Organizational Unit
<p>
<img src="https://github.com/user-attachments/assets/b7136025-5de1-47e3-b2d2-2e6c7587fd5b" width="550" alt="Disk Sanitization Steps"/>
</p>

### Create the following OUs: `USA`, `Europe` and `Asia`
<p>
<img src="https://github.com/user-attachments/assets/8da67ea5-e38b-4202-9a86-e0306bc4a139" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/2b377d3e-f458-4454-b43e-a80bfe2db4b9" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/6e6dfa77-32a9-4695-b6ba-8cf73e639593" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/dca8c28c-47af-42bb-9dce-e64648637fa4" width="550" alt="Disk Sanitization Steps"/>
</p>

### Create the following OUs within the `USA` OU, `Europe` OU and `Asia` OU: `Users`, `Computers` and `Servers`
<p>
<img src="https://github.com/user-attachments/assets/cf1f2a63-9761-4010-8bcf-905e6e7569aa" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/418e2c8e-db1e-46ff-bb60-bbd5266efaf4" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/a1d8e3f6-cae3-417a-8087-a49b6eace479" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/843ea783-1ecc-46dd-88a8-99ae3c8d41e7" width="550" alt="Disk Sanitization Steps"/>
</p>

### Create the following OUs in the `Users`, `Computers` and `Servers` OUs within the `USA`, `Asia` and `Europe` OUs: `IT`, `Accounting`, `HR`, `Sales`, `Management`
<p>
<img src="https://github.com/user-attachments/assets/74267fb9-6096-4c7b-8e0b-3b67c02788f7" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/d75fca2f-818a-4d4a-b273-2f4cbb260cba" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/75760e07-5637-4f67-8e22-ee8acd58da6f" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/9da2c04f-d214-4e5d-b305-daec929d85d9" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/78dc1c95-297d-4b3a-b7c6-70168fa6372b" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/45f52336-7d1d-40a5-a3c0-5811d93d06df" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/45f52336-7d1d-40a5-a3c0-5811d93d06df" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/11be43f7-2983-4ba6-8b7b-bc124bdf93d0" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/6ca0329f-35cd-4ff5-b66d-702275440224" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/ef10ce1f-c840-4887-b460-2d935a8ce6b9" width="550" alt="Disk Sanitization Steps" />
</p>

## Adding Groups
### Create the groups and users for each department
### Group
<p>
<img src="https://github.com/user-attachments/assets/ad1b2a1a-5ac4-479b-b0ec-892aef569d06" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/88b5f26e-44cd-4005-bdb7-350b8c9fee3f" width="550" alt="Disk Sanitization Steps" />
</p>


### User
<p>
<img src="https://github.com/user-attachments/assets/b550a1df-8151-42c3-bc8c-4f5dda79dee5" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/06ed3367-693d-46ba-a84c-d029ee6b09a1" width="550" alt="Disk Sanitization Steps" />
</p>

### Set a password for the user
### Once the user input their password for the very first time, they will need to change their password afterwards
<p>
<img src="https://github.com/user-attachments/assets/720ff7bf-002a-4696-9e60-658dd0cb46e9" width="550" alt="Disk Sanitization Steps" />
</p>
<p>
<img src="https://github.com/user-attachments/assets/c05b162f-768e-4022-9827-ad383fd51f01" width="550" alt="Disk Sanitization Steps" />
</p>

---

<br />


# End of Project
