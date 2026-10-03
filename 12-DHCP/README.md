## DHCP Server Configuration

## Objective

Configure Windows Server 2022 to provide centralized DHCP services for the
bennylab.local environment and automatically provide IPv4 network
configuration to clients on the lab network.

## Configuration

### DHCP Server
| Setting | Value |
|---|---|
| Server | BEN-SERVER1 |
| Server IP | 192.168.8.176 |
| Domain | bennylab.local |
| Network | 192.168.8.0/24 |

### Corporate LAN Scope

| Setting | Value |
|---|---|
| Scope Name | Corporate LAN |
| Address Range | 192.168.8.100 - 192.168.8.200 |
| Subnet Mask | 255.255.255.0 |
| Lease Duration | 8 Days |

<img width="772" height="332" alt="DHCP layout" src="https://github.com/user-attachments/assets/f3a22730-a141-4e98-bb5c-c982a0b4f3b4" />

### Scope Options

The DHCP scope was configured to provide clients with the lab gateway,
Active Directory DNS server, and domain suffix.

| Option | Value |
|---|---|
| 003 Router | 192.168.8.1 |
| 006 DNS Servers | 192.168.8.176 |
| 015 DNS Domain Name | bennylab.local |

<img width="905" height="278" alt="DHCP Scope Options" src="https://github.com/user-attachments/assets/41543036-58ac-4c6e-8511-193b1c83ba74" />


## Verification

DHCP functionality was verified by confirming that clients successfully
received addresses from the Corporate LAN scope.

<img width="835" height="267" alt="DHCP address leases" src="https://github.com/user-attachments/assets/e16c9d25-c360-43fa-b9a6-bebb5000a137" />


PowerShell was also used to verify the DHCP scope, options, authorization,
service status, and network binding.

```powershell
Get-DhcpServerInDC
Get-Service DHCPServer
Get-DhcpServerv4Binding
Get-DhcpServerv4Scope
Get-DhcpServerv4OptionValue -ScopeId 192.168.8.0
Get-DhcpServerv4Lease -ScopeId 192.168.8.0
