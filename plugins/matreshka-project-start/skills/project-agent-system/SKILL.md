---
name: project-agent-system
description: Propose or install Matreshka Project Start specialist-agent contracts in a repository. Use when a user wants clear roles such as repo-scout, implementer, test-runner, browser-checker, reviewer, security-reviewer, docs-maintainer or deployer.
---

# Project Agent System

Install a small, useful agent system around a project — not a decorative folder of roles.

## Default: inspect, then propose

First run read-only discovery. Determine the project risk level, current instructions, tests, deployment boundaries and the coding environments that will use the project. Do not create agent files merely because the plugin contains them.

Choose the smallest role set:

| Project need | Recommended roles |
| --- | --- |
| Small local frontend | repo-scout, implementer, test-runner, reviewer |
| Next.js/React app with accounts or API | Add browser-checker and security-reviewer |
| Product with regular changes | Add spec-writer, planner and docs-maintainer |
| Staging/production delivery | Add deployer and deploy-verifier after a separate infrastructure decision |

## Proposal and approval

Before writing, show the exact paths, selected roles, target coding environments and what each role can and cannot do. The canonical role contracts in this plugin may be copied into a project only after an approval naming those paths.

Never grant access to Git, browser profiles, secrets, SSH, SFTP, production databases or deployment merely by installing a role definition. Keep `workflows/permissions.md` as the shared permission model.

## Result

Return:

```text
Status: AGENT_SYSTEM_PROPOSED | AGENT_SYSTEM_COMPLETE | BLOCKED
Selected roles:
Created or changed:
Permissions intentionally not granted:
Evidence:
Open decisions:
Recommended next action:
```
