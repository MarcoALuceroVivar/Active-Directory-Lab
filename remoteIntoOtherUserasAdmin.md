#Remote into the users computer as an administrator
Step 1: Enable Remote Desktop on the Client VM
Action: Log into the Windows 11 client machine (JORDYM) and enable remote access.

How: Navigate to Settings > System > Remote Desktop and toggle it to On.

Why: By default, Windows 11 blocks RDP for security; manually enabling it establishes the workstation as "manageable" over the network.
<img width="1022" height="853" alt="image" src="https://github.com/user-attachments/assets/b437a9ac-0f32-43cb-b23e-caaa68296b11" />
the IP address of the user:
<img width="1024" height="847" alt="image" src="https://github.com/user-attachments/assets/af95f980-8cfb-41a3-954c-0cefc62e5abb" />


Step 2: Verify Network Line-of-Sight
Action: Ensure the Administrator on NY-DC-01 can "see" the client machine.

How: Open Command Prompt on the Server and ping 10.1.10.3 (the client's static IP).

Why: Without a successful ping, the RDP request will timeout, usually indicating a firewall or DNS mismatch.
ADMINISTRATOR being able to ping the user:
<img width="1189" height="839" alt="image" src="https://github.com/user-attachments/assets/7b19c6dc-d8f1-4ff6-883e-1eeb835634f9" />

Step 3: Initiate the RDP Session from the Server
Action: Launch the Remote Desktop Connection (mstsc.exe) from the Domain Controller.

How: Enter the IP 10.1.10.3 and click Connect.

Why: This simulates the "Admin-to-User" support model common in enterprise help desks.

<img width="1189" height="842" alt="image" src="https://github.com/user-attachments/assets/34c4c451-2837-4f62-834e-e6bd1be288b0" />

Type in the users IP:
<img width="1187" height="844" alt="image" src="https://github.com/user-attachments/assets/eccd5049-481f-42b0-8781-e2055ac79af6" />

Should say "Initiating connection":
<img width="420" height="140" alt="image" src="https://github.com/user-attachments/assets/71c2a066-bf66-4c07-b5e4-3a35fb44434e" />

Accept the certificate
<img width="1189" height="840" alt="image" src="https://github.com/user-attachments/assets/837cd854-0700-4fee-992e-070c6242032f" />

THe users machine will ask you to allow the connection
<img width="1024" height="846" alt="image" src="https://github.com/user-attachments/assets/959821a3-32c8-4ad5-98e3-b881d7367b47" />


