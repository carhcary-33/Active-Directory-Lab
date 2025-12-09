# Active Directory Lab Project (Cary.local Domain)

## Overview
This project is a fully built enterprise-style Active Directory (AD) lab on Windows Server.  
It demonstrates real-world identity administration practices, including:

- Domain Controller installation
- DNS setup
- OU structure design
- Group Policy creation + security hardening
- Role-Based Access Control (RBAC)
- Privileged access separation
- User and group lifecycle management
- Security groups mapped to job functions

This repository serves as both a portfolio project and a technical reference for Active Directory administration.

---

## Lab Architecture

### Domain:
Cary.local

### Primary Domain Controller (PDC):
- Windows Server 2022  
- AD DS + DNS installed  
- SYSVOL + NETLOGON functioning

---

## Organizational Unit (OU) Structure

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

---

## Users Created

### Privileged Users
- Jessica Admin  
- Robert Admin  

### Standard Users
- John Doe  
- John Miller  
- Sarah Davis  

---

## Role-Based Access Control (RBAC) Security Groups

| Group Name           | Purpose                      | Members                              |
|----------------------|------------------------------|---------------------------------------|
| IT-Admins            | Domain administration        | Jessica Admin, Robert Admin           |
| Remote-Access        | RDP permissions              | Robert Admin                           |
| GG-StandardUsers     | Standard workforce access    | John Doe, John Miller, Sarah Davis     |

Additional groups created:
- GG-FileShareAdmins  
- GG-ServerAdmins  
- GG-WorkstationAdmins  

---

## Group Policy (GPO) Security Hardening

### Password Policy
- Minimum password length: 14 characters  
- Password history: 24 remembered  
- Complexity: Enabled  
- Maximum password age: 60 days  

### Account Lockout Policy
- Lockout threshold: 5 invalid attempts  
- Lockout duration: 30 minutes  
- Reset account lockout counter: 30 minutes  

---

## GPO Deployment Commands

To force GPO updates:
Gpupdate /force

To validate domain health:
dcdiag /v

---

## Skills Demonstrated
- Active Directory Domain Services  
- DNS configuration  
- Group Policy creation + hardening  
- Role-Based Access Control (RBAC)  
- Privileged Access Management  
- Least privilege design  
- User lifecycle + group modeling  
- Windows Server Administration  
- IAM fundamentals  

---

## Screenshots Folder
A folder named **/docs** will be added to include images of:
- OU structure  
- GPO configuration  
- User and group management  
- Security groups  

---

## Future Enhancements
- Add a secondary domain controller  
- Join a Windows 11 workstation  
- Configure file server + NTFS permissions  
- Add certificate authority (PKI)  
- Test SSO/SAML integrations  

---

## About
This lab was created as a hands-on IAM + Windows Server portfolio project to demonstrate identity administration and enterprise security concepts.


