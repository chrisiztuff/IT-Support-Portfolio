# Active Directory Domain Networking Lab
CompTIA Certmaster guided lab | Windows Server | Windows 11 | Active Directory
## Live recorded unlisted video of me doing the guided lab:
https://www.youtube.com/watch?v=kL88qlCQv7U
## What This Project Is About
In this guided lab, I practiced connecting a Windows computer to a company domain, checking network problems, creating a new user, working with a sign-in script, setting Group Policy, and checking folder permissions.
A domain is a way for a company to manage work computers and employee accounts together. The screenshots below come from my recorded training lab. 

## Step 1: Starting the lab 
The lab began on the Windows computers used for this exercise. The administrator account was used for tasks that need extra permission. An administrator is an account that can change important computer settings. 

<details>
<summary>View Image</summary>

<img width="1300" height="708" alt="image" src="https://github.com/user-attachments/assets/0bfeca1a-7360-4c76-8bb2-92da52f06d0d" />

</details>



## Step 2: Checking PC11

Step 1: Joining PC11 to the Active Directory Domain
On PC11, the sysdm.cpl command was entered using Run to open System Properties.
Under Computer Name → Change, the Domain option was selected, and corp.515support.com was entered.
The domain administrator's credentials were used to authorize PC11 to join the domain.
Joining PC11 to the domain allows it to be managed through Active Directory and lets domain users sign in using their work accounts.
<details>
<summary>View Image</summary>
<img width="1279" height="738" alt="image" src="https://github.com/user-attachments/assets/7b7a6ba6-e5d9-49a9-90dc-141fbce94b26" />
</details>

## Step 3: Entering the domain administrator account 
PC11 was set to join `corp.515support.com`. Windows asked for an account allowed to join the domain. The account `515support\administrator` was entered, along with the lab password.
This check stops just anyone from adding computers to the company network.
<details>
<summary>View Image</summary>
<img width="908" alt="Domain Controller Setup" src="https://github.com/user-attachments/assets/be632264-46a4-4545-874d-a2685870a751" />
</details>

## Step 4: Confirming PC11 joined the domain 
Windows showed “Welcome to the corp.515support.com domain.” This confirmed that PC11 joined the domain successfully. A domain lets a company manage many work computers and accounts together.
<details>
<summary>View Image</summary>
<img width="913" height="525" alt="image" src="https://github.com/user-attachments/assets/1cdb491f-90e1-4d1f-b84b-59c3a192fce3" />
</details>

## Step 5: Signing in after joining 
After PC11 joined the domain, a domain account was used to sign in. Jaime is a test user created to represent a regular employee in the company. This demonstrates that employees can sign in to company computers using their domain accounts instead of needing separate accounts for every computer.
<details>
<summary>View Image</summary>
<img width="1280" height="712" alt="05_04-30_domain-user-sign-in" src="https://github.com/user-attachments/assets/13727907-2f87-47bd-9f8e-51650212bf89" />
</details>

## Step 6 Checking PC11 Network Information
PowerShell was used to run the hostname and ipconfig commands.
The hostname command confirmed the computer name was PC11. The ipconfig command displayed its IP address, subnet mask, default gateway, and DNS suffix (corp.515support.com).This verifies PC11's network information before testing its connection to other computers and servers.
<details>
<summary>View Image</summary>
<img width="1280" height="712" alt="07_07-30_network-test-results" src="https://github.com/user-attachments/assets/48a19afe-adb9-488d-a535-e4b3484afbb5" />
</details>

## Step 7: Testing Network Connectivity

PowerShell was used to ping PC10 and MS10.
Both devices responded successfully with 0% packet loss. This confirms that PC11 can communicate with other computers and servers on the network.
<details>
<summary>View Image</summary>
<img width="1062" height="687" alt="image" src="https://github.com/user-attachments/assets/c620d103-c721-47e5-b633-e0e765d79a7f" />
</details>

