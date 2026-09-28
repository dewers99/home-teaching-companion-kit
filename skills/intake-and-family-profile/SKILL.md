# Intake and family profile skill

**Version:** 1.0.0

## When to use

Use this module at the start of a new relationship with a homeschooling parent, when the parent wants the companion to remember their family and teach to it. Also use it when the parent says their situation has changed (a new child starting school, a new work schedule, a move) and the stored profile needs updating. Never launch it unprompted — the user can skip it entirely and just start asking questions.

## Procedure

1. Offer the intake; never force it. Say something like: "I can run a quick get-to-know-you survey so I can tailor things to your family — takes a few minutes, one question at a time, and you can skip anything. Want to, or would you rather just dive in?" If they decline, help them as-is and learn from ordinary use instead (see step 8).
2. If they accept, run the intake as a conversational survey. Normally one question at a time so it stays light.
3. When several answers are genuinely needed before proceeding, use the conversational survey format: every question states its type — "choose one", "choose up to N", "choose all that apply", or "type your answer". Every non-text question includes an "Other" option. EVERY question allows "Skip", "I don't understand this question", and "Let's discuss this more". Never guess at ambiguity — ask.
4. Cover the topics in this order, keeping each to one question unless the survey format applies:
   a. **Family basics:** parent's name, who does the teaching, household rhythm and constraints (work schedules, nap times, appointments — the real shape of the days).
   b. **The faith question.** Ask it explicitly, in words close to these: "Do you want me to weave a Christian faith perspective into our work together — for example connecting lessons to faith — or keep things neutral?" This is "choose one"; "Other" and all the standard escape hatches apply. The default, before they answer, is neutral. Record the answer and honor it everywhere.
   c. **Each child separately:** name or nickname, age and grade level, learning-style observations ("seems to learn by doing", "loves being read to"), strengths, and needs or challenges. Keep this light — it is not a medical intake, and you are not diagnosing anything. If a concern sounds like it needs professional eyes, say so plainly and move on.
   d. **Teaching approach/philosophy** — describe the common approaches curriculum-neutrally, one plain sentence each, describe don't prescribe: Charlotte Mason (short lessons, living books, nature and narration); classical (grammar, logic, and rhetoric stages built on the trivium); unschooling (child-led learning from life and interests); eclectic (mixing methods per subject and per child); traditional/textbook (structured, grade-level curriculum); Montessori-inspired (hands-on, self-directed work with prepared materials); unit studies (multiple subjects woven around one theme). "Not sure yet" is a fine answer — say so.
   e. **Goals for the year** (a few sentences is plenty) **and the state, country, or territory they homeschool in.** Their answer routes compliance questions — the kit carries compliance guidance for nine states (Ohio, Michigan, Indiana, Texas, California, Florida, New York, Missouri, Illinois) via `skills/compliance-core/`; for states, countries, or territories not yet covered, say so honestly, suggest the homeschool association or department of education where they live, and offer the kit's state-request form (built from `state-request-form-spec.md`; if the form doesn't exist yet, skip it silently). If the place is covered, offer the compliance-check mode as a "choose one" question: "How should I keep your state's homeschool requirements verified against official sources — quarterly (each January, April, July, and October), or on demand whenever you ask?" (see `skills/compliance-update-checks/`; store the answer in the family profile). If it isn't covered, skip the compliance-check offer — say the quarterly checks will become available if their place gets added.
5. If the user types "Cancel" at any point, stop the survey and ask whether to keep the answers collected so far or drop them.
6. After the last question, READ BACK everything collected — the family basics, the faith answer, each child, the approach, the goals — and ask them to confirm or correct before you act on any of it.
7. Only after confirmation, write the profile: one filled `templates/family-profile.template.md` plus one filled `templates/child-profile.template.md` per child.
8. **Conversational alternative (no survey):** the user may skip the survey and just use the companion. In that case, learn from ordinary use: when you notice something worth remembering (a child's age, a work constraint, the faith answer), propose it as a profile note and ask approval before storing it. NEVER rewrite stored notes silently — always propose, get a yes, then update.

## Output

A confirmed, filled `templates/family-profile.template.md` and one confirmed, filled `templates/child-profile.template.md` per child. If the AI tool you are running on cannot save files, say so honestly and paste the filled profiles as plain markdown the user can copy and keep.

## Boundaries

- Does not diagnose learning disabilities, developmental conditions, or medical conditions. If a concern comes up, suggest consulting a qualified professional and keep the intake moving.
- Does not give legal advice. State homeschool law questions get routed honestly — the companion routes compliance questions through `skills/compliance-core/` and the nine state modules (Ohio, Michigan, Indiana, Texas, California, Florida, New York, Missouri, Illinois); for states, countries, or territories not yet covered, say so, suggest the user check the homeschool association or department of education where they live, and offer the kit's state-request form (built from `state-request-form-spec.md`; if the form doesn't exist yet, skip it silently).
- Never addresses, tutors, or interacts with a child as a student. If a child appears to be the one typing, gently redirect: ask for the parent, and wait. A student-facing kit is a separate future project — do not build student features here.
