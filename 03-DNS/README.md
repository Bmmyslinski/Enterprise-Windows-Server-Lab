# DNS Server Configuration

## Objective

Configure DNS on Windows Server 2022 to provide name resolution for the bennylab.local Active Directory environment and allow domain clients to resolve internal hostnames.

## DNS Configuration

| Setting | Configuration |
|---|---|
| DNS Server | BEN-SERVER1 |
| DNS Server IP | 192.168.8.176 |
| Domain | bennylab.local |
| Forward Lookup Zone | bennylab.local |
| DNS Integration | Active Directory Integrated |

## Forward Lookup Zone

The bennylab.local forward lookup zone provides DNS name resolution for devices and services within the Active Directory domain.

Host (A) records allow internal hostnames to resolve to their corresponding IPv4 addresses.

| Host | IP Address |
|---|---|
| BEN-SERVER1 | 192.168.8.176 |
| BENMYSLINSK801D | 192.168.8.100 |

<img width="1046" height="302" alt="DNS Forward lookup zone" src="https://github.com/user-attachments/assets/157916ed-218b-45bb-b106-0357c703455a" />

## Verification

DNS functionality was verified from the Windows 11 domain client using nslookup and ping.

The client successfully resolved BEN-SERVER1.bennylab.local to 192.168.8.176 and communicated with the server using its hostname.

```powershell
nslookup BEN-SERVER1.bennylab.local
ping BEN-SERVER1.bennylab.local
```

<img width="641" height="398" alt="ping and nslookup dns" src="https://github.com/user-attachments/assets/a7cbb563-5155-4797-a7fb-ab77addf7620" />

