---
name: ux-five-planes
description: >
  Plan, audit, or diagnose any product/site/app with Jesse James Garrett's five-plane model of user
  experience (strategy, scope, structure, skeleton, surface), from "The Elements of User Experience"
  (2nd ed.). Use it whenever someone wants to: start a product or redesign "the right way"; write product
  objectives, success metrics, personas, user segments or a strategy/vision document; write or review
  functional specifications and content requirements; prioritize or cut features / fight scope creep;
  design information architecture (categories, hierarchy vs matrix vs organic vs sequential, controlled
  vocabulary, metadata, facets); design interaction flows, conceptual models and error handling; plan
  navigation (global/local/supplementary/contextual/courtesy, site maps, indexes) and wayfinding;
  produce or critique wireframes, design comps or a style guide; judge a visual design by "where does
  the eye go first", contrast, uniformity, grids, color palettes and typography; or figure out WHICH
  layer a UX complaint really lives on ("the button is wrong" - surface, skeleton or structure?).
  Also triggers on phrasings like "UX audit", "UX review", "why does this product feel confusing",
  "help me structure this site", "what should go in our spec", "is this requirement good",
  "what research should we do", "our project keeps slipping / perpetual beta", "we jumped straight to
  visual design", or any request to plan a product from scratch, even if the book is never named.
---

# UX Five Planes (Garrett, *The Elements of User Experience*, 2nd ed.)

This skill gives you Garrett's framework for making every aspect of a user's experience the result of
a conscious, explicit decision instead of an accident. The thesis, operationally: a product is built on
five planes that go from abstract to concrete, **strategy -> scope -> structure -> skeleton -> surface**,
each plane depending on the one below it. Every plane has two faces: the product as **functionality**
(tasks, tools, steps) and the product as **information** (finding, absorbing, making sense). Problems,
decisions and deliverables belong to a specific plane; most UX failures come from skipping the lower,
invisible planes (strategy, scope, structure) and from decisions nobody can justify with "why did we do
it that way?". The book is explicitly "not a book of answers" but a book about asking the right
questions, so this skill is strongest as a question engine, audit frame and planning scaffold.

## Workflow

Use this sequence whether you are planning something new or auditing something existing.

1. **Locate the problem on a plane.** Before proposing anything, ask which plane the issue lives on
   (ch. 8 "big purple button": is it the size/color = surface, the position = skeleton, or that the
   function does not do what users expect = structure?). Fixing the wrong plane wastes the fix.
2. **Check the foundation below it.** Each plane constrains the one above; a decision that is "out of
   bounds" on an upper plane forces rework below (ch. 2 ripple effect). If strategy is unstated, no
   amount of surface polish will hold. Ask for the two root questions: *What do we want to get out of
   this product? What do our users want to get out of it?* (ch. 3)
3. **Work the plane with its own elements and deliverables** (see table below and
   `references/planes-checklist.md`). Keep the functionality side and the information side both in view;
   most products are hybrids (ch. 2).
4. **Trace consequences up and down.** Every choice ripples: a navigation scheme that works in one
   section may fail in another; an innovative wizard may fail technophobic users (ch. 8).
5. **Schedule by the ripple rule:** work on a plane may *start* before the plane below is finished, but
   it must not *finish* before the plane below has finished. Don't build the roof before you know the
   shape of the foundation; don't treat lower-plane decisions as set in stone either (ch. 2).
6. **Justify.** For every decision be able to answer "Why did you do it that way?" with reference to
   product objectives, user needs, research, convention or an explicit trade-off (ch. 8).

| Plane | Functionality side | Information side | Core question | Main deliverables |
|---|---|---|---|---|
| Strategy | Product objectives + user needs (shared) | same | Why are we making this? | Strategy/vision document, success metrics, segments, personas |
| Scope | Functional specifications | Content requirements | What are we going to make? | Requirements list (prioritized), content inventory |
| Structure | Interaction design | Information architecture | How do the pieces fit together? | Architecture diagram, conceptual models, error-handling plan, controlled vocabulary/metadata |
| Skeleton | Interface design + information design | Navigation design + information design | What form does it take on the page? | Wireframes, navigation specs |
| Surface | Sensory (visual) design | same | How does it reach the senses? | Design comps, style guide |

## Core rules

