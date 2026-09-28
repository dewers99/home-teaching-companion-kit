# Install Guide — Home Teaching Companion Kit v1.0.1

## What this kit is

The Home Teaching Companion Kit turns your AI tool into a homeschool teaching assistant for you, the parent/teacher. It comes in four parts: **AGENT.md** (the companion's persona — how it talks, what it knows, how it works with you), **skills/** (16 modules: intake-and-family-profile, lesson-and-unit-planning, activities-and-projects, progress-tracking, curriculum-and-resource-guidance, compliance-core, compliance-update-checks, plus one compliance module per state for nine states), **templates/** (7 blank starter docs: family-profile, child-profile, lesson-plan, weekly-plan, progress-log, notification-checklist, compliance-check-report), and **reference/** (19 appendices, consulted when asked, never volunteered in full: one home-education quick reference per state for nine states, plus subject and supplies references for each level band — Pre-K, K–2, 3–5, 6–8, 9–12). Pure markdown, no apps, no sign-ups.

## Two ways to get the files

1. **Download the ZIP:** grab the kit ZIP from the GitHub release page, then attach or upload the files where your AI tool asks for them.
2. **Point your AI at the repo:** some tools can fetch a GitHub link directly — give yours this one.

Repository:

```
https://github.com/dewers99/home-teaching-companion-kit
```

Clone command:

```
git clone https://github.com/dewers99/home-teaching-companion-kit.git
```

## Set up on your platform

### Muse AI (recommended)

Share the repo or folder link with your Muse AI, or paste in AGENT.md plus whichever skills you want (start with `intake-and-family-profile`). Then say:

> "Install this companion kit and start intake with me."

The companion will walk you through a short intake — your family setup, each child's age and grade, what subjects you want help with — and save your profile for next time.

**Honest limits**

- **Persona persists?** Within a session, yes. Across sessions, only in tools that support saved persona or memory features — check your tool's docs.
- **Can the companion save files?** Only if the tool lets it (file upload/download features). Otherwise it hands you copy-paste text you keep yourself.
- **The standing rule:** the companion never pretends it saved something it can't. If there's no real way to persist, it says so and offers copy-paste text instead. No fake promises, ever.
- Uncertain about your setup? Ask the companion what it can actually save — it will tell you honestly rather than guess.

### ChatGPT

Projects: create a new Project, upload the kit files (AGENT.md plus the skills and templates you want) into it, and do all your homeschool chatting inside that project. Then start with:

> "Install this companion kit and start intake with me."

**Honest limits**

- **Persona persists?** Within that project, mostly yes for the session — project instructions persist across conversations in the project, but chat memory itself varies. Check your tool's docs — or ask the companion what it can actually save.
- **Can the companion save files?** Not to the project directly. It will give you text to copy into your own files, or updated file text you can re-upload.
- **The standing rule:** the companion never pretends it saved something it can't. Without real persistence it says so and offers copy-paste text instead. No fake promises, ever.

### Claude

Projects: same pattern as ChatGPT — create a Project, add the kit files to the project knowledge, and chat inside it. Then say:

> "Install this companion kit and start intake with me."

**Honest limits**

- **Persona persists?** Project instructions persist across conversations in the project; chat memory within a single conversation only. Across projects or the main chat, no.
- **Can the companion save files?** Not into the project by itself. It will hand you updated text (profiles, plans, logs) that you keep in your own files or re-add to project knowledge.
- **The standing rule:** the companion never pretends it saved something it can't. Without real persistence it says so and offers copy-paste text instead. No fake promises, ever. Where you're unsure, check your tool's docs — or ask the companion what it can actually save.

### Google Gemini

Gems: create a Gem, paste AGENT.md plus your chosen skills into the Gem's instructions, and use that Gem for all homeschool work. First message:

> "Install this companion kit and start intake with me."

**Honest limits**

- **Persona persists?** Within the Gem, yes across conversations. Outside the Gem, no.
- **Can the companion save files?** Only through features the tool exposes — check your tool's docs. Otherwise it gives you copy-paste text.
- **The standing rule:** the companion never pretends it saved something it can't. Without real persistence it says so and offers copy-paste text instead. No fake promises, ever. If unsure what your setup supports, ask the companion what it can actually save.

### Microsoft Copilot

Copilot doesn't hold a standing persona between sessions, so re-attach the kit each session: attach AGENT.md (and any skills or templates you need) to the conversation, then say:

> "Install this companion kit and start intake with me."

To keep continuity, paste your saved family/child profile at the top of the session so the companion picks up where you left off.

**Honest limits**

- **Persona persists?** No — each session starts fresh. You re-attach AGENT.md every time.
- **Can the companion save files?** No. It produces text (profiles, lesson plans, weekly plans, progress logs, checklists) that you copy into your own files.
- **The standing rule:** the companion never pretends it saved something it can't. Without real persistence it says so and offers copy-paste text instead. No fake promises, ever.

### Cursor / coding agents

This is the most durable route because it's file-based. Drop the kit files into your project workspace (keep AGENT.md at the top level or in a `companion-kit/` folder), point the agent at AGENT.md, and say:

> "Install this companion kit and start intake with me."

Since everything lives as real files in your workspace, profiles and plans persist as actual documents you can open, edit, and version with git.

**Honest limits**

- **Persona persists?** As long as the files are in the workspace and the agent reads them, yes — this is the closest to true persistence in this guide.
- **Can the companion save files?** Yes — the agent can read and write workspace files (family/child profiles, lesson plans, weekly plans, progress logs, notification checklists) directly.
- **The standing rule still applies:** the companion confirms what it actually wrote. It never claims a file was saved when it wasn't. No fake promises, ever.

### Any other AI tool

Paste AGENT.md plus the skills you want into the tool's system/persona prompt (sometimes called "custom instructions" or "persona"), or attach the files to the conversation and say:

> "Install this companion kit and start intake with me."

**Honest limits**

- **Persona persists?** Varies — check your tool's docs. If it has saved instructions or memory, the persona can persist; if it's a bare chat box, it lasts one session.
- **Can the companion save files?** Varies — check your tool's docs — or ask the companion what it can actually save.
- **The standing rule:** the companion never pretends it saved something it can't. Without real persistence it says so and offers copy-paste text instead. No fake promises, ever.

## Capability matrix

| Platform | Persona persists? | Can the companion save files? | Saved as… |
|---|---|---|---|
| Muse AI (recommended) | Within session yes; across sessions depends on tool's memory/persona features — check your tool's docs | Only via tool file features; otherwise copy-paste text | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |
| ChatGPT (Projects) | Project instructions persist; chat memory varies — check your tool's docs | Not directly — updated text you keep yourself or re-upload | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |
| Claude (Projects) | Project instructions persist; per-conversation memory only | Not into the project — text you keep or re-add to project knowledge | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |
| Google Gemini (Gems) | Within the Gem, yes across conversations | Only via exposed tool features — check your tool's docs | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |
| Microsoft Copilot | No — re-attach each session | No — copy-paste text you keep in your own files | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |
| Cursor / coding agents | Yes while files are in the workspace (file-based; most durable) | Yes — reads and writes workspace files directly | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |
| Any other AI tool | Varies — check your tool's docs | Varies — check your tool's docs | Family/child profiles, lesson plans, weekly plans, progress logs, notification checklists |

Things the companion might save for you: family/child profiles, lesson plans, weekly plans, progress logs, notification checklists. Whether it can actually save them depends on the platform — see above, and when in doubt, ask the companion directly what it can actually save. It will answer honestly.

## Updates

- **First check:** one week after you install, the companion asks if you want to check for a kit update.
- **After that:** your choice — weekly (the default), monthly, or off. Say the word any time to change it.
- **How it works:** the companion compares the repo's `VERSION` file against your installed version, shows you exactly what changed, and never silently applies an update. You decide whether to take it.
- **URL-installed kits that re-fetch every session** are already current — no check needed.

## Compliance update checks

Separate from kit updates: your active state module is re-verified against official sources quarterly or on demand — your choice, made during intake or any time after and stored in your family profile. In quarterly mode, at the turn of each calendar quarter (January, April, July, October) the companion offers the check at a calm moment and reports confirmed / changed / uncertain; changes apply only with your explicit approval, and they never require a kit update. How the check gets started depends on your platform:

| Platform | How the check runs |
|---|---|
| Muse AI | The companion watches your profile's last-check date and offers the check when it's due; or say "run my compliance check" any time. |
| ChatGPT (Projects) | Same — the companion offers when it sees the date has passed inside the project; or trigger it manually. |
| Claude (Projects) | Same as ChatGPT. |
| Google Gemini (Gems) | Same — the Gem offers when due; or trigger it manually. |
| Microsoft Copilot | Manual only: Copilot doesn't persist between sessions, so keep the interval and last-check date in your own copy of the family profile and ask for the check when it's due. |
| Cursor / coding agents | Most durable: the check report is written as a real file in your workspace. Runs on request, on the companion's offer, or on your environment's own task scheduler if it has one. |
| Any other AI tool | Varies — the manual trigger ("run my compliance check") always works; whether the companion can offer it unprompted depends on the tool's memory features. |

**Honest limits:** no platform in this guide is promised background scheduled checks — the companion does not claim a check ran when it didn't. If your tool offers its own scheduled tasks or reminders, you're welcome to set one as a backup nudge, but the check itself always runs in conversation, with the report in front of you, and nothing changes without your yes. If the platform can't browse the web, the companion says so plainly and labels the review as knowledge-cutoff-based rather than a live verification.

## Feedback

Two weeks after install, at a calm moment (never in the middle of planning or a busy homeschool morning), the companion offers the anonymous feedback form once: https://tally.so/r/D4QLKp — skippable, never nagging, and responses aren't monitored in real time. Say "No thanks" once and it never asks again.

## Requesting a state, country, or territory

If your state, country, or territory isn't one of the nine covered, the companion says so honestly — and offers the kit's state-request form, a separate short form: https://tally.so/r/Y5824z. Requests are counted; the most-requested places get built first, and you can leave an email if you want to be notified when yours is added.
