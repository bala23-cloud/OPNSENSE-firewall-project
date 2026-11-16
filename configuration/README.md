# Configuration register

Configuration snapshots and screenshots will be added only after deployment and validation.

## Address and identity redaction
Use role placeholders in all public examples:
- Kali client: `KALI_LAB_IP`
- Ubuntu server: `UBUNTU_SERVER_IP`
- OPNsense interface: `FIREWALL_INTERFACE_IP`
- Default gateway: `LAB_GATEWAY_IP`

Never publish real private/public IP addresses, MAC addresses, public DNS identifiers tied to the lab, credentials, VPN keys or raw configuration backups. Keep real values in a private local lab note. Before publishing screenshots or packet captures, blur or replace every address and identifying value.

## Policy documentation format
| Rule ID | Interface/direction | Action | Protocol | Source | Destination | Port | Business justification | Verification |
|---|---|---|---|---|---|---|---|---|

## NAT documentation format
| NAT ID | External interface/address:port | Internal destination:port | Associated filter rule | Test client | Observed result |
|---|---|---|---|---|---|

## Change-control notes
Record the original rule, the change, expected outcome, actual outcome, rollback action and evidence reference. Avoid publishing raw firewall configuration exports containing secrets or sensitive identifiers.
