# Lesson and unit planning skill

**Version:** 1.0.1

## When to use

Use this module when the parent wants a plan: a single day's lessons, a week's schedule, or a multi-week unit study around a theme. It also applies when an existing plan needs adjusting — a sick day, a field-trip week, or a subject that needs more time. Plans are built for the parent/teacher to run, not handed to the child.

## Procedure

1. Confirm the scope first: one day, one week, or a multi-week unit? Which subjects should it cover? Which child or children is it for? Plans are per-child by default; a shared family activity (a read-aloud, a nature walk) can span children — note which parts are shared and which are per-child.
2. Ask about constraints: time available, materials on hand, appointments or interruptions to plan around. Household-realistic beats ambitious — a plan that survives Tuesday is better than a plan that looks good on Sunday night.
3. Check the family/child profile if one exists and use it (ages, learning styles, approach, rhythm). If no profile exists, ask only the minimum needed for this plan — age/grade, subjects, time available. Never force the full intake to get a lesson plan.
4. Build the plan:
   - Keep it household-realistic: short focused sprints for little ones, margin for interruptions, rest and play treated as real parts of the day, not filler.
   - Mix the modes as age-appropriate: focused work, hands-on activities, read-aloud, independent work.
   - For children ages 3–5, plan by developmental domain, not school subject — consult `reference/prek-domains.md` for the domain structure, typical objectives, and the weekly rhythm.
   - For Kindergarten through 2nd grade, plan by subject — consult `reference/k-2-subjects.md` for per-grade objectives and weekly time guidance.
   - For 3rd through 5th grade, plan by subject — consult `reference/3-5-subjects.md` for per-grade objectives and weekly time guidance.
   - For 6th through 8th grade, plan by subject — consult `reference/6-8-subjects.md` for per-grade objectives and weekly time guidance.
   - For 9th through 12th grade, plan backward from the student's goals — consult `reference/9-12-subjects.md` for the credit framework, per-subject sequences, and transcript/diploma guidance.
   - Reference the family's own materials and teaching approach — you are not a curriculum publisher. Name the specific book, workbook, or resource the family uses rather than inventing one.
   - For a unit: give a plain outline — theme, week-by-week arc, key activities per week, and what the child practices — not a script.
5. Present the plan, then offer to adjust: swap activities, shrink or expand a day, shift things between days. Iterate until the parent says it fits.
6. If the user asks about alignment to a state standard, only claim alignment if you can honestly check it against the actual standard. Otherwise say plainly that the plan follows their materials and approach, not a certified scope and sequence.

## Output

A filled `templates/lesson-plan.template.md` for a daily plan, a filled `templates/weekly-plan.template.md` for a weekly plan, or a plain unit outline in chat for a multi-week unit study. If the AI tool you are running on cannot save files, say so honestly and paste the plan as plain markdown the user can copy and keep.

## Boundaries

- Not a curriculum publisher: plans reference the family's own materials and approach; never invent or require a specific commercial curriculum.
- Does not promise alignment to any state standard unless the user asks and it can honestly be checked.
- Keeps plans adaptable, never rigid — a plan is a starting point the parent can rearrange, not a contract.
- Never addresses the child directly; everything here is written for the parent/teacher to use.
