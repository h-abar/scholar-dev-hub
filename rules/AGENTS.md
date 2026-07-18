# AGENTS.md

> Generic rules every modern AI coding agent (Aider, Cursor, Codex, Gemini CLI,
> Kimi CLI, Qwen Code, OpenCode, and others) reads automatically. Copy this file
> into your repository root and fill in the `[BRACKETED]` sections.
>
> This is a starter template from Scholar Dev Hub. Remove anything that doesn't
> apply, and add anything specific to your project. Keep it scannable — agents
> read this on every turn.

## Project overview

- **Name:** [PROJECT_NAME]
- **What it does:** [one-sentence description]
- **Primary language(s):** [e.g. Python 3.12 / TypeScript 5.4]
- **Repository type:** [library / CLI / web app / service / notebook]

## Build, run, and verify

Always run the relevant verification command before declaring a task done.

- **Install deps:** `[COMMAND]` (e.g. `uv sync` / `npm ci` / `pip install -e .`)
- **Run locally:** `[COMMAND]`
- **Run tests:** `[COMMAND]` (e.g. `pytest -q` / `npm test` / `cargo test`)
- **Lint:** `[COMMAND]` (e.g. `ruff check .` / `npm run lint`)
- **Format:** `[COMMAND]` (e.g. `black .` / `prettier --write .`)
- **Type check:** `[COMMAND]` (e.g. `mypy .` / `tsc --noEmit`)

If a command fails after your change, **fix it before reporting done**.

## Architecture notes

- [Where the entry points live]
- [The main modules/packages and what each owns]
- [Where shared state / config / env vars are read]
- [Critical invariants that must not be broken]

## Conventions

- **Public surface:** only `[MODULE]` exports are part of the public API.
- **Naming:** [snake_case for Python, camelCase for JS, etc.], constants `UPPER_SNAKE`.
- **Errors:** raise specific exception classes; never return `None` to signal error.
- **Async:** prefer `async def` for I/O paths; never block the event loop.
- **Comments:** explain *why*, not *what*. Don't restate code.
- **No commented-out code or dead branches left behind.**

## Commit and PR style

- Commit messages: `type(scope): subject` — subject ≤ 72 chars, imperative mood.
  - Allowed types: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `perf`.
- One logical change per commit. No mixing refactors with features.
- PRs: lead with the motivation, then the change, then how it was verified.

## Guardrails — do NOT

- Do **not** add new dependencies without confirming they're justified and licensed compatibly.
- Do **not** disable, weaken, or rewrite tests to make them pass.
- Do **not** commit secrets, API keys, or `.env` files.
- Do **not** push, amend, force-push, or create PRs unless explicitly asked.
- Do **not** edit generated/locked files (lockfiles, dist artifacts) by hand.
- Do **not** introduce silent failures (empty `except`, swallowed promises).

## How to verify your work

1. Run the full **Build, run, and verify** suite from above.
2. Re-read your diff and ask: would a careful reviewer accept this as-is?
3. If anything is uncertain or you changed behavior, write it in the PR description — never hide it.

## Context the agent should remember

- [Link to architecture doc / ADR index, if any]
- [Current sprint goal / hot area, if relevant]
- [Known fragile tests that sometimes flake — don't "fix" by deletion]

---

Template from [Scholar Dev Hub](https://github.com/h-abar/scholar-dev-hub) · CC0.