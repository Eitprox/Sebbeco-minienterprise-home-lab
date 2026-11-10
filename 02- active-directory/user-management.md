
# User and Group Management

## Overview

Active Directory user accounts and security groups are used to manage access to resources and simplify administration.

## User Accounts

The following test accounts have been created:

| Username | Department | Purpose |
|---|---|---|
| hr.test1 | HR | Test employee account |
| it.admin1 | IT | IT administration test account |

## Security Groups

| Group Name | Location | Purpose |
|---|---|---|
| IT-Support | Sebbeco/IT | Represents the IT support team |

## Implemented Tasks

- Created department-specific user accounts.
- Organized users into their respective Organizational Units.
- Created an IT-Support security group.
- Used a domain account to verify authentication on CLIENT01.

## Why Use Security Groups?

Security groups make access management easier. Instead of assigning permissions to individual users, administrators can assign permissions to a group and manage membership centrally.

## Security Considerations

- Use individual accounts instead of shared accounts.
- Apply least-privilege principles.
- Avoid using privileged accounts for everyday tasks.
- Use strong passwords and appropriate account policies.
