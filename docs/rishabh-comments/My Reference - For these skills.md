---
name: My Reference - For these skills
description: Which of these skills you type yourself, and which only feed other skills.
tags:
  - source/ai-generated/claude-code
  - source-trust/unverified
rating:
related_notes:
  - "[[_MOC_rishabh-comments]]"
---

# Skills You Use, and Skills That Only Feed Other Skills

````ad-question
title: Question
What skills are user-facing and should be used by me, and what are just reference skills for other skills to use?
````

Only four are true reference skills. Everything else is for you.

## Reference layer — do not type these (4)

These hold vocabulary and method. Other skills consume them. Typing them alone gives you definitions, not work.

| Skill | What it holds | Who consumes it |
| --- | --- | --- |
| `/domain-modeling` | Glossary and ADR rules | `/grill-with-docs` |
| `/codebase-design` | Words for module shape (depth, seam, adapter) | `/tdd`, `/improve-codebase-architecture` |
| `/grilling` | The interview method itself | `/grill-me`, `/grill-with-docs`, `/triage`, `/wayfinder` |
| `/writing-for-agents` | Rules for writing skills and AGENTS.md | Used when editing skill files |

The `/ask-matt` map says this itself. It calls `/domain-modeling` and `/codebase-design` the "vocabulary underneath," and calls `/grilling` a primitive that two named skills wrap.

## Your skills — type these (18)

- **Start and shape work:** `/grill-with-docs`, `/grill-me`, `/wayfinder`, `/research`, `/prototype`, `/to-questionnaire`
- **Turn thinking into a build:** `/to-spec`, `/to-tickets`, `/implement`, `/tdd`, `/code-review`
- **Handle incoming and broken things:** `/triage`, `/improve-codebase-architecture`
- **Run the session:** `/ask-matt`, `/wait-what`, `/handoff`, `/teach`
- **Once, at setup:** `/setup-matt-pocock-skills`

## The honest edge case

`/wizard` sits between two groups. It writes a setup script for steps only a human can do. I start it when I hit a wall, but you can also type it. Call it yours.
