---
name: study-up
description: Teach the kit the person's specific world — their job code, training pipeline, standards, certs, and community. Use when they name a career field, MOS/AFSC/rating, a pipeline or selection course (PJ, SF, SEAL, aircrew, EOD, nuke, corpsman, cyber…), say "learn my job", "get smarter about my field", "add my certs", or when another skill hits a person-specific gap it can't fill generically. Researches official sources, confirms with the person, and records it cited into situation/career-field.md.
---

## What this skill does

There is no single "military experience," so this kit doesn't ship one. `/study-up` is how the kit
gets smarter about **this** person — their actual job, the pipeline they're in, the standards they
have to hit, the certs they're earning, the community around them. It **researches official sources,
reads what it found back to the person, and records only what they confirm** — every fact cited —
into `situation/career-field.md`. Over time each person's kit grows to fit them.

This is the same discipline `/benefits-check` uses (research official source → cite by URL → write to
a personal file), pointed at the person's *field* instead of their benefits.

## Safety (read `CLAUDE.md` — non-negotiable here)

- **Cite or abstain, then verify before you commit (Rule 3).** Every recorded fact is fetched from an
  official `.gov`/`.mil`/branch-careers source and cited. A pipeline's stage list, a fitness
  standard, a rep count, a score, a deadline — those are **catalog content that changes** (see
  `references/branches-and-jobs.md`, "Read the shape, not the catalog"). Never write one from memory.
  If you can't verify it live, leave it blank and record the official page to check instead.
- **Read it back before writing.** Show the person what you found and the source; write to their file
  only after they confirm it's right. Draft, don't commit silently (Rule 7).
- **OPSEC/PII (Rule 4).** Record the résumé-safe shape of a field — not unit movements, deployment
  specifics, or anything classified. If researching their path surfaces sensitive detail, keep it out
  of the file.
- **Crisis signal → Veterans Crisis Line first** (`references/crisis-resources.md`), before anything.

## Execution

### 1. Find the gap
Read `situation/stage.md`, `situation/service-record.md`, and `situation/career-field.md`. What does
the kit not yet know about this person's world? Common triggers: a decoded job code, a training
pipeline they're entering, a new cert they earned, a field-specific community/resource, or a
question another skill couldn't answer generically.

### 2. Research it — official sources, cited
Pull from official sources and cite each: branch careers sites (`references/branches-and-jobs.md` has
the list), the official special-warfare/pipeline worksheet, `.gov`/`.mil` pages, DoD COOL for
credentialing. Decode the **shape** from knowledge; fetch the **specifics** (stages, standards,
titles, scores) live. If a fact isn't verifiable right now, say so and capture the link, not a guess.

### 3. Read it back and confirm
Show the person plainly: "Here's what I found about your field, and where it came from — does this
match your reality?" Correct anything they flag. Nothing goes into the file unconfirmed.

### 4. Record it (cited)
Write the confirmed facts into `situation/career-field.md`: the plain-English role, the decoded code,
the pipeline shape, the standards (named, with the official worksheet as source of truth), certs
earned/targeted, field community/resources, and the transferable core for `/translate`. Fill the
**Researched & cited** table — what you learned · official source · date confirmed. Stamp
`**Last updated:**`. On a big field change (reclass, new pipeline), archive the prior file to
`archives/study-up-{YYYY-MM-DD-HHMM}/` first, like `/onboard` does.

### 5. Hand off
Point to the skill that now works better: `/next-move` (stage-correct advice that speaks their field),
`/translate` (their certs and record → civilian, with the crosswalk), or `/benefits-check`.

## Certs, as they're earned

When the person earns or is about to earn a cert (paramedic/NREMT, dive, airborne, A&P, CDL, cyber,
language), log it under certs and flag the civilian value: **preserve the documentation now** for
licensure/reciprocity later. Prompt them to tell you when new ones land — and if they mention one, add
it. Don't state state-by-state licensure rules from memory; point to the official credentialing page
and cite it.

## Rules

1. **Verify before you commit.** Cited + confirmed, or it doesn't get written.
2. **Shape from knowledge, specifics from the official source.** Never recite pipeline/standard numbers from memory.
3. **Generic references, specific person-file.** New knowledge about *this person* lives in *their* `career-field.md`, not in `references/`.
4. **Idempotent.** Re-run to deepen; archive prior state on a field change.
