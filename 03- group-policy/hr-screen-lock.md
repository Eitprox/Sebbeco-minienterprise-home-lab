
# HR Screen Lock Group Policy

## Overview

A Group Policy Object (GPO) was created to enforce screen saver security settings for users in the HR department.

The purpose is to reduce the risk of unauthorized access when employees leave their workstations unattended.

## GPO Configuration

| Setting | Value |
|---|---|
| GPO Name | GPO-HR-ScreenLock-5min |
| Linked OU | Sebbeco/HR |
| Screen Saver | Enabled |
| Screen Saver Timeout | 300 seconds |
| Password Protection | Enabled |

## Configuration Path

User Configuration → Policies → Administrative Templates → Control Panel → Personalization

The following settings were configured:

- Enable screen saver: Enabled
- Screen saver timeout: 300 seconds
- Password protect the screen saver: Enabled

## Verification

The policy was tested on CLIENT01 using the HR domain account `AD\hr.test1`.

The following commands were used:

```powershell
gpupdate /force
gpresult /r
```

The `gpresult /r` output confirmed that the HR screen-lock GPO was applied to the user.

## Result

The Group Policy was successfully linked to the HR Organizational Unit and confirmed as applied to the HR test account.

## Skills Demonstrated

- Group Policy Management
- Active Directory administration
- Windows security configuration
- Policy deployment and troubleshooting
- PowerShell verification

