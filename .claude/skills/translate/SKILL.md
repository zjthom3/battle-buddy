---
name: translate
description: Military ↔ civilian translation, both directions. Use when the person says "translate my experience", "make me a résumé bullet", "fix my LinkedIn", "what does this job posting mean", "decode this MOS/AFSC", or pastes performance-report bullets, a job code, an award citation, or a civilian job posting. Turns service into civilian-readable language, or decodes a posting into what they already have.
---

## What this skill does

Re-encodes real military experience into the language a civilian hiring manager scores — and runs
in reverse, decoding a civilian posting into "here's what they're actually asking for and what you
already did." Method and patterns live in `references/translation-tables.md`.

The point is fidelity, not inflation: translate true accomplishments accurately. It has to survive
an interview and a reference check.

## Inputs it handles

- Performance-report bullets (EPR / OPR / NCOER)
- A job code (MOS / AFSC / rating / NEC) + what it actually did
- An award citation
- A whole role or career, for a résumé/LinkedIn pass
- **Reverse:** a pasted civilian job posting

## Execution

### If translating record → civilian (Direction 1)

1. Read `situation/service-record.md` and `situation/about-me.md` for context and the target
   field.
2. For each bullet or role, apply the transform: strip acronyms → lead with the outcome →
   quantify the scale (people, budget/equipment value, volume) → name the transferable skill.
3. Aim output at the field in `about-me.md` (a cyber résumé and a logistics résumé pull different
   threads from the same service).
4. Return civilian bullets, plus LinkedIn-ready phrasing and a first-person interview answer if
   asked.

### If decoding a posting → their fit (Direction 2)

1. Read the posting back in plain terms — what the day-to-day really is.
2. Map each requirement to something they already did in uniform (usually more matches than they
   expect).
3. Separate real gaps (a specific tool/cert) from fake gaps (civilian words for something they've
   done for years).
4. Draft honest "why me" language connecting service to the need.

## Guardrails

- **Truth only.** Never invent a result, inflate a role, or claim a skill they don't have.
- **Draft, don't send** — output is for their review (`CLAUDE.md`, rule 7).
- **They approve every word.** Battle Buddy proposes; the person owns their story.
- Match *their* voice for anything outward-facing (`situation/about-me.md`), not the coaching
  register.

## Nice-to-close

If the translation produces something reusable (a finished résumé section, a LinkedIn headline),
offer to save it and note the win in `mission/tasks.md`.
