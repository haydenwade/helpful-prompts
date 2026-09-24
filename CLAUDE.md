# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A content library, not a codebase — a collection of standalone prompts, one per file under `prompts/`, each linked directly from LinkedIn posts/comments. There is no build, lint, or test step; the only artifacts are markdown files.

## Structure

- `prompts/<slug>.md` — one prompt per file, filename is the slug only (no date prefix).
- Related prompts may be grouped into a subfolder, e.g. `prompts/skill-building/<slug>.md`, when there are enough of them to warrant it.
- Each prompt file follows this format:

```markdown
---
title: <Title>
date: YYYY-MM-DD
tags: [tag1, tag2]
---

## What it does
One or two sentences on the use case.

## Prompt
\`\`\`
<the actual prompt text>
\`\`\`

## Notes
Optional: when to use it, expected output, tweaks.
```

## Adding a new prompt

Use the `add-prompt` skill (`.claude/skills/add-prompt/`) rather than editing files by hand — it encodes the file format and naming convention above.
