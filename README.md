<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

Once osTicket is installed, it must be configured to:

- Define agent permissions

- Organize departments

- Control ticket visibility

- Establish service level agreements (SLAs)

- Create help topics for proper routing

- Add agents and users

This guide walks through each section inside the Admin and Agent panels.
<h2>Configuration Steps</h2>

# osTicket System Configuration Guide

This repository outlines the essential post-installation configuration steps for setting up **osTicket** in a structured help desk environment. After completing the installation on your virtual machine via Remote Desktop, these steps prepare the system for real-world IT support operations.

---

# Admin Panel vs Agent Panel

### Admin Panel

<p>
<img width="853" height="498" alt="Screenshot RD26" src="https://github.com/user-attachments/assets/d1afe101-bca2-47bb-9205-e9ac6626184b" />
</p>

Used for system configuration and management:

* Roles
* Departments
* Teams
* SLAs
* Help Topics
* User settings

This is where administrators control how the help desk functions.

### Agent Panel

<p>
<img width="853" height="498" alt="Screenshot RD27" src="https://github.com/user-attachments/assets/bd6931b4-dc4e-460d-8fa3-7b9c07140fd2" />
</p>

Used for operational tasks:

* Viewing and responding to tickets
* Managing users
* Daily support workflow

This is where support staff work tickets.

---

# Create Roles (Permission Groups)

<p>
<img width="853" height="498" alt="Screenshot RD28" src="https://github.com/user-attachments/assets/0f1968f0-02ef-48e7-b718-c4c56184fe61" />
</p>

 Admin Panel → Agents → Roles

Create:

 - "Supreme Admin"

Roles determine what agents are allowed to do within the system (edit tickets, manage users, configure settings, etc.).

---

# Create Departments (Ticket Routing & Visibility)

<p>
<img width="853" height="498" alt="Screenshot RD29" src="https://github.com/user-attachments/assets/9946c687-633e-48e4-b454-1af7317c515d" />
</p>

 Admin Panel → Agents → Departments

Create:

 - "SysAdmins"

Departments help separate responsibilities such as:

 - Help Desk
 - System Administration
 - Networking

They control ticket assignment and visibility.

---

# Create Teams (Cross-Department Groups)

<p>
<img width="853" height="498" alt="Screenshot RD30" src="https://github.com/user-attachments/assets/d9cb80f8-f861-4d1a-90de-d230b27be9c0" />
</p>

 Admin Panel → Agents → Teams

Create:

 - "Online Banking"

Teams allow agents from different departments to collaborate on specific services or projects.

---

# Configure Ticket Submission Settings

<p>
<img width="853" height="498" alt="Screenshot RD31" src="https://github.com/user-attachments/assets/039c0e67-5c9c-421e-af2f-1853a4b9673a" />
</p>

 Admin Panel → Settings → User Settings

To allow anyone to submit tickets:

 - Disable “Registration Required”

To require authentication before ticket creation:

 - Enable “Require registration and login”

For business environments, requiring registration is recommended.

---

# Add Agents (Staff Members)

<p>
<img width="853" height="498" alt="Screenshot RD32" src="https://github.com/user-attachments/assets/98b20fea-63f6-40e5-9a85-a433cf4f8029" />
</p>

<p>
<img width="851" height="497" alt="Screenshot RD33" src="https://github.com/user-attachments/assets/8e5c53ac-0b4b-4cb3-8926-d713d49cf3c2" />
</p>

 Admin Panel → Agents → Add New

Add:

 - "Jane" → Department: SysAdmins
 - "John" → Department: Support

Agents are internal employees responsible for resolving tickets.

---

# Add Users (Customers)

<p>
<img width="853" height="497" alt="Screenshot RD34" src="https://github.com/user-attachments/assets/23052496-f1a6-45be-91aa-88bca3ef0240" />
</p>

<p>
<img width="853" height="497" alt="Screenshot RD35" src="https://github.com/user-attachments/assets/d50e0654-3144-49dd-abab-e38d8d4cb7d8" />

</p>

 Agent Panel → Users → Add New

Add:

 - "Karen"
 - "Ken"

Users represent customers or employees submitting support requests.

---

# Configure Service Level Agreements (SLAs)

 Admin Panel → Manage → SLA

Create:

<p>
<img width="853" height="497" alt="Screenshot RD36" src="https://github.com/user-attachments/assets/9999b900-611e-406b-a2da-fba285b493d0" />
</p>

"Sev-A"

  - 1-hour response time
  - 24/7 schedule

<p>
<img width="853" height="497" alt="Screenshot RD37" src="https://github.com/user-attachments/assets/9ca1e47d-da2b-4475-9028-f4aaf0ccd562" />
</p>

"Sev-B"

  - 4-hour response time
  - 24/7 schedule

<p>
<img width="853" height="497" alt="Screenshot RD38" src="https://github.com/user-attachments/assets/6c7213b3-86dc-4c34-a8b4-8a82bb562c56" />
</p>

"Sev-C"

  - 8-hour response time
  - Business hours schedule

SLAs define how quickly tickets must be addressed based on priority.

---

# 📝 Create Help Topics

📍 Admin Panel → Manage → Help Topics

Add:

* Business Critical Outage
* Personal Computer Issues
* Equipment Request
* Password Reset
* Other

Help Topics help categorize and route tickets efficiently.

---

# ✅ Outcome

After completing these configurations:

* Permissions are structured
* Departments are organized
* Teams enable collaboration
* Agents and users are created
* SLAs enforce response expectations
* Help topics streamline ticket intake

The help desk system is now fully structured and ready for production-level use.

---

🚀 This configuration transforms osTicket from a basic installation into a functional, enterprise-style ticketing environment suitable for IT support operations.
