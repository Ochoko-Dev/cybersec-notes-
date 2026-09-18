---
tags: [linux, filtering, command-line]
module: Linux Fundamentals
---

# Filtering & Reading Files

Reading files directly from the command line — tools: `more` and `less`.

## /etc/passwd
Acts like a phone directory for users on the system — includes username, user ID, group ID, home directory, and default shell.

## Building a Filtering Pipeline
Starting from a raw file and narrowing down to clean, structured output:

1. **grep** — search for lines matching a pattern, or exclude with `-v`:
   Excludes users with a disabled shell (`/bin/false` or `/usr/bin/nologin`).

2. **cut** — extract specific fields from each line:`-d` sets the delimiter, `-f` sets the field/column to output.
3. **tr** — translate/replace characters:Replaces every colon with a space, making the output space-delimited.
4. **column -t** — format into aligned columns:
5. **awk** — process text pattern-by-pattern and print specific fields:
cat /etc/passwd | grep -v "false|nologin" | tr ":" " " | awk '{print $1, $NF}'
   `$1` = first field, `$NF` = last field (Number of Fields). Prints username and default shell for each user.

## Related
- [[linux-filtering-commands]] (cheatsheet)
- [[regular-expressions]]