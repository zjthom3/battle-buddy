---
name: benefits-check
description: A stage-aware sweep of what the person may be eligible for right now, every line cited to an official source. Use when they ask "what am I eligible for?", "what benefits am I missing?", "what am I leaving on the table?", "check my benefits", or run /benefits-check. Never states a rating, amount, or deadline from memory — verifies each against an official .gov page and cites it.
---

## What this skill does

Figures out which benefits are live for the person's stage, checks their personal status against
what they've already claimed, and — for each one that matters — **fetches the current
eligibility/amount/deadline from the official page and cites it**. Ends with the single most
worthwhile thing to act on and the exact link.

The reference file `references/va-benefits-map.md` is the *map* (what each benefit is + the
official URL). It deliberately contains **no numbers**. The numbers come live, here, at run time.

## Safety — this skill lives or dies on the cite rule

- **Cite or abstain.** Every eligibility rule, dollar amount, percentage, and deadline is
  fetched live from an official `.gov`/`.mil` source and cited by URL. If you can't verify it:
  *"I don't know the current figure — here's the official page,"* with the link. **Never** state
  one from memory or from an unverified web snippet (`CLAUDE.md`, rule 3).
- **Not a VSO / attorney / clinician.** Never predict a disability rating, never file anything.
  Claims work routes to a **free accredited VSO** (`references/veteran-orgs.md`).
- Crisis signal → Veterans Crisis Line first.

## Execution

1. **Read the person.** `situation/stage.md`, `situation/service-record.md`,
   `sustainment/benefits.md` (their status ledger). **Check the component** — if Reserve or
   National Guard, read `references/guard-reserve.md`; eligibility often hinges on qualifying
   active-duty (Title 10) time and several rules differ from active duty.

2. **Scope by stage.** Only surface what's actually relevant:
   - `pre-enlistment` → mostly education/future framing; be honest that benefits accrue *after*
     qualifying service. No overpromising.
   - `in-service` → the set-up-now items, especially **GI Bill transfer to dependents** (usually
     must be done while serving) and building toward the GI Bill/education path.
   - `transitioning` → the time-boxed windows: pre-discharge disability claim, health-care
     enrollment, plus setting up education/home-loan. Cross-check `references/transition-timeline.md`.
   - `veteran` → the full sweep: health care, disability, GI Bill (+ Rogers STEM), VR&E, home
     loan (COE), VALife, state/local benefits.

3. **For each relevant benefit:** open the official page from `va-benefits-map.md`, fetch the
   current eligibility/amount/deadline, and report it **with the citation**. Note where the person
   already stands (from their ledger) vs. what's open.

4. **Update the ledger.** Write findings and the "source checked" + date into
   `sustainment/benefits.md`.

5. **Land on one action.** The single highest-value thing to do now (e.g. "enroll in VA health
   care — here's the window and the link" or "start a claim with a free VSO — here's who").

## Output shape

- A short table: benefit · your status · what's current (cited) · next action.
- Then: **the one thing to do now**, with the exact official link.
- If anything involves a claim, name a specific **free** VSO to take it to.

## Rules

1. **No uncited figure, ever.** This is the whole safety posture of the skill.
2. **Stage-scoped** — don't dump the veteran sweep on a pre-enlistment user.
3. **Route claims to a free VSO.** Never imply Battle Buddy files or rates.
4. **Update `sustainment/benefits.md`** so the picture compounds over time.
