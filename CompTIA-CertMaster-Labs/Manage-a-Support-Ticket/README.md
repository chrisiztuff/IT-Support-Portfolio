# Manage a Support Ticket
**CompTIA CertMaster Guided Lab | IT Help Desk | osTicket | Windows**

## Live recorded unlisted video of me doing the guided lab:
https://www.youtube.com/watch?v=USTvKOX6VQg&list=PLhUaWIVkfPbpP9TSJuC9po715y6H1ul6G&index=49
## What This Project Is About
In this guided lab, I practiced using **osTicket**, a help desk ticketing system used to organize and manage IT support requests. A support ticket is a record of a problem reported by an employee, such as a forgotten password, broken printer, or VPN connection issue. The goal of this section was to sign in to the support center, review the open ticket queue, and identify password reset requests.

## Step 1: Accessing the PC10 Virtual Machine

The lab began on the Windows computer named **PC10**.

The lab instructions directed me to sign in using the test account **Jaime**. This account was used to access the Windows desktop and the support center application.

PC10 was the computer used to complete the help desk tasks.

IT support technicians often sign in to company computers or virtual machines to access the tools needed for their work.

<details>
<summary>View Image</summary>

<img width="1113" height="836" alt="image" src="https://github.com/user-attachments/assets/457547a8-0368-4dba-b51c-3a4a7f4c775f" />

</details>

## Step 2: Opening the Support Center Ticketing System

On the PC10 desktop, I located the shortcut named **Support Center Tickets**.

I double-clicked the shortcut to open the company's help desk ticketing application.

The shortcut opened **osTicket**, a system used by IT support staff to manage employee problems and requests.

Help desk technicians use ticketing systems to keep track of reported issues, document their work, and make sure employees receive assistance.

<details>
<summary>View Image</summary>

<img width="1489" height="610" alt="image" src="https://github.com/user-attachments/assets/5916da1e-b2a2-4a3f-b325-25e353da10dd" />

</details>

## Step 3: Signing In to osTicket

After opening the Support Center Tickets application, the osTicket login page appeared.

I entered the username **Jaime** and the password provided in the training lab.

The login page displayed a **Log In** button, which was used to access the ticketing system.


Help desk applications require employees to sign in so that support activities can be associated with authorized accounts.

<details>
<summary>View Image</summary>

<img width="1179" height="642" alt="image" src="https://github.com/user-attachments/assets/587d531a-3ec4-4523-82eb-3265597c172d" />

</details>

## Step 4: Reviewing the Open Ticket Queue

After signing in, I opened the **Tickets** section of osTicket.

The ticket queue displayed several employee support requests, including:

| Ticket Subject | Employee | Priority |
|---|---|---|
| Printer broken | Zuri | Normal |
| VPN access | Sam | Normal |
| Reset password | Jaylan | Normal |
| Password reset | Dani | Normal |
| Can't print | Morgan | Normal |
| Can't access sales share | Angel | Normal |

I reviewed the ticket subjects to identify requests involving password resets.

Two tickets were related to password resets:

1. **Reset password** — submitted by Jaylan.
2. **Password reset** — submitted by Dani.

The correct answer to the lab question was **2 password reset tickets**.


Help desk technicians review incoming tickets to understand which employees need assistance and what problems have been reported.

Reading the ticket subject and priority helps technicians decide which requests should be handled first.

<details>
<summary>View Image</summary>

<img width="1443" height="502" alt="image" src="https://github.com/user-attachments/assets/53fb7225-f0d9-4d2e-8b08-85b7d380c682" />

</details>

## Step 5: Reviewing Password Reset Ticket #608869

In the osTicket ticket queue, I located ticket **#608869**, titled **Reset password**.

I moved the mouse pointer over the ticket number to display a pop-up window containing additional information about the request.

The ticket summary showed the following details:

| Ticket Information | Details |
|---|---|
| Ticket Number | 608869 |
| Subject | Reset password |
| Submitted By | Jaylan |
| Email | jaylan@515support.com |
| Department | Maintenance |
| Status | Open — Overdue |
| Assigned To | Unassigned |
| Help Topic | Report a Problem |

The ticket was marked as **overdue**, meaning its due date had passed without the ticket being completed.

The ticket was also **unassigned**, meaning no support technician had taken responsibility for it yet.

At the bottom of the pop-up window, I selected **Assign** to open the ticket details.


Help desk technicians review ticket details to understand the employee's problem, check its urgency, and determine whether someone is already working on it.

<details>
<summary>View Image</summary>

<img width="1440" height="572" alt="image" src="https://github.com/user-attachments/assets/073ae0a9-a3ca-428d-9f4e-0b5ceb93d525" />

</details>

## Step 6: Claiming Ownership of Ticket #608869

After opening ticket **#608869**, I located the person-shaped assignment icon near the top of the ticket details page.

I clicked the small downward arrow next to the icon. A menu appeared with three options:

- Claim
- Agent
- Team

I selected **Claim** to take ownership of the ticket.

Claiming a ticket means that the support technician takes responsibility for handling the employee's request.

This helps other IT team members know that someone is already working on the problem.

