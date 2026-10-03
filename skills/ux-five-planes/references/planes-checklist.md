# Planes checklist: questions and deliverables per plane

Use to plan a product from scratch (work bottom-up, overlapping planes but finishing each only after
the one below) or to audit an existing product (walk every plane; a symptom on one plane usually has a
cause on the plane below). Each plane lists: the plane's question, the functionality side and the
information side, questions to answer, deliverables, and a pass test. Based on Garrett, *The Elements
of User Experience* (2nd ed.); chapter references in parentheses.

## Table of contents
0. Before you start: locating the problem and scheduling
1. Strategy plane (ch. 3)
2. Scope plane (ch. 4)
3. Structure plane (ch. 5)
4. Skeleton plane (ch. 6)
5. Surface plane (ch. 7)
6. Cross-plane audit (ch. 2, 8)
7. Minimal versions for small teams

---

## 0. Before you start (ch. 2, 8)

- [ ] Which plane is this task or problem on? (surface: look/feel; skeleton: placement, controls,
      navigation, info presentation; structure: flows, categories, behavior; scope: which features and
      content; strategy: why and for whom)
- [ ] Is the plane below it settled enough to build on? If not, start there (you may work in
      parallel, but you cannot finish above before finishing below).
- [ ] Is the product mostly functionality (tasks/tools), mostly information (find/absorb/understand),
      or a hybrid? Plan both columns.