## Step 8 : Opening Active Directory (On device 'DC10')
On the server side of the lab, Active Directory Users and Computers was opened, on Device DC10. This is where domain accounts are managed.
This tool lets IT staff manage accounts from one place.
<details>
<summary>View Image</summary>
<img width="1280" height="712" alt="14_24-30_ad-users-computers" src="https://github.com/user-attachments/assets/2b558254-59a5-4697-9367-8a63259ec984" />
</details>

 ## Step 9: Creating 'Ronnie' 
A new user was created for the `corp.515support.com` domain. The account was created in the `Nonadmins` organizational unit (OU). An OU is like a folder that helps keep company accounts organized. 

<details>
<summary>View Image</summary>
<img width="1280" height="712" alt="16_27-30_nonadmins-ou" src="https://github.com/user-attachments/assets/e6c02253-1fed-4ef2-a63e-67ba39ad274a" />
</details>

The user sign-in name was `ronnie`. A user account gives a person their own work sign-in.

<details>
<summary>View Image</summary>
<img width="1498" height="663" alt="image" src="https://github.com/user-attachments/assets/139040da-c20d-4c40-a24e-ff6f5b0a1af4" /> 
</details>



## Step 10 : Setting Ronnie’s account options 
The account options were set to match the training lab. The lab called for Password never expires and for Ronnie not to change the password at the next sign-in.
These are lab settings, not general advice for real company passwords.
<details>
<summary>View Image</summary>
<img width="1303" height="596" alt="image" src="https://github.com/user-attachments/assets/27d816f7-c149-4450-8642-8b739fbd1eca" />
</details>


## Step 11 Adding a User to a Security Group

In Active Directory Users and Computers, the test user 'ronnie' was selected to be added to the sec-glo-sales security group.
This group represents employees in the Sales department.
Security groups make it easier to manage permissions. Instead of giving each employee access separately, permissions can be assigned to a group.


<details>
<summary>View Image</summary>
<img width="1674" height="736" alt="image" src="https://github.com/user-attachments/assets/684a2d85-258f-4550-bd2f-4f44f48522c2" />
</details>

<details>
<summary>View Image</summary>
<img width="1256" height="698" alt="image" src="https://github.com/user-attachments/assets/9362f651-4403-4965-93b8-604fcf7d1588" />
</details>

## Step 12: Starting the sign-in script task 
The next part of the lab worked with settings and files used when a user signs in.
A sign-in script is a small set of commands that can run automatically at sign-in.
A script was opened in a text editor and worked on as part of the sign-in setup.
This script 'tickets.vbs' was created using Notepad++. The script is designed to create a desktop shortcut called Tickets that opens the company's IT support website.
 Scripts can automate repetitive tasks. Instead of manually creating shortcuts on every computer, administrators can use scripts to make the process easier.
<details>
<summary>View Image</summary>
<img width="1280" height="712" alt="19_30-30_script-in-editor" src="https://github.com/user-attachments/assets/9570cedd-a40a-4d59-b594-ef8658d9ab6c" />
</details>
| Code | Explanation |
|------|--------------------|
| `CreateObject("WScript.Shell")` | Gives the script access to Windows features |
| `SpecialFolders("Desktop")` | Finds the desktop folder |
| `sTarget` | Stores the support website address |
| `CreateObject("Scripting.FileSystemObject")` | Allows the script to create files |
| `CreateTextFile` | Creates a file named `Tickets.url` |
| `BASEURL` and `URL` | Tell the shortcut which website to open |
| `IconFile` and `IconIndex` | Choose the shortcut's icon |
| `Close` | Saves and closes the file |

## Step 13: Saving the VBScript File
The script was saved to the \\DC10\netlogon shared folder on the domain controller.
 The NETLOGON folder allows domain computers to access the script so it can run automatically when assigned users sign in.
The script was saved as 'tickets.vbs' . 
The .vbs extension identifies the file as a VBScript that Windows can execute. Saving the script allows it to be executed to automatically create the IT support website shortcut on the desktop.

