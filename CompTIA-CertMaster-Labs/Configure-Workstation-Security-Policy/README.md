# Configure Workstation Security Policy


## Live recorded unlisted video of me doing the guided lab:
https://www.youtube.com/watch?v=uE_L0u2_OPE&list=PLhUaWIVkfPbpP9TSJuC9po715y6H1ul6G&index=43

## Project Description

In this guided lab, I practiced configuring security policies on a Windows workstation using Local Security Policy. I changed password requirements, configured account lockout settings, and improved login security to help protect employee accounts from unauthorized access.

I also tested different passwords to make sure the security policies were working correctly. The screenshots below come from my recorded training lab and show the steps I completed.

### Step 1: Signing In to the Windows Workstation

I started by opening the Windows workstation and signing in to the account named **Morgan**. This allowed me to access the computer and begin changing its security settings.

The goal of this lab was to configure password rules that would help protect employee accounts from unauthorized access.

<details>
<summary>View Image</summary>

<img width="1536" height="673" alt="image" src="https://github.com/user-attachments/assets/dedcb5d1-dade-464e-adaa-f26c9c355ba5" />

</details>

### Step 2: Opening Local Security Policy

After signing in, I used the Windows search bar to search for **Local Security Policy**.

I opened this application because it allows administrators to manage security settings on a Windows computer, including password requirements and account lockout rules.

<details>
<summary>View Image</summary>

<img width="1491" height="731" alt="image" src="https://github.com/user-attachments/assets/e03b66dc-d2e2-462b-8772-5f52f3d9d57d" />

</details>

### Step 3: Reviewing the Password Policy Settings

Inside Local Security Policy, I expanded **Account Policies** and selected **Password Policy**.

I reviewed the existing settings, including:

- Enforce password history
- Maximum password age
- Minimum password age
- Minimum password length
- Password complexity requirements

I noticed that password history was set to remember **0 passwords**, maximum password age was **42 days**, minimum password age was **0 days**, and minimum password length was **0 characters**.

These settings needed to be changed to match the company's security requirements.

<details>
<summary>View Image</summary>

<img width="1188" height="588" alt="image" src="https://github.com/user-attachments/assets/593dd6fa-1826-4f38-b147-7d953f544cc6" />

</details>

### Step 4: Configuring Password History

I opened **Enforce password history** and changed the setting from **0 to 10 passwords remembered**.

This setting prevents employees from immediately reusing their previous ten passwords.

It helps improve account security by encouraging users to create different passwords instead of repeatedly using the same ones.

<details>
<summary>View Image</summary>

<img width="1249" height="637" alt="image" src="https://github.com/user-attachments/assets/b120c6f9-5d03-4c04-8cfa-1d142e24d7fb" />

</details>

### Step 5: Changing the Maximum Password Age

Next, I opened **Maximum password age** and changed the setting from **42 days to 30 days**.

This setting controls how long employees can use a password before Windows requires them to change it.

The company's policy required passwords to expire after 30 days.

<details>
<summary>View Image</summary>

<img width="1314" height="698" alt="image" src="https://github.com/user-attachments/assets/23fc6f8e-60c2-4851-888b-1cd92e29a62e" />

</details>

### Step 6: Configuring the Minimum Password Age

I opened **Minimum password age** and changed the setting from **0 days to 7 days**.

This setting prevents employees from changing their passwords repeatedly within a short period.

It also helps prevent users from quickly cycling through ten passwords just to reuse an old one.

<details>
<summary>View Image</summary>

<img width="1249" height="600" alt="image" src="https://github.com/user-attachments/assets/82a833db-f9e3-4809-a6ff-294830f1dcae" />

</details>

### Step 7: Setting the Account Lockout Threshold

I selected **Account Lockout Policy** and opened **Account lockout threshold**.

I changed the setting from **0 to 5 invalid login attempts**.

This means that Windows will lock the account after five unsuccessful sign-in attempts.

This helps protect employee accounts against repeated password-guessing attempts.

<details>
<summary>View Image</summary>

<img width="1456" height="507" alt="image" src="https://github.com/user-attachments/assets/70cb6c94-2b91-4a28-8079-057da529bb7d" />

</details>

### Step 8: Configuring the Account Lockout Duration

After setting the account lockout threshold, Windows displayed a **Suggested Value Changes** window.

The window recommended:

- Account lockout duration: **30 minutes**
- Reset account lockout counter after: **30 minutes**

I accepted these recommended settings by selecting **OK**.

These settings help prevent repeated login attempts while allowing the account to become available again after the lockout period.

<details>
<summary>View Image</summary>

<img width="553" height="269" alt="image" src="https://github.com/user-attachments/assets/1b42b380-ec6b-4a24-8a70-c1c563192db5" />

</details>

### Step 9: Setting the Minimum Password Length

I returned to **Password Policy** and opened **Minimum password length**.

I entered **10 characters** to match the company's password requirements.

