# Manage a Support Ticket

**CompTIA CertMaster Guided Lab | Windows 10 | Ubuntu Linux | SSH | PowerShell**

## Live recorded unlisted video of me doing the guided lab:
https://www.youtube.com/watch?v=Vj9ehKp7rPA&list=PLhUaWIVkfPbpP9TSJuC9po715y6H1ul6G&index=45


# Use Remote Access Technologies

## 1. Enable Secure Shell (SSH)

### Step 1: Signing In to Windows and Testing the SSH Connection

I signed in to the Windows 10 virtual machine using the **Morgan** account and opened **Windows PowerShell**.
<details> \<summary>View Image\</summary>

<img width="1538" height="666" alt="image" src="https://github.com/user-attachments/assets/30f5bb11-9de9-4d64-9f3b-2490799f8cb2" />
</details>

I attempted to connect to the Ubuntu Linux computer named `tuxbox` by entering:

`ssh tux@tuxbox`

PowerShell displayed the error:

`ssh: connect to host tuxbox port 22: Connection refused`

This meant that Windows could reach the Linux computer, but the SSH service was not accepting connections on port 22. I needed to enable SSH on the Linux computer before I could connect remotely.

<details> \<summary>View Image\</summary>

<img width="1589" height="686" alt="image" src="https://github.com/user-attachments/assets/2e08428f-22e7-4952-807c-829ddd542895" />
</details>

### Step 2: Signing In to Ubuntu and Updating the Software List

I switched to the **Ubuntu Linux** virtual machine and signed in using the `tux` account.

After opening the Terminal, I entered:

`sudo apt update`

This command refreshed Ubuntu's list of available software packages. The system downloaded package information from Ubuntu's software repositories.

Updating the package list helped make sure Ubuntu could find the available software needed to install the SSH server.

<details> \<summary>View Images\</summary>

<img width="1508" height="656" alt="image" src="https://github.com/user-attachments/assets/1b7198e7-d978-4e39-b671-b198a8ae36fb" />

<img width="1419" height="584" alt="image" src="https://github.com/user-attachments/assets/7d8fdd12-4a92-49a7-ab49-c00b8096e0e7" />


</details>

### Step 3: Installing the SSH Server

After the software package list finished updating, I entered:

`sudo apt install ssh -y`

This command was used to install the SSH server on Ubuntu. The `-y` option automatically accepted the installation confirmation.

The SSH server allows another computer to connect to Ubuntu remotely through an encrypted connection.

<details> <summary>View Image\</summary>

<img width="1419" height="584" alt="image" src="https://github.com/user-attachments/assets/e55b2c64-5b5b-43de-af34-6605b5b4d857" />
</details>

### Step 4: Connecting to Ubuntu Remotely Using PowerShell

I returned to the Windows 10 virtual machine and tried the SSH connection again:

`ssh tux@tuxbox`

This time, PowerShell displayed a message asking whether I wanted to trust the Linux computer's SSH host key.

I entered `yes` to accept the connection and then entered the password for the `tux` account.

The connection succeeded, and PowerShell displayed the Ubuntu welcome message and the Linux command prompt:

`tux@tuxbox:~$`

This confirmed that I could remotely access the Ubuntu computer from Windows using SSH.

<details> <summary>View Image\</summary>

<img width="1520" height="610" alt="image" src="https://github.com/user-attachments/assets/0a2d364d-94f8-4d12-b163-0f95a3dec4f9" />

</details>

### Step 5: Running Linux Commands Through SSH

After connecting to Ubuntu, I tested the remote connection by running several Linux commands.

| Command    | What it does                                                     |
| ---------- | ---------------------------------------------------------------- |
| `whoami`   | Displays the username currently signed in                        |
| `uname -a` | Displays information about the Linux operating system and kernel |
| `ls -l`    | Lists files and folders with detailed information                |

The `whoami` command returned `tux`, confirming that I was signed in to the correct Linux account.

