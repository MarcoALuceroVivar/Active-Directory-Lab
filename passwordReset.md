## Scenario
A user is unable to log in due to an account lockout and submits a ticket through the help desk system.

---

## Step 1 – Ticket Creation
The user submits a support ticket through the osTicket portal indicating they are locked out of their account.

![Ticket Created]

---

## Step 2 – Ticket Review
The administrator reviews the ticket in the osTicket staff control panel to confirm the issue.

![Ticket Review]

---

## Step 3 – Verify Locked Account
The administrator checks for locked accounts using PowerShell:

```powershell
Search-ADAccount -LockedOut | Select Name, SamAccountName
