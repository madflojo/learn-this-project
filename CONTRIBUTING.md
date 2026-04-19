# Contributing

Thanks for contributing to `learn-this-project`.

This repository packages a reusable skill prompt, so the main standard is
clarity under real repo-triage conditions. Changes should make the skill more
reliable, more evidence-driven, or easier to maintain.

## Good contributions

Useful pull requests usually do one of these:

- tighten ambiguous wording in the main skill
- improve the repo-triage workflow
- strengthen evidence and confidence guidance
- fix broken links, formatting, or release metadata
- add small supporting docs only when they materially improve the skill

## Before opening a larger PR

Open an issue or start a discussion first if the change would:

- rename the canonical skill identifier
- change the output contract materially
- weaken the evidence standard or ambiguity handling
- add a new reference document or major workflow section
- introduce host-specific behavior that reduces portability

Small editorial fixes can go straight to a pull request.

## Contribution guidelines

1. Preserve the canonical skill name.
   The published skill identifier is `learn-this-project`. Do not rename the
   directory or metadata unless the repository is intentionally being
   republished under a new identity.

2. Keep the skill evidence-first.
   Prefer guidance that tells the agent how to verify claims from code, config,
   tests, docs, and workflows rather than how to summarize prose alone.

3. Do not overfit to one repo shape.
   Keep guidance generic enough to work across application repos, libraries,
   monorepos, and small utilities.

4. Be explicit about uncertainty.
   If you change the skill's behavior around confidence, ambiguity, or missing
   evidence, update the surrounding sections so the guidance stays aligned.

5. Keep additions small and testable.
   This repository is intentionally lightweight. Add supporting material only
   when it changes the skill's usefulness in practice.

## Pull request expectations

A good pull request is:

- focused in scope
- clear about why the change improves repo triage
- consistent with the published install path and repository docs
- updated anywhere else the same guidance appears

## Commit messages and releases

This repository uses Release Please to generate release pull requests, tags, and
GitHub Releases from conventional commit history.

Preferred commit prefixes:

- `feat:` for new skill capabilities or materially expanded guidance
- `fix:` for corrected instructions, links, or misleading wording
- `docs:` for user-visible documentation improvements
- `refactor:` for structural cleanup without changing behavior
- `ci:`, `build:`, `test:`, and `chore:` for repository maintenance

Examples:

- `feat: add large-repo sampling guidance`
- `fix: clarify insufficient-evidence handling`
- `docs: switch install examples to learn-this-project`

The `metadata.version` field in `skills/learn-this-project/SKILL.md` is
informational. Repository releases are managed by Git tags and Release Please.

## Repository structure

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

The repository-level docs, workflows, and release configuration exist only to
make the skill easier to publish and maintain.
