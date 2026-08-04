---
name: project-adapter-setup
description: Add a thin project adapter for Codex, Claude Code, Antigravity or Pi without duplicating the canonical project workflow. Use when the user wants the same AI-agent process available across different coding environments.
---

# Project Adapter Setup

Connect a project to a requested coding environment while keeping one canonical source of truth.

## Canonical source

The project-level `AGENTS.md`, project profile, context index, role contracts and workflows remain canonical. Environment-specific files must be small bridges that point to those files. Never generate separate, conflicting safety rules for Codex, Claude Code, Antigravity and Pi.

## Supported adapters

- **Codex:** root and nested `AGENTS.md` files by directory scope.
- **Claude Code:** optional concise `CLAUDE.md` bridge, only if requested.
- **Antigravity:** native project-instruction bridge for the installed version, only if requested.
- **Pi:** optional `.pi/agents/` and `.pi/mcp.json`; configure MCPs separately and never store secrets in the repository.

## Process

1. Identify the requested environment and inspect existing instructions read-only.
2. Detect overlap or conflict with current project conventions.
3. Propose the exact bridge files; do not overwrite existing environment instructions.
4. Wait for scope confirmation before writing.
5. Verify that each bridge points back to the canonical project documentation.

## Result

```text
Status: ADAPTER_PROPOSED | ADAPTER_COMPLETE | BLOCKED
Environment:
Canonical source:
Created or changed:
Not configured (tools/credentials/permissions):
Validation:
Recommended next action:
```
