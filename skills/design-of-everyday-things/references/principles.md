# Principles and concepts — The Design of Everyday Things (Norman, rev. ed. 2013)

Each entry: definition (Norman's terms), why it matters, how to apply, pitfalls. Chapter attributions in parentheses.

## Table of contents
1. Foundations: discoverability, understanding, HCD, the three models and the system image, paradox of technology
2. The fundamental principles of interaction: affordances, signifiers, mappings, feedback, conceptual models, constraints, forcing functions, conventions and standards
3. The psychology of action: gulfs, seven stages, seven questions, feedforward/feedback, seven principles, three levels of processing, emotion and expectation, flow, storytelling and blame, learned helplessness
4. Knowledge in the head and in the world: precise behavior from imprecise knowledge, memory types and limits, approximate models, reminders, the world/head trade-off, culture and metaphors
5. Human error: definitions, slips, mistakes, detection, social pressure, checklists, reporting, Swiss cheese, resilience, automation, design principles for error
6. Design thinking: double diamond, HCD cycle, activity-centered design, iteration vs waterfall, Norman's law, multidisciplinary teams, inclusive design, complexity vs confusion, standardization, deliberate difficulty
7. Design in business: competition, featuritis, timing, incremental vs radical innovation, legacy, moral obligations, rise of the small

---

## 1. Foundations

### Discoverability and understanding (ch. 1)
- **Discoverability**: can the person figure out what actions are possible and where/how to perform them? **Understanding**: what does it all mean, how is it supposed to be used, what do the controls and settings mean? Norman calls these the two most important characteristics of good design.
- Why: when discoverability fails (the invisible-hinge glass doors) people get stuck; when understanding fails they memorize one setting and ignore the rest (the washer-dryer).
- Apply: discoverability comes from five concepts (affordances, signifiers, constraints, mappings, feedback); understanding comes from the sixth, the conceptual model.
- Pitfall: a simple thing that needs a sign (PUSH, PULL, "DON'T PUSH!") or a manual is a design failure. Complex devices may legitimately need instruction; everyday things should not.

### Human-centered design, HCD (ch. 1, 6)
- An approach that puts human needs, capabilities and behavior first, then designs to accommodate them. A philosophy and set of procedures, not an area of focus (industrial, interaction and experience design are areas of focus; HCD is the process that makes any of them fit people).
- Core moves: understand people through observation (people are often unaware of their real needs); avoid specifying the problem as long as possible; iterate on rapid approximations, revising both the approach and the problem definition after each test.
- Design must communicate machine-to-person: what actions are possible, what is happening, what is about to happen. The hard and necessary part is making things work when they go wrong, not only when they go right.

### Designer's model, user's model, system image (ch. 1)
- Three vertices: the **designer's conceptual model**, the **user's mental model**, and the **system image** = everything the user can perceive: the product's look and behavior, prior experience with similar things, sales literature, ads, website, manuals, help lines.
- Why: designer and user never talk; the whole burden of communication rests on the system image. An incoherent, incomplete or contradictory system image yields a wrong user model (the refrigerator with two controls).
- Apply: audit every channel of the system image for one consistent story; make sure it supports the user when things go wrong, which is when a model is actually needed.

### The paradox of technology (ch. 1)
- The same technology that simplifies life by adding functions complicates it by making devices harder to learn and use. Many functions, little room for controls or signifiers (the watch).
- Apply: resist adding functions without adding ways to discover and understand them; where the device cannot carry the knowledge, standardize so it is learned once.

### The design challenge (ch. 1, 6)
- A product must be usable, attractive, affordable, reliable, manufacturable, serviceable, distinguishable, and bought. Every discipline (marketing: price and features; engineering: reliability; manufacturing: existing plants; support: fewer service calls) is right.
- Apply: put representatives of all constituencies in the same room for the whole process; clashes come from disciplines working independently and passing results downstream.
- Purchaser and user often differ; in the store people judge price, appearance, prestige; at home, function and usability.

---

## 2. The fundamental principles of interaction

### Affordance (ch. 1, 4)
- A **relationship** between the properties of an object and the capabilities of the agent that determines how the object could possibly be used. Not a property: a chair affords lifting to a strong adult, not to a child. Term from J. J. Gibson.
- **Anti-affordance**: the prevention of interaction (glass blocks passage). **Perceived affordance**: an affordance that is visible; invisible affordances exist but do not help (glass hides its anti-affordance, so people and birds hit it).
- Why: visible affordances let people act without labels (flat plate affords pushing; knobs afford turning, pushing, pulling; slots afford inserting).
- Apply: make the desired affordances perceivable and use their physical form to constrain action (a push bar can only be pushed). If an affordance or anti-affordance cannot be perceived, add a signifier.
- Pitfalls: saying "I added an affordance" when you added an arrow or label; that is a signifier. Perceived affordances can be misleading (things that look pushable but are not) and can be accidental (a flat-topped wall collects cups).

### Signifier (ch. 1, 4)
- Any mark or sound, any perceivable indicator that communicates appropriate behavior to a person: what actions are possible, where and how. Deliberate (a PUSH sign, an arrow, the panic bar's colored band) or accidental (a trail through snow, a bookmark showing pages left, people waiting on a platform). Intention does not matter; perceivability does.
- Why: "Affordances determine what actions are possible. Signifiers communicate where the action should take place." For designers, signifiers matter more than affordances because they are what communicates.
- Apply: for every possible action ask what signals it and where. Prefer signifiers built into the form (plate, handle shape, recess) over added words. Signifiers also carry feedback ("the feedback is well communicated").
- Pitfalls: hand-lettered signs stuck on products mean the design failed. Gesture-controlled faucets and towel dispensers have good mappings but no signifiers, so people cannot tell broken from empty from wrong gesture.

### Mapping and natural mapping (ch. 1, 3, 4)
- **Mapping**: the relationship between two sets of things, e.g., controls and the things they control. **Natural mapping**: exploiting spatial analogies and cultural/biological correspondences so the relationship is immediately understood (move the control up to move the thing up; up = more; arrange switches like the lights; a seat control shaped like the seat).
- Three levels, in decreasing effectiveness (ch. 3): (1) controls mounted directly on the item controlled; (2) controls as close as possible to the item; (3) controls arranged in the same spatial configuration as the items.
- Gestalt grouping and proximity: group related controls; put controls near what they control. Mappings are also helped by temporal contiguity.
- Why: good mapping puts the knowledge in the world and reduces memory load and error; bad mapping (four burners in a rectangle, four knobs in a row, four possible assignments all in commercial use) guarantees errors even after years.
- Pitfalls: "natural" is culture- and metaphor-dependent (which button is "next"? does the window move or the text?). Expect confusion whenever a metaphor is switched. Standardize if a natural mapping is impossible.

### Feedback (ch. 1, 2, 4)
- Communicating the results of an action and the current state. Rules Norman gives:
  - **Immediate**: even a delay of a tenth of a second (0.1 s) can be disconcerting; modern systems aim to acknowledge within 0.1 s; too-long delays make people give up or repeat the action.
  - **Informative**: cheap beeps and blinking lights say "something happened" but not what or what to do; coded flash/beep patterns cannot be learned, differ per device, and you cannot tell which device spoke.
  - **Planned and prioritized**: confirm every action unobtrusively; important signals must capture attention; in emergencies even important signals need prioritization, otherwise everything alarms at once and operators waste time silencing alarms.
  - **Not too much**: too much feedback is worse than too little (backseat driver, 3 a.m. dishwasher beep); people disable everything and miss the critical signal.
- For long operations show progress (hourglass, progress bar); when predictable show a time estimate; underpredict: show the range or the slowest value so expectations are exceeded.
- Pitfall: poor feedback can be worse than none because it distracts and provokes anxiety. Lack of feedback makes people assume the action did not register and repeat it harder or more times (toggle actions then cancel).

### Conceptual model (ch. 1, 2, 3, 6)
- An explanation, usually highly simplified, of how something works. It need not be complete or accurate, only useful: it lets people predict the effects of actions and figure out what to do when things go wrong. **Mental models** are the conceptual models in people's heads; one person can hold several, even conflicting, models.
- Why: without a model people operate by rote and are helpless in novel situations or failures. A wrong model implied by the device (two refrigerator controls implying two thermostats; a thermostat treated as a valve) makes correct use impossible.
- Apply: project the model through the system image: controls that imply the real mechanism, displays that show state and what the device is doing and will do (the Nest-style display: current temperature, target, heating/cooling color, "will be 72° in 20 minutes"). Simplified models are fine as long as the assumptions behind them hold (the "cloud" model breaks when the connection drops). A good conceptual model is the single most important principle for taming complexity (ch. 6).
- Pitfalls: people invent stories from fragmentary evidence; in the absence of information their imagination fills the gap with a plausible wrong model.

### Constraints: physical, cultural, semantic, logical (ch. 3, 4)
- **Physical**: the world limits what fits (a big peg will not fit a small hole). Most effective when easy to see and interpret, so the action set is restricted before anything is tried; otherwise they only block a wrong action after the attempt (batteries, keys, USB plugs: constrained, but the orientation is hard to perceive).
- **Cultural**: learned conventions and schemas/scripts/frames for what is acceptable (red light at the rear; elevator etiquette). They change over time (yellow headlights).
- **Semantic**: the meaning of the situation limits sensible actions (the rider faces forward; the windshield goes in front). Also change with technology (brake lights on self-driving cars).
- **Logical**: what remains must go in the remaining place; a leftover part after reassembly signals an error. Natural mappings work by providing logical constraints.
- Why: constraints let people act correctly in novel situations without instructions (the 15-piece Lego motorcycle assembled by people who were not told what it was) and dramatically reduce what must be remembered (10 parts = 3.5 million orders in principle, only a few real choices).
- Apply: for each decision the user must make, ask which constraint could remove it. Prefer constraints that are visible in advance.

### Forcing functions: interlocks, lock-ins, lockouts (ch. 4, 5)
- A forcing function is a physical constraint in which failure at one stage prevents the next step (the car will not start without the key or token).
- **Interlock**: forces operations into the proper sequence (microwave cuts power when the door opens; automatic transmission leaves Park only with the brake pressed; dead man's switch).
- **Lock-in**: keeps an operation active and prevents premature stopping (the "save before quitting?" prompt; playpens).
- **Lockout**: prevents entering a dangerous space or triggering an event (the gate that stops people fleeing a fire from running into the basement; child caps; fire-extinguisher pin; ATM returns the card before the cash).
- Why: the strongest tool against memory-lapse slips and dangerous actions. Pitfall: forcing functions are a nuisance, so people disable them (tie down the dead man's switch, prop open the door). Minimize nuisance while keeping the safety value; make the desired action available directly from the prompt (the save prompt became Norman's preferred way to exit).

### Conventions, standards, and the principle of desperation (ch. 4, 6)
- Conventions are cultural constraints about how to behave; some become standards or laws. The interpretation of a perceived affordance is itself a convention (a knob on a door means "open"; the same knob on a wall means "hold").
- **Standardization is a cultural constraint**: once you learn one car you can drive any car. "If all else fails, standardize": when knowledge cannot be put into the device, standardize what must be kept in the head. Standards should encode the psychological conceptual model, not the physical mechanics (blade faucet handles: both pulled toward you for more water, even though that means opposite rotations).
- Changing conventions: people always object; the merits are irrelevant, the change itself is upsetting. If a new way is only slightly better, stay consistent. If you change, everybody must change; mixed systems confuse everyone. If vastly superior, change and expect a period of confusion (destination-control elevators, metric system, scrolling direction, attitude indicators).
- Standards take years (five or more), are political, often an inferior compromise or several incompatible standards (HDTV: about 35 years, multiple formats). Standardize too early and you lock in primitive technology; too late and no agreement is possible.

---

## 3. The psychology of action

### The gulfs of execution and evaluation (ch. 2, 5)
- **Gulf of Execution**: the gap between what the person wants to do and figuring out how the device does it. **Gulf of Evaluation**: the effort needed to interpret the device's state and judge whether the goal was met. The designer's job is to bridge both.
- Bridge execution with signifiers, constraints, mappings and a conceptual model (feedforward). Bridge evaluation with feedback and a conceptual model. The evaluation gulf is small when state information is easy to get, easy to interpret, and matches how the person thinks about the system.
- Either gulf is an opportunity for product enhancement; learn to observe them.

### The seven stages of action (ch. 2)
1. Goal (form the goal)
2. Plan (the action)
3. Specify (an action sequence)
4. Perform (the action sequence)
5. Perceive (the state of the world)
6. Interpret (the perception)
7. Compare (the outcome with the goal)
- Three execution stages (plan, specify, perform), three evaluation stages (perceive, interpret, compare), plus the goal. Behavior can be goal-driven (start at the top) or event/data-driven (start from the world); much everyday behavior is opportunistic. Skilled behavior runs the stages subconsciously; attention is needed only when something is novel or blocked.
- Goals form hierarchies; asking "why?" repeatedly (root cause analysis) finds the real goal: people do not want a drill, nor a hole; they want shelves up, or maybe no shelves at all. Incremental innovation comes from the gulfs; radical innovation from reconsidering the goal.

### The seven fundamental design questions (ch. 2)
One per stage; a product should let the person answer all seven at any time:
1. What do I want to accomplish?
2. What are the alternative action sequences?
3. What action can I do now?
4. How do I do it?
5. What happened?
6. What does it mean?
7. Is this okay? Have I accomplished my goal?
- **Feedforward** answers the execution questions (signifiers, constraints, mappings, conceptual model). **Feedback** answers the evaluation questions (explicit information about the effect of the action, interpreted through the conceptual model). Both must be presented in a form that matches the person's goals and expectations.

### The seven fundamental principles of design (ch. 2)
1. **Discoverability**: it is possible to determine what actions are possible and the current state of the device.
2. **Feedback**: full and continuous information about results of actions and the current state; after an action the new state is easy to determine.
3. **Conceptual model**: the design projects all the information needed to create a good conceptual model, leading to understanding and a feeling of control.
4. **Affordances**: the proper affordances exist to make the desired actions possible.
5. **Signifiers**: effective signifiers ensure discoverability and intelligible feedback.
6. **Mappings**: the relationship between controls and their actions follows good mapping, enhanced through spatial layout and temporal contiguity.
7. **Constraints**: physical, logical, semantic and cultural constraints guide actions and ease interpretation.

### Three levels of processing: visceral, behavioral, reflective (ch. 2)
- **Visceral**: fast, automatic, subconscious judgments of good/bad, safe/dangerous; driven by appearance, sound, touch, smell; almost no learning; no cause assigned. For design: style and immediate perception; attraction or repulsion, independent of usability.
- **Behavioral**: home of learned skills; largely subconscious; every action carries an **expectation**; feedback confirming or disconfirming expectations produces satisfaction/relief or disappointment/frustration. Feeling of control comes from understanding plus knowledge of results; lack of feedback produces a feeling of lack of control. The emotional system reacts to changes of state.
- **Reflective**: conscious, slow, after the fact; assigns causes, hence guilt/pride and blame/praise; produces the longest-lasting emotions and the memories that drive recommendations.
- Design must work at all three. "Attractive things work better": strong visceral appeal can outweigh behavioral difficulties in reflective memory; but heavy frustration, especially at the end of use, can erase visceral positives. Understanding arises at behavioral + reflective; enjoyment requires all three.
- Mapping to stages: visceral = approaching the task and sensing the world; behavioral = expectations on the execution side and their confirmation on the evaluation side; reflective = goal/plan setting and the final comparison.
- Subconscious vs conscious thought (Table 2.1): subconscious is fast, automatic, multi-resource, controls skilled behavior; conscious is slow, controlled, limited, invoked for novel situations, learning, danger and things going wrong. Positive affect broadens and favors creativity; negative affect focuses (too much: tunnel vision).

### Flow (ch. 2)
- Immersion when the challenge slightly exceeds skill so full attention is continually required (Csikszentmihalyi). Too easy: boredom and apathy; too hard: frustration, anxiety, helplessness. Expectation-based emotions at the behavioral level drive it.

### People as storytellers, blaming the wrong things (ch. 2)
- People look for causes and build conceptual models from fragmentary evidence; two events in succession are assumed causal. Absence of feedback is read as "I did it wrong," so the action is repeated, harder (deaths at inward-opening exit doors; hence outward doors and panic bars). Delayed electronic feedback leads to repeated presses, all of which register.
- Attribution: we blame our own odd behavior on the environment and others' on their personality; but with everyday objects we blame ourselves, which hides the real design fault behind a conspiracy of silence (the Return/Enter key users who never reported losing work).

### Learned helplessness and positive psychology (ch. 2)
- Repeated failure leads people to decide a task cannot be done by them and stop trying; a few bad experiences suffice. Everyday things and math curricula produce "taught helplessness" and self-fulfilling prophecies.
- Replace "failure" with "learning experience"; fail often, fail fast. Norman's advice to designers: do not blame people; treat their difficulties as signifiers of where the product can improve; eliminate error messages in favor of help and guidance; let people fix the problem from the message and continue, never start over; assume what they did is partially correct.
- Norman's credo: eliminate the term human error; treat interaction as collaboration; the machine should accept normal human behavior and judge the quality of what it is given to catch slips; minimize inappropriate actions with affordances, signifiers, mapping and constraints; maximize the chance that an inappropriate action is discovered and rectified with intelligible feedback and a clear model.

---

## 4. Knowledge in the head and in the world

### Precise behavior from imprecise knowledge (ch. 3)
Four reasons: (1) knowledge is both in the head and in the world; (2) great precision is not required: combined knowledge need only distinguish the right choice from the alternatives; (3) natural (physical) constraints exist in the world; (4) cultural constraints and conventions exist in the head. People only remember enough to discriminate among the items they usually face (fewer than half of students recognized the correct penny; new coins too similar to old ones fail: the French 10-franc coin was withdrawn within weeks). When the set changes, previously sufficient descriptions fail.

### Declarative vs procedural knowledge (ch. 2, 3)
- **Declarative** ("knowledge of"): facts and rules; easy to write and teach; may be false; knowing a rule does not mean following it. **Procedural** ("knowledge how"): skills; hard to describe; taught by demonstration, learned by practice; subconscious, behavioral level.

### Memory: structure and limits (ch. 3)
- **Short-term/working memory**: the just-present; automatic and effortless but tiny and fragile. Traditional capacity five to seven items (ten to twelve with rehearsal); for design assume **three to five**. Capacity is in items (chunks). Any distraction wipes it. Design rules: do not count on much being retained; never show critical information in a message that disappears when it is needed (nurses writing on their hands because the record system logs them out when interrupted); use multiple modalities: visual, auditory and haptic information interfere little with each other (driving is visual, so give instructions by sound and lane warnings by seat/wheel vibration on the appropriate side).
- A useful approximate model: "five memory slots; each new item knocks out an old one." Scientifically wrong, good enough for design.
- **Long-term memory**: slow in and out; reconstructive, so biased and subject to false memories; retrievable only under the interpretation used at storage; effectively unlimited in size; the problem is retrieval (tip of the tongue; a wrong retrieval blocks the right one, so switch activity).
- **Arbitrary vs meaningful** material: rote learning of arbitrary sequences (commands, gestures, key sequences) is slow, and when something goes wrong the memorized sequence gives no hint of what to do. Meaningful structure (a conceptual model, even a technically wrong one such as the motorcycle turn-signal reinterpretation) makes things learnable. Best of all, make memory unnecessary by putting the information in the world (menus you can scan).

### Approximate models (ch. 3)
- Practice needs "good enough," not truth: °C ≈ (°F − 30) / 2 is within about 3 °F (1.7 °C) across −5 to 25 °C; 27 × 293 ≈ 30 × 300 = 9,000 (14% high), minus 3 × 300 = 8,100 (within 2%). Conceptual models need only produce correct behavior in the intended situation. Write things down: "it is things that make us smart."

### Reminders and prospective memory (ch. 3)
- A reminder has two parts: the **signal** (something is to be remembered) and the **message** (what). A string on the finger is signal only; a note is message only; a good reminder has both and arrives at the right time or place (too early or too late is useless). Put the burden on the thing itself (keys under the book you must take).

### The trade-off between knowledge in the world and in the head (ch. 3, Table 3.1)
- World: available whenever perceivable; interpretation replaces learning (how easily depends on the designer); slower to find and interpret; high ease at first encounter; can be cluttered and inelegant. Head: available only if in working memory, otherwise effort; requires learning (easier with structure or a good model); efficient once automated; low ease at first encounter; nothing need be visible, so cleaner looks at the cost of learnability. World knowledge depends on the environment staying stable; "out of sight, out of mind." Screens hide information unless it is always shown.
- Experts can run on knowledge in the head; still provide knowledge in the world for novices, rare operations and returning users (ch. 5).

### Transactive memory and distributed cognition (ch. 3, 7)
- Groups reconstruct what no member could alone; technology ("cybermind") provides clues and candidates. The person plus the artifact is what is smart; without the artifacts we are less capable, and that is normal. Human + machine + good process beats either alone (freestyle chess).

### Culture, metaphors and "natural" (ch. 3)
- What is natural depends on point of view and metaphor: does the person move through the content or the content toward the person (next-slide button; moving-window vs moving-text scrolling; outside-in vs inside-out attitude indicators)? Time lines run left-to-right or right-to-left with writing direction; some cultures put the past in front or orient time to the compass. Design trouble appears when metaphors are switched; people eventually adapt.

---

## 5. Human error

### Definitions (ch. 5)
- **Error**: any deviance from "appropriate" behavior (often known only after the fact). Two classes: **slips** and **mistakes**. Deliberate **violations** (routine or situational) are intentional and are organizational/societal problems, outside this classification; they are often caused by rules written for legal compliance rather than real work, and rewarded when they succeed.
- 75–95% of industrial accidents are attributed to human error; at that rate the real cause is design. Treat human failures like bridge collapses: find the fundamental cause and redesign. If the system lets you make the error it is badly designed; if it induces the error it is really badly designed. If many people make the same error, look for another cause; "I knew better" is not an analysis.

### Slips (ch. 5)
- Intend one action, do another; goal right, execution wrong. Occur more in skilled people (automatic performance, low attention) than novices. Two classes: **action-based** (wrong action performed) and **memory-lapse** (intended action not done or results not checked).
- **Capture slip**: a more frequent or recent activity with the same opening steps captures the intended one at the divergence point. Design: avoid procedures with identical opening steps that then diverge; make sequences differ from the start; provide reminders for the infrequent variant.
- **Description-similarity slip**: correct action on the wrong object because the internal description is too vague (shirt into the toilet; identical flap and gear switches). Worse when tired, stressed, or when many similar objects are present. Design: make controls and displays for different purposes significantly different in look and feel (shape coding), and keep easily confused controls far apart.
- **Memory-lapse slip**: steps skipped or repeated, outcome forgotten, goal forgotten; immediate cause is interruption. Design: minimize steps, give vivid reminders of remaining steps, and use forcing functions (card out before cash; chained pens).
- **Mode error**: the same control means different things in different states; inevitable when there are more functions than controls. Design: avoid modes; if unavoidable, make the current mode highly visible and distinct; never rely on the user remembering a mode set long ago (Airbus −3.3° vs −3,300 ft/min; the ship silently in dead-reckoning mode). "Mode error is really design error."

### Mistakes (ch. 5)
- Wrong goal or plan, or faulty comparison; the actions match the plan, the plan is wrong. Novices make more mistakes; experts more slips. Rasmussen's levels: **skill-based** (errors are slips), **rule-based** (wrong rule chosen = mistake; execution error = slip), **knowledge-based** (novel situation, conscious problem solving; the conceptual model is essential).
- **Rule-based mistake**: situation misclassified, wrong rule applied; or correct rule but the rule is faulty; or correct rule but outcome misevaluated. Hard to detect because evidence supports the wrong classification and matching to memory is biased by recency, regularity and uniqueness. Design: present system state coherently, ideally graphically; offer alternative interpretations.
- **Knowledge-based mistake**: misdiagnosis from wrong or incomplete knowledge (fuel computed in pounds instead of kilograms). Needs a good conceptual model, cooperative problem-solving tools, procedure guides keyed to observations; humans and automation designed as a collaborative system.
- **Memory-lapse mistake**: forgetting the goal, plan or the evaluation already made (often after interruption), so decisions are remade wrongly. Design: keep goals, plans and current evaluation continuously visible; do not erase them once acted upon; assume interruption and support resumption.
- Mistakes are hard to detect: nothing signals a wrong goal; correctly executed actions add false confidence; misdiagnoses are plausible, so initial actions look helpful; anomalies get explained away (Las Vegas billboards on the road to Mammoth). Once a misdiagnosis is made, all later information is read through it; fresh eyes at shift turnover or after a break help.

### Hindsight (ch. 5)
- Knowing the outcome makes it look obvious and predictable (Fischhoff). During an incident there is too much irrelevant information, high workload and stress. Judge operators by what they knew then; distrust early reports; wait for careful investigations.

### Social and institutional pressures (ch. 5)
- Time and economic pressure, authority gradients and the wish not to look foolish drive risky decisions (Tenerife, Air Florida, divers not dropping weights). Counter with training, rewarding safety over economics, making dangers visible and explicit; design alone is insufficient.

### Checklists (ch. 5)
- Proven to reduce slips and memory lapses, especially under interruptions and with multiple people. Best: two people, one reads, one executes (and the reader confirms). Worse: one does, another checks later. Paradox: more checkers can mean less care. Resistance comes from pride and authority lines; senior insistence raises authority. Design iteratively with experts and designers; do not force sequence unless the task requires it; electronic lists can track skipped items and refuse completion until all are done.

### Reporting error (ch. 5)
- Errors can only be reduced if admitted and collected; reward reporting, do not punish. Toyota's **Jidoka** (stop the line, converge, ask why until the root cause is fixed), **poka-yoke** (simple jigs, fixtures, asymmetric parts, switch covers that make the correct operation the only one; green dots beside keyholes), NASA's semi-anonymous aviation reporting system with immunity for self-reported minor infractions.

### Root cause analysis and the Five Whys (ch. 2, 5, 6)
- Keep asking why past the first "human error"; the analysis has only just begun when a person is found. Not exactly five; the name means keep going. Limits: "why" is ambiguous; investigators stop at the limit of their understanding; it biases toward a single cause.

### The Swiss cheese model (ch. 5)
- Accidents require holes in many defensive layers to line up; any one "if only" would have prevented it, but none is "the" cause. Reduce accidents by adding layers of defense, reducing the number and size of holes (better design), using different mechanisms in different layers so holes do not align, and alerting operators when several holes have lined up. "Design redundancy and layers of defense."

### Resilience engineering (ch. 5)
- Design systems, procedures, management and training so people can cope with complexity under pressure; continually assess, test and improve, including deliberately failing live systems because small simulations miss the real stress. Safety is a core value shown by events that do not happen; measure the ability to create foresight.

### The paradox of automation (ch. 5)
- Automation takes the dull tasks and does them well, then gives up on the complex ones, exactly when help is needed, usually without warning, with the human out of the loop. Fewer accidents, but bigger ones. Pilots have minutes and training; drivers have fractions of a second and none. Reliable automation erodes manual checking (Royal Majesty).

### Design principles for dealing with error (ch. 5)
- Assume every possible mishap will happen; minimize opportunities and mitigate consequences. Put the knowledge in the world; use constraints, forcing functions and natural mappings; bridge both gulfs with feedforward and feedback. Add sensibility checks, undo, prominent display of the object being acted upon, and help instead of error messages. Embrace error: understand causes, assist rather than scold. See `design-for-error.md`.

---

## 6. Design thinking

### Solve the correct problem (ch. 6)
- Never solve the problem as given; it is usually a symptom. Designers diverge first, treating the stated problem as a suggestion, asking why (Five Whys), generating many directions, then converge. "A brilliant solution to the wrong problem can be worse than no solution at all."

### The double diamond (ch. 6)
- British Design Council (2005): diverge and converge to find the right problem (**discover**, **define**), then diverge and converge to find the right solution (**develop**, **deliver**). Expect to loop back when the problem was misformulated; the second pass is faster. Managers: encourage exploration, hold the schedule and budget; a firm deadline forces convergence.

### The human-centered design cycle (ch. 6)
- Four activities iterated as a spiral: **observation**, **ideation**, **prototyping**, **testing**, used inside both diamonds. Observation = applied ethnography in the real context with people matching the intended population (activities matter more than demographics; go to the country, include natives). Ideation: many ideas, no criticism, question everything with "stupid" questions. Prototyping: sketches, cardboard, slides, skits, Wizard of Oz. Testing: five representative people, pairs thinking aloud, observe and record, debrief; fix and test five more. Requirements made in the abstract or by asking people are invariably wrong; they come from watching people; most cases are "special," so allow for special cases.
- Design research (deep, qualitative, tens of people: what people need) and market research (broad, quantitative, thousands: what people buy) answer different questions; both are required.

### Activity-centered design; tasks vs activities (ch. 6)
- For worldwide, heterogeneous populations design around the activity: let the conceptual model of the product follow the conceptual model of the activity. People accept complexity and learning that feel essential to the activity (driving) and reject arbitrary requirements. An activity is a set of tasks toward a high-level goal; a task is a cohesive set of operations toward a low-level goal; designing for tasks alone is too restrictive (the iPod supported the whole activity: discover, buy, load, playlist, listen, share). Goal levels: be-goals, do-goals, motor-goals.

### Iterative vs linear (waterfall, gated) development (ch. 6)
- Iteration is best early and for getting the specification right; it scales poorly to huge projects. Gates give management control but are slow. Best practice: iterate inside stages between gates; delay precise specifications until rapid prototypes have been tested, while controlling schedule, budget and quality. Even large systems can be prototyped (scale models, 3-D prints, drawings, animation, virtual reality).

### Norman's Law of Product Development (ch. 6, 7)
- "The day a product development process starts, it is behind schedule and above budget." Schedules are set by outside events; staffing takes unscheduled time; "next time we'll do it right" never comes. Remedies: keep design and market researchers permanently in the field so findings pre-exist the project; run multidisciplinary teams with all disciplines present from launch decision to returns and repairs; design the time and money constraints into the process.

### Multiple conflicting requirements (ch. 1, 6, 7)
- Purchasers (developers, purchasing departments, distributors) often are not users and buy on price and feature lists; usability is seldom specified, yet it costs the buyer later in time, service calls, training and morale. Study purchasers as well as users. Downstream groups (engineering, manufacturing, sales, service) are users of the design team's output; if their needs are ignored they change the design piecemeal and weaken it.

### Designing for special people; inclusive design; stigma (ch. 6)
- There is no average person; the 95th percentile excludes 15 million Americans, the 99th still 3 million (70 million worldwide). Sometimes make several versions. Aids are rejected when they advertise infirmity; design them to be good for everyone and market them that way (the OXO peeler). Universal design helps all: larger high-contrast type, adjustability. Flexibility (adjustable sizes, heights, lighting, fonts, contrast) is the best general answer; fixed solutions always fail someone.

### Complexity is good; confusion is bad (ch. 6)
- Tools must match complex tasks; "complicated" means confusing. Confusion lives in the mind, not the object; a good conceptual model turns complex into understood.

### Deliberately making things difficult (ch. 6)
- Legitimate when keeping people in or out, security, dangerous equipment or operations, secrets, disrupting routine actions, two-person controls, child resistance, games. Make only the one critical part difficult; the rest follows normal rules. The rules in reverse: hide critical components, use unnatural mappings for execution, make actions physically hard, require precise timing, give no feedback, make state hard to interpret. Safety features create secondary hazards that need their own signs.

---

## 7. Design in the world of business

### Competitive forces (ch. 7)
- Companies compete on price, features and quality, often in that order, plus speed. Development cycles of one to two years mean the next model starts before the current ships; feedback from customers seldom reaches designers; distributors and investors are customers too. Zeitgeist: ideas are "in the air," competitors appear before launch.

### Featuritis / creeping featurism (ch. 7)
- After success, pressure to add features comes from customers wanting more, competitors adding features, and saturated markets needing an upgrade reason. No budget to remove features. Products become unusable (the 15-piece Lego motorcycle became 29 pieces and needed instructions). Matching competitors feature for feature makes products identical (Moon). Strategy: strengthen your strengths, ignore irrelevant weaknesses, be "good enough" elsewhere; leadership must withstand marketing; focus obsessively on customers' real needs (Bezos), which usually survives only while the founder leads.

### Timing: how long it takes (ch. 7)
- Rule of thumb: about 20 years from first lab demonstration to commercial product, then one to two decades to widespread adoption; most innovations fail; good ideas fail when too early and succeed later with different companies (digital cameras, multitouch, videophone: 140 years from concept). Technology changes fast; people and culture slowly; old products linger. Large companies are failure-averse; startups try and mostly fail.

### Incremental vs radical innovation; hill climbing (ch. 7)
- Incremental = hill climbing by test-and-refine (the heart of HCD); it finds the top of the current hill, never a higher hill. Radical innovation starts fresh, driven by new technology or a reconsideration of what the technology means (the Internet collapsing publishing, broadcasting and music into "information providers"); rarely succeeds and takes decades. HCD cannot produce radical innovation. "Radical innovation changes lives and industries. Incremental innovation makes things better. We need both."

### The legacy problem and Stigler's law (ch. 4, 7)
- Installed bases block better designs (batteries, keys, QWERTY: Dvorak is only slightly faster; "the gain is not worth the pain"). Credit goes to whoever capitalized, not who originated; originating is the easy part.

### Moral obligations of design (ch. 7)
- Durable goods face saturation, so businesses use planned obsolescence, fashion cycles, model years and subscriptions, at environmental cost. "The design of everyday things is in great danger of becoming the design of superfluous, overloaded, unnecessary things." Design succeeds only if people buy, use and enjoy; it is flawed if it cannot be engineered or manufactured within cost and schedule; consider the full life cycle including service, repair and recycling.

### The rise of the small (ch. 7)
- Cheap tools (sensors, motors, 3-D printing, self-publishing, video, open source) let individuals and small groups design and manufacture; developing nations produce "handed-up" technology that is simpler and lower-power. The fundamental principles (discoverability, feedback, affordances, signifiers, mappings, conceptual models) remain permanent.
