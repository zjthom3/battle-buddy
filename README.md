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

## Start here — never done this before?

If you've never installed a tool like this or opened a terminal, you're in the right place. This
walkthrough assumes zero experience. Take it one step at a time; it's about 15 minutes end to end,
and you can stop and come back.

> **Rather not touch a terminal?** Claude Code also runs as a **[desktop app](https://claude.com/download)**
> (Mac/Windows/Linux) and on the **[web](https://claude.ai/code)** — same Battle Buddy, no command
> line. Install one of those and pick up at **Step 2**.
>
> New to the terminal but want to learn it? Anthropic has a
> **[beginner terminal guide](https://code.claude.com/docs/en/terminal-guide)**. And once Claude Code
> is running, you can just **tell it you're new** — it'll slow down and walk you through anything.

### Step 0 — What you'll need

- A computer (Mac, Windows, or Linux) and about 15 minutes.
- A **paid Claude plan** — Pro, Max, Team, or Enterprise — **or** a
  [Claude Console](https://console.anthropic.com/) (pay-as-you-go API) account. Heads up: the **free
  Claude.ai plan does not include Claude Code.** See [plans](https://claude.com/pricing).
- **No coding knowledge.** You'll type a couple of setup commands, then everything else is plain
  English.

### Step 1 — Install Claude Code

Open your Terminal (Mac/Linux) or PowerShell (Windows) and paste **one** line:

```bash
# macOS / Linux
curl -fsSL https://claude.ai/install.sh | bash
```

```powershell
# Windows (PowerShell)
irm https://claude.ai/install.ps1 | iex
```

Prefer clicking to typing? Download links and every other install method are on
**[claude.com/claude-code](https://claude.com/claude-code)** and the
**[setup guide](https://code.claude.com/docs/en/setup)**.

To confirm it worked, run `claude --version` — you should see a version number:

```text
$ claude --version
2.1.x (Claude Code)
```

<!-- screenshot: 01-install-version.png -->
*(screenshot: the version line after install)*

### Step 2 — Get Battle Buddy onto your computer

**If you have git** (or just installed Claude Code, which sets it up for you), paste:

```bash
git clone https://github.com/zjthom3/battle-buddy.git
cd battle-buddy
```

**No git, or not sure?** On this page, click the green **Code** button ▸ **Download ZIP**, then
unzip it. You'll get a folder called `battle-buddy`. That's your copy.

```text
battle-buddy/        ← this folder is yours now
├── README.md
├── situation/       ← where you are on the journey (fills in during setup)
├── mission/         ← what you're driving at
└── ...
```

<!-- screenshot: 02-repo-folder.png -->
*(screenshot: the battle-buddy folder / the clone finishing)*

### Step 3 — Open it and log in

From **inside** the `battle-buddy` folder, start Claude Code:

```bash
claude
```

The first time, it opens your browser to log in to your Claude account. After that you're in —
you'll see a prompt showing the model and the folder you're in. Type a `/` to see everything
Battle Buddy can do.

```text
 Welcome to Claude Code
 model: claude-opus-4-8 · cwd: ~/battle-buddy

 > /
   /onboard      Set up (or re-point) the system. Start here.
   /next-move    Your single next action, ready to act on.
   /study-up     Teach the kit your specific job/field.
   ...
```

<!-- screenshot: 03-claude-prompt.png -->
*(screenshot: the Claude Code prompt with the slash-command menu open)*

### Step 4 — Run `/onboard` (the important one)

Type it and press enter:

```text
> /onboard
```

It asks **where you are on the journey first** — because a pre-enlistment answer and a veteran
answer are completely different — then a handful of questions, one at a time. About 10 minutes.
Everything you tell it is written to files **on your machine and nowhere else.**

```text
Where are you on the journey right now?

  1. Thinking about enlisting, or in the process
  2. Currently serving
  3. Separation or retirement is in sight
  4. Already out

You: 1

Got it. Who are you out of uniform, and what do you want next?
```

When it's done, you'll see your setup confirmed and your first move pointed out:

```text
✓ You're set up. Battle Buddy knows your stage, your record, and what you're driving at.

Now run: /next-move   — I'll give you the one thing to do next, ready to act on.
Want me to learn your specific field (pipeline, standards, certs)? Run /study-up.
Any time your situation changes (ship, PCS, reclass, separate), re-run /onboard.
```

<!-- screenshot: 04-onboard-stage-menu.png -->
*(screenshot: the four-option stage menu)*

### Step 5 — Run `/next-move`

This is the one you'll come back to. It gives you **one** clear next action — not a to-do list —
tailored to exactly where you are, with the first step already drafted.

```text
> /next-move

Your next move: Write down the three questions you still can't answer about your
top job choice, and bring them to your recruiter this week.

Why it's the one: You're weighing a commitment, and the cheapest thing you can do
right now is get better information before you sign anything.

Here's the start: I drafted the three questions for you below — read them, cut or
add as you like...
```

<!-- screenshot: 05-next-move.png -->
*(screenshot: a /next-move reply)*

### What to expect going forward

- **Come back to `/next-move`.** It's the daily driver. Most days, that's the only command you need.
- **Set a rhythm you'll actually keep** — a battle rhythm. `/next-move` daily, a quick review weekly.
  Small and steady beats ambitious and abandoned.
- **Re-run `/onboard` whenever your situation changes** — you ship to basic, you PCS, you separate.
  That's a big deal, and it re-points the whole system around the new you.
- **Teach it your world with `/study-up`** — your job code, pipeline, certs, community. It researches
  official sources, confirms with you, and records it (cited) into your own copy.
- **The guardrails are always on:** if you're in crisis it stops and gets you the Veterans Crisis
  Line first; it never makes up a benefit number (it pulls the official page and cites it, or hands
  you the link); it routes claims to a **free** accredited VSO; and your files stay on your machine.

The full menu of commands is just below.

## What ships

The full set of commands. You met the first three in the walkthrough above; the rest are here when
you need them.

| Command | What it does |
|---|---|
| `/onboard` | Sets up (or re-points) the system. Asks your stage first. Re-run it any time your situation changes. |
| `/study-up` | Teaches the kit *your* world — job code, pipeline, certs, community. Researches official sources, confirms with you, records it cited. |
| `/next-move` | One OODA cycle → your single next action. The daily driver. |
| `/translate` | Military ↔ civilian, both directions. Record → résumé/LinkedIn/interview; or job posting → what they're really asking for. |
| `/benefits-check` | A stage-aware sweep of what you may be eligible for, every line cited to an official source. |
| `/aar` | An after-action review of your own setup — what's in place, what's missing, what to fix first. |

## License & credit

MIT © 2026 Zachary Thomas. Use it, fork it, build on it.

Inspired by the AIOS pattern popularized by Nate Herk.
