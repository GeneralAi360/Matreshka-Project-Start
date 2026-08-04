# Permission gates

The project owner selects the scope. Absence of a prohibition is not permission.

| Action | Default | Explicit approval must name |
| --- | --- | --- |
| Read source, docs, Git status and safe config | Allowed for discovery | Project root if ambiguous |
| Create or change project docs/instructions | Blocked | Exact paths or bounded setup scope |
| Change application/test/CI code | Blocked | Feature or approved plan scope |
| Install, update or remove dependencies | Blocked | Package and reason |
| Local migration or destructive test setup | Blocked | Database/environment and rollback/restore boundary |
| Stage, commit, push, branch or PR | Blocked | Repository, branch and Git scope |
| External API action, email, payment, storage mutation | Blocked | System, exact action and target boundary |
| Staging deployment | Blocked | Environment and revision |
| Production deployment or migration | Blocked | Environment, revision, approval, health check and rollback |

Never request or reproduce secrets in chat, source code, documentation, command output or Git history. Use the project's approved environment secret mechanism.
