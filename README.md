# Sebbeco-minienterprise-home-lab
A virtual mini enterprise environment lab. Build with Windows server, Active directory, Windows 11 
# Sebbeco Enterprise Home Lab

## Overview

This project documents the design, implementation and administration of a virtual enterprise IT environment.

The purpose is to gain practical experience in IT infrastructure, system administration, networking and cybersecurity by simulating a small corporate network.

The lab is built using VMware Workstation and consists of Windows Server and Windows 11 virtual machines.

## Lab Environment

| Component | Technology | Purpose |
|---|---|---|
| Hypervisor | VMware Workstation | Virtualization |
| Domain Controller | Windows Server 2025 | Active Directory and DNS |
| Client Workstation | Windows 11 Pro | Domain-connected workstation |
| Directory Services | Active Directory Domain Services | Centralized identity management |
| Group Policy | Group Policy Management | Centralized security configuration |

## Network Architecture

| Device | Hostname | IP Address |
|---|---|---|
| Domain Controller | DC01 | 192.168.10.10 |
| Client Workstation | CLIENT01 | 192.168.10.20 |

**Active Directory Domain:** `ad.Sebbeco.test`

## Implemented Features

### 1. Active Directory

- Installed and configured Active Directory Domain Services.
- Promoted Windows Server to a Domain Controller.
- Created the `ad.Sebbeco.test` domain.
- Configured DNS services.
- Created Organizational Units for IT, HR, Finance and Management.
- Created test user accounts and security groups.

### 2. Domain Management

- Joined a Windows 11 Pro workstation to the Active Directory domain.
- Verified domain authentication using a domain user account.
- Tested network connectivity between the client and Domain Controller.
- Verified DNS resolution.

### 3. Group Policy Management

- Created a dedicated Group Policy Object for the HR department.
- Configured automatic screen saver activation after 300 seconds.
- Enabled password protection when resuming from the screen saver.
- Verified policy application using `gpupdate` and `gpresult`.

## Technologies and Tools

- VMware Workstation
- Windows Server 2025
- Windows 11 Pro
- Active Directory
- DNS
- Group Policy Management
- PowerShell
- Networking and TCP/IP

## Future Improvements

- Implement additional Group Policy security configurations.
- Configure Windows Defender security policies.
- Deploy Wazuh SIEM for centralized security monitoring.
- Integrate Sysmon for endpoint event logging.
- Perform network scanning and security assessments.
- Document security incidents and investigation procedures.

## Project Status

**Ongoing development.**

This is a practical learning project. New configurations, tests and documentation will be added as the lab evolves.
