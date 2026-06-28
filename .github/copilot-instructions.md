# Copilot Review Instructions

## Core principle

Prefer silence over uncertainty. A review comment has a cost — it demands the author's attention, may trigger another round, and can obscure the comments that actually matter. Only post a comment when you are confident the issue is real and material.

## What to flag

Flag genuine defects in the diff: logic errors, incorrect conditions, missing error handling, concurrency hazards, resource leaks, security regressions, data corruption. These always warrant a comment.

## What not to flag

- **Style and formatting** — CI enforces these automatically. Do not comment on indentation, line length, naming conventions, comment phrasing, or anything a linter or formatter would catch.
- **Pre-existing issues** — if a problem exists in code the PR did not introduce, do not raise it. The PR is not the right vehicle to fix it.
- **Low-confidence observations** — if you are not certain an issue is real, stay silent. Do not post speculative or "consider whether..." comments.
- **Already-raised issues** — if you flagged something in an earlier review round on this PR and the author did not act on it, do not raise it again. Either it was resolved, or the author made a deliberate choice. Repeating it creates noise without value.

## Threshold

Before posting, ask: is this a correctness or security defect that a careful human reviewer would block the PR on? If not, stay silent.

<!--VITE PLUS START-->

# Using Vite+, the Unified Toolchain for the Web

This project is using Vite+, a unified toolchain built on top of Vite, Rolldown, Vitest, tsdown, Oxlint, Oxfmt, and Vite Task. Vite+ wraps runtime management, package management, and frontend tooling in a single global CLI called `vp`. Vite+ is distinct from Vite, and it invokes Vite through `vp dev` and `vp build`. Run `vp help` to print a list of commands and `vp <command> --help` for information about a specific command.

Docs are local at `node_modules/vite-plus/docs` or online at https://viteplus.dev/guide/.

## Review Checklist

- [ ] Run `vp install` after pulling remote changes and before getting started.
- [ ] Run `vp check` and `vp test` to format, lint, type check and test changes.
- [ ] Check if there are `vite.config.ts` tasks or `package.json` scripts necessary for validation, run via `vp run <script>`.
- [ ] If setup, runtime, or package-manager behavior looks wrong, run `vp env doctor` and include its output when asking for help.

<!--VITE PLUS END-->
