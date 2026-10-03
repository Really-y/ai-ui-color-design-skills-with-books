---
name: atomic-design
description: >
  Interface design systems with Brad Frost's Atomic Design (2016). Use it whenever
  someone is scoping, building, documenting, or maintaining a UI component system:
  "design system not pages", "atoms molecules organisms templates pages", "interface
  inventory / audit", "pattern library / style guide", "Pattern Lab includes / data.json /
  pseudo-patterns", "sell a design system", "waterfall to collaborative workflow",
  "governance / makers and users / holy grail sync", "name patterns / lineage /
  viewport testing / annotations". Applies even when the book is not mentioned —
  any task about making UIs consistent, reusable, and maintainable across devices.
---

# Atomic Design — system thinking for interfaces

This skill gives you Brad Frost's working method: **we're not designing pages,
we're designing systems of components** (Stephen Hay). Operationally: scope work
by components not pages; build atoms → molecules → organisms → templates → pages
as a mental model (not a linear process); stitch them with DRY includes; separate
structure from content with JSON data; prove variations with pseudo-patterns; drive
the work with interface inventories and a collaborative browser-first workflow; and
maintain the system as a living product with makers, users, and governance.

Source fidelity: every rule below comes from *Atomic Design* (Brad Frost, 2016,
189 pp., 5 chapters). No mixing with Refactoring UI, Albers, Krug, Norman, or
Garrett. See `references/chapter-map.md` for chapter-to-skill mapping and what
was deliberately left out as filler.

## Workflow

Use the same loop whether you are starting a system, adding to one, or fixing one.

1. **Reframe from pages to system.** Translate "N pages / homepage / redesign"
   into content types + layouts + components. Estimate by patterns, never by page
   count (see `references/methodology.md` § scope).
2. **Audit what exists.** Run a 30–90 min interface inventory before designing
   anything new: screenshot by category, present 5–10 min per category, merge into
   one über-document, decide keep / merge / drop (see `references/playbook.md` §1).
3. **Name and classify atomically.** Sort every pattern into atom / molecule /
   organism / template / page. Names describe structure, never context or content
   ("card" not "homepage carousel", "product card" only if content truly constrains
   it). Blur content to test the name.
4. **Build DRY from the bottom up.** Atoms inside molecules inside organisms
   inside templates via includes (`{{> atoms-thumb }}`). One source of truth:
   change once, update everywhere. Keep molecules single-responsibility.
5. **Separate structure from content.** Define `data.json` defaults (grayscale FPO +
   character limits + image sizes), override per page JSON, articulate variations
   with pseudo-patterns (`dashboard~admin.json`, `isAdmin: true`). Design worst
   cases, not just Sara Smith best cases.
6. **Prove it in context.** Show templates (skeleton + content structure) then pages
   (real representative content). Test across the whole resolution spectrum
   (small-ish / medium-ish / large-ish, not 3 device widths). Attach lineage (what
   it contains + where it is used), code view, and living annotations.
7. **Ship collaboratively, maintain as product.** Browser-first, parallel
   disciplines, WIP reviews (sculpture, not waterfall). After launch: official team,
   governance, changelog/roadmap, training + support, public if possible. Never
   treat the library as an auxiliary side project.

Key questions to keep asking: *Is this scoped by components or by pages? What
level is this — atom, molecule, organism, template, or page? Does the name survive
if I move it or swap its content? What is its worst-case content? What contains it
and where is it used — what breaks if I change it? Is this a one-off or a second
use that earns a place in the system?*

## Core rules (atomic skills)

Each rule is one concrete ability. Chapter in parentheses.

Scope and strategy (ch. 1)
1. Translate any "N-page website / homepage estimate / 30,000-page redesign" into
   content types + layouts + pattern list before estimating.
2. Argue against bulldoze-and-replace redesigns with the Magic Escalator cost:
   propose MVP + iterative shipping instead.
3. Distinguish capital-A Agile (Scrum/Lean/manifesto) from lowercase-a agile;
   write down concretely "what we will be" (Harned) instead of "more agile".
4. Chunk content for COPE (Create Once, Publish Everywhere): structured,
   platform-agnostic chunks, not page-shaped copy (McGrane).
5. Establish design atmosphere without full comps: style tiles (Warren) for
   color/type/texture, element collages (Mall) for exploded components.
