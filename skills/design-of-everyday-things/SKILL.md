---
name: design-of-everyday-things
description: Apply Don Norman's The Design of Everyday Things (revised & expanded edition) to real design work — reviewing or auditing a UI, screen, form, device, control panel or physical product; diagnosing why people "can't figure out" something or keep making the same error; designing controls, feedback, conceptual models, constraints and forcing functions; classifying human error (slips vs mistakes, modes, capture, memory lapses) and designing for error (undo, sensibility checks, checklists, Swiss cheese layers, resilience); running human-centered design (observation, ideation, prototyping, 5-user testing, iteration, double diamond, activity-centered design); and making product decisions under business pressure (featuritis, standards, incremental vs radical innovation, timing, Norman's Law). Use it whenever a request mentions affordances, signifiers, mapping, feedback, discoverability, mental/conceptual models, usability, "users don't understand", "people press the wrong button", "is this error the user's fault", accident or root-cause analysis, Five Whys, poka-yoke, HCD, design thinking, UX review, or "how would Norman look at this" — even if the book is not named.
---

# The Design of Everyday Things — operational skill

This skill gives you Norman's way of seeing: every artifact (a door, a form field, a dashboard, a procedure, an API error message) is a communication from designer to user carried entirely by the **system image**, and people act through a predictable cycle of **seven stages** across two **gulfs** (execution: "what can I do and how?"; evaluation: "what happened and did it work?"). Good design bridges the gulfs with **feedforward** (affordances, signifiers, mappings, constraints, a conceptual model) and **feedback**, puts the required knowledge **in the world** rather than in the head, assumes people **will** be interrupted and **will** err, and treats every "human error" as a design signal to be fixed at the system level. The process that gets there is **human-centered design**: find the right problem before the right solution, observe real people doing real activities, prototype cheaply, test with five, iterate — while accepting the real-world constraints of schedules, budgets, purchasers who are not users, competitors, standards and legacy.

## Workflow

1. **Frame the goal, not the feature.** Ask "why?" at least twice to find the real goal and the activity it belongs to (ch. 2, 6). Decide whether you are solving the problem as given or the underlying one (double diamond, ch. 6).
2. **Audit or diagnose** with the seven stages and seven questions (ch. 2) — see `references/diagnose-interaction.md`. Locate the breakdown (which stage, which gulf), name the missing principle precisely (signifier vs affordance, mapping, feedback timing, hidden mode, false model), check memory/attention load, and classify any error (slip vs mistake vs violation, ch. 5).
3. **Design the fix from the strongest rung down**: make the wrong action impossible (constraints) → force the right sequence (interlock/lock-in/lockout) → make it obvious before acting (signifiers, natural mapping, visible state) → make it correctable after (immediate informative feedback, undo, sensibility checks) → standardize → only then document. Never "tell the user to be careful."
4. **Project a coherent conceptual model** through every channel of the system image (form, controls, displays, sounds, docs, marketing) so people can predict effects and recover when things go wrong (ch. 1, 2).
5. **Design for error** with `references/design-for-error.md`: assume interruption, shrink and diversify the holes in the Swiss cheese, reward reporting, build checklists and resilience (ch. 5).
6. **Run HCD**: observe in context, ideate widely, prototype roughly (even Wizard of Oz), test with five representative people, fix, test five more; iterate inside management gates; keep researchers in the field permanently so Norman's Law does not kill the research (ch. 6).
7. **Decide under business reality**: who buys vs who uses, what featuritis would cost, whether to follow or change a convention, incremental hill-climbing vs radical bets, and timing (ch. 6, 7). See `references/playbook.md` §15–17.
8. **Verify** by re-walking the seven stages with real people; check that the fix added no mode, no identical-looking control, no disappearing message, no secondary hazard.

Key questions to keep asking: What does this look like to someone who has never seen it? What tells them what to do and where? What tells them what happened? What story will they build about how it works, and is it true? What happens after an interruption, a wrong press, a timeout? If many people get it wrong, what in the design induces it?

## Core rules

