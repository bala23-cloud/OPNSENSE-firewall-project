# Day 07 — Port Forwarding and Inbound Access

**Guide status:** Documentation complete. Practical validation has not yet been recorded.

## Scenario
A small company needs to strengthen its network security while keeping business services available. This day's lab focuses on port forwarding and inbound access.

## Objective
Publish one controlled internal service through a specific external port.

## Lab plan
Use an isolated test service; configure a port-forward and its associated filter rule; restrict source addresses where practical.

## How it will be validated
Test from a genuinely separate outside network; verify service listener, route, NAT mapping, filter rule, return path and logs.

## Key lesson
A port forward is not proof of reachability; the full packet path and return path must work.

## Notes
This challenge will be marked completed only after the configuration has been performed and the relevant tests have been observed. Add actual commands, screenshots, log extracts and troubleshooting notes after the practical. Do not publish credentials or sensitive network details.
