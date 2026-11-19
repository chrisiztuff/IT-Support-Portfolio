# Configure Workstation Security Policy


## Live recorded unlisted video of me doing the guided lab:
https://www.youtube.com/watch?v=uE_L0u2_OPE&list=PLhUaWIVkfPbpP9TSJuC9po715y6H1ul6G&index=43



# Configure Workstation Security Policy

## 1. Changing Windows Security Policies

### Step 1: Signing In to the Windows Workstation

I started by opening the Windows workstation and signing in to the account named **Morgan**. This allowed me to access the computer and begin changing its security settings.

The goal of this lab was to configure password rules that would help protect employee accounts from unauthorized access.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

</details>

### Step 2: Opening Local Security Policy

After signing in, I used the Windows search bar to search for **Local Security Policy**.

I opened this application because it allows administrators to manage security settings on a Windows computer, including password requirements and account lockout rules.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

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

<img src="PASTE_IMAGE_URL_HERE" />

</details>

### Step 4: Configuring Password History

I opened **Enforce password history** and changed the setting from **0 to 10 passwords remembered**.

This setting prevents employees from immediately reusing their previous ten passwords.

It helps improve account security by encouraging users to create different passwords instead of repeatedly using the same ones.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

</details>

### Step 5: Changing the Maximum Password Age

Next, I opened **Maximum password age** and changed the setting from **42 days to 30 days**.

This setting controls how long employees can use a password before Windows requires them to change it.

The company's policy required passwords to expire after 30 days.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

</details>

### Step 6: Configuring the Minimum Password Age

I opened **Minimum password age** and changed the setting from **0 days to 7 days**.

This setting prevents employees from changing their passwords repeatedly within a short period.

It also helps prevent users from quickly cycling through ten passwords just to reuse an old one.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

</details>

### Step 7: Setting the Account Lockout Threshold

I selected **Account Lockout Policy** and opened **Account lockout threshold**.

I changed the setting from **0 to 5 invalid login attempts**.

This means that Windows will lock the account after five unsuccessful sign-in attempts.

This helps protect employee accounts against repeated password-guessing attempts.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

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

<img src="PASTE_IMAGE_URL_HERE" />

</details>

### Step 9: Setting the Minimum Password Length

I returned to **Password Policy** and opened **Minimum password length**.

I entered **10 characters** to match the company's password requirements.

This setting requires employees to create passwords containing at least ten characters.

Longer passwords generally make it more difficult for attackers to guess passwords.

<details>
<summary>View Image</summary>

<img src="PASTE_IMAGE_URL_HERE" />

</details>
