# Active-Directory-Lab
### **Phase 1: Server Infrastructure Setup**
* **Domain Controller Promotion:** Successfully promoted `NY-DC-01` to a primary domain controller for the `Machine.org` forest.
* **Network Configuration:** Implemented a static IPv4 address (`10.1.10.2`) to ensure consistent DNS resolution for all domain-joined assets.
* **Evidence:**
    ![Server Dashboard](images/ServerImage.png)
    ![Server IP Settings](images/AdminIPV4.png)

---

### **Phase 2: Identity Management**
* **User Provisioning:** Created and managed centralized user accounts within Active Directory.
* **Standardization:** Configured User Principal Names (UPN) to maintain organizational naming conventions.
* **Security Groups:** Assigned users to specific security groups to establish baseline access controls.
* **Evidence:**
    ![Directory User List](images/ServerUsers.png)
    ![User Properties](images/JORDYUSER.png)
    ![Security Group Membership](images/{2C55D2CD-AB76-4876-8066-D1D361D7C62C}.png)

---

### **Phase 3: Client Connectivity**
* **Client Networking:** Configured Windows 11 client DNS to point to the Domain Controller for service location.
* **Domain Integration:** Successfully joined the workstation to the domain and verified the secure channel status via PowerShell.
* **Evidence:**
    ![Client Network Settings](images/IPV4ConnectionofJOrdy.jpg)
    ![Secure Channel Verification](images/ProofofJOrdy.png)

---

### **Phase 4: Data Governance & Security**
* **Least Privilege:** Engineered a network share (`LAB`) utilizing the Principle of Least Privilege.
* **Permission Audit:** Restricted user access to **Modify** rights, preventing unauthorized changes to folder security or inheritance.
* **Resource Access:** Verified successful end-to-end connectivity by mapping the share as a persistent Z: drive.
* **Evidence:**
    ![Access Control List](images/PartialOwnership.png)
    ![Mapped Network Drive](images/SharedDrive.png)
    ![Final Directory Audit](images/USersinSErber.png)