1. Two hallmarks of good design: **discoverability** (what can I do, where, how) and **understanding** (what does it mean). A simple thing that needs a sign or a manual is a design failure (ch. 1).
2. **Affordances** are relationships (what is possible); **signifiers** are perceivable signals (where and how). Designers mostly work with signifiers; "I added an affordance" almost always means "I added a signifier" (ch. 1).
3. Anti-affordances and affordances must be perceivable to work; if they cannot be seen, signal them (glass doors) (ch. 1).
4. **Natural mapping**, best to worst: control on the item; control adjacent; controls in the same spatial layout as the items. Never map two dimensions onto one row (ch. 3).
5. **Feedback** must be immediate (acknowledge within 0.1 s; a tenth-second delay is already disconcerting), informative (what happened, what next), prioritized, and not excessive; poor feedback can be worse than none, and too much gets disabled (ch. 1).
6. For long operations show progress; underpredict durations (show the range or the slowest value) so expectations are exceeded (ch. 2).
7. A **conceptual model** need not be accurate, only useful: it must let people predict effects and act when things go wrong. The system image carries the entire burden of communicating it (ch. 1).
8. The hard part of design is when things go wrong; design the failure paths first-class (ch. 1, 2, 5).
9. The seven questions must be answerable at any moment: what do I want; what are the alternatives; what can I do now; how; what happened; what does it mean; is this okay (ch. 2).
10. Design for all three levels: visceral (appearance, immediate feel), behavioral (expectations confirmed by feedback; feeling of control), reflective (the story remembered and retold; "attractive things work better," but end-of-use frustration erases it) (ch. 2).
11. People blame themselves and hide their errors; treat every difficulty as a signifier of where the design can improve; never blame users (ch. 2).
12. Replace error messages with help and guidance that lets people fix the problem in place and continue; never make them start over; treat what they did as partially correct (ch. 2).
13. Accept any intelligible input format (dates, times, phone numbers, names, amounts) and normalize it; arbitrary precision requirements are programmer laziness, not machine needs (ch. 2).
14. Put knowledge in the world; make remembering unnecessary. Assume working memory holds **three to five** items and is wiped by any distraction; never show critical information in something that disappears (ch. 3).
15. Use different modalities for different information streams (sight, sound, touch, spatial location); auditory and haptic channels do not interfere much with a visual task (ch. 3).
16. Reminders need both a **signal** and a **message**, delivered at the right time or place; put the reminder on the thing itself (ch. 3).
17. Rote-learned arbitrary sequences give no help when things go wrong; provide meaningful structure, or better, visible options (ch. 3).
18. The more complex the password/security rules, the less secure the system; design for human memory and real workflows or people will write it down and prop the door open (ch. 3).
19. **Constraints** (physical, cultural, semantic, logical) let people act correctly in novel situations without instructions; make physical constraints perceivable before the action is tried (ch. 4).
20. **Forcing functions** — interlocks, lock-ins, lockouts — are the strongest defense against memory lapses and dangerous actions; minimize their nuisance or they will be bypassed, and offer the desired action directly in any blocking prompt (ch. 4).
21. **If all else fails, standardize**; encode the user's psychological model of the action, not the mechanics. Change a convention only when the new way is vastly superior; then change everything at once and expect complaints and a confusion period regardless of merit (ch. 4, 6).
22. Use natural, informative sound for what cannot be seen; generic beeps inform little and annoy; silence where sound is expected is a feedback failure (ch. 4).
23. **Error = slip or mistake.** Slips (right goal, wrong execution: capture, description-similarity, mode, memory-lapse) afflict experts; mistakes (wrong goal/plan: rule-based, knowledge-based, memory-lapse) afflict novices and novel situations. Each class has its own fix (ch. 5).
24. Make controls for different purposes look and feel different; keep confusable ones apart; make procedures diverge from their first step; avoid modes, or make the mode continuously visible — "mode error is really design error" (ch. 5).
25. Interruptions are the main cause of memory lapses; design for resumption (goal, place in sequence, system state still visible) and protect critical phases (sterile periods) (ch. 5).
26. Keep asking why past the first human error (Five Whys); if the system lets you make the error it is badly designed, if it induces the error it is really badly designed; if many people make it, look for another cause (ch. 5).
27. Accidents have multiple causes (Swiss cheese): add defensive layers, shrink holes, diversify mechanisms so holes do not align, and alert when several line up. No single act by one person should cause widespread damage (ch. 5).
28. Provide undo (multi-level where possible), recoverable deletion, sensibility checks against normal ranges, and confirmations that show the object being acted upon; expect confirmations to catch slips but not mistakes (ch. 5).
29. Collaborative checklists (one reads, one does, the reader confirms) reduce slips and lapses; do not force sequence unless the task requires it; track skipped items (ch. 5).
30. Reward error reporting; never punish it; data you do not have cannot improve the design (Jidoka, NASA reporting) (ch. 5).
31. Automation handles the dull tasks and gives up on the complex ones, silently, with the human out of the loop; make automation state and failures loud; design human + machine as a collaborative team (ch. 5).
32. Solve the right problem: treat the stated problem as a suggestion; diverge, converge on the problem; diverge, converge on the solution (double diamond) (ch. 6).
33. Requirements made in the abstract or by asking people are invariably wrong; they come from watching people in their natural environment; most cases are "special," so allow for special cases (ch. 6).
34. Test with **five** representative people, individually or in pairs thinking aloud, then fix and test five more; iterate rather than running one big study (ch. 6).
35. Design for activities, not just tasks or demographics; people accept complexity that feels essential to the activity and reject arbitrary requirements (ch. 6).
36. Complexity is good, confusion is bad; the cure for confusion is a good conceptual model, not fewer functions (ch. 6).
37. There is no average person: a 95th-percentile design excludes 5% (15 million in the US); prefer adjustability; design aids to be good for everyone and market them without stigma (ch. 6).
38. Norman's Law: the day a product development process starts it is behind schedule and above budget; keep design and market researchers in the field continuously and run one multidisciplinary team from launch decision to returns (ch. 6, 7).
39. Purchasers are often not users (landlords, purchasing departments, distributors); study and influence them, and make usability a purchasing requirement (ch. 6, 7).
40. Featuritis has no vaccine: before adding a feature, ask who demands it and what discoverability it costs; strengthen strengths rather than matching competitors feature for feature; budget removal (ch. 7).
41. Incremental innovation (HCD hill climbing) makes things better but cannot find a higher hill; radical innovation changes industries, mostly fails, and takes decades (~20 years lab-to-product, 10–20 more to adoption); timing and legacy beat "better" (ch. 7).

