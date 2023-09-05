<p align="center">
<img src="https://i.imgur.com/4Xx73lO.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1> Intuition for DNS (Azure)</h1>
In this tutorial, we will use Client-1 and DC-1 to learn how DNS works.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- DNS

<h2>Operating Systems Used </h2>

- Windows Server 2022 (Domain Controller)
- Windows 10 (21H2)


<h2> Steps </h2>

<p>
</p>
<p>

First, we will need to log into our domain controller (DC-1), using our jane_admin account (mydomain.com\jane_admin). After this, log in to Client-1 as an admin, using the same admin account, then from Client-1 try and ping mainframe, you will notice that it will fail. We will then need to type in the command "nslookup mainframe" to notice that this fails, meaning that there will be no DNS record. In that case, create a DNS-A record on DC-1, then go back and ping "mainframe" again. You will observe that the address of the new record will show up.

<img src="https://i.imgur.com/J7OvldM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/6yqFuxU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MOIwBMA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/390GDCs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/36XTxL9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
