---
tags: [linux, permissions, chmod, chown]
module: Linux Fundamentals
---

# Permission Management

Linux's permission system is based on the octal number system. Three permission types can be assigned to a file or directory:

- `r` — Read
- `w` — Write
- `x` — Execute

## chmod
Modifies permissions using permission group references and `+`/`-` to add or remove them:
- `u` — owner
- `g` — group
- `o` — others
- `a` — all users

## chown
Changes the owner and/or group assignment of a file or directory:

## Related
- [[text-filtering]]