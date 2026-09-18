---
tags: [cheatsheet, regex]
module: Linux Fundamentals
---

# Regex Grouping Operators Cheatsheet

| Operator | Description                                                                           |
| -------- | ------------------------------------------------------------------------------------- |
| `(a)`    | Round brackets group parts of a regex — patterns inside are processed together.       |
| `[a-z]`  | Square brackets define a character class — a list of characters to search for.        |
| `{1,10}` | Curly brackets define a quantifier — a number/range for how often a pattern repeats.  |
| `\|`     | OR operator — matches when either of two expressions matches.                         |
| `.*`     | Acts like an AND operator — matches only when both expressions are present, in order. |