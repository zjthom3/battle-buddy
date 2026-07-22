---
name: next-move
description: The daily driver. Use when the person asks "what do I do next?", "what should I focus on?", "I'm stuck", "what now?", or just runs /next-move. Runs one honest OODA cycle against their stage, mission, and open loops, and returns the single most important next action — drafted, not just named. Output differs completely by stage.
---

## What this skill does

Runs **one OODA cycle** (`references/ooda-loop.md`) and produces **one next action**, ready to
act on. Not a list — the single highest-leverage thing right now, and the drafted first step. This
is the skill the person comes back to; it has to earn that.

**Stage changes everything.** Read `situation/stage.md` first. The same person's "next move" is a
different species of thing at each stage.

## Safety

- Crisis signal → Veterans Crisis Line first, nothing else (`references/crisis-resources.md`).
- Any dollar/deadline/eligibility figure in the answer is **fetched live from an official source
  and cited**, or replaced with "here's the official page to check." Never state one from memory
  (`CLAUDE.md`, rule 3).

## Execution — the four steps

### 1. Observe — read the real picture

Read: `situation/stage.md`, `situation/about-me.md`, `situation/ground-truth.md`,
`situation/career-field.md` (so the move speaks their actual field, not a generic one),
`mission/objective.md`, `mission/tasks.md` (done ledger **first**, so you don't re-serve finished
work), and `sustainment/` if relevant. Note the **key date** in `stage.md` — a **ship date**
(`pre-enlistment`) or a **separation date** (`transitioning`) both drive a backward countdown.

**Re-entry / life-changed check:** if the picture is stale or the plan just changed, the move *is*
re-pointing the system — say so to them, don't just note it. Cases:
- **Stale files / a key date now in the past** (a ship date that's passed → they're in basic or
  serving; a separation date that's passed → they're likely a veteran; a `Last updated` long ago):
  welcome them back and tell them to run **`/onboard`** to re-point before anything else.
- **They washed out, reclassed, or their field changed:** that's a real re-plan, not a failure to
  gloss. Tell them to re-run **`/onboard`** and **`/study-up`** on the new field, so the record and
  advice match who they actually are now. Be human first.
Either way, the drafted next action is the re-point itself.

### 2. Orient — interpret it against their stage

This is the step that makes the answer good. Apply the stage lens:

- **`pre-enlistment`:** the move is almost always *getting better information before a
  commitment* — a question to bring a recruiter, decoding a job code or contract term, ASVAB
  prep. Never push toward signing. If they have a **ship date**, count down to it: DEP is prep time
  (get in shape to the standard, lock contract details in writing, questions to still raise) and the
  move is whichever prep window closes soonest. If they're aiming at a pipeline (special warfare,
  aircrew, etc.), the move often lives in `situation/career-field.md` — run `/study-up` if it's thin.
  (`references/enlistment-path.md`, `branches-and-jobs.md`.)
- **`in-service`:** the move is *set up future-you* — the thing that's cheap now and expensive or
  impossible later. GI Bill transfer (must usually be done while serving), certs that map to a
  civilian field, saving, starting a degree, a SkillBridge plan. (`va-benefits-map.md`,
  `transition-timeline.md`.) **Two sub-contexts change the answer:**
  - *In a demanding pipeline / tech school right now* (selection, A-school, a wash-out-risk course)?
    Don't hand them "start a degree." The move is **pass the next gate, don't get hurt, recover** —
    future-setup waits for the first duty station. Read `career-field.md` for their gates.
  - *Chasing the next rank?* Advancement is a real move. Name what they **control** (PME, decorations,
    a PT test, the specialty-knowledge study) vs. what they don't (time-in-service/grade). Point to
    the official promotion page and cite any cutoff/points figure live — never state one from memory.
    (`references/rank-and-pay.md`.)
- **`transitioning`:** the move is *the next thing on the backward countdown from your separation
  date* — whichever time-boxed window closes soonest (TAP, SkillBridge, pre-discharge claim,
  health-care enrollment, DD-214 check). Verify the current window live. (`transition-timeline.md`.)
- **`veteran`:** the move is *claim what you're owed and turn service into a civilian result* — a
  benefit left on the table, a claim to start with a free VSO, a résumé/LinkedIn translation, a
  mentor match. (`va-benefits-map.md`, `veteran-orgs.md`, `translation-tables.md`.) Once the
  transition scramble is over, the value goes *recurring, not one-shot* — a claim-status check-in, a
  periodic benefits re-sweep, a community touchpoint (`comms/battle-rhythm.md`, the veteran cadence).
  And name the quiet-hard part honestly (`references/voice.md`): the identity shift out of the
  uniform and the seniority/pay reset are real — a settled result, not a failing.

Then pick: what moves the mission most, what unlocks other things, and what are they avoiding
because it's uncomfortable rather than unimportant?

### 3. Decide — name one action

State the single next action in one sentence. Small enough to start today, clear enough to know
when it's done. Say *why* this one (tie it to the mission and the stage).

### 4. Act — make it real

Don't stop at advice. Do the first step:
- If it's an email (to a recruiter, a VSO, a mentor, an employer) → draft it for their review.
- If it's a benefit question → fetch and cite the official current details.
- If it's a translation → run the first bullet.
- If it's a task → add it to `mission/tasks.md` open loops.

Draft, don't send (`CLAUDE.md`, rule 7).

## Output shape

Keep it phone-readable:

1. **Your next move:** one sentence.
2. **Why it's the one:** two lines, tied to mission + stage.
3. **Here's the start:** the drafted artifact / the cited fact / the added task.
4. **If you've got more time:** at most one secondary thing — optional, not a pile.

## Rules

1. **One move, not a list.** The discipline is the value.
2. **Stage-specific or it failed.** A generic answer that would fit anyone is a failure.
3. **Cite live for any figure.** No remembered numbers.
4. **Read the done ledger first.** Don't re-serve finished work.
5. **Close the loop.** When they tell you something's done, strike it in `mission/tasks.md` and
   append to the done ledger.
