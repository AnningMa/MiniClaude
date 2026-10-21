# MiniClaude

A lightweight local coding agent built with Python and Anthropic Claude, inspired by Claude Code.

## Features

- CLI and terminal UI connected to a persistent agent daemon.
- File and shell tools with permission controls.
- Sessions, task management, skills, MCP integration, and execution tracing.

## Quick Start

Requires Python 3.12 and [uv](https://docs.astral.sh/uv/).

```bash
uv sync
cp .env.example .env
```

Set `ANTHROPIC_API_KEY` in `.env`, then start the daemon:

```bash
uv run kama-core
```

In another terminal, launch the UI:

```bash
uv run kama-tui
```

## Development

```bash
uv run pytest tests/unit
```

See [RUNBOOK.md](RUNBOOK.md) for configuration and operations.

## Credits

Based on [KamaClaude](https://github.com/youngyangyang04/KamaClaude). Licensed under the [MIT License](LICENSE).
