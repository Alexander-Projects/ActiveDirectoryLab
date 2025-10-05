<h1>🖥️ Active Directory Home Lab</h1>

<h2>Description</h2>
The Active Directory Home lab consists of installing Windows Server 2016 and Windows 10 operating systems on a virtual machine through VirtualBox to explore Active Directory and its functionalities. Along with installing these from scratch, I will create users to simulate a company environment and the day-to-day tasks an IT person may encounter. <br />


<h2>Utilities Used</h2>

- <b>Windows 2016 Server</b> 
- <b>Windows 10 Operating System </b>
- <b>VirtualBox</b>

<h2>Enviroments Used</h2>

- <b>Windows 2016 Server</b>
- <b>Windows 10 Operating System </b>

<h2>Active Directory Home Lab project walk through walk-through:</h2>

<p align="center">
After installation of Windows 2019 server on a VM, I am installing Active Directory tools through Server Manager: <br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/3082dfbb-0c43-45d6-8926-f94a8abb8926_rw_1200.png?h=f89680be953620830bbf8d1680ff8b5c" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
After installing Active Directory, I am able to create a new user. This new user is called helpdesk and will have the same abilities as an administrator would have. To create this user, I am going to copy the administrator user and rename that user to helpdesk. To confirm the copy was done correctly, I will do a side-by-side comparison of the administrator and helpdesk properties <br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/9d3762f0-9993-401b-bb55-f088bc7abd6c_rw_1200.png?h=8504fff984bd4d059118629492ded5ca" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Upon creating the new user helpdesk account in the homelab.local domain, I created another VM that has the Windows 10 operating system. In order for the helpdesk user account to have Active Directory without logging into the administrator command, I am going to install the RSAT tools into the helpdesk account. RSAT tools will allow the same functionalities as Active Directory in the administrator account.<br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/ea129a04-e37f-4c59-8731-ef78e92b001f_rw_1200.png?h=4c0138c5a29ee0fd40c4c78f37978356" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Meanwhile, the RSAT tools are being installed, I went ahead and changed the computer name to a more recognizable name. To connect with the Windows 2016 server, I have to configure the TCP/IPv4 properties manually. AS a result, I assigned the virtual machine an IP address. After assigning the VM an IP address, I configured it to use the DNS server address of the Windows 2016 server. This will allow the VM to have communication with the server and vice versa .<br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/097c5453-9c15-4f03-85f5-aaaf927e6099_rw_1200.png?h=dd14fe5d10887559b3dad8e09abceb08" height="80%" width="80%" alt="Active Directory Home Lab">
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/65482e9c-1d81-43ed-8067-df59cd704923_rw_1200.png?h=b8212dd4a2bf1d9b774e73c8fdf9b703" height="80%" width="80%" alt="Active Directory Home Lab"/>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
