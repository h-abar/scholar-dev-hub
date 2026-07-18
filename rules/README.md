# Agent Rules Templates

Drop-in configuration files that make any modern AI coding agent productive in your repository immediately — instead of you re-explaining the project every time.

> **Why these exist:** Scholar Dev Hub is more than a curated list — it ships a reusable engineering environment. The advantage as AI agents become part of every developer's workflow will come from the **quality of the engineering environment surrounding the model**, not the model itself. These templates are that environment, distilled.

## The files

| File | Purpose | Read automatically by |
|---|---|---|
| [`AGENTS.md`](AGENTS.md) | Generic project rules, conventions, commands, and guardrails | Aider, Cursor, Codex, Gemini CLI, Kimi CLI, Qwen Code, OpenCode, and most agent-CLI tools |
| [`CLAUDE.md`](CLAUDE.md) | Claude Code project memory: skills, permissions, conventions | Claude Code (Anthropic) |
| [`opencode.json`](opencode.json) | opencode configuration: model, provider, permissions | opencode (sst) |
| [`mcp-example.json`](mcp-example.json) | Example Model Context Protocol (MCP) server wiring | Claude Code, Cursor, Windsurf, Cline, and any MCP-aware client |

## How to use

```bash
# 1) Copy the templates you need into your project
git clone https://github.com/h-abar/scholar-dev-hub.git
cp scholar-dev-hub/rules/AGENTS.md        your-project/
cp scholar-dev-hub/rules/CLAUDE.md        your-project/
cp scholar-dev-hub/rules/opencode.json    your-project/opencode.json
cp scholar-dev-hub/rules/mcp-example.json your-project/.mcp.json

# 2) Edit the bracketed sections ([PROJECT_NAME], [YOUR_NAME]…) to match your project
# 3) Open the project in your AI coding agent — it picks the rules up automatically
```

## Pair with the dev container

For a fully reproducible environment, also copy [`.devcontainer/`](../.devcontainer/) into your project. VS Code / Codespaces will then offer a one-click "Reopen in Container" that provisions Python, Node, Git, and the GitHub CLI so every agent just runs.

## Contributing

Found a rule that improved agent performance? A guardrail that prevented a real bug? Open a PR — these templates evolve with real usage, and your edge case helps everyone.

## License

CC0 1.0 Universal — copy, modify, ship. These belong to everyone.