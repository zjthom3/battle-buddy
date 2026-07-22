---
name: aar
description: An after-action review of the person's own setup and progress. Use when they say "how's my setup", "review my progress", "run an AAR", "what am I missing", "is this working", or run /aar. Read-only. Checks whether each OPORD layer is in place and current, then reports what was supposed to happen / what happened / why / what changes.
---

## What this skill does

The AAR is the ritual every service member knows: an honest look at what was supposed to happen,
what actually happened, why the gap, and what changes next time. Here it does double duty —
auditing whether the **system itself** is set up right, and reviewing **progress** against the
mission. Read-only: it reports and recommends; it doesn't change files.

## Execution

### Part 1 — Is the system in place? (audit the OPORD layers)

Walk the five layers and rate each **in place / thin / missing**:

| Layer | In place means… | Check |
|---|---|---|
| Situation | Stage set, record + about-me + ground-truth filled | `situation/` |
| Mission | A one-sentence mission with a date exists and still fits | `mission/objective.md` |
| Execution | They've actually run the skills, not just installed them | recent activity |
| Sustainment | Benefits status is tracked; real people are in `people.md` | `sustainment/` |
| Command & Signal | A battle rhythm exists and is being kept | `comms/battle-rhythm.md` |

Flag anything stale — e.g. a `transitioning` stage with a separation date now in the past means
it's time to re-run `/onboard`.

### Part 2 — Progress against the mission (the real AAR)

1. **What was supposed to happen** — the mission and the open loops from `mission/tasks.md`.
2. **What happened** — the done ledger; what actually moved.
3. **Why** — the honest read on the gap. Was it the wrong plan, a real blocker, or avoidance?
4. **What changes** — the one or two adjustments that make next week better. If a skill or task is
   never getting used, say so.

## Output shape

- **Setup scoreboard:** five layers, each in place / thin / missing, with the top gap called out.
- **The AAR:** supposed-to / happened / why / changes — short and honest.
- **The one fix:** the single highest-leverage thing to close before next review. Hand it to
  `/next-move` as the follow-through.

## Rules

1. **Read-only.** Report and recommend; don't edit files. (Suggest the person or `/next-move`
   make the change.)
2. **Honest, not flattering.** A clean scoreboard nobody uses is worse than a messy one that
   moves the mission. Say the true thing.
3. **End with one fix**, not a backlog.
