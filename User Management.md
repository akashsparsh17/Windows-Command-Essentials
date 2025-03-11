
###### Table of Contents

- [Types of Groups in Windows](#Types%20of%20Groups%20in%20Windows)
- [1. Local Groups](#1.%20Local%20Groups)
	- [Common Local Groups and Their Roles:](#Common%20Local%20Groups%20and%20Their%20Roles:)
- [2. Built-in Security Groups](#2.%20Built-in%20Security%20Groups)
	- [Key Built-in Security Groups:](#Key%20Built-in%20Security%20Groups:)
- [3. Special Identity Groups](#3.%20Special%20Identity%20Groups)
	- [Common Special Identity Groups:](#Common%20Special%20Identity%20Groups:)
- [4. Domain Groups (in Active Directory environments)](#4.%20Domain%20Groups%20(in%20Active%20Directory%20environments))
	- [Common Domain Groups in Active Directory:](#Common%20Domain%20Groups%20in%20Active%20Directory:)
- [5. Custom Groups](#5.%20Custom%20Groups)
	- [Examples of Custom Groups:](#Examples%20of%20Custom%20Groups:)
		- [User Management commands](#User%20Management%20commands)
			- [View User Privileges](#View%20User%20Privileges)
			- [view Users and Groups](#view%20Users%20and%20Groups)
				- [- To list all users](#-%20To%20list%20all%20users)
				- [- To get details about a specific user](#-%20To%20get%20details%20about%20a%20specific%20user)
				- [- to get details about local groups](#-%20to%20get%20details%20about%20local%20groups)
			- [Managing Users](#Managing%20Users)
				- [- To add a new user](#-%20To%20add%20a%20new%20user)
				- [To delete user](#To%20delete%20user)
				- [update User password](#update%20User%20password)
				- [Add user into group](#Add%20user%20into%20group)
				- [Remove user from group](#Remove%20user%20from%20group)
			- [Enable and Disable Accounts](#Enable%20and%20Disable%20Accounts)
				- [- To enable a user account](#-%20To%20enable%20a%20user%20account)
				- [To disable a user account](#To%20disable%20a%20user%20account)


# User Management

## Types of Groups in Windows

Windows operating systems use various groups to manage permissions and access control. These groups help administrators define roles and access levels for different users.

---

## 1. Local Groups

Local groups exist on a single computer and are used to manage access and permissions for users on that machine. They are stored in the **Local Security Authority (LSA)** database.

### Common Local Groups and Their Roles:

- **Administrators**
    
    - Have full control over the system, including installing software, managing system settings, and modifying other user accounts.
        
    - **Example:** A user in the Administrators group can enable or disable the firewall and change system policies.
        
- **Power Users**
    
    - Have more privileges than standard users but fewer than administrators. They can install software and modify system settings that do not affect other users.
        
    - **Example:** A department head who needs to install specialized software without requiring full administrator rights.
        
- **Users**
    
    - Can run most applications but cannot make system-wide changes or install software.
        
    - **Example:** A company employee using office applications without the ability to modify network settings.
        
- **Guests**
    
    - Have very limited access, typically used for temporary access without the ability to change settings or install software.
        
    - **Example:** A visiting consultant logging in to check emails but restricted from accessing confidential files.
        
- **Backup Operators**
    
    - Can override file permissions to back up and restore files on the computer.
        
    - **Example:** IT staff responsible for scheduled backups of important data.
        
- **Remote Desktop Users**
    
    - Can access the system remotely via **Remote Desktop Protocol (RDP)**.
        
    - **Example:** A remote employee connecting to the office workstation from home.
        
- **Network Configuration Operators**
    
    - Can modify networking settings without full administrative privileges.
        
    - **Example:** A network administrator managing network settings remotely.
        

---

## 2. Built-in Security Groups

Built-in security groups are automatically created during the installation of Windows and are used to manage system-wide permissions.

### Key Built-in Security Groups:

- **Authenticated Users**
    
    - Includes all users who have logged in with valid credentials.
        
    - **Example:** Any employee logging in with their corporate username and password.
        
- **Everyone**
    
    - Includes all users, including guests and those who have not been authenticated.
        
    - **Example:** A public folder accessible by both employees and visitors.
        
- **System**
    
    - Represents the operating system itself and has full control over system processes and security settings.
        
    - **Example:** The Windows Update service running system-level updates.
        
- **Creator Owner**
    
    - Assigns special permissions to the user who created a file or folder.
        
    - **Example:** A user creating a private document and automatically becoming its owner.
        
- **Service**
    
    - Includes all accounts running services (e.g., background processes).
        
    - **Example:** The "Local Service" or "Network Service" account used by system processes.
        

---

## 3. Special Identity Groups

Special identity groups do not have explicit members; their membership is determined dynamically by how a user accesses the system.

### Common Special Identity Groups:

- **Anonymous Logon**
    
    - Includes users who access the system without authentication.
        
    - **Example:** A public-facing web server allowing anonymous access to view basic information.
        
- **Interactive**
    
    - Includes users who log in to the system locally.
        
    - **Example:** A user physically logging into their workstation.
        
- **Network**
    
    - Includes users accessing the system over a network.
        
    - **Example:** A file server being accessed from another machine in the office.
        
- **Dialup**
    
    - Includes users connecting via dial-up modems.
        
    - **Example:** A legacy system allowing remote access via a telephone line.
        
- **Terminal Server Users**
    
    - Includes users logged in via a remote session through a **Terminal Server**.
        
    - **Example:** Employees using a corporate remote desktop server to access company resources.
        
- **Remote Interactive Logon**
    
    - Includes users logging in remotely using tools like **Remote Desktop Connection (RDC)**.
        
    - **Example:** A support technician accessing a client’s computer remotely.
        

---

## 4. Domain Groups (in Active Directory environments)

Domain groups exist in **Active Directory (AD)** environments and provide centralized management of users and resources across multiple computers.

### Common Domain Groups in Active Directory:

- **Enterprise Admins**
    
    - Have administrative control over all domains in a **forest** (a collection of domains).
        
    - **Example:** A global IT administrator managing user accounts and policies across different company branches.
        
- **Domain Admins**
    
    - Have full administrative control within a **single domain**.
        
    - **Example:** A system administrator responsible for managing all computers and users in a corporate office.
        
- **Domain Users**
    
    - Includes all standard user accounts in the domain.
        
    - **Example:** Every employee with a company login ID.
        
- **Domain Guests**
    
    - Includes guest accounts with very limited access.
        
    - **Example:** A contractor temporarily accessing non-sensitive company resources.
        
- **Schema Admins**
    
    - Can modify the Active Directory **schema** (the database structure of AD).
        
    - **Example:** A specialist adding new user attributes to support an HR system integration.
        
- **Group Policy Creator Owners**
    
    - Can create and manage **Group Policy Objects (GPOs)** in Active Directory.
        
    - **Example:** An IT security officer defining password-complexity rules for all users.
        

---

## 5. Custom Groups

Administrators can create **custom groups** to manage access to specific resources or applications. These groups help enforce the **Principle of Least Privilege (PoLP)** by restricting permissions only to what is necessary.

### Examples of Custom Groups:

- **Finance Team**
    
    - Members have access to financial records and accounting software but cannot access HR or IT data.
        
- **Developers**
    
    - Members can modify code repositories but do not have administrative privileges over production servers.
        
- **Help Desk Technicians**
    
    - Members can reset passwords and troubleshoot IT issues but cannot install new software without approval.
        

---


#### User Management commands

##### View User Privileges

To list user privileges

```cmd
whoami /all
```

![](attachments/Pasted%20image%2020250304072726.png)

---

##### view Users and Groups

###### - To list all users
```cmd
net user
```

![](attachments/Pasted%20image%2020250304072941.png)

###### - To get details about a specific user
```cmd
net user Armour
net user u1
net user %username%
```

![](attachments/Pasted%20image%2020250304073324.png)

###### - to get details about local groups

```cmd
net localgroup
```

![](attachments/Pasted%20image%2020250304073445.png)

To get details about a specific group
```cmd
net localgroup administrators
```

![](attachments/Pasted%20image%2020250304073806.png)


---

##### Managing Users

###### - To add a new user
```cmd
net user u1 /add
```

![](attachments/Pasted%20image%2020250304075059.png)

add user with passsword
```cmd
net user armour test@123 /add
```

*armour*     -     Username
*test@123*     -     Password


![](attachments/Pasted%20image%2020250304075254.png)


###### To delete user 
```cmd
net user u1 /delete
```

![](attachments/Pasted%20image%2020250304080159.png)

###### update User password
```cmd
net user armour 1234
```

![](attachments/Pasted%20image%2020250304080424.png)

###### Add user into group

```cmd
net localgroup administrators u1 /add
```

*administrators*     -     Group name
*u1*     -     Username

![](attachments/Pasted%20image%2020250304075651.png)


###### Remove user from group

```cmd
net localgroup "Remote Desktop Users" u1 /delete
```

![](attachments/Pasted%20image%2020250304083150.png)


---

##### Enable and Disable Accounts

###### - To enable a user account
```cmd
net user Guest /active:yes
```

![](attachments/Pasted%20image%2020250304081114.png)

![](attachments/Pasted%20image%2020250304081349.png)

![](attachments/Pasted%20image%2020250304081510.png)


###### To disable a user account
```cmd
net user guest /active:yes
```


