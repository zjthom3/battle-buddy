---
name: translate
description: Military ↔ civilian translation, plus writing eval bullets in military format. Use when the person says "translate my experience", "make me a résumé bullet", "fix my LinkedIn", "what does this job posting mean", "decode this MOS/AFSC", "help me write my EPR/NCOER/eval bullets", "does my cert transfer to a civilian license", or pastes performance-report bullets, a job code, an award citation, or a civilian job posting. Turns service into civilian-readable language, decodes a posting into what they already have, or drafts performance-report bullets in their branch's format.
---

## What this skill does

Re-encodes real military experience into the language a civilian hiring manager scores — and runs
in reverse, decoding a civilian posting into "here's what they're actually asking for and what you
already did." Method and patterns live in `references/translation-tables.md`.

The point is fidelity, not inflation: translate true accomplishments accurately. It has to survive
an interview and a reference check.

## Inputs it handles

- Performance-report bullets from **any branch** — NCOER/OER (Army), EPR/OPR (Air Force & Space
  Force), EVAL/FITREP (Navy & Coast Guard), FITREP/ProCon (Marine Corps)
- A job code from **any branch** — MOS (Army/Marines), AFSC (Air Force), USSF specialty code
  (Space Force), rating + NEC (Navy), rating (Coast Guard), or an officer designator — plus what
  it actually did. (Recognize the branch's system; decode the code's *shape*, not catalog specifics
  from memory — see `references/branches-and-jobs.md`.)
- An award citation
- A whole role or career, for a résumé/LinkedIn pass
- **Reverse:** a pasted civilian job posting

## Execution

### If translating record → civilian (Direction 1)

1. Read `situation/service-record.md`, `situation/about-me.md`, and `situation/career-field.md` (if
   filled — it holds the decoded field and the certs) for context and the target field.
2. For each bullet or role, apply the transform: strip acronyms → lead with the outcome →
   quantify the scale (people, budget/equipment value, volume) → name the transferable skill.
3. Aim output at the field in `about-me.md` (a cyber résumé and a logistics résumé pull different
   threads from the same service).
4. Return civilian bullets, plus LinkedIn-ready phrasing and a first-person interview answer if
   asked.
5. **Credential crosswalk.** If their record/`career-field.md` shows a cert or qual that maps to a
   civilian credential (medic → NREMT/paramedic license, corpsman/68W likewise, dive, A&P, CDL,
   cyber certs, MP → state POST), say so — it's often their highest-value transferable asset. Point
   to the **official** credentialing/reciprocity page (e.g. DoD COOL, the state licensing board) and
   have them verify there. Don't state state-by-state licensure rules or reciprocity from memory —
   cite or abstain (`CLAUDE.md`, rule 3). This is a lead to verify, not a promise. **Tell them to
   preserve the documentation now** — training records, cert cards, course completions, the DD-214 —
   because licensure boards ask for proof, and it's far easier to hold onto than to recover later.

### If decoding a posting → their fit (Direction 2)

1. Read the posting back in plain terms — what the day-to-day really is.
2. Map each requirement to something they already did in uniform (usually more matches than they
   expect).
3. Separate real gaps (a specific tool/cert) from fake gaps (civilian words for something they've
   done for years).
4. Draft honest "why me" language connecting service to the need.

### If writing a performance-report bullet → military format (Direction 3)

Someone still in uniform faces the most-repeated writing task of a career: eval bullets, every
cycle. This runs the transform *in reverse* — from what they did into their **branch's** eval format
(NCOER/OER, EPR/OPR, EVAL/FITREP, FITREP/ProCon — recognize the right one; see
`references/translation-tables.md`, and never hand one branch another's format).

1. Get the raw material: what they led or did, the scale (people, $/equipment, volume), the result.
2. Build the bullet: **action (strong verb) → scope/scale → measurable result.**
3. Keep it **OPSEC-safe** — no place names, unit movements, dates, or mission specifics; accomplishment,
   scale, and impact only (`CLAUDE.md`, rule 4).
4. **Use only what they gave you (rule 6).** Never manufacture the result to fill the format — no
   inventing "team certified mission-ready," "zero downtime," "set the standard," or a percentage they
   didn't state. If a bullet needs a result the person hasn't provided, **leave it as a `[ bracket ]`
   and ask them for the real number** rather than filling it in. A true bullet with a gap beats a
   polished one that won't survive their supervisor.
5. It's a **draft** for their review; they own the wording (rule 7). Bonus: these outcome-first
   bullets `/translate` cleanly into civilian résumé lines later.

## Guardrails

- **Truth only.** Never invent a result, inflate a role, or claim a skill they don't have.
- **Draft, don't send** — output is for their review (`CLAUDE.md`, rule 7).
- **They approve every word.** Battle Buddy proposes; the person owns their story.
- Match *their* voice for anything outward-facing (`situation/about-me.md`), not the coaching
  register.

## Nice-to-close

If the translation produces something reusable (a finished résumé section, a LinkedIn headline),
offer to save it and note the win in `mission/tasks.md`.
