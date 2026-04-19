# Output Guidance

Use this reference when preparing the final repo summary for the user.

## Required Sections

The final report should cover:

1. Project Summary
   - Purpose, audience, and primary capabilities
   - State whether each point is evidence-backed or inferred

2. Tech Stack and Tooling
   - Languages, frameworks, package managers, build tools, CI, and notable
     dependencies

3. Architecture and Execution Model
   - Major components, boundaries, and how requests, commands, jobs, or data
     move through the system

4. Conventions and Quality Signals
   - Testing style, configuration patterns, layout choices, error handling,
     documentation quality, and release automation

5. Ambiguities and Gaps
   - Conflicting signals, missing evidence, and open questions

6. Confidence Notes
   - Call out where confidence is high, medium, or limited
   - If the repo was sampled, say that explicitly

## Writing Rules

- Be concise, but do not compress away important caveats.
- Prefer bullets or short paragraphs over long prose dumps.
- Reference concrete files whenever they materially support a claim.
- Do not fabricate implementation details, business context, or deployment
  environments.
- If the repository is tiny, say so instead of forcing a large-architecture
  summary.
- If the repository is large, explain the sampling approach you used.

## Template

Use `assets/report-template.md` when a fill-in structure will help you produce
a clearer summary.
