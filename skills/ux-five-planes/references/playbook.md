# Playbook: task-oriented procedures from *The Elements of User Experience* (2nd ed.)

"When doing X: steps, checklists, decision rules." Chapter references in parentheses. For per-plane
question lists and deliverables see `planes-checklist.md`.

## Table of contents

Strategy
1. Write product objectives
2. Define success metrics
3. Segment users and choose research
4. Build personas and the strategy document

Scope
5. Decide whether and how much to document requirements
6. Elicit requirements (stakeholders, users, scenarios, competitors)
7. Write a requirement (and review one)
8. Write content requirements; prioritize and cut scope

Structure
9. Choose and apply a conceptual model
10. Design error handling
11. Build an information architecture (top-down + bottom-up, structure class, organizing principles)
12. Build nomenclature, controlled vocabulary, thesaurus and metadata
13. Document the structure (architecture diagram)

Skeleton
14. Sort a skeleton problem (interface / navigation / information design)
15. Decide whether to follow or break a convention; use or drop a metaphor
16. Design an interface screen (priority, defaults, control selection)
17. Design navigation and wayfinding
18. Produce wireframes at the right level

Surface
19. Review a visual design (follow the eye, contrast, uniformity)
20. Make a design system consistent (internal and external)
21. Build a color palette and type system
22. Produce design comps and a style guide

Process
23. Diagnose which plane a UX problem is on
24. Run user testing that asks the right questions
25. Rescue a project that is sprinting / cutting foundations

---

## Strategy

### 1. Write product objectives (ch. 3)
1. Answer in writing: *What do we want to get out of this product?* Then separately: *What do our users
   want to get out of it?*
2. Calibrate each objective: if it reads "make money / save money", push for *how this product* does
   that; if it names a feature or technology ("real-time text tool"), pull back to the outcome it is
   supposed to produce for the organization and the user.
3. Add a brand-identity objective: list the specific conceptual associations and emotional reactions
   the product should create (the impression forms anyway).
4. Check the objective describes conditions for success without prescribing the path.
5. Note relationships among objectives and any priority order (this ordering will later decide feature
   priorities, ch. 4).

Decision rule: an objective is good when a stranger could later judge whether the product met it, yet
it does not tell the designer what to build.

### 2. Define success metrics (ch. 3)
1. For each objective, pick an indicator trackable after launch (analytics: time per visit, visits per
   registered user per month, conversion rate, impressions; indirect: support calls, sales-cycle time).
2. Decide the direction you want (time per visit up for exploration, down for get-in-get-out).
3. Confirm the metric is tied to user behavior that the design can shape; UX influences return visits,
   not initial acquisition.
4. Set a target line and plan to read the metric alongside outside events (competitor campaigns, press,
   marketing) rather than in isolation.
5. Reject metrics that can be inflated at users' expense (extra navigation layers to raise impressions).

### 3. Segment users and choose research (ch. 3)
1. Start from the candidate segmentation axes: demographics; psychographics; attitude toward
   technology (hours online/week, enjoys tech?, upgrades early or late?); subject-matter expertise;
   social/professional role.
2. Research, then revise: split segments whose needs differ, merge those whose needs match. Keep only
   as many segments as there are distinct sets of needs.
3. Look for opposed needs (novice step-by-step vs expert all-in-one). If found, decide now: serve one
   segment, or build two paths. Record the decision; it ripples through every plane.
4. Choose methods by question type:
   - What are users' attitudes/perceptions? -> surveys, interviews, focus groups (write down exactly what
     you need to learn first; "what they do" vs "why").
   - How do they actually behave with the product? -> user tests, field studies.
   - Need deep understanding of their context and resources allow? -> contextual inquiry (expensive).
   - Need the precise steps of a task? -> task analysis via story interviews or field observation.
   - How do they group content? -> card sorting with several users.
   - Nothing built yet? -> test paper sketches, lo-fi mockups or click-through prototypes.
