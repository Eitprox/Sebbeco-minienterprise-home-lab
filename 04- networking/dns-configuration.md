

# DNS Configuration

## Overview

DNS (Domain Name System) translates domain names into IP addresses.

In the Sebbeco Enterprise Home Lab, DC01 runs the DNS Server role and provides DNS resolution for the Active Directory domain.

## DNS Configuration

| Setting | Value |
|---|---|
| DNS Server | DC01 |
| DNS Server IP | 192.168.10.10 |
| DNS Zone | ad.Sebbeco.test |
| Client DNS Server | 192.168.10.10 |

## Implemented Tasks

- Installed the DNS Server role on DC01.
- Configured DNS as part of Active Directory Domain Services.
- Configured CLIENT01 to use DC01 as its preferred DNS server.
- Verified domain name resolution from CLIENT01.

## DNS Testing

The following commands were used on CLIENT01:

### Test DNS Resolution

```powershell
nslookup ad.Sebbeco.test
```

Expected result: the domain resolves to the domain controller's IP address, `192.168.10.10`.

### Test Domain Controller Connectivity

```powershell
ping DC01
```

### Test Active Directory Service Records

```powershell
nslookup -type=SRV _ldap._tcp.dc._msdcs.ad.Sebbeco.test
```

This query checks whether DNS can locate the LDAP service records used by Active Directory clients to find domain controllers.

## Why DNS Matters

Active Directory depends on DNS to locate domain controllers and services such as LDAP and Kerberos.

Incorrect DNS configuration can prevent clients from joining the domain or authenticating successfully.
