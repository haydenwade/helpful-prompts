---
name: add-prompt
description: Add a new prompt to this repository's prompts/ directory, following the standard file format and naming convention. Use when the user wants to save, add, or create a new prompt for the helpful-prompts collection.
---

Prompts live one-per-file under `prompts/`, named `slug.md` (lowercase, hyphen-separated, no date prefix). Related prompts may live in a subfolder, e.g. `prompts/skill-building/<slug>.md` — check for an existing subfolder that fits the new prompt's topic before defaulting to the top level.

To add a new prompt:

1. Create `prompts/<slug>.md` (or `prompts/<subfolder>/<slug>.md` if it belongs with an existing group) using this format:

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

2. Use today's date for the `date` field.
3. Keep the prompt text itself verbatim — don't edit or "improve" it unless asked.
4. No index file needs updating; the `prompts/` directory structure is the index.
