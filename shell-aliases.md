---
url: https://raw.githubusercontent.com/earendil-works/pi/main/packages/coding-agent/docs/shell-aliases.md
title: "Shell Aliases"
description: ""
access_date: 2026-08-03T18:13:42.033Z
current_date: 2026-08-03T18:13:42.033Z
---

# Shell Aliases

Pi runs bash in non-interactive mode (`bash -c`), which doesn't expand aliases by default.

To enable your shell aliases, add to `~/.pi/agent/settings.json`:

```json
{
  "shellCommandPrefix": "shopt -s expand_aliases\neval \"$(grep '^alias ' ~/.zshrc)\""
}
```

Adjust the path (`~/.zshrc`, `~/.bashrc`, etc.) to match your shell config.
