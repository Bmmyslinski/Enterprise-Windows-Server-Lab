# Active Directory Domain Services

## Objective

Configure Active Directory Domain Services (AD DS) on Windows Server 2022 to provide centralized identity and computer management for the bennylab.local lab environment.

## Domain Configuration

| Setting | Configuration |
|---|---|
| Domain Name | bennylab.local |
| NetBIOS Name | BENNYLAB |
| Domain Controller | BEN-SERVER1 |
| Domain Controller IP | 192.168.8.176 |
| Operating System | Windows Server 2022 |
## Organizational Unit Structure

A custom organizational unit structure was created to organize users, computers, servers, service accounts, and security groups within the domain.

The structure separates user accounts by department, allowing Group Policy settings and access controls to be applied based on organizational role.

```text
BennyLab
├── Computers
├── Groups
├── Servers
├── Service Accounts
└── Users
    ├── Accounting
    ├── HR
    ├── IT
    ├── Management
    └── Sales
