# User Provisioning Automation (CSV → Active Directory)

## Overview
This project demonstrates automated user provisioning in Active Directory using a CSV file and PowerShell.

User accounts are created, organized into Organizational Units (OUs), and assigned to security groups based on their roles.

---

## Tools Used
- Windows Server 2022
- Active Directory Domain Services
- PowerShell
- CSV Data Source

---

## Objective
- Import user data from a CSV file
- Automatically create Active Directory users
- Create Organizational Units (OUs)
- Assign users to security groups
- Organize users based on roles

---

## CSV Structure

```csv
Name,Username,GroupName,Position
Aaron Judge,AJudge,Players,Outfielder
Paul Goldschmidt,PGoldschmidt,Players,First Baseman
