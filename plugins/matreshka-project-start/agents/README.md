# Specialist agents

These role contracts are the canonical source of truth for the Matreshka Project Start workflow. They are deliberately tool-neutral: an adapter may translate the relevant role into a Codex instruction, a Claude Code subagent, an Antigravity agent, or a Pi agent definition.

Use a role only when its bounded responsibility helps. Do not delegate merely to create more agents. The orchestrator keeps the approved specification and plan; specialist agents return short evidence-based handoffs rather than raw logs or a hidden chain of reasoning.

Every role must obey the project `AGENTS.md` files, the current user approval, and the permission gate in `workflows/permissions.md`.

## Handoff format

```text
Role:
Scope:
Status: PASS | FAIL | BLOCKED | NEEDS_DECISION
Verified facts:
Evidence: commands, files, screenshots or URLs actually used
Risks or gaps:
Changes made: none | exact paths
Recommended next action:
```
