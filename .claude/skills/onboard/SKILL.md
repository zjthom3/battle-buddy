---
name: onboard
description: Use on first run of Battle Buddy, when someone says "set me up", "onboard me", "get started", or has just cloned the kit — and any time their situation changes (shipped to basic, PCS, separated). Stage-first interview that fills the situation/ and mission/ files. Idempotent; re-run any time.
---

## What this skill does

Sets up (or re-points) the whole system around the person. **Stage is the first question and it
drives everything** — a pre-enlistment setup and a veteran setup ask for different things and
produce different files. At the end, it points them at `/next-move` as the first real win.

Re-running is a first-class event, not an edge case: shipping to basic, a PCS, or separating all
change the stage, and the honest move is to re-run and re-point the system.

## Safety (read `CLAUDE.md` — these are non-negotiable here)

- **Refuse OPSEC/PII.** If the person offers an SSN, DoD ID, unit movements, deployment
  specifics, or clearance details, decline and explain why. Keep only résumé-safe record fields.
- **Minors.** A pre-enlistment user may be 17. Collect no PII, apply zero pressure toward
  enlisting, present real tradeoffs, and never contradict "talk to your parents / a trusted
  adult."
- **Crisis routing overrides the interview.** Any distress signal → Veterans Crisis Line first
  (`references/crisis-resources.md`).

## Execution

### Step 1 — Stage (always first)

Ask: **"Where are you on the journey right now?"**

1. Thinking about enlisting, or in the process → `pre-enlistment`
2. Currently serving → `in-service`
3. Separation or retirement is in sight → `transitioning`
4. Already out → `veteran`

Write it to `situation/stage.md` immediately, with the date. **Capture the key date** for the stage
and store it in the `Key date` field (it drives the `/next-move` countdown): `pre-enlistment` → the
**ship date** if they have one (DEP counts down to it just like transition counts down to
separation); `transitioning` → the **separation/target date**. Leave blank if there isn't one yet.

If re-running and the stage changed, back up the current `situation/`, `mission/`, `sustainment/`,
and `comms/` files to `archives/onboard-{YYYY-MM-DD-HHMM}/` before overwriting.

**Plan changed, not just stage?** A washout, reclass, or a pipeline that didn't pan out is a real
event, not a failure to hide — treat it like a stage change. Back up prior state, re-decode the new
path, and re-run the interview from where they actually are now. Then `/study-up` on the new field.
Re-entry after time away (basic, a deployment, a school with no contact) is the same move: if the
files are stale, welcome them back and re-point the system before serving advice.

### Step 2 — The interview (branch on stage)

Ask **one question at a time**, write answers as you go so the person can stop and resume. Keep
it to the essentials below — don't expand into a 20-question grind.

**All stages:**
- Who are you out of uniform, and what do you want next? → `situation/about-me.md`
- What's the real ground truth — family, time, money shape, hard constraints? →
  `situation/ground-truth.md` (no account numbers, just the shape)

**`pre-enlistment` — add:**
- What's drawing you to service, and which branches are you weighing?
- What matters more to you: a guaranteed job, a bonus, a ship date, a location?
- (Mission = an informed enlistment decision, not a signature. See `enlistment-path.md`.)

**`in-service` — add:**
- Branch, paygrade, job code, dates → `situation/service-record.md` (résumé-safe only)
- What are you setting up now for later — GI Bill transfer, certs, a degree, saving?
- (Flag early: GI Bill transfer to dependents usually must be set up *while serving*.)

**`transitioning` — add:**
- Branch, paygrade, job code, dates, awards → `situation/service-record.md`
- Separation date (if not already captured) and what "landed on my feet" looks like.
- Which track is loudest: a job, school, or starting something?

**`veteran` — add:**
- Branch, paygrade, job code, dates, awards → `situation/service-record.md`
- How long out, and what's the pressing thing — a claim, a job, school, benefits?

### Step 3 — Draft the mission

From what you heard, draft a one-sentence mission with a date and write it to
`mission/objective.md` — then read it back and let them correct it. A mission they can recite is
the goal.

### Step 4 — Seed the files

In one batch, fill: `situation/*`, `mission/objective.md`, and a first honest line or two in
`sustainment/benefits.md` (what's untouched) and `sustainment/people.md` (who's already in their
corner). Seed `situation/career-field.md` with the plain-English role and job code from the
interview, and note that `/study-up` will deepen it (pipeline, standards, certs) from official
sources. Leave `comms/battle-rhythm.md` with the starter rhythm — for a `veteran`, seed the veteran
cadence (a periodic `/benefits-check` re-sweep, claim-status check-ins, a community touchpoint) so the
kit still has a reason to be opened after the transition scramble ends.

### Step 5 — The first win

Close with three lines, not a menu:

```
✓ You're set up. Battle Buddy knows your stage, your record, and what you're driving at.

Now run: /next-move   — I'll give you the one thing to do next, ready to act on.
Want me to learn your specific field (pipeline, standards, certs)? Run /study-up.
Any time your situation changes (ship, PCS, reclass, separate), re-run /onboard.
```

Then, if they run `/next-move`, deliver a genuinely stage-specific first action (see that skill).

## Rules

1. **Stage first, always.** Never skip it; it's the spine of every other skill.
2. **One question at a time.** Write as you go.
3. **Idempotent.** Re-run refreshes; back up prior state on a stage change.
4. **Refuse PII/OPSEC in real time**, with a plain reason.
5. **No pressure on pre-enlistment users**, ever.
