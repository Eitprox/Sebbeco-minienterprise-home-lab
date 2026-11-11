

# Network Configuration

## Overview

The Sebbeco Enterprise Home Lab uses an isolated virtual network to allow communication between the domain controller and client workstation.

## Network Details

| Setting | Value |
|---|---|
| Hypervisor | VMware Workstation |
| Network Adapter | VMnet1 |
| Network Type | Host-only |
| Subnet | 192.168.10.0/24 |
| Default Gateway | Not configured |

## IP Address Configuration

| Device | Hostname | IP Address | Subnet Mask |
|---|---|---|---|
| Domain Controller | DC01 | 192.168.10.10 | 255.255.255.0 |
| Client Workstation | CLIENT01 | 192.168.10.20 | 255.255.255.0 |

## DNS Configuration

CLIENT01 uses DC01 as its DNS server:

- Preferred DNS server: 192.168.10.10

## Connectivity Testing

Connectivity between CLIENT01 and DC01 was tested using:

```powershell
ping 192.168.10.10
```

The test returned successful replies, confirming network connectivity between the two virtual machines.

## Purpose

The isolated network provides a controlled environment for testing Active Directory, DNS, domain authentication and future security monitoring tools.
