# Evidence and Confidence

Use this reference when the repository is ambiguous, stale, large, or lightly
documented, or when you need to make confidence judgments explicit.

## Evidence Standards

- Prefer source code, configuration, tests, build files, and workflows over
  prose docs alone.
- Label direct observations as evidence.
- Label conclusions drawn from multiple clues as inference.
- Do not present inference as confirmed fact.

## Confidence Levels

- High confidence: directly supported by code, config, tests, workflows, or
  repeated signals across multiple repo artifacts.
- Medium confidence: a reasonable inference from several artifacts, but not
  directly spelled out.
- Low confidence: weak or incomplete evidence. Prefer reporting
  "insufficient evidence" instead.

When possible, cite files inline. Examples:

- `README.md` states the repository goal.
- `cmd/server/main.go` wires the HTTP service.
- `.github/workflows/test.yml` shows the project runs unit tests and linting.
- `internal/store/postgres_test.go` demonstrates the integration-test pattern.

## Ambiguity Handling

If the repo is unclear, use this sequence:

1. Check whether the ambiguity comes from stale docs, partial code, generated
   files, or multiple products living in one repo.
2. Prefer code and active workflows over older prose.
3. Report the ambiguity plainly.
4. State the most likely interpretation only if the evidence supports a
   bounded inference.
5. Ask the user a concise question only if the ambiguity blocks the current
   task.

## Insufficient-Evidence Guidance

Say "insufficient evidence" when:

- the purpose is not confirmed by repo artifacts
- architecture is only implied by directory names
- dependencies are referenced but not wired
- tests exist but do not show the claimed behavior
- docs describe systems that are missing from the code

When evidence is insufficient, list the missing artifacts that would improve
confidence, such as runtime entrypoints, architecture docs, test coverage, or
deployment manifests.