6. Decide framework vs custom deliberately: list Bootstrap/Foundation speed
   gains (tested patterns, fast prototype, community) against sameness,
   unused weight, and client-specific needs — default to "tiny Bootstrap per
   client" only when it fits.
7. Justify a style guide with six benefits: shared vocabulary, education
   (Debenham: "websites are systems"), empathetic cross-discipline hub, isolated
   testing, speed after upfront cost (Holgado/MailChimp), long-haul foundation
   that survives redesigns.

Methodology — the five stages (ch. 2, detail in `references/methodology.md`)
8. Classify atoms: indivisible HTML (label, input, button, h1, img) + their
   intrinsic properties (dimensions, font-size). Show them as base-styles
   reference; never present them as finished UI.
9. Compose molecules: 2+ atoms with one job (search form = label + input +
   button). Enforce single responsibility; testable, portable, droppable
   anywhere search is needed.
10. Compose organisms: molecules/atoms/organisms as distinct sections (header =
    logo + primary-nav + search; product grid = same molecule repeated). State
    whether heterogeneous (header) or homogeneous (grid).
11. Define templates: organisms/molecules placed in layout articulating content
    structure (image sizes, headline character lengths), not final content
    (Boulton: structure-first). Prove parts add to a functioning whole.
12. Instantiate pages: template + real representative content (Time Inc.
    homepage: Beyoncé hero "Moving People", not Lorem Ipsum FPO). Most concrete
    stage — what users see and stakeholders sign.
13. Traverse abstract↔concrete on demand: zoom out to pages/templates for
    context, zoom in to molecules/atoms to fix ("header's broken!").
14. Apply the method beyond marketing websites: same five stages for native apps
    (Instagram example), intranets, dashboards — "atomic design is for UIs".
15. Stop the chemistry analogy at organisms: switch to client-safe language
    (templates/pages) so stakeholders don't think you're crazy.

Pattern library mechanics (ch. 3, detail in `references/patternlab.md`)
16. State what Pattern Lab is / isn't: static-site generator + documentation +
    starter kit; NOT a UI framework, NOT language-dependent, NOT a CMS
    replacement. Output is backend-agnostic HTML/CSS/JS (PHP or Node engine).
17. Build with nesting-doll includes: `{{> atoms-logo }}`, `{{> molecules-search }}`,
    `{{> organisms-header }}`; name template instances with Mustache sections
    (`{{# factoid-advertising }}...{{/ factoid-advertising }}`) so content can
    latch on. Keep folders renamable — team-effective names beat canonical ones.
18. Separate data with `data.json` defaults → per-page override
    (`00-homepage.json` replaces hero Lorem Ipsum + FPO with real headline/image).
    Leverage four payoffs: DRY structure/content split, ad hoc CMS without
    MySQL, backend blueprint (static vs dynamic bits), non-devs edit copy/images
    without touching markup.
19. Articulate variations with pseudo-patterns: `dashboard~admin.json` inherits
    base + sets `"isAdmin": true` to conditionally render edit/delete actions.
    Always design empty / overflow / long-string / no-image / nested-comment
    states alongside the happy path.
20. Test fluidity across the spectrum with ish-style resizing (small-ish /
    medium-ish / large-ish randomized), not 320/480/768 device widths; use it to
    teach stakeholders device-agnosticism. Aim patterns at containers
    (container-query mindset), not viewports.
21. Expose the right code view: HTML always; template include always
    (`{{> molecules-block-post }}`); CSS/JS per team need; holy-grail teams
    expose only the include (Rizzo model) as single source of truth.
22. Document alive, not in PDFs: per-pattern Markdown description + interactive
    numbered annotations pinned to the living UI (accessibility, performance,
    rationale in context).
23. Publish lineage for every pattern: lists what it contains (media-block →
    atoms-square + molecules-button-bar) and where it is used (→ media-block-list
    organism). Use it to scope QA/retest and to weed redundant/underused patterns.
24. Vet any pattern-library tool against six qualities: descriptions+annotations,
    relevant code, full-spectrum viewport, variations, dynamic real content,
    lineage/context. Tool serves principles — never the reverse.

Workflow — people and process (ch. 4, steps in `references/playbook.md`)
25. Start now with a pilot: "when to establish a system? Now." Pick one suitable
    project; don't wait for permission or perfect timing.
