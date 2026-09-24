---
title: Package a Conversation Into a Skill
date: 2026-09-21
tags: [skills, prompt-engineering, workflow]
---

## What it does
After working through a task interactively with Claude, packages the whole back-and-forth (including corrections you made) into a reusable SKILL.md — with the description written around phrases you'd actually type, an explicit output template, and worked examples.

## Prompt
```
Package what we just did into a skill.

Before you write it:
- List the corrections I made and turn each into an explicit rule.
- Write the description so it names the trigger phrases I'd actually
  type, not just what the skill does.
- Include the output template verbatim and two short input → output examples.
- Say what the skill should do when a required input is missing.

Keep SKILL.md tight, no explanations of things you already know.
Show me the SKILL.md before saving it.
```

## Notes
Run this at the end of a session where you corrected Claude's output a few times on a repeatable task — those corrections are the raw material the skill needs. Review the generated SKILL.md and delete any line that just explains a general concept rather than telling Claude something about how you specifically work, before saving it.

## What's next
Save the skill:
```
Save that skill.
```
Then, in a fresh chat, ask for this task using natural phrasing without naming the skill — confirm it fires automatically. If it doesn't fire on its own, that's a discovery problem, not an execution one — see the ["Fix a Skill Description That Won't Fire"](fix-skill-discovery.md) prompt.
