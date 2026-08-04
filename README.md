# Matreshka Project Start

Matreshka Project Start is a Codex plugin for beginning a software project in a controlled way. It works with a new folder or an existing repository and does not assume a particular stack.

It helps a person and an AI coding agent move through one predictable path:

```text
discover the project → agree the setup → make approved changes → verify readiness
```

The plugin does not create a generic application template. It first learns the actual project structure, protects existing work, and distinguishes verified facts from assumptions.

## Included skills

| Skill | What it does |
| --- | --- |
| `project-discovery` | Safely maps a repository, its stack, instructions, quality commands, and risks. |
| `project-start` | Coordinates discovery, a short intake, and a bounded setup proposal. |
| `project-setup` | Applies only the specific project files the user has explicitly approved. |
| `project-readiness` | Checks that the agreed project foundation is present and usable. |

## Safety model

- Discovery is read-only by default.
- No dependency installation, source-code changes, database changes, deployment, Git commit, push, or secret access occurs without separate permission.
- Existing documentation and agent instructions are preserved and extended only when approved.
- The plugin never invents project commands, architecture, owners, URLs, or environment values.

## Example prompts

```text
Use Matreshka Project Start. Inspect this project in read-only mode and show a safe setup proposal. Do not change files.
```

```text
Use project-setup. I confirm the setup scope: create AGENTS.md and docs/project only. Do not alter code, CI, Git, or deployment settings.
```

## Repository layout

The plugin is stored under `plugins/matreshka-project-start`. The repository also contains a Codex marketplace manifest in `.agents/plugins/marketplace.json`.

## License

MIT. See [LICENSE](LICENSE).
