<p align="center">
<img src="https://github.com/user-attachments/assets/3729c9bd-7cff-4dd4-830b-2efd0aee6d51" width="650" alt="Microsoft Active Directory Logo"/>
</p>


<h1>Installing and setting up Windows Server 2022 in VMware Workstation Pro</h1>
This project outlines the installation and set up of Windows Server 2022 along with the installation and management of Active Directory within VMware Workstation Pro 17.<br />


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


<br>


<h1>Deployment and Configuration Steps</h1>

## Installing and setting up Windows Server 2022
### Go to a search browser and type on the following `windows server 2022 iso download` choose the highlighed link
<p>
<img src="https://github.com/user-attachments/assets/8b4ec958-9a33-4684-ad29-01ca6860cf1c" width="550" alt="Disk Sanitization Steps"/>
</p>

### Click on the `64-bit edition` download, based on your network speed, this may take between 5-30 minutes
<p>
<img src="https://github.com/user-attachments/assets/e02ed9d9-ed8c-4074-9173-873bc0eab825" width="550" alt="Disk Sanitization Steps"/>
</p>

### Save the ISO in any location, in this case I have saved the ISO to the following location, I've also renamed the ISO image:
<p>
<img src="https://github.com/user-attachments/assets/1626d3d0-a726-4de8-80e9-73476cde68dd" width="550" alt="Disk Sanitization Steps"/>
</p>

### Open VMware Workstation Pro and create a new VM
<p>
<img src="https://github.com/user-attachments/assets/cc525cd1-4138-4a4b-84db-7d0f720788ba" width="550" alt="Disk Sanitization Steps"/>
</p>

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/b99d9086-cb9f-47e6-b9d6-6677b41b1386" width="550" alt="Disk Sanitization Steps"/>
</p>

### To aviod any issue with the VM starting up successfully, choose `I will install the operating system later.` radio option, then click next
<p>
<img src="https://github.com/user-attachments/assets/600e745f-0ce4-4dbc-abf7-bf99e481a92d" width="550" alt="Disk Sanitization Steps"/>
</p>

### Select `Microsoft Windows` as the OS, and `Windows Server 2022` as the version
<p>
<img src="https://github.com/user-attachments/assets/defaccac-cc49-4621-996c-f5e958ee37c9" width="550" alt="Disk Sanitization Steps"/>
</p>

### Give the VM a name, and choose a file path
<p>
<img src="https://github.com/user-attachments/assets/6e01934c-051b-4e20-8c81-db10ce7c3e19" width="550" alt="Disk Sanitization Steps"/>
</p>

### Depending on your computer specs, assign the necessary amount of storage to the VM
<p>
<img src="https://github.com/user-attachments/assets/223cc538-d1ad-422e-b05b-3fb40a039749" width="550" alt="Disk Sanitization Steps"/>
</p>

### Click finish
<p>
<img src="https://github.com/user-attachments/assets/6d15807f-e3f6-4fd7-96e8-0a27b432984c" width="550" alt="Disk Sanitization Steps"/>
</p>

### Go to the newly created VM, right-click on the VM and choose settings
<p>
<img src="https://github.com/user-attachments/assets/58f8f74c-6aa0-4d60-9a05-53e018668e41" width="550" height="550" alt="Disk Sanitization Steps"/>
</p>

### Based on the specs of your device, change the memory to a decent amount so that the VM will run smoothly
<p>
<img src="https://github.com/user-attachments/assets/c7d84a28-f3bd-46b9-9462-0f683fba072c" width="550" alt="Disk Sanitization Steps"/>
</p>

### Add the ISO file onto the VM
<p>
<img src="https://github.com/user-attachments/assets/ba3962db-f735-4b31-9852-d8fd28449bb8" width="550" alt="Disk Sanitization Steps"/>
</p>

### Power up the VM
<p>
<img src="https://github.com/user-attachments/assets/125cba7f-1d0d-4e98-b404-d57591b840d6" width="550" alt="Disk Sanitization Steps"/>
</p>

### Once the VM is powered on, click within the VM and rapidly press space bar or any key of your choosing until you see the following, then hit enter
<p>
<img src="https://github.com/user-attachments/assets/673de096-0f20-48aa-9ece-1defee174ec9" width="550" alt="Disk Sanitization Steps"/>
</p>

### Click Next
<p>
<img src="https://github.com/user-attachments/assets/5a2f044b-79d7-4c62-a745-a7ad0d71afce" width="550" alt="Disk Sanitization Steps"/>
</p>

### Click Install now
<p>
<img src="https://github.com/user-attachments/assets/e437c752-91c3-4064-8cc8-2583498a19c8" width="550" alt="Disk Sanitization Steps"/>
</p>

### Choose the `Windows Server 2022 Standard Evaluation(Desktop Experience)` to have a Graphical User Interface(GUI) for the VM, then click Next
<p>
<img src="https://github.com/user-attachments/assets/f0a85cc3-4c76-47a8-8e67-7bd8b1502449" width="550" alt="Disk Sanitization Steps"/>
</p>

### Go through the Mircosoft Software License Terms, click the checkbox to agree then click Next
<p>
<img src="https://github.com/user-attachments/assets/29749b67-470e-4e6b-a355-8703bf4f7a69" width="550" alt="Disk Sanitization Steps"/>
</p>

### Since this is a brand new VM with a brand new OS, choose the custom option to create a new OS
<p>
<img src="https://github.com/user-attachments/assets/150f1f9f-6ed7-467b-adf2-4589a65d9e66" width="550" alt="Disk Sanitization Steps"/>
</p>

### Ensure that the storage is correct, then click Next
<p>
<img src="https://github.com/user-attachments/assets/2386fa37-4f0d-4dec-9da3-5e05c38b45ba" width="550" alt="Disk Sanitization Steps"/>
</p>

### Depending on your network speed, the process of installing the OS can take between 5-30 minutes
<p>
<img src="https://github.com/user-attachments/assets/6ff01d6e-89c6-46b6-9d01-6a1e63f24900" width="550" alt="Disk Sanitization Steps"/>
</p>

### Once the OS has been installed, input a password, be sure to remember the password, or you will need to re-install the OS if you forget it, then click Finish
<p>
<img src="https://github.com/user-attachments/assets/1c4d5835-9756-47b6-b92a-e715181386a6" width="550" alt="Disk Sanitization Steps"/>
</p>

### After inputting the new password, press Ctrl+Alt+Insert to unlock the Windows Start Screen within the VM
<p>
<img src="https://github.com/user-attachments/assets/f8a8e5ad-710b-47b6-978f-fe4a9e39d4bb" width="550" alt="Disk Sanitization Steps"/>
</p>

### Enter the new password
<p>
<img src="https://github.com/user-attachments/assets/ed45f5f3-75f0-45de-b840-9ece2dfd4d4a" width="550" alt="Disk Sanitization Steps"/>
</p>

### Once logged in, Server Manager will be the first application that will open
<p>
<img src="https://github.com/user-attachments/assets/8c57e57d-62a4-419d-a2b7-97162208121a" width="550" alt="Disk Sanitization Steps"/>
</p>

<br>

## Installing and setting up Active Directory
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
