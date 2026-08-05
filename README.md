<h1>Home Lab – Active Directory Computer and Group Policy Management</h1>

<h3>Project Overview</h3>
This home lab demonstrates how Active Directory Organizational Units (OUs) and Group Policy Objects (GPOs) are used to organize computer objects, standardize security settings, and enforce administrative policies across a Windows domain. The lab simulates common enterprise tasks performed by IT Support and Systems Administrators to improve security, simplify management, and ensure consistent workstation configurations. 
<br />

<h3>Objectives </h3>

- Organize computer objects using Organizational Units (OUs)
- Deploy and manage Group Policy Objects (GPOs)
- Configure domain password policies
- Restrict access to Windows Control Panel
- Enforce automatic workstation locking
- Demonstrate centralized Windows administration

<h3>Environment </h3>

- Windows Server 2019
- Active Directory Domain Services (AD DS)
- Group Policy Management Console (GPMC)
- Windows 10 Client

<h3>Skills Demonstrated </h3>

- Active Directory Administration
- Organizational Unit (OU) Management
- Group Policy Administration
- Password Policy Configuration
- Account Lockout Policy
- Endpoint Security
- Windows Security Hardening
- Centralized Policy Management
- Windows Server Administration
</p>  
<br />

<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCGDiagram.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br /> 


<h2>Scenario 1 – Organizing Computer Objects</h2>


<h3>Issue </h3>
To improve administration and policy deployment, company workstations and servers must be organized into separate Organizational Units.
</p>  
<br />

<h3>Actions Performed </h3>

- Created dedicated Workstations and Servers Organizational Units
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG1.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Moved computer objects from the default Computers container
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG2.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br /> 

<h2>Scenario 2 – Reviewing and Configuring Domain Password Policies</h2>


<h3>Issue </h3>
The organization requires stronger password requirements to improve domain security.
</p>  
<br />

<h3>Actions Performed </h3>

- Reviewed the existing Default Domain Policy
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG3.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Examined current password and account lockout settings
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG4.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Edit in Default Domain Policy
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG5.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Navigated to: Computer Configuration → Policies → Windows Settings → Security Settings → Account Policies → Password Policy
- Updated the Minimum Password Length policy to 10 characters
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG6.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h2>Scenario 3 – Restricting Access to Control Panel</h2>

<h3>Issue </h3>
Standard users should not be able to modify system settings through Control Panel, while IT administrators retain full access
</p>  
<br />

<h3>Actions Performed </h3>

- Created a new Group Policy Object named Restrict Control Panel Access
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG7.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Configured the policy under: User Configuration → Administrative Templates → Control Panel
- Enabled the policy to prevent access to Control Panel
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG8.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Linked the GPO to the appropriate Organizational Units
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG9.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

<h2>Scenario 4 – Configuring Automatic Workstation Lock</h2>
To improve endpoint security, workstations should automatically lock after a period of inactivity. First, I create a new Group Policy Object named Auto Lock Screen.

<h3>Issue </h3>
To improve endpoint security, company workstations should automatically lock after a period of inactivity.
</p>  
<br />

<h3>Actions Performed </h3>

- Created a new Group Policy Object named Auto Lock Screen
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG10.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br /> 

- Configured the Machine Inactivity Limit policy under: Computer Configuration → Policies → Windows Settings → Security Settings → Local Policies → Security Options
- Set the inactivity timeout to 300 seconds (5 minutes)
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG11.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- Linked the policy at the domain level
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG12.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />


- <b>Summary</b> <br />
This lab demonstrates core Windows Server administration skills through the organization of Active Directory objects and the deployment of Group Policy Objects. Tasks included creating Organizational Units, managing computer objects, configuring domain password policies, restricting user access through Group Policy, and enforcing automatic workstation lock policies. These exercises reflect common responsibilities performed by IT Support and Systems Administrators in enterprise Windows environments.
<br />
<br />
