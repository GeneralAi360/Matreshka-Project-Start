---
name: project-runtime-setup
description: Design or apply a safe local development runtime convention for start, stop, status and logs. Use when an AI agent needs reliable local process visibility without guessing how services are running.
---

# Project Runtime Setup

Make local application state observable through verified project commands and bounded scripts. This is not a production deployment skill.

## Discovery first

Read-only inspect the existing runtime commands, package manager, operating systems to support, service topology, existing logs, ports, containers and test setup. Do not invent `npm run dev:start`, use `taskkill`, kill a process or add scripts until the owner approves a concrete design.

## Design rules

- Prefer existing commands and platform-native process management.
- Any start/stop script must record only its own process identity; it must never kill by broad process name or port without an explicit project boundary.
- Logs must exclude secrets and be ignored by Git.
- A status command should report evidence, not claim a service is healthy merely because a PID file exists.
- Separate local development from test, staging and production. E2E destructive setup must require a dedicated test environment and explicit gate.

## Approval scope

Before creating scripts or changing `package.json`, list the exact files, supported OSes, ports, logs, commands and stop behavior. Dependency installation, container changes, cloud access and remote actions are separate approvals.

## Result

```text
Status: RUNTIME_PROPOSED | RUNTIME_COMPLETE | BLOCKED
Verified existing commands:
Proposed or changed files:
Safety boundaries:
Validation:
Recommended next action:
```
