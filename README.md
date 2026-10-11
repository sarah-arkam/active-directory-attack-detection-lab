# Active Directory Attack & Detection Lab

## Table of Contents
- [Overview](#overview)
- [Goals](#goals)
- [Project Status](#project-status)
- [Screenshots](#screenshots)
  - [01 - AD DS Installed](#01---ad-ds-installed)
  - [02 - Active Directory Domain Structure](#02---active-directory-domain-structure)
  - [03 - Users and Organizational Units](#03---users-and-organizational-units)
  - [04 - Domain-Joined Windows Workstation](#04---domain-joined-windows-workstation)
  - [05 - Domain-Joined Workstation Verification](#05---domain-joined-workstation-verification)
  - [06 - Security Group Membership](#06---security-group-membership)
  - [07 - Group Policy Management](#07---group-policy-management)
  - [08 - Domain User Authentication](#08---domain-user-authentication)
  - [09 - Sysmon Deployment on Windows 11 Workstation](#09---sysmon-deployment-on-windows-11-workstation)
  - [10 - Live Sysmon Telemetry Verification](#10---live-sysmon-telemetry-verification)
  - [11 - Sysmon Service Verification](#11---sysmon-service-verification)
  - [12 - Wazuh Agent Enrollment Status](#12---wazuh-agent-enrollment-status)
  - [13 - Wazuh Endpoint Monitoring Dashboard](#13---wazuh-endpoint-monitoring-dashboard)

## Overview

This project demonstrates the design and deployment of a small Active Directory environment for learning Windows administration, authentication security, threat detection, and security monitoring.

The lab currently consists of a Windows Server Domain Controller and a domain-joined Windows 11 workstation. The lab now integrates Sysmon and Wazuh SIEM to provide centralized security monitoring, endpoint telemetry collection, and detection engineering capabilities.

## Goals

- Build and administer an Active Directory environment
- Configure domain users, groups, and organizational units
- Investigate authentication and account management events
- Collect and analyze Windows logs using Wazuh
- Develop detection workflows for common attack techniques
- Document findings and mitigation recommendations


## Project Status

🚧 **In Progress**

**Current Phase:** Telemetry Collection & Security Monitoring

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
- Installed Sysmon on WS01
- Integrated Wazuh SIEM
- Enrolled DC01 and WS01 in Wazuh
- Verified endpoint telemetry collection

### Next Steps

- Validate Sysmon telemetry ingestion within Wazuh
- Monitor authentication and account management events
- Create custom detection rules in Wazuh
- Simulate Active Directory attack scenarios
- Map detections to MITRE ATT&CK techniques
- Develop security monitoring dashboards
- Document investigation and incident response workflows
  
## Screenshots

### 01 - AD DS Installed

Installed Active Directory Domain Services (AD DS) on Windows Server 2022 in preparation for domain controller promotion.

<img width="791" height="567" alt="01-ad-ds-installed" src="https://github.com/user-attachments/assets/6dbe9be4-4a05-46e2-9147-dbdce5e08043" />

---

### 02 - Active Directory Domain Structure

Verified the successful creation of the `arkam.local` Active Directory domain and reviewed the default organizational structure, including built-in containers for users, computers, domain controllers, and security principals.

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

### 09 - Sysmon Deployment on Windows 11 Workstation

Successfully deployed Sysmon on a domain-joined Windows 11 workstation using a tuned monitoring configuration. Sysmon provides detailed endpoint telemetry including process creation, network connections, and security-relevant system activity used for detection engineering and threat hunting.

<img width="922" height="307" alt="09" src="https://github.com/user-attachments/assets/b19d7e9e-7cad-4133-940d-86d4382c071b" />

### 10 - Live Sysmon Telemetry Verification

Verified successful Sysmon deployment by reviewing live endpoint telemetry through the Microsoft-Windows-Sysmon Operational log. Sysmon captured process creation (Event ID 1) and file creation (Event ID 11) activity, providing enriched telemetry for future threat detection and Wazuh SIEM integration.

<img width="982" height="282" alt="10" src="https://github.com/user-attachments/assets/20a0021c-0fc9-4edb-9637-afe45cc2273a" />

### 11 - Sysmon Service Verification

Verified successful Sysmon deployment on a domain-joined Windows 11 workstation. The Sysmon64 service is running and collecting endpoint telemetry that will be forwarded to Wazuh for centralized security monitoring and threat detection.

<img width="642" height="102" alt="11" src="https://github.com/user-attachments/assets/478fc59c-6a58-4013-80eb-fbd9e8557026" />

### 12 - Wazuh Agent Enrollment Status

Successfully integrated Windows endpoints with the Wazuh SIEM platform. Both the Windows Server 2022 Domain Controller (DC01) and Windows 11 workstation (WS01) are actively enrolled and forwarding security telemetry for centralized monitoring and threat detection.

<img width="947" height="312" alt="12" src="https://github.com/user-attachments/assets/e3a1839f-7386-4eb1-ac2e-3943842750e6" />

### 13 - Wazuh Endpoint Monitoring Dashboard

Successfully enrolled the Windows 11 workstation (WS01) into Wazuh SIEM and verified active endpoint monitoring. Wazuh is collecting security telemetry, mapping events to MITRE ATT&CK techniques, performing security configuration assessments, and monitoring endpoint activity for threat detection.

<img width="1917" height="917" alt="13" src="https://github.com/user-attachments/assets/54c25863-de82-4350-b4b6-adc3e1ea5eac" />
