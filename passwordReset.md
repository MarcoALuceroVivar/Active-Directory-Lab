## Scenario
A user is unable to log in due to an account lockout and submits a ticket through the help desk system.

---

## Step 1 – Ticket Creation
The user submits a support ticket through the osTicket portal indicating they are locked out of their account.
<img width="1228" height="530" alt="image" src="https://github.com/user-attachments/assets/a44f5873-3e15-4aeb-96f0-385373d56981" />


---

## Step 2 – Ticket Review
The administrator reviews the ticket in the osTicket staff control panel to confirm the issue.
<img width="1054" height="516" alt="image" src="https://github.com/user-attachments/assets/9cf4e2c7-ee88-4e1c-aaa2-5a26d762f84d" />



---

## Step 3 – Verify Locked Account
The administrator checks for locked accounts using PowerShell:

```powershell
Search-ADAccount -LockedOut | Select Name, SamAccountName
```
<img width="978" height="264" alt="image" src="https://github.com/user-attachments/assets/4a4bf7b1-dfd7-4012-b5da-035e87bc8e10" />