<details>
<summary>View Image</summary>
<img width="1321" height="691" alt="image" src="https://github.com/user-attachments/assets/3458c387-94f5-4485-ac90-2b90a3025aca" />
</details>

## Step 14: Configuring a Logon Script for Domain Users
In Active Directory Users and Computers, multiple test user accounts were selected from the Nonadmins Organizational Unit (OU).
The Properties window was opened for the selected users. Under the Profile tab, tickets.vbs was entered in the Logon script field. This allows the script to run automatically when the assigned domain users sign in, creating a shortcut to the company's IT support website on their desktop. 

<details>
<summary>View Image</summary>
<img width="1445" height="698" alt="image" src="https://github.com/user-attachments/assets/e76065a6-9bf2-456e-890b-a18f84fb7e11" />
</details>

<details>
<summary>View Image</summary>
<img width="1457" height="649" alt="image" src="https://github.com/user-attachments/assets/1615e2f0-5256-43fa-8263-1e1cb7e80712" />
</details>



## Step 15: Testing the Logon Script on PC11
PC11 was signed in using Ronnie's domain account. Ronnie is a test user created to represent a regular employee.
After signing in, the tickets.vbs logon script automatically created the Tickets shortcut on the desktop.
This confirms that the logon script works and can automatically provide employees with the company's IT support website shortcut when they sign in.


<details>
<summary>View Image</summary>
<img width="1487" height="771" alt="image" src="https://github.com/user-attachments/assets/54595af0-554e-41d6-aebe-bb84a23f0e66" />
</details>



## Step 16: Configuring Folder Redirection Using Group Policy

In Group Policy Management, a new Group Policy Object (GPO) named 515support Folder Redirection Policy was created and linked to the Nonadmins Organizational Unit (OU).
Under User Configuration → Policies → Windows Settings → Folder Redirection, the Documents folder was configured to redirect to the shared network location \\MS10\ROAMING.
Folder Redirection allows employees' Documents folders to be stored on a central server instead of only on their local computers. This makes files easier to access when employees use different company computers.
<details>
<summary>View Image</summary>
<img width="1524" height="672" alt="image" src="https://github.com/user-attachments/assets/6bdb8f2b-404e-4133-83ae-ea98e509edd7" />
</details>
<details>
<summary>View Image</summary>
<img width="1592" height="656" alt="image" src="https://github.com/user-attachments/assets/62f20a92-0c44-4af2-9204-57001ddde276" />
</details>

## step 17: Begin configuring a shared folder on ms10
The MS10 virtual machine was opened, and the domain account 515support\Jaime was used to sign in.
MS10 was the server used to store shared files for employees.
<details>
<summary>View Image</summary>
<img width="1764" height="771" alt="image" src="https://github.com/user-attachments/assets/c66ee52b-3a1d-4a2c-8b51-14edaf319945" />
</details>

## Step 18: Locating the ROAMING Folder
File Explorer was opened on MS10.
The C:\ drive was selected, and the existing ROAMING folder was located.
This folder would be used to store employees' redirected Documents.
<details>
<summary>View Image</summary>
<img width="1669" height="712" alt="image" src="https://github.com/user-attachments/assets/f0264b82-df66-49b6-8542-a83d4a3461b7" />
</details>

## Step 19: Opening Advanced Sharing
The ROAMING folder was right-clicked, and Properties was selected.
Under the Sharing tab, Advanced Sharing was opened.
This allowed the folder to be shared with other computers on the network.
The Share this folder checkbox was selected.
The share name was set to ROAMING.
The Permissions button was selected to configure who could access the shared folder.
<details>
<summary>View Image</summary>
<img width="1681" height="813" alt="image" src="https://github.com/user-attachments/assets/2d40eaaa-51b9-4373-833e-b1d4f845f42f" />
</details>

