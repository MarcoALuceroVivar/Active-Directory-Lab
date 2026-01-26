# Active-Directory-Lab
🛡️ Enterprise Identity & Data Governance Lab

📌 Executive Summary
In a modern business environment, decentralized systems pose significant risks. Without centralized control, every computer acts as a "management island," creating massive security vulnerabilities, inefficient data silos, and an unmanageable overhead for IT departments.

This project simulates the implementation of a Centralized Identity Management System using Microsoft Active Directory. By architecting a Primary Domain Controller, I established a "Single Source of Truth" for the network. This infrastructure enables a single administrator to manage thousands of identities and assets from a unified interface, enforcing rigorous security policies and granular data access across the entire organization.

🏗️ Key Technical Pillars
🔐 Centralized Authentication
* Domain Integration: Transitioned from insecure local accounts to a unified Machine.org domain.
* Scalability: Enabled seamless "roaming" profiles and centralized security auditing for all network logins.

📡 Network Service Engineering
* Static Infrastructure: Engineered a reliable backbone using static IPv4 addressing (10.1.10.2).
* DNS Routing: Configured manual DNS pointers to ensure high-availability communication between the server and its clients.

🚧 Principle of Least Privilege (PoLP)
* Access Control: Implemented advanced NTFS and SMB share permissions.
* Data Governance: Verified that specific users (e.g., Jordy) can only access authorized departmental data, preventing unauthorized lateral movement.

### **Phase 1: Server Infrastructure Setup**
* **Domain Controller Promotion:** Successfully promoted `NY-DC-01` to a primary domain controller for the `Machine.org` forest.
* **Network Configuration:** Implemented a static IPv4 address (`10.1.10.2`) to ensure consistent DNS resolution for all domain-joined assets.
* **Evidence:**
<img width="1183" height="845" alt="ServerImage" src="https://github.com/user-attachments/assets/80b0ee28-63d6-44bd-9512-b0225a7071a2" />
* Context: Showcases the healthy status of the NY-DC-01 Domain Controller.
  
<img width="1180" height="838" alt="AdminIPV4" src="https://github.com/user-attachments/assets/b5dd3076-23d9-49bc-9d1b-80a09ddf717c" />
* Context: Proves the server is using a static IP (10.1.10.2) to ensure DNS reliability.

---

### **Phase 2: Identity Management**
* **User Provisioning:** Created and managed centralized user accounts within Active Directory.
* **Standardization:** Configured User Principal Names (UPN) to maintain organizational naming conventions.
* **Security Groups:** Assigned users to specific security groups to establish baseline access controls.
* **Evidence:**
<img width="1188" height="842" alt="ServerUsers" src="https://github.com/user-attachments/assets/20c2731d-b1cb-4d1b-b2f5-6cdaa192077a" />
* Context: Displays the full list of domain users, including the newly created Jordy and Marco L accounts.
* 
<img width="1179" height="841" alt="JORDYUSER" src="https://github.com/user-attachments/assets/05c9b26f-b618-4efa-a900-4fbe54deaa19" />
* Context: Shows the advanced account settings and the specific Jordy@Machine.org UPN.

---

### **Phase 3: Client Connectivity**
* **Client Networking:** Configured Windows 11 client DNS to point to the Domain Controller for service location.
* **Domain Integration:** Successfully joined the workstation to the domain and verified the secure channel status via PowerShell.
* **Evidence:**
<img width="953" height="799" alt="bruh" src="https://github.com/user-attachments/assets/9ca56261-4624-4ff8-9623-950f86f81129" />
* Context: Shows the Windows 11 client configured to talk to the Server's DNS.
* 
<img width="1015" height="850" alt="ProofofJOrdy" src="https://github.com/user-attachments/assets/f3270c3e-71f6-41e0-b551-20a556539ca3" />
* Context: The PowerShell confirmation that the domain connection is "True" and healthy.

---

### **Phase 4: Data Governance & Security**
* **Least Privilege:** Engineered a network share (`LAB`) utilizing the Principle of Least Privilege.
* **Permission Audit:** Restricted user access to **Modify** rights, preventing unauthorized changes to folder security or inheritance.
* **Resource Access:** Verified successful end-to-end connectivity by mapping the share as a persistent Z: drive.
* **Evidence:**
    <img width="1191" height="843" alt="PartialOwnership" src="https://github.com/user-attachments/assets/82b14b4c-adcc-49b3-b683-4050b0863ce8" />
* Context: Proves the application of Least Privilege by giving Jordy Modify access instead of Full Control.
   
    <img width="1023" height="847" alt="SharedDrive" src="https://github.com/user-attachments/assets/b07fecea-a91a-4e61-803a-cf2815c6de31" />
* Context: Shows the shared folder successfully mapped as the Z: drive on the client desktop.

    <img width="1191" height="840" alt="USersinSErber" src="https://github.com/user-attachments/assets/e99b4639-a446-4ad3-94de-487457b55b90" />
* Context: A final PowerShell audit table listing the status of all domain accounts.
