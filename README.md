# Active-Directory-Lab
### **Phase 1: Server Infrastructure Setup**
* **Domain Controller Promotion:** Successfully promoted `NY-DC-01` to a primary domain controller for the `Machine.org` forest.
* **Network Configuration:** Implemented a static IPv4 address (`10.1.10.2`) to ensure consistent DNS resolution for all domain-joined assets.
* **Evidence:**
<img width="1183" height="845" alt="ServerImage" src="https://github.com/user-attachments/assets/80b0ee28-63d6-44bd-9512-b0225a7071a2" />
<img width="1180" height="838" alt="AdminIPV4" src="https://github.com/user-attachments/assets/b5dd3076-23d9-49bc-9d1b-80a09ddf717c" />

---

### **Phase 2: Identity Management**
* **User Provisioning:** Created and managed centralized user accounts within Active Directory.
* **Standardization:** Configured User Principal Names (UPN) to maintain organizational naming conventions.
* **Security Groups:** Assigned users to specific security groups to establish baseline access controls.
* **Evidence:**
<img width="1188" height="842" alt="ServerUsers" src="https://github.com/user-attachments/assets/20c2731d-b1cb-4d1b-b2f5-6cdaa192077a" />

<img width="1179" height="841" alt="JORDYUSER" src="https://github.com/user-attachments/assets/05c9b26f-b618-4efa-a900-4fbe54deaa19" />

    ![Security Group Membership](images/{2C55D2CD-AB76-4876-8066-D1D361D7C62C}.png)

---

### **Phase 3: Client Connectivity**
* **Client Networking:** Configured Windows 11 client DNS to point to the Domain Controller for service location.
* **Domain Integration:** Successfully joined the workstation to the domain and verified the secure channel status via PowerShell.
* **Evidence:**
![IPV4ConnectionofJOrdy](https://github.com/user-attachments/assets/72e60907-5a58-4c87-a5d8-67fb597c54ed)


<img width="1015" height="850" alt="ProofofJOrdy" src="https://github.com/user-attachments/assets/f3270c3e-71f6-41e0-b551-20a556539ca3" />


---

### **Phase 4: Data Governance & Security**
* **Least Privilege:** Engineered a network share (`LAB`) utilizing the Principle of Least Privilege.
* **Permission Audit:** Restricted user access to **Modify** rights, preventing unauthorized changes to folder security or inheritance.
* **Resource Access:** Verified successful end-to-end connectivity by mapping the share as a persistent Z: drive.
* **Evidence:**
    <img width="1191" height="843" alt="PartialOwnership" src="https://github.com/user-attachments/assets/82b14b4c-adcc-49b3-b683-4050b0863ce8" />

    <img width="1023" height="847" alt="SharedDrive" src="https://github.com/user-attachments/assets/b07fecea-a91a-4e61-803a-cf2815c6de31" />

    <img width="1191" height="840" alt="USersinSErber" src="https://github.com/user-attachments/assets/e99b4639-a446-4ad3-94de-487457b55b90" />