5. Balance depth vs breadth: more time per participant means fewer participants.
6. Low budget: mine server logs and feedback messages; recruit friends/family/co-workers for informal
   tests (ch. 8).
7. Include rank-and-file staff who talk to customers daily; they know what users struggle with.

### 4. Build personas and the strategy document (ch. 3)
Persona sheet (one per distinct need set; the book shows two):
- Name + stock photo; a one-line quote capturing the attitude ("I need quick answers" / "I want a site
  that will explain everything").
- Age, occupation, family, household income.
- Technical profile: comfort with technology, device and age, connection, hours online per week.
- Internet use: where (home/work split) and for what; favourite sites.
- Keep details consistent with research; invent the specifics. Post them; use them as a test
  ("Would that work for Janet?").

Strategy/vision document:
- Objectives + user needs, with an analysis of how they relate and fit the organization.
- Supporting quotes from stakeholders, rank-and-file and users (a user research report may be separate,
  but one place is better).
- Concise. Shared with everyone on the team. Revised systematically as learning accumulates.

---

## Scope

### 5. Decide whether and how much to document requirements (ch. 4)
- Always define; "definition, not documentation". Write only what is needed to avoid confusion in design
  and development, and only decisions actually made.
- Size the detail to the project: a complex subsystem needs fine detail; a homogeneous content mass
  needs general requirements.
- Make the process lightweight enough to survive implementation changes (update, don't abandon).
- Signs you need it badly: "perpetual beta", no milestones, everyone describes the product
  differently, features appear from whatever someone read last night.

### 6. Elicit requirements (ch. 4)
1. Ask users (most productive) and stakeholders (most common) using ch. 3 methods.
2. Classify what you hear: (a) wanted and good; (b) a proposed solution that may address a symptom
   (ask what problem it solves, find the real requirement); (c) ideas nobody had yet (surface via
   brainstorming anchored to strategic objectives).
3. Run a cross-functional brainstorm (engineer, customer-service agent, marketer); insiders forget which
   constraints are real.
4. Generate from impediments: for a user who already decided to act, what removes friction from
   selecting and completing?
5. Write scenarios: a persona pursuing one need, step by step; harvest requirements from each step.
6. Mine competitors (how did they resolve the same trade-offs?) and non-competitors (features from other
   categories).
7. List product-wide requirements separately: branding, supported browsers/OS, hardware capabilities
   (camera, GPS, sensors).
8. Ask "what content does this function need?" (instructions, error messages) and "what functionality
   does this content need?" (CMS, workflow, formats, personalization).

### 7. Write a requirement, and review one (ch. 4)
Checklist for each requirement:
- [ ] Positive: says what the system does, not what it won't allow.
- [ ] Specific: terms like "popular", "highlighted", "fast" are defined (which metric, over what period,
      shown how).
- [ ] Falsifiable: someone could demonstrate it was NOT met.
- [ ] Objective: taste words replaced by a reference (branding guidelines document) or a number.
- [ ] Quantified where it can be (users, time, size).
- [ ] Traceable to at least one product objective or user need.
- [ ] Feasible (technology, resources, time) or explicitly deferred to a later release.

Rewrite ladder (from the book): "hip, flashy style" -> "meets the hipness expectations of Wayne the mail
clerk" (still arbitrary) -> "conforms to the company branding guidelines document" (testable).

### 8. Write content requirements; prioritize and cut scope (ch. 4)
Per content feature record:
- Purpose (the user need it serves), not just format; challenge "we need FAQs" with "what information
  do people need ready access to?"
- Content types involved (text, images, audio, video) and whether they can be produced.
- Rough size: word count; pixel dimensions; file size for downloads.
- Owner for creation and for ongoing maintenance.
- Update frequency, derived from objectives (how often should users return?) and needs (how often do
  they expect fresh information?), then compromised against resources.
- Intended audience(s).
- For existing material: a content inventory spreadsheet.

Prioritization procedure:
1. Map each requirement to the objectives/needs it serves (many-to-many is normal).
2. Score feasibility: impossible / resource-limited / time-limited / feasible.
3. Rank by the objective hierarchy from the strategy document.
4. Time-limited: move to a later milestone (v1.1). Resource-limited: ask whether a technology or
   organizational change lifts it; if not, defer. Impossible: drop.
5. Resolve feature conflicts by the strategic objectives (one-step order vs legacy data: which does
   strategy favor?).
6. For an out-of-scope idea that is feasible and good: check whether strategy has shifted; if you keep
   doing this, requirements started too early.
7. Stakeholder fights: restate each champion's feature as the goal it serves; show the goal can be met
   another way; be empathetic.

---

## Structure

### 9. Choose and apply a conceptual model (ch. 5)
1. For each major component, name the model: thing consumed / place visited / object acquired;
   container (cart), order form, magazine, etc.
2. Prefer the convention your users already know from other products (retail-store cart) unless you
   have a clear reason and an alternative users will interpret correctly.
3. Derive functions and vocabulary from the model (container -> add/remove, "put in / take out",
   checkout; order form -> edit, "send in").
4. Apply it consistently; never let an element be a place in one screen and an object in another.
5. Don't explain the model to users; don't render it literally (no telephone picture for reservations).
6. Validate: does the system's behavior match the implicit expectations users bring?

### 10. Design error handling (ch. 5)
Work through the layers in order for each risky action:
1. Can the error be made impossible (constrain inputs/states, like a car that won't start in gear)?
2. If not, can it be made difficult?
3. Will the user notice it happened? Provide a helpful message and an interface that makes the state
   legible (contrast the message on the surface plane, ch. 7).
4. Can the user fix it easily? If the system fixes it automatically, make sure that doesn't become
   something users must keep undoing.
5. For errors visible only later: provide recovery (undo or equivalent).
6. For unrecoverable actions: warn, and keep confirmations rare so the important one is noticed.
7. Write every error message as a content requirement (ch. 4).

### 11. Build an information architecture (ch. 5)
1. Set the node level explicitly (page, section, or in-page element).
2. Top-down pass: from objectives and user needs, draft the broadest categories and logical
   subsections (an empty shell).
3. Bottom-up pass: from the content inventory/requirements, group items into low-level categories,
   then higher ones.
4. Reconcile the two; where they disagree, ask which serves the users' foremost concerns.
5. Choose the structure class:
   - Hierarchical: default; parent/child; most common.
   - Matrix: when different segments browse by different attributes; cap at three dimensions for
     primary navigation.
   - Organic: exploration of evolving/unclear topics; accept weak sense of place; add remote tools so
     users can find things again.
   - Sequential: individual articles/sections; whole-product only when order is essential (training).
6. Pick organizing principles per level: top levels from objectives/needs (audience, geography,
   chronology); lower levels from content (sport, topic, product type).
7. Choose facets deliberately: the attributes foremost in users' minds for this audience (weight for
   shippers, make/model for consumers); do not expose every facet.
8. Validate with card-sort results and scenarios; judge flows by whether each step makes sense, not by
   step count.
9. Stress-test for growth: can a section absorb new items? Can a whole new section be added? When will
   the organizing principle need to change (daily press releases -> by topic)?

### 12. Build nomenclature, controlled vocabulary, thesaurus, metadata (ch. 5)
1. Collect the users' own terms from research; ban internal jargon.
2. Publish a controlled vocabulary: one approved term per concept, used by all content producers.
3. Extend to a thesaurus: map jargon, shorthand, slang, acronyms to approved terms; record broader /
   narrower / related terms; use it to spot alternative architectures.
4. Define a metadata schema per content type (e.g. author, date, piece type, product, product type,
   customer industry, related topics) and fill it using only vocabulary terms.
5. Wire search to the thesaurus and metadata so disallowed terms map to preferred ones and results
   include related recommendations.
6. Use consistent metadata to automate related links and to spin up new sections quickly.

### 13. Document the structure (ch. 5)
- Simple hierarchy: a text outline. Complex: spreadsheet/database plus a diagram.
- Diagram conceptual relationships (which categories belong together, how an interaction's steps
  connect), not every link. Call it an architecture diagram, not a site map. A standard notation
  (Visual Vocabulary) keeps diagrams readable across projects.

---

## Skeleton

### 14. Sort a skeleton problem (ch. 6)
Ask in order: Is it about letting users DO something (interface design)? GO somewhere (navigation
design)? UNDERSTAND something (information design)? Fix information design first when in doubt; good
navigation can't rescue bad information design.

### 15. Follow or break a convention; use or drop a metaphor (ch. 6)
Convention:
- Default to the convention users meet elsewhere (keypads, carts, standard controls).
- Deviate only when the new approach has a clear, articulable benefit; write the reason down.
- Rank internal consistency above external: same conceptual model -> same controls; "start / finish /
  go back / save" treated identically everywhere.
Metaphor test:
- Does it reduce mental effort for nearly all users (phone-book icon for a directory)? Keep.
- Could users read it several ways (telephone icon), does it depend on culture, or does it come from a
  physical constraint screens don't have (page turning)? Drop it and label plainly.

### 16. Design an interface screen (ch. 6)
1. From the interaction design, list the functions on this screen.
2. Rank them by likelihood of use; make the top ones easiest to notice and use; shrink, tuck away or
   remove the rest (edge cases don't get equal weight).
3. Set defaults to what most users want; remember prior selections if the technology allows.
4. Choose controls by trade-off:
   - independent options: checkboxes (list box if many);
   - mutually exclusive: radio buttons (dropdown if many and space is scarce, accepting hidden options);
   - six-ish options: prefer visible checkboxes/radios over a dropdown or free-text entry;
   - free text only when options are unbounded; action button to commit.
5. Check the screen also communicates (labels, instructions, errors): that is information design.

### 17. Design navigation and wayfinding (ch. 6)
1. Verify the three goals on every page: can users get where they need to go; are the relationships
   among nav items clear (importance, difference); is it clear how these items relate to this page?
2. Assume no memory between pages; every page states where the user is and where they can go.
3. Assemble the layers: global (key access points; ideally persistent), local (parent/siblings/
   children), supplementary (related shortcuts), contextual (inline links at the moment of need, kept
   sparse), courtesy (contact, feedback, policies).
4. Add remote tools: site map limited to two levels (if it needs more, fix the architecture); an index
   only for large, diverse content, possibly per section.
5. Add non-navigational wayfinding cues: section color coding (always reinforcing another cue), icons,
   labels, typography.

### 18. Produce wireframes at the right level (ch. 6)
1. Identify the small set of standard screen types (by functional/navigational diversity); one
   template may be enough for a small product.
2. For each, lay out: branding/logo, global nav, local nav, supplementary nav, courtesy nav, wayfinding
   cues, search controls, interface elements, content blocks, partner/secondary content.
3. Annotate: pointers to the architecture diagram, functional specs, content requirements, existing
   content locations; notes on intended behavior; optionally a navigational specification.
4. Build it jointly with the visual designer.
5. Choose fidelity by team distance: sketches + sticky notes for a co-located pair; formal documents for
   distributed teams. Don't under-document to save time.

---

## Surface

### 19. Review a visual design (ch. 7)
1. Where does the eye go first? Ask the designer, ask test users (call out elements in order), or
   squint/blur/view from across the room.
2. Is the first element strategically important or a distraction?
3. Does the eye flow smoothly, or bounce ("busy", "cluttered")? Does the path give a guided tour of the
   options relevant to the current task without hiding needed functions?
4. Does the look reinforce the structure (sections clearly distinct, options clear) or blur it?
5. Does it express the brand identity defined at strategy?
6. Contrast audit: are important elements (including error messages) clearly different? Are any two
   treatments similar-but-not-the-same? Is contrast overused into clutter?
7. Uniformity audit: consistent element sizes, grid placement, consistent use of each color/type style.

### 20. Make a design system consistent (ch. 7)
1. List recurring elements across interface, navigation and information design contexts.
2. Design each once in isolation; then try it in every context (checkout vs crowded customization
   page); rework until it works everywhere.
3. Check the elements form a system, not a pile of nice parts.
4. Check external consistency with the organization's other products and media at every level.
5. If the grid or standard no longer fits new functionality, revise the foundation rather than forcing it.

### 21. Build a color palette and type system (ch. 7)
- Palette: core brand colors inside a broader set chosen to complement; bold/bright for foreground
  attention, muted for backgrounds; every shade clearly distinguishable from its neighbors and used
  for one consistent purpose.
- Type: simple faces for body text; more personality only for large text and short labels; a handful
  of fonts; a new style only when it marks a different kind of information; enough contrast between
  styles; no near-duplicates.

### 22. Produce design comps and a style guide (ch. 7)
- Comp: build from the wireframe; keep a one-to-one mapping of components; preserve relative
  importance and grouping (especially information design) even if the layout changes.
- Style guide order: global standards first (grid, palette, typography, logo treatment), then
  section/function standards, then individual interface and navigation elements. Record reasons so the
  organization keeps its memory when people leave. Assign enforcement high enough to bind decentralized
  teams.

---

## Process

### 23. Diagnose which plane a UX problem is on (ch. 2, 8)
Use this ladder for any complaint ("the button is wrong", "users can't find X", "it feels off"):
| Symptom pattern | Likely plane | First check |
|---|---|---|
| Looks cluttered, colors clash, nothing stands out, brand feels off | Surface | eye path, contrast, palette/type consistency |
| Right function, wrong place/size/control; users miss it; can't tell where they are | Skeleton | interface priority, navigation layers, wayfinding cues, info grouping |
| Function doesn't behave as expected; categories make no sense; labels in jargon; errors trap users | Structure | conceptual model, IA/organizing principles, vocabulary, error layers |
| Feature missing or half-built; nobody owns content; scope keeps growing; stale content | Scope | requirements list, content owners/frequency, priorities |
| Nobody can say why the product exists or who it's for; metrics absent; segments conflict | Strategy | objectives, user needs, metrics, segmentation decision |
Then check the plane below the suspected one: an upper-plane symptom often has a lower-plane cause.
Also screen for the three unconscious modes: default (mirrors the database/org chart), mimicry
(copied convention), fiat (someone's preference).

### 24. Run user testing that asks the right questions (ch. 3, 8)
1. State the problem under investigation and the plane it sits on before recruiting.
2. Choose the artifact (finished product, work in progress, paper, lo-fi, click-through) by stage.
3. Strip unrelated issues from the prototype so they don't cloud the result (if testing wording,
   neutralize color).
4. Ask element-specific questions (navigation wording vs color; does the design reinforce the brand?).
5. Don't expect users to articulate needs; observe behavior and infer.
6. Never let testing replace design, and never schedule it only at the end as "acceptance".

### 25. Rescue a project that is sprinting / cutting foundations (ch. 2, 8)
1. Check what has been cut: strategy, scope and structure work are usually the first casualties and the
   most important.
2. Re-apply the scheduling rule: upper-plane work may continue, but it must not be finalized before
   the lower planes are.
3. Alternate pushes (prototypes, ideas) with pull-backs (test, integrate, refine the big picture).
4. For every current decision, demand "why did we do it that way?"; where the answer is default,
   mimicry or fiat, re-decide from objectives and user needs.
5. Expect deliberate decisions to cost time now and save more later; cite the cycle of "next project =
   fixing the last one" to the schedule owners.
