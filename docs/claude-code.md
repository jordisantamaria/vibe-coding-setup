# Claude Code

AI coding assistant CLI by Anthropic.

## Installation

```bash
npm install -g @anthropic-ai/claude-code
```

## Usage

```bash
# Start interactive session
claude

# Start with a prompt
claude "explain this code"

# Pass files
claude "describe this image" /path/to/image.png
```

## Workflow with WezTerm

Recommended pane layout:

```
+---------------------------+----------+
|                           |          |
|   Neovim                  |  Claude  |
|                           |  Code    |
|                           |          |
+---------------------------+----------+
```

1. `Ctrl+A` then `|` to split horizontal
2. Left pane: Neovim for editing
3. Right pane: Claude Code for AI assistance

## Key commands

| Command | Action |
|---|---|
| `/help` | Show help |
| `/compact` | Compact conversation context |
| `/clear` | Clear conversation |
| `Ctrl+C` | Cancel current generation |
| `Escape` | Exit |

## Image support

With WezTerm (no tmux), you can paste images directly into Claude Code for analysis. This was the main reason for switching from Kitty + tmux to WezTerm.
