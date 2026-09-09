---
tags: [cheatsheet, vim]
module: Linux Fundamentals
---

# Vim Commands Cheatsheet (vimtutor)

| Command | Action |
|---|---|
| `h j k l` | Move cursor left / down / up / right |
| `ESC` | Return to normal mode |
| `:q!` `<ENTER>` | Discard changes made |
| `x` | Delete unwanted character |
| `i` | Insert text |
| `A` | Append text |
| `:wq` | Save file and exit |
| `dw` | Delete a word |
| `d$` | Delete to the end of the line |
| `dd` | Delete a whole line |
| `2dd` | Delete 2 lines |
| `u` | Undo a command |
| `U` | Fix a whole line |
| `p` | Put (paste) previously deleted text after cursor |
| `CTRL-G` | Show current location in file and file status |
| `G` | Move to a specific line in the file |
| `%` | Find matching `)` `}` `]` |
| `$` | Move to end of the line |
| `0` | Move to start of the line |
| `gg` | Move to the first line of the file |
| `/text` | Search forward for target text |
| `?text` | Search backward for target text |
| `yy` | Copy a whole line |
| `2yy` | Copy 2 lines |
| `yw` | Copy a word |
| `CTRL-R` | Redo undone changes |