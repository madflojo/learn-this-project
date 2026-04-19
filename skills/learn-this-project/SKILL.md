---
name: learn-this-project
description: >-
  Triage a repository quickly and produce an evidence-backed summary of its
  purpose, architecture, stack, workflows, and conventions without
  overstating certainty.
  Use this skill to get up to speed on an unfamiliar codebase, identify the
  main components and how they fit together, and find the key files that support
  the repo's stated purpose and capabilities.
license: Apache-2.0
metadata:
  version: "1.0.0"
  author: Benjamin Cane
  repository: learn-this-project
---

# Learn This Project

Use this skill to learn an unfamiliar repository fast and report only what is
supported by evidence in the repo.

The goal is not to read everything. The goal is to produce a reliable working
model of the project, identify the key files that support that model, and stay
explicit about uncertainty.

## When to Use

Use this skill when:

- a task starts in an unfamiliar repository
- the user asks for a repo overview, architecture summary, or onboarding help
- you need to identify conventions before making changes
- you need a quick triage pass before deeper implementation or review work

Do not use this skill as a substitute for task-specific investigation once the
relevant subsystem is already known.

## Core Objectives

1. Identify the repository's likely purpose, audience, and main capabilities.
2. Map the major components, boundaries, and execution flow.
3. Capture the tech stack, workflows, and engineering conventions that matter
   for follow-on work.
4. Separate direct evidence from inference and avoid false certainty.
5. Call out ambiguity or insufficient evidence instead of guessing.

## Working Rules

- Prefer primary artifacts such as code, config, tests, manifests, workflows,
  and runtime entrypoints over prose docs alone.
- Treat a fast repo triage as intentionally partial unless you actually
  inspected the repo broadly.
- Cite concrete files whenever they materially support a claim.
- If the repository is large, sample deliberately instead of wandering.
- If the evidence is weak, say so plainly.

## How to Learn the Repo

Start broad, then narrow:

1. Inspect the top-level repository shape.
2. Read project framing such as `README*`, manifests, `Makefile`, and CI.
3. Confirm the implementation surface through entrypoints, package boundaries,
   service wiring, or exported APIs.
4. Inspect configuration, integrations, and quality signals.
5. Summarize conventions and remaining uncertainties.

For the detailed workflow, sampling strategy, and ambiguity rules, load:

- `references/WORKFLOW.md` for the step-by-step repo-triage process
- `references/EVIDENCE.md` for confidence levels, evidence standards, and
  insufficient-evidence handling

## Output

Produce a concise report that covers:

- project summary
- tech stack and tooling
- architecture and execution model
- conventions and quality signals
- ambiguities and gaps
- confidence notes

Use the output template in `assets/report-template.md` when you need a concrete
response shape. Load it before writing the final report if the user wants a
structured project summary or if the repo is complex enough that a fixed format
improves clarity.

For more output guidance, load:

- `references/OUTPUT.md` for section expectations and writing rules
- `assets/report-template.md` for a fill-in template

## Loading Guidance

Do not load every supporting file by default.

- Load `references/WORKFLOW.md` when you are actively exploring a repository.
- Load `references/EVIDENCE.md` when the repo is ambiguous, large, stale, or
  lightly documented.
- Load `references/OUTPUT.md` and `assets/report-template.md` when preparing
  the final summary for the user.

## Success Criteria

The skill is successful when the final report:

- gives a useful working model of the repository
- distinguishes evidence from inference
- references the files that matter most
- avoids invented details
- tells the reader what is still unclear
