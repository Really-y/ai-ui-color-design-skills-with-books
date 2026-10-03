# Playbook — task-oriented procedures from The Design of Everyday Things

"When doing X: steps, checklist, decision rules." Chapter references in parentheses. For diagnosing a specific bad interaction see `diagnose-interaction.md`; for error-proofing see `design-for-error.md`.

## Table of contents
1. Review or audit an existing product, screen or device
2. Design controls and displays (mapping, grouping, modes)
3. Design feedback (timing, content, priority, progress)
4. Communicate a conceptual model through the system image
5. Reduce memory load: knowledge in the world, reminders, forms
6. Choose constraints and forcing functions
7. Decide on conventions, standards and changing them
8. Use sound, alarms and warnings
9. Run the human-centered design process (observation, ideation, prototyping, testing, iteration)
10. Do activity-centered design and task analysis
11. Analyze an accident or recurring error (root cause, Five Whys, Swiss cheese)
12. Design a checklist and an error-reporting culture
13. Balance security, safety and usability (deliberate difficulty)
14. Design for diverse and special populations
15. Make product and feature decisions under business pressure
16. Choose an innovation strategy and judge timing
17. Organize the product team and process

---

## 1. Review or audit an existing product, screen or device (ch. 1, 2, 4)
1. Pick 3–5 real goals a representative person brings to it (not features). Write each as a goal hierarchy by asking "why?" twice (ch. 2).
2. For each goal, walk the seven stages and answer the seven questions from the user's chair: What do I want? What are the alternatives? What can I do now? How? What happened? What does it mean? Did it work? Mark every question the product does not answer (ch. 2).
3. Score the seven principles: discoverability, feedback, conceptual model, affordances, signifiers, mappings, constraints (ch. 2). For each failure, name the missing element precisely (missing signifier, not missing "affordance"; wrong model implied by the controls; mapping needing labels; feedback later than 0.1 s; a mode that is not visible).
4. Look for the tell-tale symptoms of bad design: stuck-on signs and labels explaining controls (ch. 1); rows of identical switches or controls (ch. 4, 5); instructions needed for a simple thing (ch. 1, 4); users who memorize one setting and ignore the rest (ch. 1); people repeating actions harder (ch. 2); error messages instead of help (ch. 2); critical information that disappears from the screen (ch. 3).
5. Check the failure paths, not just the happy path: what happens after an interruption, a wrong press, a timeout, a lost connection? The hard part of design is when things go wrong (ch. 1, 2, 5).
6. Check all three levels: visceral (does it look and feel right?), behavioral (do expectations get confirmed by feedback?), reflective (what story will people tell afterward; how does the experience end?) (ch. 2).
7. Before criticizing, ask how the design came about (installer, contractor, purchasing department, competing disciplines) and propose what could have been done otherwise: "Don't criticize unless you can do better" (ch. 2).
8. Test in the realistic context with representative people rather than inspecting: usability is invisible in a showroom; pretend to cook a meal in the store (ch. 3).

## 2. Design controls and displays (ch. 1, 3, 4, 5)
- Mapping, in order of preference: control on the item itself; control adjacent to the item; controls laid out in the same spatial pattern as the items (ch. 3). Never map two dimensions onto one row (stove burners vs a row of knobs). If the layout cannot be spatial, use the activity instead (see §10) or standardize.
- Use natural correspondences: up = more/on, control moves in the direction of the effect; related controls grouped; controls near what they affect (Gestalt grouping and proximity) (ch. 1).
- Make controls for different purposes look and feel different (shape, size, color, position); keep easily confused controls far apart; hide controls irrelevant to the current operation behind extra effort (ch. 5).
- Avoid modes. If unavoidable: make the current mode obvious at all times, make modes visually distinct, and never let two modes accept the same input format with different units (vertical speed shown as four digits, angle as two) (ch. 5).
- Avoid identical opening steps for procedures that diverge later; make infrequent variants start differently and remind the user of the difference (capture slips) (ch. 5).
- Make physical constraints perceivable in advance (orientation of plugs, keys, batteries), or remove the constraint by making orientation irrelevant (ch. 4).
- Where a standard exists, follow it unless the new way is vastly superior. Do not invent private psychology ("mirror-image" faucet handles) (ch. 4).
- Keep physical affordances in mind when moving to touch screens: a screen cannot be hit with an elbow when hands are full (ch. 4).