The `uname -a` command displayed information about the Ubuntu system, and `ls -l` displayed folders in the user's home directory.

These results confirmed that I could run Linux commands remotely from Windows PowerShell.

<details> <summary>View Image\</summary>


<img width="1547" height="656" alt="image" src="https://github.com/user-attachments/assets/d0f47716-0841-4929-ad5c-231c0dc22926" />


</details>

### Step 6: Disconnecting From the Linux Computer

After finishing the remote commands, I entered:

`exit`

The terminal displayed:

`logout`

`Connection to tuxbox closed.`

PowerShell then returned to the Windows prompt:

`PS C:\Users\Morgan>`

This confirmed that I had successfully ended the SSH session and returned to my Windows computer.

<details> \<summary>View Image\</summary>
  <img width="808" height="250" alt="image" src="https://github.com/user-attachments/assets/4cf64e46-57ea-4607-9713-4465f9a1d97c" />

</details>
SSH allows IT support technicians and system administrators to securely access and manage computers without physically being in front of them.

### Step 7: Finding the Windows Computer's IP Address

I returned to the Windows 10 virtual machine and opened **Windows PowerShell**.

I entered the following command:

`ipconfig`

This command displayed the computer's network information, including its IPv4 address, subnet mask, and default gateway.

The Windows computer had the following network information:

| Network Setting | Value           |
| --------------- | --------------- |
| IPv4 Address    | `192.168.1.101` |
| Subnet Mask     | `255.255.255.0` |
| Default Gateway | `192.168.1.1`   |

I recorded the IPv4 address `192.168.1.101` because I needed it to attempt a remote desktop connection from Ubuntu.

<details> \<summary>View Image\</summary>

<img width="1443" height="343" alt="image" src="https://github.com/user-attachments/assets/c40ac3cd-ce25-4d8b-b031-bd5cc9cff3cb" />

</details>

### Step 8: Finding and Opening Remmina on Ubuntu

I switched to the **Ubuntu Linux** virtual machine and opened **Show Applications** from the dock.

In the search bar, I typed `remote` to find a remote desktop application.

Ubuntu displayed **Remmina**, which is a program that allows users to connect to other computers remotely.

I selected Remmina to open the application.

<details>
<summary>View Images\</summary>

<img width="1482" height="724" alt="image" src="https://github.com/user-attachments/assets/5beb05a7-9c6d-469e-9186-32aea937bb5e" />

<img width="1417" height="701" alt="image" src="https://github.com/user-attachments/assets/acc829f9-b8ac-44b1-9010-8261a33d7aeb" />

</details>

### Step 9: Attempting to Connect to Windows Using RDP

After opening Remmina, I selected **RDP (Remote Desktop Protocol)** as the connection type.

I entered the Windows computer's IPv4 address:

`192.168.1.101`

I pressed **Enter** to start the remote desktop connection.

RDP is a technology that allows someone to view and control another computer's desktop over a network.

In this case, I was attempting to access the Windows 10 computer from Ubuntu.

<details> \<summary>View Image\</summary>

<img width="1487" height="654" alt="image" src="https://github.com/user-attachments/assets/cf015b93-e059-4c57-bc25-5ad8c1e79ffa" />

</details>

### Step 10: Checking the Remote Desktop Connection Result

After attempting the connection, Remmina displayed the following message:

`Lost connection to the RDP server "192.168.1.101".`

This showed that the remote desktop connection was unsuccessful.

The message did not identify the exact cause of the failure. Possible reasons include Remote Desktop not being enabled on Windows, a firewall blocking the connection, or the Windows computer not accepting RDP connections.

I clicked **Close** to dismiss the error message and left the Ubuntu applications open as instructed.

<details>
<summary>View Image\</summary>

<img width="1382" height="654" alt="image" src="https://github.com/user-attachments/assets/debc6705-9145-409b-9ab3-a01f49b0fffa" />

