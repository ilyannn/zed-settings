# Zed Editor Configuration

Personal configuration for [Zed](https://zed.dev), focused on Python and
TypeScript development with Vim navigation and a compact interface.

## Highlights

### Editor

- Cursor base keymap with Vim mode, relative line numbers, and system clipboard
- Auto-save when changing windows
- Format-on-save limited to Git-modified lines
- Preview tabs, smart-case search, inline diagnostics, and LSP result pickers
- Input Mono at 14 px with comfortable line height
- Tiniri themes and Catppuccin file icons

### Language tooling

- **Python**: Basedpyright for navigation and type checking; Ruff for linting
  and formatting
- **TypeScript/JavaScript/TSX**: Zed's default vtsls for code intelligence;
  Biome for formatting, import organization, and safe fixes when a Biome
  configuration is present
- **JSON**: Biome formatting
- **Markdown and LaTeX**: language-specific wrapping widths

Project-specific Python rules belong in `pyproject.toml`, `ruff.toml`, or
`pyrightconfig.json` so editor behavior agrees with CI.

### Git and interface

- Inline blame with commit summaries
- Git and project panels on the right; Agent, terminal, and outline on the left
- Lockfiles and generated TeX files open read-only
- Collaboration, search, outline, and debugger panel buttons are hidden

### Privacy and security

- Usage metrics and diagnostic telemetry are disabled
- New worktrees require explicit trust before project settings can launch tools
- Edit predictions are disabled
- A local LiteLLM proxy exposes a custom GPT-5 model to the Agent Panel

### File scanning

The exclusion list preserves Zed's built-in VCS and OS exclusions and adds
editor metadata, Python environments and caches, and `node_modules`. Generic
`build`, `dist`, and `.cache` directories are left to each project's
`.gitignore` so tracked source directories are not hidden globally.

### Tasks

`tasks.json` provides Command Palette tasks for:

- Claude and Codex CLI sessions
- Claude-assisted commits, pushes, pull requests, and CI checks
- Running, formatting, and linting Python files
- Git status and quick commits
- `just test`

## Files

- `settings.json` — Zed preferences and language configuration
- `tasks.json` — reusable project tasks

## Installation

1. Install [Zed](https://zed.dev/download).
2. Clone or copy this repository to `~/.config/zed/`.
3. Install the Tiniri and Catppuccin icon themes and the Input Mono font.
4. Restart Zed.

Optional task dependencies include `claude`, `codex`, `uvx`, and `just`.
The custom GPT-5 model also requires the configured LiteLLM proxy.

## License

Personal configuration — feel free to adapt it.
