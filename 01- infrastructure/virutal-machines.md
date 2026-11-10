
# Virtual Machines

This document describes the virtual machines used in the Sebbeco Enterprise Home Lab.

## Domain Controller – DC01

| Setting | Value |
|---|---|
| Operating System | Windows Server 2025 Standard Evaluation |
| Hostname | DC01 |
| IP Address | 192.168.10.10 |
| RAM | 4 GB |
| CPU | 2 vCPU |
| Disk | 80 GB |
| Role | Active Directory Domain Services and DNS |

## Client Workstation – CLIENT01

| Setting | Value |
|---|---|
| Operating System | Windows 11 Pro |
| Hostname | CLIENT01 |
| IP Address | 192.168.10.20 |
| RAM | 6 GB |
| CPU | 2 vCPU |
| Disk | 64–80 GB |
| Role | Domain-connected client workstation |

## Virtualization

- Hypervisor: VMware Workstation
- Network: Host-only (VMnet1)
- Network subnet: 192.168.10.0/24

## Purpose

The virtual machines simulate a small enterprise IT environment. DC01 provides centralized identity and DNS services, while CLIENT01 represents an employee workstation joined to the Active Directory domain.
