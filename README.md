<h1>Home Lab – Active Directory Computer and Group Policy Management</h1>

<h2>Description</h2>
This home lab demonstrates how to organize computer objects and manage Group Policy Objects (GPOs) within an Active Directory environment. The lab simulates common Windows Server administration tasks, including organizing Organizational Units (OUs), configuring domain security policies, restricting user access, and enforcing workstation security settings. 
<br />

<h2>Environments Used </h2>

- <b>Windows 10</b>

<h2>Program walk-through:</h2>


- <b>Organizing Computers with Organizational Units (OUs)</b> <br />
To improve administration and policy management, company devices are organized into separate Organizational Units. First, I create dedicated Workstations and Servers Organizational Units.
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br /> 

Move computer objects from the default Computers container into the appropriate OUs. Organize devices to allow targeted Group Policy deployment. <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG1.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- <b>Managing Group Policy Objects (GPOs)</b> <br />
After organizing the Active Directory environment, I reviewed existing Group Policy Objects and their scope. First, I review the Default Domain Policy.
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG2.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br /> 

Identify policies applied to the domain. <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG3.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

Examine password and account lockout configurations. <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG4.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

New policy has been set to use a minimum of 10 characters for passwords. The GPO Default Domain Policy was chosen to edit for all computers.   <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG5.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

Navigate to: Computer Configurations -> Policies -> Windows Setting -> Security Settings -> Account Policies -> Password Policy and changing the required policy value to 10.    <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG6.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- <b>Restricting Access to Control Panel</b> <br/>
Standard users should not have access to Control Panel settings, while IT staff retain administrative access. First, I create a new Group Policy Object named Restrict Control Panel Access.  <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG7.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

Enabled the policy under: User Configuration -> Administrative Templates -> Control Panel ->.  <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG8.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

Linked the GPO to the appropriate Organizational Units while excluding the IT department.  <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG9.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

- <b>Auto Lock Screen in GPO</b> <br />
To improve endpoint security, workstations should automatically lock after a period of inactivity. First, I create a new Group Policy Object named Auto Lock Screen.
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG10.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br /> 

Configure the Machine Inactivity Limit policy under: Computer Configurations -> Policies -> Windows Setting -> Security Settings -> Local Policies -> Security Options. Set the inactivity timeout to 300 seconds (5 minutes)  <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG11.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />

Linked the policy at the domain level to enforce the setting across managed devices.  <br />
<br />
<p align="center">
<img src="https://github.com/DanielYoon82/ActiveDirectoryComputersGroups/blob/main/image/ActiveDirectoryCG12.jpg" height="95%" width="95%" alt="Disk Sanitization Steps"/>
</p>
<br />


- <b>Summary</b> <br />
This lab demonstrates core Windows Server administration skills through the organization of Active Directory objects and the deployment of Group Policy Objects. Tasks included creating Organizational Units, managing computer objects, configuring domain password policies, restricting user access through Group Policy, and enforcing automatic workstation lock policies. These exercises reflect common responsibilities performed by IT Support and Systems Administrators in enterprise Windows environments.
<br />
<br />
