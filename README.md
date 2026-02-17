<img width="304" height="166" alt="image" src="https://github.com/user-attachments/assets/33ff58bf-c2a4-41fd-b424-dc71dfaa6364" />
                
# Preparing-Active-Directory-Infrastructure-in-Azure
This project demonstrates the preparation of Active Directory infrastructure in Microsoft Azure. The focus of this lab is building the foundational cloud environment required before deploying Active Directory Domain Services.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines / Virtual Network)
- Remote Desktop 
- DNS
- Command Prompt/ PowerShell

<h2>Operating Systems Used</h2>

- Windows Server 2022 (Domain Controller: DC-1)
- Windows 11 pro (Client-1)

<h2>Infrastructure Setup Steps</h2>

<h3>1. Resource Group Creation</h3>

<img width="1486" height="860" alt="01-Resource group" src="https://github.com/user-attachments/assets/1dd8197c-b7ce-4a21-9486-83c9918983f1" />



<p>
A dedicated Resource Group was created in Azure to organize all components of this lab environment. 
This allows me to manage, monitor, and control all related resources in one place.
</p>

<h3>2. Virtual Network and Subnet Configuration</h3>

<img width="1512" height="982" alt="02-Virtual Network" src="https://github.com/user-attachments/assets/afb0c58e-f27c-47fd-85bb-15a673a7f7a7" />


<p>
A Virtual Network and subnet were configured to allow communication between the Domain Controller (DC-1) and Client-1.This ensures both machines can communicate securely within the same environment.

</p>

<h3>3. Domain Controller Virtual Machine (DC-1) Deployment and Status </h3>

<img width="1512" height="982" alt="03-DC-1 VM running" src="https://github.com/user-attachments/assets/d93be32c-5507-4887-81ea-908f6dadf77f" />


<p>
A Windows Server 2022 virtual machine named DC-1 was successfully deployed in Azure and verified to be running. This server will later be promoted to a Domain Controller after the infrastructure setup is complete.
</p>

<h3>4. Client Virtual Machine (Client-1) Deployment and Status </h3>

<img width="1512" height="982" alt="04-Client-1 VM running" src="https://github.com/user-attachments/assets/896286c3-62a2-481f-984a-705bf54f6422" />


<p>
A Windows 11 Pro virtual machine named Client-1 was successfully deployed and verified to be running. This machine will serve as the client workstation within the Active Directory environment.

</p>

<h3>5. Static Private IP Configuration</h3>

<img width="1512" height="982" alt="05-Static private IP" src="https://github.com/user-attachments/assets/0357df74-89c1-4fdc-8ed1-6c4a7fd02545" />

<p>
DC-1 was configured with a static private IP address to maintain consistent DNS resolution and stable network communication within the Virtual Network.
</p>

<h3>6. Client DNS Configuration</h3>

<img width="1512" height="982" alt="06-Client 1 DNS setting" src="https://github.com/user-attachments/assets/68b4a1bb-1ff0-4b31-8c41-617ea5a63b26" />

<p>
Client-1 was configured to use DC-1’s private IP address as its DNS server, which is required for Active Directory communication.
</p>

<h3>7. Connectivity Validation (Ping Test)</h3>

<img width="1512" height="982" alt="07-Successful ping test" src="https://github.com/user-attachments/assets/819034e3-9a12-4dd9-8b9e-ed81428c508c" />


Connectivity was verified through a successful ping from Client-1 to DC-1, confirming proper Virtual Network communication and DNS configuration.
