---
name: project-start
description: Prepare a new or existing software project for safe, predictable AI-assisted development. Use when a user wants to start a project, bring an existing repository into order, set up project instructions, AI-agent context, quality checks, documentation structure, or GitHub-ready development practices for Codex, Claude Code, Cursor, Antigravity, or Pi.
---

# Matreshka Project Start

Set up the working foundation around a project, not a generic application template. Preserve the project's stack, conventions, history, and existing work. Keep the result usable with different AI coding environments.

## Operating rule

Start in **read-only discovery** unless the user explicitly authorizes project-local changes. Never treat a request to inspect, explain, plan, or design as permission to change files.

Never install or upgrade dependencies; alter application, database, infrastructure, or CI code; read, print, copy, or commit secrets; stage, commit, push, create a pull request, deploy, or run a remote migration; or overwrite or move existing instructions and documentation without explicit approval for that action.

Do not create a second application scaffold inside an existing project. Do not introduce a framework because the project is not Next.js, React, or NestJS. Work with the stack actually discovered.

## 1. Classify the request

| Situation | Default first outcome |
| --- | --- |
| New project | Foundation proposal and an intake interview |
| Existing project | Read-only project map and compatibility plan |
| Existing project with a problem | Evidence of the problem and a focused repair proposal |
| Project template requested | Hand off to specification and implementation workflow |

If the root is unclear, ask the user to open the intended folder or provide its path.

## 2. Discover before proposing writes

Use `project-discovery` or perform its read-only procedure. Confirm repository state, actual stack, commands, instructions, source and test areas, CI, environment examples, and data or deployment boundaries. Do not turn a guess into a project fact.

## 3. Ask only decision-critical questions

Ask only for information that cannot be learned safely from the project:

1. What does the project do and who uses it?
2. Is it new work, a redesign, or a continuation?
3. Which environments are in scope: local, preview, staging, or production?
4. Which external systems matter?
5. What must never change automatically?
6. Does the user want guided approvals, assisted work, or autonomous local work in an agreed scope?

Never ask for API keys, passwords, tokens, private URLs, or customer data.

## 4. Produce a bounded proposal

Separate verified existing material from proposed additions. Include the workflow, files to create or minimally update, exact existing validation commands, prerequisites needing a decision, later permissions, and exclusions.

Use the following layout only when it does not conflict with existing conventions:

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | Concise project map, safety boundaries, commands, and working rules |
| `docs/project/PROJECT_PROFILE.md` | Verified stack, architecture, environments, commands, and unknowns |
| `docs/project/DECISIONS.md` | Confirmed decisions with dates and sources |
| `docs/specs/` | Approved feature specifications |
| `docs/plans/` | Executable implementation plans |
| `docs/runs/` | Optional multi-session evidence and handoffs |

Do not create `.github/` as decoration. Do not duplicate existing sources of truth. Keep primary project guidance tool-neutral; propose thin adapters only when requested.

Before writing, show the exact file list and wait for approval that names the permitted scope. Then hand off to `project-setup`.

## 5. Handoff format

```text
Status: DISCOVERED | SETUP_PROPOSED | BLOCKED
Verified:
Proposed files:
Validation to run:
Not included:
Open decisions:
Recommended next action:
```
