# Organizational Unit Structure

## Overview

Organizational Units (OUs) are used to organize users and computers within Active Directory. They also allow Group Policies to be applied to specific departments.

## OU Structure

The lab uses the following structure:

ad.Sebbeco.test
└── Sebbeco
    - IT
    - HR
    - Finance
    - Management

## Department OUs

| Organizational Unit | Purpose |
|---|---|
| IT | IT staff and support accounts |
| HR | Human Resources employees |
| Finance | Finance department employees |
| Management | Management accounts |

## Purpose

This structure simulates a small enterprise where users are organized by department.

It provides a foundation for:
- Department-specific Group Policies.
- Delegated administration.
- User and computer management.
- Access control based on organizational roles.
