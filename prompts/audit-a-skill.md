---
title: SKILL.md Audit
date: 2026-09-21
tags: [skills, prompt-engineering, audit]
---

## What it does
Audits a SKILL.md file against six requirements for well-structured skills (timeframe rules, citations, few-shot examples, output format, input handling, numbered verification steps), gives exact lines to add for anything weak or missing, and trims explanations Claude already understands.

## Prompt
```
Audit this SKILL.md against these six requirements:

1. Clear timeframe rules
2. Citation or source requirements
3. Few-shot input → output examples
4. An explicit output format
5. A description of expected inputs and what to do when they're missing
6. Numbered steps with at least one verification step

[paste SKILL.md here or attach it or state skill name]

For each requirement, label it as present, weak, or missing.

For anything weak or missing, write the exact lines I should add. Do not just describe the improvement.

Then remove anything that explains concepts Claude already understands. Tell me the before and after line count.
```

## Notes
Replace the placeholder line with the target skill: paste the SKILL.md content directly, attach the file, or just name an installed skill Claude already has access to. Best for a skill already in use that needs frequent corrections or gives inconsistent results — not first-time authoring.

## What's next
Once you've reviewed the findings, apply them:
```
Update the skill to fix the gaps identified above.
```
