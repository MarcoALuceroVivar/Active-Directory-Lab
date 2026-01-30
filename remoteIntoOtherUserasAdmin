Step 1: Enable Remote Desktop on the Client VM
Action: Log into the Windows 11 client machine (JORDYM) and enable remote access.

How: Navigate to Settings > System > Remote Desktop and toggle it to On.

Why: By default, Windows 11 blocks RDP for security; manually enabling it establishes the workstation as "manageable" over the network.

Step 2: Verify Network Line-of-Sight
Action: Ensure the Administrator on NY-DC-01 can "see" the client machine.

How: Open Command Prompt on the Server and ping 10.1.10.3 (the client's static IP).

Why: Without a successful ping, the RDP request will timeout, usually indicating a firewall or DNS mismatch.

Step 3: Initiate the RDP Session from the Server
Action: Launch the Remote Desktop Connection (mstsc.exe) from the Domain Controller.

How: Enter the IP 10.1.10.3 and click Connect.

Why: This simulates the "Admin-to-User" support model common in enterprise help desks.
