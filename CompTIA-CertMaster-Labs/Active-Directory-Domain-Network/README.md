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
<img width="1280" height="712" alt="19_30-30_script-in-editor" src="https://github.com/user-attachments/assets/9570cedd-a40a-4d59-b594-ef8658d9ab6c" />

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
<img width="1321" height="691" alt="image" src="https://github.com/user-attachments/assets/3458c387-94f5-4485-ac90-2b90a3025aca" />

## Step 14: Configuring a Logon Script for Domain Users
In Active Directory Users and Computers, multiple test user accounts were selected from the Nonadmins Organizational Unit (OU).
The Properties window was opened for the selected users. Under the Profile tab, tickets.vbs was entered in the Logon script field. This allows the script to run automatically when the assigned domain users sign in, creating a shortcut to the company's IT support website on their desktop. 
<img width="1445" height="698" alt="image" src="https://github.com/user-attachments/assets/e76065a6-9bf2-456e-890b-a18f84fb7e11" />
<img width="1457" height="649" alt="image" src="https://github.com/user-attachments/assets/1615e2f0-5256-43fa-8263-1e1cb7e80712" />


## Step 15: Testing the Logon Script on PC11
PC11 was signed in using Ronnie's domain account. Ronnie is a test user created to represent a regular employee.
After signing in, the tickets.vbs logon script automatically created the Tickets shortcut on the desktop.
This confirms that the logon script works and can automatically provide employees with the company's IT support website shortcut when they sign in.
<img width="1487" height="771" alt="image" src="https://github.com/user-attachments/assets/54595af0-554e-41d6-aebe-bb84a23f0e66" />



## Step 16: Configuring Folder Redirection Using Group Policy

In Group Policy Management, a new Group Policy Object (GPO) named 515support Folder Redirection Policy was created and linked to the Nonadmins Organizational Unit (OU).
Under User Configuration → Policies → Windows Settings → Folder Redirection, the Documents folder was configured to redirect to the shared network location \\MS10\ROAMING.
Folder Redirection allows employees' Documents folders to be stored on a central server instead of only on their local computers. This makes files easier to access when employees use different company computers.

<img width="1524" height="672" alt="image" src="https://github.com/user-attachments/assets/6bdb8f2b-404e-4133-83ae-ea98e509edd7" />
<img width="1592" height="656" alt="image" src="https://github.com/user-attachments/assets/62f20a92-0c44-4af2-9204-57001ddde276" />




Step 18: Checking user settings 
The lab returned to user settings to connect the account setup with the sign-in task.
Why this matters: User settings tell Windows what should happen when someone logs in.
![Step 18: Checking user settings](screenshots/21_33-30_account-properties.jpg)

Step 19: Editing the sign-in script 
The sign-in script was edited and checked against the lab directions.
Why this matters: A small typing mistake in a script can keep it from working.
![Step 19: Editing the sign-in script](screenshots/22_36-00_login-script-editing.jpg)

Step 20: Saving the script 
The script was saved so it could be used later in the lab.
Why this matters: Saving the file makes the script available for the next steps.
![Step 20: Saving the script](screenshots/23_37-30_save-script.jpg)

Step 21: Opening Group Policy tools 
The lab moved to Group Policy on the Windows server.
Why this matters: Group Policy lets IT set rules for many computers or users at once.
![Step 21: Opening Group Policy tools](screenshots/24_41-30_server-manager-gpo.jpg)

Step 22: Working with Group Policy 
The Group Policy editor was used to set up the policy in the lab.
Why this matters: Instead of changing every PC by hand, IT can manage shared settings in one place.
![Step 22: Working with Group Policy](screenshots/25_43-30_group-policy-editor.jpg)

Step 23: Checking the policy settings 
The policy settings were reviewed as part of the setup.
Why this matters: A policy must be set up correctly before it can affect a user or computer.
![Step 23: Checking the policy settings](screenshots/26_46-30_gpo-policy-settings.jpg)

Step 24: Working with shared folders 
The lab worked with shared folder settings. The lab used `C:\LABFILES` and the network location `\\MS10\ROAMING` in its folder tasks.
Why this matters: A shared folder lets approved people use files stored on another computer.
![Step 24: Working with shared folders](screenshots/27_50-30_shared-folder-properties.jpg)

## Step 25: Setting folder permissions 
Windows folder security settings were opened to manage who could use the folder.
Why this matters: Permissions decide who can open, change, or delete files.
![Step 25: Setting folder permissions](screenshots/28_52-30_ntfs-permissions.jpg)

## Step 26: Reviewing advanced permissions 
The advanced security settings were reviewed for the folder.
Why this matters: Checking permissions helps prevent the wrong people from accessing files.
![Step 26: Reviewing advanced permissions](screenshots/29_55-00_advanced-security.jpg)

## Step 27: Testing the final setup 
Near the end, the lab tested the user setup on `PC11`. The lab included refreshing Group Policy with `gpupdate`, signing in as Ronnie, and checking the `\\MS10\ROAMING` folder for the folder-related task.
Why this matters: A final test matters because it shows whether the setup works for the actual user.
![Step 27: Testing the final setup](screenshots/30_58-00_ronnie-sign-in-policy.jpg)

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