26. Pitch in stakeholder language: frame as time + money saved (not craft purity);
    then show-don't-tell with an interface inventory über-document (37 button
    styles beat 100 slides).
27. Conduct a 5-step interface inventory: (1) round up cross-disciplinary troops,
    (2) standardize capture tool (same software, Slides canvas), assign UI
    categories (buttons, forms, nav, media, tables, feedback), (3) 30–90 min
    screenshot sprint of everything incl. 404/FAQ/legal/sizing charts, (4) 5–10
    min/category present + surface naming collisions ("utility bar" vs "admin
    nav"), merge into über-doc, (5) small working group decides keep/merge/drop,
    names, and path to living library.
28. When blocked, ask forgiveness not permission: bake the system by default like
    performance/a11y/responsiveness (Lego organized-pile vs rummage-pile, Nagel).
    Show progress on the whole while organizing the parts; reveal the system
    after on-time/on-budget delivery if you must.
29. Reset expectations explicitly: expand "design" beyond aesthetics to accessible
    + resilient, flexible layouts, performance-as-design, progressive enhancement,
    future-friendly. Use Mall's line ("selling paintings vs access") and the
    3-image device-explosion story (desktop-only → today's potpourri → tomorrow's
    unknown).
30. Kill the waterfall: replace sequential UX→visual→frontend handoff + giant PDF
    signoff with parallel wax-and-wane collaboration where every discipline
    consults throughout. Name the failure mode ("looks fantastic, but… pops")
    when you see signoff theater.
31. Treat front-end as design: get into HTML/CSS/presentational JS early to
    confront flexibility, network, interaction, motion, ergonomics, rendering,
    pixel density, scroll perf, quirks, user preferences — not just pictures of
    websites. Pair static atmosphere sketches with working browser prototypes.
32. Iterate like subtractive sculpture: broad passes → detail face, then arms,
    then legs, stepping back each time; normalize WIP reviews and undo. Call out
    Gantt-chart false precision; substitute honest conversation + tight loops.
33. Establish content/display patterns lo-fi first: bulleted IA + grayscale
    mobile-first blocks ("right things? right order?"), gestural site-wide
    patterns (TechCrunch "featured island" without layout/function assumptions),
    or a spreadsheet (pattern | content | order | role on screen).
34. Establish visual direction cheaply: 20-second gut test (20–30 sites incl.
    non-industry + client logo swapped in, 1=quit-and-cry to 10=ecstatic on
    type/color/density/illustration/vibe, discuss top-5/bottom-5), then tiles/
    collages — never 10 full comps to "see what sticks".
35. Redefine comps as hypotheses: static tools for atmosphere, browser for
    decisions; decide responsive behavior, states, and motion where they live.

Maintenance — make it last (ch. 5, detail in `references/playbook.md` §3)
36. Think product not artifact (Curtis): shift from "sites/apps are the job,
    library is docs" to "system underpins products". Apply friendly friction —
    fix the dropdown globally when one instance underperforms, don't hotfix one
    page and let the system erode.
37. Make it official in three moves: (1) make a thing (weekend pilot packaged for
    show), (2) show it's useful (time/money + cross-discipline testimonials +
    scaled vision), (3) get sanction (people + budget + governance + roadmap).
    If refused, keep growing grassroots until value is undeniable.
38. Separate makers from users (Bolton: "system informs product, product informs
    system"): makers govern/create (Salesforce dozen FTE at scale; senior staff
    wearing the hat at small orgs; consultants teach-to-fish), users apply/report.
    Staff hands (UX/visual/frontend) vs advisors (backend/exec/users) explicitly.
39. Govern for change: answer nine questions up front (when to modify vs swap vs
    create, new-pattern requests, retirement, bugs, approver, docs owner, who
    codes, deploy to apps, announce). Hold state-of-the-union reviews; keep
    Slack/Yammer/office-hours/bug-tracker doors open.
40. Handle the three pattern changes correctly: modify (feature/bug/visual/perf/
    a11y/refactor — keep fresh, no Web-2.0 bevels), add (assume one-off until a
    second app says "I want that!", follow Vanilla-style decision tree), remove
    (deprecate with warning + alternative — Sass Deprecate model — never rug-pull).
41. Chase the holy grail: library and production in sync so one change updates
    both (Rizzo/Twig/Drupal bridges, Phase2 Starter 8). Until then, minimize
    update friction or neglect (Schleifer) kills the system.
