# Network-Attacks-Phishing-Malicious-Links
Network Attacks: Phishing &amp; Malicious Links


Project Guide
OBJECTIVE 1
Cloning a Website for Credential Harvesting
Jile has experienced a surge in phishing attempts targeting its employees. Attackers are sending deceptive emails and hosting malicious websites to harvest credentials, often impersonating popular services like Google or Twitter. Your task is to simulate one of these phishing campaigns using the Social Engineering Toolkit (SET) and observe how easily attackers can gather sensitive information. By the end of this lab, you will understand how phishing attacks can trick unsuspecting users, how credentials are captured, and how defenders can recognize and mitigate these threats.

Run the following command to start the Social Engineering Toolkit.
<img src="https://imgur.com/kHf595P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<img src="https://imgur.com/utTTX61.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<img src="https://imgur.com/undefined.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

Type 1 and press Enter to select Social-Engineering Attacks from the main SET menu.

Type 2 to select Website Attack Vectors and press Enter.

Type 3 to select the Credential Harvester Attack Method.

Type 1 to select Web Templates and load a pre-configured phishing site.

When prompted for the POST back in Harvester/Tabnabbing, enter the IP address or hostname:ttacker.server.

Choose a template from the menu, type 2 to select Google, to clone the corresponding login page.
<img src="https://imgur.com/UlOgIKx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

Return to the Connections page in the browser, and open the Victim Server in the new tab.
In the Microsoft Edge address bar, enter your cloned site’s URL:

http://attacker.server



Crafting and Executing a Malicious File

In the Web Attack Module, type 99 and press Enter to return to the Main Menu.

From the SET Main Menu, type 4 and press Enter to access the Create a Payload and Listener section.

<img src="https://imgur.com/ADJb9KL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<img src="https://imgur.com/ADJb9KL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

In the payload options, type 4 and press Enter to select Windows Shell Reverse_TCP X64.

When prompted, enter 172.31.24.30 as the Local Host(LHOST) for the payload listener.
Then specify 4444 as the PORT for the reverse listener.

<img src="https://imgur.com/TWnhLy8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


Once payload is generated, type yes followed by Enter to start the payload listener.
In the Metasploit console, run Python HTTP server to transfer the payload from the Social Engineering Toolkit Server to Generic Server.
<img src="https://imgur.com/ljilRrj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

On the Generic Server, download payload from the Social Engineering Toolkit Server and store it in the Samba shared directory (/home/share/) by running the following command:

<img src="https://imgur.com/rifuX9f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

Switch Back to Victim Server and open the Run dialog by searching for Run in the Start Menu.
