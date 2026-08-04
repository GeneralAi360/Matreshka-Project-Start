# Feature delivery workflow

This is the default end-to-end workflow. It scales down for a tiny copy change and scales up for authorization, payments, migrations, external APIs or production work.

```text
Request
→ repo-scout (read-only)
→ approved specification
→ planner
→ approved plan
→ implementer: RED → minimal change → GREEN
→ test-runner and browser-checker where applicable
→ reviewer and security-reviewer where applicable
→ docs-maintainer
→ explicit Git handoff
→ explicit deployment handoff
```

## Required boundaries

- A specification describes the goal and acceptance criteria; a plan describes files, order, tests and risks. Do not merge the two silently.
- Tests and a green build are evidence, not an independent review.
- Documentation follows verified behavior; it never retroactively changes the specification.
- Commit, push, PR, migration, staging and production release each need an explicit instruction from the project owner.
- A failed check may not be bypassed by loosening assertions, removing the scenario or changing unrelated configuration.

## Minimal handoff to the owner

At every pause, report: current status, verified evidence, changed paths, remaining risks, approvals needed and the exact next action.
