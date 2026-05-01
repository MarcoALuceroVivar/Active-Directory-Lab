# Active-Directory-Lab
 Enterprise Identity & Data Governance Lab

 Executive Summary
In a modern business environment, decentralized systems pose significant risks. Without centralized control, every computer acts as a "management island," creating massive security vulnerabilities, inefficient data silos, and an unmanageable overhead for IT departments.

This project simulates the implementation of a Centralized Identity Management System using Microsoft Active Directory. By architecting a Primary Domain Controller, I established a "Single Source of Truth" for the network. This infrastructure enables a single administrator to manage thousands of identities and assets from a unified interface, enforcing rigorous security policies and granular data access across the entire organization.
## Tools Used
- Windows Server 2022 (Domain Controller)
- Active Directory Domain Services
- PowerShell
- Windows 11 Client
- osTicket (Help Desk System)
- Oracle VirtualBox
Key Technical Pillars:

 Centralized Authentication
* Domain Integration: Transitioned from insecure local accounts to a unified Machine.org domain.
* Scalability: Enabled seamless "roaming" profiles and centralized security auditing for all network logins.

 Network Service Engineering
* Static Infrastructure: Engineered a reliable backbone using static IPv4 addressing (10.1.10.2).
* DNS Routing: Configured manual DNS pointers to ensure high-availability communication between the server and its clients.

 Principle of Least Privilege (PoLP)
* Access Control: Implemented advanced NTFS and SMB share permissions.
* Data Governance: Verified that specific users (e.g., Jordy) can only access authorized departmental data, preventing unauthorized lateral movement.
