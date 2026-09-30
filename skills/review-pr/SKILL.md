---
name: review-pr
description: Review a GitHub PR diff and post structured feedback
triggers: [review pr, review this pr, pr review, code review]
author: lumenlabsllc
homepage: https://github.com/lumenlabsllc/blyue-skills
license: MIT
tags: [git, github, review]
version: 1.0.0
---

When the user asks you to review a PR:

1. Ask which PR (number or URL) if not specified.
2. Run `gh pr view <n> --json title,body,files` to get metadata.
3. Run `gh pr diff <n>` to get the full diff.
4. Review for, in order of severity:
   - Correctness: logic errors, edge cases, off-by-ones
   - Security: injection, secrets in code, unsafe deserialization
   - Performance: N+1 queries, unnecessary allocations, blocking I/O
   - Tests: does the change have tests? do they cover the new paths?
   - Style: matches project conventions, dead code, naming
5. Output a numbered list of findings. Each finding: file:line, severity
   (blocker / major / minor / nit), one-sentence description, suggested fix.
6. End with an overall verdict: approve, request changes, or comment.

Do not restate the diff. Review only.
