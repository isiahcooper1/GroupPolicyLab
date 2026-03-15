<h1>Active Directory Home Lab</h1>

<h2>Description</h2>
Deployed a simulated enterprise Active Directory environment using Microsoft Hyper-V to practice core identity and access management skills. The lab includes a Windows Server 2022 domain controller, a Windows 11 domain-joined workstation, a structured Organizational Unit hierarchy, domain users and security groups, and three enforced Group Policy Objects modeled after real-world security baselines. This environment mirrors what an administrator would manage in a small-to-mid size on-premises or hybrid organization.
<br>
<br>


<h2>Utilities Used</h2>

- <b>Active Directory Domain Services (AD DS)</b> 
- <b>Group Policy Management Console (GPMC)</b>
- <b>Active Directory Users and Computers (ADUC)</b>
- <b>Windows PowerShell (gpresult verification)</b>

<h2>Environments Used </h2>

- <b>Windows Server 2022 Evaluation (Domain Controller — DC01)</b>
- <b>Windows 11 (Domain Workstation — WS01)</b>
- <b>Internal Hyper-V Virtual Switch (AD-Lab-Internal, isolated network)</b>

<h2>Lab Architecture</h2>

<h2>Program walk-through:</h2>

<p align="center">
1. DC01 and WS01 are running on an isolated internal Hyper-V switch (AD-Lab-Internal), simulating a segmented enterprise network with no external exposure. <br/>
<img src="https://github.com/user-attachments/assets/948663bb-ab0b-4664-9eb1-2a5e62de0fb1" height="80%" width="80%" alt="Organizational Units"/>
<br />
<br />
2. Organizational Units are structured by department (IT, HR, Finance) with sub-OUs under IT for Admins and Helpdesk, reflecting a real delegation model. <br/>
<img src="https://github.com/user-attachments/assets/3094e2e9-7b37-4e75-8853-c0376093e492" height="80%" width="80%" alt="Domain Users"/>
<br />
<br />
3. Five domain user accounts provisioned across departments using a firstname.lastname naming convention and placed in their corresponding OUs for policy scoping. <br/>
<img src="https://github.com/user-attachments/assets/3e057cd1-ac62-4bda-8081-cf8c20815b11" height="80%" width="80%" alt="OU Structure with Sydney IT Group"/>
<br />
<br />
4. Three GPOs linked at different levels: Password-Policy at the domain root, Workstation-Lockscreen scoped to the Workstations OU, and HR-Restrict-ControlPanel scoped to the HR OU.<br/>
<img src="https://github.com/user-attachments/assets/e1ea985f-4254-4711-a6e3-1a205f462192" height="80%" width="80%" alt="Shared Drive"/>
<br />
<br />
5. Domain-wide password policy enforcing a 12-character minimum length, complexity requirements, and a 90-day maximum password age.  <br/>
<img src="https://github.com/user-attachments/assets/af3a0103-a3d2-449d-b43d-a3247a1b1234" height="80%" width="80%" alt="Password Policy GPO Linked to Domain"/>
<br />
<br />
<img src="https://github.com/user-attachments/assets/3a332561-eb52-4637-9f45-8dd5cdfbc9b3" height="80%" width="80%" alt="Password Policy GPO"/>
<br />
<br />
6. User configuration policy prohibiting access to Control Panel and PC Settings, scoped exclusively to the HR OU to limit user-side system changes.  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
7. System Properties on WS01 confirming successful domain join to corp.local, with DC01 serving as the authenticating domain controller.  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
8. Command-line verification showing all three GPOs applied to the workstation, confirming correct linking, scope, and inheritance.  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
9. HR domain user account receiving an access restriction when attempting to open Control Panel, confirming the GPO is applying correctly at the user level.  <br/>
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