42. Make it cross-disciplinary + approachable + visible + bigger: carousel test
    (business/editorial/copy/art/UX/frontend/backend all shape it — house their
    concerns in one pattern page); attractive navigable home (Yelp model: what /
    who / how); evangelize early (blog/Yammer), communicate change (changelog,
    roadmap, success stories, tips where teams hang out + auto PR→Slack alerts),
    train (pair/workshop/webinar/tutorial/onboarding) + support (JIRA/GitHub
    issues, office hours, chat, forum, proactive outreach + PRs/interviews/
    feedback-requests/surveys/state-of-union); go public (accountability +
    recruiting Bat-Signal — Bolton joined Salesforce for its style guide);
    co-house brand/voice/code/principles/writing + native iOS/Android alongside
    web (Harmony model).
43. Name context-agnostic, show contextual: call it "carousel"/"card" not
    "homepage carousel"/"product card"; blur content to name structure; then
    demonstrate usage with photos/videos (Material model) + lineage paper trail
    for QA. End state checklist: official, adaptable, maintainable,
    cross-disciplinary, approachable, visible, bigger, agnostic, contextual,
    lasting — wine, not used car.

## When to read which reference

| Task | Read |
|---|---|
| Need the five stages with book examples and level tests | `references/methodology.md` |
| Need Pattern Lab mechanics: includes, data.json, pseudo-patterns, ish, code, annotations, lineage | `references/patternlab.md` |
| Need step-by-step: interface inventory, lo-fi direction, gut test, governance, 10 makes | `references/playbook.md` |
| Need principles distilled by chapter with pitfalls | `references/principles.md` |
| Need concrete book cases to cite or copy | `references/examples.md` |
| Need chapter→skill map, coverage proof, filler list | `references/chapter-map.md` |
| Need terms (atom..page, COPE, lineage, pseudo-pattern, holy grail, makers/users) | `references/glossary.md` |
| Quick decision: tool vetting, naming, variation, maintenance | SKILL.md core rules 24, 39–43 |

## Anti-patterns Frost calls out

- Scoping/estimating by pages; "how long will the homepage take?" without asking
  what's on it; 30,000 pages as difficulty signal (ch. 1).
- Bulldoze-and-replace redesigns; set-it-and-forget-it Ron Popeil sites;
  New-And-Shiny → Old-And-Crusty without process change (ch. 1, 5).
- "More agile" with no definition; capital-A ceremony without lowercase-a behaviors (ch. 1).
- Page-shaped content; desktop-only publishing; grayscale Lorem Ipsum presented
  as final (ch. 1–3).
- Full comps for every page; Photoshop-as-truth (Hay); comps implying unbuilt
  features; signoff theater then "make it pop" (ch. 1, 4).
- Framework defaultism: Bootstrap-everywhere sameness, jumpsuit future; or
  framework puritanism ("never use frameworks") without discernment (ch. 1).
- Auxiliary-project pattern library; nice-to-have that dies first under pressure;
  accessibility/perf/responsiveness as extra line items (ch. 1, 4).
- Pattern library as loosely arranged spray of modules with no methodology;
  no context/lineage (where used? what breaks?) (ch. 1, 3).
- Best-case-only design (Sara Smith, equal columns, full profiles); ignoring
  empty/overflow/long/no-image/nested states (ch. 3).
- Device-width testing (320/480/768) instead of spectrum; viewport-fixed
  components instead of fluid/container-aware (ch. 3).
- PDF spec docs as documentation; annotations divorced from living UI (ch. 3).
- Waterfall handoffs, designer→developer floors/buildings apart, frontend as
  "middleware/database" engineering; static pictures shown to stakeholders as
  the design (ch. 4).
- Organizing nothing (rummage-pile Lego) while staring only at the whole (ch. 4).
- Context/content-bound names ("homepage carousel", "product card" for any block);
  inconsistent labels per discipline never reconciled (ch. 4–5).
- One-off hotfixes eroding the system; custom dropdown fixed on one page while
  rotting everywhere else (ch. 5).
- Rigid unchangeable system (handcuffs → shadow systems); or Wild West
  (every whim = new pattern, bloat); rug-pull deprecation without warning (ch. 5).
- Hidden intranet library, no changelog/roadmap/training/support, makers as
  support bottleneck, users as dumb consumers (ch. 5).
