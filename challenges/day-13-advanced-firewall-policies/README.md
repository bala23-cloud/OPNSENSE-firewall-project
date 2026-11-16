# Day 13 — Advanced Firewall Policies

**Guide status:** Documentation complete. Practical validation has not yet been recorded.

## Scenario
The company needs predictable firewall behaviour as its policy set grows. Rules must remain understandable and avoid accidentally allowing traffic that should be denied.

## Objective
Understand floating rules, interface rules, schedules, direction and rule evaluation order.

## Lab activities
- Review interface-specific and floating rules and when each is appropriate.
- Understand the effect of direction and the quick option.
- Plan a time-based rule using a schedule.
- Document the intended rule order and the business reason for each rule.
- Avoid adding broad allow rules just to make a test pass.

## Validation approach
Create a rule decision table with source, destination, protocol, port, interface and expected action. Test matching and non-matching traffic, then inspect the firewall log and state table to confirm which rule handled each flow.

## Key lesson
A firewall rule cannot be judged in isolation. Its interface, direction, order and evaluation behaviour all affect the result.

## Practical notes
Record the actual configuration and test output after performing the lab. If the current topology cannot support a test, document the limitation rather than reporting a successful result.
