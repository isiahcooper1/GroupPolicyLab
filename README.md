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
<img src="https://github.com/user-attachments/assets/9de55fe6-ae18-451e-ab05-fefb26d657ec" height="80%" width="80%" alt="Network"/>
<br />
<br />
2. Organizational Units are structured by department (IT, HR, Finance) with sub-OUs under IT for Admins and Helpdesk, reflecting a real delegation model. <br/>
<img src="https://github.com/user-attachments/assets/3094e2e9-7b37-4e75-8853-c0376093e492" height="80%" width="80%" alt="Domain Users"/>
<br />
<br />
3. Domain user accounts were created using a PowerShell script that imports user data from a CSV file, automatically provisioning each account into the correct Organizational Unit and security group without manual intervention. <br/>
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
<img src="https://github.com/user-attachments/assets/9133ff4c-c3b8-4739-9e23-df4f74397355" height="80%" width="80%" alt="Control Panel Policy"/>
<br />
<br />
7. System Properties on WS01 confirming successful domain join to corp.local, with DC01 serving as the authenticating domain controller.  <br/>
<img src="https://github.com/user-attachments/assets/9bf162b3-8717-49d8-9201-b781d4738820" height="80%" width="80%" alt="Domain-Joined PC"/>
<br />
<br />
8. Command-line verification showing all three GPOs applied to the workstation, confirming correct linking, scope, and inheritance.  <br/>
<img src="https://github.com/user-attachments/assets/e3137365-5eb8-4d4d-ab46-37d35e233d61" height="80%" width="80%" alt="CLI verification"/>
<br />
<br />
9. HR domain user account receiving an access restriction when attempting to open Control Panel, confirming the GPO is applying correctly at the user level.  <br/>
<img src="https://github.com/user-attachments/assets/f45d879c-2fc2-4a88-990d-3df2dd1a0f83" height="80%" width="80%" alt="Restricted Access"/>
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
