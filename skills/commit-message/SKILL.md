---
name: commit-message
description: Write a conventional commit message from staged changes
triggers: [commit, commit message, git commit]
author: lumenlabsllc
homepage: https://github.com/lumenlabsllc/blyue-skills
license: MIT
tags: [git, workflow]
version: 1.0.0
---

When the user asks for a commit message:

1. Run `git diff --staged` to see staged changes. If nothing is staged, run
   `git status` and tell the user.
2. Run `git log --oneline -10` to match the project's commit style.
3. Write a Conventional Commits message:
   - type: feat, fix, docs, style, refactor, test, chore
   - format: `type(scope): subject`
   - subject: under 72 characters, imperative mood, no trailing period
   - body: only if the change needs explanation; wrap at 72 columns
4. Output only the message. No preamble, no markdown fence.
