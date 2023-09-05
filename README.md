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
</p>
<p>

Now, let's complete a cache exercise, go back to DC-1 and change the mainframe's record address to 8.8.8.8, then go back to Client-1 and ping "mainframe" again, do observe that it will ping the old address. Now go and observe the local dns cache by entering the command ipconfig /displaydns, then flush the dns cache by entering the command ipconfig /flushdns, you'll observe that the cache is empty. Now ping the "mainframe" again, observe that it will ping the new address.

<img src="https://i.imgur.com/lEoYcJO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/GTGh0Q0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2jflzJI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/n1Kr7y1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yMHXGo6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
</p>
<p>

Now, let's create a CNAME record, in DC-1, this will point the host "search" to www.google.com. Now go back to Client-1 and attempt to ping "search" and observe the results of the CNAME record, then use the command nslookup, and nslookup "search", and observe the results of the CNAME record.

<img src="https://i.imgur.com/bClzoWM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/l7UVzlV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
