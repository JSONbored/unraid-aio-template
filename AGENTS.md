# unraid-aio-template Agent Notes

This repository is the baseline template for the public `*-aio` repos.

## Purpose

- Start new AIO repos from this template.
- Keep workflow policy, repo structure, and automation defaults aligned across the portfolio.
- Treat this repo as the source of truth for inherited GitHub Actions behavior.

## Durable Conventions

- Validation and smoke tests should run on branch and PR work.
- Image publishing should happen only from the default branch after merge.
- Workflow actions should stay pinned to full commit SHAs.
- Renovate should stay PR-first rather than auto-merging.
- Public READMEs must stay user-facing; maintainer-only guidance belongs in internal notes, not product docs.

## Important Template Expectations

- New repos should expose a beginner-first Unraid XML with safe defaults.
- Advanced options should be available when the wrapped upstream product supports them, but default installs must still work cleanly.
- Each derived repo should keep `upstream.toml` accurate and use PR-based upstream update automation.
- The template should continue to support `awesome-unraid` sync.

## Repo Status Notes

- There is known local work in this repo that has not all been pushed yet.
- The build workflow was patched locally so GHCR image names are forced to lowercase before publish.
- Funding should include both GitHub Sponsors (`JSONbored`) and Ko-fi (`jsonbored`).

## Recommended Memory For Future Sessions

- When changing shared workflow behavior here, check all derived repos for drift.
- Avoid putting maintainer-only setup steps into public README content.
- If GitHub Actions naming looks odd in the sidebar, check whether the workflow exists on the default branch before changing YAML just for UI cosmetics.
