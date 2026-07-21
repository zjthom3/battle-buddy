---
name: level-up
description: Weekly — find one thing the person does by hand over and over and build a shortcut for it. Use when they say "level up", "what should I automate", "make this easier", "I keep doing this manually", or run /level-up. Runs an OODA cycle aimed at their own workflow and ships one small improvement.
---

## What this skill does

Once a week, find the single most repetitive or annoying thing in the person's routine and make
it easier — a saved template, a reusable prompt, a small new skill, a checklist. One run = one
shipped improvement. It's the same OODA loop (`references/ooda-loop.md`) turned on their own way
of working.

This is what keeps Battle Buddy compounding instead of sitting still: the person's system gets a
little more capable every week, shaped to how *they* actually operate.

## Execution

### Observe — what keeps repeating?

Look at recent activity and ask: what has the person done by hand more than a couple of times?
What do they dread, put off, or re-type from scratch each time? Prompt them directly: "What did
you do this week that felt like the third time you'd done the same thing?"

### Orient — is it worth automating?

Pressure-test before building (don't automate a thing that shouldn't exist):
- Does this actually recur, or did it just feel annoying once?
- Is the manual version even the right thing to do?
- What's the smallest shortcut that removes most of the pain?

Sort the candidate:
- **Eliminate** — should this even happen? Kill it if not.
- **Templatize** — a reusable draft/checklist in `references/` or `templates/`.
- **Skill** — worth a small new `.claude/skills/` entry if it's multi-step and recurring.

### Decide — pick one

The one that saves the most annoyance for the least build. Small and shipped beats big and
someday.

### Act — build it this session

Actually make the artifact — write the template, draft the reusable prompt, or scaffold the small
skill — and show the person how to trigger it. Don't leave it as "you could build…"; leave it
built.

## Output

- **The pattern spotted:** the repetitive thing, named.
- **The shortcut shipped:** the actual file/template/skill, ready to use.
- **How to trigger it:** one line.
- Log it in `decisions/log.md` if it changed how the system works, and add it to the battle
  rhythm if it's recurring.

## Rules

1. **Ship one thing.** Not a roadmap — a built artifact.
2. **Pressure-test first.** Eliminate before you automate.
3. **Small and real** beats ambitious and unfinished — that's the whole habit.
