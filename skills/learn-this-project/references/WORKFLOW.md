# Repo-Triage Workflow

Use this reference when you are actively learning a repository and need the
step-by-step process.

## Exploration Order

Work in this order unless the repository clearly demands a different path:

1. Identify the repository shape.
   - List top-level files and directories.
   - Note likely entrypoints, package roots, apps, services, libraries, docs,
     infra directories, and test locations.

2. Read the project framing.
   - Check `README*`, docs indexes, package manifests, module files, lockfiles,
     `Makefile`, build scripts, and CI workflows.
   - Record the repo's stated purpose and the operational commands it exposes.

3. Confirm the implementation surface.
   - Read entrypoints, main packages, exported APIs, service wiring, router
     setup, worker startup, CLI commands, or package boundaries.
   - Map the major components and how control flows through them.

4. Inspect configuration and integration edges.
   - Review environment handling, config files, dependency manifests, external
     services, databases, queues, and network boundaries.

5. Inspect quality signals.
   - Read representative tests, lint config, formatting config, benchmarks, and
     release or CI automation.
   - Note what kinds of failures the repo appears designed to catch.

6. Summarize conventions.
   - Capture naming, layout, dependency injection style, error handling,
     testing approach, code-generation use, and documentation habits.

## Large-Repo Sampling

For large repositories, sample deliberately instead of wandering:

1. Start with the root and one level below it.
2. Find the primary execution path or package boundary.
3. Sample one representative file for each major subsystem.
4. Sample at least one test file for each important executable or package area
   you mention in the summary.
5. Stop when additional files stop changing your mental model materially.

If you sampled instead of reading broadly, say so in the output.

Good sampling signals:

- root documentation and manifests
- top-level app or service entrypoints
- dependency injection or wiring code
- router, handler, controller, or command registration files
- domain package boundaries
- representative tests
- CI and release automation
