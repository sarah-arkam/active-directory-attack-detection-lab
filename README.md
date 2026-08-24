# Active Directory Attack & Detection Lab

## Overview

This project demonstrates the design and deployment of a small Active Directory environment for learning Windows administration, authentication security, threat detection, and security monitoring.

The lab consists of a Windows Server Domain Controller, a domain-joined Windows workstation, Sysmon, and Wazuh SIEM.

## Goals

- Build and administer an Active Directory environment
- Configure domain users, groups, and organizational units
- Investigate authentication and account management events
- Collect and analyze Windows logs using Wazuh
- Develop detection workflows for common attack techniques
- Document findings and mitigation recommendations

## Lab Architecture

```text
Domain Controller (Windows Server)
            |
            |
      Active Directory
            |
            |
Domain-Joined Workstation
            |
            |
          Sysmon
            |
            |
          Wazuh
```
## Technologies

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- Windows 10/11
- Sysmon
- Wazuh SIEM
- VMware Workstation

## Planned Attack Scenarios

- Failed Logon Attempts
- Account Lockouts
- New User Creation
- Privileged Group Membership Changes
- PowerShell Execution Monitoring
- Password Spraying
- Kerberoasting *(Future Enhancement)*

## Planned Detection Use Cases

- Authentication Failures
- Excessive Login Attempts
- Account Changes
- Privilege Escalation Activity
- Suspicious PowerShell Usage

## Skills Demonstrated

- Windows Administration
- Active Directory Management
- Identity and Access Management (IAM)
- Security Monitoring
- Threat Analysis
- Incident Investigation
- Technical Documentation and Reporting

## Project Status

🚧 **In Progress**

**Current Phase:** Environment Design & Deployment
