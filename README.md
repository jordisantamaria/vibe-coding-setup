# Vibe Coding Setup

Development environment setup for macOS: terminal, editor, and AI-assisted coding.

## Stack

| Tool | Purpose |
|---|---|
| [WezTerm](docs/wezterm.md) | Terminal emulator + built-in multiplexer |
| [Neovim + LazyVim](docs/neovim.md) | Editor |
| [Claude Code](docs/claude-code.md) | AI coding assistant (CLI) |

## Philosophy

- **WezTerm** replaces Kitty + tmux. Built-in multiplexer means no image/clipboard issues.
- **LazyVim** as Neovim framework with manual plugin management (no extras, full control).
- **Claude Code** runs in a WezTerm pane alongside Neovim.

## Config locations

| Tool | Config path |
|---|---|
| WezTerm | `~/.config/wezterm/wezterm.lua` |
| Neovim | `~/.config/nvim/` |
| Claude Code | `~/.claude/` |

## Quick reference

- WezTerm leader: `Ctrl+A`
- Neovim leader: `Space`
- Split terminal: `Ctrl+A` then `v` (vertical) or `-` (horizontal)
- Split editor: `Space v` (vertical) or `Space -` (horizontal)
