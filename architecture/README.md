# Architecture and traffic-flow plan

## Target design (not yet deployed)
Windows physical host acts as an outside test client. OPNsense separates the outside-facing test network from an internal VirtualBox LAN containing Kali and Ubuntu.

```text
Windows (outside) -- OPNsense WAN | firewall / NAT | OPNsense LAN -- internal switch -- Kali + Ubuntu
```

### Design decisions
- Use separate virtual networks for outside and inside; do not attach Windows directly to the internal LAN for the inbound firewall demonstration.
- Kali and Ubuntu share one Layer-2 LAN. Direct Kali↔Ubuntu traffic does not necessarily traverse OPNsense.
- Select an outside-facing VirtualBox adapter mode that lets the physical Windows host reach OPNsense while keeping lab services isolated.
- Verify gateway, subnet, routes, listening sockets, return path and policy before claiming any inbound NAT success.
- Port forwarding alone is insufficient unless the associated filtering policy permits the intended traffic.
- Do not treat OPNsense's own successful HTTP request as proof of Windows→LAN reachability.

## Address inventory (masked)
Historical lab observations used private lab addresses. They are intentionally not reproduced in this public repository:
- Kali test client: `KALI_LAB_IP`
- Ubuntu HTTP server: `UBUNTU_SERVER_IP`
- OPNsense interface/gateway values: `FIREWALL_INTERFACE_IP`

These labels are placeholders, not literal addresses. The current addressing plan must be measured again after the topology is redesigned. Keep the real values only in a private local lab note.

## Required evidence
VirtualBox adapter screenshots, OPNsense interface assignments, Windows routes, Kali/Ubuntu routes, firewall/NAT rules, and two-sided packet captures. Blur or replace all IP addresses in screenshots and terminal output before committing them.