Strategy (ch. 3)
1. Write product objectives explicitly; most failures trace to never answering the two root questions.
2. Objectives sit between "make money" (too general) and "build a real-time chat tool" (a solution, too specific): define conditions for success without defining the path.
3. Treat brand identity (conceptual associations, emotional reactions) as an explicit objective; the impression forms anyway, by accident or by choice.
4. Define success metrics you can track after launch and that are tied to user behavior your design shapes; never read a metric in isolation (competitor campaigns, bad press, marketing all move it).
5. Create only as many user segments as there are distinct sets of needs; split or merge segments after research.
6. When segments' needs conflict (novices want step-by-step, experts want one unified fast interface), choose: serve one segment, or build two paths. Decide this at strategy, because it ripples everywhere.
7. Pick research by what you need: surveys/interviews/focus groups for attitudes; user tests/field studies for behavior; contextual inquiry for depth (expensive); task analysis for precise steps; card sorting for how users group content. More time per user = more depth, fewer users.
8. Usability is "the most universal user need of all"; usable beats feature-rich.
9. Turn research into personas (name, photo, quote, age, occupation, family, income, technical profile, hours online, favourite sites) and use them as a test: "Would this work for Janet?"
10. Write a concise strategy document and give the whole team access; a locked-away strategy is the worst outcome. Let strategy evolve systematically, but not as a moving target.

Scope (ch. 4)
11. Define requirements so you know what you ARE building and what you are NOT building (now); stockpile out-of-scope ideas for the next release instead of letting the snowball roll.
12. "Documentation won't solve your problems. Definition will." Keep specs lightweight: clarity and accuracy, not volume; record decisions made, not an idealized future.
13. Write every requirement positive ("will direct the user to the kite-string page if..."), specific ("videos with the most views in the last week appear at the top"), falsifiable ("conforms to the branding guidelines document", not "hip and flashy"), and quantified where possible ("supports at least 1,000 simultaneous users").
14. Expect three kinds of stakeholder input: what they say they want, what they say but don't actually want (symptom-level solutions; dig for the real need), and what they don't know they want (brainstorm from objectives, cross-functional).
15. Content and functionality each imply the other: error messages and on-screen instructions are content requirements (otherwise "Null input field exception" ships); content needs CMS/workflow functionality.
16. For each content feature record: purpose (not just format; "FAQ" is a format), content types, rough size (word count, pixel dimensions, file size), owner, update frequency, intended audience. Content is hard work and needs constant maintenance.
17. Prioritize by fit to product objectives + user needs + feasibility (technical, resources, time). Resolve feature fights by appealing to strategic goals, not means; if you keep revisiting strategy, you started requirements too early.

