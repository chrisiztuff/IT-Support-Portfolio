# Manage a Support Ticket
**CompTIA CertMaster Guided Lab | IT Help Desk | osTicket | Windows**

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



