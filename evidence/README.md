# Evidence collection

Screenshots and packet captures will be added after real tests. There are no fabricated images or results.

Suggested names: `day-04-wan-interface.png`, `day-04-port-forward-rule.png`, `day-04-windows-curl.png`, `day-04-firewall-live-log.png`.

## Redaction before publishing
- Replace private/public IP addresses with role placeholders such as `KALI_LAB_IP`, `UBUNTU_SERVER_IP` and `FIREWALL_INTERFACE_IP`.
- Blur MAC addresses, public IPs, hostnames, usernames, browser tabs and any personal identifiers.
- Remove passwords, API tokens, VPN keys, QR codes and configuration secrets.
- Do not commit raw firewall backups or packet captures unless they have been reviewed and sanitized.

For each artifact record:
- Test date/time and topology version
- Source and destination roles, protocol/port (not real IPs)
- Exact test command with addresses replaced by placeholders
- Expected result
- Actual output and interpretation
- Redactions applied

Never invent evidence. Commit screenshots only after collecting them from the actual lab.
