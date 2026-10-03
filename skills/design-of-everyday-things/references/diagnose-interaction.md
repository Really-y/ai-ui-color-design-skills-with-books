# Diagnose a bad interaction — step-by-step procedure

Use when someone reports "people can't figure out X," "users keep doing Y wrong," or when you yourself are stuck with a device, screen, form or control. Output: a located failure (which stage), a named deficiency (which principle), an error classification, and a fix that changes the design rather than the person. Based on ch. 2 (seven stages, seven questions, seven principles), ch. 4 (constraints, discoverability, feedback) and ch. 5 (error classification).

## Step 0. Set the frame
- Start from the premise that the difficulty is in the design, not the person; if several people have the same trouble, that is evidence, not coincidence (ch. 2, 5).
- Collect what actually happened from observation or a retraced walkthrough, not from the summary "user error." People under-report their own errors and over-report system faults, so ask specifically about near-misses and workarounds (ch. 2, 5).
- Write down the person's real goal by asking "why?" at least twice; the proximate goal ("press the right button") is rarely the real one (ch. 2).

## Step 1. Walk the seven stages and answer the seven questions
For the goal in question, go through each stage from the person's chair and record whether the product answers the question. The first unanswered question is usually where the breakdown starts.

| Stage | Question the person must answer | What the design must supply (feedforward or feedback) | Typical failures |
|---|---|---|---|
| 1 Goal | What do I want to accomplish? | A conceptual model that shows what the product is for and its current state | Product does not reveal its purpose or state; wrong goal adopted from a false model |
| 2 Plan | What are the alternative action sequences? | Visible options, structure, constraints that prune impossible plans | Options hidden in modes or menus; no way to see alternatives |
| 3 Specify | What action can I do now? | Signifiers and perceivable affordances; constraints that remove wrong actions | No signifier; misleading perceived affordance; identical-looking controls |
| 4 Perform | How do I do it? | Mappings between control and effect; physical form guiding the motion; conventions | Unnatural or inconsistent mapping; needs precise timing or format; mode-dependent meaning |
| 5 Perceive | What happened? | Immediate (≤0.1 s), perceivable feedback where attention is | Nothing visible/audible; feedback too late, too faint, or gone before it can be read |
| 6 Interpret | What does it mean? | Informative feedback plus the conceptual model | A beep or a code; a message in system terms; no indication of cause or next step |
| 7 Compare | Is this okay? Did I reach the goal? | Visible resulting state in the user's terms; explicit success/failure; recovery path | State hidden; delayed effect (24 hours for the refrigerator; 5 s for the shower); no undo |

Record: execution-side failures (stages 2–4) mean the **Gulf of Execution** is too wide; evaluation-side failures (5–7) mean the **Gulf of Evaluation** is too wide (ch. 2).

## Step 2. Check each of the seven principles
Mark each as OK / weak / missing, with the specific evidence.
1. **Discoverability**: can a newcomer tell what actions are possible and what state the device is in without instruction? Evidence of failure: signs, labels, manuals, "you'll get used to it."
2. **Feedback**: is every action acknowledged immediately, informatively, at the right priority, and is the new state easy to see? Evidence: repeated presses, people pushing harder, waiting, disabling alarms.
3. **Conceptual model**: does the system image (form, controls, displays, documentation, prior experience) project one coherent model that predicts behavior and explains failures? Evidence: users' stories contradict the mechanism; they operate by rote.
4. **Affordances**: do the needed affordances exist and are they perceivable? Evidence: physically possible actions people never attempt; anti-affordances that cannot be seen (glass).
5. **Signifiers**: is each action signified where it happens, by form or by mark or sound, unambiguously? Evidence: perceived affordances that mislead; gestures with nothing indicating them.
6. **Mappings**: do controls relate to their effects by position, shape, direction and timing (on the item, next to it, or in its spatial pattern)? Evidence: labels needed to pick the right control; different products use different mappings.
7. **Constraints**: do physical, cultural, semantic and logical constraints remove wrong choices before they are tried? Evidence: parts fit the wrong way; wrong-order steps possible; forcing functions bypassed.

## Step 3. Check the memory and attention load (ch. 3, 5)
- Does any step require holding more than three to five items, or carrying information across screens, interruptions, or a delay?
- Is critical information shown in something that disappears (toast, timeout, auto-logout)?
- Is there a mode, and is it visible at all times?
- Does the procedure share its opening steps with a more frequent procedure and diverge later?
- Does the interface assume uninterrupted attention? What happens on resumption?
- Is a precise, arbitrary format or sequence demanded that the machine could infer?

