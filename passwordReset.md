# Active Directory Password Reset Guide
## Step-by-Step Instructions

### 1. Open Administrative Tools
From the **Server Manager** dashboard, navigate to the top-right corner and click **Tools**. Select **Active Directory Users and Computers** from the drop-down menu.

<img width="512" height="169" alt="image" src="https://github.com/user-attachments/assets/a80d2d90-d45a-4f9f-8277-d7f37c659a92" />

### 2. Locate the User Account
In the ADUC interface, expand the **Machine.org** domain tree in the left pane. Select the **Users** container to view all active directory objects.

<img width="512" height="328" alt="image" src="https://github.com/user-attachments/assets/7d587611-28e5-4d2e-86e1-3bc78a9f382d" />

### 3. Initiate the Reset
Right-click on the target user (e.g., **Jordy**) and select **Reset Password...** from the context menu.

<img width="512" height="328" alt="image" src="https://github.com/user-attachments/assets/d32ba5f7-1dc4-457a-a7b6-1b4fd68a12c4" />



### 4. Configure New Credentials
In the **Reset Password** dialog box:
* **New password**: Enter the temporary password.
* **Confirm password**: Re-enter the password for verification.
* **User must change password at next logon**: Ensure this is **checked** to maintain security best practices.
* **Unlock the user's account**: Check this if the user was previously locked out.
<img width="512" height="255" alt="image" src="https://github.com/user-attachments/assets/aeceba6b-6935-41ce-bdf0-32f9efd28f4b" />


### 5. Confirm Completion
Click **OK**. A confirmation message will appear stating, "The password for Jordy has been changed". Click **OK** to close the wizard.
<img width="512" height="225" alt="image" src="https://github.com/user-attachments/assets/a57f4b9e-4362-4097-8cbd-faca071c2a27" />

