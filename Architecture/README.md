# IT Support Home Lab Architecture

## Network Diagram

![Network Diagram](network-diagram.png)

## Environment

The lab consists of a Windows Server 2025 domain controller and a Windows 11 workstation connected through an isolated VirtualBox internal network. The environment simulates a small business Active Directory infrastructure used to practice common Help Desk and systems administration tasks.

### Domain
- **Domain:** RockyPetSupply.local

### Domain Controller
- **Hostname:** RPS-DC01
- **IP Address:** 192.168.10.10
- **Services:** Active Directory Domain Services (AD DS), DNS, File Shares

### Workstation
- **Hostname:** RPS-WS01
- **IP Address:** 192.168.10.20
- **Status:** Domain Joined

## Lab Workflow

1. User logs into the domain.
2. Authentication is handled by Active Directory.
3. DNS resolves domain resources.
4. The user accesses shared folders and mapped drives.
5. Issues are documented and resolved through Jira Service Management.
