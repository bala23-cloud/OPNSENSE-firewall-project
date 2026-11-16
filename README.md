# OPNsense Enterprise Firewall Engineering Lab

**15-day practical network security and firewall engineering project** | VirtualBox · OPNsense · Kali Linux · Ubuntu · Windows

## Project overview
I am building a controlled virtual enterprise network to understand how firewalls enforce security boundaries. The project records the reason for each rule, the packet path it affects, the tests performed, failures encountered and the evidence collected.

**Documentation status:** The full Day 1–15 roadmap and challenge guides are documented. Practical execution is tracked separately: Days 1–2 have been covered, Day 3 remains in progress, and Day 4 has an alias and TCP/80 pass rule configured while traffic verification is pending. Days 5–15 are written as detailed challenge guides; they are not claimed as completed lab work.

## Objectives
- Build a reproducible virtual network with distinct outside and inside trust zones.
- Configure and validate firewall rules, state tracking, NAT, aliases and segmentation.
- Learn DHCP/DNS security, VPN, high availability, IDS/IPS and monitoring.
- Troubleshoot traffic using routes, states, logs and packet captures.
- Keep configuration, test observations and limitations clear and reproducible.

## Proposed architecture
```text
Physical Windows host (outside test client)
              |
    OPNsense outside-facing interface
        [routing / firewall / NAT]
    OPNsense inside-facing interface
              |
        Internal virtual LAN
           /       \
     Kali Linux   Ubuntu HTTP server
```
Kali and Ubuntu on the same Layer-2 LAN can communicate directly without crossing OPNsense. Their east-west traffic is not protected by OPNsense merely because it is the default gateway. Windows-to-internal traffic must be deliberately routed through OPNsense without a bypass path. The proposed topology is not yet deployed or validated. All IPs in this repository are lab examples or redacted.

## 15-day progress
| Day | Focus | Documentation / practical status |
|---|---|---|
| 01 | Firewall fundamentals and logging | Concepts and initial lab work covered; screenshots pending |
| 02 | Rule matching, order and conflicts | Concepts and lab work covered; screenshots pending |
| 03 | Protocol rules and stateful inspection | In progress; timeout and block observations recorded |
| 04 | IP aliases and alias-based policy | Alias and TCP/80 pass rule configured; curl verification pending |
| 05 | Network segmentation and VLANs | Challenge guide documented; lab validation not recorded |
| 06 | Outbound NAT | Challenge guide documented; lab validation not recorded |
| 07 | Port forwarding and inbound access | Challenge guide documented; lab validation not recorded |
| 08 | DHCP and DNS security | Challenge guide documented; lab validation not recorded |
| 09 | Firewall log analysis and monitoring | Challenge guide documented; lab validation not recorded |
| 10 | VPN and remote access | Challenge guide documented; lab validation not recorded |
| 11 | High availability and failover | Challenge guide documented; lab validation not recorded |
| 12 | IDS/IPS with Suricata | Challenge guide documented; lab validation not recorded |
| 13 | Advanced firewall policies | Challenge guide documented; lab validation not recorded |
| 14 | Troubleshooting and security audit | Challenge guide documented; lab validation not recorded |
| 15 | Enterprise firewall capstone | Challenge guide documented; capstone execution not recorded |

See [the complete 15-day roadmap](ROADMAP.md) and [daily challenge notes](challenges/).

## Repository navigation
- [Architecture](architecture/README.md) — topology, IP planning and packet paths
- [Configuration](configuration/README.md) — policies, aliases, NAT and change control
- [Challenges](challenges/README.md) — day-by-day challenge guides
- [Troubleshooting](troubleshooting/incident-journal.md) — observed problems and investigation
- [Evidence](evidence/README.md) — evidence notes and capture guidance
- [Final report](final-report/README.md) — capstone report structure
- [LinkedIn posts](linkedin-posts/README.md) — project communication

## How progress is reported
A guide being written does not mean the practical has been performed. Each day distinguishes documentation, configuration, observed results and verified results. A timeout alone does not identify the cause; a logged ICMP block does not prove HTTP was blocked. Only mark a test verified after repeating it and recording the actual output.

## Safety
This is an authorized isolated homelab. Do not expose test servers to public networks. Redact credentials, public IPs, host identifiers and sensitive network details before publishing.

## Current next step
Continue Day 4 verification: test Kali-to-Ubuntu HTTP access through the alias-based rule, inspect the matching firewall log/state, then test a controlled block. Record the actual output before changing the status.