- [ ] Who is responsible for thinking about each plane? (Titles don't matter; coverage does.)
- [ ] Can you answer "why did you do it that way?" for every existing decision? Flag answers of the
      form "the database works that way" (default), "everyone does it" (mimicry), "the boss likes it"
      (fiat).

## 1. Strategy plane (ch. 3)

Plane question: **Why are we making this product?**
Elements (shared by both sides): product objectives; user needs.

Questions
- [ ] What do we want to get out of this product? (specific to this product; neither "make money" nor
      a feature description)
- [ ] What do our users want to get out of it?
- [ ] What impression (brand identity: associations, emotional reactions) should the product leave?
- [ ] For each objective, which success metric will show it is met after launch? What is the target?
      Does the design actually influence that behavior? What outside factors could move it?
- [ ] Who are the users? Which segmentation axes matter (demographic, psychographic, attitude toward
      technology, subject expertise, role)? How many distinct need sets exist?
- [ ] Do any segments have opposed needs? If so: one segment, or two paths?
- [ ] What do we know vs assume about users? Which research fills the gaps (surveys/interviews/focus
      groups for attitudes; user tests/field studies for behavior; contextual inquiry; task analysis;
      card sorting; prototype tests)? What exactly do we want each study to tell us?
- [ ] Who are the stakeholders (owners of affected parts of the organization)? Which rank-and-file
      staff talk to users daily and should be heard?
- [ ] What does the competition do about the same needs and objectives?

Deliverables
- Strategy/vision document: objectives, user needs, analysis of their relationships and fit with the
  organization, supporting quotes, priority order among objectives; concise; shared with the whole team.
- Success metrics with targets and a review plan.
- User segments and personas (name, photo, quote, age, occupation, family, income, technical profile,
  internet use, favourite sites).
- User research report (may be part of the strategy document).

Pass test: a newcomer can read one short document and state why the product exists, for whom, what
"success" will look like in numbers, and which trade-off was made between conflicting user groups.

## 2. Scope plane (ch. 4)

Plane question: **What are we going to make?**
Functionality side: functional specifications. Information side: content requirements.

Questions
- [ ] Which requirements apply to the whole product (branding, supported platforms/browsers, hardware
      capabilities such as camera/GPS/sensors)?
- [ ] For each feature: which objective(s) and user need(s) does it serve? Is it feasible technically,
      in resources, in time? If not now, which later release?
- [ ] Have we distinguished what people say they want, what they actually need (symptom vs cause), and
      what they haven't imagined yet (brainstorm from objectives, cross-functionally)?
- [ ] Have we walked scenarios for each persona and harvested requirements from each step?
- [ ] Have we looked at competitors and non-competitors for how they met the same needs?
- [ ] Is each requirement positive, specific, falsifiable, non-subjective, quantified where possible?
- [ ] For each function: what content does it need (instructions, error messages, labels)? Who writes it?
- [ ] For each content feature: purpose (not just format), content types, rough size (words, pixels,
      file size), owner, update frequency, intended audience? What CMS/workflow functionality does it
      imply (languages, formats, approvals, personalization)?
- [ ] Do we have a content inventory of existing material?
- [ ] Which feature conflicts exist, and which strategic objective decides each?
- [ ] Which good ideas are out of scope and parked for later? Do any suggest a strategy shift?
- [ ] Are stakeholder feature fights being settled by appeal to strategy rather than politics?

Deliverables
- Functional specifications (requirements list) at the detail level the project needs.
- Content requirements table (purpose, types, size, owner, frequency, audience).
- Content inventory (for existing content).
- Prioritized scope: in this release / next milestone / dropped, with reasons.

Pass test: every team member can say what is and isn't being built now, each requirement can be shown
to be met or not, and every content feature has a named owner and an update rhythm.

## 3. Structure plane (ch. 5)

Plane question: **How do the pieces fit together into a cohesive whole?**
Functionality side: interaction design. Information side: information architecture.

Questions, interaction design
- [ ] For each component: what conceptual model (container, order form, place, object...) are we using?
      Is it the one users already hold from other products? If we break convention, why, and will users
      interpret the new model correctly?
- [ ] Is each model applied consistently (never a place here and an object there)? Are we avoiding
      literal metaphors?
- [ ] How does the system respond to every likely user action (the "dance")?
- [ ] For each risky action: can the error be made impossible? difficult? Will users notice and be able
      to fix it? Is there recovery (undo)? For unrecoverable actions, is there a noticeable warning, and
      are confirmations rare enough to be noticed? Does any auto-correction become a nuisance?

Questions, information architecture
- [ ] What is our node level (page, section, element)?
- [ ] Top-down: what broad categories follow from objectives and user needs?
- [ ] Bottom-up: what groupings emerge from the actual content inventory? Where do the two disagree?
- [ ] Which structure class fits: hierarchical, matrix (<= 3 dimensions as primary nav), organic,
      sequential? Different classes in different areas?
- [ ] Which organizing principle at each level (audience, geography, chronology at top; content topics
      lower)? Which facets are foremost in users' minds, and which are deliberately not exposed?
- [ ] Does each flow make sense step by step (not: is it the fewest clicks)?
- [ ] Can the structure absorb new items and new sections? When will the organizing principle need
      revisiting?
- [ ] Are labels in the users' language? Is there a controlled vocabulary? A thesaurus mapping jargon,
      slang, acronyms? A metadata schema per content type, filled with vocabulary terms? Is search
      wired to them?

Deliverables
- Architecture diagram (conceptual relationships; standard notation), or outline/spreadsheet for simple
  or very complex cases.
- Conceptual-model notes per component.
- Error-handling matrix (action -> prevention / correction / recovery / warning).
- Controlled vocabulary or thesaurus; metadata schema.

Pass test: someone can trace any persona's scenario through the diagram, each step following
naturally; any new content item has an obvious home and consistent metadata; no label uses internal
jargon.

## 4. Skeleton plane (ch. 6)

Plane question: **What form does the structure take on each screen?**
Functionality side: interface design. Information side: navigation design. Both: information design.

Questions
- [ ] For each screen problem: is it about doing (interface), going (navigation) or understanding
      (information design)? Is information design sound before navigation is polished?
- [ ] Which conventions do our users bring? Where do we deviate, and what clear benefit justifies it?
- [ ] Are features with the same conceptual model using the same controls? Are "start/finish/back/save"
      treated identically everywhere?
- [ ] Do any metaphors invite multiple readings or depend on culture? Can plain labels replace them?
- [ ] On each screen: what do users most likely do? Is that easiest to notice and use? What is hidden
      or removed? What are the defaults, and do they match most users' intent? Can prior choices be
      remembered?
- [ ] Is each control the right trade-off (checkbox / radio / text field / dropdown / list box / action
      button) given option count, space and user load?
- [ ] Navigation on every page: can users get where they need to? Are relationships among nav items
      clear? Is their relation to the current page clear? Would a user arriving from a search engine
      know where they are?
- [ ] Which navigation layers exist: global (persistent?), local, supplementary, contextual (sparse),
      courtesy? Remote tools: site map (two levels max), index (only for large diverse content)?
- [ ] Wayfinding cues beyond navigation: color coding (reinforcing another cue), icons, labels,
      typography?
- [ ] Information presented in the groupings and order users think in? Charts and icons chosen for
      comprehension? Error and instructional messages designed and written?
- [ ] Wireframes for the standard screen types, annotated with links to diagram and requirements,
      built with the visual designer, at a fidelity matching team distance?

Deliverables
- Wireframes (page schematics) for each standard screen type, annotated.
- Navigation specification (if needed).
- Control and default decisions; information-grouping decisions.

Pass test: a developer can build any screen's behavior from the wireframe and its references; a first-
time visitor landing on any page can say where they are and where to go; the most common task on each
screen is the most visible path.

## 5. Surface plane (ch. 7)

Plane question: **How does it reach the senses, and does that serve everything below?**
Element (shared): sensory design (vision mainly; also sound, touch).

Questions
- [ ] Which senses are in play (vision, sound cues, vibration, materials)? What should each communicate?
- [ ] Where does the eye go first? Is that strategically important? Does the eye flow smoothly and get a
      guided tour of relevant options, or bounce among competing elements?
- [ ] Does the visual design reinforce the structure (sections distinct, options clear) and the brand
      identity from strategy?
- [ ] Is contrast used to mark what matters (including error messages) and to show groupings? Are all
      differences large enough to read as intentional? Any near-duplicates? Any overuse into clutter?
- [ ] Are element sizes uniform; is there a grid; is placement consistent? Is the grid still working on
      current devices and features, or has it become a straitjacket?
- [ ] Internal consistency: recurring elements designed once and verified in every context? Do they form
      a system?
- [ ] External consistency: matches the organization's other products and media at every level?
- [ ] Palette: brand colors inside a complementary set; bold foreground, muted background; shades
      distinguishable and each used one way?
- [ ] Type: simple faces for body text; personality only in large text/labels; a handful of fonts; new
      styles only for new kinds of information?
- [ ] Design comps map one-to-one to wireframe components and preserve importance and grouping?
- [ ] Style guide: grid, palette, typography, logo rules, section standards, element standards, with
      reasons; owned and enforced?

Deliverables
- Design comps for the standard screens.
- Style guide (global standards first, then section/function, then element level).
- Color palette and type specification.

Pass test: a non-designer can look at a page, name the first thing they see, and it is the element the
strategy most needs them to see; two people can build new screens from the style guide that look like
siblings.

## 6. Cross-plane audit (ch. 2, 8)

Run after the per-plane pass:
- [ ] Trace three persona scenarios top to bottom: does each plane's decision honor the plane below?
- [ ] For every change proposed on an upper plane, list the lower-plane assumptions it depends on; for
      every lower-plane change, list the upper-plane work it invalidates.
- [ ] Any "out of bounds" choice (an upper-plane option the lower plane didn't allow)? Re-decide below.
- [ ] Are strategy, scope and structure tasks being cut from the schedule because they produce no
      visible artifact? Restore them; they're the foundation.
- [ ] Is user evaluation happening throughout, or only as end-stage "acceptance"?
- [ ] Does the team pace like a marathon (push, then pull back to test and refine)?

## 7. Minimal versions for small teams (ch. 3, 6, 8)

The book stresses mindset over headcount; adapt the artifacts, not the questions:
- Strategy: one page with the two answers, three metrics, two personas built from logs, feedback
  messages and conversations with support staff.
- Scope: a single prioritized list with owner, release and a one-line falsifiable statement per item.
- Structure: a whiteboard diagram photographed; a one-page vocabulary list.
- Skeleton: pencil wireframes with sticky notes when designer and developer sit together.
- Surface: a palette, two or three fonts, and a growing style page; squint tests with co-workers.
