# Active Directory Attack & Detection Lab

## Overview

This project demonstrates the design and deployment of a small Active Directory environment for learning Windows administration, authentication security, threat detection, and security monitoring.

The lab currently consists of a Windows Server Domain Controller and a domain-joined Windows 11 workstation. Future phases will integrate Sysmon and Wazuh SIEM to support security monitoring, threat detection, and attack simulation.

## Goals

- Build and administer an Active Directory environment
- Configure domain users, groups, and organizational units
- Investigate authentication and account management events
- Collect and analyze Windows logs using Wazuh
- Develop detection workflows for common attack techniques
- Document findings and mitigation recommendations


## Project Status

🚧 **In Progress**

**Current Phase:** Active Directory Administration & Identity Management

### Completed

- Built a Windows Server 2022 Domain Controller
- Installed Active Directory Domain Services (AD DS)
- Created and deployed the `arkam.local` domain
- Created Organizational Units (Employees, IT)
- Created and managed domain user accounts
- Joined a Windows 11 workstation to the domain
- Created security groups and configured role-based access control (RBAC)
- Created and linked a Group Policy Object (GPO)
- Authenticated to a domain-joined workstation using an Active Directory account

### Next Steps

- Install Sysmon on domain assets
- Integrate Wazuh SIEM
- Monitor authentication and account management events
- Simulate attack scenarios
- Develop detection use cases
- Create security monitoring dashboards
  
## Screenshots

### 01 - AD DS Installed


Installed Active Directory Domain Services (AD DS) on Windows Server 2022 in preparation for domain controller promotion.

<img width="791" height="567" alt="01-ad-ds-installed" src="https://github.com/user-attachments/assets/6dbe9be4-4a05-46e2-9147-dbdce5e08043" />

---

### 02 - Active Directory Domain Structure

Verified the successful creation of the `arkam.local` Active Directory domain and reviewed the default organizational structure, including built-in containers for users, computers, domain controllers, and security principals.
Show more lines

<img width="205" height="130" alt="02-active-directory-domain-structure" src="https://github.com/user-attachments/assets/7b32658c-7927-4fcd-9922-5ff2554962f5" />
---

### 03 - Users and Organizational Units

Created Organizational Units (OUs) and user accounts within the `arkam.local` Active Directory domain to simulate a small enterprise environment. User accounts were organized within the Employees OU to demonstrate identity and access management concepts commonly used in corporate networks.

<img width="567" height="266" alt="03-users-and-ous" src="https://github.com/user-attachments/assets/e4ec51e6-aaa9-4e83-abac-48ae48b90e64" />
---

### 04 - Domain-Joined Windows Workstation

Successfully joined a Windows 11 workstation to the `arkam.local` Active Directory domain. Domain membership enables centralized authentication, account management, and access control across the environment.

<img width="511" height="476" alt="04-domain-join-success" src="https://github.com/user-attachments/assets/7e6cbebc-a61a-4032-b557-7582e8edf1d2" />
---

### 05 - Domain-Joined Workstation Verification

Verified successful enrollment of a Windows 11 workstation into the `arkam.local` Active Directory domain. The workstation appears in Active Directory and can now be centrally managed through domain-based administration.

<img width="741" height="501" alt="05-domain-workstation-in-active-directory" src="https://github.com/user-attachments/assets/99cb413e-6eb0-4bf2-833f-01c55c3eda07" />
---

### 06 - Security Group Membership

Created an Active Directory security group (`IT_Admins`) and assigned a domain user to the group to demonstrate role-based access control (RBAC) and identity management within an enterprise environment.

Group memberships allow administrators to manage permissions through security groups instead of assigning access directly to individual users.

<img width="807" height="477" alt="06-security-group-membership" src="https://github.com/user-attachments/assets/4c53af2b-05ec-4b4e-9efd-d79dcdc470b4" />
---

### 07 - Group Policy Management

Created and linked a Group Policy Object (GPO) named `Security Baseline` within the `arkam.local` domain to demonstrate centralized policy administration.

Group Policy allows administrators to enforce security and configuration settings across domain-joined systems from a central management interface.

<img width="256" height="120" alt="07-group-policy-management" src="https://github.com/user-attachments/assets/a2395d41-d9b8-4341-9511-507c7354b5fd" />
---

### 08 - Domain User Authentication

Successfully authenticated to a domain-joined Windows 11 workstation using the Active Directory account `Sarah.Arkam`. This demonstrates centralized authentication and identity management within the `arkam.local` environment.

<img width="350" height="137" alt="08-domain-user-authentication" src="https://github.com/user-attachments/assets/0f082f74-77a3-461a-bd6f-9298fb856214" />