</details>

Remote Desktop Protocol (RDP) allows IT support technicians to access and troubleshoot another computer without being physically present.


### Step 11: Opening Remote Desktop Settings

I switched back to the Windows 10 computer and searched for **Remote Desktop Settings** using the Windows search bar. I opened the settings page to configure the computer for remote access.

Remote Desktop allows someone to access and control a Windows computer from another computer over a network.

<details>
<summary>View Image</summary>

<img width="3188" height="1188" alt="image" src="https://github.com/user-attachments/assets/76938eee-c1ba-4b5f-9291-7664da7cf826" />

</details>

### Step 12: Enabling Remote Desktop

Inside Remote Desktop Settings, I turned on the **Enable Remote Desktop** switch. Windows displayed a confirmation message asking whether I wanted to allow remote connections.

I selected **Confirm** to enable the feature. The switch turned blue and displayed **On**, confirming that Remote Desktop was enabled.

This was important because the earlier connection attempt from Ubuntu failed while Remote Desktop was disabled.

<details>
<summary>View Image</summary>

<img width="1293" height="666" alt="image" src="https://github.com/user-attachments/assets/fe9af99f-1f79-44f8-a109-10faa7f90401" />

</details>

### Step 13: Verifying Remote Desktop Was Enabled

I selected the **Score** button in the CompTIA CertMaster lab to check whether Remote Desktop was configured correctly.

The lab displayed a green **Task complete** message, confirming that Remote Desktop was enabled successfully.

<details>
<summary>View Image</summary>

<img width="1254" height="549" alt="image" src="https://github.com/user-attachments/assets/d8d03d37-f8c7-4532-922b-36ebd492bf75" />

</details>

### Step 14: Reconnecting from Ubuntu Using Remmina

I switched back to the Ubuntu computer and opened **Remmina**, the remote desktop application.

The Windows computer's IP address, `192.168.1.101`, was already entered in the RDP connection box.

I pressed **Enter** to attempt the connection again. This time, Remmina reached the Windows computer and displayed a certificate confirmation screen.

<details>
<summary>View Image</summary>

<img width="1450" height="624" alt="image" src="https://github.com/user-attachments/assets/ab3fcf04-ec41-4f81-a13d-164e27d930e2" />

</details>

### Step 15: Accepting the Remote Desktop Certificate

Remmina displayed a message asking whether I wanted to accept the Windows computer's certificate.

The certificate included information about the computer and its security fingerprint.

I selected **Yes** to continue connecting to the Windows computer.

This certificate helps identify the remote computer and supports a secure connection.

<details>
<summary>View Image</summary>

<img width="1429" height="586" alt="image" src="https://github.com/user-attachments/assets/52c0cc93-e75f-400c-ae08-7bbfcade22fb" />

</details>

### Step 16: Entering the Windows Login Credentials

After accepting the certificate, Remmina displayed the Remote Desktop login screen.

I entered the following information:

- **Username:** Morgan
- **Password:** The Windows account password provided by the lab
- **Domain:** Left blank

I selected **OK** to sign in to the Windows computer remotely.

This step was important because Remote Desktop requires an authorized Windows account before allowing access.

<details>
<summary>View Image</summary>

<img width="1377" height="511" alt="image" src="https://github.com/user-attachments/assets/89a565a2-08c1-4877-acb9-95a6c0d188bf" />

</details>

### Step 17: Successfully Accessing the Windows Desktop

After entering the correct credentials, the Windows 10 desktop appeared inside the Remmina application on Ubuntu.

I was able to view the Windows Remote Desktop Settings page from the Ubuntu computer.

This confirmed that the Remote Desktop connection was working and that I could access the Windows computer remotely.

<details>
<summary>View Image</summary>

<img width="1541" height="691" alt="image" src="https://github.com/user-attachments/assets/4d35236f-96db-4b68-ba45-237058bde80c" />

</details>


