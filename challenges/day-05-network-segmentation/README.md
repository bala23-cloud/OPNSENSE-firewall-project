# Day 05 — Network Segmentation and VLANs

**Guide status:** Documentation complete. Practical validation has not yet been recorded.

## Scenario
A small company needs to strengthen its network security while keeping business services available. This day's lab focuses on network segmentation and vlans.

## Objective
Separate user, server and management networks; understand inter-VLAN routing and least-privilege access.

## Lab plan
Plan VLAN IDs and subnets; create VLAN interfaces only when the VirtualBox/network setup supports them; assign interfaces; add narrowly scoped inter-network rules.

## How it will be validated
Test permitted and denied traffic between each network, verify routes and inspect firewall logs.

## Key lesson
A VLAN creates a logical boundary, but firewall policy must control traffic between VLANs.

## Notes
This challenge will be marked completed only after the configuration has been performed and the relevant tests have been observed. Add actual commands, screenshots, log extracts and troubleshooting notes after the practical. Do not publish credentials or sensitive network details.
