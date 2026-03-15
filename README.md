<h1>Active Directory Home Lab</h1>

<h2>Description</h2>
Deployed a simulated enterprise Active Directory environment using Microsoft Hyper-V to practice core identity and access management skills. The lab includes a Windows Server 2022 domain controller, a Windows 11 domain-joined workstation, a structured Organizational Unit hierarchy, domain users and security groups, and three enforced Group Policy Objects modeled after real-world security baselines. This environment mirrors what an administrator would manage in a small-to-mid size on-premises or hybrid organization.
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
<img src="https://github.com/user-attachments/assets/948663bb-ab0b-4664-9eb1-2a5e62de0fb1" height="80%" width="80%" alt="Organizational Units"/>
<br />
<br />
2. Created multiple domain user accounts to simulate employees across different departments.  <br/>
<img src="https://github.com/user-attachments/assets/3094e2e9-7b37-4e75-8853-c0376093e492" height="80%" width="80%" alt="Domain Users"/>
<br />
<br />
3. Implemented Role-Based Access Control (RBAC) using Active Directory security groups. <br/>
<img src="https://github.com/user-attachments/assets/3e057cd1-ac62-4bda-8081-cf8c20815b11" height="80%" width="80%" alt="OU Structure with Sydney IT Group"/>
<br />
<br />
4. Created an IT department shared directory on DC01 and configured NTFS permissions using the Sydney_IT_Admins security group. Verified access by mapping the network drive from the IT user's profile on the domain-joined client.<br/>
<img src="https://github.com/user-attachments/assets/e1ea985f-4254-4711-a6e3-1a205f462192" height="80%" width="80%" alt="Shared Drive"/>
<br />
<br />
5. Created and configured Group Policy Objects (GPOs) using Group Policy Management Console.  <br/>
<img src="https://github.com/user-attachments/assets/af3a0103-a3d2-449d-b43d-a3247a1b1234" height="80%" width="80%" alt="Password Policy GPO Linked to Domain"/>
<br />
<br />
<img src="https://github.com/user-attachments/assets/3a332561-eb52-4637-9f45-8dd5cdfbc9b3" height="80%" width="80%" alt="Password Policy GPO"/>
<br />
<br />
6. Configured workstation restrictions using Group Policy linked to the Workstations Organizational Unit.  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. Implemented PowerShell automation to streamline user account creation.  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
8. Verified Group Policy application on the domain client machine.  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
9. Verified Group Policy application on the domain client machine.  <br/>
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
