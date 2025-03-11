
###### Table of Contents

- [1. Change Directory (cd)](#1.%20Change%20Directory%20(cd))
- [2. system Information (systeminfo):](#2.%20system%20Information%20(systeminfo)
- [3. Windows Version (ver)](#3.%20Windows%20Version%20(ver))
- [4. Current User detail (whoami)](#4.%20Current%20User%20detail%20(whoami))
- [5. Print a Message (echo),](#5.%20Print%20a%20Message%20(echo),)
- [6. Display Environment Variables (set)](#6.%20Display%20Environment%20Variables%20(set))
- [7. Display system PATH (echo %PATH% or path )](#7.%20Display%20system%20PATH%20(echo%20%25PATH%25%20or%20path%20))
- [8. Display environment variable value ( echo %\<variable name\>%)](#8.%20Display%20environment%20variable%20value%20(%20echo%20%25%5C%3Cvariable%20name%5C%3E%25))
- [9. Create a File ( > Redirection Operator)](#9.%20Create%20a%20File%20(%20%3E%20Redirection%20Operator))
- [10. View File contents (type)](#10.%20View%20File%20contents%20(type))
- [11. Change Directory to SystemRoot ( cd %SystemRoot% )](#11.%20Change%20Directory%20to%20SystemRoot%20(%20cd%20%25SystemRoot%25%20))
- [12. Define a New Environment Variable ( set DEMO=Armour )](#12.%20Define%20a%20New%20Environment%20Variable%20(%20set%20DEMO=Armour%20))
- [13.  Displays a list of files and Subdirectories (dir)](#13.%20%20Displays%20a%20list%20of%20files%20and%20Subdirectories%20(dir))
- [13. Create a New Folder (md or mkdir)](#13.%20Create%20a%20New%20Folder%20(md%20or%20mkdir))
- [14. Delete Folder  (rd or rmdir)](#14.%20Delete%20Folder%20%20(rd%20or%20rmdir))
- [15. Delete a File (del)](#15.%20Delete%20a%20File%20(del))
- [16. Display or set Date & Time](#16.%20Display%20or%20set%20Date%20&%20Time)
- [17. Rename a File or Folder (ren or rename)](#17.%20Rename%20a%20File%20or%20Folder%20(ren%20or%20rename))
- [18. Get MAC Address of the System](#18.%20Get%20MAC%20Address%20of%20the%20System)
- [19. Exit Command Prompt (exit)](#19.%20Exit%20Command%20Prompt%20(exit))
- [20. Change Command Prompt Title](#20.%20Change%20Command%20Prompt%20Title)
- [21. Pause Execution (pause)](#21.%20Pause%20Execution%20(pause))
- [22. Change Command Prompt Display (prompt)](#22.%20Change%20Command%20Prompt%20Display%20(prompt))
- [23. Call another Batch File (call)](#23.%20Call%20another%20Batch%20File%20(call))
- [24. Copying Files and Folders in Windows](#24.%20Copying%20Files%20and%20Folders%20in%20Windows)
- [25. Changing File and Folder Attributes Using ATTRIB](#25.%20Changing%20File%20and%20Folder%20Attributes%20Using%20ATTRIB)
- [26. Taking Ownership of a File Using TAKEOWN](#26.%20Taking%20Ownership%20of%20a%20File%20Using%20TAKEOWN)
- [27. Modifying File Permissions with CACLS Command](#27.%20Modifying%20File%20Permissions%20with%20CACLS%20Command)
- [28. Managing File and Folder Permissions in Windows with ICACLS command](#28.%20Managing%20File%20and%20Folder%20Permissions%20in%20Windows%20with%20ICACLS%20command)
- [Understanding the ACL Entries](#Understanding%20the%20ACL%20Entries)
- [Key Observations](#Key%20Observations)
- [Basic Access Permissions](#Basic%20Access%20Permissions*)
- [Inheritance Settings in ICACLS](#Inheritance%20Settings%20in%20ICACLS)
- [Detailed Permissions](#Detailed%20Permissions)
- [29 Restarting a Windows system](#29%20Restarting%20a%20Windows%20system)
- [30 Tasklist](#30%20Tasklist)

###### 1. Change Directory (cd)
Displays the current working directory.

```cmd
cd
```

![](attachments/Pasted%20image%2020250226185847.png)

To navigate to a specific folder:

```cmd
cd <path>

cd Users\win11
```

![](attachments/Pasted%20image%2020250226193332.png)

<br> 
---

###### 2. system Information (systeminfo)
Displays detailed information about the system, including OS version, hardware specs, network configuration, and uptime.

```
systeminfo 
```

![](attachments/Pasted%20image%2020250226193502.png)

<br> 
---
<br>

###### 3. Windows Version (ver)
Displays the current Windows operating system version.

```cmd
ver 
```

![](attachments/Pasted%20image%2020250226193641.png)

<br> 
---
<br>
###### 4. Current User detail (whoami)
Shows the currently logged-in user, including the domain (e.g., DESKTOP\User).

```cmd
whoami
```

![](attachments/Pasted%20image%2020250226193915.png)

Show detail information about logged-in user. ( User Information , Group Information and Privilege Information )

```cmd
whoami /all
```

![](attachments/Pasted%20image%2020250226194430.png)

<br> 
---
<br>
###### 5. Print a Message (echo), 
Displays the text "Armour Infosec" in the command prompt.

```cmd
echo Armour Infosec
```

![](attachments/Pasted%20image%2020250226194636.png)

<br> 
---
<br>
###### 6. Display Environment Variables (set) 
Display  All system environment variables and their values.

```cmd
set 
```

![](attachments/Pasted%20image%2020250226195036.png)

<br> 
---
<br>
###### 7. Display system PATH (echo %PATH% or path )
Shows the directories where executable files are searched when running commands.
If command or application is available below path then we can run it  using cmd without specifying it's whole path.

```cmd
echo %PATH%
	OR
path 
```

![](attachments/Pasted%20image%2020250226200355.png)
<br> 
---
<br>
###### 8. Display environment variable value ( echo %\<variable name\>%)

```cmd
echo %USERNAME%

echo %SystemRoot%

echo %cd%
```

![](attachments/Pasted%20image%2020250226201007.png)
<br> 
---
<br>
###### 9. Create a File ( > Redirection Operator)
Creates a file 1.txt and writes "Armour" into it.
```cmd
echo "Armour" > 1.txt
```

![](attachments/Pasted%20image%2020250226201705.png)
<br> 
---
<br>
###### 10. View File contents (type)
Displays the content of the File in the command prompt 
```cmd
type <filename.txt>

type 1.txt
```

![](attachments/Pasted%20image%2020250226201842.png)

<br> 
---
<br>
###### 11. Change Directory to SystemRoot ( cd %SystemRoot% )
%systemRoot% is an environment variable that points to the Windows installation directory ( typically  C:\Windows ).

```cmd
cd %SystemRoot%
```

![](attachments/Pasted%20image%2020250226202835.png)

<br> 
---
<br>
###### 12. Define a New Environment Variable ( set DEMO=Armour )
Creates a temporary environment variable DEMO with the value "Armour".

``` cmd
set DEMO=Armour 

echo %DEMO% ---> use to show DEMO environment variable value 
```

![](attachments/Pasted%20image%2020250226203206.png)

<br> 
---
<br>
###### 13.  Displays a list of files and Subdirectories (dir) 
 
Display Help for dir Command, Displays all available options and usage details for the dir command

```cmd
dir /?
```

![](attachments/Pasted%20image%2020250226205322.png)

Listing Files and Folders

```cmd
dir 
```

![](attachments/Pasted%20image%2020250226211114.png)

Display Short File Names (8.3 Format), shows files with their short (8.3) filenames, used for backward compatibility.

```cmd
dir /x
```

![](attachments/Pasted%20image%2020250226211306.png)

Display Files in a Folder in Bare Format,

```cmd
dir /b 
```

*/b*   -  Removes extra details (shows only full paths)  

![](attachments/Pasted%20image%2020250226211548.png)

Display recursive directory contains 

```cmd
dir /s
```

*/s*  -  subdirectories / recursive 
![](attachments/Pasted%20image%2020250226212819.png)

List Only Hidden and System Files 

```cmd
dir /A:SH 
```

*/A*  -  Use to define attribute 
*SH*    -  System hidden Files 

![](attachments/Pasted%20image%2020250226213329.png)

List Only Hidden Files 

```cmd
dir /A:H 
```

![](attachments/Pasted%20image%2020250226213458.png)

Also we can use more that one options in single run

```
dir /s /b
dir /A:SH /b /S
dir /A:H /S /b 
```

<br> 
---
<br>
###### 13. Create a New Folder (md or mkdir)
Creates a folder named NewFolder in the current directory.

```cmd
md NewFolder 

	OR

mkdir NewFolder1
```

![](attachments/Pasted%20image%2020250226214553.png)


Create Multiple Folders at Once

```cmd
md Folder1 Folder2 Folder3

	OR

mkdir Folder1 Folder2 Folder3
```

![](attachments/Pasted%20image%2020250226215108.png)

Create Multiple Nested Directories (Subdirectories in one Command)

```cmd
md Parent\Child\GrandChild

	OR

mkdir Parent\Child\GrandChild
```

![](attachments/Pasted%20image%2020250226215542.png)
<br> 
---
<br>

###### 14. Delete Folder  (rd or rmdir)
Delete an Empty Folder, Deletes the data folder only if it is empty.

```cmd
rd data 

	OR

rmdir data
```

![](attachments/Pasted%20image%2020250226234420.png)

Delete a Folder Without confirmation 

```cmd
rd data /q

	OR

rmdir data /q
```

*/q*   -   quite mode 

Delete a Folder and All Its Contents 

```cmd
rd data /s /q

	OR

rmdir data /s /q
```

*/s*   -    Removes directory , subdirectories and files 
<br> 
---
<br>
###### 15. Delete a File (del)
```cmd
del <filename.txt>

del 1.txt
```

![](attachments/Pasted%20image%2020250226235241.png)

Delete Files Recursively 

```
del /s /f /q data 
```

*/s*    -   Deletes all matching files in subdirectories.
*/f*    -   Force delete read-only files.
*/q*   -   Quiet mod (no confirmation).

<br> 
---
<br>
###### 16. Display or set Date & Time
```cmd
date 

time 
```

<br> 
---
<br>
###### 17. Rename a File or Folder (ren or rename)
```cmd
ren oldname newname

	OR

rename oldname newname
```

<br> 
---
<br>
###### 18. Get MAC Address of the System 
```cmd
getmac 
```

![](attachments/Pasted%20image%2020250226235016.png)
<br> 
---
<br>
###### 19. Exit Command Prompt (exit)

```cmd
exit
```

<br> 
---
<br>
###### 20. Change Command Prompt Title

```cmd
title Armour 
```

![](attachments/Pasted%20image%2020250226235914.png)

<br> 
---
<br>
###### 21. Pause Execution (pause)
Displays "Press any key to continue... " and waits for user input.

```cmd
pause
```

<br> 
---
<br>
###### 22. Change Command Prompt Display (prompt)
```cmd
prompt 

prmompt MyPrompt
```

![](attachments/Pasted%20image%2020250227000852.png)
<br> 
---
<br>
###### 23. Call another Batch File (call)
Runs runme.bat without stopping the current script execution.

```cmd
call c:\runme.bat
```

<br> 
---
<br>
###### 24. Copying Files and Folders in Windows 
Copying Files and folders in Windows 

- Basic Copying with COPY

```cmd
copy /a <source file>  <destination>

copy /a c:\data\file.txt  e:\data  /v /y
```

*/a*   -   Specifies the source file (ASCII mode).
*/v*   -   Verifies the copied file for accuracy.
*/y*   -   Suppresses confirmation prompts when overwriting existing files.

**Note : ** Using copy command we can copy single file 
<br> 
---
<br>
-  Advanced Copying with XCOPY 
XCOPY is a more powerful alternative to COPY for copying directories , files  ,and subdirectories.

```cmd
 xcopy  d:\data\*.*  c:\test\ /a /d /p /s /v /w
```

*/a*   -   Copies only files with the archive attribute.
*/d*   -   Copies files modified after a specified data.
*/p*   -   Prompts before copying each file.
*/s*   -   Copies directories and subddirectories, except empty ones.
*/v*   -   Verifies copied files.
*/w*  -   Waits for confirmation before starting.

<br> 
---
<br>
- Robust Copying with ROBOCOPY

ROBOCOPY (Robust File Copy)  is a more powerful tool introduced in later Windows version.

Basic ROBOCOPY Usage, Copies all files from C:\data to C:\data1, including subdirectories.

```cmd
robocopy C:\data C:\data1 /s  
```

Copy a Specific File 

```cmd
robocopy <source>  <destination>  <filename>

robocopy C:\data  C:\data1  test.txt  /s 
```

Copy Specific File Types 

```cmd
robocopy e:\data  c:\js *.js /s

robocopy e:\data c:\css  *.css /s

robocopy e:\eata c:\html  *.html /s 
```

Copy Multiple File Types,

```cmd
robocopy C:\data\  C:\allfiles  *.jpg  *.png  *.png *.html *.txt /s

robocopy C:\data\ C:\all *.txt *.css *.js /s 
```

**Additional Options **

*/r:1*     -    Retries once if a file fails to copy.
*/w:1*    -   Waits one second between retries.
*/ndl*     -   Prevents directories from being listed in the output.
*/xjd*     -   Excludes junction points (to avoid infinite loops).

<br> 
---
<br>
###### 25. Changing File and Folder Attributes Using ATTRIB
The ATTRIB command in Windows allows users to modify file and folder attributes such as Hidden, System, Read-Only, and Archive.

**Basic Syntax**
```cmd
attrib  [filename]
```

Display help information for the attrib command.

```cmd
attrib /?
```

![](attachments/Pasted%20image%2020250227085015.png)

Attribute Flags

| Flag                                   | Description                           |
| -------------------------------------- | ------------------------------------- |
| +H / -H                                | Adds / removes the Hidden attribute   |
| +S / -S                                | Add / removes the System attribute    |
| +R / -R                                | Add / removes the Read-Only attribute |
| +A / -A                                | Adds / removes the Archive attribute  |
| /S                                     | Applies changs to all subdirectories  |
| /D                                     | Applies changes to directories        |

Modifying File Attributes. 

Make a file hidden, System, and Read-Obly

```cmd
attrib +s +h +r test.txt
```

![](attachments/Pasted%20image%2020250227090235.png)


Remove System, Hidden, and Read-Only attributes

```cmd
attrib -s -h -r test.txt
```

![](attachments/Pasted%20image%2020250227090643.png)


Applying attribute to All Files in a Directory

Apply Hidden, System, and Read-Only attributes to all files  it's not apply on folders

```cmd
attrib +s +h +r  C:\data\* /s
```


Applying Attributes to All files in a Directory

Apply  Hidden, System, and Read-Only attributes to all files 

```cmd 
attrib +s +h +r E:\* /s      # hidden all files except directories from E drive 

attrib +s +r +h E:\* /S /D   # hidden all files and directories from E drive 
```


Remove Hidden, System, and Read-Only attributes from all files 

```cmd
attrib -s -h -r E:\* /s   
```


Protecting a file from accidental deletion

```cmd
attrib +r important.docx 
```

<br> 
---
<br>
###### 26. Taking Ownership of a File Using TAKEOWN

The TAKEOWN command in Windows allows an administrator to take ownership of files and folders, especially when access is denied due to permission issues. 

Displays help information for the TAKEOWN command 

```cmd
takeown /?
```

![](attachments/Pasted%20image%2020250227210326.png)

Basic Syntax 

```cmd
takeown /F <filename>
```

Takes ownership of a Specified file

```cmd
takeown /F secret.txt
```

Takes ownership of all files recursively in a folder

```cmd
takeown /F <foldername> /R /D Y

takeown /F logs /R /D y
```

![](attachments/Pasted%20image%2020250227210953.png)


Take Ownership of All Files in a Drive 

```cmd
takeown /F E:\* /R /D Y 
```

<br> 
---
<br>
###### 27. Modifying File Permissions with CACLS Command

The CACLS command is used to view and modify file access control lists (ACLs) in Windows. However, CACLS is deprecated and replaced by ICACLS in modern Windows version

Shows the current permission of the specified file
```cmd
cacls <filename>

cacls iisstart.htm
```

![](attachments/Pasted%20image%2020250227211819.png)


Grants a specific user the specified permissions.

```cmd
 cacls <filename> /G <username>:<permission> 

cacls iisstart.htm /G Armour:F
```



*Permission Levels in CACLS*

When using `CACLS`, the permission levels are represented by specific letters:

| **Permission**   | **Symbol** | **Description** |
|-----------------|-----------|----------------|
| **Read**        | `R`       | Allows the user to read the file/folder but not modify it. |
| **Write**       | `W`       | Allows the user to write or modify the file. |
| **Change**      | `C`       | Grants both `R` (Read) and `W` (Write) permissions. |
| **Full Control**| `F`       | Grants full access, including the ability to delete or modify permissions. |
<br> 
<br>
---
<br> 
<br>
###### 28. Managing File and Folder Permissions in Windows with ICACLS command

ICACLS is the modern command-Line tool in Windows for managing file and folder permissions. IT replaces CACLS and provides more granular control over Access Control Lists (ACLs).

Basic Syntax

```cmd
ICACLS <File_or_Folder> [Options]
```

Displays the current ACLs of iisstart.png 

```cmd
ICACLS  iisstart.png 
```

![](attachments/Pasted%20image%2020250227212733.png)


Modifying Permissions, Grant Permissions 
Grants Full control (F) to Armour 

```cmd
icacls iisstart.htm /grant Armour:F
```

![](attachments/Pasted%20image%2020250227213112.png)

Grants Read (R) access to Everyone.

```cmd
icacls iisstart.htm /grant Everyone:R
```

![](attachments/Pasted%20image%2020250227213237.png)


Remove Permissions,

Remove Everyone from the ACL list 

```cmd
icacls iisstart.htm /remove Everyone 
```

![](attachments/Pasted%20image%2020250227213431.png)


Modify Inheritance
Disables inheritance for the file.

```cmd
icacls iisstart.htm /inheritance:d
```

Enable inheritance for the file.

```cmd
icacls iisstart.htm /inheritance
```


Set Ownership
Changes the owner to Administrator.

```cmd
icacls iisstart.htm /setowner Administrator
```


Backup and Restore ACLs

Saves current ACLs to backup_acl.txt

```cmd
icacls iisstart.htm /save /C:\backup_acl.txt 
```

![](attachments/Pasted%20image%2020250228071229.png)

![](attachments/Pasted%20image%2020250228071316.png)

Restores ACLs from backup_acl.txt

```cmd
icacls iisstart.htm  /restore  backup_acl.txt
```



**Permission Levels in ICACLS**

In Windows, `ICACLS` is the recommended command-line utility for viewing and modifying file and folder permissions. It provides more flexibility than the older `CACLS`.  


*Standard Permission Levels in ICACLS*

| **Permission**       | **Symbol** | **Description** |
|----------------------|-----------|----------------|
| **Full Control**     | `F`       | Grants all permissions, including modifying permissions and taking ownership. |
| **Modify**          | `M`       | Allows reading, writing, executing, and deleting files. |
| **Read & Execute**   | `RX`      | Allows viewing and executing files. |
| **Read**            | `R`       | Allows viewing files but not modifying them. |
| **Write**           | `W`       | Allows modifying and creating files but not deleting them. |


*Advanced (Special) Permissions in ICACLS * 

| **Permission**                     | **Symbol** | **Description** |
|-------------------------------------|-----------|----------------|
| **Traverse Folder / Execute File**  | `RX`      | Allows navigating through folders and executing files. |
| **List Folder / Read Data**         | `R`       | Allows listing folder contents or reading file data. |
| **Read Attributes**                 | `R`       | Grants access to file attributes (e.g., read-only, hidden). |
| **Read Extended Attributes**        | `R`       | Grants access to additional metadata. |
| **Create Files / Write Data**       | `W`       | Allows modifying file contents. |
| **Create Folders / Append Data**    | `W`       | Allows adding data to existing files or creating folders. |
| **Write Attributes**                | `W`       | Allows modifying file attributes. |
| **Write Extended Attributes**       | `W`       | Allows modifying metadata. |
| **Delete**                          | `D`       | Grants permission to delete the file or folder. |
| **Delete Subfolders and Files**     | `D`       | Allows deleting all contents inside a folder. |
| **Change Permissions**              | `P`       | Allows modifying permissions. |
| **Take Ownership**                  | `O`       | Grants control to change ownership of the file/folder. |

Grant read Access to a folder & subfolders

Grants Read (R) permission to Everyone recursively (/t).

```cmd
icacls C:\MyFolder  /grant  Everyone:R /t
```


Remove All Permissions for a User

Removes all  Permissions  for Armour

```cmd
icacls  C:\example.txt  /remove Armour
```


Reset All Permissions to Default

Resets permissions to default settings

```cmd
icacls  C:\example.txt  /reset 
```



##### Understanding the ACL Entries

| **Entry**                                      | **Meaning** |
|------------------------------------------------|------------|
| `DESKTOP-SQPBP0N\Armour:(F)`                   | The Armour user has Full Control (F) over the file. |
| `BUILTIN\IIS_IUSRS:(RX)`                       | The IIS_IUSRS group has Read & Execute (RX) permissions. |
| `NT SERVICE\TrustedInstaller:(F)`              | The TrustedInstaller service has Full Control (F) over the file. |
| `NT AUTHORITY\SYSTEM:(F)`                      | The SYSTEM account has Full Control (F). |
| `BUILTIN\Administrators:(F)`                   | The Administrators group has Full Control (F). |
| `BUILTIN\Users:(RX)`                           | All Users have Read & Execute (RX) permissions. |
| `DESKTOP-SQPBP0N\Administrator:(F)`            | The Administrator account has Full Control (F). |
| `BUILTIN\IIS_IUSRS:(I)(RX)`                    | The `(I)` means this permission is inherited from a parent folder. |
| `NT SERVICE\TrustedInstaller:(I)(F)`           | Inherited Full Control (F) for TrustedInstaller. |
| `NT AUTHORITY\SYSTEM:(I)(F)`                   | Inherited Full Control (F) for SYSTEM. |
| `BUILTIN\Administrators:(I)(F)`                | Inherited Full Control (F) for Administrators. |
| `BUILTIN\Users:(I)(RX)`                        | Inherited Read & Execute (RX) for Users. |
| `DESKTOP-SQPBP0N\Administrator:(I)(F)`         | Inherited Full Control (F) for Administrator. |


##### Key Observations

**"Inherited" (I) Entries
- The file inherits permissions from its parent folder (`C:\inetpub\wwwroot`).
- Any changes to `C:\inetpub\wwwroot` will affect this file unless inheritance is disabled.

**Permissions Breakdown
- Administrator, SYSTEM, TrustedInstaller, and Administrators** have **Full Control**.
- Users and IIS_IUSRS** have **Read & Execute** access.
- The Armour user** has **explicit Full Control**.


##### Basic Access Permissions*

| **Flag** | **Meaning**                             |
| -------- | --------------------------------------- |
| `D`      | Delete access                           |
| `F`      | Full access (includes all permissions)  |
| `N`      | No access                               |
| `M`      | Modify access (read, write, and delete) |
| `RX`     | Read & Execute                          |
| `R`      | Read-only                               |
| `W`      | Write-only                              |

##### Inheritance Settings in ICACLS

These flags control how permissions propagate to child objects (files/folders):

| **Flag** | **Meaning** |
|----------|---------------------------------------------------------------|
| `(OI)`   | **Object Inherit** → Applies to files within a folder. |
| `(CI)`   | **Container Inherit** → Applies to subfolders within a folder. |
| `(IO)`   | **Inherit Only** → Does not apply to this folder, only to child objects. |
| `(NP)`   | **No Propagate Inherit** → Inherited permissions will not be passed down further. |
| `(I)`    | **Inherited** → This permission is inherited from the parent folder. |

##### Detailed Permissions

These fine-tune access control:

| **Flag** | **Meaning**                           |
| -------- | ------------------------------------- |
| `DE`     | Delete                                |
| `RC`     | Read control (view security settings) |
| `WDAC`   | Write DAC (change security settings)  |
| `WO`     | Write owner (change file owner)       |
| `S`      | Synchronize (used for processes)      |
| `AS`     | Access system security                |
| `MA`     | Maximum allowed permissions           |
| `GR`     | Generic Read                          |
| `GW`     | Generic Write                         |
| `GX`     | Generic Execute                       |
| `GA`     | Generic All (Full Control)            |
| `RD`     | Read Data / List Directory            |
| `WD`     | Write Data / Add File                 |
| `AD`     | Append Data / Add Subdirectory        |
| `REA`    | Read Extended Attributes              |
| `WEA`    | Write Extended Attributes             |
| `X`      | Execute / Traverse                    |
| `DC`     | Delete Child                          |
| `RA`     | Read Attributes                       |
| `WA`     | Write Attributes                      |

<br> 
---
<br>
###### 29 Restarting a Windows system 
Restarting a Windows system immediately without any delay

```cmd
shutdown /r /t 0 /f 
```

*/r*      -   Restart the computer.
*/t 0*   -   Set the time delay to 0 seconds (immediate restart).
*/f*      -   Force close all running applications without warning.


Warning before restart

Restart the system after 60 seconds, allowing the user to cancel it with:

```cmd
shutdown /r /t 60 
```

allowing the user to cancel it with:
```cmd
shutdown /a 
```

Shuts down the system after 60 seconds.

```cmd
shutdown /s /t 60
```

Disables Hibernate Mode (frees up space by removing hiberfil.sys )

```cmd
powercfg /h off
```

Generate a detailed battery report (batttery-report.html in C:\Windows\system32)

```cmd
powercfg /batteryreport
```

<br> 
---
<br>
###### 30 Tasklist

lists all running processes

```cmd
tasklist
```

Force kill process

force kill notepad
```cmd
takkill /f /im notepad.exe
```

Kill process by PID

```cmd
taskkill /f /pid 1234
```