This setting requires employees to create passwords containing at least ten characters.

Longer passwords generally make it more difficult for attackers to guess passwords.

<details>
<img width="871" height="582" alt="image" src="https://github.com/user-attachments/assets/b1336b31-a88f-40d3-8842-554c07f43d9b" />

</details>


### Step 10: Opening Security Options

I opened **Local Security Policy**, expanded **Local Policies**, and selected **Security Options**.

This section contains settings that control how users sign in to Windows and how the computer protects user accounts.

I needed to change a setting so Windows would stop automatically displaying the username of the last person who signed in.

<details>
<summary>View Image</summary>

<img width="1443" height="628" alt="image" src="https://github.com/user-attachments/assets/d3aa0eae-39fd-4995-ac95-67cf0eeb1049" />

</details>

### Step 11: Finding the Last Signed-In User Policy

I scrolled through the list of security settings until I found **Interactive logon: Don't display last signed-in**.

The setting was originally **Disabled**, which meant Windows could display the previous user's account name on the sign-in screen.

I selected this policy to change how usernames appeared when someone signed in.

<details>
<summary>View Image</summary>

<img width="1111" height="481" alt="image" src="https://github.com/user-attachments/assets/4a54d234-1b80-4797-9477-84163da47377" />

</details>

### Step 12: Opening the Policy Properties

I right-clicked **Interactive logon: Don't display last signed-in** and selected **Properties**.

This opened the settings window where I could enable or disable the policy.

<details>
<summary>View Image</summary>

<img width="1312" height="607" alt="image" src="https://github.com/user-attachments/assets/bd580720-618b-48bd-ac58-475edcdda741" />

</details>

### Step 13: Enabling the Security Policy

Inside the policy settings, I selected **Enabled** and saved the change.

This setting prevents Windows from automatically showing the username of the previous person who signed in.

It helps protect user privacy by making it harder for someone looking at the login screen to identify the last user.

<details>
<summary>View Image</summary>

<img width="747" height="367" alt="image" src="https://github.com/user-attachments/assets/3cea0c04-8038-48b3-9a3e-65fe6bd57aa7" />

</details>

### Step 14: Validating the Policy and Signing Out

After enabling the setting, I clicked the **Score** button to check whether the policy was configured correctly.

The lab displayed **Policy change confirmed — Task complete**, showing that the security setting passed validation.

I then pressed **Ctrl + Alt + Delete** and selected **Sign out** to test the new login behavior.

<details>
<summary>View Image</summary>

<img width="1345" height="593" alt="image" src="https://github.com/user-attachments/assets/cb2d752a-f637-4517-ad4b-e20fc07f7824" />

</details>

### Step 15: Returning to the Windows Login Screen

After signing out, I returned to the Windows lock screen.

I pressed **Ctrl + Alt + Delete** to open the sign-in screen and check whether the previous username would still appear automatically.

<details>
<summary>View Image</summary>

<img width="1484" height="465" alt="image" src="https://github.com/user-attachments/assets/dcd80c9d-3451-419c-b734-65c5bad47ca3" />

</details>

### Step 16: Verifying the New Login Security Setting

The Windows sign-in screen displayed **Other user** instead of automatically showing the previous user's account.

I entered the username **Morgan** and the lab password to sign back in.

This confirmed that the new security policy was working as expected.

The computer now required users to enter their usernames instead of automatically displaying the last signed-in account.

<details>
<summary>View Image</summary>

<img width="1393" height="628" alt="image" src="https://github.com/user-attachments/assets/6bdca4d3-d344-433e-8531-59fd8837fb40" />

</details>


## 3. Testing the Password Security Policy

### Step 17: Testing a Weak Password

I opened the **Change a password** screen for the Windows user **Morgan** by pressing **Ctrl + Alt + Delete** and selecting **Change a password**.

I entered the existing password and attempted to change it to `12345678`.

This password did not meet the company's security requirements because it was too short and did not contain uppercase letters or special characters.

The purpose of this test was to check whether Windows would prevent users from creating weak passwords.

<details>
<summary>View Image</summary>

<img width="1261" height="658" alt="image" src="https://github.com/user-attachments/assets/7a64467a-9d9c-40ef-882f-a241b3990948" />

</details>

### Step 18: Confirming That Windows Rejected the Weak Password

After submitting the weak password, Windows displayed an error message:

**"Unable to update the password. The value provided for the new password does not meet the length, complexity, or history requirements of the domain."**

This confirmed that Windows rejected the password because it did not meet the security requirements.

I clicked **OK** to close the message.

 Password requirements help prevent employees from using simple passwords that attackers could easily guess.

<details>
<summary>View Image</summary>

<img width="950" height="591" alt="image" src="https://github.com/user-attachments/assets/886ea969-d3ab-464d-9e9d-4a062753ef6b" />

</details>

### Step 19: Testing a Password Without Uppercase Letters or Numbers

