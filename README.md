# Zed Editor Configuration

Personal configuration for [Zed](https://zed.dev), a high-performance, multiplayer code editor.

## Overview

This repository contains my customized Zed settings optimized for:
- Python development with Ruff integration
- Vim mode with system clipboard integration
- AI-powered coding assistance (Copilot + custom LLM)
- Clean, focused interface with minimal distractions

## Key Features

### Editor
- **Vim mode** enabled with relative line numbers
- **Auto-save** on window change
- **Format on save** with language-specific formatters
- Smart search with case sensitivity
- Preview tabs for quick file exploration

### Development Tools
- **Python**: Ruff for linting/formatting via `uvx`
- **TypeScript/JavaScript**: Auto-organize imports
- **Git**: Inline blame with commit summaries
- **AI**: GitHub Copilot predictions + GPT-5 via LiteLLM proxy

### UI Customization
- **Theme**: Dayfox (opaque background)
- **Font**: Input Mono, 12pt
- **Layout**: Agent panel (left), Terminal (left), Project panel (right)
- Hidden panels: Collaboration, Chat, Search, Outline

### Custom Tasks
Quick access to common commands via Command Palette (Cmd+Shift+P):
- **Claude Tasks**: Interactive AI assistance, commit creation, CI checks, push review, PR creation
- **Python Tasks**: Run current file, format with Ruff, lint with Ruff
- **Git Tasks**: Quick status check, quick commits

## Files

- `settings.json` - Main configuration file with comprehensive inline documentation
- `tasks.json` - Custom tasks for quick access to common commands
- `.gitignore` - Excludes workspace-specific and temporary files

## Installation

1. Install [Zed](https://zed.dev/download)
2. Clone or copy these files to `~/.config/zed/`
3. Restart Zed to apply settings

## Requirements

For full functionality:
- `claude` - Claude CLI for AI-powered tasks
- `uvx` - Python tool runner (for Ruff formatting)
- `ruff` - Python linter/formatter
- GitHub Copilot subscription (optional)
- LiteLLM proxy setup (optional, for custom LLMs)

## License

Personal configuration - feel free to use and modify as needed.