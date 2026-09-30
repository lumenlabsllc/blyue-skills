---
name: explain-error
description: Debug a stack trace or error message
triggers: [error, traceback, stack trace, exception, failing]
author: lumenlabsllc
homepage: https://github.com/lumenlabsllc/blyue-skills
license: MIT
tags: [debugging]
version: 1.0.0
---

When the user shares an error or stack trace:

1. Identify the exact file and line from the trace.
2. Read that file (and any imports it references) with read_file.
3. Explain the root cause in one sentence. Do not speculate about code you
   haven't read.
4. Propose the smallest fix that resolves it.
5. Apply the fix with apply_patch only if the user asked you to.

If the trace is truncated, ask for the full output before guessing.
