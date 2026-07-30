# Claudette Can Code (Pro) — CDCC

Non-bypassable **D2R plan enforcement for Claude Code**. A plugin that reads an approved D2R four-document bundle (PRD, TRD, AVD, TQCD) and structurally enforces the resulting plan — rather than trusting a model to follow it.

It eliminates four categories of silent failure:

- **Silent model substitution** — a cheaper model running a stage assigned to a stronger one
- **Silent skill-skipping** — writing directly to the main session instead of invoking the assigned sub-agent skill
- **Silent gate-skipping** — advancing past a verification gate that never ran
- **Silent plan drift** — executing something other than the approved plan

Enforcement is via hooks, so it refuses rather than warns.

## Where the code is

The plugin lives in **[`plugin/`](plugin/)** — see [`plugin/README.md`](plugin/README.md) for installation, configuration, and the full enforcement model.

## Status

**MVP v0.9.** Residual verification work is outstanding; this is not a finished 1.0.

## Licence

MIT © 2026 Krystal Martinez. See [`LICENSE`](LICENSE).
