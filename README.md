[
](https://www.google.com/imgres?q=microsoft%20azure%20logo&imgurl=https%3A%2F%2Fwww.bizstream.com%2Fwp-content%2Fuploads%2F2022%2F04%2Fmicrosoft-azure-logo.png&imgrefurl=https%3A%2F%2Fwww.bizstream.com%2Ftechnology%2Fazure%2F&docid=J2s0Ai9tsO-N6M&tbnid=GszYxn5eIJWdwM&vet=12ahUKEwjzw4XW4N6SAxWCFVkFHXiYDp0QnPAOegQIJRAB..i&w=1000&h=342&hcb=2&ved=2ahUKEwjzw4XW4N6SAxWCFVkFHXiYDp0QnPAOegQIJRAB)<img width="384" height="131" alt="image" src="https://github.com/user-attachments/assets/9c52ba68-a6ae-4d26-8031-b4ea14352c3d" />
# Preparing-Active-Directory-Infrastructure-in-Azure
This project demonstrates the preparation of Active Directory infrastructure in Microsoft Azure. The focus of this lab is building the foundational cloud environment required before deploying Active Directory Domain Services.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines / Virtual Network)
- Remote Desktop 
- DNS
- Command Prompt/ PowerShell

<h2>Operating Systems Used</h2>

- Windows Server 2022 (Domain Controller: DC-1)
- Windows 10 (Client-1)

<h2>Infrastructure Setup Steps</h2>

<h3>1. Resource Group Creation</h3>

<img width="1512" height="982" alt="01-Resource-group" src="https://github.com/user-attachments/assets/1f252139-1ee9-452c-af52-90c84e02cfe4" />

<p>
A dedicated Resource Group was created in Azure to organize all components of this lab environment. 
This allows centralized management of related resources.
</p>

<h3>2. Virtual Network and Subnet Configuration</h3>

<img width="1512" height="982" alt="02-Virtual Network" src="https://github.com/user-attachments/assets/82c23c71-4877-44db-84ea-25f45773abed" />

<p>
A Virtual Network and subnet were configured to allow communication between DC-1 and Client-1 within the same Azure region.
</p>

<h3>3. Domain Controller Virtual Machine (DC-1)</h3>

<img width="1512" height="982" alt="03-DC-1 VM running" src="https://github.com/user-attachments/assets/7e359d38-af14-415c-83b9-aec06fea34df" />

<p>
A Windows Server 2022 virtual machine named DC-1 was deployed to serve as the future Domain Controller.
</p>

<img width="1512" height="982" alt="03-Client-1 VM running" src="https://github.com/user-attachments/assets/b9682f22-83e6-43be-b192-84868a71756c" />

<p>
A Windows Server 2022 virtual machine named Client-1 was deployed to serve as the Client
</p>

<h3>4. Static Private IP Configuration</h3>

<img width="1512" height="982" alt="04-Static private IP" src="https://github.com/user-attachments/assets/3320fbf4-8b93-482d-8f41-d56273f6f0a4" />

<p>
DC-1 was configured with a static private IP address to ensure reliable DNS resolution and consistent network communication.
</p>

<h3>5. Client DNS Configuration</h3>

<img width="1512" height="982" alt="05-Client 1 DNS setting" src="https://github.com/user-attachments/assets/88ec29f2-64a4-4635-94ab-79db1280582e" />

<p>
Client-1 was configured to use DC-1’s private IP address as its DNS server, which is required for Active Directory communication.
</p>

<h3>6. Connectivity Validation (Ping Test)</h3>

<img width="1512" height="982" alt="06-Successful ping test" src="https://github.com/user-attachments/assets/a1e4f0ec-3e28-4aa3-bb0e-014ca40aa11d" />


