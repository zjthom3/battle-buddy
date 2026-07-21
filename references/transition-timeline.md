# The transition timeline — the countdown that matters

> **Verified:** 2026-07-21 · **Contains no volatile figures.** The exact windows, day-counts, and
> deadlines change and vary by situation — this file names the milestones and their official
> sources; `/next-move` pulls the current windows live and counts them against your real
> separation date.

Transition is the highest-stakes stretch, because several benefit windows are **time-boxed** and
some doors close for good once you're out. The move is to work backward from your separation date
and hit each milestone early, not on the last day.

> **Guard / Reserve?** This timeline assumes an active-duty separation. If the person is demobilizing
> or leaving a Guard/Reserve component, the milestones, documents (NGB-22 vs DD-214), and benefit
> windows can differ — read `references/guard-reserve.md` first and verify each window live.

## The milestones (roughly in order, working toward your date)

- **TAP — Transition Assistance Program.** Congressionally required; start it as early as your
  command allows, not at the last minute. Covers the mandatory pieces plus tracks (employment,
  education, entrepreneurship). Official: https://www.dol.gov/agencies/vets/programs/tap
- **SkillBridge.** Lets you spend your final stretch doing a civilian internship/training with an
  employer while still on active-duty pay. Command approval required; apply *well* ahead.
  Official: https://skillbridge.osd.mil
- **VA disability claim — the pre-discharge options.** You can start a claim *before* you separate
  (pre-discharge programs) so it's not starting from zero after you're out. There are specific
  filing windows tied to your separation — verify the current windows on VA.gov and file inside
  them. Claims help = a **free** accredited VSO (`veteran-orgs.md`), never a paid service.
  Official: https://www.va.gov/disability/how-to-file-claim/
- **VA health care enrollment.** There's an enrollment pathway for recently separated combat
  veterans with its own window, plus general enrollment. Get in the system. Official:
  https://www.va.gov/health-care/how-to-apply/
- **Terminal leave.** Using accrued leave at the end can effectively overlap military pay with
  starting a civilian job or SkillBridge. Plan it deliberately.
- **The DD-214.** Your discharge document and the key that unlocks most benefits. Check it for
  accuracy before you sign out — errors are painful to fix later. Store copies safely.
- **Final out.** Stage becomes `veteran` — re-run `/onboard`.

## How `/next-move` uses this

Given your separation date in `situation/stage.md`, `/next-move` in the `transitioning` stage
builds a backward countdown: which of these windows is open now, which closes soonest, and the
single next action to not miss one. Every date it cites is verified live against the official
page — it will not guess a deadline.

## Official hubs

- **VA transition hub:** https://www.va.gov/careers-employment/
- **DoD TAP:** https://www.dol.gov/agencies/vets/programs/tap
- **VA benefits by discharge:** https://www.va.gov
