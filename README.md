<h1>Active Directory Administration & Group Policy Management</h1>

<h2>Description</h2>
This project builds on the infrastructure created in Project 1: Virtual Home Lab.
<br>
<br>
The objective of this lab was to simulate common Active Directory administrative tasks performed in enterprise environments. Tasks included creating Organizational Units (OUs), managing domain user accounts, implementing role-based access control using security groups, and enforcing centralized security policies using Group Policy.
<br>
<br>
This lab demonstrates practical system administration skills including identity management, centralized configuration management, and automation using PowerShell.
<br>
<br>


<h2>Utilities Used</h2>

- <b>Active Directory Domain Services (AD DS)</b> 
- <b>Group Policy Management Console (GPMC)</b>
- <b>Windows Server 2022</b>
- <b>PowerShell</b>

<h2>Environments Used </h2>

- <b>Windows Server 2022 Domain Controller (DC01)</b>
- <b>Windows 11 Domain-Joined Client</b>
- <b>corp.lab Active Directory Domain</b>

<h2>Lab Architecture</h2>

<h2>Program walk-through:</h2>

<p align="center">
1. Created Organizational Units (OUs) within the corp.lab domain to organize users and computers by department. <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
2. Created multiple domain user accounts to simulate employees across different departments.  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
3. Implemented Role-Based Access Control (RBAC) using Active Directory security groups. <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
4. Created and configured Group Policy Objects (GPOs) using Group Policy Management Console.  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
5. Configured workstation restrictions using Group Policy linked to the Workstations Organizational Unit.  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
6. Implemented PowerShell automation to streamline user account creation.  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. Verified Group Policy application on the domain client machine.  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. Verified Group Policy application on the domain client machine.  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
