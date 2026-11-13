# Sebbeco Enterprise Home Lab

A virtual mini-enterprise environment built to develop practical skills in IT infrastructure, system administration, networking and cybersecurity.

## Overview

This project documents the design, implementation and administration of a virtual enterprise IT environment.

The purpose is to gain practical experience by simulating a small corporate network using VMware Workstation, Windows Server, Windows 11 and Ubuntu Server.

The lab is continuously expanded with new infrastructure configurations, security monitoring capabilities and practical investigation exercises.

## Lab Environment

| Component | Technology | Purpose |
|---|---|---|
| Hypervisor | VMware Workstation | Virtualization |
| Domain Controller | Windows Server 2025 | Active Directory and DNS |
| Client Workstation | Windows 11 Pro | Domain-connected workstation |
| SIEM Server | Ubuntu Server 24.04.5 | Wazuh Manager, Indexer and Dashboard |
| Directory Services | Active Directory Domain Services | Centralized identity management |
| Group Policy | Group Policy Management | Centralized security configuration |

## Network Architecture

The virtual machines communicate through an isolated VMware Host-only network.

| Device | Hostname | IP Address |
|---|---|---|
| Domain Controller | DC01 | 192.168.10.10 |
| Client Workstation | CLIENT01 | 192.168.10.20 |
| SIEM Server | WAZUH01 | 192.168.10.30 |

**Network:** `192.168.10.0/24`

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
- Created a security GPO enabling PowerShell Script Block Logging.
- Verified policy application using `gpupdate` and `gpresult`.

### 4. Security Monitoring and SIEM

- Deployed Wazuh as an all-in-one SIEM solution on Ubuntu Server.
- Installed and enrolled the Wazuh agent on CLIENT01.
- Integrated Sysmon for detailed Windows endpoint telemetry.
- Configured PowerShell Operational event collection.
- Enabled raw JSON event archiving on the Wazuh Manager.
- Configured a Wazuh Dashboard index pattern for archived events.
- Verified centralized event collection through Wazuh Discover.

### 5. Security Event Investigation

Collected and investigated the following event types:

| Event ID | Source | Description |
|---|---|---|
| 1 | Sysmon | Process creation |
| 3 | Sysmon | Network connection |
| 5 | Sysmon | Process termination |
| 11 | Sysmon | File creation |
| 4104 | PowerShell | Script Block Logging |

Practical exercises include:

- Investigating parent-child process relationships.
- Analyzing PowerShell execution and script contents.
- Investigating endpoint network connections.
- Correlating process and network activity.
- Assessing suspicious behaviour using available event evidence.

All current investigation exercises use controlled, benign activity within the isolated lab.

## Technologies and Tools

- VMware Workstation
- Windows Server 2025
- Windows 11 Pro
- Ubuntu Server 24.04.5 LTS
- Active Directory Domain Services
- DNS
- Group Policy Management
- PowerShell
- Sysmon
- Wazuh SIEM
- Linux administration
- Networking and TCP/IP
- Git and GitHub

## Future Improvements

- Implement additional Group Policy security configurations.
- Expand Windows Defender monitoring.
- Configure PowerShell Module Logging.
- Develop custom Wazuh detection rules.
- Perform network scanning and service enumeration using Nmap.
- Document additional security incidents and investigation procedures.
- Expand SOC investigation and incident response exercises.

## Project Status

**Ongoing development.**

The core infrastructure, Active Directory environment and initial security monitoring implementation are operational.

Wazuh successfully collects Sysmon and PowerShell events from CLIENT01, which can be investigated centrally through Wazuh Dashboard.

New configurations, tests and documentation will continue to be added as the lab evolves.
