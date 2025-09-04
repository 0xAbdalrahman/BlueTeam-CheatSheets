# 🌐 Windows Networking Cheat Sheet (PowerShell)

## TCP Connections
#### Show all active TCP connections
`Get-NetTCPConnection | Select-Object LocalAddress, RemoteAddress, State`

#### Show TCP connections by Process ID (PID)
`Get-NetTCPConnection | Where-Object { $_.OwningProcess -eq 1234 }`

#### Show TCP connections for a specific local port (e.g., 80)
`Get-NetTCPConnection -LocalPort 80`

#### Show detailed TCP connections (with ports, state, PID)
`Get-NetTCPConnection | Format-Table LocalAddress, LocalPort, RemoteAddress, RemotePort, State, OwningProcess -AutoSize`
<br>
## **UDP Endpoints**

`Get-NetUDPEndpoint` – Shows **UDP** listeners (UDP doesn’t establish connections like TCP, so it shows bound ports).

#### Show all UDP endpoints:
`Get-NetUDPEndpoint`

#### Show endpoints with selected fields:
`Get-NetUDPEndpoint | Select-Object LocalAddress, LocalPort, OwningProcess`

#### Filter for a specific UDP port (e.g., 53):
`Get-NetUDPEndpoint | Where-Object { $_.LocalPort -eq 53 }`

