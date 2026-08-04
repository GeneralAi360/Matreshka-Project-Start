# Codex adapter

Codex discovers `AGENTS.md` files by directory scope. The root `AGENTS.md` should contain the concise repository map and safety boundaries; deeper `AGENTS.md` files add only area-specific rules and take precedence inside their directories.

Use the canonical contracts in `agents/` and workflows in `workflows/` as the source when a task calls for a specialist role. Do not duplicate the full role text into every project instruction.

Recommended prompts:

```text
Use project-discovery. Inspect this repository read-only and return the required report.
```

```text
Use the repo-scout contract, then prepare a specification. Do not modify files.
```