In a real IT help desk, claiming tickets helps prevent multiple technicians from working on the same issue unnecessarily.

It also makes it easier to track who is responsible for resolving each support request.

<details>
<summary>View Image</summary>

<img width="1508" height="670" alt="image" src="https://github.com/user-attachments/assets/8179d075-0be4-4fbb-aac0-9aacfcec0edf" />

</details>

## Step 7: Confirming Ticket Ownership

After selecting **Claim**, a confirmation window appeared with the message:

**"Are you sure you want to CLAIM this ticket?"**

I clicked **Yes, Claim** to confirm that I wanted to take responsibility for ticket **#608869**.

The lab instructions indicated that the ticket details would update with the activity message **"Jamie Admin claimed this."**

This activity message records which support technician claimed the ticket.

Confirming ticket ownership helps IT departments track technician responsibilities and maintain a record of actions performed on support requests.

<details>
<summary>View Image</summary>

<img width="1471" height="605" alt="image" src="https://github.com/user-attachments/assets/c4bb1785-ad3c-4458-8545-3ddc6bd9c690" />

</details>

## Step 8: Identifying the Employee Who Submitted the Ticket

After claiming the ticket, I reviewed the ticket details to identify the employee who submitted the request.

Under the **User** section, the following information appeared:

| Field | Information |
|---|---|
| User | Jaylan |
| Email | jaylan@515support.com |
| Source | Web |
| Help Topic | Report a Problem |
| Last Message | March 8, 2022, 11:00 AM |

The ticket was created by **Jaylan**.

The **Source: Web** field indicated that the request was submitted through the web-based ticketing system.

I selected **Jaylan** as the answer to the lab question.

Before helping an employee, an IT support technician needs to identify who reported the issue.

Reviewing the user's information helps the technician understand who needs assistance and locate the correct support request.

<details>
<summary>View Image</summary>

<img width="1107" height="511" alt="image" src="https://github.com/user-attachments/assets/6677f3a9-5d4a-4966-9d7c-dac14c9a454c" />

</details>


## Step 9: Resetting Jaylan's Password in Active Directory

After reviewing Jaylan's password reset ticket **#608869**, I minimized the Microsoft Edge browser and opened the **Active Directory Administrative Center**.

Active Directory is used by companies to manage employee accounts, passwords, and access to company computers.

Inside the Active Directory Administrative Center, I located the **Reset Password** section.

I entered the following information:

| Field                                    | Information                |
| ---------------------------------------- | -------------------------- |
| User name                                | `515support\jaylan`        |
| Password                                 | Lab-provided password      |
| Confirm password                         | Same lab-provided password |
| User must change password at next log on | Unchecked                  |

After entering the information, I clicked **Apply** to reset Jaylan's password.

The option **User must change password at next log on** was left unchecked because the training lab specifically required this setting.

Help desk technicians frequently assist employees who forget their passwords or cannot access their accounts.

Active Directory allows authorized IT staff to reset an employee's password without needing access to the employee's computer.

<details>
<summary>View Image\</summary>

<img width="1461" height="481" alt="image" src="https://github.com/user-attachments/assets/156e4f03-0497-42a6-8a15-84e8c4bd05d8" />

</details>




## Step 10: Verifying Jaylan's Password Reset

After clicking **Apply**, the Active Directory Administrative Center displayed the following confirmation:

**"Password for 515support\jaylan has been reset successfully."**

This confirmed that Jaylan's account password had been updated.

After verifying the successful password reset, I returned to the osTicket application using Microsoft Edge.

IT technicians should always verify that a requested change was completed successfully before updating a support ticket.

A confirmation message provides evidence that the password reset operation succeeded.

<details>
<summary>View Image\</summary>
<img width="1636" height="736" alt="image" src="https://github.com/user-attachments/assets/d1288348-3571-4162-b434-c3d113cd559f" />

</details>

## Step 11: Updating Jaylan's Support Ticket

After resetting Jaylan's password, I returned to ticket **#608869** in osTicket.

I entered the following message into the response box:

**"Account has been reset, please call the help desk at x333 to obtain the updated password"**

This message informed Jaylan that the account password had been reset and explained how to obtain the updated password.

Instead of including the password directly in the ticket, the message instructed Jaylan to contact the help desk.

I left the ticket status as **Open (current)** because the employee had not yet confirmed that the new password worked.

I then clicked the orange **Post Reply** button to submit the response.

The ticket details displayed a new last-response timestamp, confirming that the reply was recorded.

Help desk technicians need to document the actions they perform and communicate the next steps to employees.

Keeping the ticket open allows the technician to follow up if the employee continues experiencing login problems.

<details>
<summary>View Image\</summary>

<img width="1617" height="652" alt="image" src="https://github.com/user-attachments/assets/5b35fd03-e448-4cc1-ab7e-c46209837268" />

</details>

## Step 12: Reviewing Dani's Password Reset Ticket #920821

After updating Jaylan's ticket, I returned to the **Open** ticket queue in osTicket.

