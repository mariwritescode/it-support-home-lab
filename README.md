# IT Support Home Lab

## Overview

This project builds on the **Active Directory Administration Lab** by simulating common Help Desk and IT support tasks in a Windows Server 2025 environment. Using realistic support tickets, I diagnosed and resolved issues involving file share permissions, mapped network drives, DNS, and Active Directory while documenting each case in Jira Service Management and creating supporting knowledge base articles.

The lab includes:
- Managing Active Directory users and security groups
- Configuring NTFS and file share permissions
- Mapping and troubleshooting network drives
- Diagnosing and resolving DNS issues
- Documenting incidents in Jira Service Management
- Creating knowledge base articles for common support issues

### Example Help Desk Scenarios

- **HD-001: User Unable to Access Accounting Share** – Diagnosed NTFS permission issues preventing access to a departmental file share and restored the appropriate permissions.
- **HD-002: Accounting Network Drive Missing** – Restored a missing mapped network drive and verified successful user access.
- **HD-003: Workstation Unable to Resolve Domain Resources** – Diagnosed and corrected DNS configuration issues preventing access to domain resources.

This lab demonstrates the troubleshooting, documentation, and customer support responsibilities commonly performed by an IT Support or Help Desk technician.

## Environment

### Domain Controller
- **Operating System:** Windows Server 2025
- **Services:** Active Directory Domain Services (AD DS), DNS
- **Resources:** File Shares

### Workstation
- **Operating System:** Windows 11
- **Status:** Domain Joined

### Ticketing Platform
- Jira Service Management

## Repository Structure

```text
IT-Support-Home-Lab
│
├── Architecture
│
├── Help-Desk-Tickets
│   ├── HD-001-Accounting-Share-Access
│   ├── HD-002-Network-Drive-Missing
│   └── HD-003-DNS-Troubleshooting
│
├── Jira-Service-Management
│
├── Knowledge-Base
│
└── README.md
```
