# Day4_intership_elevate_labs
 Basic firewall management skills and understanding of network traffic filtering

🪟 On Windows (Firewall GUI):
🔹 I opened the Windows Defender Firewall via Control Panel > System and Security.

🔹 Clicked on Advanced Settings to access the firewall rule manager.

🔹 Viewed current rules under Inbound Rules.

🔹 Created a new inbound rule to block TCP port 23 (Telnet).

🔹 Selected "Block the connection" and applied it to all profiles (Domain, Private, Public).

🔹 Named the rule as "Block Telnet" and saved it.

🔹 Installed the Telnet client using the command:

cmd
Copy
Edit
dism /online /Enable-Feature /FeatureName:TelnetClient
🔹 Tested the rule using:

cmd
Copy
Edit
telnet localhost 23
The connection was blocked as expected.

🔹 Later, I deleted the block rule to restore the original state.

🐧 On Linux (UFW - Terminal):
🔹 Opened terminal and ensured UFW is installed and active.

🔹 Listed current firewall rules using:

bash
Copy
Edit
sudo ufw status numbered
🔹 Added a rule to deny incoming traffic on port 23:

bash
Copy
Edit
sudo ufw deny 23
🔹 Used telnet to test the block on port 23:

bash
Copy
Edit
telnet localhost 23
Got "connection refused", confirming the block was working.

🔹 Allowed SSH connection on port 22 using:

bash
Copy
Edit
sudo ufw allow 22
🔹 Removed the deny rule for port 23:

bash
Copy
Edit
sudo ufw delete deny 23
🧾 Summary of What I Learned:
🔸 Firewall filters traffic based on defined rules for ports, protocols, and directions (inbound/outbound).

🔸 Blocking a port prevents unwanted access, while allowing essential ports (like SSH) maintains secure connectivity.

🔸 Both Windows Firewall and UFW provide effective ways to manage network security.