## Step 20: Configuring Share Permissions
Under Share Permissions, the Everyone group was selected.
The Allow checkbox for Full Control was checked.
This also enabled Change and Read permissions.
The changes were saved by clicking OK.
Share permissions control what users can do when accessing a folder over the network.
<details>
<summary>View Image</summary>
<img width="1599" height="836" alt="image" src="https://github.com/user-attachments/assets/4815ece0-6682-4d9b-b0bc-6760b33f2b67" />
</details>

## Step 21: Verifying the Shared Folder
The Advanced Sharing window was closed.
Under the Sharing tab, the folder was shown as shared with the network path:
\\MS10\roaming
This confirmed that the ROAMING folder was configured as a network share.
<details>
<summary>View Image</summary>
<img width="1713" height="840" alt="image" src="https://github.com/user-attachments/assets/da0edb84-fd61-4022-b91a-4b9db4bc4445" />
</details>

Configuring NTFS Security Permissions on MS10

Step 1: Opening the ROAMING Folder Security Settings and Disabling Permission Inheritance

On MS10, the C:\ROAMING folder's Properties window was opened.
The Security tab was selected, followed by Advanced.

This opened the advanced security settings, where access to the folder could be managed.

In Advanced Security Settings, the Disable inheritance button was selected.

The option Convert inherited permissions into explicit permissions on this object was chosen.

This stopped the ROAMING folder from automatically receiving permissions from its parent folder, C:\.

The existing permissions were kept so they could be changed manually.
Disabling inheritance allows the ROAMING folder to have its own security permissions instead of automatically using the permissions from the C: drive.

<details>
<summary>View Image</summary>
<img width="1498" height="726" alt="image" src="https://github.com/user-attachments/assets/1d21f3d8-91c6-4fa9-91f8-e6bee635bf4a" />
</details>

Step 3: Removing the Users Group

In the permission entries list, each Users (MS10\Users) entry was selected and removed.

The Remove button was used to delete these entries.

This helped prevent the general local Users group from keeping its previous access permissions.

<details>
<summary>View Image</summary>

</details>

Step 4: Adding Authenticated Users

The Add button was selected in Advanced Security Settings.

Next, Select a principal was clicked.

In the Select User or Group window, authenticated users was entered and Check Names was selected.

After the group was recognized, OK was clicked.

This added the Authenticated Users group to the permission settings.

<details>
<summary>View Image</summary>

</details>

Step 5: Setting Permissions for Authenticated Users

The permission entry for Authenticated Users was configured.

Under Applies to, This folder only was selected.

Next, Show advanced permissions was clicked.

Only the following permissions were checked:

Traverse folder / execute file

Read attributes

Create folders / append data

All other permissions were left unchecked.

Why this matters: These permissions allow authenticated users to create their own folders inside ROAMING without automatically receiving full access to other employees' folders.

<details>
<summary>View Image</summary>

</details>

Step 6: Saving the NTFS Permissions

After configuring the permissions, OK was selected.

The Advanced Security Settings window was closed by clicking OK again.

The ROAMING Properties window was then closed.

The lab's Score button was used to validate the configuration.

<details>
<summary>View Image</summary>

</details>

Why This Lab Matters

NTFS permissions help protect employee files stored on a shared server.

The ROAMING folder was configured so authenticated employees could create their own folders.

The goal was to allow each employee to store Documents in a personal folder without automatically giving other employees access to those files.

This is important for Folder Redirection, where employee Documents are stored on a company server instead of only on individual computers.





What I Learned
This lab helped me understand how a work computer joins a domain, why the computer needs to reach the domain server, how an employee account is created, how sign-in settings and Group Policy work, and how access to folders can be controlled.
Skills Practiced
Joining a Windows computer to a domain
Checking network connections and DNS
Using Active Directory Users and Computers
Creating and organizing a user account
Working with sign-in scripts
Working with Group Policy
Checking shared folders and file permissions
Testing the setup from a user computer