<details>
<summary>View Image\</summary>
<img width="1478" height="567" alt="image" src="https://github.com/user-attachments/assets/bb79abbd-c027-44de-a46b-a75ed741f4e2" />

</details>

I located ticket **#920821**, titled **Password reset**, and moved the mouse pointer over the ticket number.

A pop-up window appeared showing the following information:

| Ticket Information | Details                                            |
| ------------------ | -------------------------------------------------- |
| Ticket Number      | 920821                                             |
| Subject            | Password reset                                     |
| Submitted By       | Dani                                               |
| Email              | [dani@515support.com](mailto\:dani@515support.com) |
| Department         | Maintenance                                        |
| Priority           | Normal                                             |
| Ticket State       | Open — Overdue                                     |
| Assigned To        | Unassigned                                         |

The ticket was marked as overdue and had not yet been assigned to a technician.

I selected **Assign** to open the ticket details.

<details>
<summary>View Image\</summary>

<img width="1454" height="598" alt="image" src="https://github.com/user-attachments/assets/f8599891-7cde-4f4b-ab02-b97f6304121e" />
<details>

### What Dani Wrote in Her Ticket

After opening the ticket, I reviewed the message Dani submitted:

**"I remember changing my password on Friday but cannot remember what I set it too."**

<details>
<summary>View Image\</summary>

<img width="957" height="567" alt="image" src="https://github.com/user-attachments/assets/b9903933-b8d9-4816-975c-5f544710160a" />
<details>

This explained that Dani had previously changed her password but could no longer remember the new password.

Because Dani could not remember her password, she needed assistance regaining access to her account.

In Dani's case, the message showed that she had forgotten a recently changed password.


## Step 13: Claiming Dani's Support Ticket

After reviewing Dani's request, I located the person-shaped assignment icon at the top of ticket **#920821**.

I clicked the downward arrow next to the icon and selected **Claim**.

The ticketing system asked for confirmation, and I selected **Yes, Claim**.

A green notification appeared stating:

**"Ticket assigned to you successfully"**

The ticket details showed:

| Field         | Information |
| ------------- | ----------- |
| Ticket Number | 920821      |
| User          | Dani        |
| Assigned To   | Jaime Admin |
| Status        | Open        |
| Priority      | Normal      |

This confirmed that the ticket had been assigned to the support technician account **Jaime Admin**.

I also verified that **Dani** was the employee who submitted the ticket.

Claiming a ticket allows other technicians to see who is responsible for handling the employee's problem.

It also helps prevent duplicate work and keeps support requests organized.

\<details>
\<summary>View Image\</summary>
<img width="1547" height="586" alt="image" src="https://github.com/user-attachments/assets/87c0cfe6-2977-485c-9808-518df272befc" />


\</details>

## Step 14: Resetting Dani's Password in Active Directory

After claiming Dani's ticket, I returned to the **Active Directory Administrative Center**.

Inside the **Reset Password** section, I entered Dani's domain account information.

| Field                                    | Information                |
| ---------------------------------------- | -------------------------- |
| User name                                | `515support\Dani`          |
| Password                                 | Lab-provided password      |
| Confirm password                         | Same lab-provided password |
| User must change password at next log on | Unchecked                  |

I clicked **Apply** to reset Dani's password.

The Active Directory Administrative Center displayed the confirmation:

**"Password for 515support\Dani has been reset successfully."**

This confirmed that Dani's account password had been updated.

This task demonstrated how IT support technicians can help employees regain access to their accounts using Active Directory.

It also reinforced the importance of verifying that the password reset was successful before responding to the employee.

\<details>
\<summary>View Image\</summary>

\<!-- Insert screenshot showing Dani's successful password reset -->

</details>

## Step 15: Responding to Dani's Support Ticket

After successfully resetting Dani's password, I returned to ticket **#920821** in osTicket.

In the response box, I entered the following message:

**"Account has been reset, please call the help desk at x333 to obtain the updated password"**

The message informed Dani that the password reset was completed and instructed her to contact the help desk to obtain the new password.

I left the ticket status as **Open (current)** because Dani had not yet confirmed that she could successfully sign in.

I then clicked the orange **Post Reply** button.

Posting a reply allows the employee to understand what action was taken and what they need to do next.

Leaving the ticket open helps ensure that the support request is not considered resolved before the employee confirms that the problem has been fixed.

\<details> \<summary>View Image\</summary>

\<!-- Insert screenshot showing Dani's response message -->

\<!-- Insert screenshot showing Post Reply button -->

</details>

## What I Learned From Updating Support Tickets

In this section, I practiced resetting employee passwords using Active Directory and updating help desk tickets in osTicket.

I worked with two employee support requests:

| Ticket  | Employee | Problem                          | Action Taken                      |
| ------- | -------- | -------------------------------- | --------------------------------- |
| #608869 | Jaylan   | Password reset request           | Reset password and posted a reply |
| #920821 | Dani     | Forgot recently changed password | Reset password and posted a reply |

These tasks helped me understand how IT support technicians use Active Directory and ticketing systems together to resolve employee account problems.

I also learned the importance of documenting completed work, communicating with employees, and keeping tickets open until the employee confirms that the issue has been resolved.



