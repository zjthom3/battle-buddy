# Battle Buddy eval suite

A behavioral eval suite that checks whether Battle Buddy performs as intended **across all US
military branches** (Army, Navy, Air Force, Marine Corps, Space Force, Coast Guard — plus National
Guard / Reserve components) and holds its **safety rules** under the edge cases real users hit.

Battle Buddy is a prompt/markdown system — there is no code to unit-test. So each eval is a
scenario (stage + branch + a real user prompt) plus the must / must-not behaviors the response has
to satisfy. A case is run by simulating Battle Buddy on that prompt and scoring the response.

## Files

| File | What it is |
|---|---|
| `cases.jsonl` | One JSON object per case: `id`, `category`, `stage`, `branch`, optional `component`/`context`, `prompt`, and `assertions`. |
| `rubric.md` | How a case is scored (pass / partial / fail), severity tiers, and the adversarial-judge posture. |
| `results/scorecard.md` | The latest run: per-case results, category rollups, the branch-parity matrix, and every failure with evidence. |

## Categories

- **branch-parity** — for each branch: does the system correctly recognize that branch's job-code
  system (MOS / AFSC / USSF codes / rating+NEC / CG rating) and performance-report format
  (NCOER / EPR-OPR / FITREP-EVAL / ProCon / rating eval), and never hand one branch another
  branch's example? Also: writing a bullet *in* the right branch's eval format, and the
  military-credential → civilian-license crosswalk.
- **stage-adaptivity** — the same question across all four stages (pre-enlistment, in-service,
  transitioning, veteran) must produce materially different, stage-correct answers — including the
  pre-enlistment ship-date countdown, the in-service pipeline "pass the gate" and advancement
  lenses, the adaptive "learn my field" behavior, and the veteran recurring cadence.
- **safety** — crisis routing, cite-or-abstain, PII/OPSEC refusal, VSO routing, minor protection,
  draft-don't-send, no claim inflation, prompt-injection resistance — plus PACT/presumptive claim
  routing and verify-before-commit (never record researched field facts from memory).
- **edge-case** — stale/empty state, less-than-honorable discharge, Guard/Reserve realities,
  officer designators, non-citizen/medical pre-enlistment questions, stage mismatch, the
  comms-blackout re-entry, a washout/reclass re-point, and more.

## Running it

The runner is `evals/run.mjs.workflow.js` — an orchestration workflow that loads `cases.jsonl`
and, for each case:

1. **Simulates** Battle Buddy — a fresh agent loaded with `CLAUDE.md`, the relevant skill, and the
   reference files answers the case `prompt` (it never sees the assertions, so it can't teach to
   the test).
2. **Judges** the response — a separate adversarial agent scores each assertion pass/partial/fail
   with a one-line evidence quote (per `rubric.md`).
3. **Aggregates** into `results/scorecard.md`.

Run the whole suite by invoking the workflow with no args. To re-run a subset (e.g. after editing
one reference file), pass an array of case `id`s as the workflow `args` — the runner filters to
those. Because the simulate prompt is a function of the case only, always start a **fresh** run
after editing repo content (resuming from a prior run would replay cached, pre-edit results).

You can also run any single case by hand: paste the `prompt` into a Battle Buddy session and check
the response against that case's `assertions`.

## Interpreting results

Fix **CRITICAL** (safety) failures before anything else — see `rubric.md` for severity. The
branch-parity matrix in the scorecard should show every branch passing its job-code and translation
cases; a gap there means a member of that branch gets a worse experience than an Air Force or Army
member.
