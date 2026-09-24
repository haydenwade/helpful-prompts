---
title: Skill Candidate Finder
date: 2026-09-22
tags: [skills, workflow]
---

## What it does
Audits your recent history with Claude to find recurring, structured tasks worth turning into a reusable skill — and tells you which one to build first.

## Prompt
```
Look back over the work I’ve asked you to do. Find recurring tasks I bring you repeatedly, where the facts change but the type of work stays similar. Exclude one-off requests.

For each task, tell me:
- What I ask for, in my own words
- What you produce
- How often I ask for it
- What I usually correct or rewrite

Then score each task from 0 to 2 against these five signs:

1. I repeat the same instructions.
2. The steps stay stable while the details change.
3. I provide knowledge Claude cannot infer.
4. I make the same correction each time.
5. I can clearly describe what good output looks like.

Show the score for each sign and the total out of 10. Be honest about which tasks are not worth turning into skills and explain why.

Rank the strongest candidates, recommend exactly one task to build first, and list the specific rules, preferences, and tacit knowledge I would need to write down.

If you cannot see enough of my history, say so and ask me to describe my typical week instead of guessing.
```

## Notes
Works best in a long-running conversation or project where Claude has visibility into repeated requests. If it can't see enough history, it will ask you to describe a typical week instead of guessing — let it.

If the AI says it can't find your past chats, check whether your account has a setting that lets it search or reference chat history (sometimes off by default) and turn it on before retrying — this applies to Claude and other AI chat tools alike.

## What's next
Once you've picked the top candidate, work through it interactively and correct the output as needed. Then use the ["Package Work Into a Skill"](package-work-into-a-skill.md) prompt to turn the corrected session into a skill.
