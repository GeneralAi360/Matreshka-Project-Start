---
name: project-setup
description: Apply an explicitly approved Matreshka Project Start setup to a project. Use only after the user has confirmed the exact files and edits that may be made.
---

# Project Setup

Apply only the project foundation the user has explicitly approved. This skill does not decide the scope itself.

## Preconditions

Before editing, confirm all of the following:

1. The intended project root is known.
2. Read-only discovery has identified relevant project instructions and conventions.
3. The user named the exact paths to create or amend.
4. No existing file will be overwritten, moved, or replaced without specific approval.

If any point is missing, stop and produce `SETUP_PROPOSED`, with the smallest decision required.

## Allowed default scope

When explicitly approved, create or minimally update only these project-foundation paths:

| Path | Content standard |
| --- | --- |
| `AGENTS.md` | Concise factual map; link to longer documents instead of duplicating them. |
| `docs/project/PROJECT_PROFILE.md` | Verified facts, commands, boundaries, and clearly marked unknowns. |
| `docs/project/DECISIONS.md` | Date, decision, source, and any unresolved consequence. |
| `docs/specs/` and `docs/plans/` | Empty folders only when the project actually needs this documentation workflow. |
| `docs/runs/` | Only when multi-session evidence or handoffs are needed. |

Do not create a generic application, change source code, alter CI, install packages, change databases, configure deployment, read secrets, or perform Git actions unless separately approved.

## Execution

1. Re-read relevant project instructions and check the current Git state.
2. Create only approved paths.
3. Preserve existing sources of truth and bridge to them rather than competing with them.
4. Mark anything unverified as `Unknown` or `Needs confirmation`.
5. Run only existing, non-mutating checks relevant to the changed documentation or configuration. Do not install validation tools.
6. Do not stage, commit, push, create a pull request, or deploy unless the user separately asks.

## Handoff

```text
Status: SETUP_COMPLETE | SETUP_PROPOSED | BLOCKED
Changed:
Not changed:
Validation:
Open decisions:
Recommended next action:
```
