# Battle Buddy

**An AI operating system for the whole military journey — from "should I enlist?" to "I've been
out for years."**

Battle Buddy is a free, open kit you run inside [Claude Code](https://claude.com/claude-code). It
turns Claude into a coach and executive assistant that knows where you are on the journey and
tells you your next move — in plain language, with the real sources, and without the hype.

It's built for four kinds of people, and it changes what it does for each:

- **Thinking about enlisting** — what to ask a recruiter, what's actually negotiable, what the
  job codes mean before you sign anything.
- **In the Delayed Entry Program or already serving** — what to set up *now* so future-you isn't
  scrambling at transition.
- **Transitioning out** — a countdown against your real separation date: TAP, SkillBridge,
  claims, terminal leave, the DD-214, and the benefits windows you can't afford to miss.
- **A veteran** — what you're still eligible for, what you're leaving on the table, and how to
  turn your service into civilian-readable language for a résumé, LinkedIn, or an interview.

## Why it's shaped like an operation

If you've served, you already think this way — so the system is built on doctrine you already
know, not on business-guru jargon:

- The repo is laid out like an **OPORD** (Situation, Mission, Execution, Sustainment, Command &
  Signal).
- The "what do I do next?" engine runs an **OODA loop** (Observe, Orient, Decide, Act).
- Recurring things run on a **battle rhythm**.
- You review your own setup with an **AAR**.

None of that is costume — every piece is a real framework, used the way it's actually meant to be
used.

## The honest part up front

- **This is not the VA, the DoD, or any branch.** It's a free tool made by one veteran.
- **It never guesses at your benefits.** Anything with a dollar amount, a deadline, or an
  eligibility rule gets pulled live from an official `.gov`/`.mil` page and cited — or it tells
  you it doesn't know and hands you the link. It will never make up a number.
- **It's not legal, medical, or financial advice.** For claims, it points you to a **free**
  accredited VSO — never a paid "claim shark."
- **If you're in crisis, it stops and gets you the Veterans Crisis Line** (dial **988**, then
  press **1**; or text **838255**) before anything else.

## Your data stays yours

Once you run `/onboard`, Battle Buddy fills in your files with your real life — your record, your
goals, your people. **That stays on your machine.** If you ever push your copy somewhere public,
scrub the `situation/`, `mission/`, `sustainment/`, and `comms/` folders first. It never asks for
your SSN, DoD ID, or anything OPSEC-sensitive.

## Quick start

1. **Install Claude Code** (`claude.com/claude-code`) — one-time setup. New to the terminal?
   That's expected; the setup is the part a human can walk you through.
2. **Clone this repo** and open it in Claude Code.
3. **Run `/onboard`.** It asks where you are on the journey first, then a handful of questions,
   and sets the system up around you. ~10 minutes.
4. **Run `/next-move`.** That's the one you'll come back to. It gives you your single most
   important next action, ready to act on.

## What ships

| Command | What it does |
|---|---|
| `/onboard` | Sets up (or re-points) the system. Asks your stage first. Re-run it any time your situation changes. |
| `/next-move` | One OODA cycle → your single next action. The daily driver. |
| `/translate` | Military ↔ civilian, both directions. Record → résumé/LinkedIn/interview; or job posting → what they're really asking for. |
| `/benefits-check` | A stage-aware sweep of what you may be eligible for, every line cited to an official source. |
| `/aar` | An after-action review of your own setup — what's in place, what's missing, what to fix first. |
| `/level-up` | Weekly: find one repetitive task and build a shortcut for it. |

## License & credit

MIT © 2026 Zachary Thomas. Use it, fork it, build on it.

Inspired by the AIOS pattern popularized by Nate Herk.
