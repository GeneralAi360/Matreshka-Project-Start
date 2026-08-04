---
name: project-readiness
description: Verify whether a project has the agreed foundation for safe AI-assisted development. Use after project setup or when a user wants a readiness check without changing files.
---

# Project Readiness

Verify the project against its agreed scope. This skill is read-only unless the user separately approves a repair.

## Checks

1. Read applicable repository instructions before inspecting other files.
2. Confirm the project root and Git state.
3. Verify each approved setup file exists and matches the project rather than generic assumptions.
4. Check that documented validation commands actually exist in the repository's own configuration. Do not run unavailable or invented commands.
5. Check that known safety boundaries are stated when relevant: secrets, authentication, data isolation, external actions, databases and migrations, deployments, and environment separation.
6. Check that no setup document claims facts that cannot be verified from the repository or a confirmed user decision.
7. Run only relevant, existing, non-mutating checks if they are safe to run in the current environment.

## Interpretation

- `READY`: the agreed foundation exists, is consistent with the project, and has no material known gap.
- `READY_WITH_GAPS`: usable, but important unknowns or deferred decisions remain.
- `NOT_READY`: a missing or contradictory instruction, unsafe boundary, or failed applicable check blocks the agreed workflow.

This is not a security audit and it does not certify that production systems are secure.

## Report

```text
Status: READY | READY_WITH_GAPS | NOT_READY | BLOCKED
Verified:
Gaps and risks:
Validation:
Not changed:
Recommended next action:
```
