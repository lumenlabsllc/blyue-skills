---
name: write-tests
description: Generate a test file for a given source file
triggers: [write tests, add tests, generate tests, test coverage]
author: lumenlabsllc
homepage: https://github.com/lumenlabsllc/blyue-skills
license: MIT
tags: [testing, quality]
version: 1.0.0
---

When the user asks for tests:

1. Read the source file with read_file.
2. Detect the test framework from package.json or existing tests:
   - Node: jest, vitest, mocha, node:test
   - Python: pytest, unittest
   - Rust: built-in #[test]
3. Match the project's existing test file naming (foo.test.ts, test_foo.py).
4. Write tests covering:
   - Happy path for every public function
   - Edge cases: empty input, null/undefined, boundary values
   - Error paths: what happens when things throw
5. Only test the public API. Do not reach into internals.
6. Write the test file with write_file. Do not run it unless the user asked.

Keep tests focused — one assertion per behavior.
