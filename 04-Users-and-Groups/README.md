# Active Directory Users and Groups

## Objective

Create and organize Active Directory user accounts and security groups to represent departments within the bennylab.local environment and provide centralized management of user access.

## User Organization

User accounts were organized into departmental Organizational Units (OUs) within the BennyLab structure.

The following departmental OUs were created:

- Accounting
- HR
- IT
- Management
- Sales

## Departmental Users

User accounts were created to simulate employees across multiple departments within the organization. Each user was placed in the appropriate departmental OU.

| Department | User |
|---|---|
| Accounting | Emily Davis |
| HR | Sarah Johnson |
| IT | Alex Rodriguez |
| Management | David Miller |
| Sales | Mike Chen |

## Security Groups

Department-based security groups were created to manage access to resources without assigning permissions directly to individual user accounts.

| Security Group | Department |
|---|---|
| Accounting | Accounting |
| HR | Human Resources |
| IT | Information Technology |
| Management | Management |
| Sales | Sales |

Users were added to the security group associated with their department. These groups are used throughout the lab to control access to departmental file shares and Group Policy resources.

<img width="537" height="335" alt="image" src="https://github.com/user-attachments/assets/a54ce496-a0d0-40d3-980f-870123164100" />


<img width="697" height="276" alt="image" src="https://github.com/user-attachments/assets/f80d0996-7a15-4239-b612-fe63e1729b49" />

The Accounting security group is shown above as an example, with Emily Davis assigned as a member based on her departmental role.
