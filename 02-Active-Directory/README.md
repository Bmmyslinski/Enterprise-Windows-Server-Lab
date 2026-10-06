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
```
<img width="597" height="571" alt="Active directory structure" src="https://github.com/user-attachments/assets/21775b3b-4733-4e68-a655-7515d2899511" />

## Domain Client Management

A Windows 11 client was joined to the bennylab.local domain and centrally managed through Active Directory.

The computer account was organized within the custom Computers OU, allowing computer-based Group Policy settings to be applied to the workstation.

<img width="561" height="461" alt="Screenshot 2026-10-05 at 8 11 28 PM" src="https://github.com/user-attachments/assets/bcc4e0aa-6b49-4239-bb57-8fa764cb0b18" />

## Verification

Active Directory functionality was verified by confirming that the Windows 11 workstation successfully joined the bennylab.local domain and that its computer account appeared within the custom Computers OU.

PowerShell was also used to verify the domain controller and domain-joined computer objects.

```powershell
Get-ADDomainController
Get-ADComputer -Filter *
```

<img width="1609" height="457" alt="Get-ADDomainController" src="https://github.com/user-attachments/assets/7da1cb98-8189-46b0-b518-36dbcd7f3fb0" />

<img width="705" height="385" alt="Get-ADComputer" src="https://github.com/user-attachments/assets/7bc5dddc-6d2c-40b6-8c2e-72e94a897b26" />