## When to read which reference

| Task | Read |
|---|---|
| Look up a concept, definition, distinction (affordance vs signifier, slip vs mistake, three levels, constraint types) | `references/principles.md` (§1–7), `references/glossary.md` |
| Diagnose a confusing control, screen, flow, or a recurring user error | `references/diagnose-interaction.md`; then `principles.md` §2–3 |
| Audit/review a product or UI end to end | `references/playbook.md` §1, then §2–5 for the fixes |
| Design controls, layouts, mappings, modes | `playbook.md` §2; `principles.md` §2 (mapping, constraints); `examples.md` §1 |
| Design feedback, progress, alarms, sound | `playbook.md` §3, §8; `principles.md` §2 (feedback) |
| Explain how something works / write help, onboarding, labels, docs | `playbook.md` §4; `principles.md` §1 (system image), §2 (conceptual model); `examples.md` §2 |
| Forms, codes, passwords, reminders, memory load | `playbook.md` §5; `principles.md` §4 |
| Prevent dangerous or costly actions; error-proof a flow; undo/confirmations | `references/design-for-error.md`; `playbook.md` §6; `principles.md` §5 |
| Analyze an incident, accident, or "human error" report; root cause; blame questions | `playbook.md` §11; `principles.md` §5; `examples.md` §7 |
| Build or critique a checklist, reporting system, safety culture | `playbook.md` §12; `principles.md` §5 |
| Plan or run user research, prototyping, usability tests, iteration | `playbook.md` §9–10; `principles.md` §6 |
| Decide whether to follow or break a convention; standards; migrations/redesigns | `playbook.md` §7; `principles.md` §2 (conventions), §6 (standardization); `examples.md` §6 |
| Security vs usability; deliberately difficult designs; child-proofing; games | `playbook.md` §13; `principles.md` §6 |
| Accessibility, aging, special populations | `playbook.md` §14; `principles.md` §6 |
| Feature requests, roadmap, competitive pressure, innovation strategy, timing | `playbook.md` §15–16; `principles.md` §7; `examples.md` §8 |
| Team structure, process, schedule/budget reality | `playbook.md` §17; `principles.md` §6 |
| Need a concrete case to illustrate a point | `references/examples.md` (by theme) |
| Which chapter covers what | `references/chapter-map.md` |

## Anti-patterns Norman calls out

- Calling a label, arrow or highlight an "affordance"; adding words where form should signify (ch. 1).
- Beauty that erases the clues: hingeless glass doors, invisible cabinet latches, single-lever faucets whose controls melt into the body (ch. 1, 4).
- Rows of identical switches, controls or meters; two-dimensional things controlled by a one-dimensional row (ch. 3, 4, 5).
- One cheap light or beep with coded patterns as "feedback"; alarms that all sound at once; a dishwasher that beeps at 3 a.m. (ch. 1, 5).
- Controls that imply a false model (two refrigerator knobs for one thermostat); thermostats that offer no evidence of how they work (ch. 1, 2).
- "If only people would read the manual"; "you'll get used to it"; designing for people as the engineer wishes they were (ch. 1, 4).
- Blaming "human error" and stopping the analysis there; "blame and punish, blame and train"; replacing the person instead of the design (ch. 2, 5).
- Error messages that stop people, make them start over, or demand an arbitrary input format revealed only after failure (ch. 2).
- Critical information in messages that vanish; auto-logout that discards work after an interruption; designs that assume undivided attention (ch. 3, 5).
- Modes that are not visible; the same control meaning different things hours apart; similar inputs with different units (ch. 5).
- Confirmations that ask "are you sure?" without showing the object; no undo where undo is clearly possible (ch. 5).
- Printed checklists that force an unnecessary sequence; one person doing and another checking later; adding checkers until nobody checks (ch. 5).
- Rules written for legal compliance that cannot be followed and get rewarded when violated (ch. 5).
- Assigning to machines whatever can be automated and leaving the rest to people, then expecting people to monitor for hours with machine precision (ch. 5).
- Solving the problem as handed over; writing requirements in the abstract or from what people say; one big usability study instead of iterated small ones (ch. 6).
- Big-data correlations mistaken for understanding of needs; design research dismissed because its samples are small (ch. 6).
- Disciplines working serially and rewriting each other's output; "next time we'll do the research" (ch. 6).
- Matching the competitor's feature list; model-year churn and planned obsolescence; "objects of desire, not objects of use" (ch. 7).
- Standardizing too early (locking in primitive technology) or too late (no agreement possible); breaking a convention for a marginal gain; mixed systems during a change (ch. 4, 6).
- Assuming a good idea succeeds on merit and quickly; ignoring the legacy problem and timing (ch. 7).
