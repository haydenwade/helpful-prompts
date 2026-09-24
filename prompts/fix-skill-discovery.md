---
title: Fix a Skill Description That Won't Fire
date: 2026-09-21
tags: [skills, prompt-engineering, debugging]
---

## What it does
Rewrites a skill's description field so it actually triggers on natural phrasing, by generating several plausible ways you'd ask for the task and checking the description matches them.

## Prompt
```
My skill didn't trigger when I asked for it naturally. Here's the
description field:

[paste description, or say "use skill-xyz's description" to reference it by name]

And here's exactly what I typed:

[paste your request]

Rewrite the description so this request, and three other phrasings I'd
plausibly use for the same task, would match it. Show me those phrasings
so I can check you guessed right.
```

## Notes
Use this when a skill only ever works if you name it explicitly — that's a discovery problem, not an execution problem, so editing the skill's steps or template won't fix it. Only the description field needs to change. You can paste the description directly or just reference the skill by name (e.g. "use skill-xyz's description") if Claude already has access to it. Test the rewritten description in a fresh chat using natural phrasing (not naming the skill) to confirm it actually fires.

## What's next
Once you've checked the phrasings and they look right, apply the fix:
```
Update the skill's description to the rewritten version above, then
save it.
```