## 3. Design feedback (ch. 1, 2)
- Acknowledge every action within 0.1 s. For longer operations show that work is in progress; if the duration is predictable show a progress indicator and a time estimate; show the range or the slowest value so expectations are exceeded.
- Say what happened and what to do next, not just "something happened." One cheap light or beep with coded patterns is not feedback.
- Show the resulting state and, where useful, the prediction ("now 75°, will be 72° in 20 minutes").
- Prioritize: confirm routine actions unobtrusively; make important signals attention-getting; coordinate and rank alarms so an emergency does not become a cacophony that operators silence.
- Do not over-communicate: too much feedback trains people to ignore or disable everything. Respect calm environments (no 3 a.m. beeps).
- Make feedback perceivable where attention is (a light is missed if the eyes are elsewhere; use sound or touch when eyes are busy).
- Keep feedback visible long enough to be used; never show critical information in a message that vanishes (ch. 3).
- For physical products, preserve natural informative sounds (clicks, latches) instead of replacing them with generic beeps (ch. 4).

## 4. Communicate a conceptual model through the system image (ch. 1, 2, 3, 6)
1. Write down the designer's model in one paragraph: what parts exist, what each control does, how state changes.
2. List every channel of the system image (the device's form and labels, displays, sounds, manual, packaging, website, help, what similar products taught the user) and check that each tells the same story.
3. Decide the simplest model that still predicts behavior correctly in the situations users meet, including failures; note which assumptions it depends on and what the user sees when they break (the "cloud" model when offline).
4. Make controls imply the real mechanism (two independent thermostats need two independent controls; one shared thermostat should not be presented as two). Show hidden state and causes (what the device is doing now, what it will do next, why).
5. Give structure to anything that must be learned; arbitrary sequences are rote and give no help when things go wrong. Where possible use skeuomorphic cues to let people modify an existing model rather than build a new one (ch. 4).
6. Confirm by testing: can five representative people predict what a control will do and explain what the display means? If they invent a different story, the system image is wrong.

## 5. Reduce memory load (ch. 3)
- Default rule: make remembering unnecessary. Put the needed information in the world where and when it is needed: visible options (menus), labels, state indicators, constraints, natural mappings.
- Assume working memory holds three to five items and is wiped by any distraction. Never require carrying a code from one screen to another; let information be entered as it is received (pilots keying ATC instructions straight into equipment).
- Split information across modalities (visual, auditory, haptic, spatial) to reduce interference.
- Chunk long numbers into meaningful segments; accept any intelligible input format for dates, times, phone numbers, names and amounts and normalize internally; show the expected format before, not after, an error (ch. 2).
- Reminders need both a signal and a message, delivered at the right time or place (time- and location-based triggers). Let the thing itself carry the reminder.
- For codes and passwords: complex rules push people to write secrets down and reuse them; prefer "something you have plus something you know"; do not make security so onerous that users prop the door open with a brick.
- When the environment changes (new coin, redesigned screen), expect confusion among experienced users whose descriptions were tuned to the old set; newcomers will be fine.
- Design for experts too: allow efficient operation from knowledge in the head, but keep the world knowledge available for novices, rare tasks and returning users (ch. 5).

## 6. Choose constraints and forcing functions (ch. 4, 5)
Decision rule for each possible wrong action, from strongest to weakest:
1. Make it impossible (physical constraint, shape coding, orientation-free parts).
2. Make the right sequence mandatory (interlock), keep the task alive until done (lock-in), or block entry to danger (lockout).
3. Make it semantically or logically obvious (only one place it can go; a leftover part signals error).
4. Make it culturally conventional (follow or set a standard).
5. Make it visible and reversible (signifier + feedback + undo).
Then: reduce the nuisance of each forcing function so people do not disable it; put the desired action directly in any blocking prompt; design the shelf that blocks the door, the gate that is noticed but not propped open. Poka-yoke: add simple jigs, asymmetric holes, covers on critical switches, colored dots beside keyholes.

## 7. Conventions, standards, and changing them (ch. 4, 6)
- If knowledge cannot be put in the device, standardize what must be in the head. Standards should encode the user's conceptual model of the action, not the mechanism.
- Decision table for change:
  - New way only slightly better: keep the convention.
  - New way vastly superior: change, change everything (no mixed systems), announce and support the transition, and expect complaints and a period of confusion regardless of merit.
  - Switching metaphors (which thing moves?) is the most disruptive kind of change; pilots need training and testing to switch instrument conventions.
- Expect committee standards to take five years or more and to be compromises; standardize neither too early (locks in primitive technology) nor too late (too many incompatible practices). Build for conversion between formats.

## 8. Sound, alarms and warnings (ch. 1, 4, 5)
- Use sound to convey what cannot be seen and when the eyes are busy; make it informative about the source and the action (natural or naturalistic sounds with rich spectra), not a generic beep.
- Criteria for a continuous presence sound (electric vehicles): alerting, orientation (location, speed, approaching or receding), lack of annoyance, and a balance of standardization (interpretable by everyone) with individualization (trackable, brand). Silence where sound is expected is a feedback failure.
- Warnings: loud or bright enough to notice, not so much that they are disabled; must both capture attention and say what the event is; coordinate across instruments (standards) so emergencies do not produce simultaneous uninformative alarms. Speech warnings work when few, in quiet environments, and when operators need not converse.
- Expect disabled alarms to stay disabled (memory lapse); design restoration into the procedure.

## 9. Run the human-centered design process (ch. 6)
Overriding rule: solve the right problem first (double diamond: discover, define; then develop, deliver).
1. **Observation (design research)**: go where the product will be used; watch real people doing the real activity (applied ethnography); match the intended population by activity more than demographics; for other countries go there and include natives; study purchasers as well as users. Do not rely on what people say they need or do.
2. **Ideation**: generate many ideas; no criticism; question every assumption with "stupid" questions; run ideation for the problem as well as the solution.
3. **Prototyping**: fastest possible mock-ups (sketches, cardboard, slides, index cards, skits, Wizard of Oz with a hidden human). In the problem phase, an existing product the population uses is a prototype.
4. **Testing**: five representative people, individually (or in pairs thinking aloud; groups if the product is used by groups); use it as they really would; observe unobtrusively; record; retrace their steps afterward. Then fix and test five more; repeat rather than testing twenty once.
5. **Iteration**: fail frequently, fail fast; each cycle sharpens the problem and the prototypes; converge after a few cycles; stop when the product manager's schedule says so.
6. Combine with management gates: iterate inside the stages; delay rigid specifications until prototypes have been tested; keep schedule, budget and quality under control.
7. Pair design research (deep, tens of people, real needs) with market research (broad, thousands, what sells); specs must cover both buying and using.

## 10. Activity-centered design and task analysis (ch. 4, 6)
1. Name the activity (high-level goal) and decompose it into tasks and operations; include the exceptional cases observed in the field.
2. Build the product's conceptual model around the activity's conceptual model; package the tasks of one activity so they flow without interfering with each other (the whole music activity, not just playback).
3. For control panels, prefer activity-centered presets ("lecture", "video") over device-centered screens, but only after a detailed activity analysis; always keep manual controls, and invoking a manual adjustment must not cancel the current activity.
4. For worldwide products, trust that activities are similar across cultures but verify local modifications and symbolic/fashion roles.
5. Accept necessary complexity that feels essential to the activity; eliminate arbitrary requirements.

## 11. Analyze an accident or recurring error (ch. 2, 5)
1. Treat it like a bridge collapse: the goal is redesign, not blame. Do not stop when a person is found; that is where the analysis begins.
2. Reconstruct what the people knew and saw at the time (hindsight bias); ignore early press and executive statements.
3. Five Whys: keep asking why beyond the proximate cause; expect multiple contributing causes (Swiss cheese), including procedures, time pressure, social pressure, interruptions, modes and misleading displays.
4. Classify each human contribution: slip (action, memory lapse, capture, description-similarity, mode) or mistake (rule-based, knowledge-based, memory-lapse) or deliberate violation (routine or situational, usually caused by unworkable rules). Each class has its own fix (see `design-for-error.md`).
5. Decide fixes at the system level: add defensive layers, shrink holes (better displays, constraints, forcing functions), diversify mechanisms so holes do not align, alert when several holes line up, and change the rules that force violations. Then verify the change was actually made.
6. Make the error reportable without punishment (Jidoka, NASA-style semi-anonymous reporting).

## 12. Design a checklist and an error-reporting culture (ch. 5)
- Two people: one reads, the other performs, the reader confirms. Avoid "do now, check later."
- Design the list iteratively with subject-matter experts and designers; cover the essentials without burden; most objections are to bad lists, not to checklists.
- Do not force sequence unless the task requires it; let items be skipped and tracked, and block completion until all are done (electronic lists do this).
- Senior people should insist on the checklist; it increases rather than threatens authority.
- Reward reporting; thank reporters; separate reporting from punishment; aggregate reports to find patterns.

## 13. Security, safety and deliberate difficulty (ch. 3, 6)
- Decide which single part must be hard (keeping people in or out, dangerous operations, secrets, two-person actions, child resistance, games); design everything else by the normal rules.
- To make something hard, invert the principles deliberately: hide components, use unnatural mappings, require physical effort or precise timing, give no feedback, make state uninterpretable.
- Watch for the point where security defeats itself: too-complex passwords get written down; too-secure doors get propped open; forcing functions get bypassed.
- Every safety feature can create a secondary hazard; design the signifiers for the barrier as well.

## 14. Design for diverse and special populations (ch. 6)
- There is no average person; decide explicitly whom a single design excludes (95th percentile leaves out 5%) and whether to offer multiple versions.
- Prefer flexibility and adjustability (size, height, angle, lighting, font size, contrast) over fixed dimensions.
- Design aids to be good for everyone and market them that way; avoid designs that advertise infirmity; make them desirable (color, style).
- Larger, higher-contrast text helps everyone; expect reduced near focus from the mid-forties, slower reaction and divided attention with age, and compensate.

## 15. Product and feature decisions under business pressure (ch. 7)
- Before adding a feature, ask who demanded it (existing customers, a competitor's list, a saturated market needing an upgrade reason, a new technology) and whether it serves a real need or only matches the herd.
- Strengthen strengths; be good enough elsewhere; ignore irrelevant weaknesses; make the whole product consistent, coherent and understandable.
- Budget feature removal as well as addition; count the discoverability and understanding cost of each addition.
- Satisfy every customer class (users, purchasers, distributors, investors) but stay customer-obsessed about real needs.
- Keep designers in contact with customers; a company that forbids it cuts its own feedback loop.
- Remember distributors and purchasing departments often decide on price and feature lists; make usability a purchasing requirement by making its costs (training, service calls, lost time) visible.

## 16. Innovation strategy and timing (ch. 2, 7)
- Use HCD hill climbing for incremental improvement; it will not find a different hill. For radical ideas, revisit the goal (root cause analysis) or new technology's meaning, and accept that most radical attempts fail and successes take decades.
- Timing rule of thumb: ~20 years from lab demonstration to product, then 10–20 more to wide adoption. Being first does not guarantee success; a failed early product often returns later under another company. Check whether the technology is cheap and reliable enough and whether the culture is ready.
- Respect the legacy problem: an installed base and learned habits beat a modestly better design (QWERTY vs Dvorak); change only when the gain clearly exceeds the pain.
- Weigh the moral and environmental cost of model years, planned obsolescence and feature bloat.

## 17. Organize the product team and process (ch. 1, 6, 7)
- Assume Norman's Law (behind schedule and over budget on day one) and plan for it: field research done continuously, before the project exists; prototypes ready early.
- One multidisciplinary team with design, engineering, manufacturing, marketing, sales, service and support present from the launch decision through shipping, service and returns; conflicts resolved jointly, not serially.
- Treat downstream groups as users of the design output; collect their requirements at the start to avoid piecemeal changes later.
- Hold exploration to deadlines and budgets; expect the final result in the last 24 hours.
- Mix ages and backgrounds on the team; younger members experiment, older ones bring wisdom.
