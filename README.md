<h1>Active Directory: Domain Services, Remote Access, and DHCP Server Roles Configuration</h1>


<h2>Description</h2>
This project involves creating an internal network with virtual machines. DHCP, NAT, and AD Domain services will be set up to provide users with IP addresses, allowing internet access through the Domain Controller rather than an external connection. A PowerShell script will be used to create a bulk of random user accounts. Successful connectivity will be confirmed by logging into a user account with provided login username and password. This will be a good demonstration of networking and Windows Command Line commands. 

<br/>


<h2>Environments and Technologies Used</h2>

- <b>Windows Command Terminal</b>
- <b>PowerShell</b>
- <b>Remote Desktop</b>
- <b>Network Configuration</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Server 2019</b>

<h2>Configuration Steps:</h2>

__1. User Generation with Powershell Script__ <br/>
<br/>
a. In the Domain Controller virtual machine, open PowerShell ISE and run the [script](https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1) to generate a mass of user accounts. This will simulate the number of users in a enterprise environment: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_users/blob/fcb97f27b5d67bdf8609bf550ba8bbd1529a2587/images/ug_1.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
b.Confirm the new users are present in orgainizational unit we made earlier:<br/>
<img src="https://github.com/henrykim-projects/activedirectory_users/blob/21f23db221ff455ae30f7733b5d632f9c2801afc/images/ug_3.PNG" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<br />  
<br />

__2. Confirm Network Connectivity in Client Computer__ <br/>
<br/>
a. Configure a second virtual machine that will act as the client computer and log in using one of the generated user accounts: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_users/blob/21f23db221ff455ae30f7733b5d632f9c2801afc/images/ug_4.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
b. As we open Windows Command terminal and run ipconfig, we can see that the information matches our manual configuration: The DNS is coming from mydomain.com, as well as the default gateway. The IP address of the user's computer is 172.16.0.100, the very first of the scope we set earlier: <br/>
<img src="https://github.com/henrykim-projects/activedirectory_users/blob/21f23db221ff455ae30f7733b5d632f9c2801afc/images/ug_2.PNG" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br/> 
<br/>
</p>

<h2>Final Thoughts</h2>
In this portion, we created user accounts, logged in with one of them, and confirmed that our internal network is up and running. This project was a comprehensive review of Active Directory as well as essential concepts in the A+ exam. 
<br><br/>
