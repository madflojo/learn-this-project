# learn-this-project

An agent skill for triaging unfamiliar repositories quickly and producing an
evidence-backed project summary.

The canonical skill identifier is `learn-this-project`. The repository is
structured so it can be installed directly with GitHub CLI or copied manually
into an agent skill directory.

## What the skill does

The `learn-this-project` skill helps an agent:

- map a repository quickly without pretending to be exhaustive
- separate direct evidence from inference
- report architecture, tooling, and conventions with file-backed support
- handle ambiguity explicitly instead of guessing
- use deliberate sampling for large repositories
- say "insufficient evidence" when the repo does not support a strong claim

This is intended for the first pass on an unfamiliar codebase, before deeper
task-specific investigation begins.

## Repository layout

```text
skills/
  learn-this-project/
    SKILL.md
    assets/
      report-template.md
    references/
      EVIDENCE.md
      OUTPUT.md
      WORKFLOW.md
```

The main prompt lives at `skills/learn-this-project/SKILL.md`.
Supporting docs live under `references/`, and the structured report template
lives under `assets/`.

## Installing the skill

Primary path: install from GitHub CLI with `gh skill install`.

```bash
gh skill install madflojo/learn-this-project
```

Optional: pin to a tag or commit for reproducible installs:

```bash
gh skill install madflojo/learn-this-project@v1.0.0
gh skill install madflojo/learn-this-project@<commit-sha>
```

Fallback path: manually copy `skills/learn-this-project/` into either:

- `.agents/skills/` in a repository
- `~/.agents/skills/` for a user-level install

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution and release guidance.

## License

Licensed under [Apache-2.0](LICENSE).
