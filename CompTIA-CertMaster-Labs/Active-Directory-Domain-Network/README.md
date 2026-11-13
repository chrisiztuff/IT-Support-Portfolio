# Active Directory Domain Networking Lab
CompTIA Certmaster guided lab | Windows Server | Windows 11 | Active Directory
## Live recorded unlisted video of me doing the guided lab:
https://www.youtube.com/watch?v=kL88qlCQv7U
## What This Project Is About
In this guided lab, I practiced connecting a Windows computer to a company domain, checking network problems, creating a new user, working with a sign-in script, setting Group Policy, and checking folder permissions.
A domain is a way for a company to manage work computers and employee accounts together. The screenshots below come from my recorded training lab. 

## Step 1: Starting the lab 
The lab began on the Windows computers used for this exercise. The administrator account was used for tasks that need extra permission. An administrator is an account that can change important computer settings.
<img width="1300" height="708" alt="image" src="https://github.com/user-attachments/assets/0bfeca1a-7360-4c76-8bb2-92da52f06d0d" />


## Step 2: Checking PC11
On PC11, the computer name and domain settings were opened. The computer was named `PC11`. Every computer has a name so it can be found on a network.
<img width="1279" height="738" alt="image" src="https://github.com/user-attachments/assets/7b7a6ba6-e5d9-49a9-90dc-141fbce94b26" />

## Step 3: Entering the domain administrator account 
PC11 was set to join `corp.515support.com`. Windows asked for an account allowed to join the domain. The account `515support\administrator` was entered, along with the lab password.
This check stops just anyone from adding computers to the company network.
<img width="908" alt="Domain Controller Setup" src="https://github.com/user-attachments/assets/be632264-46a4-4545-874d-a2685870a751" />
## Step 4: Confirming PC11 joined the domain 
Windows showed “Welcome to the corp.515support.com domain.” This confirmed that PC11 joined the domain successfully. A domain lets a company manage many work computers and accounts together.
<img width="913" height="525" alt="image" src="https://github.com/user-attachments/assets/1cdb491f-90e1-4d1f-b84b-59c3a192fce3" />

## Step 5: Signing in after joining 
After PC11 joined the domain, a domain account was used to sign in. Jaime is a test user created to represent a regular employee in the company. This demonstrates that employees can sign in to company computers using their domain accounts instead of needing separate accounts for every computer.
<img width="1280" height="712" alt="05_04-30_domain-user-sign-in" src="https://github.com/user-attachments/assets/13727907-2f87-47bd-9f8e-51650212bf89" />

## Step 6: Opening the network checks 
The lab moved to checking network connections. PowerShell was used to run network commands.
Why this matters: PowerShell is a place to type commands that check or change computer settings.
![Step 6: Opening the network checks](screenshots/06_06-30_powershell-connectivity.jpg)

## Step 7: Reading connection results 
The results of a network check were reviewed to see whether the computer could reach the right network services.
Why this matters: A computer must be able to reach the domain server for many domain features to work.
![Step 7: Reading connection results](screenshots/07_07-30_network-test-results.jpg)


## Step 8: Testing Network Connectivity

PowerShell was used to ping PC10 and MS10.
Both devices responded successfully with 0% packet loss. This confirms that PC11 can communicate with other computers and servers on the network.
<img width="1062" height="687" alt="image" src="https://github.com/user-attachments/assets/c620d103-c721-47e5-b633-e0e765d79a7f" />


## Step 9 : Opening Active Directory 
On the server side of the lab, Active Directory Users and Computers was opened. This is where domain accounts are managed.
This tool lets IT staff manage accounts from one place.
<img width="1280" height="712" alt="14_24-30_ad-users-computers" src="https://github.com/user-attachments/assets/2b558254-59a5-4697-9367-8a63259ec984" />

##Step 13: Creating Ronnie 
A new user named Ronnie was created for the `corp.515support.com` domain. The user sign-in name was `ronnie`.
A user account gives a person their own work sign-in.
<img width="1498" height="663" alt="image" src="https://github.com/user-attachments/assets/139040da-c20d-4c40-a24e-ff6f5b0a1af4" /> 
The Ronnie account was created in the `Nonadmins` organizational unit (OU).
An OU is like a folder that helps keep company accounts organized.
<img width="1280" height="712" alt="16_27-30_nonadmins-ou" src="https://github.com/user-attachments/assets/e6c02253-1fed-4ef2-a63e-67ba39ad274a" />

Step 15: Setting Ronnie’s account options 
The account options were set to match the training lab. The lab called for Password never expires and for Ronnie not to change the password at the next sign-in.
Why this matters: These are lab settings, not general advice for real company passwords.
![Step 15: Setting Ronnie’s account options](screenshots/17_28-30_account-properties.jpg)

Step 16: Starting the sign-in script task 
The next part of the lab worked with settings and files used when a user signs in.
Why this matters: A sign-in script is a small set of commands that can run automatically at sign-in.
![Step 16: Starting the sign-in script task](screenshots/18_29-00_login-script-configuration.jpg)

Step 17: Working on the script 
A script was opened in a text editor and worked on as part of the sign-in setup.
Why this matters: A script can save time by doing the same task for many users.
![Step 17: Working on the script](screenshots/19_30-30_script-in-editor.jpg)

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


