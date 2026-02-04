# WezTerm

GPU-accelerated terminal emulator with built-in multiplexer. Replaces Kitty + tmux.

## Installation

```bash
brew install --cask wezterm
```

## Config file

`~/.config/wezterm/wezterm.lua`

## Appearance

| Setting | Value |
|---|---|
| Color scheme | Catppuccin Mocha |
| Font | JetBrains Mono Medium |
| Font size | 14 |
| Line height | 1.1 |
| Background opacity | 0.95 |
| macOS blur | 20 |
| Tab bar | Bottom, hidden if single tab |
| Cursor | Blinking bar |
| Scrollback | 10000 lines |

## Keybindings

Leader key: `Ctrl+A` (timeout 1s)

### Panes

| Keybind | Action |
|---|---|
| `Leader` `v` | Split vertical |
| `Leader` `\|` | Split vertical (alt) |
| `Leader` `-` | Split horizontal |
| `Leader` `h` | Navigate left |
| `Leader` `j` | Navigate down |
| `Leader` `k` | Navigate up |
| `Leader` `l` | Navigate right |
| `Leader` `H` | Resize left |
| `Leader` `J` | Resize down |
| `Leader` `K` | Resize up |
| `Leader` `L` | Resize right |
| `Leader` `x` | Close pane |
| `Leader` `z` | Toggle zoom |

### Tabs

| Keybind | Action |
|---|---|
| `Leader` `c` | New tab |
| `Leader` `,` | Rename tab |
| `Leader` `n` | Next tab |
| `Leader` `Shift+N` | Previous tab |
| `Leader` `1-5` | Go to tab N |

### Clipboard

| Keybind | Action |
|---|---|
| `Leader` `p` | Paste image from clipboard (saves to /tmp and types path) |
| `Leader` `[` | Copy mode |
| `Leader` `Ctrl+A` | Send literal Ctrl+A |

> Requires `pngpaste`: `brew install pngpaste`

## Why WezTerm over Kitty + tmux

- tmux breaks image protocols (can't paste images in Claude Code)
- tmux filters escape sequences, breaking clipboard integration
- WezTerm's built-in mux provides panes/tabs natively without these issues
- Single config file in Lua (same language as Neovim config)
