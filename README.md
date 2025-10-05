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
<br />
<br />
To confirm that both the user (helpdesk) and the VM (Desktop1) were added to the homelab domain, I logged into the server account and checked Active Directory Users and Computers. In this section, we can see I was successful in adding the VM to the domain, and the helpdesk as a user.<br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/ffbcd4f2-f1bd-43d9-a5e7-edcc059cb59b_rw_1200.png?h=ea3e32a3b4e523aed32fc247df1e6cbe" height="80%" width="80%" alt="Active Directory Home Lab">
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/11e65528-983a-4d90-a8a1-e93366ebe0b4_rw_1200.png?h=f265544b7a81d7e38fad048ec2411f68" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Currently, I have a homelab.com domain where the user helpdesk with administrator rights under the domain. Next, I will create two organizational units called IT and HR, where my two new users will be located. These new users will act as regular users without administrative rights and controls.<br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/e4b8df82-3985-4f27-90fa-2bc5afc4b26a_rw_1200.png?h=981a7291d900c78de7bad089f8e4ee12" height="80%" width="80%" alt="Active Directory Home Lab">
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/1617c7f0-c2ca-470e-bdbf-78aa2dae0bce_rw_1200.png?h=ad447e01eb3a5a11e9e5bad18888e8b1" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
These two new users come with default configurations. In this next step, I will be using Group Policy Management tool to edit and save the new configurations made to these accounts. To start, I will be changing the password policies for these accounts. Password policies are one of the most important due to limiting the number of attempts a person can have and the period of time an account can be locked out in case the person is an authorized user. 
<br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/a68435b7-1074-42e2-89cf-fccca70fc217_rw_1200.png?h=9d47f84b2f53cd0f81f79e4ae284a9e7" height="80%" width="80%" alt="Active Directory Home Lab">
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/507891c8-0886-462a-92bc-dd0e65acd441_rw_1200.png?h=f66f5ee6f018b090cb8e999444dc5718" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Now that all the user accounts have given policies to their respective role in the company, the computers they are accessing their accounts from will also have to be connected to the homelab.com domain. In order to do this, I created another VM called desktop2 on which either user can sign in on this machine and access their account. In the image below, you can find the desktop2 being successfully connected to the homelab.com domain. 
<br/>
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/f13ce00e-13e4-42c4-aeed-f7df77b63660_rw_1200.png?h=f112d59427833df050647370a2ca6dc6" height="80%" width="80%" alt="Active Directory Home Lab">
<img src="https://cdn.myportfolio.com/8dbb6c1b-feee-4c96-8037-bd867d15097e/c207feb4-2712-45e4-ad3d-f98af872f67c_rw_1200.png?h=df368946c650e68c7142f54ca6cf5a30" height="80%" width="80%" alt="Active Directory Home Lab"/>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
