Active Directory Lab Project (Cary.local Domain)
📝 Overview

This project is a full enterprise-style Active Directory (AD) lab built on Windows Server.
It demonstrates real-world identity administration practices, including:

Domain Controller installation

DNS setup

OU structure design

Group Policy creation + security hardening

Role-Based Access Control (RBAC)

Privileged access separation

User and group lifecycle management

Security groups mapped to job functions

This repository serves as both a portfolio project and a technical reference for Active Directory administration.

🏗️ Lab Architecture
Domain:

Cary.local

Primary Domain Controller (PDC):

Windows Server 2022

DNS + AD DS installed

SYSVOL + NETLOGON functioning

Organizational Units structured for enterprise-style management

📁 Organizational Unit (OU) Structure
Cary.local
│
├── Administration
│   ├── Admins
│   └── Service Accounts
│
├── Users
│   ├── Privileged Users
│   └── Standard Users
│
├── Computers
│   ├── Workstations
│   └── Servers
│
└── Groups
    ├── Security Groups
    └── Distribution Groups

👥 Users Created
Privileged Users

Jessica Admin

Robert Admin

Standard Users

John Doe

John Miller

Sarah Davis

🔐 Role-Based Access Control (RBAC) Security Groups
Group Name	Purpose	Members
IT-Admins	Domain administration	Jessica Admin, Robert Admin
Remote-Access	RDP permissions	Robert Admin
GG-StandardUsers	General workforce access	John Doe, John Miller, Sarah Davis

Additional groups include:

GG-FileShareAdmins

GG-ServerAdmins

GG-WorkstationAdmins

GG-StandardUsers

🛡️ Group Policy Objects (GPOs) Configured
Password Policy

Minimum length: 14 characters

Password history: 24 remembered

Maximum age: 60 days

Complexity requirements: Enabled

Account Lockout Policy

Lockout threshold: 5 invalid attempts

Lockout duration: 30 minutes

Reset account lockout counter after: 30 minutes

🔄 GPO Deployment & Verification

Policies applied domain-wide using:

gpupdate /force


Domain health verified via:

dcdiag

🧠 Skills Demonstrated

✔ Active Directory Domain Services (AD DS)
✔ DNS configuration & domain name resolution
✔ OU + GPO architecture and hardening
✔ Privileged access management
✔ RBAC / least privilege design
✔ User lifecycle + group membership modeling
✔ Windows Server administration
✔ Identity & Access Management fundamentals

🖼️ Screenshots

A dedicated folder exists in this repo for screenshots:

/screenshots

(To be populated with OU structure, GPO settings, security groups, etc.)

📌 Future Enhancements

Add a second domain controller

Join a Windows 11 workstation to the domain

Create mapped network drives via GPO

Add a file server with NTFS permissions

Implement a Certificate Authority (PKI)

Test SSO/SAML integrations in the lab

📣 About This Project

Created as a hands-on Identity & Access Management (IAM) and Windows Server administration portfolio project.