Structure (ch. 5)
18. Pick a conceptual model (container "shopping cart", catalog order form...) and apply it consistently; users need not be told it, and metaphors taken literally fail (Southwest's picture of a service desk, Slate's page-turning magazine).
19. Stick to a convention (retail-store cart) when users use it elsewhere; break it only with a good reason and a model users can interpret correctly.
20. Error handling in layers: make errors impossible > make them difficult > help users notice and fix > let them recover (undo) > warn before unrecoverable actions. Too many "Are you sure?" dialogs bury the important one; auto-correction that users must undo is worse than none.
21. Build IA both top-down (from objectives and needs) and bottom-up (from actual content); either alone fails (overlooks content details / too fitted to today's content).
22. Judge a structure by whether each step makes sense and follows naturally, not by click count: users prefer a clear seven-step process to a confusing three-step one.
23. Choose the structure class on purpose: hierarchical (default, most common), matrix (several browse dimensions; more than three breaks as primary navigation), organic (exploration; weak sense of place), sequential (small-scale articles, instructional material).
24. Organizing principles at the top follow objectives and user needs (audience, geography, chronology); at lower levels follow the content. Choose the facets foremost in users' minds; exposing every facet is worse than none.
25. Use the users' language, enforced by a controlled vocabulary (and a thesaurus mapping jargon/slang/acronyms to approved terms); consistent metadata makes new sections, automated linking and smarter search possible.
26. Document structure with an architecture diagram of conceptual relationships, not every link.

Skeleton (ch. 6)
27. Sort each problem first: ability to DO things = interface design; ability to GO places = navigation design; COMMUNICATING ideas = information design. Good navigation cannot rescue bad information design.
28. Be cautious about deviating from convention (nonstandard phone keypad: ~3 frustrating seconds per call); deviate only for clear benefit; internal consistency outranks consistency with other products.
29. Make the likely actions easiest and the unimportant ones less visible or absent; do not weight edge cases like the majority. Set smart defaults; remember last choices when feasible.
30. Choose controls by trade-off, not habit: dropdowns save space but hide options; with six choices, checkboxes/radios may be better.
31. Navigation must simultaneously: get users from A to B, show how its items relate to each other, and show how they relate to the current page. Assume users carry no knowledge page to page (any page can be an entry point).
32. Provide layered navigation: global, local, supplementary, contextual/inline, courtesy, plus remote tools (site map: at most two levels; index only for large diverse content).
33. Wayfinding = navigation + non-navigational cues (color coding, icons, labels, typography); color coding never stands alone.
34. Wireframe the small set of standard screens, annotated with pointers to the architecture diagram and requirements; UX and visual designers build it together; use the lightest documentation that still works (sketches for a co-located pair, formal for a remote team).

Surface (ch. 7)
35. Judge visual design by how well it supports the lower planes, not by taste; a technical, authoritative brand is not comic fonts and pastels.
36. Follow the eye: where does it go first? Is that strategically important? A good design gives a smooth flow and a guided tour; "busy"/"cluttered" means the eye bounces.
37. Contrast is the tool for attention and grouping; differences must be big enough to read as intentional (similar-but-not-same confuses). Error messages need contrast (e.g. red).
38. Uniformity via consistent element sizes and a grid; revisit the grid when it stops working rather than wearing a straitjacket.
39. Design each recurring element once, test it in every context, rework; keep internal and external (cross-media brand) consistency.
40. Palette: bold colors foreground, muted background; distinguishable shades used consistently. Type: simple faces for body text, personality only for large text/labels, a handful of fonts, different styles only for different information.
41. Design comp maps one-to-one onto wireframe components (not necessarily the same layout); the style guide records grids, palette, type, logo rules down to individual elements so the organization does not get "amnesia".

Process (ch. 8)
42. Beware the three unconscious design modes: by default (UX mirrors the database or org chart), by mimicry (copying conventions regardless of fit), by fiat (the SVP likes orange).
43. Testing is never a substitute for design; evaluation tacked on at the end ("user acceptance testing") finds problems too late to fix. Users cannot articulate their needs; understand them better than they do.
44. Run a marathon, not a sprint: push (prototype, generate) then pull back (test, refine); strategy/scope/structure are the first tasks cut when late and the most important ones.

## When to read which reference

| Task | Read |
|---|---|
| Plan a new product / redesign end-to-end; audit an existing product plane by plane | `references/planes-checklist.md` (question lists + deliverables per plane) |
| Need a definition, the author's reasoning, or pitfalls for a concept | `references/principles.md` (indexed by plane) |
| Write objectives, metrics, segments, personas, a strategy doc | `references/playbook.md` sections 1-4 |
| Write/review requirements, specs, content requirements; prioritize; fight scope creep | `references/playbook.md` sections 5-8; `principles.md` Scope |
| Design or review IA, conceptual models, error handling, vocabulary/metadata, diagrams | `references/playbook.md` sections 9-13; `principles.md` Structure |
| Design or review navigation, interface controls, information grouping, wireframes | `references/playbook.md` sections 14-18; `principles.md` Skeleton |
| Review visual design, build palette/type system, comps, style guide | `references/playbook.md` sections 19-22; `principles.md` Surface |
| Diagnose "which plane is this problem on?", run a user test well, fix the process | `references/playbook.md` sections 23-25 |
| Want the concrete cases (kite string spec, Southwest, Slate, phone keypad, car-weight facets...) | `references/examples.md` |
| Need the author's precise term for something | `references/glossary.md` |
| Verify a claim against the book | `references/chapter-map.md` |

## Anti-patterns the author calls out

- Starting without explicit product objectives and user needs; "most common reason sites fail" (ch. 3).
- Objectives stated as solutions ("provide a real-time text tool"), or as vague money goals (ch. 3).
- Designing for "one idealized user, someone exactly like us" (ch. 3).
- Gaming a metric against users (extra navigation layers to inflate ad impressions) (ch. 3).
- Hoarding the strategy document from the team (ch. 3).
- "Perpetual beta": refusing to write requirements because everyone shares an office; the Telephone game; everyone assumes someone else owns a crucial piece (ch. 4).
- Scope creep snowball; feature champions negotiating by politics instead of strategy (ch. 4).
- Subjective, non-falsifiable, negative requirements ("hip, flashy", "will not allow") (ch. 4).
- Confusing content format with content purpose ("we need FAQs"); post-and-forget content; nobody assigned to own a content feature (ch. 4).
- Engineers' placeholder error messages shipping because nobody treated them as content (ch. 4).
- Designing for the machine's convenience; "computer literacy" as the fix for bad software (ch. 5).
- Mixed conceptual models (an element is a place sometimes, an object other times); literal metaphors (ch. 5).
- Over-correcting software (Word-style auto-fixes); confirmation-dialog fatigue (ch. 5).
- Counting clicks as the quality measure; exposing every facet; internal jargon in labels (ch. 5).
- Pure top-down or pure bottom-up IA (ch. 5).
- Deviating from convention without a clear benefit; cute metaphors (coffee shop = chat) (ch. 6).
- Giving edge cases equal weight with the main path; hiding important options in dropdowns (ch. 6).
- Hyperlink-stuffed text (contextual nav as clutter); site maps deeper than two levels (ch. 6).
- Documentation for its own sake, or fooling yourself you can get by with less than you need (ch. 6).
- Arguing visual design by taste; similar-but-not-quite-the-same treatments; grids worn as straitjackets; too many fonts (ch. 7).
- Design by default, mimicry or fiat; UX evaluation bolted on at the end; sprinting a marathon; cutting strategy/scope/structure to save time (ch. 8).
