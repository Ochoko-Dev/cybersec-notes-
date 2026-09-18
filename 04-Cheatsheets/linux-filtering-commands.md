---
tags: [cheatsheet, linux, filtering]
module: Linux Fundamentals
---

# Text Filtering Commands Cheatsheet

| Command                 | Description                                                               |
| ----------------------- | ------------------------------------------------------------------------- |
| `more` / `less`         | Read files directly from the command line, page by page.                  |
| `head`                  | Get the first lines of a file (default 10).                               |
| `tail`                  | Get the last lines of a file (default 10).                                |
| `sort`                  | Sort results alphabetically or numerically.                               |
| `grep "pattern"`        | Search for lines matching a pattern.                                      |
| `grep -v "pattern"`     | Exclude lines matching a pattern.                                         |
| `cut -d":" -f1`         | Extract a field from each line (`-d` = delimiter, `-f` = field position). |
| `tr "x" "y"`            | Replace occurrences of character `x` with character `y`.                  |
| `column -t`             | Auto-format input into aligned tabular columns.                           |
| `awk '{print $1, $NF}'` | Print specific fields — `$1` = first field, `$NF` = last field.           |