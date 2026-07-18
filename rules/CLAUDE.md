# CLAUDE.md

> Project memory for [Claude Code](https://www.anthropic.com/claude-code).
> Claude Code reads this file automatically when working in the repository.
> Copy this template into your project root and fill the `[BRACKETED]` sections.
>
> Template from Scholar Dev Hub. Trim aggressively — Claude's context is precious.

## One-line project description

[PROJECT_NAME] is a [what it does] built with [main language/framework].

## Quick facts Claude must know

- **Runtime:** [e.g. Python 3.12 / Node 20 / Go 1.22]
- **Package manager:** [uv / npm / pnpm / cargo / pip]
- **Test command:** [the exact command Claude should run to verify]
- **Lint command:** [the exact command Claude should run before reporting done]
- **Don't touch:** [paths Claude must never modify, e.g. `dist/`, `*.lock`, generated files]

## Coding conventions in this repo

- [Naming, file layout, public API rules — keep to ~5 bullet points max]
- Prefer [pattern X] over [pattern Y] for [reason].
- All public functions get type hints and a one-line docstring.
- No `print()` in library code — use the `log` module.

## Commands Claude should use

```bash
# install deps
[COMMAND]
# run the app
[COMMAND]
# verify changes — ALWAYS run before claiming success
[COMMAND]
# fix formatting / lint before finishing a change
[COMMAND]
```

## How to make a change end-to-end

1. Confirm the request against the relevant tests first.
2. Make the smallest correct change.
3. Run the verification command from above.
4. If it passes: summarize the change in 2-3 lines. Do not commit unless asked.
5. If it fails: fix the failure before reporting done — never weaken a test.

## Guardrails

- Never commit secrets or `.env`. Never push without being asked.
- Never delete tests to make a suite pass.
- Never introduce a dependency without stating the justification.
- Prefer editing existing code over creating new files unless a new file is clearly the right structure.

## Project-specific knowledge (add as you learn)

- [Quirk 1: e.g. "the `auth/` module intentionally has no async — see ADR #4"]
- [Quirk 2: e.g. "tests in `tests/integration/` hit a local fixture server; port 5099 must be free"]
- [Known flaky test names to re-run once rather than "fix"]

## Skills & permissions (optional)

- Claude has permission to run: `[verify command]`, `[lint command]`.
- Claude must ask before: installing packages, editing `Makefile`, touching `migrations/`.

---

Template from [Scholar Dev Hub](https://github.com/h-abar/scholar-dev-hub) · CC0.