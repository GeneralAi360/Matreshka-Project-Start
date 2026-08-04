# Matreshka Project Start

**Matreshka Project Start** prepares a new or existing repository for predictable AI-assisted development. It is a project-foundation plugin, not a Vue, Next.js, or NestJS application template.

It supports the same working logic across Codex, Claude Code, Antigravity and optional Pi:

```text
read-only discovery → approved specification → implementation plan
→ focused change + tests → independent review → verified handoff
```

The plugin does not make project changes just because an agent was asked to inspect or explain something. Every material write has an approval boundary.

## What is inside

### Seven skills

| Skill | Purpose |
| --- | --- |
| `project-discovery` | Read-only map of the repository, stack, commands, instructions and risks. |
| `project-start` | Coordinates discovery, a short intake and a bounded setup proposal. |
| `project-setup` | Applies only an explicitly approved project foundation. |
| `project-readiness` | Read-only readiness check after setup. |
| `project-agent-system` | Proposes or installs the approved specialist-agent contracts. |
| `project-runtime-setup` | Proposes or installs safe local run, status and log conventions. |
| `project-adapter-setup` | Adds thin, optional adapters for Codex, Claude Code, Antigravity or Pi. |

### Specialist agent contracts

The `agents/` folder defines what each role may read, change, run and return. The contracts are tool-neutral, so one workflow can be used with different coding environments.

| Role | Default authority |
| --- | --- |
| `repo-scout` | Read-only repository investigation. |
| `spec-writer` | Requirements and acceptance criteria; no code. |
| `planner` | Implementation plan; no code. |
| `implementer` | Approved scoped code and tests; no Git or deployment. |
| `test-runner` | Runs declared checks and reports evidence; no fixes. |
| `browser-checker` | Browser-only functional check; no source changes. |
| `reviewer` | Independent specification and diff review. |
| `security-reviewer` | Auth, permissions, input, secrets and external-action review. |
| `docs-maintainer` | Documentation only, after GREEN and review. |
| `deployer` | Explicitly approved environment release only. |
| `deploy-verifier` | Read-only smoke and health verification. |

The files are **instructions and handoff contracts**. They do not magically grant a coding tool access to a browser, server, GitHub or production. The chosen environment and the project owner must separately configure tools and permissions.

## Structure

```text
plugins/matreshka-project-start/
├── agents/                  # Specialist role contracts
├── adapters/                # Thin integration guidance for each coding environment
├── skills/                  # User-invoked Project Start workflows
├── templates/               # Stack-neutral project files created only after approval
├── workflows/               # Feature delivery and permission gates
└── .codex-plugin/plugin.json
```

## Recommended first use

Open the intended repository in your coding environment and run:

```text
Use Matreshka Project Start / project-discovery.
Inspect this project in read-only mode and show the exact setup proposal.
Do not change files.
```

After you approve the resulting file list, use `project-setup`, then (when needed) `project-agent-system`, `project-runtime-setup`, and `project-adapter-setup`.

## Safety model

- Discovery, planning, review and verification are read-only by default.
- No dependency installation, source-code change, database migration, Git action, deployment, or secret access occurs without separate permission.
- `docs-maintainer` runs only after tests are GREEN and independent review is complete.
- Deployment requires the selected environment, release reference, rollback method and explicit approval.

## License

MIT. See [LICENSE](LICENSE).