Next, I tested another password to check whether Windows was enforcing password complexity requirements.

I entered the existing password and attempted to use **`duration-unstamped`** as the new password.

Although this password was longer than 10 characters, it did not contain uppercase letters or numbers.

This test helped me understand that password length alone does not guarantee that a password meets company security requirements.

<details>
<summary>View Image</summary>

<img width="1414" height="546" alt="image" src="https://github.com/user-attachments/assets/aab30c75-99e5-47d5-bdd9-141fcc88ad9a" />

</details>

### Step 20: Confirming That the Second Password Was Rejected

After submitting `duration-unstamped`, Windows displayed another error message explaining that the password did not meet the required length, complexity, or history settings.

This showed that Windows was enforcing additional password requirements beyond password length.

I clicked **OK** to close the error message.

Password complexity rules can help reduce the risk of employees choosing easily guessed passwords.

<details>
<summary>View Image</summary>

<img width="1415" height="652" alt="image" src="https://github.com/user-attachments/assets/70b22169-be18-4cac-b27c-1e81c2a4bc9f" />

</details>

### Step 21: Entering a Password That Met the Security Requirements

Next, I attempted to change Morgan's password to **`DURATION-unstamped-11`.**

This password included:

- Uppercase letters
- Lowercase letters
- Numbers
- Special characters
- More than 10 characters

I entered the existing password and typed the new password into the **New password** and **Confirm password** fields.

This test was intended to verify that Windows would accept a password that met the configured security requirements.

<details>
<summary>View Image</summary>

<img width="1489" height="658" alt="image" src="https://github.com/user-attachments/assets/e4db3ad8-bd47-48cb-bd57-988c37ec81d3" />

</details>


The password change was successful:

<details>
<summary>View Image</summary>

<img width="1319" height="689" alt="image" src="https://github.com/user-attachments/assets/c449eab3-c0e9-487c-b5d2-f6c8640e909c" />
</details>

### Step 22: Opening the Password Change Screen Again

After testing the new password, I returned to the Windows security options using **Ctrl + Alt + Delete**.

I selected **Change a password** again to test the password history policy.

The password history policy had previously been configured to remember the last **10 passwords**.

This setting was designed to prevent users from immediately reusing their previous passwords.

<details>
<summary>View Image</summary>

<img width="1508" height="771" alt="image" src="https://github.com/user-attachments/assets/f3f391be-b73d-4387-ae95-13b2cae65aa1" />

</details>

### Step 23: Selecting Change a Password

On the Windows security screen, I selected **Change a password**.

This opened the password change form again.

I used this screen to test whether Windows would allow the same password to be reused.

Reusing passwords can weaken account security, especially when an old password has been exposed.

<details>
<summary>View Image</summary>

<img width="1345" height="665" alt="image" src="https://github.com/user-attachments/assets/5c0bbbd6-19d4-48b4-9269-3d4547481359" />
</details>

### Step 24: Attempting to Reuse the Same Password

I entered `DURATION-unstamped-11` as the existing password and attempted to enter the same value into the new password fields.

The purpose was to test whether Windows would prevent a user from reusing a recently used password.

Because the password history setting remembered the previous 10 passwords, the same password should not have been accepted again.

<details>
<summary>View Image</summary>

<img width="901" height="411" alt="image" src="https://github.com/user-attachments/assets/60c2d073-23a8-4995-b7b6-3bcc25af8ba0" />

</details>

### Step 25: Confirming That Password Reuse Was Blocked

After attempting to reuse the password, Windows displayed an error message:

**"Unable to update the password. The value provided for the new password does not meet the length, complexity, or history requirements of the domain."**

This result was consistent with the password history restriction because the new password matched the existing password.

Password history policies help prevent users from repeatedly choosing the same password.

<details>
<summary>View Image</summary>

<img width="831" height="404" alt="image" src="https://github.com/user-attachments/assets/200569f9-2727-4586-a74f-9a80179a8a0e" />

</details>

### Step 26: Completing the Security Policy Knowledge Check

At the end of the lab, I answered a question asking why it was important to test whether security changes worked as expected.

I selected:

**"It's easy to make a mistake."**

The lab displayed a green **Correct!** message.

This helped me understand that configuring security settings is only part of the process. IT professionals must also test their changes to make sure the settings work correctly.

<details>
<summary>View Image</summary>

<img width="462" height="294" alt="image" src="https://github.com/user-attachments/assets/5577ea0b-0828-4027-890d-cd08989f2cbf" />

</details>


# What I Learned
I learned how to configure Windows security policies, including setting password history to 10 passwords, maximum password age to 30 days, minimum password age to 7 days, and minimum password length to 10 characters. I also configured an account lockout threshold of 5 failed login attempts with a 30-minute lockout duration and enabled the policy to hide the last signed-in username. Finally, I tested weak passwords, password complexity requirements, and password reuse restrictions to verify that the security settings were working correctly.
