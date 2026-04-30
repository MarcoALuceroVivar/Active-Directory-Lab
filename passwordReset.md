## Scenario
A user is unable to log in due to an account lockout and submits a ticket through the help desk system.

---

## Step 1 – Ticket Creation
The user submits a support ticket through the osTicket portal indicating they are locked out of their account.
<img width="1228" height="530" alt="image" src="https://github.com/user-attachments/assets/a44f5873-3e15-4aeb-96f0-385373d56981" />


---

## Step 2 – Ticket Review
The IT user reviews the ticket in the osTicket staff control panel to confirm the issue.
<img width="1054" height="516" alt="image" src="https://github.com/user-attachments/assets/9cf4e2c7-ee88-4e1c-aaa2-5a26d762f84d" />



---

## Step 3 – Verify Locked Account
The IT user checks for locked accounts using PowerShell:

```powershell
Search-ADAccount -LockedOut | Select Name, SamAccountName
```
<img width="978" height="264" alt="image" src="https://github.com/user-attachments/assets/4a4bf7b1-dfd7-4012-b5da-035e87bc8e10" />

## Step 4- Reset User Password and Unlock Account
user logs in with the password provided

```powershell
Set-ADAccountPassword -Identity Jordy -Reset `
-NewPassword (ConvertTo-SecureString "NewPass123!" -AsPlainText -Force)

Set-ADUser -Identity Jordy -ChangePasswordAtLogon $true

Unlock-ADAccount -Identity Jordy
```

<img width="979" height="582" alt="image" src="https://github.com/user-attachments/assets/8e73bac5-783a-42ff-a3e4-26626690c092" />
---

## Step 5-User Log-in & Password Change
the user logs in successfully, changes their password and is able to keep on with their day.

<img width="1021" height="848" alt="image" src="https://github.com/user-attachments/assets/227cdcc0-c476-48d2-93d3-bcfa7e7f860e" />

the Password must be changed before they are able to get access to the computer once again
<img width="1024" height="854" alt="image" src="https://github.com/user-attachments/assets/8f8d3fc5-f385-4bdb-809a-5fc729a590a1" />

the user makes a change to the password supplied by IT
<img width="1027" height="849" alt="image" src="https://github.com/user-attachments/assets/097160c3-f953-4bae-bc95-9156120e8fd7" />

Then the user gets confirmation that their password has indeed been changed
<img width="1023" height="853" alt="image" src="https://github.com/user-attachments/assets/bacbdef3-1396-4f59-b235-2d51ef53ce0f" />


---
## Step 6- Close Ticket
The IT user closes the ticket and document how to resolve the issue. 

<img width="1060" height="520" alt="image" src="https://github.com/user-attachments/assets/a8a9d5fc-9c5a-476e-95b9-aee5a41eb200" />



