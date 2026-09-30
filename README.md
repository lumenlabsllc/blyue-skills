# BLYUE Skills

**Community skill store for BLYUE Code — the LUMEN terminal coding agent**

[![npm](https://img.shields.io/npm/v/blyuecode)](https://www.npmjs.com/package/blyuecode)
[![license](https://img.shields.io/badge/license-MIT-blue)](./LICENSE)

---

## What is a skill?

A skill is a markdown file with a small YAML header. BLYUE loads it into its
system prompt when a trigger keyword matches your message, or when you run
`/skill <name>`.

## Install

Open BLYUE and run `/skillstore`. Arrow keys to browse, `i` to install,
`u` to update all, `esc` to close.

## Available skills

| Skill | Description |
|---|---|
| commit-message | Write a conventional commit message from staged changes |
| explain-error | Debug a stack trace or error message |
| review-pr | Review a GitHub PR diff and post structured feedback |
| write-tests | Generate a test file for a given source file |

## Contributing

1. Fork this repo
2. Add `skills/<your-skill>/SKILL.md` with frontmatter
3. Add an entry to `index.json`
4. Open a PR

## License

MIT — see LICENSE.

Built by LUMEN Labs.
