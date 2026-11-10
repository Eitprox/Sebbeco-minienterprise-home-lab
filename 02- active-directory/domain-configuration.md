
# Active Directory Domain Configuration

## Overview

Active Directory Domain Services (AD DS) is used to provide centralized identity and access management in the Sebbeco Enterprise Home Lab.

## Domain Information

| Setting | Value |
|---|---|
| Domain Name | ad.Sebbeco.test |
| NetBIOS Name | AD |
| Domain Controller | DC01 |
| Domain Controller IP | 192.168.10.10 |
| Operating System | Windows Server 2025 |

## Implemented Configuration

- Installed Active Directory Domain Services.
- Installed DNS Server.
- Promoted DC01 to a domain controller.
- Created the `ad.Sebbeco.test` domain.
- Configured DNS on the domain controller.
- Joined CLIENT01 to the domain.

## Domain Authentication

CLIENT01 successfully joined the domain.

A domain user account (`AD\hr.test1`) was used to verify that domain authentication works.

## Purpose

The domain provides centralized authentication and management of users and computers, simulating a small business IT infrastructure.
