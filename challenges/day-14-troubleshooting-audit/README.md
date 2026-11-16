# Day 14 — Troubleshooting and Security Audit

**Guide status:** Documentation complete. Practical validation has not yet been recorded.

## Scenario
A department reports that an internal service is unreachable. The engineer must identify the cause without making several unrelated configuration changes.

## Objective
Use a repeatable troubleshooting method and review the firewall configuration for unnecessary access.

## Lab activities
- Confirm interface status, IP address, subnet mask and default gateway.
- Check routes and verify the forward and return paths.
- Confirm that the destination service is listening on the expected port.
- Check DNS resolution where hostnames are involved.
- Review NAT mappings, firewall rules, states and relevant logs.
- Review broad rules and remove or narrow unnecessary access only after understanding dependencies.

## Validation approach
Reproduce a known allowed flow and a known blocked flow. Record the symptom, commands used, observations, likely cause, change made and retest result. Confirm that unrelated connectivity still works after the fix.

## Key lesson
Follow the packet path one step at a time. Changing multiple settings together makes the root cause harder to identify.

## Practical notes
Add real command output and redacted screenshots after completing the investigation. Do not claim a root cause until the observations support it.
