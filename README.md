<img width="384" height="131" alt="image" src="https://github.com/user-attachments/assets/dcb2d4b4-0864-45ef-9cc1-3d12e9b1bfd4" />

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

<img width="1512" height="982" alt="01-Resource-group" src="https://github.com/user-attachments/assets/1f252139-1ee9-452c-af52-90c84e02cfe4" />

<p>
A dedicated Resource Group was created in Azure to organize all components of this lab environment. 
This allows me to manage, monitor, and control all related resources in one place.
</p>

<h3>2. Virtual Network and Subnet Configuration</h3>

<img width="1512" height="982" alt="02-Virtual Network" src="https://github.com/user-attachments/assets/82c23c71-4877-44db-84ea-25f45773abed" />

<p>
A Virtual Network and subnet were configured to allow communication between the Domain Controller (DC-1) and Client-1.This ensures both machines can communicate securely within the same environment.

</p>

<h3>3. Domain Controller Virtual Machine (DC-1)</h3>

<img width="1512" height="982" alt="03-DC-1 VM running" src="https://github.com/user-attachments/assets/7e359d38-af14-415c-83b9-aec06fea34df" />

<p>
The Windows Server 2022 virtual machine named DC-1 was promoted to a Domain Controller to manage authentication and directory services.
</p>

<h3>4. Client Virtual Machine Deployment (Client-1)</h3>

<img width="1512" height="982" alt="03-Client-1 VM running" src="https://github.com/user-attachments/assets/b9682f22-83e6-43be-b192-84868a71756c" />

<p>
A Windows 11 pro virtual machine named Client-1 was deployed to simulate a client workstation within the network.
</p>

<h3>5. Static Private IP Configuration</h3>

<img width="1512" height="982" alt="04-Static private IP" src="https://github.com/user-attachments/assets/3320fbf4-8b93-482d-8f41-d56273f6f0a4" />

<p>
DC-1 was configured with a static private IP address to ensure reliable DNS resolution and consistent network communication.
</p>

<h3>6. Client DNS Configuration</h3>

<img width="1512" height="982" alt="05-Client 1 DNS setting" src="https://github.com/user-attachments/assets/88ec29f2-64a4-4635-94ab-79db1280582e" />

<p>
Client-1 was configured to use DC-1’s private IP address as its DNS server, which is required for Active Directory communication.
</p>

<h3>7. Connectivity Validation (Ping Test)</h3>

<img width="1512" height="982" alt="06-Successful ping test" src="https://github.com/user-attachments/assets/a1e4f0ec-3e28-4aa3-bb0e-014ca40aa11d" />

I verified connectivity by successfully pinging DC-1 from Client-1. This confirms that the Virtual Network and DNS settings were configured correctly.