## Step 4. Classify the error (ch. 5)
Decide first: was the goal/plan right and the execution wrong (**slip**), or was the plan itself wrong (**mistake**), or did the person knowingly break a rule (**violation**)?

**Slips** (goal right; more common in experienced users):
- Action slip, **capture**: a familiar sequence took over at the branch point. Fix: differentiate sequences from the first step; remind at the branch.
- Action slip, **description-similarity**: right action, wrong object because objects look/feel alike. Fix: make objects and controls distinct; separate them; reduce the number of similar things present.
- **Mode error**: control meant something else in the current state. Fix: remove the mode; otherwise make it continuously visible and distinct; use different input formats per mode.
- **Memory-lapse slip**: a step skipped or repeated, outcome not checked, usually after interruption. Fix: fewer steps; vivid reminders of what remains; forcing functions that order the goal after the forgettable step.

**Mistakes** (plan wrong; more common in novices and in novel situations):
- **Rule-based**: situation misclassified or a bad rule applied or outcome misjudged. Fix: show state coherently and graphically; offer alternative interpretations; fix the rule; make unusual feedback understood (ABS pulsing).
- **Knowledge-based**: wrong or missing knowledge, misdiagnosis. Fix: supply the conceptual model; guides keyed to observations; design human + automation as collaborators; fresh eyes for stuck diagnoses.
- **Memory-lapse mistake**: goal, plan or earlier evaluation forgotten. Fix: keep goals, plans and current status continuously on display; support resumption.

**Violations**: routine (so common it is ignored) or situational. Fix the rule or procedure that makes compliance impossible; stop rewarding successful violations; make the safe choice socially rewarded.

Also note: was it a chain? Many failures are a mistake plus a slip (oven at maximum, then wandering off) or several layers lining up (Swiss cheese).

## Step 5. Judge detectability and recoverability (ch. 5)
- Could the person have noticed the error? Action slips need visible results; memory lapses produce nothing to see; mistakes produce consistent actions that look right.
- How costly is it, and is it reversible? Is there undo, a trash, a confirmation that shows the object, a sensibility check against normal ranges?
- Did hindsight make the "obvious" signal look obvious? Reconstruct what was visible at the time.

## Step 6. Find the systemic causes (ch. 2, 4, 5, 6)
- Ask why at least five times past the person: time pressure, interruption, unworkable rules, authority gradient, missing training or currency, poor purchase specs, legacy constraints, coordination failures among the people who built and installed the thing.
- List every layer that could have stopped it; propose adding layers, shrinking holes and diversifying mechanisms.

## Step 7. Choose the fix, strongest first (ch. 4, 5)
1. Remove the possibility (physical constraint, orientation-free part, no mode).
2. Force the right sequence or block the dangerous one (interlock, lock-in, lockout, poka-yoke).
3. Make it obvious before acting (signifier, natural mapping, visible state, grouping, shape coding).
4. Make it correctable after acting (immediate informative feedback, undo, trash, sensibility check, prominent display of the object in confirmations).
5. Make it standard (follow or set a convention) and make the knowledge available in the world for novices, rare tasks and returning users.
6. Only then: documentation, training, warnings — and never blame.
Reject fixes that consist of "tell users to be careful," "add a warning beep," or "write it in the manual" unless everything above is impossible.

## Step 8. Verify
- Prototype the fix and test with five representative people doing the real task, in pairs thinking aloud; iterate.
- Check that the fix did not add a mode, a step, a similar-looking control, or a new secondary hazard, and that forcing functions are not so annoying that they will be disabled.
- Re-walk the seven stages and confirm every question is now answerable.

## One-page checklist
- [ ] Real goal identified (why? why?)
- [ ] Seven questions answered from the user's chair; first unanswered one marked
- [ ] Gulf located: execution or evaluation
- [ ] Seven principles scored with evidence
- [ ] Memory/attention/mode/interruption load checked
- [ ] Error classified: slip (capture, description-similarity, mode, memory-lapse) / mistake (rule, knowledge, memory-lapse) / violation
- [ ] Detectability and reversibility judged; hindsight bias discounted
- [ ] Five Whys past the person; contributing layers listed
- [ ] Fix chosen from the strongest rung possible; no blame-based fixes
- [ ] Fix tested with five people and re-walked
