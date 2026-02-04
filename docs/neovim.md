# Neovim + LazyVim

## Installation

```bash
brew install neovim
```

Config lives at `~/.config/nvim/`.

## Framework

**LazyVim** as base framework with no extras enabled. All plugins are manually configured in `lua/plugins/`.

## Config structure

```
~/.config/nvim/
  init.lua                  # Bootstrap, loads config.lazy
  lazyvim.json              # LazyVim extras (empty, all manual)
  lua/
    config/
      lazy.lua              # Plugin manager setup
      keymaps.lua           # Custom keybindings
      options.lua           # Vim options
      autocmds.lua          # Autocommands
    plugins/
      editor.lua            # Neo-tree, flash, grug-far
      ui.lua                # Colorscheme, zen-mode
      navigation.lua        # vim-tmux-navigator
      git.lua               # Fugitive, rhubarb, gitsigns, git-messenger
      csv.lua               # CSV/table editing
      which-key.lua         # Keybinding hints
```

## Settings

| Setting | Value |
|---|---|
| Autoformat on save | Disabled |
| Colorscheme | Tokyonight Storm |

## Plugins (44)

### Core

| Plugin | Purpose |
|---|---|
| LazyVim | Framework |
| lazy.nvim | Plugin manager |

### Completion & Snippets

| Plugin | Purpose |
|---|---|
| blink.cmp | Completion engine |
| friendly-snippets | Snippet library |
| lazydev.nvim | Neovim API completion |

### UI

| Plugin | Purpose |
|---|---|
| catppuccin | Colorscheme (installed) |
| tokyonight.nvim | Colorscheme (active, storm) |
| lualine.nvim | Status line |
| bufferline.nvim | Buffer tabs |
| noice.nvim | UI for messages/cmd |
| nui.nvim | UI component library |
| snacks.nvim | Utilities collection |
| zen-mode.nvim | Distraction-free mode (width=120) |
| mini.icons | Icon support |

### LSP & Linting

| Plugin | Purpose |
|---|---|
| nvim-lspconfig | LSP configuration |
| mason.nvim | LSP/formatter installer |
| mason-lspconfig.nvim | Mason + lspconfig bridge |
| nvim-lint | Linter integration |
| conform.nvim | Code formatter |

### Treesitter

| Plugin | Purpose |
|---|---|
| nvim-treesitter | Syntax highlighting |
| nvim-treesitter-textobjects | Text objects |
| ts-comments.nvim | Comment handling |
| nvim-ts-autotag | Auto-close HTML tags |

### Navigation & Search

| Plugin | Purpose |
|---|---|
| neo-tree.nvim | File explorer (width=45) |
| flash.nvim | Enhanced f/F/t/T movement |
| grug-far.nvim | Search and replace |
| vim-tmux-navigator | Vim/tmux pane navigation |

### Editing

| Plugin | Purpose |
|---|---|
| vim-abolish | Case conversion (crs/crc/crm) |
| vim-repeat | Repeat for plugin actions |
| nvim-colorizer.lua | Hex color preview |
| mini.ai | Text objects |
| mini.pairs | Auto pairing |

### Git

| Plugin | Purpose |
|---|---|
| vim-fugitive | Git commands (:Git, :Gdiffsplit, :Gblame) |
| vim-rhubarb | GitHub integration (:GBrowse) |
| gitsigns.nvim | Git signs in gutter |
| git-messenger.vim | Show commit message for line |

### Data / Tables

| Plugin | Purpose |
|---|---|
| csv.vim | CSV editing |
| vim-table-mode | Markdown tables |

### Utilities

| Plugin | Purpose |
|---|---|
| trouble.nvim | Diagnostics UI |
| todo-comments.nvim | TODO/FIXME highlighting |
| persistence.nvim | Session persistence |
| which-key.nvim | Keybinding hints |
| plenary.nvim | Utility library |

## Keybindings

Leader key: `Space`

