# Design-for-error checklist

Norman's premise (ch. 5): errors are inevitable because machines demand precision, alertness and accuracy that people are not built for; so assume every possible mishap will happen, minimize the opportunities and mitigate the consequences. "Human error" usually means design error. Use this checklist when designing or reviewing any flow where a wrong action is possible.

## A. Attitude and process
- [ ] The word "error" is not used to blame; difficulties are treated as signifiers of where the design must improve (ch. 2).
- [ ] The design has been reviewed for what happens when things go wrong, not only the intended path (ch. 1, 2).
- [ ] If several people make the same error, the design, not the people, has been changed; teaching the mapping is not the fix (ch. 5).
- [ ] Observed errors and near-misses are collected without punishment and analyzed with the Five Whys past the first human cause (ch. 5).
- [ ] Rules and procedures are checked against real work: if following them would stop the job, they will be violated and successful violations rewarded; fix the rule (ch. 5).

## B. Prevent: knowledge in the world and constraints
- [ ] The information needed to operate is visible at the point of need; experts may ignore it, novices, rare tasks and returning users rely on it (ch. 3, 5).
- [ ] Physical constraints make wrong insertions, orders and connections impossible, and the constraint is perceivable before trying (ch. 4).
- [ ] Logical and semantic constraints remove choices (only one place left; a leftover part means error) (ch. 4).
- [ ] Natural mappings and cultural conventions are used; no private "clever" mappings (ch. 1, 3, 4).
- [ ] Forcing functions are applied where a skipped step is dangerous: interlocks (right sequence), lock-ins (cannot quit early), lockouts (cannot enter danger); the forgettable step comes before the goal (card before cash) (ch. 4, 5).
- [ ] Each forcing function's nuisance is low enough that it will not be tied down, taped over or propped open; the desired action is available directly from any blocking prompt (ch. 4).
- [ ] Poka-yoke: simple jigs, asymmetric parts, covers on critical switches, colored marks that make the correct operation the only or obvious one (ch. 5).
- [ ] Critical or irreversible controls are segregated and covered; irrelevant controls are off the current screen (ch. 5).

## C. Prevent slips
- [ ] Controls, displays and objects for different purposes are significantly different in appearance, position and feel (shape coding); no rows of identical switches or meters (ch. 4, 5).
- [ ] Easily confused controls are physically far apart (ch. 5).
- [ ] Procedures that share opening steps with a more frequent procedure have been redesigned to differ from the first step; the infrequent variant has a visible reminder at the branch (capture) (ch. 5).
- [ ] Modes are eliminated; any remaining mode is continuously visible, visually distinct, and does not accept the same input with a different meaning (Airbus: four digits vs two) (ch. 5).
- [ ] The number of steps is minimized; steps still to do are vividly indicated; completed steps are visible (memory lapse) (ch. 5).
- [ ] The design assumes interruption: on return, the goal, the place in the sequence and the system state are still displayed; nothing critical has timed out or auto-logged out without preserving state (ch. 3, 5).
- [ ] Critical phases are protected from interruption where possible (sterile periods); multitasking is not required (ch. 5).
- [ ] Working memory load stays within three to five items; information is captured as it arrives; different streams use different modalities (ch. 3).
- [ ] Input accepts any intelligible format and normalizes it; no arbitrary precision is demanded of the person (ch. 2, 5).

## D. Prevent mistakes
- [ ] The system state is presented coherently, ideally graphically, in the user's terms, including what the device is doing and will do (ch. 2, 5).
- [ ] The conceptual model is explicit and correct for the situations users meet, including failures; the system image does not imply a false model (ch. 1, 2).
- [ ] Alternative interpretations and the evidence for them can be seen, so a misdiagnosis can be revisited; handovers or breaks are built in for long incidents (ch. 5).
- [ ] Units and scales are unambiguous (pounds vs kilograms; a.m./p.m. vs 24-hour; angle vs rate) (ch. 5).
- [ ] Unfamiliar but correct feedback (ABS pulsing) is explained or redesigned so it is not read as malfunction (ch. 5).
- [ ] Guides and procedures are keyed to observable symptoms; human and automation are designed as a collaborative team, with the human kept in the loop and told when automation hands back or degrades (ch. 5).
- [ ] Goals, plans and the current evaluation are kept on display; they are not erased once acted upon (ch. 5).

## E. Detect: feedback
- [ ] Every action is acknowledged within 0.1 s; long operations show progress and an (under-)estimated time (ch. 1, 2).
- [ ] Feedback says what happened and what it means, not just that something happened; it is perceivable where the person's attention is (ch. 1).
- [ ] The resulting state is visible immediately, so a slip can be noticed by the discrepancy between intended and actual (ch. 5).
- [ ] Absence of action (memory lapse) is made visible: pending items, unfinished checklists, "card still in machine" signals (ch. 5).
- [ ] Warnings are prioritized and coordinated; they attract attention and name the event; they are not so frequent or similar that they get ignored or disabled; disabled warnings are restored by design (ch. 1, 5).
- [ ] Sensibility checks: values far outside the person's or the domain's normal range (1000x dose, a million-dollar transfer) are questioned before execution (ch. 5).
- [ ] Automation failures and mode switches announce themselves loudly, not in tiny letters (ch. 5).

## F. Correct: recovery
- [ ] Undo exists wherever possible, ideally multi-level; deletions go to a recoverable trash; "don't save" keeps a hidden copy that can be restored (ch. 5).
- [ ] Irreversible actions are harder to do than reversible ones and are clearly marked as irreversible (ch. 5).
- [ ] Confirmations show the object being acted upon prominently (enlarged, colored) and the action, with "cancel" and "do it" — not a yes/no about an unnamed thing; the design recognizes that confirmations catch slips (unexpected dialog) but rarely mistakes (expected dialog) (ch. 5).
- [ ] Error messages are replaced by help and guidance that lets the person fix the problem in place and continue; the person is never made to start over; partial input is kept and treated as approximately right (ch. 2).
- [ ] The person can tell what state the system is in after a failure and what the appropriate next actions are (ch. 2).

## G. Layers and resilience
- [ ] No single act by a single person can cause widespread damage; defensive layers are counted (Swiss cheese), holes shrunk, and mechanisms diversified so holes do not align (ch. 2, 5).
- [ ] Operators are alerted when several layers have failed at once (ch. 5).
- [ ] Two-person collaborative checklists (reader + executor + confirmation) are used for complex, interruptible procedures; lists do not force sequence unless the task does; skipped items are tracked and block completion (ch. 5).
- [ ] Safety features have been checked for the secondary hazards they create and signified accordingly (ch. 6).
- [ ] Backups and recovery procedures are exercised under realistic conditions, not only in simulations (resilience engineering) (ch. 5).
- [ ] Social and time pressures are addressed: the safe choice (stopping, reporting, dropping the weights) is rewarded, dangers are made visible, authority gradients are offset by procedure (ch. 5).
- [ ] Where people truly are at fault (fatigue, intoxication, lack of training), limits and licensing apply — but this is not assumed by default (ch. 5).

## H. Final questions
- Can one simple slip cause large or irreversible damage? If yes, you are not done.
- Would an expert returning after a year, or a novice under interruption, still get it right?
- Have you tested the failure paths with five representative people?
