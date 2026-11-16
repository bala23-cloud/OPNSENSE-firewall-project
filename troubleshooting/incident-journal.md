# Troubleshooting and incident journal

## LAB-001 — Kali-to-Ubuntu HTTP timeout (unresolved, historical topology)
**Context:** Kali (`KALI_LAB_IP`) attempted TCP/80 to Ubuntu (`UBUNTU_SERVER_IP`) during Day 3. The real private lab addresses are masked in this public repository.

**Observed:** A request to `http://UBUNTU_SERVER_IP:80/` timed out after approximately five seconds.

**Related logs:** OPNsense OPT1 showed inbound ICMP blocks from Kali to Ubuntu labeled `Default deny / state violation rule`. Those are ICMP entries, not TCP/80 evidence.

**Investigations discussed:** inspect listener, route, interface assignment, live logs and packet captures. A conclusive packet path and HTTP block reason were **not established**.

**Resolution:** Unresolved. Work paused by design; a simpler Windows-outside / shared-internal-LAN topology is planned. Do not label the issue fixed.

**Next validation:** measure actual routes and adapters after redesign; establish a working baseline before adding NAT/filter rules.

## Journal template
Date/time · business impact · topology version · exact command (with addresses masked) · observed output · hypothesis · test performed · evidence path · confirmed root cause · fix · rollback · lesson.
