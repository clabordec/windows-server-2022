<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Setting Up Active Directory in VMware Workstation Pro</h1>
This project outlines the installation of on-premises Active Directory within Vmware Workstation Pro 17.<br />


<h2>Environments and Technologies Used</h2>

- VMware Workstation Pro (Virtual Machines/Compute)
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022

<h2>High-Level Deployment and Configuration Steps</h2>

- Add Active Directory Domain Services to the Server
- Create a Virtual Network
- Create a Domain Controller with the Windows Server 2022 Datacenter OS named `dc-1`
    - Username: adminuser
    - Password: AdminSecurePassword123!!!
- Create a CLient VM with the Windows 10 Pro OS name `client-1`
    - Username: labuser
    - Password: SecurePassword123!!!
- Assign `client-1` DNS settings to match the private IP address from `dc-1`

<h2>Deployment and Configuration Steps</h2>

## Create Virtual Network
### Within Azure create a virtual network, this vn with allow the Virtual Machiness to communicate within the same network
<p>
<img src="https://github.com/user-attachments/assets/ad2197a9-c243-4080-a395-6775cce5ad10" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/091eb8ec-bd16-460a-810e-02ed50089eec" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/b54cf44c-1ffb-4e54-9c7c-d7905435191e" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/2ef952ef-9b55-4f0c-8b25-7223e54312f1" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/ee40c40e-a48f-4f5e-8925-6492477fc548" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />


## Create the Domain Controller VM
<p>
<img src="https://github.com/user-attachments/assets/03fe46f0-14cd-4409-8521-ff6f95d09b46" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/984a29d1-5a11-437d-aa9a-4477b5f5e269" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/6600e096-fe7d-4892-94bf-aeb886e6152a" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/17b0f803-57b2-41b9-8d77-0e029fb00d7c" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/5dcb7277-92dc-4ddd-9bb6-fc58871020b7" width="550" alt="Disk Sanitization Steps"/>
</p>
<br />

### Be sure to check the Licensing to aviod any errors
<p>
<img src="https://github.com/user-attachments/assets/bef855ee-cdf5-42d8-89b3-c9d63783953f" width="550" alt="Disk Sanitization Steps" />
</p>
<br />


### Click on the Network section and assign the `windows-vnet` to the VM
<p>
<img src="https://github.com/user-attachments/assets/46cbaada-41c5-4b4a-8ff2-56c7c03cd2a0" width="550" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/aa0a4ed0-dc9d-42c9-9f5d-668c4d5a1d6b" width="550" alt="Disk Sanitization Steps"/>
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
