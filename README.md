# Active Directory Home Lab

## Overview

This project documents a hands-on Active Directory home lab built on Windows Server 2022 using VirtualBox. The lab simulates a real-world Windows enterprise environment covering the core tasks performed by IT help desk technicians and system administrators on a daily basis.

All configurations were performed on a live Windows Server 2022 Domain Controller connected to a Windows 10 client machine.

---

## Skills Demonstrated

- Active Directory Domain Services installation and configuration
- Domain Controller promotion and domain creation
- Organizational Unit design and management
- User account creation, modification, and lifecycle management
- Security group creation and group-based access management
- Common help desk tasks: password resets, account unlocks, account disables
- Group Policy Object creation and linking
- Password and account lockout policy enforcement
- Targeted GPO design for department-level access control
- DNS forward and reverse lookup zone configuration
- DHCP scope creation and management

---

## Lab Environment
Host Machine:       Windows 11
Hypervisor:         Oracle VirtualBox
Domain Controller:  Windows Server 2022 — DC01
Client Machine:     Windows 10
Domain:             lab.local
DC IP Address:      192.168.1.100
DHCP Scope:         192.168.1.150 – 192.168.1.200

---

## Modules

| Module | Topic | Key Concepts |
|--------|-------|-------------|
| [Module 1](./module-1-active-directory.md) | Active Directory & Domain Controller | AD DS installation, domain promotion, lab.local domain |
| [Module 2](./module-2-user-management.md) | User & Group Management | OUs, user creation, security groups, help desk tasks |
| [Module 3](./module-3-group-policy.md) | Group Policy | Password policy, account lockout, department GPOs |
| [Module 4](./module-4-dns-dhcp.md) | DNS & DHCP | Forward/reverse lookup zones, DHCP scope |
| Coming Soon | Ticketing System | osTicket installation, ticket workflow simulation |

---

## Real-World Relevance

**Module 1** mirrors the process IT administrators follow when setting up a new Windows domain environment from scratch. Every company running Windows uses Active Directory so, understanding how it's deployed is foundational knowledge for any IT role.

**Module 2** covers the most frequent daily tasks of an IT help desk technician. Password resets, account unlocks, and user onboarding are the top three tickets in any Windows environment. Hands-on experience with these tasks means hitting the ground running on day one.

**Module 3** demonstrates how IT departments enforce security policies across an entire organization from one central location. Group Policy is how companies ensure every machine meets security standards without touching each device individually.

**Module 4** covers the two services that keep a network running. When users report they can't connect to the network or can't reach internal resources, DNS and DHCP are almost always the first place to look.

---

## User Accounts Created

| Name | Username | Department | OU |
|------|----------|------------|----|
| John Smith | jsmith | IT | IT |
| Lisa Wilson | lwilson | IT | IT |
| Sarah Johnson | sjohnson | HR | HR |
| Mike Davis | mdavis | Finance | Finance |

---

## Group Policy Objects

| GPO Name | Linked To | Purpose |
|----------|-----------|---------|
| Default Domain Policy | lab.local | Password and account lockout policy |
| IT-Department-Policy | IT OU | Control Panel access enabled for IT staff |
| HR-Department-Policy | HR OU | Control Panel access restricted for HR staff |

---

## Screenshots

All lab screenshots are located in the [`/screenshots`](./screenshots/) directory, organized by module.

---

## Tools & Services Used

- Oracle VirtualBox
- Windows Server 2022
- Windows 10
- Active Directory Domain Services
- Group Policy Management
- DNS Manager
- DHCP Manager

---
