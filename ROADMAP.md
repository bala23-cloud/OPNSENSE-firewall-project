# 15-Day OPNsense Firewall Engineering Roadmap

This roadmap is fully documented from Day 1 through Day 15. Every day has a scenario, objective, lab activities, validation approach and key learning outcome. The roadmap being documented does not mean every practical has already been executed. Actual lab progress is tracked in the main README and each daily note.

| Day | Challenge | Main deliverable |
|---|---|---|
| 01 | Firewall fundamentals: interfaces, PASS/BLOCK rules and logging | Basic policy understanding and initial rule tests |
| 02 | Rule matching, source/destination, order and conflicts | Rule decision matrix and matching tests |
| 03 | Protocol/port rules and stateful inspection: ICMP, HTTP and SSH | Protocol-specific connectivity tests |
| 04 | IP aliases and alias-based firewall policies | Reusable host aliases and policy validation |
| 05 | Network segmentation and VLANs | Segmentation design and permitted/denied traffic matrix |
| 06 | Outbound NAT and address translation | NAT configuration review and before/after packet-path analysis |
| 07 | Port forwarding and inbound access control | Controlled external-to-internal service test |
| 08 | DHCP and DNS security | Address assignment and name-resolution validation |
| 09 | Firewall log analysis and monitoring | Investigation of allowed and blocked events |
| 10 | VPN: OpenVPN/IPsec and remote access | Tunnel, route and access-policy validation |
| 11 | High availability with CARP and configuration synchronization | Primary/backup design and failover test where supported |
| 12 | IDS/IPS with Suricata | Detection validation and prevention assessment |
| 13 | Advanced policies: floating rules, schedules and policy order | Policy review and rule-interaction test matrix |
| 14 | Troubleshooting and security audit | Repeatable troubleshooting report and regression checks |
| 15 | Enterprise firewall capstone | Final architecture, policy review, test report and project presentation |

## Daily workflow
1. Understand the business scenario and security objective.
2. Record the current topology, interfaces, routes and prerequisites.
3. Make one controlled configuration change at a time.
4. Test both the expected allowed traffic and the expected blocked traffic.
5. Check firewall logs, states and packet path.
6. Record the actual result, troubleshooting and key lesson.
7. Mark a practical verified only when its test evidence exists.

## Lab constraints
Some topics require extra virtual adapters, VLAN support, a second firewall VM or additional memory. If the current VirtualBox setup cannot support a task, document the limitation and complete the design/research portion without claiming a successful deployment. Preserve the existing working network configuration unless a specific day's change is planned and backed up.
