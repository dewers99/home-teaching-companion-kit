# Compliance core skill

**Version:** 1.0.0

## When to use

Use this module when where the family homeschools isn't set yet, when they ask how homeschool law compares across states, or when they want the big picture before diving into their own state's module. This module is the state-neutral hub: it teaches the patterns that hold across all nine researched states, shows how the states differ, and routes to the right by-state module. Once the family's state is known, load that state's `skills/<state>-compliance/` module for the exact facts — this core never answers a state-specific question from memory.

## Design note (deliberate)

This core intentionally carries cross-state comparison tables — notification tiers, testing and evaluation, record-keeping mandates, the compulsory-age table, and the state watch-outs index — even though the rest of the core is state-ambiguous. The comparison layer is this core's job: no single state module can show how states differ, and families comparing states or moving between them need the at-a-glance picture. The trade-off is duplication, since the same facts also live in the state modules. Maintenance rule: whenever a state module's facts change, check this core's tables and update them in the same pass. The quarterly re-verification covers both.

## Procedure

1. Determine where the family homeschools. If it's one of the nine researched states (Ohio, Michigan, Indiana, Texas, California, Florida, New York, Missouri, Illinois), name the module and load it: `skills/<state>-compliance/`. If it's any other state, country, or territory, say so honestly: the kit covers nine states; for the rest, the core's universal truths and "records anyway" guidance still apply, but the parent must verify the homeschool law where they live. Offer the kit's state-request form so the parent can ask for their state, country, or territory to be added (built from `state-request-form-spec.md`; if the form doesn't exist yet, skip it silently).
2. Before answering any state-specific question, consult that state's module and its quick reference. The modules hold the verified facts (researched 2026-09-27); this core holds the patterns.
3. Share the pattern-level picture below as needed — notification tiers, testing, records, ages — and close with the honest-limits line.

## The state-neutral picture

### What states require before you start (notification tiers)

- **No notice to anyone:** Michigan (under the home-school exemption), Indiana, Texas, Illinois, Missouri. You simply begin. (Leaving a public school is different — see each state's module: written withdrawal letters are wise everywhere, and Indiana requires a signed withdrawal form for high-schoolers.)
- **One-time notice:** Florida. File a signed notice of intent with the district superintendent within 30 days of starting — once, not annually.
- **Notice plus annual renewal:** Ohio. Notify the district superintendent within 5 calendar days of starting, moving districts, or withdrawing — and again annually by August 30.
- **Annual filing plus ongoing paperwork:** California (a Private School Affidavit filed with the state each year) and New York (annual notice of intent, an Individualized Home Instruction Plan, four quarterly reports, and an annual assessment). New York is the most paperwork-intensive state in the kit.

### Testing and evaluation

- **No testing required:** Ohio, Michigan, Indiana, Texas, California, Illinois, Missouri. (Missouri substitutes an hours-and-records system instead; Indiana wants attendance records.)
- **Annual evaluation, parent's choice of method:** Florida — five statutory options, from a certified teacher reviewing the portfolio to a normed test to a psychologist's evaluation.
- **Annual assessment, grade-banded rules:** New York — a normed test is the default; a written narrative from an evaluator works every year in grades 1–3, every other year in grades 4–8, and not at all in grades 9–12 (test only there).

### Record-keeping mandates

- **None mandated:** Ohio, Michigan, Texas, Illinois.
- **Attendance records:** Indiana (daily record, 180 days of instruction, produced on request) and New York (attendance required; quarterly reports on top).
- **Portfolio-style records:** Florida (activity log plus work samples, kept 2 years, shown on 15 days' written notice) and Missouri (plan book, work samples, evaluations — kept by the parent, filed with no one, reviewable only by the local prosecuting attorney).
- **School-style records:** California (attendance register, courses of study, faculty names/addresses/qualifications).

### Compulsory-attendance ages

| State | Ages |
|---|---|
| Ohio | 6–18 |
| Michigan | 6–18 |
| Indiana | 7–18 |
| Texas | 6 (by Sept 1) to 19th birthday |
| California | 6–18 |
| Florida | 6–16 |
| New York | 6–16 (17 in New York City) |
| Missouri | 7–17 (or 16 credits) |
| Illinois | 6 (by Sept 1)–17 |

## Universal truths (all nine states)

These hold in every researched state — they're the safest things the companion can say without looking anything up:

1. **No parent or teacher qualifications are required to homeschool.** No state in the kit asks the parent to hold a degree, certificate, or credential to teach their own child under the home-school path. (Michigan also offers a *nonpublic-school* exemption path, which technically requires a teaching certificate with a religious-objection exemption — the Michigan module explains it. The home-school path needs nothing.)
2. **The parent determines graduation and issues the diploma.** No state issues a homeschool diploma; no state sets graduation requirements for homeschoolers. Colleges, employers, and the military set their own admissions expectations — keep the transcript and course descriptions (see `reference/9-12-subjects.md`).
3. **Re-enrollment and credit transfer are always the receiving school's decision.** Every state leaves grade placement and credit acceptance to the school the child re-enters. Good records are what make that conversation go well.
4. **Laws change; re-verify before acting.** Every module's facts were verified 2026-09-27 against official sources — with one flagged exception: an Indiana section cross-checked from secondary sources when the legislature's site was unfetchable (the Indiana module says so) — and each module lists its official links. Bills get filed, sections get renumbered (Missouri restructured its entire framework in 2024–2025), and guides go stale. When it matters, check the official source.
5. **This is public legal information, never legal advice.** Edge cases, disputes with a district, special-education questions, or anything adversarial go to the school district or an attorney.

## The "records anyway" principle

Even where the law mandates nothing, keep three things for every child:

- **An attendance log** — days or hours of instruction.
- **A portfolio** — samples of work across subjects through the year.
- **Copies of everything filed or received** — notices, evaluations, acknowledgment letters, district correspondence.

These are what re-enrollment, college applications, scholarship programs (Florida's Bright Futures paperwork runs through the district home-education office), and any dispute all ask for. The progress-tracking module's logs cover the first two; keep the third in a folder, physical or digital.

## State watch-outs index

Each state's module carries the full picture; these are the one-line flags worth knowing:

- **Ohio** (`skills/ohio-compliance/`) — post-October-2023 law; most online guides still describe the old 900-hour/assessment rules.
- **Michigan** (`skills/michigan-compliance/`) — two legal routes: the no-notice home-school exemption vs. the nonpublic-school route; don't mix them up.
- **Indiana** (`skills/indiana-compliance/`) — daily attendance records are the one mandate; high-schoolers leaving public school need a signed state withdrawal form or the BMV treats them as dropouts.
- **Texas** (`skills/texas-compliance/`) — the *Leeper* subjects are reading, spelling, grammar, math, and good citizenship (not writing); TEA regulates nothing.
- **California** (`skills/california-compliance/`) — file the annual Private School Affidavit with the state; the district gets nothing.
- **Florida** (`skills/florida-compliance/`) — three separate legal paths (home education, umbrella private school, PEP scholarship) that guides constantly conflate; keep them fenced.
- **New York** (`skills/new-york-compliance/`) — the district reviews for compliance but never *approves*; and start the superintendent's "substantial equivalence" letter early if SUNY/CUNY is on the horizon.
- **Missouri** (`skills/missouri-compliance/`) — the 2024–2025 rewrite moved everything to RSMo 167.012 and repealed the old declaration process; nearly all guides are stale.
- **Illinois** (`skills/illinois-compliance/`) — the lightest touch of all nine; HB 2827 ("the Homeschool Act") is *not* law but could revive in 2026 — watch this space.

## Keeping modules current

Laws change on their own schedule, so each state module is checked on its own clock — independent of kit updates. The full system lives in `skills/compliance-update-checks/`: the parent picks quarterly or on-demand checking, stored in the family profile, and each check re-verifies the active state's facts against its official sources, reports confirmed / changed / uncertain, and applies changes only on explicit approval. Each state module carries its own **Version:** (bumped only on content change — patch for corrections, minor for substantive law/deadline/procedure changes) and **Last verified:** date (updated every check). The core kit `VERSION` never changes for a state-module update.

## Output

A routing answer: which module applies, the pattern-level context the parent needs, and pointers to the official sources. State-specific answers always come from the state module, never from this core.

## Boundaries

- Never legal advice. Same honest limits as every state module: public legal facts plus official sources; edge cases go to the district or an attorney.
- Never answers a state-specific question from this core's summary tables alone — loads the state module first.
- Never presents a bill that hasn't passed (Illinois HB 2827, Michigan's failed 2023–24 registration bills, Indiana's dead SB 483, California's dead AB 2756) as current law.
- Defers record-keeping and progress questions to the progress-tracking module; defers curriculum questions to the curriculum-and-resource-guidance module.
