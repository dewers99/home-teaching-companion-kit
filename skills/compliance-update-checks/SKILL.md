# Compliance update checks skill

**Version:** 1.0.1

## When to use

Use this module when the parent wants to set up, run, or change the recurring check that keeps their **active state compliance module** current. This is separate from the kit's own update check (the `VERSION`-file comparison in AGENT.md): the kit check tracks the companion itself; this check tracks the *law* — statutes, deadlines, procedures, and agency guidance in the family's state. Laws change on their own schedule, so each state module carries its own version and verification date, independent of the kit version.

## Setup — quarterly or on demand

Offer the choice during intake (after the state is known) or any time later — "Say the word any time to change it" applies here too. Two options, nothing fancier:

- **Quarterly (the default).** The companion re-verifies the active state's module against official sources once per calendar quarter — January, April, July, October — and reports confirmed / changed / uncertain. Law moves on legislative calendars, not weekly news cycles, so quarterly catches real changes without crying wolf. The first check is due at the first quarter boundary after setup (a family installing in February gets their first check in April).
- **On demand.** The parent triggers the check whenever they want — say "run my compliance check" — and the companion doesn't watch the calendar. Good for families who track legislation themselves and only want verification when something's in the news.

Store two lines in the family profile (`templates/family-profile.template.md`): **Compliance check mode** (quarterly / on demand) and **Last compliance check** (date and quarter covered).

## How the check runs — per platform, honestly

The check itself is the same everywhere; what differs is *who starts it*, and that depends entirely on what the family's AI tool can do. Base this on INSTALL.md's honest limits — never promise scheduling a platform can't deliver:

- **Muse AI, ChatGPT (Projects), Claude (Projects), Google Gemini (Gems):** in quarterly mode the companion checks the family profile at the turn of each quarter (January, April, July, October) and, if no check is recorded for the new quarter, offers it at a calm moment — never mid-lesson or mid-crisis. In on-demand mode it never watches the calendar. Either way the parent can trigger the check any time by saying "run my compliance check." None of these platforms is documented in INSTALL.md as guaranteeing background scheduled tasks, so don't promise one: if the tool happens to offer scheduled tasks, the parent is welcome to set a reminder there, but the check does not depend on it.
- **Cursor / coding agents:** the file-based route — the most durable. The check report is written as a real file in the workspace, and the updated module files are real edits. If the agent environment has its own task scheduler, a recurring check can be configured there; otherwise it runs on request or on the companion's offer, same as above.
- **Microsoft Copilot:** no persistence between sessions, so the companion can't watch the clock. The parent keeps the check mode and last-check date in their own copy of the family profile, pastes it in at the start of a session, and asks for the check when it's due (quarterly mode) or whenever they want it (on demand).
- **Any other AI tool:** varies — check the tool's docs. The fallback everywhere is the manual trigger plus the companion's offer when it can see the date has passed.

If the platform can't browse the web, say so plainly at the start of the check (see step 2 below) — never fake a verification.

## The check procedure

Run these steps in order, every time:

1. **Load the inputs.** The family's active state module (`skills/<state>-compliance/`), its quick reference (`reference/<state>-compliance-quick-reference.md`), every official source link the module lists, and the module's honest-limits re-check list — those flagged items get checked first.
2. **Re-verify each checkable fact against the official sources.** Where the platform allows browsing, browse the statute pages, department-of-education pages, and bill-status pages directly. Where browsing is unavailable, say so explicitly and do a knowledge-cutoff-based review instead — clearly labeled as such, and every finding from it lands in *Uncertain*, never *Confirmed*.
3. **Write the findings** into `templates/compliance-check-report.template.md`: state, check date, check mode, sources consulted, then three sections — **Confirmed** (still accurate as written), **Changed** (the law, deadline, procedure, or guidance moved — with old vs. new), **Uncertain** (couldn't verify, bill filed but not passed, source unreachable). Include the proposed module diff and the explicit approval prompt.
4. **Check-don't-apply.** Present the report conversationally — confirmed first, then changed, then uncertain — and apply changes **only** on the parent's explicit approval. A declined change stays declined; an uncertain item stays flagged, never silently resolved.
5. **On approval, update the module.** Edit the state skill and its quick reference, bump the module version per the rules below, and set **Last verified:** to the check date. The core kit `VERSION` file is never touched by a state-module update.

## Per-module independent versioning

Each state skill and quick reference carries two lines under its title:

- **Version:** — the *module* version. Starts at 1.0.1 for all nine states.
- **Last verified:** — the date of the most recent check.

Rules:

- **Every check updates the date**, even when nothing changed. A fresh date with an unchanged version means "looked, still good."
- **Patch (1.0.1 → 1.0.1):** corrections, clarifications, rewording, official-link updates. The law didn't move; the module just says it better.
- **Minor (1.1.0):** substantive changes — a statute amended or a bill signed into law, a deadline or filing procedure changed, agency guidance changed, or a court decision affecting the framework.
- **The core kit VERSION never changes for a state-module update.** The kit's own update check and the compliance check are two independent systems; a family can be on kit v1.0.1 with a state module at v1.2.0 and that's exactly how it's supposed to work.
- **Modules update only as needed.** A module version bumps when a compliance change requires it (rules above) or when a kit change requires a module edit — e.g., a renamed shared template the module references, or a changed core procedure the module follows. If a kit release touches no module content, no module version changes. Never bump modules in lockstep with kit releases.

## What counts as a change worth applying

- A statute was amended or a bill was **signed into law**.
- A deadline, filing procedure, form, or fee changed.
- Agency guidance (department of education, attorney general opinion) changed.
- A court decision affecting the homeschool framework.
- An official source link moved or died (patch-level).

What does **not** count: a bill merely *filed* (that's watch-list material for *Uncertain*), a blog or guide claiming something new, an expired or failed proposal, or another state's law.

## Output

The filled `templates/compliance-check-report.template.md` (as a file where the platform allows, otherwise as copy-paste text), presented in conversation with the approval question. On approval, the updated module files with new version and date.

## Boundaries

- Never legal advice. Same honest limits as every compliance module: public legal facts plus official sources; edge cases go to the district or an attorney.
- Never applies a change without explicit approval — check-don't-apply is the whole point.
- Never presents a knowledge-cutoff review as a live verification.
- Never presents an unverified or uncertain item as confirmed.
- Never bumps the core kit `VERSION` for a state-module change.
- Never treats another state's law, a filed-but-unpassed bill, or a third-party guide as a change to the family's state module.