### General

| Keybind | Mode | Action |
|---|---|---|
| `jk` | Insert | Exit insert mode |
| `Ctrl+S` | Normal | Save file |
| `Space n` | Normal | Clear search highlights |

### Motion

| Keybind | Mode | Action |
|---|---|---|
| `H` | Normal/Visual/Op | Line start |
| `L` | Normal/Visual/Op | Line end |
| `g.` | Normal | Last insertion point |

### Buffers

| Keybind | Mode | Action |
|---|---|---|
| `TAB` | Normal | Next buffer |
| `Shift+TAB` | Normal | Previous buffer |

### Editing

| Keybind | Mode | Action |
|---|---|---|
| `<` | Normal | Indent left |
| `>` | Normal | Indent right |
| `=` | Normal | Auto-indent inner block |
| `y` | Visual | Yank and go to end |
| `p` | Visual/Normal | Paste and go to end |

### Windows

| Keybind | Mode | Action |
|---|---|---|
| `Space v` | Normal | Split vertical |
| `Space -` | Normal | Split horizontal |
| `Alt+k` | Normal | Decrease height |
| `Alt+j` | Normal | Increase height |
| `Alt+h` | Normal | Decrease width |
| `Alt+l` | Normal | Increase width |
| `Ctrl+H/J/K/L` | Normal | Navigate panes (tmux-aware) |

### Diagnostics

| Keybind | Mode | Action |
|---|---|---|
| `Ctrl+P` | Normal | Previous diagnostic |
| `Ctrl+N` | Normal | Next diagnostic |

### Quickfix

| Keybind | Mode | Action |
|---|---|---|
| `Ctrl+M` | Normal | Next quickfix item |
| `Space qn` | Normal | Next quickfix |
| `Space qp` | Normal | Previous quickfix |
| `Space qo` | Normal | Open quickfix |
| `Space qc` | Normal | Close quickfix |
| `Space ql` | Normal | Last quickfix |

### Git

| Keybind | Mode | Action |
|---|---|---|
| `Space gS` | Normal | Git status (fugitive) |
| `Space gd` | Normal | Git diff split |
| `Space gD` | Normal | Git diff |
| `Space gO` | Normal | Open in GitHub |
| `Space gm` | Normal | Git message for line |
| `Space g1` | Normal | Diffget left (//2) |
| `Space g3` | Normal | Diffget right (//3) |

### Actions

| Keybind | Mode | Action |
|---|---|---|
| `Space ai` | Normal | Ignore case on |
| `Space aI` | Normal | Ignore case off |
| `Space z` | Normal | Zen mode |
| `Space tm` | Normal | Toggle table mode |

### CSV

| Keybind | Mode | Action |
|---|---|---|
| `Space Xh` | Normal | Highlight column |
| `Space XH` | Normal | Header toggle |
| `Space Xd` | Normal | Delete column |
| `Space XD` | Normal | Check duplicates |
| `Space Xw` | Normal | Column name |
| `Space XW` | Normal | Column number |
| `Space Xn` | Normal | Num columns |

### Cheatsheets

| Keybind | Action |
|---|---|
| `Space Cc` | Clean code |
| `Space Cr` | Resources |
| `Space Cd` | Docker |
| `Space Cp` | Python |
| `Space Cv` | Vue |
| `Space Cs` | Software structure (DDD) |
| `Space Ca` | AWS |
| `Space Ct` | Tmux |
| `Space Cb` | Bash |
| `Space Cm` | Markdown |
| `Space Cn` | Neovim mappings |
| `Space Cq` | PostgreSQL |

### Command line

| Keybind | Mode | Action |
|---|---|---|
| `Ctrl+P` | Cmd | Previous command |
| `Ctrl+N` | Cmd | Next command |

## Case conversion (vim-abolish)

| Command | Result |
|---|---|
| `crs` | snake_case |
| `crc` | camelCase |
| `crm` | MixedCase |
