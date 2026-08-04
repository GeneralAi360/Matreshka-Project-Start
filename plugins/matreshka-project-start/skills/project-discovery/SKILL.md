---
name: project-discovery
description: Safely inspect a new or existing software project before any setup work. Use when the user asks what a repository contains, which stack it uses, how it is organized, which quality commands exist, or whether it is safe to begin AI-assisted development.
---

# Project Discovery

Create an evidence-based map of a software project without changing it. This skill is read-only.

## Guardrails

Do not modify, stage, commit, push, deploy, install, upgrade, or delete anything. Do not open or print `.env` files, credentials, private keys, production dumps, or secrets.

If the project folder is unclear, ask the user to open it or give its path. Do not search parent folders for unrelated repositories.

## Inspection order

1. Read every applicable `AGENTS.md` and repository instruction before inspecting source files.
2. Confirm the project root, Git state, current branch, and configured remotes.
3. Detect the actual stack from manifests, lockfiles, language files, framework configuration, containers, database schema, and deployment configuration.
4. Identify existing commands from project manifests, Makefiles, task runners, CI workflows, and documentation. Never invent a command.
5. Find existing agent context and documentation, including `README.md`, `CONTRIBUTING.md`, `AGENTS.md`, `CLAUDE.md`, `.github/`, `docs/`, and editor rules.
6. Inspect the smallest useful set of source, tests, CI configuration, and environment-variable examples.
7. Identify boundaries: authentication, data, payments, integrations, deployments, migrations, and user-provided content.

## Required report

Return only verified observations in this form:

```text
Status: DISCOVERED | BLOCKED
Project state
- Root and repository state:
- Stack actually detected:
- Existing quality commands:
- Documentation and agent instructions:
- Deployment and data boundaries:
- Risks, inconsistencies, and unknowns:

Recommended next action:
```

Mark missing or unverified information explicitly as `Unknown` or `Needs confirmation`. Scale the investigation to the project: do not perform an architecture audit for a small static site, but inspect boundaries more closely for projects handling users, payments, sensitive data, production databases, or external actions.
